---
title: "Parallel LINQ (PLINQ) | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-standard"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "PLINQ, overview"
ms.assetid: 3d4d0cd3-bde4-490b-99e7-f4e41be96455
caps.latest.revision: 17
author: "rpetrusha"
ms.author: "ronpet"
manager: "wpickett"
caps.handback.revision: 14
---
# Parallel LINQ (PLINQ)
Параллельный LINQ \(PLINQ\) является параллельной реализацией LINQ to Objects.  PLINQ реализует полный набор стандартных операторов запроса LINQ как методы расширения для пространства имен T:System.Linq и имеет дополнительные операторы для параллельных операций.  PLINQ объединяет простоту и удобство чтения синтаксиса LINQ с мощностью параллельного программирования.  Подобно коду, предназначенному для библиотеки параллельных задач, запросы PLINQ масштабируют в степень параллелизма на основе возможностей главного компьютера.  
  
 Во многих сценариях PLINQ может значительно увеличить скорость запросов LINQ to Objects, более эффективно используя все доступные ядра на главном компьютере.  Повышенная производительность увеличивает вычислительную мощностью на рабочем столе.  
  
## Содержание  
 [Introduction to PLINQ](../../../docs/standard/parallel-programming/introduction-to-plinq.md)  
  
 [Understanding Speedup in PLINQ](../../../docs/standard/parallel-programming/understanding-speedup-in-plinq.md)  
  
 [Order Preservation in PLINQ](../../../docs/standard/parallel-programming/order-preservation-in-plinq.md)  
  
 [Merge Options in PLINQ](../../../docs/standard/parallel-programming/merge-options-in-plinq.md)  
  
 [How to: Create and Execute a Simple PLINQ Query](../../../docs/standard/parallel-programming/how-to-create-and-execute-a-simple-plinq-query.md)  
  
 [How to: Control Ordering in a PLINQ Query](../../../docs/standard/parallel-programming/how-to-control-ordering-in-a-plinq-query.md)  
  
 [How to: Combine Parallel and Sequential LINQ Queries](../../../docs/standard/parallel-programming/how-to-combine-parallel-and-sequential-linq-queries.md)  
  
 [How to: Handle Exceptions in a PLINQ Query](../../../docs/standard/parallel-programming/how-to-handle-exceptions-in-a-plinq-query.md)  
  
 [How to: Cancel a PLINQ Query](../../../docs/standard/parallel-programming/how-to-cancel-a-plinq-query.md)  
  
 [How to: Write a Custom PLINQ Aggregate Function](../../../docs/standard/parallel-programming/how-to-write-a-custom-plinq-aggregate-function.md)  
  
 [How to: Specify the Execution Mode in PLINQ](../../../docs/standard/parallel-programming/how-to-specify-the-execution-mode-in-plinq.md)  
  
 [How to: Specify Merge Options in PLINQ](../../../docs/standard/parallel-programming/how-to-specify-merge-options-in-plinq.md)  
  
 [How to: Iterate File Directories with PLINQ](../../../docs/standard/parallel-programming/how-to-iterate-file-directories-with-plinq.md)  
  
 [How to: Measure PLINQ Query Performance](../../../docs/standard/parallel-programming/how-to-measure-plinq-query-performance.md)  
  
 [PLINQ Data Sample](../../../docs/standard/parallel-programming/plinq-data-sample.md)  
  
## См. также  
 <xref:System.Linq.ParallelEnumerable>   
 [Parallel Programming](../../../docs/standard/parallel-programming/index.md)   
 [LINQ \(Language\-Integrated Query\)](../Topic/LINQ%20\(Language-Integrated%20Query\).md)