---
title: Не удалось загрузить сведения для класса &#39; &lt;classname&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc30712
- bc30712
helpviewer_keywords:
- BC30712
ms.assetid: c7ffbd6d-05c6-4261-b44b-1bcd521bb350
ms.openlocfilehash: 368484d9138d1ae10efb8c63f6cfaa6bcefa6ed8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528970"
---
# <a name="unable-to-load-information-for-class-39ltclassnamegt39"></a><span data-ttu-id="7c21b-102">Не удалось загрузить сведения для класса &#39; &lt;classname&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="7c21b-102">Unable to load information for class &#39;&lt;classname&gt;&#39;</span></span>
<span data-ttu-id="7c21b-103">Использовалась ссылка на класс, который не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7c21b-103">A reference was made to a class that is not available.</span></span>  
  
 <span data-ttu-id="7c21b-104">**Идентификатор ошибки:** BC30712</span><span class="sxs-lookup"><span data-stu-id="7c21b-104">**Error ID:** BC30712</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="7c21b-105">Исправление ошибки</span><span class="sxs-lookup"><span data-stu-id="7c21b-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="7c21b-106">Убедитесь, что класс был определен и что имя указано правильно.</span><span class="sxs-lookup"><span data-stu-id="7c21b-106">Verify that the class is defined and that you spelled the name correctly.</span></span>  
  
2.  <span data-ttu-id="7c21b-107">Попробуйте обратиться к одному из членов, объявленных в модуле.</span><span class="sxs-lookup"><span data-stu-id="7c21b-107">Try accessing one of the members declared in the module.</span></span> <span data-ttu-id="7c21b-108">В некоторых случаях среда отладки не может найти члены, потому что модули, в которых они объявлены, еще не были загружены.</span><span class="sxs-lookup"><span data-stu-id="7c21b-108">In some cases, the debugging environment cannot locate members because the modules where they are declared have not been loaded yet.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c21b-109">См. также</span><span class="sxs-lookup"><span data-stu-id="7c21b-109">See also</span></span>
- [<span data-ttu-id="7c21b-110">Отладка в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7c21b-110">Debugging in Visual Studio</span></span>](/visualstudio/debugger/debugging-in-visual-studio)
