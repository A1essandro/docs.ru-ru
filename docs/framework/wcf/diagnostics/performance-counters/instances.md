---
title: Экземпляры
ms.date: 03/30/2017
ms.assetid: c8cf3460-0ca1-4411-8262-e9ecaf7f0a31
ms.openlocfilehash: 1b2801b5df3a5d2ca6d7fd03299ecdf4b7df426a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520281"
---
# <a name="instances"></a><span data-ttu-id="c2075-102">Экземпляры</span><span class="sxs-lookup"><span data-stu-id="c2075-102">Instances</span></span>
<span data-ttu-id="c2075-103">Имя счетчика: экземпляры.</span><span class="sxs-lookup"><span data-stu-id="c2075-103">Counter Name: Instances.</span></span>  
  
## <a name="description"></a><span data-ttu-id="c2075-104">Описание</span><span class="sxs-lookup"><span data-stu-id="c2075-104">Description</span></span>  
 <span data-ttu-id="c2075-105">Число контекстов экземпляра, которое в настоящий момент содержит служба.</span><span class="sxs-lookup"><span data-stu-id="c2075-105">Number of instance contexts that the service currently contains.</span></span>  
  
 <span data-ttu-id="c2075-106">В большинстве случаев число контекстов экземпляра идентично числу экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c2075-106">Most of the time, the number of instance contexts is identical to the number of instances.</span></span> <span data-ttu-id="c2075-107">Однако приведенные ниже сценарии являются исключением из этого правила.</span><span class="sxs-lookup"><span data-stu-id="c2075-107">However, the following scenarios are exception to this rule.</span></span>  
  
-   <span data-ttu-id="c2075-108">Метод службы явным образом вызывает метод <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A>.</span><span class="sxs-lookup"><span data-stu-id="c2075-108">A service method calls the <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> method explicitly.</span></span>  
  
-   <span data-ttu-id="c2075-109"><xref:System.ServiceModel.ReleaseInstanceMode> применяется к экземпляру <xref:System.ServiceModel.OperationBehaviorAttribute>.</span><span class="sxs-lookup"><span data-stu-id="c2075-109">A <xref:System.ServiceModel.ReleaseInstanceMode> is applied to an <xref:System.ServiceModel.OperationBehaviorAttribute> instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2075-110">См. также</span><span class="sxs-lookup"><span data-stu-id="c2075-110">See also</span></span>
- <xref:System.ServiceModel.OperationBehaviorAttribute>
