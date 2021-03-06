---
title: Выражение типа <type> не доступно для запроса
ms.date: 07/20/2015
f1_keywords:
- bc36593
- vbc36593
helpviewer_keywords:
- BC36593
ms.assetid: 6f1f5860-bf97-4885-9ebb-bc87d028095c
ms.openlocfilehash: 7f74d56b47629ff76f9b935d26278ace8df4c353
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2019
ms.locfileid: "58842334"
---
# <a name="expression-of-type-type-is-not-queryable"></a>Выражение типа \<тип > не поддерживает запросы
Выражение типа \<тип > не поддерживает запросы. Убедитесь, что не пропущена импорта сборки ссылки или пространство имен для поставщика LINQ.  
  
 Запрашиваемые типы определяются в <xref:System.Linq>, <xref:System.Data.Linq>, и <xref:System.Xml.Linq> пространства имен. Необходимо импортировать один или несколько из этих пространств имен для выполнения запросов LINQ.  
  
 <xref:System.Linq> Пространства имен позволяет отправлять запрос объектов, таких как массивы и коллекции с помощью LINQ.  
  
 <xref:System.Data.Linq> Пространства имен позволяет запрашивать наборы данных ADO.NET и баз данных SQL Server с помощью LINQ.  
  
 <xref:System.Xml.Linq> Пространства имен позволяет запрашивать XML с помощью LINQ и использования возможностей XML в Visual Basic.  
  
 **Идентификатор ошибки:** BC36593  
  
## <a name="to-correct-this-error"></a>Исправление ошибки  
  
1.  Добавить `Import` инструкции для <xref:System.Linq>, <xref:System.Data.Linq>, или <xref:System.Xml.Linq> пространства имен в файл кода. Можно также импортировать пространство имен для проекта с помощью **ссылки** страницы в конструкторе проектов (**Мой проект**).  
  
2.  Убедитесь, что тип, определенный как источник запроса является запрашиваемым типом. То есть тип, реализующий <xref:System.Collections.Generic.IEnumerable%601> или <xref:System.Linq.IQueryable%601>.  
  
## <a name="see-also"></a>См. также

- <xref:System.Linq>
- <xref:System.Data.Linq>
- <xref:System.Xml.Linq>
- [Introduction to LINQ in Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md) (Знакомство с LINQ в Visual Basic)
- [LINQ](../../../visual-basic/programming-guide/language-features/linq/index.md)
- [XML](../../../visual-basic/programming-guide/language-features/xml/index.md)
- [Ссылки и оператор Imports](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)
- [Оператор Imports (пространство имен и тип .NET)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
- [Страница "Ссылки" в конструкторе проектов (Visual Basic)](/visualstudio/ide/reference/references-page-project-designer-visual-basic)
