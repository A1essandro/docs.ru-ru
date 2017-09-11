---
title: "Сравнение указателей (Руководство по программированию в C#)"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- pointers [C#], comparison
ms.assetid: fcafd514-7405-4deb-8490-cc58efda5495
caps.latest.revision: 14
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
ms.openlocfilehash: a68a9a419349b8ba09afa27f09086f8316fd0583
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="pointer-comparison-c-programming-guide"></a><span data-ttu-id="403db-102">Сравнение указателей (Руководство по программированию в C#)</span><span class="sxs-lookup"><span data-stu-id="403db-102">Pointer Comparison (C# Programming Guide)</span></span>
<span data-ttu-id="403db-103">Для сравнения указателей любого типа можно применять следующие операторы:</span><span class="sxs-lookup"><span data-stu-id="403db-103">You can apply the following operators to compare pointers of any type:</span></span>  
  
 <span data-ttu-id="403db-104">**==   !=   \<   >   \<=   >=**</span><span class="sxs-lookup"><span data-stu-id="403db-104">**==   !=   \<   >   \<=   >=**</span></span>  
  
 <span data-ttu-id="403db-105">Операторы сравнения сравнивают адреса двух операндов, принимая их как целые числа без знака.</span><span class="sxs-lookup"><span data-stu-id="403db-105">The comparison operators compare the addresses of the two operands as if they are unsigned integers.</span></span>  
  
## <a name="example"></a><span data-ttu-id="403db-106">Пример</span><span class="sxs-lookup"><span data-stu-id="403db-106">Example</span></span>  
 <span data-ttu-id="403db-107">[!code-cs[csProgGuidePointers#16](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-comparison_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="403db-107">[!code-cs[csProgGuidePointers#16](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-comparison_1.cs)]</span></span>  
  
 <span data-ttu-id="403db-108">[!code-cs[csProgGuidePointers#17](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-comparison_2.cs)]</span><span class="sxs-lookup"><span data-stu-id="403db-108">[!code-cs[csProgGuidePointers#17](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-comparison_2.cs)]</span></span>  
  
## <a name="sample-output"></a><span data-ttu-id="403db-109">Пример результатов выполнения</span><span class="sxs-lookup"><span data-stu-id="403db-109">Sample Output</span></span>  
 `True`  
  
 `False`  
  
## <a name="see-also"></a><span data-ttu-id="403db-110">См. также</span><span class="sxs-lookup"><span data-stu-id="403db-110">See Also</span></span>  
 <span data-ttu-id="403db-111">[Руководство по программированию на C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="403db-111">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="403db-112">[Выражения указателей](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md) </span><span class="sxs-lookup"><span data-stu-id="403db-112">[Pointer Expressions](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md) </span></span>  
 <span data-ttu-id="403db-113">[Операторы в C#](../../../csharp/language-reference/operators/index.md) </span><span class="sxs-lookup"><span data-stu-id="403db-113">[C# Operators](../../../csharp/language-reference/operators/index.md) </span></span>  
 <span data-ttu-id="403db-114">[Обработка указателей](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md) </span><span class="sxs-lookup"><span data-stu-id="403db-114">[Manipulating Pointers](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md) </span></span>  
 <span data-ttu-id="403db-115">[Типы указателей](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md) </span><span class="sxs-lookup"><span data-stu-id="403db-115">[Pointer types](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md) </span></span>  
 <span data-ttu-id="403db-116">[Типы](../../../csharp/language-reference/keywords/types.md) </span><span class="sxs-lookup"><span data-stu-id="403db-116">[Types](../../../csharp/language-reference/keywords/types.md) </span></span>  
 <span data-ttu-id="403db-117">[unsafe](../../../csharp/language-reference/keywords/unsafe.md) </span><span class="sxs-lookup"><span data-stu-id="403db-117">[unsafe](../../../csharp/language-reference/keywords/unsafe.md) </span></span>  
 <span data-ttu-id="403db-118">[Оператор fixed](../../../csharp/language-reference/keywords/fixed-statement.md) </span><span class="sxs-lookup"><span data-stu-id="403db-118">[fixed Statement](../../../csharp/language-reference/keywords/fixed-statement.md) </span></span>  
 [<span data-ttu-id="403db-119">stackalloc</span><span class="sxs-lookup"><span data-stu-id="403db-119">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)

