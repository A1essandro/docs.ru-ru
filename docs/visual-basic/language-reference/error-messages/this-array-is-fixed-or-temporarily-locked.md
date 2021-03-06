---
title: Массив имеет фиксированный размер или временно заблокирован (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrID10
ms.assetid: de6713a6-51d7-4edb-8515-d5fb544e2091
ms.openlocfilehash: f0b80e2be007ff44569365f37a2331f1ecd7a216
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2019
ms.locfileid: "58839409"
---
# <a name="this-array-is-fixed-or-temporarily-locked-visual-basic"></a>Массив имеет фиксированный размер или временно заблокирован (Visual Basic)
Эта ошибка имеет следующие возможные причины:  
  
-   С помощью `ReDim` изменение числа элементов массива фиксированного размера.  
  
-   Изменение размерности динамического массива на уровне модуля, в котором один элемент был передан процедуре в качестве аргумента. Если передается элемент, массив заблокирован, чтобы предотвратить освобождение памяти для ссылочного параметра в процедуре.  
  
-   Попытка присвоить значение `Variant` переменную, содержащую массив, но `Variant` в данный момент заблокирована.  
  
## <a name="to-correct-this-error"></a>Исправление ошибки  
  
1.  Сделайте исходный массив динамическим, а не устранена, объявив ее с `ReDim` (при объявлении массива в процедуре), либо путем объявления его без указания числа элементов (если массив был объявлен на уровне модуля.  
  
2.  Определите, необходима ли передача элемента, так как он является видимым в пределах всех процедур в модуле.  
  
3.  Определите, что заблокирована `Variant` и разблокируйте ее.  
  
## <a name="see-also"></a>См. также

- [Массивы](../../../visual-basic/programming-guide/language-features/arrays/index.md)
