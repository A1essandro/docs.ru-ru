---
title: "Метод IManagedObject::GetSerializedBuffer"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IManagedObject.GetSerializedBuffer
api_location: mscoree.dll
api_type: COM
f1_keywords: GetSerializedBuffer
helpviewer_keywords:
- IManagedObject::GetSerializedBuffer method [.NET Framework hosting]
- GetSerializedBuffer method [.NET Framework hosting]
ms.assetid: c17105bb-b49f-434e-8f9b-77f8c85b9220
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d326fba5cbdb38dd2c5d07f4f69f3f2d8e75114c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="imanagedobjectgetserializedbuffer-method"></a><span data-ttu-id="a7281-102">Метод IManagedObject::GetSerializedBuffer</span><span class="sxs-lookup"><span data-stu-id="a7281-102">IManagedObject::GetSerializedBuffer Method</span></span>
<span data-ttu-id="a7281-103">Возвращает строковое представление данного управляемого объекта.</span><span class="sxs-lookup"><span data-stu-id="a7281-103">Gets the string representation of this managed object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7281-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7281-104">Syntax</span></span>  
  
```  
HRESULT GetSerializedBuffer (  
    [out] BSTR *pBSTR  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a7281-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7281-105">Parameters</span></span>  
 `pBSTR`  
 <span data-ttu-id="a7281-106">[out] Указатель на строку, являющуюся сериализованный объект.</span><span class="sxs-lookup"><span data-stu-id="a7281-106">[out] A pointer to a string that is the serialized object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a7281-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7281-107">Remarks</span></span>  
 <span data-ttu-id="a7281-108">`GetSerializedBuffer` Метод сериализует объект, поэтому он может быть маршалирован клиенту.</span><span class="sxs-lookup"><span data-stu-id="a7281-108">The `GetSerializedBuffer` method serializes the object so it can be marshaled to the client.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a7281-109">Требования</span><span class="sxs-lookup"><span data-stu-id="a7281-109">Requirements</span></span>  
 <span data-ttu-id="a7281-110">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a7281-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a7281-111">**Заголовок:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a7281-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a7281-112">**Библиотека:** включена как ресурс в MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a7281-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a7281-113">**Версии платформы .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a7281-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a7281-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a7281-114">See Also</span></span>  
 [<span data-ttu-id="a7281-115">IManagedObject-интерфейс</span><span class="sxs-lookup"><span data-stu-id="a7281-115">IManagedObject Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/imanagedobject-interface.md)
