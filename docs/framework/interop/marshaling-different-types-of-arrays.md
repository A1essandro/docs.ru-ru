---
title: Маршалинг различных типов массивов
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- marshaling, Arrays sample
- data marshaling, Arrays sample
ms.assetid: c5ac9920-5b6e-4dc9-bf2d-1f6f8ad3b0bf
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 56ca8e6c077d41552f85b65ba5f6b755165ee11a
ms.sourcegitcommit: 15ab532fd5e1f8073a4b678922d93b68b521bfa0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58654618"
---
# <a name="marshaling-different-types-of-arrays"></a>Маршалинг различных типов массивов
Массив является ссылочным типом в управляемом коде, содержащим один или несколько элементов одного и того же типа. Несмотря на то, что массивы являются ссылочными типами, они передаются в неуправляемые функции в виде параметров In. Это поведение не согласуется со способом передачи управляемых массивов в управляемые объекты в виде параметров In/Out. Подробнее см. в разделе [Копирование и закрепление](copying-and-pinning.md).  
  
 В таблице ниже перечислены параметры маршалинга для массивов и описывается их использование.  
  
|Массив|Описание|  
|-----------|-----------------|  
|Целые числа по значению.|Передает массив целых чисел в виде параметра In.|  
|Целые числа по ссылке.|Передает массив целых чисел в виде параметра In/Out.|  
|Целые числа по значению (двухмерный массив).|Передает матрицу целых чисел в виде параметра In.|  
|Строки по значению.|Передает массив строк в виде параметра In.|  
|Структуры с целыми числами.|Передает массив структур, содержащих целые числа, в виде параметра In/Out.|  
|Структуры со строками.|Передает массив структур, содержащих только строки, в виде параметра In или Out. Элементы массива можно изменять.|  
  
## <a name="example"></a>Пример  
 В этом примере показаны способы передачи массивов следующих типов:  
  
-   массив целых чисел по значению;  
  
-   массив целых чисел, размер которого может быть изменен, по ссылке;  
  
-   многомерный массив (матрица) целых чисел по значению;  
  
-   массив строк по значению;  
  
-   массив структур с целыми числами;  
  
-   массив структур со строками.  
  
 Если маршалинг массива по ссылке не выполняется явным образом, то по умолчанию он осуществляется в виде параметра In. Это поведение можно изменить, применив явным образом атрибуты <xref:System.Runtime.InteropServices.InAttribute> и <xref:System.Runtime.InteropServices.OutAttribute> .  
  
 В этом примере используются перечисленные ниже неуправляемые функции, показанные со своими исходными объявлениями.  
  
-   Функция**TestArrayOfInts** , экспортированная из PinvokeLib.dll.  
  
    ```  
    int TestArrayOfInts(int* pArray, int pSize);  
    ```  
  
-   Функция**TestRefArrayOfInts** , экспортированная из PinvokeLib.dll.  
  
    ```  
    int TestRefArrayOfInts(int** ppArray, int* pSize);  
    ```  
  
-   Функция**TestMatrixOfInts** , экспортированная из PinvokeLib.dll.  
  
    ```  
    int TestMatrixOfInts(int pMatrix[][COL_DIM], int row);  
    ```  
  
-   Функция**TestArrayOfStrings** , экспортированная из PinvokeLib.dll.  
  
    ```  
    int TestArrayOfStrings(char** ppStrArray, int size);  
    ```  
  
-   Функция**TestArrayOfStructs** , экспортированная из PinvokeLib.dll.  
  
    ```  
    int TestArrayOfStructs(MYPOINT* pPointArray, int size);  
    ```  
  
-   Функция**TestArrayOfStructs2** , экспортированная из PinvokeLib.dll.  
  
    ```  
    int TestArrayOfStructs2 (MYPERSON* pPersonArray, int size);  
    ```  
  
 [PinvokeLib.dll](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/as6wyhwt(v=vs.100)) — это пользовательская неуправляемая библиотека, содержащая реализации ранее описанных функций и две переменные структуры: **MYPOINT** и **MYPERSON**. Структуры содержат следующие элементы:  
  
```  
typedef struct _MYPOINT  
{  
   int x;   
   int y;   
} MYPOINT;  
  
typedef struct _MYPERSON  
{  
   char* first;   
   char* last;   
} MYPERSON;  
```  
  
 В этом примере структуры `MyPoint` и `MyPerson` содержат внедренные типы. Чтобы гарантировать последовательное размещение членов в памяти в порядке их появления, применяется атрибут <xref:System.Runtime.InteropServices.StructLayoutAttribute> .  
  
 Класс `LibWrap` содержит набор методов, вызываемых классом `App` . Конкретные сведения о передаче массивов см. в комментариях к приведенному ниже примеру. Массив, который является ссылочным типом, по умолчанию передается в виде параметра In. Чтобы вызывающий объект мог получать результаты, необходимо явным образом применить атрибуты **InAttribute** и **OutAttribute** к аргументу, содержащему массив.  
  
### <a name="declaring-prototypes"></a>Объявление прототипов  
 [!code-csharp[Conceptual.Interop.Marshaling#31](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.interop.marshaling/cs/arrays.cs#31)]
 [!code-vb[Conceptual.Interop.Marshaling#31](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.interop.marshaling/vb/arrays.vb#31)]  
  
### <a name="calling-functions"></a>Вызов функций  
 [!code-csharp[Conceptual.Interop.Marshaling#32](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.interop.marshaling/cs/arrays.cs#32)]
 [!code-vb[Conceptual.Interop.Marshaling#32](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.interop.marshaling/vb/arrays.vb#32)]  
  
## <a name="see-also"></a>См. также
- [Типы данных в вызове неуправляемого кода](marshaling-data-with-platform-invoke.md#platform-invoke-data-types)
- [Создание прототипов в управляемом коде](creating-prototypes-in-managed-code.md)
