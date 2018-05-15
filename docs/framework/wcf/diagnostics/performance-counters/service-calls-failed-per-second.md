---
title: 'Служба: количество сбоев вызовов в секунду'
ms.date: 03/30/2017
ms.assetid: 5a2c7939-107d-4f0c-b43c-e02e079e8a9d
ms.openlocfilehash: 6af8f79d1fe163967a5c6e8220697aa11bee66c7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
---
# <a name="service-calls-failed-per-second"></a><span data-ttu-id="4825a-102">Служба: количество сбоев вызовов в секунду</span><span class="sxs-lookup"><span data-stu-id="4825a-102">Service: Calls Failed Per Second</span></span>
<span data-ttu-id="4825a-103">Имя счетчика: Calls Failed Per Second.</span><span class="sxs-lookup"><span data-stu-id="4825a-103">Counter Name: Calls Failed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="4825a-104">Описание</span><span class="sxs-lookup"><span data-stu-id="4825a-104">Description</span></span>  
 <span data-ttu-id="4825a-105">Число вызовов с необработанными исключениями, получаемых этой службой за секунду.</span><span class="sxs-lookup"><span data-stu-id="4825a-105">Number of calls that have unhandled exceptions, and are received by this service in a second.</span></span>  
  
 <span data-ttu-id="4825a-106">Этот счетчик является счетчиком производительности типа [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), значение которого вычисляется по следующей формуле.</span><span class="sxs-lookup"><span data-stu-id="4825a-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="4825a-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="4825a-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="4825a-108">В управляемом коде исключения создаются в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="4825a-108">In managed code, exceptions are thrown when error conditions occur.</span></span>  
  
 <span data-ttu-id="4825a-109">В управляемом коде исключения создаются в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="4825a-109">In managed code, exceptions are thrown when error conditions occur.</span></span>  
  
 <span data-ttu-id="4825a-110">Значение этого счетчика увеличивается при каждом обнаружении необработанного исключения в данной службе.</span><span class="sxs-lookup"><span data-stu-id="4825a-110">This counter is incremented every time there is an unhandled exception in this service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4825a-111">См. также</span><span class="sxs-lookup"><span data-stu-id="4825a-111">See Also</span></span>  
 [<span data-ttu-id="4825a-112">Указание и обработка сбоев в контрактах и службах</span><span class="sxs-lookup"><span data-stu-id="4825a-112">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
