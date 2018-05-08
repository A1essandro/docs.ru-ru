---
title: Практическое руководство. Переход по заданному URL с помощью элемента управления WebBrowser
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- WebBrowser.Navigate
helpviewer_keywords:
- WebBrowser control [Windows Forms], examples
- URLs [Windows Forms], navigating to
- WebBrowser control [Windows Forms], navigating to URLs
- examples [Windows Forms], WebBrowser control
ms.assetid: b3ec38cb-f509-4d0b-bd79-9f3611259c62
ms.openlocfilehash: f34577d45ddfbd2445fd4558c5694facf3f1aa29
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-navigate-to-a-url-with-the-webbrowser-control"></a>Практическое руководство. Переход по заданному URL с помощью элемента управления WebBrowser
В следующем примере кода показано, как переходить <xref:System.Windows.Forms.WebBrowser> управления определенный URL-адрес.  
  
 Чтобы определить, когда новый документ полностью загружен, необходимо обработать событие <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> событий. Это событие см [как: печать с элементом управления WebBrowser](../../../../docs/framework/winforms/controls/how-to-print-with-a-webbrowser-control.md).  
  
## <a name="example"></a>Пример  
  
```vb  
Me.webBrowser1.Navigate("http://www.microsoft.com")  
```  
  
```csharp  
this.webBrowser1.Navigate("http://www.microsoft.com");  
```  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Для этого примера требуются:  
  
-   элемент управления <xref:System.Windows.Forms.WebBrowser> с именем `webBrowser1`;  
  
-   ссылки на сборки `System` и `System.Windows.Forms`.  
  
## <a name="see-also"></a>См. также  
 <xref:System.Windows.Forms.WebBrowser>  
 <xref:System.Windows.Forms.WebBrowser.DocumentCompleted?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.WebBrowser.Navigating?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.WebBrowser.Navigated?displayProperty=nameWithType>  
 [Элемент управления WebBrowser](../../../../docs/framework/winforms/controls/webbrowser-control-windows-forms.md)  
 [Практическое руководство. Печать с использованием элемента управления WebBrowser](../../../../docs/framework/winforms/controls/how-to-print-with-a-webbrowser-control.md)
