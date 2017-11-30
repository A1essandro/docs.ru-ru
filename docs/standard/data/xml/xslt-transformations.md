---
title: "Преобразования XSLT"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 202f8820-224c-494f-b61e-cd127eac6e03
caps.latest.revision: "4"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 0d7fa8492487daff68fd8ebaf4159dd537d13e51
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="xslt-transformations"></a><span data-ttu-id="68f78-102">Преобразования XSLT</span><span class="sxs-lookup"><span data-stu-id="68f78-102">XSLT Transformations</span></span>
<span data-ttu-id="68f78-103">Язык XSLT позволяет преобразовать содержимое исходного XML-документа в другой документ, отличный по формату или структуре.</span><span class="sxs-lookup"><span data-stu-id="68f78-103">The Extensible Stylesheet Language Transformation (XSLT) lets you transform the content of a source XML document into another document that is different in format or structure.</span></span> <span data-ttu-id="68f78-104">Например, с помощью XSLT можно преобразовать XML в HTML для использования на веб-узле или преобразовать в документ, в котором будут только поля, необходимые приложению.</span><span class="sxs-lookup"><span data-stu-id="68f78-104">For example, you can use XSLT to transform XML into HTML for use on a Web site or to transform it into a document that contains only the fields required by an application.</span></span> <span data-ttu-id="68f78-105">Этот процесс преобразования определяется [преобразований XSL (XSLT) W3C версии 1.0](http://go.microsoft.com/fwlink/?LinkID=49919).</span><span class="sxs-lookup"><span data-stu-id="68f78-105">This transformation process is specified by the [W3C XSL Transformations (XSLT) Version 1.0 recommendation](http://go.microsoft.com/fwlink/?LinkID=49919).</span></span>  
  
 <span data-ttu-id="68f78-106">Класс <xref:System.Xml.Xsl.XslCompiledTransform> является обработчиком XSLT в платформе .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="68f78-106">The <xref:System.Xml.Xsl.XslCompiledTransform> class is the XSLT processor in the .NET Framework.</span></span> <span data-ttu-id="68f78-107">Класс <xref:System.Xml.Xsl.XslCompiledTransform> поддерживает рекомендации W3C XSLT 1.0.</span><span class="sxs-lookup"><span data-stu-id="68f78-107">The <xref:System.Xml.Xsl.XslCompiledTransform> class supports the W3C XSLT 1.0 recommendation.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="68f78-108">Класс <xref:System.Xml.Xsl.XslTransform> в платформе .NET Framework версии 2.0 является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="68f78-108">The <xref:System.Xml.Xsl.XslTransform> class is obsolete in .NET Framework version 2.0.</span></span> <span data-ttu-id="68f78-109">Класс <xref:System.Xml.Xsl.XslCompiledTransform> является новой реализацией обработчика XSLT.</span><span class="sxs-lookup"><span data-stu-id="68f78-109">The <xref:System.Xml.Xsl.XslCompiledTransform> class is a new implementation of the XSLT engine.</span></span> <span data-ttu-id="68f78-110">Улучшена его производительность и добавлены новые средства безопасности.</span><span class="sxs-lookup"><span data-stu-id="68f78-110">It includes performance improvements and new security features.</span></span> <span data-ttu-id="68f78-111">XSLT-приложения рекомендуется создавать с помощью класса <xref:System.Xml.Xsl.XslCompiledTransform></span><span class="sxs-lookup"><span data-stu-id="68f78-111">The recommended practice is to create XSLT applications using the <xref:System.Xml.Xsl.XslCompiledTransform> class.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="68f78-112">Содержание</span><span class="sxs-lookup"><span data-stu-id="68f78-112">In This Section</span></span>  
 [<span data-ttu-id="68f78-113">Использование класса XslCompiledTransform</span><span class="sxs-lookup"><span data-stu-id="68f78-113">Using the XslCompiledTransform Class</span></span>](../../../../docs/standard/data/xml/using-the-xslcompiledtransform-class.md)  
 <span data-ttu-id="68f78-114">Содержит сведения об использовании класса <xref:System.Xml.Xsl.XslCompiledTransform>.</span><span class="sxs-lookup"><span data-stu-id="68f78-114">Provides information on using the <xref:System.Xml.Xsl.XslCompiledTransform> class.</span></span>  
  
 [<span data-ttu-id="68f78-115">Миграция с класса XslTransform</span><span class="sxs-lookup"><span data-stu-id="68f78-115">Migrating From the XslTransform Class</span></span>](../../../../docs/standard/data/xml/migrating-from-the-xsltransform-class.md)  
 <span data-ttu-id="68f78-116">Обсуждается перенос кода из класса <xref:System.Xml.Xsl.XslTransform>.</span><span class="sxs-lookup"><span data-stu-id="68f78-116">Discusses how to migrate code from the <xref:System.Xml.Xsl.XslTransform> class.</span></span>  
  
 [<span data-ttu-id="68f78-117">XSLT-компилятор (xsltc.exe)</span><span class="sxs-lookup"><span data-stu-id="68f78-117">XSLT Compiler (xsltc.exe)</span></span>](../../../../docs/standard/data/xml/xslt-compiler-xsltc-exe.md)  
 <span data-ttu-id="68f78-118">Предоставляются сведения об использовании XSLT-компилятора.</span><span class="sxs-lookup"><span data-stu-id="68f78-118">Provides information on using the XSLT compiler.</span></span>  
  
 [<span data-ttu-id="68f78-119">XSLT-преобразования с помощью класса XslTransform</span><span class="sxs-lookup"><span data-stu-id="68f78-119">XSLT Transformations with the XslTransform Class</span></span>](../../../../docs/standard/data/xml/xslt-transformations-with-the-xsltransform-class.md)  
 <span data-ttu-id="68f78-120">Содержит сведения об использовании класса <xref:System.Xml.Xsl.XslTransform>.</span><span class="sxs-lookup"><span data-stu-id="68f78-120">Provides information on using the <xref:System.Xml.Xsl.XslTransform> class.</span></span>  
  
 <span data-ttu-id="68f78-121">**Примечание** <xref:System.Xml.Xsl.XslTransform> класс не используется в версии .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="68f78-121">**Note** The <xref:System.Xml.Xsl.XslTransform> class is obsolete in the .NET Framework 2.0 release.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="68f78-122">Ссылка</span><span class="sxs-lookup"><span data-stu-id="68f78-122">Reference</span></span>  
 <xref:System.Xml.Xsl.XslCompiledTransform>  
  
 <xref:System.Xml.Xsl.XsltArgumentList>  
  
 <xref:System.Xml.Xsl.XsltSettings>  
  
## <a name="related-sections"></a><span data-ttu-id="68f78-123">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="68f78-123">Related Sections</span></span>  
 [<span data-ttu-id="68f78-124">XML-документы и данные</span><span class="sxs-lookup"><span data-stu-id="68f78-124">XML Documents and Data</span></span>](../../../../docs/standard/data/xml/index.md)
