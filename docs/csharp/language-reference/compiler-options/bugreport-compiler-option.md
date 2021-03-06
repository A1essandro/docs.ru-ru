---
title: -bugreport (параметры компилятора C#)
ms.date: 07/20/2015
f1_keywords:
- /bugreport
helpviewer_keywords:
- /bugreport compiler option [C#]
- -bugreport compiler option [C#]
- bugreport compiler option [C#]
ms.assetid: f39665e3-4f6f-4357-88a2-3274c7bec0c1
ms.openlocfilehash: 63d64acc0d0a1ed90a722db75b467bd3ce5f260e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560344"
---
# <a name="-bugreport-c-compiler-options"></a>-bugreport (параметры компилятора C#)
Указывает, что отладочную информацию следует поместить в файл для последующего анализа.  
  
## <a name="syntax"></a>Синтаксис  
  
```console  
-bugreport:file  
```  
  
## <a name="arguments"></a>Аргументы  
 `file`  
 Имя файла, который будет содержать отчет об ошибках.  
  
## <a name="remarks"></a>Примечания  
 Параметр **-bugreport** указывает, что в `file` нужно поместить следующую информацию:  
  
-   Копия всех файлов исходного кода, включенных в компиляцию.  
  
-   Список параметров компилятора, используемых при компиляции.  
  
-   Сведения о версии компилятора, среды выполнения и операционной системы.  
  
-   Сборки и модули, на которые задаются ссылки, в формате шестнадцатеричных чисел, за исключением сборок, входящих в комплект поставки .NET Framework и SDK.  
  
-   Выходные данные компилятора (если есть).  
  
-   Описание проблемы, которое вам потребуется предоставить.  
  
-   Описание предполагаемого способа разрешения проблемы, которое вам потребуется предоставить.  
  
 Если этот параметр используется с параметром **-errorreport:prompt** или **-errorreport:send**, содержимое файла будет передано в корпорацию Майкрософт.  
  
 Поскольку в `file` будут помещены копии всех файлов исходного кода, рекомендуется воспроизводить предполагаемую ошибку в коде с использованием максимально короткой программы.  
  
 Этот параметр компилятора недоступен в Visual Studio и не может быть изменен программным способом.  
  
 Обратите внимание, что содержимое созданного файла раскрывает исходный код, что может привести к непреднамеренному разглашению информации.  
  
## <a name="see-also"></a>См. также

- [Параметры компилятора C# ](../../../csharp/language-reference/compiler-options/index.md)
- [-errorreport (параметры компилятора C#)](../../../csharp/language-reference/compiler-options/errorreport-compiler-option.md)
- [Управление свойствами проектов и решений](/visualstudio/ide/managing-project-and-solution-properties)
