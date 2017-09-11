---
title: "Секционирование данных (Visual Basic) | Документы Microsoft"
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
ms.assetid: 69c59379-b66e-422c-b324-5b5c07760ef7
caps.latest.revision: 3
author: dotnet-bot
ms.author: dotnetcontent
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 9d0df2bc473f48fba4bbb094317166407f7c7ec2
ms.contentlocale: ru-ru
ms.lasthandoff: 04/12/2017

---
# <a name="partitioning-data-visual-basic"></a><span data-ttu-id="7621e-102">Секционирование данных (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7621e-102">Partitioning Data (Visual Basic)</span></span>
<span data-ttu-id="7621e-103">Секционирование в LINQ — это операция разделения входной последовательности на два раздела без изменения порядка элементов, а затем возвращения одного из разделов.</span><span class="sxs-lookup"><span data-stu-id="7621e-103">Partitioning in LINQ refers to the operation of dividing an input sequence into two sections, without rearranging the elements, and then returning one of the sections.</span></span>  
  
 <span data-ttu-id="7621e-104">Ниже показаны результаты трех различных операций секционирования в последовательности символов.</span><span class="sxs-lookup"><span data-stu-id="7621e-104">The following illustration shows the results of three different partitioning operations on a sequence of characters.</span></span> <span data-ttu-id="7621e-105">Первая операция возвращает первые три элемента в последовательности.</span><span class="sxs-lookup"><span data-stu-id="7621e-105">The first operation returns the first three elements in the sequence.</span></span> <span data-ttu-id="7621e-106">Вторая операция пропускает первые три элемента и возвращает остальные элементы.</span><span class="sxs-lookup"><span data-stu-id="7621e-106">The second operation skips the first three elements and returns the remaining elements.</span></span> <span data-ttu-id="7621e-107">Третья операция пропускает первые два элемента в последовательности и возвращает три следующих элемента.</span><span class="sxs-lookup"><span data-stu-id="7621e-107">The third operation skips the first two elements in the sequence and returns the next three elements.</span></span>  
  
 <span data-ttu-id="7621e-108">![Операции секционирования LINQ](../../../../csharp/programming-guide/concepts/linq/media/linq_partition.png "LINQ_Partition")</span><span class="sxs-lookup"><span data-stu-id="7621e-108">![LINQ Partitioning Operations](../../../../csharp/programming-guide/concepts/linq/media/linq_partition.png "LINQ_Partition")</span></span>  
  
 <span data-ttu-id="7621e-109">В следующем разделе перечислены методы стандартных операторов запросов, выполняют секционирование.</span><span class="sxs-lookup"><span data-stu-id="7621e-109">The standard query operator methods that partition sequences are listed in the following section.</span></span>  
  
## <a name="operators"></a><span data-ttu-id="7621e-110">Операторы</span><span class="sxs-lookup"><span data-stu-id="7621e-110">Operators</span></span>  
  
|<span data-ttu-id="7621e-111">Имя оператора</span><span class="sxs-lookup"><span data-stu-id="7621e-111">Operator Name</span></span>|<span data-ttu-id="7621e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7621e-112">Description</span></span>|<span data-ttu-id="7621e-113">Синтаксис выражения запроса для Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7621e-113">Visual Basic Query Expression Syntax</span></span>|<span data-ttu-id="7621e-114">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="7621e-114">More Information</span></span>|  
|-------------------|-----------------|------------------------------------------|----------------------|  
|<span data-ttu-id="7621e-115">Пропустить</span><span class="sxs-lookup"><span data-stu-id="7621e-115">Skip</span></span>|<span data-ttu-id="7621e-116">Пропускает элементы до указанной позиции в последовательности.</span><span class="sxs-lookup"><span data-stu-id="7621e-116">Skips elements up to a specified position in a sequence.</span></span>|`Skip`|<span data-ttu-id="7621e-117"><xref:System.Linq.Enumerable.Skip%2A?displayProperty=fullName></xref:System.Linq.Enumerable.Skip%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="7621e-117"><xref:System.Linq.Enumerable.Skip%2A?displayProperty=fullName></span></span><br /><br /> <span data-ttu-id="7621e-118"><xref:System.Linq.Queryable.Skip%2A?displayProperty=fullName></xref:System.Linq.Queryable.Skip%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="7621e-118"><xref:System.Linq.Queryable.Skip%2A?displayProperty=fullName></span></span>|  
|<span data-ttu-id="7621e-119">SkipWhile</span><span class="sxs-lookup"><span data-stu-id="7621e-119">SkipWhile</span></span>|<span data-ttu-id="7621e-120">Пропускает элементы, пока элемент не удовлетворит условию функции предиката.</span><span class="sxs-lookup"><span data-stu-id="7621e-120">Skips elements based on a predicate function until an element does not satisfy the condition.</span></span>|`Skip While`|<span data-ttu-id="7621e-121"><xref:System.Linq.Enumerable.SkipWhile%2A?displayProperty=fullName></xref:System.Linq.Enumerable.SkipWhile%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="7621e-121"><xref:System.Linq.Enumerable.SkipWhile%2A?displayProperty=fullName></span></span><br /><br /> <span data-ttu-id="7621e-122"><xref:System.Linq.Queryable.SkipWhile%2A?displayProperty=fullName></xref:System.Linq.Queryable.SkipWhile%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="7621e-122"><xref:System.Linq.Queryable.SkipWhile%2A?displayProperty=fullName></span></span>|  
|<span data-ttu-id="7621e-123">Take</span><span class="sxs-lookup"><span data-stu-id="7621e-123">Take</span></span>|<span data-ttu-id="7621e-124">Возвращает элементы указанной позиции в последовательности.</span><span class="sxs-lookup"><span data-stu-id="7621e-124">Takes elements up to a specified position in a sequence.</span></span>|`Take`|<span data-ttu-id="7621e-125"><xref:System.Linq.Enumerable.Take%2A?displayProperty=fullName></xref:System.Linq.Enumerable.Take%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="7621e-125"><xref:System.Linq.Enumerable.Take%2A?displayProperty=fullName></span></span><br /><br /> <span data-ttu-id="7621e-126"><xref:System.Linq.Queryable.Take%2A?displayProperty=fullName></xref:System.Linq.Queryable.Take%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="7621e-126"><xref:System.Linq.Queryable.Take%2A?displayProperty=fullName></span></span>|  
|<span data-ttu-id="7621e-127">TakeWhile</span><span class="sxs-lookup"><span data-stu-id="7621e-127">TakeWhile</span></span>|<span data-ttu-id="7621e-128">Принимает элементы, пока элемент не удовлетворит условию функции предиката.</span><span class="sxs-lookup"><span data-stu-id="7621e-128">Takes elements based on a predicate function until an element does not satisfy the condition.</span></span>|`Take While`|<span data-ttu-id="7621e-129"><xref:System.Linq.Enumerable.TakeWhile%2A?displayProperty=fullName></xref:System.Linq.Enumerable.TakeWhile%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="7621e-129"><xref:System.Linq.Enumerable.TakeWhile%2A?displayProperty=fullName></span></span><br /><br /> <span data-ttu-id="7621e-130"><xref:System.Linq.Queryable.TakeWhile%2A?displayProperty=fullName></xref:System.Linq.Queryable.TakeWhile%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="7621e-130"><xref:System.Linq.Queryable.TakeWhile%2A?displayProperty=fullName></span></span>|  
  
## <a name="query-expression-syntax-examples"></a><span data-ttu-id="7621e-131">Примеры синтаксиса выражений запросов</span><span class="sxs-lookup"><span data-stu-id="7621e-131">Query Expression Syntax Examples</span></span>  
  
### <a name="skip"></a><span data-ttu-id="7621e-132">Пропустить</span><span class="sxs-lookup"><span data-stu-id="7621e-132">Skip</span></span>  
 <span data-ttu-id="7621e-133">В следующем примере кода `Skip` предложения в [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] для пропуска первых четырех строк в массиве строк перед возвращением оставшихся строк в массиве.</span><span class="sxs-lookup"><span data-stu-id="7621e-133">The following code example uses the `Skip` clause in [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] to skip over the first four strings in an array of strings before returning the remaining strings in the array.</span></span>  
  
 <span data-ttu-id="7621e-134">[!code-vb[CsLINQPartitioning&#1;](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/partitioning-data_1.vb)]</span><span class="sxs-lookup"><span data-stu-id="7621e-134">[!code-vb[CsLINQPartitioning#1](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/partitioning-data_1.vb)]</span></span>  
  
### <a name="skipwhile"></a><span data-ttu-id="7621e-135">SkipWhile</span><span class="sxs-lookup"><span data-stu-id="7621e-135">SkipWhile</span></span>  
 <span data-ttu-id="7621e-136">В следующем примере кода `Skip While` предложения в [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] для пропуска строк в массиве, начинающихся с буквы «».</span><span class="sxs-lookup"><span data-stu-id="7621e-136">The following code example uses the `Skip While` clause in [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] to skip over the strings in an array while the first letter of the string is "a".</span></span> <span data-ttu-id="7621e-137">Оставшиеся строки массива возвращаются.</span><span class="sxs-lookup"><span data-stu-id="7621e-137">The remaining strings in the array are returned.</span></span>  
  
 <span data-ttu-id="7621e-138">[!code-vb[CsLINQPartitioning&#2;](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/partitioning-data_2.vb)]</span><span class="sxs-lookup"><span data-stu-id="7621e-138">[!code-vb[CsLINQPartitioning#2](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/partitioning-data_2.vb)]</span></span>  
  
### <a name="take"></a><span data-ttu-id="7621e-139">Take</span><span class="sxs-lookup"><span data-stu-id="7621e-139">Take</span></span>  
 <span data-ttu-id="7621e-140">В следующем примере кода `Take` предложения в [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] для возврата первых двух строк в массиве строк.</span><span class="sxs-lookup"><span data-stu-id="7621e-140">The following code example uses the `Take` clause in [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] to return the first two strings in an array of strings.</span></span>  
  
 <span data-ttu-id="7621e-141">[!code-vb[CsLINQPartitioning&#3;](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/partitioning-data_3.vb)]</span><span class="sxs-lookup"><span data-stu-id="7621e-141">[!code-vb[CsLINQPartitioning#3](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/partitioning-data_3.vb)]</span></span>  
  
### <a name="takewhile"></a><span data-ttu-id="7621e-142">TakeWhile</span><span class="sxs-lookup"><span data-stu-id="7621e-142">TakeWhile</span></span>  
 <span data-ttu-id="7621e-143">В следующем примере кода `Take While` предложения в [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] для возврата из массива строк, тогда как длина строки меньше пяти.</span><span class="sxs-lookup"><span data-stu-id="7621e-143">The following code example uses the `Take While` clause in [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] to return strings from an array while the length of the string is five or less.</span></span>  
  
 <span data-ttu-id="7621e-144">[!code-vb[CsLINQPartitioning&#4;](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/partitioning-data_4.vb)]</span><span class="sxs-lookup"><span data-stu-id="7621e-144">[!code-vb[CsLINQPartitioning#4](../../../../visual-basic/programming-guide/concepts/linq/codesnippet/VisualBasic/partitioning-data_4.vb)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7621e-145">См. также</span><span class="sxs-lookup"><span data-stu-id="7621e-145">See Also</span></span>  
 <span data-ttu-id="7621e-146"><xref:System.Linq></xref:System.Linq></span><span class="sxs-lookup"><span data-stu-id="7621e-146"><xref:System.Linq></span></span>   
<span data-ttu-id="7621e-147"> [Общие сведения о стандартных операторах (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md) </span><span class="sxs-lookup"><span data-stu-id="7621e-147"> [Standard Query Operators Overview (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md) </span></span>  
<span data-ttu-id="7621e-148"> [Предложение SKIP](../../../../visual-basic/language-reference/queries/skip-clause.md) </span><span class="sxs-lookup"><span data-stu-id="7621e-148"> [Skip Clause](../../../../visual-basic/language-reference/queries/skip-clause.md) </span></span>  
<span data-ttu-id="7621e-149"> [Предложение Skip While](../../../../visual-basic/language-reference/queries/skip-while-clause.md) </span><span class="sxs-lookup"><span data-stu-id="7621e-149"> [Skip While Clause](../../../../visual-basic/language-reference/queries/skip-while-clause.md) </span></span>  
<span data-ttu-id="7621e-150"> [Предложение Take](../../../../visual-basic/language-reference/queries/take-clause.md) </span><span class="sxs-lookup"><span data-stu-id="7621e-150"> [Take Clause](../../../../visual-basic/language-reference/queries/take-clause.md) </span></span>  
<span data-ttu-id="7621e-151"> [Предложение Take While](../../../../visual-basic/language-reference/queries/take-while-clause.md)</span><span class="sxs-lookup"><span data-stu-id="7621e-151"> [Take While Clause](../../../../visual-basic/language-reference/queries/take-while-clause.md)</span></span>
