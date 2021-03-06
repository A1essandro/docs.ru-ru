---
title: Метод ICorDebug::DebugActiveProcess
ms.date: 03/30/2017
api_name:
- ICorDebug.DebugActiveProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::DebugActiveProcess
helpviewer_keywords:
- DebugActiveProcess method [.NET Framework debugging]
- ICorDebug::DebugActiveProcess method [.NET Framework debugging]
ms.assetid: fdab0ade-7f56-4fa2-b3ef-f7a1d2852bba
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1b3869c9f96eee6f0e3066a99a58a154a2f5f2ee
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "57480095"
---
# <a name="icordebugdebugactiveprocess-method"></a>Метод ICorDebug::DebugActiveProcess
Присоединяет отладчик к существующему процессу.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
HRESULT DebugActiveProcess (  
    [in]  DWORD               id,  
    [in]  BOOL                win32Attach,  
    [out] ICorDebugProcess    **ppProcess  
);  
```  
  
## <a name="parameters"></a>Параметры  
 `id`  
 [in] Идентификатор процесса, к которому отладчик должен быть связан.  
  
 `win32Attach`  
 [in] Логическое значение, которое будет присвоено `true` Если отладчик должен вести себя как отладчик Win32 для процесса и отправки неуправляемых обратных вызовов; в противном случае `false`.  
  
 `ppProcess`  
 [out] Указатель на адрес объекта «ICorDebugProcess», представляющий процесс, к которому присоединен отладчик.  
  
## <a name="remarks"></a>Примечания  
 Отладки взаимодействия не поддерживается в операционных системах Win9x и не — x86 платформ, таких как основе AMD64 и IA-64-разрядных платформах.  
  
## <a name="requirements"></a>Требования  
 **Платформы:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок.** CorDebug.idl, CorDebug.h  
  
 **Библиотека:** CorGuids.lib  
  
 **Версии платформы .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>См. также
- [Интерфейс ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
