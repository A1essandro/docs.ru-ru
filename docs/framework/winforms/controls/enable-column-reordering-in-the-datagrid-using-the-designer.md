---
title: Практическое руководство. Разрешение изменения порядка столбцов в элементе управления DataGridView формы Windows с помощью конструктора
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], column order
- Windows Forms, columns
- columns [Windows Forms], reordering
- data [Windows Forms], displaying
ms.assetid: d82bd69c-6799-4439-a32c-91139c5901d1
ms.openlocfilehash: a08c15e4fea76d8f6e97db6d463c4141b7d13b4b
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57718835"
---
# <a name="how-to-enable-column-reordering-in-the-windows-forms-datagridview-control-using-the-designer"></a>Практическое руководство. Разрешение изменения порядка столбцов в элементе управления DataGridView формы Windows с помощью конструктора
При просмотре данных, отображаемых в формах Windows <xref:System.Windows.Forms.DataGridView> элемента управления, иногда пользователи хотят для сравнения значений в определенных столбцах. Это может быть неудобно, если столбцы находятся далеко друг от друга в элементе управления, особенно в том случае, если пользователям нужно прокручивать экран вперед и назад по горизонтали для просмотра всех столбцов, которые их интересуют. Можно сделать задачу сравнения значений столбца проще, позволяя пользователям изменять порядок столбцов. Когда вы включаете изменения порядка столбцов, пользователи могут переместить столбец в новое положение, перетащив заголовок столбца с помощью мыши.  
  
 Следующая процедура требуется **приложения Windows** проекта с формой, содержащей <xref:System.Windows.Forms.DataGridView> элемента управления. Сведения о настройке такого проекта см. в разделе [как: Создайте проект приложения Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) и [как: Добавление элементов управления в Windows Forms](how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Отображаемые диалоговые окна и команды меню могут отличаться от описанных в справке в зависимости от текущих параметров или выпуска. Чтобы изменить параметры, выберите в меню **Сервис** пункт **Импорт и экспорт параметров** . Дополнительные сведения см. в разделе [Персонализация интегрированной среды разработки Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-enable-column-reordering"></a>Чтобы включить изменение порядка столбцов  
  
-   Щелкните глиф смарт-тега (![глиф смарт-тега](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) в правом верхнем углу <xref:System.Windows.Forms.DataGridView> управления, а затем выберите **РазрешитьИзменениепорядкастолбцов**.  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType>
- [Практическое руководство. Закрепление столбцов в элементе управления DataGridView формы Windows с помощью конструктора](freeze-columns-in-the-datagrid-using-the-designer.md)
- [Практическое руководство. Создание проекта приложения Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project).
- [Практическое руководство. Добавление элементов управления Windows Forms](how-to-add-controls-to-windows-forms.md)
