---
title: Интерфейсы размещения
ms.date: 03/30/2017
helpviewer_keywords:
- interfaces [.NET Framework hosting]
- hosting interfaces [.NET Framework]
- unmanaged interfaces [.NET Framework], hosting
ms.assetid: cc64cb05-38da-418e-815a-daac8e8e26e5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c2bef9e1671b8487a6702cce71106c84a2984317
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436164"
---
# <a name="hosting-interfaces"></a><span data-ttu-id="41dc1-102">Интерфейсы размещения</span><span class="sxs-lookup"><span data-stu-id="41dc1-102">Hosting Interfaces</span></span>
<span data-ttu-id="41dc1-103">В этом разделе описываются интерфейсы, которые неуправляемые узлов можно использовать для интеграции общеязыковой среды выполнения (CLR) в свои приложения.</span><span class="sxs-lookup"><span data-stu-id="41dc1-103">This section describes the interfaces that unmanaged hosts can use to integrate the common language runtime (CLR) into their applications.</span></span>  
  
 <span data-ttu-id="41dc1-104">Интерфейсы размещения платформы .NET Framework версии 2.0 заменяют интерфейсы платформы .NET Framework версий 1.0 и 1.1.</span><span class="sxs-lookup"><span data-stu-id="41dc1-104">The .NET Framework version 2.0 hosting interfaces supersede the .NET Framework version 1.0 and 1.1 interfaces.</span></span> <span data-ttu-id="41dc1-105">Существуют значительные различия между двумя наборами интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="41dc1-105">There are significant differences between the two sets of interfaces.</span></span> <span data-ttu-id="41dc1-106">Смешивание их могут вызвать непредвиденное поведение и не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="41dc1-106">Mixing them could cause unexpected behavior and is not recommended.</span></span>  
  
 <span data-ttu-id="41dc1-107">Версии платформы .NET Framework 3.0 и 3.5 использовать интерфейсы размещения платформы .NET Framework версии 2.0 и не предоставляет дополнительные функции размещения.</span><span class="sxs-lookup"><span data-stu-id="41dc1-107">The .NET Framework versions 3.0 and 3.5 use the .NET Framework version 2.0 hosting interfaces, and do not introduce any hosting features.</span></span>  
  
 <span data-ttu-id="41dc1-108">[!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)] Интерфейсы размещения заменяют интерфейсы платформы .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="41dc1-108">The [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)] hosting interfaces supersede the .NET Framework 2.0 interfaces.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="41dc1-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="41dc1-109">In This Section</span></span>  
 [<span data-ttu-id="41dc1-110">Устаревшие интерфейсы размещения CLR и коклассы</span><span class="sxs-lookup"><span data-stu-id="41dc1-110">Deprecated CLR Hosting Interfaces and Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-interfaces-and-coclasses.md)  
 <span data-ttu-id="41dc1-111">Описание интерфейсов размещения, доступных в .NET Framework версий 1.0 и 1.1.</span><span class="sxs-lookup"><span data-stu-id="41dc1-111">Describes the hosting interfaces introduced in the .NET Framework versions 1.0 and 1.1.</span></span>  
  
 [<span data-ttu-id="41dc1-112">Интерфейсы размещения CLR</span><span class="sxs-lookup"><span data-stu-id="41dc1-112">CLR Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces.md)  
 <span data-ttu-id="41dc1-113">Описание размещения интерфейсов, доступных в .NET Framework версии 2.0.</span><span class="sxs-lookup"><span data-stu-id="41dc1-113">Describes the hosting interfaces introduced in the .NET Framework version 2.0.</span></span>  
  
 [<span data-ttu-id="41dc1-114">Интерфейсы размещения CLR, добавленные в версиях .NET Framework 4 и 4.5</span><span class="sxs-lookup"><span data-stu-id="41dc1-114">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)  
 <span data-ttu-id="41dc1-115">Описание размещения интерфейсов, доступных в [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="41dc1-115">Describes the hosting interfaces introduced in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="41dc1-116">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="41dc1-116">Related Sections</span></span>  
 [<span data-ttu-id="41dc1-117">Размещение коклассов</span><span class="sxs-lookup"><span data-stu-id="41dc1-117">Hosting Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)  
  
 [<span data-ttu-id="41dc1-118">Устаревшие функции размещения CLR</span><span class="sxs-lookup"><span data-stu-id="41dc1-118">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)  
  
 [<span data-ttu-id="41dc1-119">Размещение перечислений</span><span class="sxs-lookup"><span data-stu-id="41dc1-119">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)  
  
 [<span data-ttu-id="41dc1-120">Структуры размещения</span><span class="sxs-lookup"><span data-stu-id="41dc1-120">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)  
  
 [<span data-ttu-id="41dc1-121">Размещение</span><span class="sxs-lookup"><span data-stu-id="41dc1-121">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)  
  
 [<span data-ttu-id="41dc1-122">Узлы среды выполнения</span><span class="sxs-lookup"><span data-stu-id="41dc1-122">Runtime Hosts</span></span>](http://msdn.microsoft.com/library/99d9246a-b994-4fe5-985c-8588d1d59998)
