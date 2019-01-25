---
title: '&lt;тип1&gt;&#39;&lt;typename&gt; &#39; должен реализовывать &#39; &lt;имя_метода&gt; &#39; для интерфейса &#39; &lt;interfacename&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: ff9ffd50f7f21814d5e4c23fd8df50b12bf746f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642451"
---
# <a name="lttype1gt39lttypenamegt39-must-implement-39ltmethodnamegt39-for-interface-39ltinterfacenamegt39"></a><span data-ttu-id="e9934-102">&lt;тип1&gt;&#39;&lt;typename&gt; &#39; должен реализовывать &#39; &lt;имя_метода&gt; &#39; для интерфейса &#39; &lt;interfacename&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="e9934-102">&lt;type1&gt;&#39;&lt;typename&gt;&#39; must implement &#39;&lt;methodname&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39;</span></span>
<span data-ttu-id="e9934-103">Класс или структура объявляет о реализации интерфейса, но не реализует процедуры, определенные в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e9934-103">A class or structure claims to implement an interface but does not implement a procedure defined by the interface.</span></span> <span data-ttu-id="e9934-104">Каждый член интерфейса должен быть реализован.</span><span class="sxs-lookup"><span data-stu-id="e9934-104">Every member of the interface must be implemented.</span></span>  
  
 <span data-ttu-id="e9934-105">**Идентификатор ошибки:** BC30149</span><span class="sxs-lookup"><span data-stu-id="e9934-105">**Error ID:** BC30149</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="e9934-106">Исправление ошибки</span><span class="sxs-lookup"><span data-stu-id="e9934-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="e9934-107">Объявите процедуру с тем же именем и подписью, как определено в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e9934-107">Declare a procedure with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="e9934-108">Не забудьте включить по крайней мере `End Function` или `End Sub` инструкции.</span><span class="sxs-lookup"><span data-stu-id="e9934-108">Be sure to include at least the `End Function` or `End Sub` statement.</span></span>  
  
2.  <span data-ttu-id="e9934-109">Добавить `Implements` предложение в конец `Function` или `Sub` инструкции.</span><span class="sxs-lookup"><span data-stu-id="e9934-109">Add an `Implements` clause to the end of the `Function` or `Sub` statement.</span></span> <span data-ttu-id="e9934-110">Пример:</span><span class="sxs-lookup"><span data-stu-id="e9934-110">For example:</span></span>  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="e9934-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e9934-111">See also</span></span>
- [<span data-ttu-id="e9934-112">Оператор Implements</span><span class="sxs-lookup"><span data-stu-id="e9934-112">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)
- [<span data-ttu-id="e9934-113">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="e9934-113">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
