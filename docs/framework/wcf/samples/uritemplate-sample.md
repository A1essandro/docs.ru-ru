---
title: Пример UriTemplate
ms.date: 03/30/2017
ms.assetid: 0aaf91d0-ce18-468d-8006-bc9bc2e48231
ms.openlocfilehash: 565e01fd591149e7eefb7e125b917ddb9acccbfe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54735481"
---
# <a name="uritemplate-sample"></a>Пример UriTemplate
Класс <xref:System.UriTemplate> предоставляет методы для работы с наборами кодов URI, использующих общую структуру. Данный образец демонстрирует следующие ключевые понятия, связанные с `UriTemplate`.  
  
-   Синтаксис создания шаблонов.  
  
-   Создание экземпляров кодов URI из шаблона `UriTemplate` с помощью методов <xref:System.UriTemplate.BindByName%2A> и <xref:System.UriTemplate.BindByPosition%2A>.  
  
-   Метод <xref:System.UriTemplateTable.Match%2A>, являющийся обратной операцией для `BindByName` и `BindByPosition`.  
  
### <a name="to-set-up-build-and-run-the-sample"></a>Настройка, сборка и выполнение образца  
  
1.  Чтобы создать выпуск решения на языке C# или Visual Basic .NET, следуйте инструкциям в разделе [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).  
  
2.  Чтобы выполнить образец на одном или нескольких компьютерах, следуйте инструкциям в [выполнение образцов Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).  
  
> [!IMPORTANT]
>  Образцы уже могут быть установлены на компьютере. Перед продолжением проверьте следующий каталог (по умолчанию).  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Если этот каталог не существует, перейдите к [Windows Communication Foundation (WCF) и образцы Windows Workflow Foundation (WF) для .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) для загрузки всех Windows Communication Foundation (WCF) и [!INCLUDE[wf1](../../../../includes/wf1-md.md)] примеры. Этот образец расположен в следующем каталоге.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Web\UriTemplate`  
  
## <a name="see-also"></a>См. также
- [Таблица UriTemplate](../../../../docs/framework/wcf/samples/uritemplate-table-sample.md)
- [Диспетчер таблицы UriTemplate](../../../../docs/framework/wcf/samples/uritemplate-table-dispatcher-sample.md)
