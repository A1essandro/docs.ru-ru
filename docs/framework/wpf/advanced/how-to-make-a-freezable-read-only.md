---
title: Практическое руководство. Задание объекта Freezable как доступного только для чтения
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], making read-only
ms.assetid: 6c544b7d-d3c9-4736-aa90-4b8728234ccb
ms.openlocfilehash: 874724584b44c17ff6c01331295cfa1a60978d54
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57360359"
---
# <a name="how-to-make-a-freezable-read-only"></a>Практическое руководство. Задание объекта Freezable как доступного только для чтения
В этом примере показано, как сделать <xref:System.Windows.Freezable> только для чтения, вызвав его <xref:System.Windows.Freezable.Freeze%2A> метод.  
  
 Невозможно закрепить <xref:System.Windows.Freezable> объекта, если одно из следующих условий не `true` об объекте:  
  
-   Объект имеет анимированные или свойства с привязкой к данным.  
  
-   Он имеет свойства, которые задаются динамический ресурс. Дополнительные сведения о динамических ресурсов, см. в разделе [ресурсы XAML](xaml-resources.md).  
  
-   Он содержит <xref:System.Windows.Freezable> вложенные объекты, которые нельзя зафиксировать.  
  
 Если эти условия выполняются `false` для вашей <xref:System.Windows.Freezable> объекта и вы не собираетесь изменять, можно зафиксировать, чтобы получить выигрыш в производительности.  
  
## <a name="example"></a>Пример  
 В следующем примере фиксируется <xref:System.Windows.Media.SolidColorBrush>, который представляет собой разновидность <xref:System.Windows.Freezable> объекта.  
  
 [!code-csharp[freezablesample_procedural#FreezeExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#freezeexample1)]
 [!code-vb[freezablesample_procedural#FreezeExample1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#freezeexample1)]  
  
 Дополнительные сведения о <xref:System.Windows.Freezable> объектов, см. в разделе [Freezable Общие сведения об объектах](freezable-objects-overview.md).  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CanFreeze%2A>
- <xref:System.Windows.Freezable.Freeze%2A>
- [Общие сведения об объектах класса Freezable](freezable-objects-overview.md)
- [Разделы практического руководства](base-elements-how-to-topics.md)
