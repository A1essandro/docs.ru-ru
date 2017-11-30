---
title: "Реализация повторные попытки вызова HTTP с экспоненциально растущим с Polly"
description: "Архитектура Микрослужбами .NET для приложений .NET в контейнерах | Реализация повторные попытки вызова HTTP с экспоненциально растущим с Polly"
keywords: "Docker, микрослужбы, ASP.NET, контейнер"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: 1ed48142546403ea710f4c132e038521232c20ed
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="implementing-http-call-retries-with-exponential-backoff-with-polly"></a><span data-ttu-id="368c7-104">Реализация повторные попытки вызова HTTP с экспоненциально растущим с Polly</span><span class="sxs-lookup"><span data-stu-id="368c7-104">Implementing HTTP call retries with exponential backoff with Polly</span></span>

<span data-ttu-id="368c7-105">Для повторных попыток с экспоненциально растущим рекомендуется пользоваться преимуществами более сложных библиотек .NET, как открыть источник [Polly](https://github.com/App-vNext/Polly) библиотеки.</span><span class="sxs-lookup"><span data-stu-id="368c7-105">The recommended approach for retries with exponential backoff is to take advantage of more advanced .NET libraries like the open source [Polly](https://github.com/App-vNext/Polly) library.</span></span>

<span data-ttu-id="368c7-106">Polly — это библиотека .NET, которая предоставляет возможности обработки временных сбоев и устойчивости.</span><span class="sxs-lookup"><span data-stu-id="368c7-106">Polly is a .NET library that provides resilience and transient-fault handling capabilities.</span></span> <span data-ttu-id="368c7-107">Можно реализовать эти возможности легко путем применения Polly политики, такие как "Повторить", Размыкатель цепи, блочный изоляции, время ожидания и Fallback.</span><span class="sxs-lookup"><span data-stu-id="368c7-107">You can implement those capabilities easily by applying Polly policies such as Retry, Circuit Breaker, Bulkhead Isolation, Timeout, and Fallback.</span></span> <span data-ttu-id="368c7-108">Polly обращается .NET 4.x и .NET Standard версии 1.0 (который поддерживает .NET Core).</span><span class="sxs-lookup"><span data-stu-id="368c7-108">Polly targets .NET 4.x and the .NET Standard version 1.0 (which supports .NET Core).</span></span>

<span data-ttu-id="368c7-109">Политика повтора в Polly именно этот подход используется в eShopOnContainers при реализации HTTP повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="368c7-109">The Retry policy in Polly is the approach used in eShopOnContainers when implementing HTTP retries.</span></span> <span data-ttu-id="368c7-110">Можно реализовать интерфейс, поэтому можно ввести стандартных функциональных возможностей HttpClient или более устойчивым версии HttpClient, с помощью Polly, в зависимости от конфигурации политик повторных попыток, которые вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="368c7-110">You can implement an interface so you can inject either standard HttpClient functionality or a resilient version of HttpClient using Polly, depending on what retry policy configuration you want to use.</span></span>

<span data-ttu-id="368c7-111">В следующем примере показано интерфейс, реализованный в eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="368c7-111">The following example shows the interface implemented in eShopOnContainers.</span></span>

```csharp
public interface IHttpClient
{
    Task<string> GetStringAsync(string uri, string authorizationToken = null,
        string authorizationMethod = "Bearer");
        Task<HttpResponseMessage> PostAsync<T>(string uri, T item,
        string authorizationToken = null, string requestId = null,
        string authorizationMethod = "Bearer");

    Task<HttpResponseMessage> DeleteAsync(string uri,
        string authorizationToken = null, string requestId = null,
        string authorizationMethod = "Bearer");

    // Other methods ...
}
```

<span data-ttu-id="368c7-112">Если не хотите использовать устойчивым механизм, как при разработке или тестирования проще подходов можно использовать стандартную реализацию.</span><span class="sxs-lookup"><span data-stu-id="368c7-112">You can use the standard implementation if you do not want to use a resilient mechanism, as when you are developing or testing simpler approaches.</span></span> <span data-ttu-id="368c7-113">В следующем коде показано Стандартная HttpClient реализацию разрешает запросы с маркерами безопасности как дополнительный вариант.</span><span class="sxs-lookup"><span data-stu-id="368c7-113">The following code shows the standard HttpClient implementation allowing requests with authentication tokens as an optional case.</span></span>

```csharp
public class StandardHttpClient : IHttpClient
{
    private HttpClient _client;
    private ILogger<StandardHttpClient> _logger;

    public StandardHttpClient(ILogger<StandardHttpClient> logger)
    {
        _client = new HttpClient();
        _logger = logger;
    }

    public async Task<string> GetStringAsync(string uri,
        string authorizationToken = null,
        string authorizationMethod = "Bearer")
    {
        var requestMessage = new HttpRequestMessage(HttpMethod.Get, uri);
        if (authorizationToken != null)
        {
            requestMessage.Headers.Authorization =
                new AuthenticationHeaderValue(authorizationMethod, authorizationToken);
        }
        var response = await _client.SendAsync(requestMessage);
        return await response.Content.ReadAsStringAsync();
    }

    public async Task<HttpResponseMessage> PostAsync<T>(string uri, T item,
        string authorizationToken = null, string requestId = null,
        string authorizationMethod = "Bearer")
    {
        // Rest of the code and other Http methods ...
```

<span data-ttu-id="368c7-114">Интересные реализуется кода класса другой, похожий, но с использованием Polly для реализации гибкой механизмов, которые вы хотите использовать — в следующем примере повторных попыток с экспоненциально растущим.</span><span class="sxs-lookup"><span data-stu-id="368c7-114">The interesting implementation is to code another, similar class, but using Polly to implement the resilient mechanisms you want to use—in the following example, retries with exponential backoff.</span></span>

```csharp
public class ResilientHttpClient : IHttpClient
{
    private HttpClient _client;
    private PolicyWrap _policyWrapper;
    private ILogger<ResilientHttpClient> _logger;

    public ResilientHttpClient(Policy[] policies,
        ILogger<ResilientHttpClient> logger)
    {
        _client = new HttpClient();
        _logger = logger;
        // Add Policies to be applied
        _policyWrapper = Policy.WrapAsync(policies);
    }

    private Task<T> HttpInvoker<T>(Func<Task<T>> action)
    {
        // Executes the action applying all
        // the policies defined in the wrapper
        return _policyWrapper.ExecuteAsync(() => action());
    }

    public Task<string> GetStringAsync(string uri,
        string authorizationToken = null,
        string authorizationMethod = "Bearer")
    {
        return HttpInvoker(async () =>
        {
            var requestMessage = new HttpRequestMessage(HttpMethod.Get, uri);
            // The Token's related code eliminated for clarity in code snippet
            var response = await _client.SendAsync(requestMessage);
            return await response.Content.ReadAsStringAsync();
        });
    }
    // Other Http methods executed through HttpInvoker so it applies Polly policies
    // ...
}
```

<span data-ttu-id="368c7-115">Polly определять политику повторов с числом повторов, экспоненциально растущим конфигурации и действия, выполняемые при возникновении исключения HTTP, например, ведение журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="368c7-115">With Polly, you define a Retry policy with the number of retries, the exponential backoff configuration, and the actions to take when there is an HTTP exception, such as logging the error.</span></span> <span data-ttu-id="368c7-116">В этом случае политика настроена, будет предпринята попытка количество времени, указанного при регистрации типов в контейнер IoC.</span><span class="sxs-lookup"><span data-stu-id="368c7-116">In this case, the policy is configured so it will try the number of times specified when registering the types in the IoC container.</span></span> <span data-ttu-id="368c7-117">Из-за конфигурации экспоненциально растущим всякий раз, когда код обнаруживает исключение HttpRequest повторяет HTTP-запроса после ожидания за период времени, растет в геометрической прогрессии в зависимости от настроек политики.</span><span class="sxs-lookup"><span data-stu-id="368c7-117">Because of the exponential backoff configuration, whenever the code detects an HttpRequest exception, it retries the Http request after waiting an amount of time that increases exponentially depending on how the policy was configured.</span></span>

<span data-ttu-id="368c7-118">Важный метод — HttpInvoker, который указывает, что HTTP-запросы по всему служебный класс.</span><span class="sxs-lookup"><span data-stu-id="368c7-118">The important method is HttpInvoker, which is what makes HTTP requests throughout this utility class.</span></span> <span data-ttu-id="368c7-119">Внутренне выполняется HTTP-запрос с метод \_policyWrapper.ExecuteAsync, который учитывает политику повтора.</span><span class="sxs-lookup"><span data-stu-id="368c7-119">That method internally executes the HTTP request with \_policyWrapper.ExecuteAsync, which takes into account the retry policy.</span></span>

<span data-ttu-id="368c7-120">В eShopOnContainers при регистрации типов на контейнер IoC, как показано в следующем коде из указываются политики Polly [веб-приложение MVC в файле startup.cs](https://github.com/dotnet-architecture/eShopOnContainers/blob/master/src/Web/WebMVC/Startup.cs) класса.</span><span class="sxs-lookup"><span data-stu-id="368c7-120">In eShopOnContainers you specify Polly policies when registering the types at the IoC container, as in the following code from the [MVC web app at the startup.cs](https://github.com/dotnet-architecture/eShopOnContainers/blob/master/src/Web/WebMVC/Startup.cs) class.</span></span>

```csharp
// Startup.cs class
if (Configuration.GetValue<string>("UseResilientHttp") == bool.TrueString)
{
    services.AddTransient<IResilientHttpClientFactory,
        ResilientHttpClientFactory>();
    services.AddSingleton<IHttpClient,
        ResilientHttpClient>(sp =>
            sp.GetService<IResilientHttpClientFactory>().
            CreateResilientHttpClient());
}
else
{
    services.AddSingleton<IHttpClient, StandardHttpClient>();
}
```

<span data-ttu-id="368c7-121">Обратите внимание, что, чтобы подключения TCP эффективно используются службы как singleton, а не как временной создаются экземпляры объектов IHttpClient и [проблему с помощью сокетов](https://aspnetmonsters.com/2016/08/2016-08-27-httpclientwrong/) не произойдет.</span><span class="sxs-lookup"><span data-stu-id="368c7-121">Note that the IHttpClient objects are instantiated as singleton instead of as transient so that TCP connections are used efficiently by the service and [an issue with sockets](https://aspnetmonsters.com/2016/08/2016-08-27-httpclientwrong/) will not occur.</span></span>

<span data-ttu-id="368c7-122">Однако важно об устойчивости, применить политику Polly WaitAndRetryAsync в ResilientHttpClientFactory в методе CreateResilientHttpClient, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="368c7-122">But the important point about resiliency is that you apply the Polly WaitAndRetryAsync policy within ResilientHttpClientFactory in the CreateResilientHttpClient method, as shown in the following code:</span></span>

```csharp
public ResilientHttpClient CreateResilientHttpClient()
    => new ResilientHttpClient(CreatePolicies(), _logger);

// Other code
private Policy[] CreatePolicies()
    => new Policy[]
    {
        Policy.Handle<HttpRequestException>()
            .WaitAndRetryAsync(
        // number of retries
        6,
        // exponential backoff
        retryAttempt => TimeSpan.FromSeconds(Math.Pow(2, retryAttempt)),
        // on retry
        (exception, timeSpan, retryCount, context) =>
        {
            var msg = $"Retry {retryCount} implemented with Pollys RetryPolicy " +
            $"of {context.PolicyKey} " +
            $"at {context.ExecutionKey}, " +
            $"due to: {exception}.";
            _logger.LogWarning(msg);
            _logger.LogDebug(msg);
        }),
    }
```


>[!div class="step-by-step"]
<span data-ttu-id="368c7-123">[Предыдущие] (implement-custom-http-call-retries-exponential-backoff.md) [Далее] (реализуйте канал выключатель pattern.md)</span><span class="sxs-lookup"><span data-stu-id="368c7-123">[Previous] (implement-custom-http-call-retries-exponential-backoff.md) [Next] (implement-circuit-breaker-pattern.md)</span></span>
