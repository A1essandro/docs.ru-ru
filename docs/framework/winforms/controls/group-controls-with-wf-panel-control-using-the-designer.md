---
title: Практическое руководство. Группа элементов управления с помощью панели управления Windows Forms с помощью конструктора
ms.date: 03/30/2017
helpviewer_keywords:
- Panel control [Windows Forms], grouping controls
- controls [Windows Forms], grouping
- Windows Forms controls, grouping
ms.assetid: 7e1cd708-fdb1-49d8-9ca2-5640b276bf2e
ms.openlocfilehash: f1aa3b54eb842bb92e4ae2cbb562a11464acac63
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57717457"
---
# <a name="how-to-group-controls-with-the-windows-forms-panel-control-using-the-designer"></a>Практическое руководство. Группа элементов управления с помощью панели управления Windows Forms с помощью конструктора
Windows Forms <xref:System.Windows.Forms.Panel> элементы управления используются для группировки других элементов управления. Существуют три причины для группировки элементов управления. Первая — визуальная группировка связанных элементов форм для упрощения пользовательского интерфейса; Вторая — программная Группировка, переключателей, например; Последнее — перемещение элементов управления как единое целое во время разработки.  
  
> [!NOTE]
>  Отображаемые диалоговые окна и команды меню могут отличаться от описанных в справке в зависимости от текущих параметров или выпуска. Чтобы изменить параметры, выберите в меню **Сервис** пункт **Импорт и экспорт параметров** . Дополнительные сведения см. в разделе [Персонализация интегрированной среды разработки Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-create-a-group-of-controls"></a>Чтобы создать группу элементов управления  
  
1.  Перетащите <xref:System.Windows.Forms.Panel> управления из **Windows Forms** вкладки панели элементов на форму.  
  
2.  Добавьте другие элементы управления на панель, рисования каждого элемента внутри панели.  
  
     Если у вас есть существующие элементы управления, которые вы хотите включить в панель, можно выбрать все элементы управления, вырезать их в буфер обмена, выберите <xref:System.Windows.Forms.Panel> управления, а затем вставьте их в панель. Также можно перетащить их в панель.  
  
3.  (Необязательно) Если вы хотите добавить на панель границу, задайте его <xref:System.Windows.Forms.BorderStyle> свойство. Существует три варианта: <xref:System.Windows.Forms.BorderStyle.Fixed3D>, <xref:System.Windows.Forms.BorderStyle.FixedSingle>, и <xref:System.Windows.Forms.BorderStyle.None>.  
  
## <a name="see-also"></a>См. также
- [Элемент управления Panel](panel-control-windows-forms.md)
- [Общие сведения об элементе управления Panel](panel-control-overview-windows-forms.md)
- [Практическое руководство. Меняем цвет фона панели](how-to-set-the-background-of-a-windows-forms-panel.md)
