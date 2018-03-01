---
title: "Структура USER_THREAD"
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
- USER_THREAD
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- USER_THREAD
helpviewer_keywords:
- USER_THREAD structure [.NET Framework debugging]
ms.assetid: a57c7d71-c4b0-41f9-a964-0c5ee84a3124
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 50533ce25812ad49d538c5a6a6c814d7a9704053
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2017
---
# <a name="userthread-structure"></a><span data-ttu-id="70ffa-102">Структура USER_THREAD</span><span class="sxs-lookup"><span data-stu-id="70ffa-102">USER_THREAD Structure</span></span>
<span data-ttu-id="70ffa-103">Предоставляет сведения о отладчик о потоке.</span><span class="sxs-lookup"><span data-stu-id="70ffa-103">Provides information to a debugger about a thread.</span></span> <span data-ttu-id="70ffa-104">Дополнительные сведения см. в разделе [INotifySource2::SetNotifyFilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md) метод.</span><span class="sxs-lookup"><span data-stu-id="70ffa-104">For more information, see the [INotifySource2::SetNotifyFilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70ffa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70ffa-105">Syntax</span></span>  
  
```  
typedef struct tagUSER_THREAD  
{  
    BYTE    *pSidBuffer;  
    DWORD   dwSidLen;  
    DWORD   dwTid;  
} USER_THREAD;  
```  
  
## <a name="members"></a><span data-ttu-id="70ffa-106">Участники</span><span class="sxs-lookup"><span data-stu-id="70ffa-106">Members</span></span>  
  
|<span data-ttu-id="70ffa-107">Член</span><span class="sxs-lookup"><span data-stu-id="70ffa-107">Member</span></span>|<span data-ttu-id="70ffa-108">Описание:</span><span class="sxs-lookup"><span data-stu-id="70ffa-108">Description</span></span>|  
|------------|-----------------|  
|`pSidBuffer`|<span data-ttu-id="70ffa-109">Адрес буфера потока.</span><span class="sxs-lookup"><span data-stu-id="70ffa-109">Address of thread buffer.</span></span>|  
|`dwSidLen`|<span data-ttu-id="70ffa-110">Длина буфера потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="70ffa-110">Length of thread buffer, in bytes.</span></span>|  
|`dwTid`|<span data-ttu-id="70ffa-111">Идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="70ffa-111">Thread ID.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="70ffa-112">Требования</span><span class="sxs-lookup"><span data-stu-id="70ffa-112">Requirements</span></span>  
 <span data-ttu-id="70ffa-113">**Заголовок:** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="70ffa-113">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70ffa-114">См. также</span><span class="sxs-lookup"><span data-stu-id="70ffa-114">See Also</span></span>  
 [<span data-ttu-id="70ffa-115">Метод SetNotifyFilter</span><span class="sxs-lookup"><span data-stu-id="70ffa-115">SetNotifyFilter Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md)  
 [<span data-ttu-id="70ffa-116">Структуры хранилища символов диагностики</span><span class="sxs-lookup"><span data-stu-id="70ffa-116">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)
