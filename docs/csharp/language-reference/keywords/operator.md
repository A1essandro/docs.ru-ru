---
title: "operator (Справочник по C#)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
f1_keywords:
- operator_CSharpKeyword
- operator
helpviewer_keywords: operator keyword [C#]
ms.assetid: 59218cce-e90e-42f6-a6bb-30300981b86a
caps.latest.revision: "19"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 1d035319318a710ccee62a0c64ce5981767a21ca
ms.sourcegitcommit: 8bde7a3432f30fc771079744955c75c58c4eb393
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/20/2018
---
# <a name="operator-c-reference"></a><span data-ttu-id="73d42-102">operator (Справочник по C#)</span><span class="sxs-lookup"><span data-stu-id="73d42-102">operator (C# Reference)</span></span>
<span data-ttu-id="73d42-103">Ключевое слово `operator` используется для перегрузки встроенного оператора или выполнения пользовательского преобразования в объявлении класса или структуры.</span><span class="sxs-lookup"><span data-stu-id="73d42-103">Use the `operator` keyword to overload a built-in operator or to provide a user-defined conversion in a class or struct declaration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="73d42-104">Пример</span><span class="sxs-lookup"><span data-stu-id="73d42-104">Example</span></span>  
 <span data-ttu-id="73d42-105">Ниже приведен сильно упрощенный класс для дробных чисел.</span><span class="sxs-lookup"><span data-stu-id="73d42-105">The following is a very simplified class for fractional numbers.</span></span> <span data-ttu-id="73d42-106">Он перегружает операторы `+` и `*` для выполнения сложения и умножения, а также предоставляет оператор преобразования, который преобразует тип `Fraction` в тип `double`.</span><span class="sxs-lookup"><span data-stu-id="73d42-106">It overloads the `+` and `*` operators to perform fractional addition and multiplication, and also provides a conversion operator that converts a `Fraction` type to a `double` type.</span></span>  
  
 [!code-csharp[csrefKeywordsConversion#6](../../../csharp/language-reference/keywords/codesnippet/CSharp/operator_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="73d42-107">Спецификация языка C#</span><span class="sxs-lookup"><span data-stu-id="73d42-107">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="73d42-108">См. также</span><span class="sxs-lookup"><span data-stu-id="73d42-108">See Also</span></span>  
 [<span data-ttu-id="73d42-109">Справочник по C#</span><span class="sxs-lookup"><span data-stu-id="73d42-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="73d42-110">Руководство по программированию на C#</span><span class="sxs-lookup"><span data-stu-id="73d42-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="73d42-111">Ключевые слова в C#</span><span class="sxs-lookup"><span data-stu-id="73d42-111">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="73d42-112">implicit</span><span class="sxs-lookup"><span data-stu-id="73d42-112">implicit</span></span>](../../../csharp/language-reference/keywords/implicit.md)  
 [<span data-ttu-id="73d42-113">explicit</span><span class="sxs-lookup"><span data-stu-id="73d42-113">explicit</span></span>](../../../csharp/language-reference/keywords/explicit.md)  
 [<span data-ttu-id="73d42-114">Практическое руководство. Реализация определенных пользователем преобразований между структурами</span><span class="sxs-lookup"><span data-stu-id="73d42-114">How to: Implement User-Defined Conversions Between Structs</span></span>](../../../csharp/programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)
