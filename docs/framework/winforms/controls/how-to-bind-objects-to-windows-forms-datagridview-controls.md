---
title: Практическое руководство. Привязка объектов к элементам управления DataGridView Windows Forms
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], object binding
- data grids [Windows Forms], object binding
- object binding [Windows Forms], DataGridView control
ms.assetid: cb8f29fa-577e-4e2b-883f-3a01c6189b9c
ms.openlocfilehash: 9f3ce61b3692f0b83298bdf9a19cb98fb5d5ab7f
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57723807"
---
# <a name="how-to-bind-objects-to-windows-forms-datagridview-controls"></a>Практическое руководство. Привязка объектов к элементам управления DataGridView Windows Forms
В следующем примере кода показано, как связать коллекцию объектов с элементом управления <xref:System.Windows.Forms.DataGridView>, чтобы каждый объект отображался отдельной строкой. В этом примере также показано, как отобразить свойство с типом перечисления в <xref:System.Windows.Forms.DataGridViewComboBoxColumn>, чтобы в раскрывающемся списке для поля со списком содержались значения перечисления.  
  
## <a name="example"></a>Пример  
 [!code-csharp[System.Windows.Forms.DataGridView._CollectionBound#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView._CollectionBound/CS/collectionbound.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridView._CollectionBound#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView._CollectionBound/VB/collectionbound.vb#00)]  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Для этого примера требуются:  
  
-   ссылки на сборки System и System.Windows.Forms;  
  
 Сведения о выполнении сборки этого примера из командной строки для Visual Basic или Visual C#, см. в разделе [построение из командной строки](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) или [командной строки создания с помощью csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Можно также сборке этого примера в Visual Studio путем вставки кода в новый проект.  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.DataGridView>
- [Отображение данных с помощью элемента управления DataGridView в Windows Forms](displaying-data-in-the-windows-forms-datagridview-control.md)
- [Практическое руководство. Доступ к связанным объектам в Windows Forms DataGridView строк](how-to-access-objects-bound-to-windows-forms-datagridview-rows.md)
