---
title: "Метод IHostSyncManager::CreateAutoEvent"
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
- IHostSyncManager.CreateAutoEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateAutoEvent
helpviewer_keywords:
- IHostSyncManager::CreateAutoEvent method [.NET Framework hosting]
- CreateAutoEvent method [.NET Framework hosting]
ms.assetid: 3153643e-cf5c-4b44-8e0e-c2b22cb08208
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: b7874839d04af89f2fa512f82213862f34408001
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2017
---
# <a name="ihostsyncmanagercreateautoevent-method"></a><span data-ttu-id="bbbd0-102">Метод IHostSyncManager::CreateAutoEvent</span><span class="sxs-lookup"><span data-stu-id="bbbd0-102">IHostSyncManager::CreateAutoEvent Method</span></span>
<span data-ttu-id="bbbd0-103">Создает объект события автоматического сброса.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-103">Creates an auto-reset event object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bbbd0-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbbd0-104">Syntax</span></span>  
  
```  
HRESULT CreateAutoEvent (  
    [out] IHostAutoEvent **ppEvent  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bbbd0-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbbd0-105">Parameters</span></span>  
 `ppEvent`  
 <span data-ttu-id="bbbd0-106">[out] Указатель на адрес [IHostAutoEvent](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md) экземпляр реализовано узлом, или значение null, если не удается создать объект события.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-106">[out] A pointer to the address of an [IHostAutoEvent](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md) instance implemented by the host, or null if the event object could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bbbd0-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbbd0-107">Return Value</span></span>  
  
|<span data-ttu-id="bbbd0-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bbbd0-108">HRESULT</span></span>|<span data-ttu-id="bbbd0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bbbd0-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bbbd0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbbd0-110">S_OK</span></span>|<span data-ttu-id="bbbd0-111">`CreateAutoEvent`успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-111">`CreateAutoEvent` returned successfully.</span></span>|  
|<span data-ttu-id="bbbd0-112">ЗНАЧЕНИЕ HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bbbd0-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bbbd0-113">Общеязыковая среда выполнения (CLR) не был загружен в процесс или находится в состоянии, в котором не может выполнять управляемый код или успешно обработать вызов.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bbbd0-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bbbd0-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bbbd0-115">Истекло время ожидания вызова.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-115">The call timed out.</span></span>|  
|<span data-ttu-id="bbbd0-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bbbd0-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bbbd0-117">Вызывающий объект не является владельцем блокировки.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bbbd0-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bbbd0-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bbbd0-119">Событие было отменено заблокированный поток или ожидал волокон.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bbbd0-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bbbd0-120">E_FAIL</span></span>|<span data-ttu-id="bbbd0-121">Неизвестная Неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bbbd0-122">Если метод вернет значение E_FAIL, среда CLR больше не может использоваться в процессе.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bbbd0-123">Последующие вызовы размещение методы возвращают значение HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="bbbd0-124">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="bbbd0-124">E_OUTOFMEMORY</span></span>|<span data-ttu-id="bbbd0-125">Не хватает памяти была доступна для создания запрошенного объекта события.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-125">Not enough memory was available to create the requested event object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bbbd0-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="bbbd0-126">Remarks</span></span>  
 <span data-ttu-id="bbbd0-127">`CreateAutoEvent`Создает объект автоматического события, состояние которого будет автоматически изменено на несигнальное после выпуска ожидающий поток.</span><span class="sxs-lookup"><span data-stu-id="bbbd0-127">`CreateAutoEvent` creates an auto-event object whose state is automatically changed to non-signaled after the waiting thread has been released.</span></span> <span data-ttu-id="bbbd0-128">Этот метод получает зеркально Win32 `CreateEvent` функции со значением `false` указано `bManualReset` параметр</span><span class="sxs-lookup"><span data-stu-id="bbbd0-128">This method mirrors the Win32 `CreateEvent` function with a value of `false` specified for the `bManualReset` parameter</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bbbd0-129">Требования</span><span class="sxs-lookup"><span data-stu-id="bbbd0-129">Requirements</span></span>  
 <span data-ttu-id="bbbd0-130">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bbbd0-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bbbd0-131">**Заголовок:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bbbd0-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bbbd0-132">**Библиотека:** включена как ресурс в MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bbbd0-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bbbd0-133">**Версии платформы .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bbbd0-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bbbd0-134">См. также</span><span class="sxs-lookup"><span data-stu-id="bbbd0-134">See Also</span></span>  
 [<span data-ttu-id="bbbd0-135">Интерфейс ICLRSyncManager</span><span class="sxs-lookup"><span data-stu-id="bbbd0-135">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)  
 [<span data-ttu-id="bbbd0-136">Интерфейс IHostAutoEvent</span><span class="sxs-lookup"><span data-stu-id="bbbd0-136">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)  
 [<span data-ttu-id="bbbd0-137">Интерфейс IHostControl</span><span class="sxs-lookup"><span data-stu-id="bbbd0-137">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)  
 [<span data-ttu-id="bbbd0-138">Интерфейс IHostSyncManager</span><span class="sxs-lookup"><span data-stu-id="bbbd0-138">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
