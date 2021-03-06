---
title: 'EDM (модель данных с использованием сущностей): Наследование'
ms.date: 03/30/2017
ms.assetid: 42c7ef24-710a-4af9-8493-cd41c399ecb0
ms.openlocfilehash: bc0467ea1b242c13e00e115f07ccbc5c840df936
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2019
ms.locfileid: "58837137"
---
# <a name="entity-data-model-inheritance"></a>EDM (модель данных с использованием сущностей): Наследование
Entity Data Model (EDM) поддерживает наследование для [типы сущностей](../../../../docs/framework/data/adonet/entity-type.md). Наследование в модели (EDM) схоже с наследованием для классов в языках объектно-ориентированного программирования. Как и с классами в объектно ориентированных языках, в концептуальной модели можно определить тип сущности ( *производный тип*), наследуемый от другого типа сущности ( *базовый тип*). Тем не менее, в отличие от классов в объектно ориентированного программирования, в концептуальной модели производный тип всегда наследует все [свойства](../../../../docs/framework/data/adonet/property.md) и [свойства навигации](../../../../docs/framework/data/adonet/navigation-property.md) базового типа. В производном типе нельзя отменить унаследованные свойства.  
  
 В концептуальной модели можно построить иерархию наследования, в которой один производный тип наследует свойства другого производного типа. Тип в верхней части иерархии (одного типа в иерархии, который не является производным типом) называется *корневой тип*. В иерархии наследования [ключ сущности](../../../../docs/framework/data/adonet/entity-key.md) должен быть определен в корневом типе.  
  
 Нельзя построить иерархии наследования, в которых один производный тип наследует свойства более чем одного типа. Например, в концептуальной модели с типом сущности `Book` можно определить производные типы `FictionBook` и `NonFictionBook`, из которых каждый наследует свойства `Book`. Тем не менее, в дальнейшем нельзя определить тип, который бы наследовал свойства обоих типов `FictionBook` и `NonFictionBook`.  
  
## <a name="example"></a>Пример  

На следующей схеме показана концептуальная модель с четырьмя типами сущностей: `Book`, `FictionBook`, `Publisher`, и `Author`. Тип сущности `FictionBook` является производным типом, который наследует свойства от типа сущности `Book`. Тип `FictionBook` наследует свойства `ISBN (Key)`, `Title` и `Revision`, а также определяет дополнительное свойство `Genre`.  
  
 ![Схема, показывающая концептуальная модель с четырьмя типами сущностей.](./media/entity-data-model-inheritance/entity-type-inheritance.gif)  
  
 [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) использует доменный язык (DSL), называемый языком определения концептуальной схемы ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) для определения концептуальных моделей. Далее язык CSDL определяет тип сущности, `FictionBook`, который наследует свойства типа `Book` (как показано на схеме выше).  
  
 [!code-xml[EDM_Example_Model#DerivedType](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books5.edmx#derivedtype)]  
  
## <a name="see-also"></a>См. также
- [Основные понятия модели EDM](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Сущностная модель данных](../../../../docs/framework/data/adonet/entity-data-model.md)
