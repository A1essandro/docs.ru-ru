---
title: "Практическое руководство. Выполнение запроса, возвращающего сложные типы"
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
ms.assetid: c2209fdb-70ef-4dea-8bb8-097fe96f5563
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: a499c8cf9caeac480e09d7c965032db2d9fefec4
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-execute-a-query-that-returns-complex-types"></a><span data-ttu-id="8db55-102">Практическое руководство. Выполнение запроса, возвращающего сложные типы</span><span class="sxs-lookup"><span data-stu-id="8db55-102">How to: Execute a Query that Returns Complex Types</span></span>
<span data-ttu-id="8db55-103">В этом разделе показано выполнение запроса на языке [!INCLUDE[esql](../../../../../includes/esql-md.md)], который возвращает объекты типа сущности, содержащие свойство сложного типа.</span><span class="sxs-lookup"><span data-stu-id="8db55-103">This topic shows how to execute an [!INCLUDE[esql](../../../../../includes/esql-md.md)] query that returns entity type objects that contain a property of a complex type.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="8db55-104">Выполнение кода в этом примере</span><span class="sxs-lookup"><span data-stu-id="8db55-104">To run the code in this example</span></span>  
  
1.  <span data-ttu-id="8db55-105">Добавить [модели AdventureWorks Sales](http://msdn.microsoft.com/en-us/f16cd988-673f-4376-b034-129ca93c7832) в проект и настроить проект для использования [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="8db55-105">Add the [AdventureWorks Sales Model](http://msdn.microsoft.com/en-us/f16cd988-673f-4376-b034-129ca93c7832) to your project and configure your project to use the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span> <span data-ttu-id="8db55-106">Дополнительные сведения см. в разделе [как: использовать мастер моделей EDM](http://msdn.microsoft.com/en-us/dadb058a-c5d9-4c5c-8b01-28044112231d).</span><span class="sxs-lookup"><span data-stu-id="8db55-106">For more information, see [How to: Use the Entity Data Model Wizard](http://msdn.microsoft.com/en-us/dadb058a-c5d9-4c5c-8b01-28044112231d).</span></span>  
  
2.  <span data-ttu-id="8db55-107">На странице кода приложения добавьте следующие инструкции `using` (`Imports` в Visual Basic):</span><span class="sxs-lookup"><span data-stu-id="8db55-107">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
3.  <span data-ttu-id="8db55-108">Дважды щелкните EDMX-файл для отображения модели в [окне обозревателя моделей](http://msdn.microsoft.com/en-us/94e836e8-a5ea-47ff-aa3e-599d8a02ebfd) конструктора сущностей.</span><span class="sxs-lookup"><span data-stu-id="8db55-108">Double click the .edmx file to display the model in the [Model Browser window](http://msdn.microsoft.com/en-us/94e836e8-a5ea-47ff-aa3e-599d8a02ebfd) of the Entity Designer.</span></span> <span data-ttu-id="8db55-109">В области конструктора сущностей выберите `Email` и `Phone` свойства `Contact` типа сущности, а затем щелкните правой кнопкой мыши и выберите **рефакторинг в новый сложный тип**.</span><span class="sxs-lookup"><span data-stu-id="8db55-109">On the Entity Designer surface, select the `Email` and `Phone` properties of the `Contact` entity type, then right-click and select **Refactor into New Complex Type**.</span></span>  
  
4.  <span data-ttu-id="8db55-110">Новый сложный тип с выбранным `Email` и `Phone` добавлять свойства к **браузер моделей**.</span><span class="sxs-lookup"><span data-stu-id="8db55-110">A new complex type with the selected `Email` and `Phone` properties is added to the **Model Browser**.</span></span> <span data-ttu-id="8db55-111">Сложный тип присваивается имя по умолчанию: Переименование типа в тип `EmailPhone` в **свойства** окна.</span><span class="sxs-lookup"><span data-stu-id="8db55-111">The complex type is given a default name: rename the type to `EmailPhone` in the **Properties** window.</span></span> <span data-ttu-id="8db55-112">Кроме того, новое свойство `ComplexProperty` добавляется к типу сущности `Contact`.</span><span class="sxs-lookup"><span data-stu-id="8db55-112">Also, a new `ComplexProperty` property is added to the `Contact` entity type.</span></span> <span data-ttu-id="8db55-113">Измените имя свойства на `EmailPhoneComplexType.`</span><span class="sxs-lookup"><span data-stu-id="8db55-113">Rename the property to `EmailPhoneComplexType.`</span></span>  
  
     <span data-ttu-id="8db55-114">Сведения о создании и изменении сложных типов с помощью мастера моделей EDM см. в разделе [как: Рефакторинг существующего свойства в свойство сложного типа](http://msdn.microsoft.com/en-us/5b2eb3b3-693d-42cb-b43a-405812d677eb) и [как: создавать и изменять сложные типы](http://msdn.microsoft.com/en-us/afb8e206-0ffe-4597-b6d4-6ab566897e1d).</span><span class="sxs-lookup"><span data-stu-id="8db55-114">For information about creating and modifying complex types by using the Entity Data Model Wizard, see [How to: Refactor Existing Properties into a Complex Type Property](http://msdn.microsoft.com/en-us/5b2eb3b3-693d-42cb-b43a-405812d677eb) and [How to: Create and Modify Complex Types](http://msdn.microsoft.com/en-us/afb8e206-0ffe-4597-b6d4-6ab566897e1d).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8db55-115">Пример</span><span class="sxs-lookup"><span data-stu-id="8db55-115">Example</span></span>  
 <span data-ttu-id="8db55-116">В следующем примере выполняется запрос, возвращающий коллекцию `Contact` объектов и отображает два свойства `Contact` объектов: `ContactID` и значения `EmailPhoneComplexType` сложного типа.</span><span class="sxs-lookup"><span data-stu-id="8db55-116">The following example executes a query that returns a collection of `Contact` objects and displays two properties of the `Contact` objects: `ContactID` and the values of the `EmailPhoneComplexType` complex type.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts#ComplexTypeWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#complextypewithentitycommand)]
 [!code-vb[DP EntityServices Concepts#ComplexTypeWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#complextypewithentitycommand)]
