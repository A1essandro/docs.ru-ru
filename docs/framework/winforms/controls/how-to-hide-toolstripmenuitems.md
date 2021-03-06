---
title: Практическое руководство. Скрытие объектов ToolStripMenuItem
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], hiding
- MenuStrip control [Windows Forms], hiding menu items
- menus [Windows Forms], hiding menu items
- menu items [Windows Forms], hiding
- hiding menu items
ms.assetid: 418a768f-808a-44cd-8cef-f4e161883621
ms.openlocfilehash: a82df42240ae045f0d6f355f642acfb8082c87a5
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57715260"
---
# <a name="how-to-hide-toolstripmenuitems"></a>Практическое руководство. Скрытие объектов ToolStripMenuItem
Скрытие пунктов меню — это способ управления пользовательским интерфейсом приложения и ограничить команды пользователя. Часто требуется скрыть меню целиком, когда все элементы меню на нем будут недоступны. Это меньше отвлекаться для пользователя. Кроме того можно скрыть и отключить меню или пункта меню, как скрытие не запрещает пользователю доступ к команде меню с помощью сочетания клавиш.  
  
### <a name="to-hide-any-menu-item-programmatically"></a>Чтобы скрыть любой элемент меню программными средствами  
  
-   В методе, где задать свойства элемента меню, добавьте код для задания <xref:System.Windows.Forms.ToolStripItem.Visible%2A> свойства `false`.  
  
    ```vb  
    MenuItem3.Visible = False  
    ```  
  
    ```csharp  
    menuItem3.Visible = false;  
    ```  
  
    ```cpp  
    menuItem3->Visible = false;  
    ```  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.ToolStripItem.Visible%2A>
- <xref:System.Windows.Forms.MenuStrip>
- [Общие сведения об элементе управления MenuStrip](menustrip-control-overview-windows-forms.md)
- [Практическое руководство. Отключение объектов ToolStripMenuItem](how-to-disable-toolstripmenuitems.md)
