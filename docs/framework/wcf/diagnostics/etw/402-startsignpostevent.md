---
title: 402 - StartSignpostEvent
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 5e5be126-765d-4ac9-88e7-008e9ef4f0e5
caps.latest.revision: "3"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: c0cd786f78336be50ad2ef5447f74b92b2abbdc7
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="402---startsignpostevent"></a><span data-ttu-id="2a995-102">402 - StartSignpostEvent</span><span class="sxs-lookup"><span data-stu-id="2a995-102">402 - StartSignpostEvent</span></span>
## <a name="properties"></a><span data-ttu-id="2a995-103">Свойства</span><span class="sxs-lookup"><span data-stu-id="2a995-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="2a995-104">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="2a995-104">ID</span></span>|<span data-ttu-id="2a995-105">402</span><span class="sxs-lookup"><span data-stu-id="2a995-105">402</span></span>|  
|<span data-ttu-id="2a995-106">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2a995-106">Keywords</span></span>|<span data-ttu-id="2a995-107">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="2a995-107">Troubleshooting</span></span>|  
|<span data-ttu-id="2a995-108">Уровень</span><span class="sxs-lookup"><span data-stu-id="2a995-108">Level</span></span>|<span data-ttu-id="2a995-109">Сведения</span><span class="sxs-lookup"><span data-stu-id="2a995-109">Information</span></span>|  
|<span data-ttu-id="2a995-110">Канал</span><span class="sxs-lookup"><span data-stu-id="2a995-110">Channel</span></span>|<span data-ttu-id="2a995-111">Microsoft-Windows-Application Server-Applications/Analytic</span><span class="sxs-lookup"><span data-stu-id="2a995-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="2a995-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2a995-112">Description</span></span>  
 <span data-ttu-id="2a995-113">Это событие отмечает начало сквозного действия.</span><span class="sxs-lookup"><span data-stu-id="2a995-113">This event marks the beginning of an end-to-end activity.</span></span> <span data-ttu-id="2a995-114">В ней содержится имя действия.</span><span class="sxs-lookup"><span data-stu-id="2a995-114">It contains the name of the activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="2a995-115">Сообщение</span><span class="sxs-lookup"><span data-stu-id="2a995-115">Message</span></span>  
 <span data-ttu-id="2a995-116">Граница действия.</span><span class="sxs-lookup"><span data-stu-id="2a995-116">Activity boundary.</span></span>  
  
## <a name="details"></a><span data-ttu-id="2a995-117">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="2a995-117">Details</span></span>  
  
|<span data-ttu-id="2a995-118">Имя элемента данных</span><span class="sxs-lookup"><span data-stu-id="2a995-118">Data Item Name</span></span>|<span data-ttu-id="2a995-119">Тип элемента данных</span><span class="sxs-lookup"><span data-stu-id="2a995-119">Data Item Type</span></span>|<span data-ttu-id="2a995-120">Описание</span><span class="sxs-lookup"><span data-stu-id="2a995-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="2a995-121">Расширенные данные</span><span class="sxs-lookup"><span data-stu-id="2a995-121">Extended Data</span></span>|`xs:string`|<span data-ttu-id="2a995-122">Имя действия.</span><span class="sxs-lookup"><span data-stu-id="2a995-122">The name of the activity.</span></span>|  
|<span data-ttu-id="2a995-123">Домен приложения</span><span class="sxs-lookup"><span data-stu-id="2a995-123">AppDomain</span></span>|`xs:string`|<span data-ttu-id="2a995-124">Строка, возвращаемая AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="2a995-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
