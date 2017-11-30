---
title: "Метод ICorProfilerCallback::AssemblyUnloadFinished"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.AssemblyUnloadFinished
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::AssemblyUnloadFinished
helpviewer_keywords:
- AssemblyUnloadFinished method [.NET Framework profiling]
- ICorProfilerCallback::AssemblyUnloadFinished method [.NET Framework profiling]
ms.assetid: 53fca564-84b1-44d4-9e21-17a492d2aae7
topic_type: apiref
caps.latest.revision: "14"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 144f7af59afbb403d9ec1894f06c5c028b767416
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilercallbackassemblyunloadfinished-method"></a><span data-ttu-id="36e61-102">Метод ICorProfilerCallback::AssemblyUnloadFinished</span><span class="sxs-lookup"><span data-stu-id="36e61-102">ICorProfilerCallback::AssemblyUnloadFinished Method</span></span>
<span data-ttu-id="36e61-103">Уведомляет профилировщик о выгрузке сборки.</span><span class="sxs-lookup"><span data-stu-id="36e61-103">Notifies the profiler that an assembly has been unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="36e61-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36e61-104">Syntax</span></span>  
  
```  
HRESULT AssemblyUnloadFinished(  
    [in] AssemblyID assemblyId,  
    [in] HRESULT    hrStatus);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="36e61-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="36e61-105">Parameters</span></span>  
 `assemblyId`  
 <span data-ttu-id="36e61-106">[in] Идентифицирует сборку, которая выгружается.</span><span class="sxs-lookup"><span data-stu-id="36e61-106">[in] Identifies the assembly that is being unloaded.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="36e61-107">[in] Значение HRESULT, указывающее, была ли сборка выгружается успешно.</span><span class="sxs-lookup"><span data-stu-id="36e61-107">[in] An HRESULT that indicates whether the assembly was unloaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="36e61-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="36e61-108">Remarks</span></span>  
 <span data-ttu-id="36e61-109">Значение `assemblyId` является недопустимым для информационного запроса после [ICorProfilerCallback::AssemblyUnloadStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-assemblyunloadstarted-method.md) возвращает метод.</span><span class="sxs-lookup"><span data-stu-id="36e61-109">The value of `assemblyId` is not valid for an information request after the [ICorProfilerCallback::AssemblyUnloadStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-assemblyunloadstarted-method.md) method returns.</span></span>  
  
 <span data-ttu-id="36e61-110">Некоторые части выгрузку сборки может быть продолжено после `AssemblyUnloadFinished` обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="36e61-110">Some parts of unloading the assembly might continue after the `AssemblyUnloadFinished` callback.</span></span> <span data-ttu-id="36e61-111">Значение HRESULT в `hrStatus` указывает на сбой.</span><span class="sxs-lookup"><span data-stu-id="36e61-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="36e61-112">Тем не менее значение HRESULT в `hrStatus` указывает, что в первой части выгрузку сборки выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="36e61-112">However, a success HRESULT in `hrStatus` indicates only that the first part of unloading the assembly has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="36e61-113">Требования</span><span class="sxs-lookup"><span data-stu-id="36e61-113">Requirements</span></span>  
 <span data-ttu-id="36e61-114">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="36e61-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="36e61-115">**Заголовок:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="36e61-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="36e61-116">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="36e61-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="36e61-117">**Версии платформы .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="36e61-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="36e61-118">См. также</span><span class="sxs-lookup"><span data-stu-id="36e61-118">See Also</span></span>  
 [<span data-ttu-id="36e61-119">Интерфейс ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="36e61-119">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
