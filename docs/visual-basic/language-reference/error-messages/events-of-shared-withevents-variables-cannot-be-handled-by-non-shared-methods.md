---
title: События общих переменных WithEvents не могут обрабатываться не используемыми совместно методами
ms.date: 07/20/2015
f1_keywords:
- bc30594
- vbc30594
helpviewer_keywords:
- BC30594
ms.assetid: 5b9fceb4-ab11-41bb-ad3b-6f1a9da8ae7e
ms.openlocfilehash: 2b32043898986b3e3e68fab18c5f907843d7691c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2019
ms.locfileid: "58838655"
---
# <a name="events-of-shared-withevents-variables-cannot-be-handled-by-non-shared-methods"></a>События общих переменных WithEvents не могут обрабатываться не используемыми совместно методами
Переменная, объявленная с `Shared` модификатор является общей переменной. Общей переменной определяет строго одно место хранения. Переменная, объявленная с `WithEvents` модификатором обработки набора событий, вызываемых переменной типа, к которому относится переменная. Когда значение присваивается переменной, свойства, созданные `WithEvents` объявление отсоединяется от любого существующего обработчика событий и подключает обработчик событий с помощью `Add` метод.  
  
 **Идентификатор ошибки:** BC30594  
  
## <a name="to-correct-this-error"></a>Исправление ошибки  
  
-   Объявите обработчик событий `Shared`.  
  
## <a name="see-also"></a>См. также

- [Общие](../../../visual-basic/language-reference/modifiers/shared.md)
- [WithEvents](../../../visual-basic/language-reference/modifiers/withevents.md)
