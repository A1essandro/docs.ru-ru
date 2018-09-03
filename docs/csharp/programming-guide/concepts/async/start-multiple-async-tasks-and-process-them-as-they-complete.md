---
title: Запуск нескольких асинхронных задач и их обработка по мере завершения (C#)
ms.date: 07/20/2015
ms.assetid: 25331850-35a7-43b3-ab76-3908e4346b9d
ms.openlocfilehash: d59b65e456c528c63c79c97f6c75c328066be631
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2018
ms.locfileid: "43416402"
---
# <a name="start-multiple-async-tasks-and-process-them-as-they-complete-c"></a><span data-ttu-id="21751-102">Запуск нескольких асинхронных задач и их обработка по мере завершения (C#)</span><span class="sxs-lookup"><span data-stu-id="21751-102">Start Multiple Async Tasks and Process Them As They Complete (C#)</span></span>
<span data-ttu-id="21751-103">С помощью <xref:System.Threading.Tasks.Task.WhenAny%2A?displayProperty=nameWithType> можно запускать несколько задач одновременно и обрабатывать их по одной по мере завершения, а не в порядке их запуска.</span><span class="sxs-lookup"><span data-stu-id="21751-103">By using <xref:System.Threading.Tasks.Task.WhenAny%2A?displayProperty=nameWithType>, you can start multiple tasks at the same time and process them one by one as they’re completed rather than process them in the order in which they're started.</span></span>  
  
 <span data-ttu-id="21751-104">В следующем примере используется запрос для создания коллекции задач.</span><span class="sxs-lookup"><span data-stu-id="21751-104">The following example uses a query to create a collection of tasks.</span></span> <span data-ttu-id="21751-105">Каждая задача загружает содержимое указанного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="21751-105">Each task downloads the contents of a specified website.</span></span> <span data-ttu-id="21751-106">В каждой итерации цикла while ожидаемый вызов `WhenAny` возвращает задачу из коллекции задач, которая первой завершает свою загрузку.</span><span class="sxs-lookup"><span data-stu-id="21751-106">In each iteration of a while loop, an awaited call to `WhenAny` returns the task in the collection of tasks that finishes its download first.</span></span> <span data-ttu-id="21751-107">Эта задача удаляется из коллекции и обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="21751-107">That task is removed from the collection and processed.</span></span> <span data-ttu-id="21751-108">Цикл выполняется до тех пор, пока в коллекции еще есть задачи.</span><span class="sxs-lookup"><span data-stu-id="21751-108">The loop repeats until the collection contains no more tasks.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="21751-109">Для выполнения примеров необходимо, чтобы на компьютере были установлены Visual Studio 2012 или более поздняя версия и .NET Framework 4.5 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="21751-109">To run the examples, you must have Visual Studio 2012 or newer and  the .NET Framework 4.5 or newer installed on your computer.</span></span>  
  
## <a name="downloading-the-example"></a><span data-ttu-id="21751-110">Загрузка примера</span><span class="sxs-lookup"><span data-stu-id="21751-110">Downloading the Example</span></span>  
 <span data-ttu-id="21751-111">Вы можете скачать весь проект Windows Presentation Foundation (WPF) со страницы [Пример асинхронности. Тонкая настройка приложения](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea), а затем выполнить необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="21751-111">You can download the complete Windows Presentation Foundation (WPF) project from [Async Sample: Fine Tuning Your Application](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea) and then follow these steps.</span></span>  
  
1.  <span data-ttu-id="21751-112">Распакуйте загруженный файл, а затем запустите Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="21751-112">Decompress the file that you downloaded, and then start Visual Studio.</span></span>  
  
2.  <span data-ttu-id="21751-113">В строке меню выберите **Файл**, **Открыть**, **Проект/Решение**.</span><span class="sxs-lookup"><span data-stu-id="21751-113">On the menu bar, choose **File**, **Open**, **Project/Solution**.</span></span>  
  
3.  <span data-ttu-id="21751-114">В диалоговом окне **Открытие проекта** откройте папку с примером кода, который вы распаковали, а затем откройте файл решения (SLN) для AsyncFineTuningCS.</span><span class="sxs-lookup"><span data-stu-id="21751-114">In the **Open Project** dialog box, open the folder that holds the sample code that you decompressed, and then open the solution (.sln) file for AsyncFineTuningCS.</span></span>  
  
4.  <span data-ttu-id="21751-115">В **обозревателе решений** откройте контекстное меню проекта **ProcessTasksAsTheyFinish** и выберите команду **Назначить запускаемым проектом**.</span><span class="sxs-lookup"><span data-stu-id="21751-115">In **Solution Explorer**, open the shortcut menu for the **ProcessTasksAsTheyFinish** project, and then choose **Set as StartUp Project**.</span></span>  
  
5.  <span data-ttu-id="21751-116">Нажмите клавишу F5, чтобы запустить проект.</span><span class="sxs-lookup"><span data-stu-id="21751-116">Choose the F5 key to run the project.</span></span>  
  
     <span data-ttu-id="21751-117">Нажмите сочетание клавиш CTRL+F5, чтобы запустить проект без отладки.</span><span class="sxs-lookup"><span data-stu-id="21751-117">Choose the Ctrl+F5 keys to run the project without debugging it.</span></span>  
  
6.  <span data-ttu-id="21751-118">Запустите проект несколько раз, чтобы проверить, что загруженные размеры не всегда отображаются в одинаковом порядке.</span><span class="sxs-lookup"><span data-stu-id="21751-118">Run the project several times to verify that the downloaded lengths don't always appear in the same order.</span></span>  
  
 <span data-ttu-id="21751-119">Если вы не хотите скачивать проект, можете просмотреть файл MainWindow.xaml.cs в конце этого раздела.</span><span class="sxs-lookup"><span data-stu-id="21751-119">If you don't want to download the project, you can review the MainWindow.xaml.cs file at the end of this topic.</span></span>  
  
## <a name="building-the-example"></a><span data-ttu-id="21751-120">Построение примера</span><span class="sxs-lookup"><span data-stu-id="21751-120">Building the Example</span></span>  
 <span data-ttu-id="21751-121">Код из этого примера добавляется к коду, разработанному в разделе [Отмена оставшихся асинхронных задач после завершения одной из них (C#)](../../../../csharp/programming-guide/concepts/async/cancel-remaining-async-tasks-after-one-is-complete.md)[Отмена оставшихся асинхронных задач после завершения одной из них](https://msdn.microsoft.com/library/8e800b58-235a-44b7-a02c-fa4375591d76), и использует тот же пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="21751-121">This example adds to the code that’s developed in [Cancel Remaining Async Tasks after One Is Complete (C#)](../../../../csharp/programming-guide/concepts/async/cancel-remaining-async-tasks-after-one-is-complete.md)[Cancel Remaining Async Tasks after One Is Complete](https://msdn.microsoft.com/library/8e800b58-235a-44b7-a02c-fa4375591d76) and uses the same UI.</span></span>  
  
 <span data-ttu-id="21751-122">Для самостоятельной сборки примера шаг за шагом следуйте инструкциям в разделе "Загрузка примера", но выберите **CancelAfterOneTask** как **запускаемый проект**.</span><span class="sxs-lookup"><span data-stu-id="21751-122">To build the example yourself, step by step, follow the instructions in the "Downloading the Example" section, but choose **CancelAfterOneTask** as the **StartUp Project**.</span></span> <span data-ttu-id="21751-123">Добавьте изменения в данном разделе в метод `AccessTheWebAsync` в этом проекте.</span><span class="sxs-lookup"><span data-stu-id="21751-123">Add the changes in this topic to the `AccessTheWebAsync` method in that project.</span></span> <span data-ttu-id="21751-124">Изменения помечены звездочками.</span><span class="sxs-lookup"><span data-stu-id="21751-124">The changes are marked with asterisks.</span></span>  
  
 <span data-ttu-id="21751-125">Проект **CancelAfterOneTask** уже содержит запрос, который при выполнении создает коллекцию задач.</span><span class="sxs-lookup"><span data-stu-id="21751-125">The **CancelAfterOneTask** project already includes a query that, when executed, creates a collection of tasks.</span></span> <span data-ttu-id="21751-126">Каждый вызов `ProcessURLAsync` в следующем коде возвращает <xref:System.Threading.Tasks.Task%601>, где `TResult` — целое число.</span><span class="sxs-lookup"><span data-stu-id="21751-126">Each call to `ProcessURLAsync` in the following code returns a <xref:System.Threading.Tasks.Task%601> where `TResult` is an integer.</span></span>  
  
```csharp  
IEnumerable<Task<int>> downloadTasksQuery =  
    from url in urlList select ProcessURL(url, client, ct);  
```  
  
 <span data-ttu-id="21751-127">В файле MainWindow.xaml.cs проекта внесите следующие изменения в метод `AccessTheWebAsync`.</span><span class="sxs-lookup"><span data-stu-id="21751-127">In the MainWindow.xaml.cs file of the  project, make the following changes to the `AccessTheWebAsync` method.</span></span>  
  
-   <span data-ttu-id="21751-128">Выполните запрос, применяя <xref:System.Linq.Enumerable.ToList%2A?displayProperty=nameWithType> вместо <xref:System.Linq.Enumerable.ToArray%2A>.</span><span class="sxs-lookup"><span data-stu-id="21751-128">Execute the query by applying <xref:System.Linq.Enumerable.ToList%2A?displayProperty=nameWithType> instead of <xref:System.Linq.Enumerable.ToArray%2A>.</span></span>  
  
    ```csharp  
    List<Task<int>> downloadTasks = downloadTasksQuery.ToList();  
    ```  
  
-   <span data-ttu-id="21751-129">Добавьте цикл while, выполняющий следующие действия для каждой задачи в коллекции.</span><span class="sxs-lookup"><span data-stu-id="21751-129">Add a while loop that performs the following steps for each task in the collection.</span></span>  
  
    1.  <span data-ttu-id="21751-130">Ожидает вызов `WhenAny` для определения первой задачи в коллекции, чтобы завершить ее загрузку.</span><span class="sxs-lookup"><span data-stu-id="21751-130">Awaits a call to `WhenAny` to identify the first task in the collection to finish its download.</span></span>  
  
        ```csharp  
        Task<int> firstFinishedTask = await Task.WhenAny(downloadTasks);  
        ```  
  
    2.  <span data-ttu-id="21751-131">Удаляет эту задачу из коллекции.</span><span class="sxs-lookup"><span data-stu-id="21751-131">Removes that task from the collection.</span></span>  
  
        ```csharp  
        downloadTasks.Remove(firstFinishedTask);  
        ```  
  
    3.  <span data-ttu-id="21751-132">Ожидает `firstFinishedTask`, возвращаемый при вызове `ProcessURLAsync`.</span><span class="sxs-lookup"><span data-stu-id="21751-132">Awaits `firstFinishedTask`, which is returned by a call to `ProcessURLAsync`.</span></span> <span data-ttu-id="21751-133">Переменная `firstFinishedTask` представляет собой <xref:System.Threading.Tasks.Task%601>, где `TReturn` — целое число.</span><span class="sxs-lookup"><span data-stu-id="21751-133">The `firstFinishedTask` variable is a <xref:System.Threading.Tasks.Task%601> where `TReturn` is an integer.</span></span> <span data-ttu-id="21751-134">Задача уже завершена, но она ожидается для получения размера загруженного веб-сайта, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="21751-134">The task is already complete, but you await it to retrieve the length of the downloaded website, as the following example shows.</span></span>  
  
        ```csharp  
        int length = await firstFinishedTask;  
        resultsTextBox.Text += String.Format("\r\nLength of the download:  {0}", length);  
        ```  
  
 <span data-ttu-id="21751-135">Следует запустить проект несколько раз для проверки, что загруженные размеры не всегда отображаются в одинаковом порядке.</span><span class="sxs-lookup"><span data-stu-id="21751-135">You should run the project several times to verify that the downloaded lengths don't always appear in the same order.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="21751-136">Можно использовать `WhenAny` в цикле, как описано в примере, для решения проблем, которые включают небольшое число задач.</span><span class="sxs-lookup"><span data-stu-id="21751-136">You can use `WhenAny` in a loop, as described in the example, to solve problems that involve a small number of tasks.</span></span> <span data-ttu-id="21751-137">Однако когда требуется обработка большого числа задач, другие методы будут более эффективны.</span><span class="sxs-lookup"><span data-stu-id="21751-137">However, other approaches are more efficient if you have a large number of tasks to process.</span></span> <span data-ttu-id="21751-138">Дополнительные сведения и примеры см. в разделе [Обработка задач по мере их завершения](https://blogs.msdn.microsoft.com/pfxteam/2012/08/02/processing-tasks-as-they-complete/).</span><span class="sxs-lookup"><span data-stu-id="21751-138">For more information and examples, see [Processing tasks as they complete](https://blogs.msdn.microsoft.com/pfxteam/2012/08/02/processing-tasks-as-they-complete/).</span></span>  
  
## <a name="complete-example"></a><span data-ttu-id="21751-139">Полный пример</span><span class="sxs-lookup"><span data-stu-id="21751-139">Complete Example</span></span>  
 <span data-ttu-id="21751-140">Приведенный ниже код — полный текст файла MainWindow.xaml.cs для примера.</span><span class="sxs-lookup"><span data-stu-id="21751-140">The following code is the complete text of the MainWindow.xaml.cs file for the example.</span></span> <span data-ttu-id="21751-141">Звездочками помечаются элементы, добавленные для этого примера.</span><span class="sxs-lookup"><span data-stu-id="21751-141">Asterisks mark the elements that were added for this example.</span></span>  
  
 <span data-ttu-id="21751-142">Обратите внимание на то, что необходимо добавить ссылку для <xref:System.Net.Http>.</span><span class="sxs-lookup"><span data-stu-id="21751-142">Notice that you must add a reference for <xref:System.Net.Http>.</span></span>  
  
 <span data-ttu-id="21751-143">Можно загрузить проект со страницы [Пример асинхронности. Тонкая настройка приложения](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea).</span><span class="sxs-lookup"><span data-stu-id="21751-143">You can download the project from [Async Sample: Fine Tuning Your Application](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea).</span></span>  
  
```csharp  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Text;  
using System.Threading.Tasks;  
using System.Windows;  
using System.Windows.Controls;  
using System.Windows.Data;  
using System.Windows.Documents;  
using System.Windows.Input;  
using System.Windows.Media;  
using System.Windows.Media.Imaging;  
using System.Windows.Navigation;  
using System.Windows.Shapes;  
  
// Add a using directive and a reference for System.Net.Http.  
using System.Net.Http;  
  
// Add the following using directive.  
using System.Threading;  
  
namespace ProcessTasksAsTheyFinish  
{  
    public partial class MainWindow : Window  
    {  
        // Declare a System.Threading.CancellationTokenSource.  
        CancellationTokenSource cts;  
  
        public MainWindow()  
        {  
            InitializeComponent();  
        }  
  
        private async void startButton_Click(object sender, RoutedEventArgs e)  
        {  
            resultsTextBox.Clear();  
  
            // Instantiate the CancellationTokenSource.  
            cts = new CancellationTokenSource();  
  
            try  
            {  
                await AccessTheWebAsync(cts.Token);  
                resultsTextBox.Text += "\r\nDownloads complete.";  
            }  
            catch (OperationCanceledException)  
            {  
                resultsTextBox.Text += "\r\nDownloads canceled.\r\n";  
            }  
            catch (Exception)  
            {  
                resultsTextBox.Text += "\r\nDownloads failed.\r\n";  
            }  
  
            cts = null;  
        }  
  
        private void cancelButton_Click(object sender, RoutedEventArgs e)  
        {  
            if (cts != null)  
            {  
                cts.Cancel();  
            }  
        }  
  
        async Task AccessTheWebAsync(CancellationToken ct)  
        {  
            HttpClient client = new HttpClient();  
  
            // Make a list of web addresses.  
            List<string> urlList = SetUpURLList();  
  
            // ***Create a query that, when executed, returns a collection of tasks.  
            IEnumerable<Task<int>> downloadTasksQuery =  
                from url in urlList select ProcessURL(url, client, ct);  
  
            // ***Use ToList to execute the query and start the tasks.   
            List<Task<int>> downloadTasks = downloadTasksQuery.ToList();  
  
            // ***Add a loop to process the tasks one at a time until none remain.  
            while (downloadTasks.Count > 0)  
            {  
                    // Identify the first task that completes.  
                    Task<int> firstFinishedTask = await Task.WhenAny(downloadTasks);  
  
                    // ***Remove the selected task from the list so that you don't  
                    // process it more than once.  
                    downloadTasks.Remove(firstFinishedTask);  
  
                    // Await the completed task.  
                    int length = await firstFinishedTask;  
                    resultsTextBox.Text += String.Format("\r\nLength of the download:  {0}", length);  
            }  
        }  
  
        private List<string> SetUpURLList()  
        {  
            List<string> urls = new List<string>   
            {   
                "http://msdn.microsoft.com",  
                "http://msdn.microsoft.com/library/windows/apps/br211380.aspx",  
                "http://msdn.microsoft.com/library/hh290136.aspx",  
                "http://msdn.microsoft.com/library/dd470362.aspx",  
                "http://msdn.microsoft.com/library/aa578028.aspx",  
                "http://msdn.microsoft.com/library/ms404677.aspx",  
                "http://msdn.microsoft.com/library/ff730837.aspx"  
            };  
            return urls;  
        }  
  
        async Task<int> ProcessURL(string url, HttpClient client, CancellationToken ct)  
        {  
            // GetAsync returns a Task<HttpResponseMessage>.   
            HttpResponseMessage response = await client.GetAsync(url, ct);  
  
            // Retrieve the website contents from the HttpResponseMessage.  
            byte[] urlContents = await response.Content.ReadAsByteArrayAsync();  
  
            return urlContents.Length;  
        }  
    }  
}  
  
// Sample Output:  
  
// Length of the download:  226093  
// Length of the download:  412588  
// Length of the download:  175490  
// Length of the download:  204890  
// Length of the download:  158855  
// Length of the download:  145790  
// Length of the download:  44908  
// Downloads complete.  
```  
  
## <a name="see-also"></a><span data-ttu-id="21751-144">См. также</span><span class="sxs-lookup"><span data-stu-id="21751-144">See Also</span></span>  
 <xref:System.Threading.Tasks.Task.WhenAny%2A>  
 <span data-ttu-id="21751-145">[Fine-Tuning Your Async Application (C#)](../../../../csharp/programming-guide/concepts/async/fine-tuning-your-async-application.md) (Тонкая настройка асинхронного приложения в C#)</span><span class="sxs-lookup"><span data-stu-id="21751-145">[Fine-Tuning Your Async Application (C#)](../../../../csharp/programming-guide/concepts/async/fine-tuning-your-async-application.md)</span></span>  
 [<span data-ttu-id="21751-146">Асинхронное программирование с использованием ключевых слов async и await (C#)</span><span class="sxs-lookup"><span data-stu-id="21751-146">Asynchronous Programming with async and await (C#)</span></span>](../../../../csharp/programming-guide/concepts/async/index.md)  
 <span data-ttu-id="21751-147">[Async Sample: Fine Tuning Your Application](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea) (Пример использования async. Тонкая настройка асинхронного приложения)</span><span class="sxs-lookup"><span data-stu-id="21751-147">[Async Sample: Fine Tuning Your Application](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea)</span></span>
