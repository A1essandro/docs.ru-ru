---
title: "Использование пакета SDK для компилятора .NET — руководство по C#"
description: "Изучите интерфейсы API Roslyn, позволяющие создавать средства автоматической диагностики и исправления кода"
keywords: .NET, .NET Core, C#, Roslyn,
ms.date: 06/25/2016
ms.topic: article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.assetid: abed9e00-2ddc-468e-9cca-d033bd6a7e36
redirect_url: /dotnet/csharp/index
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: b227d67fd5431da328e1686fd9afc6a3b9db035e
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---

# <a name="-using-the-net-compiler-sdk"></a><span data-ttu-id="4d822-104">🔧 Использование пакета SDK для платформы компилятора .NET</span><span class="sxs-lookup"><span data-stu-id="4d822-104">🔧 Using the .NET Compiler SDK</span></span>

> <span data-ttu-id="4d822-105">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="4d822-105">**Note**</span></span>
> 
> <span data-ttu-id="4d822-106">Этот раздел еще не написан!</span><span class="sxs-lookup"><span data-stu-id="4d822-106">This topic hasn’t been written yet!</span></span> 
>
> <span data-ttu-id="4d822-107">Мы будем рады получить ваши предложения, которые помогут нам определить вопросы, требующие рассмотрения, и подход.</span><span class="sxs-lookup"><span data-stu-id="4d822-107">We welcome your input to help shape the scope and approach.</span></span> <span data-ttu-id="4d822-108">Вы можете отслеживать состояние и оставлять предложения по этой [теме](https://github.com/dotnet/docs/issues/972) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="4d822-108">You can track the status and provide input on this [issue](https://github.com/dotnet/docs/issues/972) at GitHub.</span></span>
> 
> <span data-ttu-id="4d822-109">Чтобы просмотреть черновые варианты и наброски этого раздела, оставьте сообщение со своими контактными данными в соответствующей теме.</span><span class="sxs-lookup"><span data-stu-id="4d822-109">If you would like to review early drafts and outlines of this topic, please leave a note with your contact information in the issue.</span></span>
>
> <span data-ttu-id="4d822-110">Узнать больше о том, как вы можете посодействовать, можно на сайте [GitHub](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md).</span><span class="sxs-lookup"><span data-stu-id="4d822-110">Learn more about how you can contribute on [GitHub](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md).</span></span>
>

<span data-ttu-id="4d822-111">Это раздел метаданных для всего раздела.</span><span class="sxs-lookup"><span data-stu-id="4d822-111">This is a meta-topic for an entire section.</span></span> <span data-ttu-id="4d822-112">Аспекты, которые здесь надо описать:</span><span class="sxs-lookup"><span data-stu-id="4d822-112">Areas that need to be covered here include:</span></span> 
* <span data-ttu-id="4d822-113">Начало работы</span><span class="sxs-lookup"><span data-stu-id="4d822-113">Getting Started</span></span>
* <span data-ttu-id="4d822-114">примеры и учебники;</span><span class="sxs-lookup"><span data-stu-id="4d822-114">Samples and tutorials</span></span>
* <span data-ttu-id="4d822-115">концептуальное содержимое;</span><span class="sxs-lookup"><span data-stu-id="4d822-115">conceptual content</span></span>
* <span data-ttu-id="4d822-116">общая модель API-интерфейсов;</span><span class="sxs-lookup"><span data-stu-id="4d822-116">overall model of the APIs</span></span>
* <span data-ttu-id="4d822-117">ссылки на примеры в репозитории [анализаторов roslyn](http://github.com/dotnet/roslyn-analyzers);</span><span class="sxs-lookup"><span data-stu-id="4d822-117">links to samples on the [roslyn-analyzers](http://github.com/dotnet/roslyn-analyzers) repository</span></span>
* <span data-ttu-id="4d822-118">ссылки на другие справочные материалы.</span><span class="sxs-lookup"><span data-stu-id="4d822-118">links to other reference content</span></span>

