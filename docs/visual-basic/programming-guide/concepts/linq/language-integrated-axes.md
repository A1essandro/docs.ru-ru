---
title: Загрузка встроенных в язык осей в Visual Basic (LINQ to XML)
ms.custom: ''
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: d450a556-a134-4261-b011-44e399660894
caps.latest.revision: 3
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 8360281d1d8de0cad243297cd78e97958530bae4
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2018
---
# <a name="language-integrated-axes-in-visual-basic-linq-to-xml"></a><span data-ttu-id="affd0-102">Загрузка встроенных в язык осей в Visual Basic (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="affd0-102">Language-Integrated Axes in Visual Basic (LINQ to XML)</span></span>
<span data-ttu-id="affd0-103">В этом разделе описаны компоненты, созданные непосредственно в язык Visual Basic, чтобы облегчить доступ к XML.</span><span class="sxs-lookup"><span data-stu-id="affd0-103">This section describes features built directly into the Visual Basic language to make it easy to access XML.</span></span> <span data-ttu-id="affd0-104">Во многих примерах в LINQ к XML-документации используются эти интеграции оси Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="affd0-104">Many of the examples in the LINQ to XML documentation use these integrated Visual Basic axes.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="affd0-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="affd0-105">In This Section</span></span>  
  
|<span data-ttu-id="affd0-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="affd0-106">Topic</span></span>|<span data-ttu-id="affd0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="affd0-107">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="affd0-108">Свойство дочерней оси XML</span><span class="sxs-lookup"><span data-stu-id="affd0-108">XML Child Axis Property</span></span>](../../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md)|<span data-ttu-id="affd0-109">Предоставляет доступ к дочерним элементам одного из следующих: объекта <xref:System.Xml.Linq.XElement>, объекта <xref:System.Xml.Linq.XDocument>, коллекции объектов <xref:System.Xml.Linq.XElement> или коллекции объектов <xref:System.Xml.Linq.XDocument>.</span><span class="sxs-lookup"><span data-stu-id="affd0-109">Provides access to the children of one of the following: an <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, a collection of <xref:System.Xml.Linq.XElement> objects, or a collection of <xref:System.Xml.Linq.XDocument> objects.</span></span> <span data-ttu-id="affd0-110">Эта ось эквивалентна оси <xref:System.Xml.Linq.XContainer.Elements%2A>.</span><span class="sxs-lookup"><span data-stu-id="affd0-110">This axis is equivalent to the <xref:System.Xml.Linq.XContainer.Elements%2A> axis.</span></span>|  
|[<span data-ttu-id="affd0-111">Свойство дочерней оси XML</span><span class="sxs-lookup"><span data-stu-id="affd0-111">XML Descendant Axis Property</span></span>](../../../../visual-basic/language-reference/xml-axis/xml-descendant-axis-property.md)|<span data-ttu-id="affd0-112">Предоставляет доступ к потомкам из следующих: объекта <xref:System.Xml.Linq.XElement>, объекта <xref:System.Xml.Linq.XDocument> или коллекции объектов <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="affd0-112">Provides access to the descendants of the following: an <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, or a collection of <xref:System.Xml.Linq.XElement> objects.</span></span> <span data-ttu-id="affd0-113">Эта ось эквивалентна оси <xref:System.Xml.Linq.XContainer.Descendants%2A>.</span><span class="sxs-lookup"><span data-stu-id="affd0-113">This axis is equivalent to the <xref:System.Xml.Linq.XContainer.Descendants%2A> axis.</span></span>|  
|[<span data-ttu-id="affd0-114">Свойство оси атрибута XML</span><span class="sxs-lookup"><span data-stu-id="affd0-114">XML Attribute Axis Property</span></span>](../../../../visual-basic/language-reference/xml-axis/xml-attribute-axis-property.md)|<span data-ttu-id="affd0-115">Обеспечивает доступ к атрибуту объекта <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="affd0-115">Provides access to an attribute of an <xref:System.Xml.Linq.XElement> object.</span></span> <span data-ttu-id="affd0-116">Эта ось примерно эквивалентна оси <xref:System.Xml.Linq.XElement.Attribute%2A>.</span><span class="sxs-lookup"><span data-stu-id="affd0-116">This axis is roughly equivalent to the <xref:System.Xml.Linq.XElement.Attribute%2A> axis.</span></span> <span data-ttu-id="affd0-117">Эта ось отличается от оси <xref:System.Xml.Linq.XElement.Attribute%2A> в том, что она возвращает значение атрибута, а не объект <xref:System.Xml.Linq.XAttribute>.</span><span class="sxs-lookup"><span data-stu-id="affd0-117">This axis differs from the <xref:System.Xml.Linq.XElement.Attribute%2A> axis in that it returns the value of the attribute, not an <xref:System.Xml.Linq.XAttribute> object.</span></span>|  
|[<span data-ttu-id="affd0-118">Свойство индексатора расширения</span><span class="sxs-lookup"><span data-stu-id="affd0-118">Extension Indexer Property</span></span>](../../../../visual-basic/language-reference/xml-axis/extension-indexer-property.md)|<span data-ttu-id="affd0-119">Обеспечивает доступ к отдельным элементам коллекции.</span><span class="sxs-lookup"><span data-stu-id="affd0-119">Provides access to individual elements in a collection.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="affd0-120">См. также</span><span class="sxs-lookup"><span data-stu-id="affd0-120">See Also</span></span>  
 [<span data-ttu-id="affd0-121">Оси LINQ to XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="affd0-121">LINQ to XML Axes (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-axes.md)
