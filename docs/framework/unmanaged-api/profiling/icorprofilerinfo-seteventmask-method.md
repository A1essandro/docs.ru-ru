---
title: "Метод ICorProfilerInfo::SetEventMask"
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
- ICorProfilerInfo.SetEventMask
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::SetEventMask
helpviewer_keywords:
- ICorProfilerInfo::SetEventMask method [.NET Framework profiling]
- SetEventMask method [.NET Framework profiling]
ms.assetid: 44bc0f56-32fa-491e-a62d-52fc96d48125
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 4c6fe763103e7b8aaf6d501c653342a21bd513b8
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2017
---
# <a name="icorprofilerinfoseteventmask-method"></a><span data-ttu-id="be89b-102">Метод ICorProfilerInfo::SetEventMask</span><span class="sxs-lookup"><span data-stu-id="be89b-102">ICorProfilerInfo::SetEventMask Method</span></span>
<span data-ttu-id="be89b-103">Определяет значение, указывающее типы событий, для которых профилировщик хочет получать уведомления от среды CLR.</span><span class="sxs-lookup"><span data-stu-id="be89b-103">Sets a value that specifies the types of events for which the profiler wants to receive notification from the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be89b-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be89b-104">Syntax</span></span>  
  
```  
HRESULT SetEventMask(  
    [in] DWORD dwEvents);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="be89b-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="be89b-105">Parameters</span></span>  
 `dwEvents`  
 <span data-ttu-id="be89b-106">[в] 4-байтовое значение, определяющее категории событий.</span><span class="sxs-lookup"><span data-stu-id="be89b-106">[in] A 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="be89b-107">Каждый бит управляет отдельной возможностью, поведением или типом события.</span><span class="sxs-lookup"><span data-stu-id="be89b-107">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="be89b-108">Биты описаны в [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) перечисления.</span><span class="sxs-lookup"><span data-stu-id="be89b-108">The bits are described in the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="be89b-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="be89b-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="be89b-110">Необходимо вызвать [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) вместо этого метода.</span><span class="sxs-lookup"><span data-stu-id="be89b-110">You should call the [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) method instead of this method.</span></span> <span data-ttu-id="be89b-111">Несмотря на то что `SetEventMask` метод по-прежнему поддерживается, [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) предоставляет дополнительные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="be89b-111">Although the `SetEventMask` method continues to be supported, [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) provides additional functionality.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="be89b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="be89b-112">Requirements</span></span>  
 <span data-ttu-id="be89b-113">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="be89b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="be89b-114">**Заголовок:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="be89b-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="be89b-115">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="be89b-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="be89b-116">**Версии платформы .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="be89b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be89b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="be89b-117">See Also</span></span>  
 [<span data-ttu-id="be89b-118">Интерфейс ICorProfilerInfo</span><span class="sxs-lookup"><span data-stu-id="be89b-118">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="be89b-119">Метод SetEventMask2</span><span class="sxs-lookup"><span data-stu-id="be89b-119">SetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)
