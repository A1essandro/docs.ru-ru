---
title: "Практическое руководство. Использование MetadataResolver для динамического получения метаданных привязки"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 56ffcb99-fff0-4479-aca0-e3909009f605
caps.latest.revision: "12"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: ab95212d0f7b57b2bc076bed862b3d07c3c93df9
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-use-metadataresolver-to-obtain-binding-metadata-dynamically"></a><span data-ttu-id="90a84-102">Практическое руководство. Использование MetadataResolver для динамического получения метаданных привязки</span><span class="sxs-lookup"><span data-stu-id="90a84-102">How to: Use MetadataResolver to Obtain Binding Metadata Dynamically</span></span>
<span data-ttu-id="90a84-103">В этом разделе показано, как использовать класс <xref:System.ServiceModel.Description.MetadataResolver> для динамического получения метаданных привязки.</span><span class="sxs-lookup"><span data-stu-id="90a84-103">This topic shows you how to use the <xref:System.ServiceModel.Description.MetadataResolver> class to dynamically obtain binding metadata.</span></span>  
  
### <a name="to-dynamically-obtain-binding-metadata"></a><span data-ttu-id="90a84-104">Динамическое получение метаданных привязки</span><span class="sxs-lookup"><span data-stu-id="90a84-104">To dynamically obtain binding metadata</span></span>  
  
1.  <span data-ttu-id="90a84-105">Создайте объект <xref:System.ServiceModel.EndpointAddress> с адресом конечной точки метаданных.</span><span class="sxs-lookup"><span data-stu-id="90a84-105">Create an <xref:System.ServiceModel.EndpointAddress> object with the address of the metadata endpoint.</span></span>  
  
    ```  
    EndpointAddress metaAddress  
      = new EndpointAddress(new   Uri("http://localhost:8080/SampleService/mex"));  
    ```  
  
2.  <span data-ttu-id="90a84-106">Вызовите метод <xref:System.ServiceModel.Description.MetadataResolver.Resolve%28System.Type%2CSystem.ServiceModel.EndpointAddress%29>, передающий тип службы и адрес конечной точки метаданных.</span><span class="sxs-lookup"><span data-stu-id="90a84-106">Call <xref:System.ServiceModel.Description.MetadataResolver.Resolve%28System.Type%2CSystem.ServiceModel.EndpointAddress%29>, which passes in the service type and the metadata endpoint address.</span></span> <span data-ttu-id="90a84-107">Возвращается коллекция конечных точек, реализующих указанный контракт.</span><span class="sxs-lookup"><span data-stu-id="90a84-107">This returns a collection of endpoints that implement the specified contract.</span></span> <span data-ttu-id="90a84-108">Из метаданных импортируются только сведения о привязке; сведения о контракте не импортируются.</span><span class="sxs-lookup"><span data-stu-id="90a84-108">Only binding information is imported from the metadata; contract information is not imported.</span></span> <span data-ttu-id="90a84-109">Вместо этого используется предоставленный контракт.</span><span class="sxs-lookup"><span data-stu-id="90a84-109">The supplied contract is used instead.</span></span>  
  
    ```  
    ServiceEndpointCollection endpoints = MetadataResolver.Resolve(typeof(SampleServiceClient),metaAddress);  
    ```  
  
3.  <span data-ttu-id="90a84-110">Затем можно последовательно просмотреть коллекцию конечных точек службы, чтобы извлечь требуемые сведения о привязке.</span><span class="sxs-lookup"><span data-stu-id="90a84-110">You can then iterate through the collection of service endpoints to extract the binding information you need.</span></span> <span data-ttu-id="90a84-111">Приведенный ниже код просматривает конечные точки, создает объект клиента службы, который передает привязку и адрес, связанный с текущей конечной точкой, а затем вызывает метод службы.</span><span class="sxs-lookup"><span data-stu-id="90a84-111">The following code iterates through the endpoints, creates a service client object that passes in the binding and address associated with the current endpoint, and then calls a method on the service.</span></span>  
  
    ```  
    foreach (ServiceEndpoint point in endpoints)  
    {  
       if (point != null)  
       {  
          // Create a new wcfClient using retrieved endpoints.  
          using (wcfClient = new SampleServiceClient(point.Binding, point.Address))  
          {  
             Console.WriteLine(  
               wcfClient.SampleMethod("Client used the "  
               + point.Address.ToString() + " address."));  
          }  
      }  
    }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="90a84-112">См. также</span><span class="sxs-lookup"><span data-stu-id="90a84-112">See Also</span></span>  
 [<span data-ttu-id="90a84-113">Метаданные</span><span class="sxs-lookup"><span data-stu-id="90a84-113">Metadata</span></span>](../../../../docs/framework/wcf/feature-details/metadata.md)
