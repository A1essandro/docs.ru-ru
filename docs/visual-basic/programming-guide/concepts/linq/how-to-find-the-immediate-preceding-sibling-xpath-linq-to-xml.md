---
title: Практическое руководство. Найти ближайший предшествующий одноуровневый элемент (XPath-LINQ to XML) (Visual Basic)
ms.date: 07/20/2015
ms.assetid: ec046283-9fe2-4440-b295-860bf700099d
ms.openlocfilehash: ca3602a24b80d9002a639d9a319a731541aeb2df
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2019
ms.locfileid: "58840423"
---
# <a name="how-to-find-the-immediate-preceding-sibling-xpath-linq-to-xml-visual-basic"></a>Практическое руководство. Найти ближайший предшествующий одноуровневый элемент (XPath-LINQ to XML) (Visual Basic)
Иногда требуется найти ближайший предшествующий одноуровневый элемент узла. Из-за разности в семантике позиционных предикатов для осей предшествующих одноуровневых элементов в XPath и в [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] это сравнение является одним из наиболее интересных.  
  
## <a name="example"></a>Пример  
 В этом примере в запросе [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] оператор <xref:System.Linq.Enumerable.Last%2A> используется для обнаружения последнего узла в коллекции, возвращенной методом <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A>. В отличие от этого, в выражении XPath для обнаружения ближайшего предшествующего элемента используется предикат со значением 1.  
  
```vb  
Dim root As XElement = _   
    <Root>  
        <Child1/>  
        <Child2/>  
        <Child3/>  
        <Child4/>  
    </Root>  
Dim child4 As XElement = root.Element("Child4")  
  
' LINQ to XML query  
Dim el1 As XElement = child4.ElementsBeforeSelf().Last()  
  
' XPath expression  
Dim el2 As XElement = _  
    DirectCast(child4.XPathEvaluate("preceding-sibling::*[1]"),  _  
    IEnumerable).Cast(Of XElement)().First()  
  
If el1 Is el2 Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
Console.WriteLine(el1)  
```  
  
 В этом примере выводятся следующие данные:  
  
```  
Results are identical  
<Child3 />  
```  
  
## <a name="see-also"></a>См. также

- [LINQ to XML для пользователей XPath (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
