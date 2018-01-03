---
title: "Метод ICorDebugStaticFieldSymbol::GetSize"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 72389860-7e37-4656-ba46-b6aeee1860f8
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: b67cbe6858e91e089c36047d6ed83743e45e1d1c
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugstaticfieldsymbolgetsize-method"></a><span data-ttu-id="b153e-102">Метод ICorDebugStaticFieldSymbol::GetSize</span><span class="sxs-lookup"><span data-stu-id="b153e-102">ICorDebugStaticFieldSymbol::GetSize Method</span></span>
<span data-ttu-id="b153e-103">Получает размер статического поля в байтах.</span><span class="sxs-lookup"><span data-stu-id="b153e-103">Gets the size in bytes of the static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b153e-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b153e-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b153e-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b153e-105">Parameters</span></span>  
 `pcbSize`  
 <span data-ttu-id="b153e-106">[out] Указатель на длину этого поля.</span><span class="sxs-lookup"><span data-stu-id="b153e-106">[out] A pointer to length of the field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b153e-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="b153e-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b153e-108">Этот метод доступен только в машинном коде .NET.</span><span class="sxs-lookup"><span data-stu-id="b153e-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b153e-109">Требования</span><span class="sxs-lookup"><span data-stu-id="b153e-109">Requirements</span></span>  
 <span data-ttu-id="b153e-110">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b153e-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b153e-111">**Заголовок:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b153e-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b153e-112">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b153e-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b153e-113">**Версии платформы .NET framework:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b153e-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b153e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="b153e-114">See Also</span></span>  
 [<span data-ttu-id="b153e-115">Интерфейс ICorDebugStaticFieldSymbol</span><span class="sxs-lookup"><span data-stu-id="b153e-115">ICorDebugStaticFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-interface.md)  
 [<span data-ttu-id="b153e-116">Интерфейсы отладки</span><span class="sxs-lookup"><span data-stu-id="b153e-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
