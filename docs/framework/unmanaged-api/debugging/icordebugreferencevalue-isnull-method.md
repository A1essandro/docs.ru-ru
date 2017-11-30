---
title: "Метод ICorDebugReferenceValue::IsNull"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugReferenceValue.IsNull
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugReferenceValue::IsNull
helpviewer_keywords:
- IsNull method, ICorDebugReferenceValue interface [.NET Framework debugging]
- ICorDebugReferenceValue::IsNull method [.NET Framework debugging]
ms.assetid: 99e8c8d7-a1c0-47c8-9dbd-03e0b2bcb4d5
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f8a7892900149380c979f0bee1a4229407af8c9c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugreferencevalueisnull-method"></a><span data-ttu-id="cd079-102">Метод ICorDebugReferenceValue::IsNull</span><span class="sxs-lookup"><span data-stu-id="cd079-102">ICorDebugReferenceValue::IsNull Method</span></span>
<span data-ttu-id="cd079-103">Получает значение, указывающее, является ли этот ICorDebugReferenceValue значение null, в этом случае `ICorDebugReferenceValue` не указывает на объект.</span><span class="sxs-lookup"><span data-stu-id="cd079-103">Gets a value that indicates whether this ICorDebugReferenceValue is a null value, in which case the `ICorDebugReferenceValue` does not point to an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd079-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd079-104">Syntax</span></span>  
  
```  
HRESULT IsNull (  
    [out] BOOL   *pbNull  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cd079-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd079-105">Parameters</span></span>  
 `pbNull`  
 <span data-ttu-id="cd079-106">[out] Указатель на значение типа Boolean, `true` при этом `ICorDebugReferenceValue` объекта null, в противном случае — `pbNull` — `false`.</span><span class="sxs-lookup"><span data-stu-id="cd079-106">[out] A pointer to a Boolean value that is `true` if this `ICorDebugReferenceValue` object is null; otherwise, `pbNull` is `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd079-107">Требования</span><span class="sxs-lookup"><span data-stu-id="cd079-107">Requirements</span></span>  
 <span data-ttu-id="cd079-108">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cd079-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd079-109">**Заголовок:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cd079-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cd079-110">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cd079-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cd079-111">**Версии платформы .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd079-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
