---
title: "Многомерные массивы (Руководство по программированию на C#)"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- arrays [C#], multidimensional
- multidimensional arrays [C#]
ms.assetid: 020ce02e-7dff-4273-8e53-bf0b33747232
caps.latest.revision: 16
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
ms.openlocfilehash: 0203046e2038e97cf791141f6863fd8940b22ea4
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="multidimensional-arrays-c-programming-guide"></a><span data-ttu-id="b26f7-102">Многомерные массивы (Руководство по программированию на C#)</span><span class="sxs-lookup"><span data-stu-id="b26f7-102">Multidimensional Arrays (C# Programming Guide)</span></span>
<span data-ttu-id="b26f7-103">Массивы могут иметь несколько измерений.</span><span class="sxs-lookup"><span data-stu-id="b26f7-103">Arrays can have more than one dimension.</span></span> <span data-ttu-id="b26f7-104">Например, следующее объявление создает двухмерный массив из четырех строк и двух столбцов.</span><span class="sxs-lookup"><span data-stu-id="b26f7-104">For example, the following declaration creates a two-dimensional array of four rows and two columns.</span></span>  
  
 <span data-ttu-id="b26f7-105">[!code-cs[csProgGuideArrays#11](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="b26f7-105">[!code-cs[csProgGuideArrays#11](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_1.cs)]</span></span>  
  
 <span data-ttu-id="b26f7-106">Следующее объявление создает массив из трех измерений: 4, 2 и 3.</span><span class="sxs-lookup"><span data-stu-id="b26f7-106">The following declaration creates an array of three dimensions, 4, 2, and 3.</span></span>  
  
 <span data-ttu-id="b26f7-107">[!code-cs[csProgGuideArrays#12](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_2.cs)]</span><span class="sxs-lookup"><span data-stu-id="b26f7-107">[!code-cs[csProgGuideArrays#12](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_2.cs)]</span></span>  
  
## <a name="array-initialization"></a><span data-ttu-id="b26f7-108">Инициализация массива</span><span class="sxs-lookup"><span data-stu-id="b26f7-108">Array Initialization</span></span>  
 <span data-ttu-id="b26f7-109">Массив можно инициализировать при объявлении, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b26f7-109">You can initialize the array upon declaration, as is shown in the following example.</span></span>  
  
 <span data-ttu-id="b26f7-110">[!code-cs[csProgGuideArrays#13](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_3.cs)]</span><span class="sxs-lookup"><span data-stu-id="b26f7-110">[!code-cs[csProgGuideArrays#13](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_3.cs)]</span></span>  
  
 <span data-ttu-id="b26f7-111">Также можно инициализировать массив без указания ранга.</span><span class="sxs-lookup"><span data-stu-id="b26f7-111">You also can initialize the array without specifying the rank.</span></span>  
  
 <span data-ttu-id="b26f7-112">[!code-cs[csProgGuideArrays#14](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_4.cs)]</span><span class="sxs-lookup"><span data-stu-id="b26f7-112">[!code-cs[csProgGuideArrays#14](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_4.cs)]</span></span>  
  
 <span data-ttu-id="b26f7-113">Чтобы объявить переменную массива без инициализации, используйте оператор `new` для присвоения массива переменной.</span><span class="sxs-lookup"><span data-stu-id="b26f7-113">If you choose to declare an array variable without initialization, you must use the `new` operator to assign an array to the variable.</span></span> <span data-ttu-id="b26f7-114">Использование оператора `new` показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b26f7-114">The use of `new` is shown in the following example.</span></span>  
  
 <span data-ttu-id="b26f7-115">[!code-cs[csProgGuideArrays#15](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_5.cs)]</span><span class="sxs-lookup"><span data-stu-id="b26f7-115">[!code-cs[csProgGuideArrays#15](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_5.cs)]</span></span>  
  
 <span data-ttu-id="b26f7-116">В следующем примере присваивается значение конкретному элементу массива.</span><span class="sxs-lookup"><span data-stu-id="b26f7-116">The following example assigns a value to a particular array element.</span></span>  
  
 <span data-ttu-id="b26f7-117">[!code-cs[csProgGuideArrays#16](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_6.cs)]</span><span class="sxs-lookup"><span data-stu-id="b26f7-117">[!code-cs[csProgGuideArrays#16](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_6.cs)]</span></span>  
  
 <span data-ttu-id="b26f7-118">Аналогичным образом, в следующем примере получается значение конкретного элемента массива, которое присваивается переменной `elementValue`.</span><span class="sxs-lookup"><span data-stu-id="b26f7-118">Similarly, the following example gets the value of a particular array element and assigns it to variable `elementValue`.</span></span>  
  
 <span data-ttu-id="b26f7-119">[!code-cs[csProgGuideArrays#42](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_7.cs)]</span><span class="sxs-lookup"><span data-stu-id="b26f7-119">[!code-cs[csProgGuideArrays#42](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_7.cs)]</span></span>  
  
 <span data-ttu-id="b26f7-120">В следующем примере кода элементы массива инициализируются с использованием значений по умолчанию (кроме массивов массивов).</span><span class="sxs-lookup"><span data-stu-id="b26f7-120">The following code example initializes the array elements to default values (except for jagged arrays).</span></span>  
  
 <span data-ttu-id="b26f7-121">[!code-cs[csProgGuideArrays#17](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_8.cs)]</span><span class="sxs-lookup"><span data-stu-id="b26f7-121">[!code-cs[csProgGuideArrays#17](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_8.cs)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b26f7-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b26f7-122">See Also</span></span>  
 <span data-ttu-id="b26f7-123">[Руководство по программированию на C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="b26f7-123">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="b26f7-124">[Массивы](../../../csharp/programming-guide/arrays/index.md) </span><span class="sxs-lookup"><span data-stu-id="b26f7-124">[Arrays](../../../csharp/programming-guide/arrays/index.md) </span></span>  
 <span data-ttu-id="b26f7-125">[Одномерные массивы](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md) </span><span class="sxs-lookup"><span data-stu-id="b26f7-125">[Single-Dimensional Arrays](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md) </span></span>  
 [<span data-ttu-id="b26f7-126">Массивы массивов</span><span class="sxs-lookup"><span data-stu-id="b26f7-126">Jagged Arrays</span></span>](../../../csharp/programming-guide/arrays/jagged-arrays.md)

