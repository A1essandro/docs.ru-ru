---
title: Метод IMetaDataEmit2::SaveDelta
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SaveDelta
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SaveDelta
helpviewer_keywords:
- IMetaDataEmit2::SaveDelta method [.NET Framework metadata]
- SaveDelta method [.NET Framework metadata]
ms.assetid: b95739fe-d2fa-4776-ae0d-31d9707ef799
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7098bceee6bf60cd7781606ffc889b6af9c3e3cf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445339"
---
# <a name="imetadataemit2savedelta-method"></a><span data-ttu-id="5079d-102">Метод IMetaDataEmit2::SaveDelta</span><span class="sxs-lookup"><span data-stu-id="5079d-102">IMetaDataEmit2::SaveDelta Method</span></span>
<span data-ttu-id="5079d-103">Сохраняет изменения в текущем сеансе edit and continue в указанный файл.</span><span class="sxs-lookup"><span data-stu-id="5079d-103">Saves changes from the current edit-and-continue session to the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5079d-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5079d-104">Syntax</span></span>  
  
```  
HRESULT SaveDelta (  
    [in] LPCWSTR     szFile,   
    [in] DWORD       dwSaveFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5079d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="5079d-105">Parameters</span></span>  
 `szFile`  
 <span data-ttu-id="5079d-106">[in] Имя файла, в котором хотите сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="5079d-106">[in] The file name under which to save changes.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="5079d-107">[in] Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="5079d-107">[in] Reserved.</span></span> <span data-ttu-id="5079d-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5079d-108">Must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5079d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="5079d-109">Requirements</span></span>  
 <span data-ttu-id="5079d-110">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5079d-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5079d-111">**Заголовок:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="5079d-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5079d-112">**Библиотека:** используется как ресурс в MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5079d-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5079d-113">**Версии платформы .NET framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5079d-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5079d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="5079d-114">See Also</span></span>  
 [<span data-ttu-id="5079d-115">Интерфейс IMetaDataEmit2</span><span class="sxs-lookup"><span data-stu-id="5079d-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)  
 [<span data-ttu-id="5079d-116">Интерфейс IMetaDataEmit</span><span class="sxs-lookup"><span data-stu-id="5079d-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
