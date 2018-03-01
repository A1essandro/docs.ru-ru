---
title: "Требуется ссылка на сборку &#39; &lt;assemblyname&gt;&#39; содержащий базовый класс &#39;&lt; className&gt;&#39;"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- bc30007
- vbc30007
helpviewer_keywords:
- BC30007
ms.assetid: 5f34cf47-6c6e-4954-bd8e-d6b020b75fb7
caps.latest.revision: 
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 39fa33a655b311ee39466c18cefdb0bf07a92720
ms.sourcegitcommit: 34ec7753acf76f90a0fa845235ef06663dc9e36e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/21/2017
---
# <a name="reference-required-to-assembly-39ltassemblynamegt39-containing-the-base-class-39ltclassnamegt39"></a><span data-ttu-id="634d8-102">Требуется ссылка на сборку &#39; &lt;assemblyname&gt;&#39; содержащий базовый класс &#39;&lt; className&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="634d8-102">Reference required to assembly &#39;&lt;assemblyname&gt;&#39; containing the base class &#39;&lt;classname&gt;&#39;</span></span>
<span data-ttu-id="634d8-103">Требуется ссылка на сборку "\<имя_сборки >" содержит базовый класс\<имя_класса > ".</span><span class="sxs-lookup"><span data-stu-id="634d8-103">Reference required to assembly '\<assemblyname>' containing the base class '\<classname>'.</span></span> <span data-ttu-id="634d8-104">Добавьте эту ссылку в проект.</span><span class="sxs-lookup"><span data-stu-id="634d8-104">Add one to your project.</span></span>  
  
 <span data-ttu-id="634d8-105">Класс определяется в библиотеке динамической компоновки (DLL) или в сборке, на которую в проекте нет прямой ссылки.</span><span class="sxs-lookup"><span data-stu-id="634d8-105">The class is defined in a dynamic-link library (DLL) or assembly that is not directly referenced in your project.</span></span> <span data-ttu-id="634d8-106">Компилятор [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] требует ссылки в целях устранения неоднозначности, если класс определен в нескольких библиотеках DLL или сборках.</span><span class="sxs-lookup"><span data-stu-id="634d8-106">The [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] compiler requires a reference to avoid ambiguity in case the class is defined in more than one DLL or assembly.</span></span>  
  
 <span data-ttu-id="634d8-107">**Идентификатор ошибки:** BC30007</span><span class="sxs-lookup"><span data-stu-id="634d8-107">**Error ID:** BC30007</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="634d8-108">Исправление ошибки</span><span class="sxs-lookup"><span data-stu-id="634d8-108">To correct this error</span></span>  
  
-   <span data-ttu-id="634d8-109">Включите в ссылки проекта имя библиотеки DLL или сборки, на которую нет ссылки.</span><span class="sxs-lookup"><span data-stu-id="634d8-109">Include the name of the unreferenced DLL or assembly in your project references.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="634d8-110">См. также</span><span class="sxs-lookup"><span data-stu-id="634d8-110">See Also</span></span>  
   
 [<span data-ttu-id="634d8-111">Управление ссылками в проекте</span><span class="sxs-lookup"><span data-stu-id="634d8-111">Managing references in a project</span></span>](/visualstudio/ide/managing-references-in-a-project)  
 [<span data-ttu-id="634d8-112">Диагностика неработающих ссылок</span><span class="sxs-lookup"><span data-stu-id="634d8-112">Troubleshooting Broken References</span></span>](/visualstudio/ide/troubleshooting-broken-references)
