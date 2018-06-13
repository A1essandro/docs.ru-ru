---
title: Настройка операций за счет исключительного использования хранимых процедур
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 441e8ef3-998c-4d12-8825-ce66a178f90f
ms.openlocfilehash: 3c60a9e430b4228117fd03a43a30f27342154b1b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
ms.locfileid: "33357518"
---
# <a name="customizing-operations-by-using-stored-procedures-exclusively"></a><span data-ttu-id="1342e-102">Настройка операций за счет исключительного использования хранимых процедур</span><span class="sxs-lookup"><span data-stu-id="1342e-102">Customizing Operations by Using Stored Procedures Exclusively</span></span>
<span data-ttu-id="1342e-103">Распространенным сценарием является доступ к данным с использованием только хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="1342e-103">Access to data by using only stored procedures is a common scenario.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1342e-104">Пример</span><span class="sxs-lookup"><span data-stu-id="1342e-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="1342e-105">Описание</span><span class="sxs-lookup"><span data-stu-id="1342e-105">Description</span></span>  
 <span data-ttu-id="1342e-106">Можно изменить примера, приведенного в [Настройка операций за счет хранимых процедур](../../../../../../docs/framework/data/adonet/sql/linq/customizing-operations-by-using-stored-procedures.md) , заменяя вызов метода, который создает оболочку для хранимой процедуры даже в первом запросе (в результате выполнения динамического SQL).</span><span class="sxs-lookup"><span data-stu-id="1342e-106">You can modify the example provided in [Customizing Operations By Using Stored Procedures](../../../../../../docs/framework/data/adonet/sql/linq/customizing-operations-by-using-stored-procedures.md) by replacing even the first query (which causes dynamic SQL execution) with a method call that wraps a stored procedure.</span></span>  
  
 <span data-ttu-id="1342e-107">Предположим, что `CustomersByCity` является методом, как в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1342e-107">Assume `CustomersByCity` is the method, as in the following example.</span></span>  
  
### <a name="code"></a><span data-ttu-id="1342e-108">Код</span><span class="sxs-lookup"><span data-stu-id="1342e-108">Code</span></span>  
 [!code-csharp[DLinqOverrideDefaultSproc#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefaultSproc/cs/northwind.cs#4)]
 [!code-vb[DLinqOverrideDefaultSproc#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefaultSproc/vb/northwind.vb#4)]  
  
 <span data-ttu-id="1342e-109">Следующий код выполняется без динамического SQL.</span><span class="sxs-lookup"><span data-stu-id="1342e-109">The following code executes without any dynamic SQL.</span></span>  
  
 [!code-csharp[DLinqOverrideDefaultSproc#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefaultSproc/cs/Program.cs#5)]
 [!code-vb[DLinqOverrideDefaultSproc#5](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefaultSproc/vb/Module1.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="1342e-110">См. также</span><span class="sxs-lookup"><span data-stu-id="1342e-110">See Also</span></span>  
 [<span data-ttu-id="1342e-111">Ответственность разработчика при переопределении поведения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1342e-111">Responsibilities of the Developer In Overriding Default Behavior</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/responsibilities-of-the-developer-in-overriding-default-behavior.md)
