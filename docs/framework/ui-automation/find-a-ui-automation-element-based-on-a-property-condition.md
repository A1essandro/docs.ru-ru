---
title: Нахождение Элемента Автоматизации Пользовательского Интерфейса в Зависимости от Состояния Свойства
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- elements, finding by property conditions
- UI Automation, finding elements by property conditions
ms.assetid: 3acaee5a-6ce8-4c3e-81c8-67e59eb74477
ms.openlocfilehash: 83d3a36d08463cedf46c176208625e76907db2d8
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2019
ms.locfileid: "57675112"
---
# <a name="find-a-ui-automation-element-based-on-a-property-condition"></a>Нахождение Элемента Автоматизации Пользовательского Интерфейса в Зависимости от Состояния Свойства
> [!NOTE]
>  Эта документация предназначена для разработчиков .NET Framework, желающих использовать управляемые классы [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] , заданные в пространстве имен <xref:System.Windows.Automation> . Для получения последних сведений о [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], см. в разделе [API автоматизации Windows: Модели автоматизации пользовательского интерфейса](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 В этом разделе содержится пример кода, показано, как найти элемент в [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] дерева на основе конкретного свойства или свойств.  
  
## <a name="example"></a>Пример  
 В следующем примере набор условий свойства указываются, которые задают определенный элемент (или элементов), интерес в <xref:System.Windows.Automation.AutomationElement> дерева. Затем выполняется поиск всех соответствующих элементов с <xref:System.Windows.Automation.AutomationElement.FindAll%2A> метод, который включает ряд <xref:System.Windows.Automation.AndCondition> логических операций, чтобы ограничить число найденных элементов.  
  
> [!NOTE]
>  При поиске по указанию <xref:System.Windows.Automation.AutomationElement.RootElement%2A>, следует попытаться получить только прямые потомки. Поиск потомков может выполнить итерацию сотни или даже тысячи элементов, что может привести к переполнению стека. Если вы пытаетесь получить определенный элемент на более низком уровне, необходимо запустить поиск из окна приложения или из контейнера на более низком уровне.  
  
 [!code-csharp[InvokePatternApp#1100](../../../samples/snippets/csharp/VS_Snippets_Wpf/InvokePatternApp/CSharp/InvokePatternApp.cs#1100)]
 [!code-vb[InvokePatternApp#1100](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/InvokePatternApp/VisualBasic/Client.vb#1100)]  
  
## <a name="see-also"></a>См. также
- [InvokePattern и образец элемента меню ExpandCollapsePattern](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms771636(v=vs.90))
- [Получение элементов модели автоматизации пользовательского интерфейса](../../../docs/framework/ui-automation/obtaining-ui-automation-elements.md)
- [Использование свойства AutomationID](../../../docs/framework/ui-automation/use-the-automationid-property.md)
