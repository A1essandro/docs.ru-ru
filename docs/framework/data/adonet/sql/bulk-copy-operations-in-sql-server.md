---
title: Операции массового копирования в SQL Server
ms.date: 03/30/2017
ms.assetid: 83a7a0d2-8018-4354-97b9-0b1d99f8342b
ms.openlocfilehash: 87373f55181742a243c60bc4b471334535d88ff7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
ms.locfileid: "33360430"
---
# <a name="bulk-copy-operations-in-sql-server"></a><span data-ttu-id="d529d-102">Операции массового копирования в SQL Server</span><span class="sxs-lookup"><span data-stu-id="d529d-102">Bulk Copy Operations in SQL Server</span></span>
<span data-ttu-id="d529d-103">Microsoft SQL Server включает популярную программу командной строки **bcp** обеспечивающую быстрое массовое копирование больших файлов в таблицы или представления в базах данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d529d-103">Microsoft SQL Server includes a popular command-line utility named **bcp** for quickly bulk copying large files into tables or views in SQL Server databases.</span></span> <span data-ttu-id="d529d-104">Класс <xref:System.Data.SqlClient.SqlBulkCopy> позволяет разрабатывать решения на управляемом коде, обеспечивающие аналогичную функциональность.</span><span class="sxs-lookup"><span data-stu-id="d529d-104">The <xref:System.Data.SqlClient.SqlBulkCopy> class allows you to write managed code solutions that provide similar functionality.</span></span> <span data-ttu-id="d529d-105">Существуют другие способы загрузки данных в таблицу SQL Server (например, инструкция INSERT), но класс <xref:System.Data.SqlClient.SqlBulkCopy> существенно превосходит их по производительности.</span><span class="sxs-lookup"><span data-stu-id="d529d-105">There are other ways to load data into a SQL Server table (INSERT statements, for example) but <xref:System.Data.SqlClient.SqlBulkCopy> offers a significant performance advantage over them.</span></span>  
  
 <span data-ttu-id="d529d-106">Класс <xref:System.Data.SqlClient.SqlBulkCopy> может использоваться для записи данных только в таблицы SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d529d-106">The <xref:System.Data.SqlClient.SqlBulkCopy> class can be used to write data only to SQL Server tables.</span></span> <span data-ttu-id="d529d-107">SQL Server не является единственным источником данных. Можно использовать любой источник данных при условии, что данные можно будет загрузить в экземпляр <xref:System.Data.DataTable> или считать экземпляром <xref:System.Data.IDataReader>.</span><span class="sxs-lookup"><span data-stu-id="d529d-107">But the data source is not limited to SQL Server; any data source can be used, as long as the data can be loaded to a <xref:System.Data.DataTable> instance or read with a <xref:System.Data.IDataReader> instance.</span></span>  
  
 <span data-ttu-id="d529d-108">При помощи класса <xref:System.Data.SqlClient.SqlBulkCopy> можно выполнить следующие операции.</span><span class="sxs-lookup"><span data-stu-id="d529d-108">Using the <xref:System.Data.SqlClient.SqlBulkCopy> class, you can perform:</span></span>  
  
-   <span data-ttu-id="d529d-109">Отдельную операцию массового копирования.</span><span class="sxs-lookup"><span data-stu-id="d529d-109">A single bulk copy operation</span></span>  
  
-   <span data-ttu-id="d529d-110">Несколько операций массового копирования.</span><span class="sxs-lookup"><span data-stu-id="d529d-110">Multiple bulk copy operations</span></span>  
  
-   <span data-ttu-id="d529d-111">Операцию массового копирования внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="d529d-111">A bulk copy operation within a transaction</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d529d-112">При использовании .NET Framework версии 1.1 или более ранней версии (который не поддерживает <xref:System.Data.SqlClient.SqlBulkCopy> класса), можно выполнить SQL Server Transact-SQL **BULK INSERT** инструкции с помощью <xref:System.Data.SqlClient.SqlCommand> объекта.</span><span class="sxs-lookup"><span data-stu-id="d529d-112">When using .NET Framework version 1.1 or earlier (which does not support the <xref:System.Data.SqlClient.SqlBulkCopy> class), you can execute the SQL Server Transact-SQL **BULK INSERT** statement using the <xref:System.Data.SqlClient.SqlCommand> object.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d529d-113">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d529d-113">In This Section</span></span>  
 [<span data-ttu-id="d529d-114">Установка примера массового копирования</span><span class="sxs-lookup"><span data-stu-id="d529d-114">Bulk Copy Example Setup</span></span>](../../../../../docs/framework/data/adonet/sql/bulk-copy-example-setup.md)  
 <span data-ttu-id="d529d-115">Описывает таблицы, используемые в примерах массового копирования, и содержит скрипты SQL для создания таблиц в базе данных AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="d529d-115">Describes the tables used in the bulk copy examples and provides SQL scripts for creating the tables in the AdventureWorks database.</span></span>  
  
 [<span data-ttu-id="d529d-116">Отдельные операции массового копирования</span><span class="sxs-lookup"><span data-stu-id="d529d-116">Single Bulk Copy Operations</span></span>](../../../../../docs/framework/data/adonet/sql/single-bulk-copy-operations.md)  
 <span data-ttu-id="d529d-117">Описывает выполнение отдельной операции массового копирования данных в экземпляр SQL Server с помощью класса <xref:System.Data.SqlClient.SqlBulkCopy> и операции массового копирования с помощью инструкций Transact-SQL и класса <xref:System.Data.SqlClient.SqlCommand>.</span><span class="sxs-lookup"><span data-stu-id="d529d-117">Describes how to do a single bulk copy of data into an instance of SQL Server using the <xref:System.Data.SqlClient.SqlBulkCopy> class, and how to perform the bulk copy operation using Transact-SQL statements and the <xref:System.Data.SqlClient.SqlCommand> class.</span></span>  
  
 [<span data-ttu-id="d529d-118">Несколько операций массового копирования</span><span class="sxs-lookup"><span data-stu-id="d529d-118">Multiple Bulk Copy Operations</span></span>](../../../../../docs/framework/data/adonet/sql/multiple-bulk-copy-operations.md)  
 <span data-ttu-id="d529d-119">Описывает выполнение нескольких операций массового копирования данных в экземпляр SQL Server с помощью класса <xref:System.Data.SqlClient.SqlBulkCopy>.</span><span class="sxs-lookup"><span data-stu-id="d529d-119">Describes how to do multiple bulk copy operations of data into an instance of SQL Server using the <xref:System.Data.SqlClient.SqlBulkCopy> class.</span></span>  
  
 [<span data-ttu-id="d529d-120">Транзакции и операции массового копирования</span><span class="sxs-lookup"><span data-stu-id="d529d-120">Transaction and Bulk Copy Operations</span></span>](../../../../../docs/framework/data/adonet/sql/transaction-and-bulk-copy-operations.md)  
 <span data-ttu-id="d529d-121">Описывает выполнение операции массового копирования внутри транзакции, включая фиксацию или откат транзакции.</span><span class="sxs-lookup"><span data-stu-id="d529d-121">Describes how to perform a bulk copy operation within a transaction, including how to commit or rollback the transaction.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d529d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d529d-122">See Also</span></span>  
 [<span data-ttu-id="d529d-123">SQL Server и ADO.NET</span><span class="sxs-lookup"><span data-stu-id="d529d-123">SQL Server and ADO.NET</span></span>](../../../../../docs/framework/data/adonet/sql/index.md)  
 [<span data-ttu-id="d529d-124">Центр разработчиков наборов данных и управляемых поставщиков ADO.NET</span><span class="sxs-lookup"><span data-stu-id="d529d-124">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)
