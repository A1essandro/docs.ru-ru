---
title: Практическое руководство. Установка текстового содержимого для элемента управления TextBox
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text content [WPF], setting
- TextBox control [WPF], setting text content
ms.assetid: bcd25fc7-a52f-4453-b802-2c8d2b335ab8
ms.openlocfilehash: 6c0e6e53518d382a2052efa43993d418e35fa0f2
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57364129"
---
# <a name="how-to-set-the-text-content-of-a-textbox-control"></a>Практическое руководство. Установка текстового содержимого для элемента управления TextBox
В этом примере показано, как использовать <xref:System.Windows.Controls.TextBox.Text%2A> свойство для задания начального текстового содержимого элемента <xref:System.Windows.Controls.TextBox> элемента управления.  
  
 **Примечание** несмотря на то что [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] использовать версию примера `<TextBox.Text>` теги вокруг текста каждой кнопки <xref:System.Windows.Controls.TextBox> содержимого, нет необходимости поскольку <xref:System.Windows.Controls.TextBox> применяется <xref:System.Windows.Markup.ContentPropertyAttribute> для атрибута <xref:System.Windows.Controls.TextBox.Text%2A> свойство. Дополнительные сведения см. в разделе [Обзор XAML (WPF)](../advanced/xaml-overview-wpf.md).  
  
## <a name="example"></a>Пример  
 [!code-xaml[TextBox_MiscCode#_TextBoxSetTextXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_textboxsettextxaml)]  
  
## <a name="example"></a>Пример  
 [!code-csharp[TextBox_MiscCode#_TextBoxSetText](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textboxsettext)]
 [!code-vb[TextBox_MiscCode#_TextBoxSetText](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_textboxsettext)]  
  
## <a name="see-also"></a>См. также
- [Общие сведения о TextBox](textbox-overview.md)
- [Общие сведения о RichTextBox](richtextbox-overview.md)
