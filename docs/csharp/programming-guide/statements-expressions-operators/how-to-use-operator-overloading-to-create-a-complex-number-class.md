---
title: "Практическое руководство. Перегрузка операторов для реализации класса комплексных чисел (Руководство по программированию в C#)"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- complex numbers [C#]
- classes [C#], operator overloading
- operator overloading [C#], complex numbers
- operator overloading [C#], using to create classes
- operators [C#], overloading to create a complex number class
ms.assetid: c9b8d982-5112-413f-bae3-b42ae3248ddf
caps.latest.revision: 15
author: BillWagner
ms.author: wiwagn
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 2ce629320744d46787aaabba48740f05c917fdcb
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="how-to-use-operator-overloading-to-create-a-complex-number-class-c-programming-guide"></a><span data-ttu-id="f512b-102">Практическое руководство. Перегрузка операторов для реализации класса комплексных чисел (Руководство по программированию в C#)</span><span class="sxs-lookup"><span data-stu-id="f512b-102">How to: Use Operator Overloading to Create a Complex Number Class (C# Programming Guide)</span></span>
<span data-ttu-id="f512b-103">В этом примере показывается, как использовать перегрузку оператора для создания класса комплексных чисел `Complex`, определяющего сложение комплексных чисел.</span><span class="sxs-lookup"><span data-stu-id="f512b-103">This example shows how you can use operator overloading to create a complex number class `Complex` that defines complex addition.</span></span> <span data-ttu-id="f512b-104">Программа выводит мнимую и реальную части чисел, а также результат сложения, используя переопределение метода `ToString`.</span><span class="sxs-lookup"><span data-stu-id="f512b-104">The program displays the imaginary and the real parts of the numbers and the addition result using an override of the `ToString` method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f512b-105">Пример</span><span class="sxs-lookup"><span data-stu-id="f512b-105">Example</span></span>  
 <span data-ttu-id="f512b-106">[!code-cs[csProgGuideStatements#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-operator-overloading-to-create-a-complex-number-class_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="f512b-106">[!code-cs[csProgGuideStatements#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-operator-overloading-to-create-a-complex-number-class_1.cs)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f512b-107">См. также</span><span class="sxs-lookup"><span data-stu-id="f512b-107">See Also</span></span>  
 <span data-ttu-id="f512b-108">[Руководство по программированию на C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="f512b-108">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="f512b-109">[Операторы в C#](../../../csharp/language-reference/operators/index.md) </span><span class="sxs-lookup"><span data-stu-id="f512b-109">[C# Operators](../../../csharp/language-reference/operators/index.md) </span></span>  
 <span data-ttu-id="f512b-110">[Оператор (справочник по C#)](../../../csharp/language-reference/keywords/operator.md) </span><span class="sxs-lookup"><span data-stu-id="f512b-110">[operator (C# Reference)](../../../csharp/language-reference/keywords/operator.md) </span></span>  
 [<span data-ttu-id="f512b-111">Почему перегруженные операторы всегда являются статическими в C#?</span><span class="sxs-lookup"><span data-stu-id="f512b-111">Why are overloaded operators always static in C#?</span></span>](http://go.microsoft.com/fwlink/?LinkId=112383)

