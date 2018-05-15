---
title: Использование пользовательской привязки для клиентского канала обнаружения
ms.date: 03/30/2017
ms.assetid: 36f95e75-04f7-44f3-a995-a0d623624d7f
ms.openlocfilehash: 4ef85b4c52c1f27b333413e2b6178452142d313f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
---
# <a name="using-a-custom-binding-with-the-discovery-client-channel"></a><span data-ttu-id="c91c0-102">Использование пользовательской привязки для клиентского канала обнаружения</span><span class="sxs-lookup"><span data-stu-id="c91c0-102">Using a Custom Binding with the Discovery Client Channel</span></span>
<span data-ttu-id="c91c0-103">При использовании пользовательской привязки к <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement> необходимо определить поставщик <xref:System.ServiceModel.Discovery.DiscoveryEndpointProvider>, который будет создавать экземпляры <xref:System.ServiceModel.Discovery.DiscoveryEndpoint>.</span><span class="sxs-lookup"><span data-stu-id="c91c0-103">When using a custom binding with the <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement>, you must define a <xref:System.ServiceModel.Discovery.DiscoveryEndpointProvider> that creates <xref:System.ServiceModel.Discovery.DiscoveryEndpoint> instances.</span></span>  
  
## <a name="creating-a-discoveryendpointprovider"></a><span data-ttu-id="c91c0-104">Создание DiscoveryEndpointProvider</span><span class="sxs-lookup"><span data-stu-id="c91c0-104">Creating a DiscoveryEndpointProvider</span></span>  
 <span data-ttu-id="c91c0-105"><xref:System.ServiceModel.Discovery.DiscoveryEndpointProvider> Отвечает за создание <xref:System.ServiceModel.Discovery.DiscoveryEndpoint> экземпляры по требованию.</span><span class="sxs-lookup"><span data-stu-id="c91c0-105">The <xref:System.ServiceModel.Discovery.DiscoveryEndpointProvider> is responsible for creating <xref:System.ServiceModel.Discovery.DiscoveryEndpoint> instances on demand.</span></span> <span data-ttu-id="c91c0-106">Чтобы определить поставщика конечной точки обнаружения, создайте класс из <xref:System.ServiceModel.Discovery.DiscoveryEndpointProvider>, переопределив метод <xref:System.ServiceModel.Discovery.DiscoveryEndpointProvider.GetDiscoveryEndpoint%2A>, а затем вернув новую конечную точку обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c91c0-106">To define a discovery endpoint provider, derive a class from <xref:System.ServiceModel.Discovery.DiscoveryEndpointProvider> and override the <xref:System.ServiceModel.Discovery.DiscoveryEndpointProvider.GetDiscoveryEndpoint%2A> method and return a new discovery endpoint.</span></span> <span data-ttu-id="c91c0-107">В следующем примере показан процесс создания поставщика конечной точки обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c91c0-107">The following example shows how to create a discovery endpoint provider.</span></span>  
  
```  
// Extend DiscoveryEndpointProvider class to change the default DiscoveryEndpoint  
// to the DiscoveryClientBindingElement. The Discovery ClientChannel   
// uses this endpoint to send Probe message.  
public class UdpDiscoveryEndpointProvider : DiscoveryEndpointProvider  
{  
   public override DiscoveryEndpoint GetDiscoveryEndpoint()  
   {  
      return new UdpDiscoveryEndpoint(DiscoveryVersion.WSDiscoveryApril2005);  
   }  
}  
```  
  
 <span data-ttu-id="c91c0-108">После того как поставщик конечной точки обнаружения определен, можно создать пользовательскую привязку и добавить <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement>, который содержит ссылки на поставщик конечной точки обнаружения, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="c91c0-108">Once you have defined the discovery endpoint provider you can create a custom binding and add the <xref:System.ServiceModel.Discovery.DiscoveryClientBindingElement>, which references the discovery endpoint provider as shown in the following example.</span></span>  
  
```  
DiscoveryClientBindingElement discoveryBindingElement = new DiscoveryClientBindingElement();  
  
// Provide the search criteria and the endpoint over which the probe is sent.  
discoveryBindingElement.FindCriteria = new FindCriteria(typeof(ICalculatorService));  
discoveryBindingElement.DiscoveryEndpointProvider = new UdpDiscoveryEndpointProvider();  
  
CustomBinding customBinding = new CustomBinding(new NetTcpBinding());  
// Insert DiscoveryClientBindingElement at the top of the BindingElement stack.  
// An exception is thrown if this binding element is not at the top.  
customBinding.Elements.Insert(0, discoveryBindingElement);  
```  
  
 <span data-ttu-id="c91c0-109">Дополнительные сведения об использовании клиентского канала обнаружения см. в разделе [использование клиентского канала обнаружения](../../../../docs/framework/wcf/feature-details/using-the-discovery-client-channel.md).</span><span class="sxs-lookup"><span data-stu-id="c91c0-109">For more information about using the discovery client channel, see [Using the Discovery Client Channel](../../../../docs/framework/wcf/feature-details/using-the-discovery-client-channel.md).</span></span> <span data-ttu-id="c91c0-110">Полный пример кода см. в разделе [образец элемента привязки обнаружения](../../../../docs/framework/wcf/samples/discovery-binding-element-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c91c0-110">For a complete code example, see [Discovery Binding Element Sample](../../../../docs/framework/wcf/samples/discovery-binding-element-sample.md)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c91c0-111">См. также</span><span class="sxs-lookup"><span data-stu-id="c91c0-111">See Also</span></span>  
 [<span data-ttu-id="c91c0-112">Общие сведения об обнаружении WCF</span><span class="sxs-lookup"><span data-stu-id="c91c0-112">WCF Discovery Overview</span></span>](../../../../docs/framework/wcf/feature-details/wcf-discovery-overview.md)  
 [<span data-ttu-id="c91c0-113">Использование клиентского канала обнаружения</span><span class="sxs-lookup"><span data-stu-id="c91c0-113">Using the Discovery Client Channel</span></span>](../../../../docs/framework/wcf/feature-details/using-the-discovery-client-channel.md)  
 [<span data-ttu-id="c91c0-114">Образец элемента привязки для обнаружения</span><span class="sxs-lookup"><span data-stu-id="c91c0-114">Discovery Binding Element Sample</span></span>](../../../../docs/framework/wcf/samples/discovery-binding-element-sample.md)
