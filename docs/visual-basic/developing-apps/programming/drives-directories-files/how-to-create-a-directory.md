---
title: Как выполнить Создание каталога в Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- directories [Visual Basic], creating
- folders [Visual Basic], creating
ms.assetid: 0351a2ca-24d8-43b5-bb39-9b99e6401cff
ms.openlocfilehash: a7ba9ea1e7762b0a4a6660339c331fa6cdeb7858
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2019
ms.locfileid: "56976906"
---
# <a name="how-to-create-a-directory-in-visual-basic"></a>Как выполнить Создание каталога в Visual Basic
Для создания каталога используйте метод `CreateDirectory` объекта `My.Computer.FileSystem`.  
  
 Если каталог уже существует, исключение не возникает.  
  
### <a name="to-create-a-directory"></a>Создание каталога  
  
-   Используйте метод `CreateDirectory`, указав полный путь к папке, где следует создать каталог. В этом примере создается каталог `NewDirectory` в `C:\Documents and Settings\All Users\Documents`.  
  
     [!code-vb[VbVbcnMyFileSystem#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#2)]  
  
## <a name="robust-programming"></a>Отказоустойчивость  
 При следующих условиях возможно возникновение исключения:  
  
-   Неверное имя каталога. Например, оно содержит недопустимые символы или состоит из одних пробелов (<xref:System.ArgumentException>).  
  
-   Родительский каталог создаваемого каталога доступен только для чтения (<xref:System.IO.IOException>).  
  
-   Именем каталога является `Nothing` (<xref:System.ArgumentNullException>).  
  
-   Слишком длинное имя каталога (<xref:System.IO.PathTooLongException>).  
  
-   Имя каталога состоит из двоеточия ":" (<xref:System.NotSupportedException>).  
  
-   У пользователя нет разрешения на создание каталога (<xref:System.UnauthorizedAccessException>).  
  
-   У пользователя нет разрешений в ситуации частичного доверия (<xref:System.Security.SecurityException>).  
  
## <a name="see-also"></a>См. также
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.CreateDirectory%2A>
- [Создание, удаление и перемещение файлов и каталогов](../../../../visual-basic/developing-apps/programming/drives-directories-files/creating-deleting-and-moving-files-and-directories.md)
