---
title: Практическое руководство. Элементов управления с привязкой к тому же источнику данных будут синхронизированы
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], binding multiple
- controls [Windows Forms], synchronizing with data source
ms.assetid: c2f0ecc6-11e6-4c2c-a1ca-0759630c451e
ms.openlocfilehash: 01cec80c85beb64975648b2250c914fe04d3ac95
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57721389"
---
# <a name="how-to-ensure-multiple-controls-bound-to-the-same-data-source-remain-synchronized"></a>Практическое руководство. Элементов управления с привязкой к тому же источнику данных будут синхронизированы
Иногда при работе с привязкой данных в Windows Forms, несколько элементов управления привязаны к тому же источнику данных. В некоторых случаях может потребоваться выполнить дополнительные шаги, чтобы убедиться, что привязанного свойства элементов управления будут синхронизированы друг с другом и источником данных. Эти шаги необходимы в двух случаях:  
  
-   Если источник данных не реализует <xref:System.ComponentModel.IBindingList>и поэтому вызывает <xref:System.ComponentModel.IBindingList.ListChanged> события типа <xref:System.ComponentModel.ListChangedType.ItemChanged>.  
  
-   Если источник данных реализует <xref:System.ComponentModel.IEditableObject>.  
  
 В первом случае можно использовать <xref:System.Windows.Forms.BindingSource> для привязки источника данных к элементам управления. В последнем случае используется <xref:System.Windows.Forms.BindingSource> и обрабатывать <xref:System.Windows.Forms.BindingSource.BindingComplete> событий и вызовов <xref:System.Windows.Forms.BindingManagerBase.EndCurrentEdit%2A> в связанном <xref:System.Windows.Forms.BindingManagerBase>.  
  
## <a name="example"></a>Пример  
 В следующем примере кода показано, как привязать три элемента управления — два элемента управления текстового поля и <xref:System.Windows.Forms.DataGridView> элемента управления, в том же столбце в <xref:System.Data.DataSet> с помощью <xref:System.Windows.Forms.BindingSource> компонента. В этом примере показано, как обрабатывать <xref:System.Windows.Forms.BindingSource.BindingComplete> событий и убедитесь, что при изменении текстовое значение первого поля, текстового поля и <xref:System.Windows.Forms.DataGridView> обновление элемента управления с правильным значением.  
  
 В примере используется <xref:System.Windows.Forms.BindingSource> для привязки источника данных и элементов управления. Кроме того, можно привязать элементы управления непосредственно к источнику данных и извлечь <xref:System.Windows.Forms.BindingManagerBase> для привязки из формы <xref:System.Windows.Forms.Control.BindingContext%2A> и затем обработать <xref:System.Windows.Forms.BindingManagerBase.BindingComplete> событие для <xref:System.Windows.Forms.BindingManagerBase>. Например, как это сделать, см. на странице справки <xref:System.Windows.Forms.BindingManagerBase.BindingComplete> событие <xref:System.Windows.Forms.BindingManagerBase>.  
  
 [!code-csharp[System.Windows.Forms.BindingSourceMultipleControls#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleControls/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.BindingSourceMultipleControls#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleControls/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Компиляция кода  
  
-   Данный пример кода требует  
  
-   ссылки на сборки <xref:System>, <xref:System.Windows.Forms> и <xref:System.Drawing>.  
  
-   Форма с <xref:System.Windows.Forms.Form.Load> событие как обработанное и вызов `InitializeControlsAndDataSource` метод в примере из формы <xref:System.Windows.Forms.Form.Load> обработчик событий.  
  
## <a name="see-also"></a>См. также
- [Практическое руководство. Совместное использование связанных данных в нескольких формах с помощью компонента BindingSource](./controls/how-to-share-bound-data-across-forms-using-the-bindingsource-component.md)
- [Уведомления об изменениях в привязке данных Windows Forms](change-notification-in-windows-forms-data-binding.md)
- [Интерфейсы, относящиеся к привязке данных](interfaces-related-to-data-binding.md)
- [Привязка данных Windows Forms](windows-forms-data-binding.md)
