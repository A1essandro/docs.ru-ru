---
title: "Структура USER_THREAD"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: USER_THREAD
api_location: diasymreader.dll
api_type: COM
f1_keywords: USER_THREAD
helpviewer_keywords: USER_THREAD structure [.NET Framework debugging]
ms.assetid: a57c7d71-c4b0-41f9-a964-0c5ee84a3124
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: d93002fe5460bfdb36d4e11c74410677b46a98d7
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="userthread-structure"></a>Структура USER_THREAD
Предоставляет сведения о отладчик о потоке. Дополнительные сведения см. в разделе [INotifySource2::SetNotifyFilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md) метод.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
typedef struct tagUSER_THREAD  
{  
    BYTE    *pSidBuffer;  
    DWORD   dwSidLen;  
    DWORD   dwTid;  
} USER_THREAD;  
```  
  
## <a name="members"></a>Члены  
  
|Член|Описание|  
|------------|-----------------|  
|`pSidBuffer`|Адрес буфера потока.|  
|`dwSidLen`|Длина буфера потока в байтах.|  
|`dwTid`|Идентификатор потока.|  
  
## <a name="requirements"></a>Требования  
 **Заголовок:** ProtocolNotify2.idl  
  
## <a name="see-also"></a>См. также  
 [Метод SetNotifyFilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md)  
 [Структуры хранения символов диагностики](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)
