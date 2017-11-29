---
title: 1003 - WorkflowInstanceCanceled
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 64754dc2-c160-4bf3-869a-13d56694e2dc
caps.latest.revision: "4"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 7b287c99453724f855a51e9a1b8068337dd5e373
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="1003---workflowinstancecanceled"></a><span data-ttu-id="5b5f9-102">1003 - WorkflowInstanceCanceled</span><span class="sxs-lookup"><span data-stu-id="5b5f9-102">1003 - WorkflowInstanceCanceled</span></span>
## <a name="properties"></a><span data-ttu-id="5b5f9-103">Свойства</span><span class="sxs-lookup"><span data-stu-id="5b5f9-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="5b5f9-104">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="5b5f9-104">ID</span></span>|<span data-ttu-id="5b5f9-105">1003</span><span class="sxs-lookup"><span data-stu-id="5b5f9-105">1003</span></span>|  
|<span data-ttu-id="5b5f9-106">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5b5f9-106">Keywords</span></span>|<span data-ttu-id="5b5f9-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="5b5f9-107">WFRuntime</span></span>|  
|<span data-ttu-id="5b5f9-108">Уровень</span><span class="sxs-lookup"><span data-stu-id="5b5f9-108">Level</span></span>|<span data-ttu-id="5b5f9-109">Сведения</span><span class="sxs-lookup"><span data-stu-id="5b5f9-109">Information</span></span>|  
|<span data-ttu-id="5b5f9-110">Канал</span><span class="sxs-lookup"><span data-stu-id="5b5f9-110">Channel</span></span>|<span data-ttu-id="5b5f9-111">Microsoft-Windows-Application Server-Applications/Debug</span><span class="sxs-lookup"><span data-stu-id="5b5f9-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="5b5f9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5b5f9-112">Description</span></span>  
 <span data-ttu-id="5b5f9-113">Указывает, что экземпляр рабочего процесса завершено в состоянии Canceled.</span><span class="sxs-lookup"><span data-stu-id="5b5f9-113">Indicates a workflow instance has completed in the Canceled state.</span></span>  
  
## <a name="message"></a><span data-ttu-id="5b5f9-114">Сообщение</span><span class="sxs-lookup"><span data-stu-id="5b5f9-114">Message</span></span>  
 <span data-ttu-id="5b5f9-115">Элемент WorkflowInstance с идентификатором «%1» завершил работу в состоянии Canceled.</span><span class="sxs-lookup"><span data-stu-id="5b5f9-115">WorkflowInstance Id: '%1' has completed in the Canceled state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="5b5f9-116">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="5b5f9-116">Details</span></span>  
  
|<span data-ttu-id="5b5f9-117">Имя элемента данных</span><span class="sxs-lookup"><span data-stu-id="5b5f9-117">Data Item Name</span></span>|<span data-ttu-id="5b5f9-118">Тип элемента данных</span><span class="sxs-lookup"><span data-stu-id="5b5f9-118">Data Item Type</span></span>|<span data-ttu-id="5b5f9-119">Описание</span><span class="sxs-lookup"><span data-stu-id="5b5f9-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="5b5f9-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="5b5f9-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="5b5f9-121">Идентификатор экземпляра для рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="5b5f9-121">The instance id for the workflow</span></span>|  
|<span data-ttu-id="5b5f9-122">Домен приложения</span><span class="sxs-lookup"><span data-stu-id="5b5f9-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="5b5f9-123">Строка, возвращаемая AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="5b5f9-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
