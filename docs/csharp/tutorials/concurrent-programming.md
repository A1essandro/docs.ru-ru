---
title: "Параллельное программирование. Руководство по C#"
description: "Изучите методы параллельного выполнения задач (активно использующих ресурсы ЦП)"
keywords: "C#, async, использование ресурсов ЦП, использование ресурсов сети"
ms.date: 08/24/2016
ms.topic: article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.assetid: 0f8b42de-858a-44a3-87d9-998211f26377
redirect_url: /dotnet/csharp/tutorials/index
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 00cf3b04178ca48c9f8f35eb16bc216389e6b272
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---

# <a name="-concurrent-programming"></a><span data-ttu-id="61c98-104">🔧 Параллельное программирование</span><span class="sxs-lookup"><span data-stu-id="61c98-104">🔧 Concurrent Programming</span></span>

> <span data-ttu-id="61c98-105">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="61c98-105">**Note**</span></span>
> 
> <span data-ttu-id="61c98-106">Этот раздел еще не написан!</span><span class="sxs-lookup"><span data-stu-id="61c98-106">This topic hasn’t been written yet!</span></span> 
>
> <span data-ttu-id="61c98-107">Мы будем рады получить ваши предложения, которые помогут нам определить вопросы, требующие рассмотрения, и подход.</span><span class="sxs-lookup"><span data-stu-id="61c98-107">We welcome your input to help shape the scope and approach.</span></span> <span data-ttu-id="61c98-108">Вы можете отслеживать состояние и оставлять предложения по этой [теме](https://github.com/dotnet/docs/issues/953) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="61c98-108">You can track the status and provide input on this [issue](https://github.com/dotnet/docs/issues/953) at GitHub.</span></span>
> 
> <span data-ttu-id="61c98-109">Чтобы просмотреть черновые варианты и наброски этого раздела, оставьте сообщение со своими контактными данными в соответствующей теме.</span><span class="sxs-lookup"><span data-stu-id="61c98-109">If you would like to review early drafts and outlines of this topic, please leave a note with your contact information in the issue.</span></span>
>
> <span data-ttu-id="61c98-110">Узнать больше о том, как вы можете посодействовать, можно на сайте [GitHub](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md).</span><span class="sxs-lookup"><span data-stu-id="61c98-110">Learn more about how you can contribute on [GitHub](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md).</span></span>
>

