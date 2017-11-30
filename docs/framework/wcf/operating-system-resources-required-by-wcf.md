---
title: "Ресурсы операционной системы, необходимые WCF"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: cdd9a331-53fe-4e0d-bdfe-782264aec5c9
caps.latest.revision: "6"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 6cfe114e5e044a6aaa1e356194a46b4a46011aa0
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="operating-system-resources-required-by-wcf"></a><span data-ttu-id="73de7-102">Ресурсы операционной системы, необходимые WCF</span><span class="sxs-lookup"><span data-stu-id="73de7-102">Operating System Resources Required by WCF</span></span>
[!INCLUDE[indigo1](../../../includes/indigo1-md.md)]<span data-ttu-id="73de7-103"> зависит о нескольких ресурсов, работа которых обеспечивается операционной системой.</span><span class="sxs-lookup"><span data-stu-id="73de7-103"> depends on several resources that are provided by the operating system to function.</span></span> <span data-ttu-id="73de7-104">В следующей таблице перечислены эти ресурсы.</span><span class="sxs-lookup"><span data-stu-id="73de7-104">The following table lists those resources.</span></span>  
  
|<span data-ttu-id="73de7-105">Ресурс</span><span class="sxs-lookup"><span data-stu-id="73de7-105">Resource</span></span>|<span data-ttu-id="73de7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="73de7-106">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="73de7-107">Координатор распределенных транзакций (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="73de7-107">Microsoft Distributed Transaction Coordinator (MSDTC)</span></span>|<span data-ttu-id="73de7-108">Требуется для поддержки транзакций OleTx.</span><span class="sxs-lookup"><span data-stu-id="73de7-108">Required to support OleTx transactions.</span></span>|  
|<span data-ttu-id="73de7-109">службы IIS</span><span class="sxs-lookup"><span data-stu-id="73de7-109">Internet Information Services (IIS)</span></span>|<span data-ttu-id="73de7-110">Требуется, если необходимо использовать службы IIS для размещения приложения.</span><span class="sxs-lookup"><span data-stu-id="73de7-110">Required if you want to use IIS to host your application.</span></span>|  
|<span data-ttu-id="73de7-111">Служба активации Windows (WAS)</span><span class="sxs-lookup"><span data-stu-id="73de7-111">Windows Process Activation Service (WAS)</span></span>|<span data-ttu-id="73de7-112">Требуется, если необходимо использовать WAS для размещения приложения.</span><span class="sxs-lookup"><span data-stu-id="73de7-112">Required if you want to use WAS to host your application.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="73de7-113">См. также</span><span class="sxs-lookup"><span data-stu-id="73de7-113">See Also</span></span>  
 [<span data-ttu-id="73de7-114">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="73de7-114">System Requirements</span></span>](../../../docs/framework/wcf/wcf-system-requirements.md)
