---
title: "Метод ICorDebugSymbolProvider::GetAssemblyImageMetadata"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: c3c9de67-b865-4ecf-b887-1f1d0719a0c0
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 48e5e9daf191cb2f4112dd2a957f29c0a7521398
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugsymbolprovidergetassemblyimagemetadata-method"></a><span data-ttu-id="6fc29-102">Метод ICorDebugSymbolProvider::GetAssemblyImageMetadata</span><span class="sxs-lookup"><span data-stu-id="6fc29-102">ICorDebugSymbolProvider::GetAssemblyImageMetadata Method</span></span>
<span data-ttu-id="6fc29-103">Возвращает метаданные из объединенной сборки.</span><span class="sxs-lookup"><span data-stu-id="6fc29-103">Returns the metadata from a merged assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6fc29-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fc29-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyImageMetadata(  
   [out] ICorDebugMemoryBuffer** ppMemoryBuffer  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6fc29-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fc29-105">Parameters</span></span>  
 `ppMemoryBuffer`  
 <span data-ttu-id="6fc29-106">[out] Указатель на адрес [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) , содержащий сведения о размере и адресе метаданных объединенной сборки.</span><span class="sxs-lookup"><span data-stu-id="6fc29-106">[out] A pointer to the address of an [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) object that contains information about the size and address of the merged assembly's metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6fc29-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="6fc29-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6fc29-108">Этот метод доступен только в машинном коде .NET.</span><span class="sxs-lookup"><span data-stu-id="6fc29-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6fc29-109">Требования</span><span class="sxs-lookup"><span data-stu-id="6fc29-109">Requirements</span></span>  
 <span data-ttu-id="6fc29-110">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6fc29-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6fc29-111">**Заголовок:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6fc29-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6fc29-112">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6fc29-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6fc29-113">**Версии платформы .NET framework:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6fc29-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6fc29-114">См. также</span><span class="sxs-lookup"><span data-stu-id="6fc29-114">See Also</span></span>  
 [<span data-ttu-id="6fc29-115">Интерфейс ICorDebugSymbolProvider</span><span class="sxs-lookup"><span data-stu-id="6fc29-115">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)  
 [<span data-ttu-id="6fc29-116">Интерфейсы отладки</span><span class="sxs-lookup"><span data-stu-id="6fc29-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
