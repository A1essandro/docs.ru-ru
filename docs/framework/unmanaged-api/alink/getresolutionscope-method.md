---
title: "Метод GetResolutionScope"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IALink.GetResolutionScope
api_location: alink.dll
api_type: COM
f1_keywords: GetResolutionScope
helpviewer_keywords: GetResolutionScope method
ms.assetid: 5b48ca60-dacd-44b2-9979-4a5122f00812
topic_type: apiref
caps.latest.revision: "5"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: f9dc63a7165ab472e973e0bc4f3e4cbb99e5d828
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2017
---
# <a name="getresolutionscope-method"></a><span data-ttu-id="688c4-102">Метод GetResolutionScope</span><span class="sxs-lookup"><span data-stu-id="688c4-102">GetResolutionScope Method</span></span>
<span data-ttu-id="688c4-103">Извлекает область заданного типа.</span><span class="sxs-lookup"><span data-stu-id="688c4-103">Retrieves the scope of a given type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="688c4-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="688c4-104">Syntax</span></span>  
  
```  
HRESULT GetResolutionScope(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    mdToken     TargetFile,  
    mdToken*    pScope  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="688c4-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="688c4-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="688c4-106">Идентификатор сборки.</span><span class="sxs-lookup"><span data-stu-id="688c4-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="688c4-107">Файл, которому нужна ссылка.</span><span class="sxs-lookup"><span data-stu-id="688c4-107">File that is in need of a reference.</span></span>  
  
 `TargetFile`  
 <span data-ttu-id="688c4-108">Маркер файла, этот тип определен в, как правило, полученные с помощью [метод ImportFile](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span><span class="sxs-lookup"><span data-stu-id="688c4-108">Token of file that type is defined in, usually retrieved with [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span></span>  
  
 `pScope`  
 <span data-ttu-id="688c4-109">Получает сборку или ссылку на модуль.</span><span class="sxs-lookup"><span data-stu-id="688c4-109">Receives the assembly or module reference.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="688c4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="688c4-110">Return Value</span></span>  
 <span data-ttu-id="688c4-111">Возвращает значение S_OK, если метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="688c4-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="688c4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="688c4-112">Requirements</span></span>  
 <span data-ttu-id="688c4-113">Требуется alink.h.</span><span class="sxs-lookup"><span data-stu-id="688c4-113">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="688c4-114">См. также</span><span class="sxs-lookup"><span data-stu-id="688c4-114">See Also</span></span>  
 [<span data-ttu-id="688c4-115">Интерфейс IALink</span><span class="sxs-lookup"><span data-stu-id="688c4-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="688c4-116">Интерфейс IALink2</span><span class="sxs-lookup"><span data-stu-id="688c4-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="688c4-117">API ALink</span><span class="sxs-lookup"><span data-stu-id="688c4-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
