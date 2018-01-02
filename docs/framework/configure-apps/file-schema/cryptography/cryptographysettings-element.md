---
title: "&lt;cryptographySettings&gt; элемент"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptographySettings
helpviewer_keywords:
- cryptographySettings element
- <cryptographySettings> element
ms.assetid: 6201b7da-bcb7-49f7-b9f5-ba1fe05573b9
caps.latest.revision: "11"
author: mcleblanc
ms.author: markl
manager: markl
ms.workload: dotnet
ms.openlocfilehash: 73a4f362be1612658e6911b7e7ea7a6c3e670e01
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2017
---
# <a name="ltcryptographysettingsgt-element"></a><span data-ttu-id="bc495-102">&lt;cryptographySettings&gt; элемент</span><span class="sxs-lookup"><span data-stu-id="bc495-102">&lt;cryptographySettings&gt; Element</span></span>
<span data-ttu-id="bc495-103">Содержит параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="bc495-103">Contains cryptography settings.</span></span>  
  
 <span data-ttu-id="bc495-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="bc495-104">\<configuration></span></span>  
<span data-ttu-id="bc495-105">\<mscorlib ></span><span class="sxs-lookup"><span data-stu-id="bc495-105">\<mscorlib></span></span>  
<span data-ttu-id="bc495-106">\<cryptographySettings ></span><span class="sxs-lookup"><span data-stu-id="bc495-106">\<cryptographySettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc495-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc495-107">Syntax</span></span>  
  
```xml  
      <cryptographySettings>   
</cryptographySettings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bc495-108">Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="bc495-108">Attributes and Elements</span></span>  
 <span data-ttu-id="bc495-109">В следующих разделах описаны атрибуты, дочерние и родительские элементы.</span><span class="sxs-lookup"><span data-stu-id="bc495-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bc495-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bc495-110">Attributes</span></span>  
 <span data-ttu-id="bc495-111">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="bc495-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="bc495-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bc495-112">Child Elements</span></span>  
  
|<span data-ttu-id="bc495-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="bc495-113">Element</span></span>|<span data-ttu-id="bc495-114">Описание:</span><span class="sxs-lookup"><span data-stu-id="bc495-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bc495-115">\<cryptoNameMapping ></span><span class="sxs-lookup"><span data-stu-id="bc495-115">\<cryptoNameMapping></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptonamemapping-element.md)|<span data-ttu-id="bc495-116">Содержит сопоставления классов с понятными именами.</span><span class="sxs-lookup"><span data-stu-id="bc495-116">Contains mappings of classes to friendly names.</span></span>|  
|[<span data-ttu-id="bc495-117">\<oidMap ></span><span class="sxs-lookup"><span data-stu-id="bc495-117">\<oidMap></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidmap-element.md)|<span data-ttu-id="bc495-118">Содержит сопоставления идентификатора объекта ASN.1 с классами.</span><span class="sxs-lookup"><span data-stu-id="bc495-118">Contains ASN.1 object identifier (OID) mappings to classes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bc495-119">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bc495-119">Parent Elements</span></span>  
  
|<span data-ttu-id="bc495-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="bc495-120">Element</span></span>|<span data-ttu-id="bc495-121">Описание</span><span class="sxs-lookup"><span data-stu-id="bc495-121">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="bc495-122">Корневой элемент в любом файле конфигурации, используемом средой CLR и приложениями .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="bc495-122">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`mscorlib`|<span data-ttu-id="bc495-123">Содержит `cryptographySettings` элемента.</span><span class="sxs-lookup"><span data-stu-id="bc495-123">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="bc495-124">Пример</span><span class="sxs-lookup"><span data-stu-id="bc495-124">Example</span></span>  
 <span data-ttu-id="bc495-125">Приведенный ниже показано, как использовать  **\<cryptographySettings >** элемента сопоставлений криптографических имен и сопоставлений идентификаторов Объектов.</span><span class="sxs-lookup"><span data-stu-id="bc495-125">The following example shows how use the **\<cryptographySettings>** element to contain cryptography name mappings and OID mappings.</span></span> <span data-ttu-id="bc495-126">В этом примере настраивает среду выполнения, чтобы <xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType> возвращает `MyHashClass` объекта и `MyCryptoClass` класса сопоставляется 1.3.36.2.1 идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="bc495-126">This example configures the runtime so that <xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType> returns a `MyHashClass` object and the `MyCryptoClass` class maps to the object identifier 1.3.36.2.1.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyHash="MyHashClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="System.Security.Cryptography.HashAlgorithm"  
                       class="MyHash"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"   name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="bc495-127">См. также</span><span class="sxs-lookup"><span data-stu-id="bc495-127">See Also</span></span>  
 [<span data-ttu-id="bc495-128">Схема файла конфигурации</span><span class="sxs-lookup"><span data-stu-id="bc495-128">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="bc495-129">Схема параметров шифрования</span><span class="sxs-lookup"><span data-stu-id="bc495-129">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
 [<span data-ttu-id="bc495-130">Службы криптографии</span><span class="sxs-lookup"><span data-stu-id="bc495-130">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)
