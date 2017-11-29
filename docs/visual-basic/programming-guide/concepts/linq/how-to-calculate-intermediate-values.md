---
title: "Как: вычисления промежуточных значений (Visual Basic)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 933a97b2-dfe7-4f4d-94ad-e6e20df84abd
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: eaedaf15318ea9ae521cc070e7cd9a267decf330
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-calculate-intermediate-values-visual-basic"></a><span data-ttu-id="6b0d8-102">Как: вычисления промежуточных значений (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6b0d8-102">How to: Calculate Intermediate Values (Visual Basic)</span></span>
<span data-ttu-id="6b0d8-103">В этом примере показано, как вычислять промежуточные значения, которые используются в сортировке, фильтрации и выборке.</span><span class="sxs-lookup"><span data-stu-id="6b0d8-103">This example shows how to calculate intermediate values that can be used in sorting, filtering, and selecting.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6b0d8-104">Пример</span><span class="sxs-lookup"><span data-stu-id="6b0d8-104">Example</span></span>  
 <span data-ttu-id="6b0d8-105">В следующем примере используется предложение `Let`.</span><span class="sxs-lookup"><span data-stu-id="6b0d8-105">The following example uses the `Let` clause.</span></span>  
  
 <span data-ttu-id="6b0d8-106">В этом примере используется следующий XML-документ: [Пример XML-файла. Числовые данные (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="6b0d8-106">This example uses the following XML document: [Sample XML File: Numerical Data (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).</span></span>  
  
```vb  
Dim root As XElement = XElement.Load("Data.xml")  
Dim extensions As IEnumerable(Of Decimal) = _  
    From el In root.<Data> _  
    Let extension = CDec(el.<Quantity>.Value) * CDec(el.<Price>.Value) _  
    Where extension > 25 _  
    Order By extension _  
    Select extension  
For Each ex As Decimal In extensions  
    Console.WriteLine(ex)  
Next  
```  
  
 <span data-ttu-id="6b0d8-107">Этот код выводит следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="6b0d8-107">This code produces the following output:</span></span>  
  
```  
55.92  
73.50  
89.99  
198.00  
435.00  
```  
  
## <a name="example"></a><span data-ttu-id="6b0d8-108">Пример</span><span class="sxs-lookup"><span data-stu-id="6b0d8-108">Example</span></span>  
 <span data-ttu-id="6b0d8-109">Следующий пример демонстрирует тот же запрос XML, что и в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="6b0d8-109">The following example shows the same query for XML that is in a namespace.</span></span> <span data-ttu-id="6b0d8-110">Дополнительные сведения см. в разделе [работа с пространствами имен XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="6b0d8-110">For more information, see [Working with XML Namespaces (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
 <span data-ttu-id="6b0d8-111">В этом примере используется следующий XML-документ: [Пример XML-файла. Числовые данные пространства имен](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="6b0d8-111">This example uses the following XML document: [Sample XML File: Numerical Data in a Namespace](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md).</span></span>  
  
```vb  
Imports <xmlns="http://www.adatum.com">  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = XElement.Load("DataInNamespace.xml")  
        Dim extensions As IEnumerable(Of Decimal) = _  
            From el In root.<Data> _  
            Let extension = CDec(el.<Quantity>.Value) * CDec(el.<Price>.Value) _  
            Where extension > 25 _  
            Order By extension _  
            Select extension  
        For Each ex As Decimal In extensions  
            Console.WriteLine(ex)  
        Next  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="6b0d8-112">Этот код выводит следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="6b0d8-112">This code produces the following output:</span></span>  
  
```  
55.92  
73.50  
89.99  
198.00  
435.00  
```  
  
## <a name="see-also"></a><span data-ttu-id="6b0d8-113">См. также</span><span class="sxs-lookup"><span data-stu-id="6b0d8-113">See Also</span></span>  
 [<span data-ttu-id="6b0d8-114">Базовые запросы (LINQ to XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6b0d8-114">Basic Queries (LINQ to XML) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
