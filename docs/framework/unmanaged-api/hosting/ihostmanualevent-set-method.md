---
title: "Метод IHostManualEvent::Set"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- IHostManualEvent.Set
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent::Set
helpviewer_keywords:
- Set method, IHostManualEvent interface [.NET Framework hosting]
- IHostManualEvent::Set method [.NET Framework hosting]
ms.assetid: e930c174-f71d-4faa-bb59-f0fb3df4d77b
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 30dcb7232d6e0f7d42de48fefd2fbb9433a50405
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2017
---
# <a name="ihostmanualeventset-method"></a><span data-ttu-id="04964-102">Метод IHostManualEvent::Set</span><span class="sxs-lookup"><span data-stu-id="04964-102">IHostManualEvent::Set Method</span></span>
<span data-ttu-id="04964-103">Задает текущий [IHostManualEvent](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md) экземпляр сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="04964-103">Sets the current [IHostManualEvent](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md) instance to a signaled state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04964-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04964-104">Syntax</span></span>  
  
```  
HRESULT Set ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="04964-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04964-105">Return Value</span></span>  
  
|<span data-ttu-id="04964-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="04964-106">HRESULT</span></span>|<span data-ttu-id="04964-107">Описание</span><span class="sxs-lookup"><span data-stu-id="04964-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="04964-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="04964-108">S_OK</span></span>|<span data-ttu-id="04964-109">`Set`успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="04964-109">`Set` returned successfully.</span></span>|  
|<span data-ttu-id="04964-110">ЗНАЧЕНИЕ HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="04964-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="04964-111">Общеязыковая среда выполнения (CLR) не был загружен в процесс или находится в состоянии, в котором не может выполнять управляемый код или успешно обработать вызов.</span><span class="sxs-lookup"><span data-stu-id="04964-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="04964-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="04964-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="04964-113">Истекло время ожидания вызова.</span><span class="sxs-lookup"><span data-stu-id="04964-113">The call timed out.</span></span>|  
|<span data-ttu-id="04964-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="04964-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="04964-115">Вызывающий объект не является владельцем блокировки.</span><span class="sxs-lookup"><span data-stu-id="04964-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="04964-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="04964-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="04964-117">Событие было отменено заблокированный поток или ожидал волокон.</span><span class="sxs-lookup"><span data-stu-id="04964-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="04964-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="04964-118">E_FAIL</span></span>|<span data-ttu-id="04964-119">Неизвестная Неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="04964-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="04964-120">Если метод вернет значение E_FAIL, среда CLR больше не может использоваться в процессе.</span><span class="sxs-lookup"><span data-stu-id="04964-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="04964-121">Последующие вызовы размещение методы возвращают значение HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="04964-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="04964-122">Требования</span><span class="sxs-lookup"><span data-stu-id="04964-122">Requirements</span></span>  
 <span data-ttu-id="04964-123">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="04964-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="04964-124">**Заголовок:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="04964-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="04964-125">**Библиотека:** включена как ресурс в MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="04964-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="04964-126">**Версии платформы .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="04964-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04964-127">См. также</span><span class="sxs-lookup"><span data-stu-id="04964-127">See Also</span></span>  
 [<span data-ttu-id="04964-128">Интерфейс ICLRSyncManager</span><span class="sxs-lookup"><span data-stu-id="04964-128">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)  
 [<span data-ttu-id="04964-129">Интерфейс IHostAutoEvent</span><span class="sxs-lookup"><span data-stu-id="04964-129">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)  
 [<span data-ttu-id="04964-130">Интерфейс IHostManualEvent</span><span class="sxs-lookup"><span data-stu-id="04964-130">IHostManualEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md)  
 [<span data-ttu-id="04964-131">Интерфейс IHostSemaphore</span><span class="sxs-lookup"><span data-stu-id="04964-131">IHostSemaphore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-interface.md)  
 [<span data-ttu-id="04964-132">Интерфейс IHostSyncManager</span><span class="sxs-lookup"><span data-stu-id="04964-132">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
