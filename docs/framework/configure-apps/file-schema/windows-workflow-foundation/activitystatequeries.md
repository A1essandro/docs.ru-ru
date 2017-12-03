---
title: '&lt;activityStateQueries&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: bdd3c8ae-a13f-4df1-9b3c-a9d6c4bb1b5f
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 175089dad7809e412444681076163163bd6831e7
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2017
---
# <a name="ltactivitystatequeriesgt"></a><span data-ttu-id="79d02-102">&lt;activityStateQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="79d02-102">&lt;activityStateQueries&gt;</span></span>
<span data-ttu-id="79d02-103">Представляет коллекцию запросов, которые используются для отслеживания изменений жизненного цикла действий, составляющих экземпляр рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="79d02-103">Represents a collection of queries that are used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="79d02-104">Например можно хранить список каждый раз завершение действия «Send E-Mail» внутри экземпляра рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="79d02-104">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="79d02-105">Этот запрос необходим, чтобы участник отслеживания мог подписываться на объекты записей состояния действия.</span><span class="sxs-lookup"><span data-stu-id="79d02-105">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="79d02-106">Состояния, доступные для подписки, указаны в ActivtyStates.</span><span class="sxs-lookup"><span data-stu-id="79d02-106">The available states to subscribe to are specified in ActivityStates.</span></span>  
  
 <span data-ttu-id="79d02-107">Дополнительные сведения о запросах профиля отслеживания см. в разделе [профили отслеживания](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="79d02-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="79d02-108">\<system.serviceModel ></span><span class="sxs-lookup"><span data-stu-id="79d02-108">\<system.serviceModel></span></span>  
<span data-ttu-id="79d02-109">\<Отслеживание ></span><span class="sxs-lookup"><span data-stu-id="79d02-109">\<tracking></span></span>  
<span data-ttu-id="79d02-110">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="79d02-110">\<trackingProfile></span></span>  
<span data-ttu-id="79d02-111">\<рабочий процесс ></span><span class="sxs-lookup"><span data-stu-id="79d02-111">\<workflow></span></span>  
<span data-ttu-id="79d02-112">\<activityStateQueries ></span><span class="sxs-lookup"><span data-stu-id="79d02-112">\<activityStateQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79d02-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79d02-113">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <arguments>
          <argument name="String" />
        </arguments>
        <states>
          <state name="String" />
        </states>
        <variables>
         <variable name="String" />
        </variables>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="79d02-114">Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="79d02-114">Attributes and Elements</span></span>  
 <span data-ttu-id="79d02-115">В следующих разделах описаны атрибуты, дочерние и родительские элементы.</span><span class="sxs-lookup"><span data-stu-id="79d02-115">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="79d02-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="79d02-116">Attributes</span></span>  
 <span data-ttu-id="79d02-117">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="79d02-117">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="79d02-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="79d02-118">Child Elements</span></span>  
  
|<span data-ttu-id="79d02-119">Элемент</span><span class="sxs-lookup"><span data-stu-id="79d02-119">Element</span></span>|<span data-ttu-id="79d02-120">Описание</span><span class="sxs-lookup"><span data-stu-id="79d02-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="79d02-121">\<activityStateQuery ></span><span class="sxs-lookup"><span data-stu-id="79d02-121">\<activityStateQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|<span data-ttu-id="79d02-122">Запрос, который используется для отслеживания обработки ошибок, возникающих в рамках действия.</span><span class="sxs-lookup"><span data-stu-id="79d02-122">A query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="79d02-123">Это событие возникает каждый раз, когда FaultHandler обрабатывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="79d02-123">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="79d02-124">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="79d02-124">Parent Elements</span></span>  
  
|<span data-ttu-id="79d02-125">Элемент</span><span class="sxs-lookup"><span data-stu-id="79d02-125">Element</span></span>|<span data-ttu-id="79d02-126">Описание</span><span class="sxs-lookup"><span data-stu-id="79d02-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="79d02-127">\<рабочий процесс ></span><span class="sxs-lookup"><span data-stu-id="79d02-127">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="79d02-128">Элемент конфигурации, содержащий все запросы для определенного рабочего процесса, обозначенного **activityDefinitionId** свойство.</span><span class="sxs-lookup"><span data-stu-id="79d02-128">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="79d02-129">См. также</span><span class="sxs-lookup"><span data-stu-id="79d02-129">See Also</span></span>  
 <span data-ttu-id="79d02-130"><xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="79d02-130"><xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection?displayProperty=nameWithType></span></span>       
 <span data-ttu-id="79d02-131"><xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="79d02-131"><xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType></span></span>       
 [<span data-ttu-id="79d02-132">Отслеживание и трассировка рабочих процессов</span><span class="sxs-lookup"><span data-stu-id="79d02-132">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="79d02-133">Профили отслеживания</span><span class="sxs-lookup"><span data-stu-id="79d02-133">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
