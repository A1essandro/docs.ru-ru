---
title: '&#39;#ElseIf&#39; должен предшествовать соответствующий &#39;#If&#39; или &#39;#ElseIf&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: ef904173b1791309f6c2722bd959cabdad1d71da
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
---
# <a name="39elseif39-must-be-preceded-by-a-matching-39if39-or-39elseif39"></a><span data-ttu-id="04403-102">&#39;#ElseIf&#39; должен предшествовать соответствующий &#39;#If&#39; или &#39;#ElseIf&#39;</span><span class="sxs-lookup"><span data-stu-id="04403-102">&#39;#ElseIf&#39; must be preceded by a matching &#39;#If&#39; or &#39;#ElseIf&#39;</span></span>
<span data-ttu-id="04403-103">`#ElseIf` является директивой условной компиляции.</span><span class="sxs-lookup"><span data-stu-id="04403-103">`#ElseIf` is a conditional compilation directive.</span></span> <span data-ttu-id="04403-104">`#ElseIf` Предложение должен предшествовать соответствующий `#If` или `#ElseIf` предложения.</span><span class="sxs-lookup"><span data-stu-id="04403-104">An `#ElseIf` clause must be preceded by a matching `#If` or `#ElseIf` clause.</span></span>  
  
 <span data-ttu-id="04403-105">**Идентификатор ошибки:** BC30014</span><span class="sxs-lookup"><span data-stu-id="04403-105">**Error ID:** BC30014</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="04403-106">Исправление ошибки</span><span class="sxs-lookup"><span data-stu-id="04403-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="04403-107">Убедитесь, что предшествующий `#If` или `#ElseIf` не был отделен от этого `#ElseIf` блоком условной компиляции или неправильно размещенной директивой `#End If`.</span><span class="sxs-lookup"><span data-stu-id="04403-107">Check that a preceding `#If` or `#ElseIf` has not been separated from this `#ElseIf` by an intervening conditional compilation block or an incorrectly placed `#End If`.</span></span>  
  
2.  <span data-ttu-id="04403-108">Если `#ElseIf` предшествует `#Else` директивы, либо удалите `#Else` или измените ее на `#ElseIf`.</span><span class="sxs-lookup"><span data-stu-id="04403-108">If the `#ElseIf` is preceded by a `#Else` directive, either remove the `#Else` or change it to an `#ElseIf`.</span></span>  
  
3.  <span data-ttu-id="04403-109">Если все остальное в порядке, добавьте директиву `#If` в начало блока условной компиляции.</span><span class="sxs-lookup"><span data-stu-id="04403-109">If everything else is in order, add an `#If` directive to the beginning of the conditional compilation block.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04403-110">См. также</span><span class="sxs-lookup"><span data-stu-id="04403-110">See Also</span></span>  
 [<span data-ttu-id="04403-111">Директивы #If...Then...#Else</span><span class="sxs-lookup"><span data-stu-id="04403-111">#If...Then...#Else Directives</span></span>](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
