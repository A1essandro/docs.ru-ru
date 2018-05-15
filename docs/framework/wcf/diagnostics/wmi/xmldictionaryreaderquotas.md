---
title: XmlDictionaryReaderQuotas
ms.date: 03/30/2017
ms.assetid: 9b4ca8b4-0a89-4758-97ab-528a8ce18f07
ms.openlocfilehash: 78914d52a9e57fe2e48adcfc0d7b6f911a0d8b3a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
---
# <a name="xmldictionaryreaderquotas"></a><span data-ttu-id="0c24c-102">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="0c24c-102">XmlDictionaryReaderQuotas</span></span>
<span data-ttu-id="0c24c-103">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="0c24c-103">XmlDictionaryReaderQuotas</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c24c-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c24c-104">Syntax</span></span>  
  
```  
class XmlDictionaryReaderQuotas  
{  
  sint32 MaxArrayLength;  
  sint32 MaxBytesPerRead;  
  sint32 MaxDepth;  
  sint32 MaxNameTableCharCount;  
  sint32 MaxStringContentLength;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="0c24c-105">Методы</span><span class="sxs-lookup"><span data-stu-id="0c24c-105">Methods</span></span>  
 <span data-ttu-id="0c24c-106">Класс XmlDictionaryReaderQuotas не определяет никаких методов.</span><span class="sxs-lookup"><span data-stu-id="0c24c-106">The XmlDictionaryReaderQuotas class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="0c24c-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c24c-107">Properties</span></span>  
 <span data-ttu-id="0c24c-108">Класс XmlDictionaryReaderQuotas имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="0c24c-108">The XmlDictionaryReaderQuotas class has the following properties:</span></span>  
  
### <a name="maxarraylength"></a><span data-ttu-id="0c24c-109">MaxArrayLength</span><span class="sxs-lookup"><span data-stu-id="0c24c-109">MaxArrayLength</span></span>  
 <span data-ttu-id="0c24c-110">Тип данных: sint32</span><span class="sxs-lookup"><span data-stu-id="0c24c-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="0c24c-111">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c24c-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0c24c-112">Максимально допустимая длина массива.</span><span class="sxs-lookup"><span data-stu-id="0c24c-112">The maximum allowed array length.</span></span>  
  
### <a name="maxbytesperread"></a><span data-ttu-id="0c24c-113">MaxBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="0c24c-113">MaxBytesPerRead</span></span>  
 <span data-ttu-id="0c24c-114">Тип данных: sint32</span><span class="sxs-lookup"><span data-stu-id="0c24c-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="0c24c-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c24c-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0c24c-116">Максимально допустимое число байтов, возвращаемых для каждой операции чтения.</span><span class="sxs-lookup"><span data-stu-id="0c24c-116">The maximum allowed bytes returned for each read.</span></span>  
  
### <a name="maxdepth"></a><span data-ttu-id="0c24c-117">MaxDepth</span><span class="sxs-lookup"><span data-stu-id="0c24c-117">MaxDepth</span></span>  
 <span data-ttu-id="0c24c-118">Тип данных: sint32</span><span class="sxs-lookup"><span data-stu-id="0c24c-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="0c24c-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c24c-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0c24c-120">Максимальная глубина вложенного узла для каждого чтения.</span><span class="sxs-lookup"><span data-stu-id="0c24c-120">The maximum nested node depth for each read.</span></span>  
  
### <a name="maxnametablecharcount"></a><span data-ttu-id="0c24c-121">MaxNameTableCharCount</span><span class="sxs-lookup"><span data-stu-id="0c24c-121">MaxNameTableCharCount</span></span>  
 <span data-ttu-id="0c24c-122">Тип данных: sint32</span><span class="sxs-lookup"><span data-stu-id="0c24c-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="0c24c-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c24c-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0c24c-124">Максимально допустимое количество символов в имени таблицы.</span><span class="sxs-lookup"><span data-stu-id="0c24c-124">The maximum characters allowed in a table name.</span></span>  
  
### <a name="maxstringcontentlength"></a><span data-ttu-id="0c24c-125">MaxStringContentLength</span><span class="sxs-lookup"><span data-stu-id="0c24c-125">MaxStringContentLength</span></span>  
 <span data-ttu-id="0c24c-126">Тип данных: sint32</span><span class="sxs-lookup"><span data-stu-id="0c24c-126">Data type: sint32</span></span>  
  
 <span data-ttu-id="0c24c-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c24c-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0c24c-128">Максимальное допустимое число символов в содержимом элемента XML.</span><span class="sxs-lookup"><span data-stu-id="0c24c-128">The maximum characters allowed in XML element content.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c24c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="0c24c-129">Requirements</span></span>  
  
|<span data-ttu-id="0c24c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="0c24c-130">MOF</span></span>|<span data-ttu-id="0c24c-131">Объявлено в файле Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="0c24c-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="0c24c-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0c24c-132">Namespace</span></span>|<span data-ttu-id="0c24c-133">Определено в root\ServiceModel.</span><span class="sxs-lookup"><span data-stu-id="0c24c-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0c24c-134">См. также</span><span class="sxs-lookup"><span data-stu-id="0c24c-134">See Also</span></span>  
 <xref:System.Xml.XmlDictionaryReaderQuotas>  
 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>
