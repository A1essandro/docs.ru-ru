---
title: Практическое руководство. Обрезка и масштабирование изображений
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], cropping
- images [Windows Forms], scaling
ms.assetid: 053e3360-bca0-4b25-9afa-0e77a6f17b03
ms.openlocfilehash: ff0567dca0fd86736e02a9dd827ec15df8bf2df8
ms.sourcegitcommit: 15ab532fd5e1f8073a4b678922d93b68b521bfa0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58654501"
---
# <a name="how-to-crop-and-scale-images"></a>Практическое руководство. Обрезка и масштабирование изображений
<xref:System.Drawing.Graphics> Класс предоставляет несколько <xref:System.Drawing.Graphics.DrawImage%2A> методы, некоторые из которых имеют параметры прямоугольника источника и назначения, которые можно использовать для обрезки и масштабирования изображений.  
  
## <a name="example"></a>Пример  
 В следующем примере создается <xref:System.Drawing.Image> объект из файла Apple.gif. Код рисует изображение всей apple в его исходном размере. Затем код вызывает <xref:System.Drawing.Graphics.DrawImage%2A> метод <xref:System.Drawing.Graphics> для рисования фрагмента изображения apple в прямоугольник назначения, который больше, чем исходное изображение apple.  
  
 <xref:System.Drawing.Graphics.DrawImage%2A> Метод определяет, какая часть элемента apple для рисования, просмотрев исходный прямоугольник, который задается в-четвертых, третий, пятая и шестая аргументы. В этом случае apple обрезается 75 процентов от его ширины и 75% высоты.  
  
 <xref:System.Drawing.Graphics.DrawImage%2A> Метод определяет, где рисовать обрезанное apple и как осуществлять обрезанное apple, просмотрев целевого прямоугольника, который указан с помощью второго аргумента. В этом случае целевого прямоугольника — 30% шире и 30% выше, чем исходное изображение.  
  
 Ниже показан исходный apple и масштабированное обрезанное изображение.  
  
 ![Снимок экрана исходный образ и то же изображение обрезается.](./media/how-to-crop-and-scale-images/original-image-cropped-image.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.WorkingWithImages#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Предыдущий пример предназначен для работы с Windows Forms и требует <xref:System.Windows.Forms.PaintEventArgs> `e`, который является параметром <xref:System.Windows.Forms.Control.Paint> обработчик событий. Не забудьте заменить `Apple.gif` путь, допустимые в вашей системе и имя файла изображения.  
  
## <a name="see-also"></a>См. также
- [Изображения, точечные рисунки и метафайлы](images-bitmaps-and-metafiles.md)
- [Работа с растровыми и векторными изображениями, значками и метафайлами](working-with-images-bitmaps-icons-and-metafiles.md)
