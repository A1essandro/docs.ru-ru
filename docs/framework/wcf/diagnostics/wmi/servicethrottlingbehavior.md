---
title: ServiceThrottlingBehavior
ms.date: 03/30/2017
ms.assetid: 37b9e517-1f1f-4ec4-9fcb-2b8016794f5b
ms.openlocfilehash: 98e8a720e92547ca0a893dd988b91cb7907660b5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689855"
---
# <a name="servicethrottlingbehavior"></a>ServiceThrottlingBehavior
ServiceThrottlingBehavior  
  
## <a name="syntax"></a>Синтаксис  
  
```csharp  
class ServiceThrottlingBehavior : Behavior  
{  
  sint32 MaxConcurrentCalls;  
  sint32 MaxConcurrentInstances;  
  sint32 MaxConcurrentSessions;  
};  
```  
  
## <a name="methods"></a>Методы  
 Класс ServiceThrottlingBehavior не определяет никаких методов.  
  
## <a name="properties"></a>Свойства  
 Класс ServiceThrottlingBehavior имеет следующие свойства.  
  
### <a name="maxconcurrentcalls"></a>MaxConcurrentCalls  
 Тип данных: sint32  
  
 Тип доступа: Только чтение  
  
 Максимальное количество сообщений, которые могут одновременно обрабатываться во всех объектах диспетчера в узле ServiceHost.  
  
### <a name="maxconcurrentinstances"></a>MaxConcurrentInstances  
 Тип данных: sint32  
  
 Тип доступа: Только чтение  
  
 Максимальное число объектов службы, которые могут выполняться одновременно.  
  
### <a name="maxconcurrentsessions"></a>MaxConcurrentSessions  
 Тип данных: sint32  
  
 Тип доступа: Только чтение  
  
 Максимальное число сеансов, одновременно принимаемых узлом.  
  
## <a name="requirements"></a>Требования  
  
|MOF|Объявлено в файле Servicemodel.mof.|  
|---------|-----------------------------------|  
|Пространство имен|Определено в root\ServiceModel.|  
  
## <a name="see-also"></a>См. также
- <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>
