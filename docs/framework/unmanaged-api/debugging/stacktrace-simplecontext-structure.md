---
title: Структура StackTrace_SimpleContext
ms.date: 03/30/2017
api_name:
- StackTrace_SimpleContext
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- SimpleContext
helpviewer_keywords:
- SimpleContext structure [.NET Framework debugging]
- StackTrace_SimpleContext structure [.NET Framework debugging]
ms.assetid: d4cef11f-a8ca-49bc-a1b8-6631f9e28f3e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 510ef77f217cdd6e3441e3d6684d431fc31307fd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54698925"
---
# <a name="stacktracesimplecontext-structure"></a>Структура StackTrace_SimpleContext
Обеспечивает простой контекст, который может использоваться вместо полной структуры `CONTEXT`.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
struct StackTrace_SimpleContext  
{  
    ULONG64 StackOffset;       // ESP on x86  
    ULONG64 FrameOffset;       // EBP on x86  
    ULONG64 InstructionOffset; // EIP on x86  
};  
```  
  
## <a name="members"></a>Участники  
  
|Член|Описание:|  
|------------|-----------------|  
|`StackOffset`|Указатель стека или указатель стека ввод (ESP) на x86 платформ.|  
|`FrameOffset`|Смещение кадра или регистр EBP на x86 платформ.|  
|`InstructionOffset`|Указатель инструкций или указатель инструкции ввод (EIP) на x86 платформ.|  
  
## <a name="remarks"></a>Примечания  
 Так как функции трассировки стека обычно нужно вернуть только адрес, смещение кадров и адрес в стеке, при необходимости можно использовать `SimpleContext` структуры вместо большой `CONTEXT` структуры.  
  
## <a name="requirements"></a>Требования  
 **Платформы:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок.** SOS_Stacktrace.h  
  
 **Версии платформы .NET Framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>См. также
- [Структуры отладки](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [Отладка](../../../../docs/framework/unmanaged-api/debugging/index.md)
