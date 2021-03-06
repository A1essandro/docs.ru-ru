---
title: Интерфейс IAssemblyName
ms.date: 03/30/2017
api_name:
- IAssemblyName
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName
helpviewer_keywords:
- IAssemblyName interface [.NET Framework fusion]
ms.assetid: f7f8e605-6b67-4151-936f-f04ecd671d90
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 22276e543e8eeb9c6cf9aeee7a9af92c503d3a7d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549019"
---
# <a name="iassemblyname-interface"></a>Интерфейс IAssemblyName
Предоставляет методы для описания и работа с уникальное удостоверение сборки.  
  
## <a name="methods"></a>Методы  
  
|Метод|Описание|  
|------------|-----------------|  
|[Метод Clone](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-clone-method.md)|Создает неполную копию этого `IAssemblyName` объекта.|  
|[Метод Finalize](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-finalize-method.md)|Это позволяет `IAssemblyName` объект освободить ресурсы и выполнить другие операции очистки, прежде чем его деструктора.|  
|[Метод GetDisplayName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getdisplayname-method.md)|Возвращает понятное имя сборки, упоминаемой в этом `IAssemblyName` объекта.|  
|[Метод GetName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getname-method.md)|Получает простое и незашифрованное имя сборки, упоминаемой в этом `IAssemblyName` объекта.|  
|[Метод GetProperty](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getproperty-method.md)|Возвращает указатель на свойство ссылается заданный `PropertyId`.|  
|[Метод GetVersion](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getversion-method.md)|Возвращает сведения о версии для сборки, упоминаемой в этом `IAssemblyName` объекта.|  
|[Метод IsEqual](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-isequal-method.md)|Определяет, является ли заданное `IAssemblyName` объект равен данному `IAssemblyName`, основываясь на флаги указанного сравнения.|  
|[Метод SetProperty](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-setproperty-method.md)|Задает значение свойства, который ссылается заданный `PropertyId`.|  
  
## <a name="requirements"></a>Требования  
 **Платформы:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок.** Fusion.h  
  
 **Версии платформы .NET Framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>См. также
- [Интерфейсы Fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [Интерфейс IAssemblyEnum](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md)
