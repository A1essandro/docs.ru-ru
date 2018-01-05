---
title: "Атрибуты управления сериализацией с кодировкой SOAP"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- SOAP, XML serialization
- XML serialization, SOAP
- XML serialization, attributes
- attributes [.NET Framework], XML serialization
- serialization, attributes
ms.assetid: 93ee258c-9c0f-4a08-897c-c10db7a00f91
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: ae3193a2f9ef01f8e7f71235f15ed070e84ec11c
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/23/2017
---
# <a name="attributes-that-control-encoded-soap-serialization"></a><span data-ttu-id="b88f1-102">Атрибуты управления сериализацией с кодировкой SOAP</span><span class="sxs-lookup"><span data-stu-id="b88f1-102">Attributes That Control Encoded SOAP Serialization</span></span> 
<span data-ttu-id="b88f1-103">В документе "Simple Object Access Protocol (SOAP) 1.1" консорциума World Wide Web Consortium (www.w3.org) содержится дополнительный раздел (раздел 5), в котором описаны способы кодирования параметров SOAP.</span><span class="sxs-lookup"><span data-stu-id="b88f1-103">The World Wide Web Consortium (www.w3.org) document named "Simple Object Access Protocol (SOAP) 1.1" contains an optional section (section 5) that describes how SOAP parameters can be encoded.</span></span> <span data-ttu-id="b88f1-104">Для соответствия разделу 5 спецификации следует использовать специальный набор атрибутов, расположенный в пространстве имен <xref:System.Xml.Serialization>.</span><span class="sxs-lookup"><span data-stu-id="b88f1-104">To conform to section 5 of the specification, you must use a special set of attributes found in the <xref:System.Xml.Serialization> namespace.</span></span> <span data-ttu-id="b88f1-105">Примените эти атрибуты для соответствующих классов и членов классов, а затем используйте <xref:System.Xml.Serialization.XmlSerializer> для сериализации экземпляров класса или классов.</span><span class="sxs-lookup"><span data-stu-id="b88f1-105">Apply those attributes as appropriate to classes and members of classes, and then use the <xref:System.Xml.Serialization.XmlSerializer> to serialize instances of the class or classes.</span></span>  
  
 <span data-ttu-id="b88f1-106">В следующей таблице показаны атрибуты, место их применения и выполняемые ими действия.</span><span class="sxs-lookup"><span data-stu-id="b88f1-106">The following table shows the attributes, where they can be applied, and what they do.</span></span> <span data-ttu-id="b88f1-107">Дополнительные сведения об использовании этих атрибутов для управления XML-сериализации см. в разделах [Практическое руководство. Сериализация объекта как потока XML с кодировкой SOAP](../../../docs/standard/serialization/how-to-serialize-an-object-as-a-soap-encoded-xml-stream.md) и [Практическое руководство. Переопределение сериализации XML с кодировкой SOAP](../../../docs/standard/serialization/how-to-override-encoded-soap-xml-serialization.md).</span><span class="sxs-lookup"><span data-stu-id="b88f1-107">For more information about using these attributes to control XML serialization, see [How to: Serialize an Object as a SOAP-Encoded XML Stream](../../../docs/standard/serialization/how-to-serialize-an-object-as-a-soap-encoded-xml-stream.md) and [How to: Override Encoded SOAP XML Serialization](../../../docs/standard/serialization/how-to-override-encoded-soap-xml-serialization.md).</span></span>  
  
 <span data-ttu-id="b88f1-108">Дополнительные сведения об атрибутах см. в разделе [Атрибуты](../../../docs/standard/attributes/index.md).</span><span class="sxs-lookup"><span data-stu-id="b88f1-108">For more information about attributes, see [Attributes](../../../docs/standard/attributes/index.md).</span></span>  
  
|<span data-ttu-id="b88f1-109">Атрибут</span><span class="sxs-lookup"><span data-stu-id="b88f1-109">Attribute</span></span>|<span data-ttu-id="b88f1-110">Применение</span><span class="sxs-lookup"><span data-stu-id="b88f1-110">Applies to</span></span>|<span data-ttu-id="b88f1-111">Что определяет</span><span class="sxs-lookup"><span data-stu-id="b88f1-111">Specifies</span></span>|  
|---------------|----------------|---------------|  
|<xref:System.Xml.Serialization.SoapAttributeAttribute>|<span data-ttu-id="b88f1-112">Открытое поле, свойство, параметр или возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="b88f1-112">Public field, property, parameter, or return value.</span></span>|<span data-ttu-id="b88f1-113">Член класса должен быть сериализован как атрибут XML.</span><span class="sxs-lookup"><span data-stu-id="b88f1-113">The class member will be serialized as an XML attribute.</span></span>|  
|<xref:System.Xml.Serialization.SoapElementAttribute>|<span data-ttu-id="b88f1-114">Открытое поле, свойство, параметр или возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="b88f1-114">Public field, property, parameter, or return value.</span></span>|<span data-ttu-id="b88f1-115">Класс должен быть сериализован как элемент XML.</span><span class="sxs-lookup"><span data-stu-id="b88f1-115">The class will be serialized as an XML element.</span></span>|  
|<xref:System.Xml.Serialization.SoapEnumAttribute>|<span data-ttu-id="b88f1-116">Открытое поле, являющееся идентификатором перечисления.</span><span class="sxs-lookup"><span data-stu-id="b88f1-116">Public field that is an enumeration identifier.</span></span>|<span data-ttu-id="b88f1-117">Имя элемента члена перечисления.</span><span class="sxs-lookup"><span data-stu-id="b88f1-117">The element name of an enumeration member.</span></span>|  
|<xref:System.Xml.Serialization.SoapIgnoreAttribute>|<span data-ttu-id="b88f1-118">Открытые свойства и поля.</span><span class="sxs-lookup"><span data-stu-id="b88f1-118">Public properties and fields.</span></span>|<span data-ttu-id="b88f1-119">Свойство или поле должно игнорироваться при сериализации содержащего его класса.</span><span class="sxs-lookup"><span data-stu-id="b88f1-119">The property or field should be ignored when the containing class is serialized.</span></span>|  
|<xref:System.Xml.Serialization.SoapIncludeAttribute>|<span data-ttu-id="b88f1-120">Объявления открытых производных классов и открытые методы для документов WSDL.</span><span class="sxs-lookup"><span data-stu-id="b88f1-120">Public-derived class declarations and public methods for Web Services Description Language (WSDL) documents.</span></span>|<span data-ttu-id="b88f1-121">При создании схем должен быть включен тип (чтобы его можно было распознать во время сериализации).</span><span class="sxs-lookup"><span data-stu-id="b88f1-121">The type should be included when generating schemas (to be recognized when serialized).</span></span>|  
|<xref:System.Xml.Serialization.SoapTypeAttribute>|<span data-ttu-id="b88f1-122">Объявления открытых классов.</span><span class="sxs-lookup"><span data-stu-id="b88f1-122">Public class declarations.</span></span>|<span data-ttu-id="b88f1-123">Класс должен быть сериализован как тип XML.</span><span class="sxs-lookup"><span data-stu-id="b88f1-123">The class should be serialized as an XML type.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b88f1-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b88f1-124">See Also</span></span>  
 [<span data-ttu-id="b88f1-125">Сериализация XML и SOAP</span><span class="sxs-lookup"><span data-stu-id="b88f1-125">XML and SOAP Serialization</span></span>](../../../docs/standard/serialization/xml-and-soap-serialization.md)  
 [<span data-ttu-id="b88f1-126">Практическое руководство. Сериализация объекта как потока XML с кодировкой SOAP</span><span class="sxs-lookup"><span data-stu-id="b88f1-126">How to: Serialize an Object as a SOAP-Encoded XML Stream</span></span>](../../../docs/standard/serialization/how-to-serialize-an-object-as-a-soap-encoded-xml-stream.md)  
 [<span data-ttu-id="b88f1-127">Практическое руководство. Переопределение сериализации XML с кодировкой SOAP</span><span class="sxs-lookup"><span data-stu-id="b88f1-127">How to: Override Encoded SOAP XML Serialization</span></span>](../../../docs/standard/serialization/how-to-override-encoded-soap-xml-serialization.md)  
 [<span data-ttu-id="b88f1-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b88f1-128">Attributes</span></span>](../../../docs/standard/attributes/index.md)  
 <xref:System.Xml.Serialization.XmlSerializer>  
 [<span data-ttu-id="b88f1-129">Практическое руководство. Сериализация объекта</span><span class="sxs-lookup"><span data-stu-id="b88f1-129">How to: Serialize an Object</span></span>](../../../docs/standard/serialization/how-to-serialize-an-object.md)  
 [<span data-ttu-id="b88f1-130">Практическое руководство. Десериализация объекта</span><span class="sxs-lookup"><span data-stu-id="b88f1-130">How to: Deserialize an Object</span></span>](../../../docs/standard/serialization/how-to-deserialize-an-object.md)
