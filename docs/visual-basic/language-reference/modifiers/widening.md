---
title: Widening (Visual Basic)
ms.date: 07/20/2015
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vb.widening
helpviewer_keywords:
- conversions [Visual Basic], type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- Widening keyword [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: 646ae263-94d3-40a2-b0cc-64f619292f56
caps.latest.revision: 15
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 034099397c1d296a42712b8c202e2ac99a0fb43b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="widening-visual-basic"></a><span data-ttu-id="b64ee-102">Widening (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b64ee-102">Widening (Visual Basic)</span></span>
<span data-ttu-id="b64ee-103">Указывает, что оператор преобразования (`CType`) преобразует класс или структуру к типу, который может содержать все возможные значения исходного класса или структуры.</span><span class="sxs-lookup"><span data-stu-id="b64ee-103">Indicates that a conversion operator (`CType`) converts a class or structure to a type that can hold all possible values of the original class or structure.</span></span>  
  
## <a name="converting-with-the-widening-keyword"></a><span data-ttu-id="b64ee-104">Преобразование с помощью ключевого слова Widening</span><span class="sxs-lookup"><span data-stu-id="b64ee-104">Converting with the Widening Keyword</span></span>  
 <span data-ttu-id="b64ee-105">Процедуры преобразования необходимо указать `Public Shared` в дополнение к `Widening`.</span><span class="sxs-lookup"><span data-stu-id="b64ee-105">The conversion procedure must specify `Public Shared` in addition to `Widening`.</span></span>  
  
 <span data-ttu-id="b64ee-106">Расширяющие преобразования всегда выполняться успешно во время выполнения и никогда не приводят к потере данных.</span><span class="sxs-lookup"><span data-stu-id="b64ee-106">Widening conversions always succeed at run time and never incur data loss.</span></span> <span data-ttu-id="b64ee-107">Примерами являются `Single` для `Double`, `Char` для `String`и производный тип к его базовому типу.</span><span class="sxs-lookup"><span data-stu-id="b64ee-107">Examples are `Single` to `Double`, `Char` to `String`, and a derived type to its base type.</span></span> <span data-ttu-id="b64ee-108">Это последнее преобразование является расширяющим, так как производный тип содержит все члены базового типа и поэтому является экземпляром базового типа.</span><span class="sxs-lookup"><span data-stu-id="b64ee-108">This last conversion is widening because the derived type contains all the members of the base type and thus is an instance of the base type.</span></span>  
  
 <span data-ttu-id="b64ee-109">Не используйте код-потребитель `CType` для расширяющие преобразования, даже если `Option Strict` — `On`.</span><span class="sxs-lookup"><span data-stu-id="b64ee-109">The consuming code does not have to use `CType` for widening conversions, even if `Option Strict` is `On`.</span></span>  
  
 <span data-ttu-id="b64ee-110">`Widening` Ключевое слово может использоваться в этом контексте:</span><span class="sxs-lookup"><span data-stu-id="b64ee-110">The `Widening` keyword can be used in this context:</span></span>  
  
 [<span data-ttu-id="b64ee-111">Оператор Statement</span><span class="sxs-lookup"><span data-stu-id="b64ee-111">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 <span data-ttu-id="b64ee-112">Примеры определения расширяющие и сужающие преобразования операторы, в разделе [как: определение оператора преобразования](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md).</span><span class="sxs-lookup"><span data-stu-id="b64ee-112">For example definitions of widening and narrowing conversion operators, see [How to: Define a Conversion Operator](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b64ee-113">См. также</span><span class="sxs-lookup"><span data-stu-id="b64ee-113">See Also</span></span>  
 [<span data-ttu-id="b64ee-114">Оператор Statement</span><span class="sxs-lookup"><span data-stu-id="b64ee-114">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
 [<span data-ttu-id="b64ee-115">Narrowing</span><span class="sxs-lookup"><span data-stu-id="b64ee-115">Narrowing</span></span>](../../../visual-basic/language-reference/modifiers/narrowing.md)  
 [<span data-ttu-id="b64ee-116">Расширяющие и сужающие преобразования</span><span class="sxs-lookup"><span data-stu-id="b64ee-116">Widening and Narrowing Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)  
 [<span data-ttu-id="b64ee-117">Практическое руководство. Определение оператора</span><span class="sxs-lookup"><span data-stu-id="b64ee-117">How to: Define an Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)  
 [<span data-ttu-id="b64ee-118">Функция CType</span><span class="sxs-lookup"><span data-stu-id="b64ee-118">CType Function</span></span>](../../../visual-basic/language-reference/functions/ctype-function.md)  
 [<span data-ttu-id="b64ee-119">Оператор Option Strict</span><span class="sxs-lookup"><span data-stu-id="b64ee-119">Option Strict Statement</span></span>](../../../visual-basic/language-reference/statements/option-strict-statement.md)  
 [<span data-ttu-id="b64ee-120">Практическое руководство. Определение оператора преобразования</span><span class="sxs-lookup"><span data-stu-id="b64ee-120">How to: Define a Conversion Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
