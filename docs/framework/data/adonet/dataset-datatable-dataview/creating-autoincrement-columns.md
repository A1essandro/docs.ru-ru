---
title: "Создание столбцов AutoIncrement"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: cf09732a-ab54-4d98-89e2-4d0a1f28fbce
caps.latest.revision: "4"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: dotnet
ms.openlocfilehash: 4c9c7e321ac5749aedf7168afaef9d6a7119de62
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2017
---
# <a name="creating-autoincrement-columns"></a><span data-ttu-id="e2fc3-102">Создание столбцов AutoIncrement</span><span class="sxs-lookup"><span data-stu-id="e2fc3-102">Creating AutoIncrement Columns</span></span>
<span data-ttu-id="e2fc3-103">Чтобы обеспечить наличие в столбце уникальных значений, можно указать, что значения в столбце должны увеличиваться автоматически при добавлении новых строк к таблице.</span><span class="sxs-lookup"><span data-stu-id="e2fc3-103">To ensure unique column values, you can set the column values to increment automatically when new rows are added to the table.</span></span> <span data-ttu-id="e2fc3-104">Для создания Автоувеличение <xref:System.Data.DataColumn>, задайте <xref:System.Data.DataColumn.AutoIncrement%2A> свойство столбца **true**.</span><span class="sxs-lookup"><span data-stu-id="e2fc3-104">To create an auto-incrementing <xref:System.Data.DataColumn>, set the <xref:System.Data.DataColumn.AutoIncrement%2A> property of the column to **true**.</span></span> <span data-ttu-id="e2fc3-105"><xref:System.Data.DataColumn> Затем начинается со значения, определенного в <xref:System.Data.DataColumn.AutoIncrementSeed%2A> свойство и в каждой добавляемой строке значение **AutoIncrement** столбца увеличивается на значение, определенное в <xref:System.Data.DataColumn.AutoIncrementStep%2A> свойство столбца.</span><span class="sxs-lookup"><span data-stu-id="e2fc3-105">The <xref:System.Data.DataColumn> then starts with the value defined in the <xref:System.Data.DataColumn.AutoIncrementSeed%2A> property, and with each row added the value of the **AutoIncrement** column increases by the value defined in the <xref:System.Data.DataColumn.AutoIncrementStep%2A> property of the column.</span></span>  
  
 <span data-ttu-id="e2fc3-106">Для **AutoIncrement** столбцы, мы рекомендуем <xref:System.Data.DataColumn.ReadOnly%2A> свойство **DataColumn** присвоить **true**.</span><span class="sxs-lookup"><span data-stu-id="e2fc3-106">For **AutoIncrement** columns, we recommend that the <xref:System.Data.DataColumn.ReadOnly%2A> property of the **DataColumn** be set to **true**.</span></span>  
  
 <span data-ttu-id="e2fc3-107">В следующем примере показано, как создать столбец, значения в котором начинаются с 200 и каждый раз увеличиваются с шагом 3.</span><span class="sxs-lookup"><span data-stu-id="e2fc3-107">The following example demonstrates how to create a column that starts with a value of 200 and adds incrementally in steps of 3.</span></span>  
  
```vb  
Dim workColumn As DataColumn = workTable.Columns.Add( _  
    "CustomerID", typeof(Int32))  
workColumn.AutoIncrement = true  
workColumn.AutoIncrementSeed = 200  
workColumn.AutoIncrementStep = 3  
```  
  
```csharp  
DataColumn workColumn = workTable.Columns.Add(  
    "CustomerID", typeof(Int32));  
workColumn.AutoIncrement = true;  
workColumn.AutoIncrementSeed = 200;  
workColumn.AutoIncrementStep = 3;  
```  
  
## <a name="see-also"></a><span data-ttu-id="e2fc3-108">См. также</span><span class="sxs-lookup"><span data-stu-id="e2fc3-108">See Also</span></span>  
 <xref:System.Data.DataColumn>  
 [<span data-ttu-id="e2fc3-109">Определение схемы DataTable</span><span class="sxs-lookup"><span data-stu-id="e2fc3-109">DataTable Schema Definition</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatable-schema-definition.md)  
 [<span data-ttu-id="e2fc3-110">DataTables</span><span class="sxs-lookup"><span data-stu-id="e2fc3-110">DataTables</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)  
 [<span data-ttu-id="e2fc3-111">Центр разработчиков наборов данных и управляемых поставщиков ADO.NET</span><span class="sxs-lookup"><span data-stu-id="e2fc3-111">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)
