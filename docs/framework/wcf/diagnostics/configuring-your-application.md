---
title: Настройка приложения
ms.date: 03/30/2017
ms.assetid: a2f995b0-669d-4721-b00f-4561ec7eb6a4
ms.openlocfilehash: 39d8c73809b8c2695ccebb1d69d1c016fd2313d1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54584640"
---
# <a name="configuring-your-application"></a>Настройка приложения
Windows Communication Foundation (WCF) использует систему конфигурации .NET и позволяет настраивать службы в области компьютера и приложения.  
  
 Параметры конфигурации, определенные WCF, находятся в `<system.serviceModel>` группы разделов. Дополнительные сведения о том, как настроить службу WCF см. в разделах:  
  
-   [Настройка служб](../../../../docs/framework/wcf/configuring-services.md)  
  
-   [\<system.serviceModel>](../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)  
  
 Определяемые приложением параметры конфигурации определяются в группе разделов `<appSettings>`. Дополнительные сведения о параметрах приложения в файлах конфигурации .NET см. в разделе [ \<appSettings >](https://go.microsoft.com/fwlink/?LinkId=95159).  
  
## <a name="using-the-configuration-editor"></a>Использование редактора конфигураций  
 WCF [средство редактирования конфигурации (SvcConfigEditor.exe)](../../../../docs/framework/wcf/configuration-editor-tool-svcconfigeditor-exe.md) позволяет администраторам и разработчикам создавать и изменять параметры конфигурации для служб WCF, с помощью графического интерфейса. При помощи этого средства можно управлять параметрами для привязок, поведений, служб и диагностики WCF без непосредственного редактирования XML-файлов конфигурации.  
  
## <a name="editing-configuration-files-in-visual-studio"></a>Изменение файлов конфигурации в Visual Studio  
 Чтобы изменить файл конфигурации проекта службы WCF в Visual Studio, щелкните правой кнопкой мыши в **обозревателе решений** и выберите **изменить конфигурацию WCF** пункт контекстного меню. Это откроет [средство редактирования конфигурации (SvcConfigEditor.exe)](../../../../docs/framework/wcf/configuration-editor-tool-svcconfigeditor-exe.md).  
  
> [!NOTE]
>  Если изменить файл конфигурации проекта веб-службы WCF в Visual Studio щелкните правой кнопкой мыши в **обозревателе решений**, обратите внимание, что **изменить конфигурацию WCF** отсутствует пункт контекстного меню. Чтобы решить эту проблему, щелкните **средства** меню и выберите **Редактор конфигураций служб WCF**. После этого щелкните правой кнопкой мыши файл конфигурации и использовать **изменить конфигурацию WCF** пункт контекстного меню.  
  
## <a name="see-also"></a>См. также
- [Редактор конфигурации (SvcConfigEditor.exe)](../../../../docs/framework/wcf/configuration-editor-tool-svcconfigeditor-exe.md)
- [Настройка служб](../../../../docs/framework/wcf/configuring-services.md)
- [\<system.serviceModel>](../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)
