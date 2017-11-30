---
title: "Метод ICorDebugProcess5::GetObject"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugProcess5.GetObject
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugProcess5::GetObject
helpviewer_keywords:
- GetObject method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::GetObject method [.NET Framework debugging]
ms.assetid: c8111502-5a20-447f-9dc2-76e8acd7ed5a
topic_type: apiref
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 8966b113e331488a27664de8d42eca4c2db5e51e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugprocess5getobject-method"></a><span data-ttu-id="8df80-102">Метод ICorDebugProcess5::GetObject</span><span class="sxs-lookup"><span data-stu-id="8df80-102">ICorDebugProcess5::GetObject Method</span></span>
<span data-ttu-id="8df80-103">Преобразует адрес объекта в объект «ICorDebugObjectValue».</span><span class="sxs-lookup"><span data-stu-id="8df80-103">Converts an object address to an "ICorDebugObjectValue" object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8df80-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8df80-104">Syntax</span></span>  
  
```  
HRESULT GetObject(  
    [in] CORDB_ADDRESS addr,   
    [out] ICorDebugObjectValue **ppObject  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8df80-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="8df80-105">Parameters</span></span>  
 `addr`  
 <span data-ttu-id="8df80-106">[in] Адрес объекта.</span><span class="sxs-lookup"><span data-stu-id="8df80-106">[in] The object address.</span></span>  
  
 `ppObject`  
 <span data-ttu-id="8df80-107">[out] Указатель на адрес объекта «ICorDebugObjectValue».</span><span class="sxs-lookup"><span data-stu-id="8df80-107">[out] A pointer to the address of an  "ICorDebugObjectValue" object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8df80-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="8df80-108">Remarks</span></span>  
 <span data-ttu-id="8df80-109">Если `addr` не указывает на допустимый управляемый объект `GetObject` возвращает `E_FAIL`.</span><span class="sxs-lookup"><span data-stu-id="8df80-109">If `addr` does not point to a valid managed object, the `GetObject` method returns `E_FAIL`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8df80-110">Требования</span><span class="sxs-lookup"><span data-stu-id="8df80-110">Requirements</span></span>  
 <span data-ttu-id="8df80-111">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8df80-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8df80-112">**Заголовок:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8df80-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8df80-113">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8df80-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8df80-114">**Версии платформы .NET framework:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8df80-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8df80-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8df80-115">See Also</span></span>  
 [<span data-ttu-id="8df80-116">Интерфейс ICorDebugProcess5</span><span class="sxs-lookup"><span data-stu-id="8df80-116">ICorDebugProcess5 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md)  
 [<span data-ttu-id="8df80-117">Интерфейсы отладки</span><span class="sxs-lookup"><span data-stu-id="8df80-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
