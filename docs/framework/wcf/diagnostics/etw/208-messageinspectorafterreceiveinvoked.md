---
title: 208 - MessageInspectorAfterReceiveInvoked
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: dfb5f7b0-4346-4949-8104-351726b1f502
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 670650c612ac01ab9c82028388a4524d2f08fd79
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2017
---
# <a name="208---messageinspectorafterreceiveinvoked"></a><span data-ttu-id="49b21-102">208 - MessageInspectorAfterReceiveInvoked</span><span class="sxs-lookup"><span data-stu-id="49b21-102">208 - MessageInspectorAfterReceiveInvoked</span></span>
## <a name="properties"></a><span data-ttu-id="49b21-103">Свойства</span><span class="sxs-lookup"><span data-stu-id="49b21-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="49b21-104">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="49b21-104">ID</span></span>|<span data-ttu-id="49b21-105">208</span><span class="sxs-lookup"><span data-stu-id="49b21-105">208</span></span>|  
|<span data-ttu-id="49b21-106">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="49b21-106">Keywords</span></span>|<span data-ttu-id="49b21-107">Troubleshooting, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="49b21-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="49b21-108">Уровень</span><span class="sxs-lookup"><span data-stu-id="49b21-108">Level</span></span>|<span data-ttu-id="49b21-109">Сведения</span><span class="sxs-lookup"><span data-stu-id="49b21-109">Information</span></span>|  
|<span data-ttu-id="49b21-110">Канал</span><span class="sxs-lookup"><span data-stu-id="49b21-110">Channel</span></span>|<span data-ttu-id="49b21-111">Microsoft-Windows-Application Server-Applications/Analytic</span><span class="sxs-lookup"><span data-stu-id="49b21-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="49b21-112">Описание</span><span class="sxs-lookup"><span data-stu-id="49b21-112">Description</span></span>  
 <span data-ttu-id="49b21-113">Это событие создается после того, как модель службы вызвала метод `AfterReceive` для инспектора сообщений.</span><span class="sxs-lookup"><span data-stu-id="49b21-113">This event is emitted after the Service Model has invoked the `AfterReceive` method on a message inspector.</span></span>  
  
## <a name="message"></a><span data-ttu-id="49b21-114">Сообщение</span><span class="sxs-lookup"><span data-stu-id="49b21-114">Message</span></span>  
 <span data-ttu-id="49b21-115">Диспетчер вызвал AfterReceiveReply относительно MessageInspector типа «%1».</span><span class="sxs-lookup"><span data-stu-id="49b21-115">The Dispatcher invoked 'AfterReceiveReply' on a MessageInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="49b21-116">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="49b21-116">Details</span></span>  
  
|<span data-ttu-id="49b21-117">Имя элемента данных</span><span class="sxs-lookup"><span data-stu-id="49b21-117">Data Item Name</span></span>|<span data-ttu-id="49b21-118">Тип элемента данных</span><span class="sxs-lookup"><span data-stu-id="49b21-118">Data Item Type</span></span>|<span data-ttu-id="49b21-119">Описание</span><span class="sxs-lookup"><span data-stu-id="49b21-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="49b21-120">TypeName</span><span class="sxs-lookup"><span data-stu-id="49b21-120">TypeName</span></span>|`xs:string`|<span data-ttu-id="49b21-121">Имя CLR FullName типа вызванного инспектора `MessageInspector`.</span><span class="sxs-lookup"><span data-stu-id="49b21-121">The CLR FullName of the type of the invoked `MessageInspector`.</span></span>|  
|<span data-ttu-id="49b21-122">HostReference</span><span class="sxs-lookup"><span data-stu-id="49b21-122">HostReference</span></span>|`xs:string`|<span data-ttu-id="49b21-123">Для служб, размещенных на веб-узле, это поле является уникальным идентификатором службы в веб-иерархии.</span><span class="sxs-lookup"><span data-stu-id="49b21-123">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="49b21-124">Ее формат определяется как "веб-сайт имя виртуальный путь приложения &#124; Виртуальный путь службы &#124; ServiceName ".</span><span class="sxs-lookup"><span data-stu-id="49b21-124">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="49b21-125">Пример: "по умолчанию веб-сайта или CalculatorApplication &#124;/CalculatorService.svc &#124; CalculatorService ".</span><span class="sxs-lookup"><span data-stu-id="49b21-125">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="49b21-126">AppDomain</span><span class="sxs-lookup"><span data-stu-id="49b21-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="49b21-127">Строка, возвращаемая AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="49b21-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
