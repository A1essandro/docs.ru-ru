---
title: "Другие структуры управления (Visual Basic)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- statements [Visual Basic], control flow
- control structures [Visual Basic]
ms.assetid: 24b811f7-98ba-40ec-8dd3-4d528cfa4574
caps.latest.revision: "19"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 09e59d25b3b2fc89026295e8500c30dad7b75086
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="other-control-structures-visual-basic"></a><span data-ttu-id="de404-102">Другие структуры управления (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="de404-102">Other Control Structures (Visual Basic)</span></span>
[!INCLUDE[vbprvb](~/includes/vbprvb-md.md)]<span data-ttu-id="de404-103">предоставляет структур управления, которые помогают удаления ресурсов или уменьшите число повторений ссылок на объект.</span><span class="sxs-lookup"><span data-stu-id="de404-103"> provides control structures that help you dispose of a resource or reduce the number of times you have to repeat an object reference.</span></span>  
  
## <a name="usingend-using-construction"></a><span data-ttu-id="de404-104">С помощью... Использование конструкции End</span><span class="sxs-lookup"><span data-stu-id="de404-104">Using...End Using Construction</span></span>  
 <span data-ttu-id="de404-105">`Using...End Using` Конструкции устанавливает блок операторов, в котором следует использовать ресурсы, такие как SQL-соединение.</span><span class="sxs-lookup"><span data-stu-id="de404-105">The `Using...End Using` construction establishes a statement block within which you make use of a resource such as a SQL connection.</span></span> <span data-ttu-id="de404-106">При необходимости можно запросить ресурс с `Using` инструкции.</span><span class="sxs-lookup"><span data-stu-id="de404-106">You can optionally acquire the resource with the `Using` statement.</span></span> <span data-ttu-id="de404-107">После выхода из `Using` блока [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] автоматически удаляет ресурс, чтобы он будет доступен для использования другим кодом.</span><span class="sxs-lookup"><span data-stu-id="de404-107">When you exit the `Using` block, [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] automatically disposes of the resource so that it is available for other code to use.</span></span> <span data-ttu-id="de404-108">Ресурс должен быть локальным и допускать удаление.</span><span class="sxs-lookup"><span data-stu-id="de404-108">The resource must be local and disposable.</span></span> <span data-ttu-id="de404-109">Дополнительные сведения см. в разделе [Оператор using](../../../../visual-basic/language-reference/statements/using-statement.md).</span><span class="sxs-lookup"><span data-stu-id="de404-109">For more information, see [Using Statement](../../../../visual-basic/language-reference/statements/using-statement.md).</span></span>  
  
## <a name="withend-with-construction"></a><span data-ttu-id="de404-110">С... Завершить с построением</span><span class="sxs-lookup"><span data-stu-id="de404-110">With...End With Construction</span></span>  
 <span data-ttu-id="de404-111">`With...End With` Позволяет указать ссылку на объект один раз, а затем запустите последовательность операторов, доступа к его членам.</span><span class="sxs-lookup"><span data-stu-id="de404-111">The `With...End With` construction lets you specify an object reference once and then run a series of statements that access its members.</span></span> <span data-ttu-id="de404-112">Это может упростить код и повысить производительность, поскольку [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] не восстанавливает ссылку для каждого оператора, который обращается к ней.</span><span class="sxs-lookup"><span data-stu-id="de404-112">This can simplify your code and improve performance because [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] does not have to re-establish the reference for each statement that accesses it.</span></span> <span data-ttu-id="de404-113">Дополнительные сведения см. в разделе [с... Завершить с инструкцией](../../../../visual-basic/language-reference/statements/with-end-with-statement.md).</span><span class="sxs-lookup"><span data-stu-id="de404-113">For more information, see [With...End With Statement](../../../../visual-basic/language-reference/statements/with-end-with-statement.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de404-114">См. также</span><span class="sxs-lookup"><span data-stu-id="de404-114">See Also</span></span>  
 [<span data-ttu-id="de404-115">Поток управления</span><span class="sxs-lookup"><span data-stu-id="de404-115">Control Flow</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/index.md)  
 [<span data-ttu-id="de404-116">Структуры решений</span><span class="sxs-lookup"><span data-stu-id="de404-116">Decision Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/decision-structures.md)  
 [<span data-ttu-id="de404-117">Циклические структуры</span><span class="sxs-lookup"><span data-stu-id="de404-117">Loop Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)  
 [<span data-ttu-id="de404-118">Вложенные структуры управления</span><span class="sxs-lookup"><span data-stu-id="de404-118">Nested Control Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)  
 [<span data-ttu-id="de404-119">Оператор Using</span><span class="sxs-lookup"><span data-stu-id="de404-119">Using Statement</span></span>](../../../../visual-basic/language-reference/statements/using-statement.md)  
 [<span data-ttu-id="de404-120">Оператор With...End With</span><span class="sxs-lookup"><span data-stu-id="de404-120">With...End With Statement</span></span>](../../../../visual-basic/language-reference/statements/with-end-with-statement.md)
