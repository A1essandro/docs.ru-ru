---
title: "Строки (Руководство по программированию на C#)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- C# language, strings
- strings [C#]
ms.assetid: 21580405-cb25-4541-89d5-037846a38b07
caps.latest.revision: "41"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 45dd48a53d3fae58596d9328ef8daba566b2ded1
ms.sourcegitcommit: 685143b62385500f59bc36274b8adb191f573a16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2017
---
# <a name="strings-c-programming-guide"></a>Строки (Руководство по программированию на C#)
Строка — это объект типа <xref:System.String>, значением которого является текст. Внутри программы текст хранится в виде упорядоченной коллекции объектов <xref:System.Char> только для чтения. В конце строки C# нет нуль-символов. Поэтому строка C# может содержать любое число внедренных нуль-символов ('\0'). Свойство <xref:System.String.Length%2A> строки соответствует числу содержащихся в ней объектов `Char`, но не числу символов Юникода. Для доступа к отдельным кодовым точкам Юникода в строке используйте объект <xref:System.Globalization.StringInfo>.  
  
## <a name="string-vs-systemstring"></a>Сравнение строки и System.String  
 В C# ключевое слово `string` является псевдонимом для <xref:System.String>. Таким образом, `String` и `string` эквивалентны, их можно использовать независимо от используемого соглашения об именовании. Класс `String` предоставляет множество методов для безопасного создания, обработки и сравнения строк. Кроме того, язык C# перегружает некоторые операторы для упрощения типичных операций со строками. Дополнительные сведения о ключевых словах см. в статье, посвященной [строкам](../../../csharp/language-reference/keywords/string.md). Дополнительные сведения о типе и его методах см. здесь: <xref:System.String>.  
  
## <a name="declaring-and-initializing-strings"></a>Объявление и инициализация строк  
 Вы можете объявлять и инициализировать строки различными способами, как показано в следующем примере:  
  
 [!code-csharp[csProgGuideStrings#1](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_1.cs)]  
  
 Обратите внимание, что вы не используете оператор [new](../../../csharp/language-reference/keywords/new-operator.md) для создания объекта строки, за исключением случаев инициализации строки с помощью массива символов.  
  
 Инициализируйте строку с константным значением <xref:System.String.Empty> для создания нового объекта <xref:System.String>, строка которого имеет нулевую длину. Представлением строкового литерала строки с нулевой длиной является "". Если вы инициализируете строки со значением <xref:System.String.Empty> вместо [NULL](../../../csharp/language-reference/keywords/null.md), вы снизите вероятность появления исключения <xref:System.NullReferenceException>. Используйте статический метод <xref:System.String.IsNullOrEmpty%28System.String%29>, чтобы проверить значение строки, прежде чем пытаться получить к ней доступ.  
  
## <a name="immutability-of-string-objects"></a>Неизменность строковых объектов  
 Строковые объекты являются *неизменяемыми*: их нельзя изменить после создания. Может показаться, что все методы <xref:System.String> и операторы C# изменяют строку, но в действительности они возвращают результаты в новый строковый объект. Когда содержимое `s1` и `s2` объединяется для формирования одной строки, две исходные строки не изменяются, как показано в следующем примере. Оператор `+=` создает новую строку, которая содержит объединенное содержимое. Этот новый объект присваивается переменной `s1`, а исходный объект, который был присвоен `s1`, освобождается для сборки мусора, так как ни одна переменная не ссылается на него.  
  
 [!code-csharp[csProgGuideStrings#2](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_2.cs)]  
  
 Так как "изменение" строки на самом деле является созданием новой строки, создавать ссылки на строки следует с осторожностью. Если вы создадите ссылку на строку, а затем "измените" исходную строку, ссылка будет по-прежнему указывать на исходный объект, а не на новый объект, который был создан при изменении строки. Это поведение проиллюстрировано в следующем коде:  
  
 [!code-csharp[csProgGuideStrings#25](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_3.cs)]  
  
 Инструкции по созданию новых строк, основанных на таких изменениях, как операции поиска и замены исходной строки, см. в статье [How to: Modify String Contents (C# Programming Guide)](../../../csharp/programming-guide/strings/how-to-modify-string-contents.md) (Практическое руководство. Изменение содержимого строки (руководство по программированию на C#)).  
  
## <a name="regular-and-verbatim-string-literals"></a>Регулярные и буквальные строковые литералы  
 Используйте регулярные строковые литералы, когда вам нужно внедрить escape-символы, доступные в C#, как показано в следующем примере:  
  
 [!code-csharp[csProgGuideStrings#3](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_4.cs)]  
  
 Буквальные строковые литералы используются для удобства и читабельности, если текст строки содержит символы обратной косой черты, например в путях к файлам. Так как буквальные строки сохраняют символы новой строки как часть текста строки, их можно использовать для инициализации многострочных строк. Используйте двойные кавычки, чтобы вставить кавычки в буквальной строке. В следующем примере показаны наиболее часто используемым буквальные строки:  
  
 [!code-csharp[csProgGuideStrings#4](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_5.cs)]  
  
## <a name="string-escape-sequences"></a>Escape-последовательности строк  
  
|Escape-последовательность|Имя символа|Кодировка Юникод|  
|---------------------|--------------------|----------------------|  
|\\'|Одинарная кавычка|0x0027|  
|\\"|Двойная кавычка|0x0022|  
|\\\\ |Обратная косая черта|0x005C|  
|\0|Null|0x0000|  
|\a|Предупреждение|0x0007|  
|\b|Backspace|0x0008|  
|\f|Перевод страницы|0x000C|  
|\n|Новая строка|0x000A|  
|\r|Возврат каретки|0x000D|  
|\t|Горизонтальная табуляция|0x0009|  
|\U|Escape-последовательность Юникода для суррогатных пар.|\Unnnnnnnn|  
|\u|Escape-последовательность Юникода|\u0041 = "A"|  
|\v|Вертикальная табуляция|0x000B|  
|\x|Escape-последовательность Юникода аналогична "\u", она отличается только длиной переменной.|\x0041 = "A"|  
  
> [!NOTE]
>  Во время компиляции буквальные строки преобразуются в обычные строки с теми же escape-последовательностями. Поэтому, если вы просматриваете буквальную строку в окне контрольных значений отладчика, вы увидите escape-символы, добавленные компилятором, а не буквальную версию из исходного кода. Например, буквальная строка @"C:\files.txt"будет отображаться в окне контрольных значений как "C:\\\files.txt".  
  
## <a name="format-strings"></a>Строки формата  
 Строка формата — это строка, содержимое которой можно определить динамически во время выполнения. Чтобы создать строку формата, используйте статический метод <xref:System.String.Format%2A> и внедряйте заполнители в фигурных скобках, которые будут заменены другими значениями во время выполнения. В следующем примере используется строка формата для вывода результатов каждой итерации цикла:  
  
 [!code-csharp[csProgGuideStrings#26](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_6.cs)]  
  
 Одна перегрузка метода <xref:System.Console.WriteLine%2A> принимает в качестве параметра строку формата. Поэтому можно просто внедрить строковый литерал формата без явного вызова метода. Но при использовании метода <xref:System.Diagnostics.Trace.WriteLine%2A> для отображения выходных данных отладки в Visual Studio в окне **Вывод** необходимо явно вызвать метод <xref:System.String.Format%2A>, так как метод <xref:System.Diagnostics.Trace.WriteLine%2A> принимает только строку, а не строку формата. Дополнительные сведения о строках форматах см. в статье [Formatting types](../../../standard/base-types/formatting-types.md) (Типы форматирования).  
  
## <a name="substrings"></a>Подстроки  
 Подстрока — это последовательность символов, содержащихся в строке. Используйте метод <xref:System.String.Substring%2A>, чтобы создать новую строку из части исходной строки. Одно вхождение подстроки или несколько можно найти с помощью метода <xref:System.String.IndexOf%2A>. Используйте метод <xref:System.String.Replace%2A>, чтобы заменить все вхождения указанной подстроки новой строкой. Как и метод <xref:System.String.Substring%2A>, метод <xref:System.String.Replace%2A> фактически возвращает новую строку и не изменяет исходную строку. Дополнительные сведения см. в статьях [How to: Search Strings Using String Methods (C# Programming Guide)](../../../csharp/programming-guide/strings/how-to-search-strings-using-string-methods.md) (Практическое руководство. Поиск строк с помощью строковых методов (руководство по программированию на C#)) и [How to: Modify String Contents (C# Programming Guide)](../../../csharp/programming-guide/strings/how-to-modify-string-contents.md) (Практическое руководство. Изменение содержимого строки (руководство по программированию на C#)).  
  
 [!code-csharp[csProgGuideStrings#7](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_7.cs)]  
  
## <a name="accessing-individual-characters"></a>Доступ к отдельным символам  
 Используя нотацию массива со значением индекса, можно получить доступ только для чтения к отдельным символам, как показано в следующем примере:  
  
 [!code-csharp[csProgGuideStrings#9](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_8.cs)]  
  
 Если вам необходимо изменить отдельные символы в строке и функций методов <xref:System.String> вам недостаточно, используйте объект <xref:System.Text.StringBuilder>, чтобы изменить отдельные символы "на месте", а затем создайте новую строку для сохранения результатов с помощью методов <xref:System.Text.StringBuilder>. В следующем примере предположим, что необходимо определенным образом изменить исходную строку, а затем сохранить результаты для дальнейшего использования:  
  
 [!code-csharp[csProgGuideStrings#8](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_9.cs)]  
  
## <a name="null-strings-and-empty-strings"></a>Строки NULL и пустые строки  
 Пустая строка — это экземпляр объекта <xref:System.String?displayProperty=nameWithType>, который содержит нуль символов. Пустые строки часто используются в различных сценариях программирования для представления пустого текстового поля. Вы можете вызывать методы для пустых строк, так как они являются допустимыми объектами <xref:System.String?displayProperty=nameWithType>. Пустые строки инициализируются следующим образом:  
  
```  
string s = String.Empty;  
```  
  
 В отличие от пустых строк строка NULL не ссылается на экземпляр объекта <xref:System.String?displayProperty=nameWithType>, поэтому любая попытка вызвать метод для строки NULL приводит к исключению <xref:System.NullReferenceException>. Но вы можете использовать строки NULL в операциях объединения и сравнения с другими строками. В следующих примерах показаны случаи, в которых ссылка на строку NULL вызывает и не вызывает исключение:  
  
 [!code-csharp[csProgGuideStrings#27](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_10.cs)]  
  
## <a name="using-stringbuilder-for-fast-string-creation"></a>Использование класса StringBuilder для быстрого создания строк  
 Операции со строками в .NET хорошо оптимизированы, и в большинстве случаев они не снижают производительность. Но в некоторых сценариях, например в сплошных циклах, которые выполняются сотни и тысячи раз, операции со строками могут повлиять на производительность. Класс <xref:System.Text.StringBuilder> создает строковый буфер, который ускоряет работу, если программа выполняет много операций над строками. Строка <xref:System.Text.StringBuilder> также позволяет заново присваивать отдельные символы, что не поддерживает встроенный строковый тип данных. Например, этот код изменяет содержимое строки без создания новой строки:  
  
 [!code-csharp[csProgGuideStrings#20](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_11.cs)]  
  
 В этом примере объект <xref:System.Text.StringBuilder> используется для создания строки из набора числовых типов:  
  
 [!code-csharp[csProgGuideStrings#15](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_12.cs)]  
  
## <a name="strings-extension-methods-and-linq"></a>Строки, методы расширения и LINQ  
 Так как тип <xref:System.String> использует <xref:System.Collections.Generic.IEnumerable%601>, вы можете применять методы расширения, определенные для строк в классе <xref:System.Linq.Enumerable>. Чтобы избежать визуального загромождения, эти методы исключены из IntelliSense для типа <xref:System.String>, но все равно доступны. Можно также использовать выражения запроса [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] в строках. Дополнительные сведения см. в документации по [LINQ и строкам](../../../csharp/programming-guide/concepts/linq/linq-and-strings.md).  
  
## <a name="related-topics"></a>Связанные разделы  
  
|Раздел|Описание|  
|-----------|-----------------|  
|[Практическое руководство. Изменение содержимого строки](../../../csharp/programming-guide/strings/how-to-modify-string-contents.md)|Содержит пример кода, иллюстрирующий изменение содержимого строк.|  
|[Практическое руководство. Сцепка нескольких строк](../../../csharp/programming-guide/strings/how-to-concatenate-multiple-strings.md)|Иллюстрирует использование оператора `+` и класса `Stringbuilder` для соединения строк во время компиляции и во время выполнения.|  
|[Практическое руководство. Сравнение строк](../../../csharp/programming-guide/strings/how-to-compare-strings.md)|Показывает, как выполнять сравнение строк по порядковому номеру.|  
|[How to: Parse Strings Using String.Split (C# Programming Guide)](../../../csharp/programming-guide/strings/how-to-parse-strings-using-string-split.md) (Практическое руководство. Анализ строк с помощью метода String.Split (руководство по программированию на C#))|Содержит пример кода, демонстрирующий использование метода `String.Split` для анализа строк.|  
|[Практическое руководство. Поиск строк с помощью строковых методов](../../../csharp/programming-guide/strings/how-to-search-strings-using-string-methods.md)|Объясняет, как использовать конкретные методы для поиска строк.|  
|[Практическое руководство. Поиск строк с помощью регулярных выражений](../../../csharp/programming-guide/strings/how-to-search-strings-using-regular-expressions.md)|Объясняет, как использовать регулярные выражения для поиска строк.|  
|[Практическое руководство. Определение представления числового значения в строке](../../../csharp/programming-guide/strings/how-to-determine-whether-a-string-represents-a-numeric-value.md)|Объясняет, как безопасно проанализировать строку, чтобы проверить, содержит ли она допустимое числовое значение.|  
|[Практическое руководство. Преобразование строки в значение типа "DateTime"](../../../csharp/programming-guide/strings/how-to-convert-a-string-to-a-datetime.md)|Показывает, как преобразовать строку, например "01/24/2008", в объект <xref:System.DateTime?displayProperty=nameWithType>.|  
|[Базовые операции со строками в .NET Framework](../../../../docs/standard/base-types/basic-string-operations.md)|Содержит ссылки на статьи, в которых показаны базовые операции над строками с помощью методов <xref:System.String?displayProperty=nameWithType> и <xref:System.Text.StringBuilder?displayProperty=nameWithType>.|  
|[Анализ строк в .NET Framework](../../../../docs/standard/base-types/parsing-strings.md)|Описывает способы вставки символов или пробелов в строку.|  
|[Сравнение строк в .NET Framework](../../../../docs/standard/base-types/comparing.md)|Объясняет, как сравнивать строки, и содержит примеры на языках C# и Visual Basic.|  
|[Using the StringBuilder class](../../../standard/base-types/stringbuilder.md) (Использование класса StringBuilder)|Описывает создание и изменение динамических строковых объектов с помощью класса <xref:System.Text.StringBuilder>.|  
|[LINQ и строки](../../../csharp/programming-guide/concepts/linq/linq-and-strings.md)|Содержит инструкции по выполнению различных операций со строками с помощью запросов LINQ.|  
|[Руководство по программированию на C#](../../../csharp/programming-guide/index.md)|Содержит ссылки на статьи с конструкциями программирования на C#.|  
