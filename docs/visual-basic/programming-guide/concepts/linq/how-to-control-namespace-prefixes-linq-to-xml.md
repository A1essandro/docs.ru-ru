---
title: "Практическое руководство. Управление префиксами пространств имен (Visual Basic) (LINQ to XML)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 2fcf28a5-31b6-409d-84ea-27c22f71fc9f
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: a48feeb25cc8d28d57edc7421f73b2829f8c19ef
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-control-namespace-prefixes-visual-basic-linq-to-xml"></a><span data-ttu-id="62eb9-102">Практическое руководство. Управление префиксами пространств имен (Visual Basic) (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="62eb9-102">How to: Control Namespace Prefixes (Visual Basic) (LINQ to XML)</span></span>
<span data-ttu-id="62eb9-103">В этом разделе рассматривается управление префиксами пространств имен.</span><span class="sxs-lookup"><span data-stu-id="62eb9-103">This topic describes how you can control namespace prefixes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="62eb9-104">Пример</span><span class="sxs-lookup"><span data-stu-id="62eb9-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="62eb9-105">Описание</span><span class="sxs-lookup"><span data-stu-id="62eb9-105">Description</span></span>  
 <span data-ttu-id="62eb9-106">В этом примере объявляются два пространства имен.</span><span class="sxs-lookup"><span data-stu-id="62eb9-106">This example declares two namespaces.</span></span> <span data-ttu-id="62eb9-107">Указывает, что `http://www.adventure-works.com` пространство имен имеет префикс `aw`и что `www.fourthcoffee.com` пространство имен содержит префикс `fc`.</span><span class="sxs-lookup"><span data-stu-id="62eb9-107">It specifies that the `http://www.adventure-works.com` namespace has the prefix `aw`, and that the `www.fourthcoffee.com` namespace has the prefix of `fc`.</span></span>  
  
### <a name="code"></a><span data-ttu-id="62eb9-108">Код</span><span class="sxs-lookup"><span data-stu-id="62eb9-108">Code</span></span>  
  
```vb  
Imports <xmlns:aw="http://www.adventure-works.com">  
Imports <xmlns:fc="www.fourthcoffee.com">  
  
Module Module1  
  
    Sub Main()  
        Dim root As XElement = _  
            <aw:Root>  
                <fc:Child>  
                    <aw:DifferentChild>other content</aw:DifferentChild>  
                </fc:Child>  
                <aw:Child2>c2 content</aw:Child2>  
                <fc:Child3>c3 content</fc:Child3>  
            </aw:Root>  
        Console.WriteLine(root)  
    End Sub  
  
End Module  
```  
  
### <a name="comments"></a><span data-ttu-id="62eb9-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62eb9-109">Comments</span></span>  
 <span data-ttu-id="62eb9-110">В этом примере выводятся следующие данные:</span><span class="sxs-lookup"><span data-stu-id="62eb9-110">This example produces the following output:</span></span>  
  
```xml  
<aw:Root xmlns:fc="www.fourthcoffee.com" xmlns:aw="http://www.adventure-works.com">  
  <fc:Child>  
    <aw:DifferentChild>other content</aw:DifferentChild>  
  </fc:Child>  
  <aw:Child2>c2 content</aw:Child2>  
  <fc:Child3>c3 content</fc:Child3>  
</aw:Root>  
```  
  
## <a name="see-also"></a><span data-ttu-id="62eb9-111">См. также</span><span class="sxs-lookup"><span data-stu-id="62eb9-111">See Also</span></span>  
 [<span data-ttu-id="62eb9-112">Работа с пространствами имен XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="62eb9-112">Working with XML Namespaces (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md)
