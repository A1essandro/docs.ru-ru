---
title: "Метод ISymENCUnmanagedMethod::GetSourceExtentInDocument"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymENCUnmanagedMethod.GetSourceExtentInDocument
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymENCUnmanagedMethod::GetSourceExtentInDocument
helpviewer_keywords:
- GetSourceExtentInDocument method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetSourceExtentInDocument method [.NET Framework debugging]
ms.assetid: 9c5566ab-4ec7-4b61-9753-839bb90ae78c
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 3cff81968926f608de8d28d730a00e79dc8b1c3b
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="isymencunmanagedmethodgetsourceextentindocument-method"></a><span data-ttu-id="ab58d-102">Метод ISymENCUnmanagedMethod::GetSourceExtentInDocument</span><span class="sxs-lookup"><span data-stu-id="ab58d-102">ISymENCUnmanagedMethod::GetSourceExtentInDocument Method</span></span>
<span data-ttu-id="ab58d-103">Возвращает наименьшую начальную или наибольшую конечную строку метода в определенном документе.</span><span class="sxs-lookup"><span data-stu-id="ab58d-103">Gets the smallest start line and largest end line for the method in a specific document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab58d-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab58d-104">Syntax</span></span>  
  
```  
HRESULT GetSourceExtentInDocument(  
    [in]  ISymUnmanagedDocument *document,  
    [out] ULONG32* pstartLine,  
    [out] ULONG32* pendLine);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ab58d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab58d-105">Parameters</span></span>  
 `document`  
 <span data-ttu-id="ab58d-106">[in] Указатель на документ.</span><span class="sxs-lookup"><span data-stu-id="ab58d-106">[in] A pointer to the document.</span></span>  
  
 `pstartLine`  
 <span data-ttu-id="ab58d-107">[out] Указатель на `ULONG32` , получающий начальной строки.</span><span class="sxs-lookup"><span data-stu-id="ab58d-107">[out] A pointer to a `ULONG32` that receives the start line.</span></span>  
  
 `pendLine`  
 <span data-ttu-id="ab58d-108">[out] Указатель на `ULONG32` , получающий конца строки.</span><span class="sxs-lookup"><span data-stu-id="ab58d-108">[out] A pointer to a `ULONG32` that receives the end line.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ab58d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab58d-109">Return Value</span></span>  
 <span data-ttu-id="ab58d-110">Значение S_OK, если метод выполнен успешно; в противном случае — значение E_FAIL или другим кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="ab58d-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ab58d-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ab58d-111">Requirements</span></span>  
 <span data-ttu-id="ab58d-112">**Заголовок:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ab58d-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab58d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="ab58d-113">See Also</span></span>  
 [<span data-ttu-id="ab58d-114">Интерфейс ISymENCUnmanagedMethod</span><span class="sxs-lookup"><span data-stu-id="ab58d-114">ISymENCUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)
