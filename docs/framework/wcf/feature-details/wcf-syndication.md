---
title: "Синдикация WCF"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: syndication [WCF]
ms.assetid: ebf80384-0fc9-4919-a1e8-23ca2a13e300
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 14f2aa18b1fba92f5559b463d90dcfb5b34e2a3f
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2017
---
# <a name="wcf-syndication"></a><span data-ttu-id="101e8-102">Синдикация WCF</span><span class="sxs-lookup"><span data-stu-id="101e8-102">WCF Syndication</span></span>
[!INCLUDE[indigo1](../../../../includes/indigo1-md.md)]<span data-ttu-id="101e8-103"> обеспечивает поддержку для удобной работы с веб-каналами синдикации в форматах Atom, RSS и других нестандартных форматах, что позволяет обрабатывать и создавать каналы, а также предоставлять к ним доступ в конечной точке службы.</span><span class="sxs-lookup"><span data-stu-id="101e8-103"> provides support to easily work with syndication feeds in Atom, RSS or other custom formats, which allows you to read and create them as well as expose them on a service endpoint.</span></span> <span data-ttu-id="101e8-104">В подразделах этого раздела подробно описывается модель программирования синдикации.</span><span class="sxs-lookup"><span data-stu-id="101e8-104">The topics in this section describe this programming model for syndication in detail.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="101e8-105">Содержание</span><span class="sxs-lookup"><span data-stu-id="101e8-105">In This Section</span></span>  
 [<span data-ttu-id="101e8-106">Общие сведения о синдикации WCF</span><span class="sxs-lookup"><span data-stu-id="101e8-106">WCF Syndication Overview</span></span>](../../../../docs/framework/wcf/feature-details/wcf-syndication-overview.md)  
 <span data-ttu-id="101e8-107">Общие сведения о поддержке синдикации в [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].</span><span class="sxs-lookup"><span data-stu-id="101e8-107">Provides an overview of syndication support provided by [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].</span></span>  
  
 [<span data-ttu-id="101e8-108">Архитектура синдикации</span><span class="sxs-lookup"><span data-stu-id="101e8-108">Architecture of Syndication</span></span>](../../../../docs/framework/wcf/feature-details/architecture-of-syndication.md)  
 <span data-ttu-id="101e8-109">Описание классов объектной модели и расширяемости синдикации.</span><span class="sxs-lookup"><span data-stu-id="101e8-109">Describes the classes in the object model and the extensibility of syndication.</span></span>  
  
 [<span data-ttu-id="101e8-110">Сопоставление объектной модели синдикации WCF Atom и RSS</span><span class="sxs-lookup"><span data-stu-id="101e8-110">How the WCF Syndication Object Model Maps to Atom and RSS</span></span>](../../../../docs/framework/wcf/feature-details/how-the-wcf-syndication-object-model-maps-to-atom-and-rss.md)  
 <span data-ttu-id="101e8-111">Представление веб-каналов в объектной модели синдикации WCF и их преобразование в веб-каналы RSS и Atom.</span><span class="sxs-lookup"><span data-stu-id="101e8-111">Describes how feeds are represented within the WCF Syndication Object Model and how they are converted to RSS and Atom feeds.</span></span>  
  
 [<span data-ttu-id="101e8-112">Как: создание базового RSS-канала</span><span class="sxs-lookup"><span data-stu-id="101e8-112">How to: Create a Basic RSS Feed</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-basic-rss-feed.md)  
 <span data-ttu-id="101e8-113">Создание службы, которая предоставляет доступ к базовому RSS-каналу.</span><span class="sxs-lookup"><span data-stu-id="101e8-113">Shows how to create a service that makes a basic RSS feed available.</span></span>  
  
 [<span data-ttu-id="101e8-114">Как: создание базового канала Atom</span><span class="sxs-lookup"><span data-stu-id="101e8-114">How to: Create a Basic Atom Feed</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-basic-atom-feed.md)  
 <span data-ttu-id="101e8-115">Создание службы, которая предоставляет доступ к базовому ATOM-каналу.</span><span class="sxs-lookup"><span data-stu-id="101e8-115">Shows how to create a service that makes a basic ATOM feed available.</span></span>  
  
 [<span data-ttu-id="101e8-116">Как: предоставить доступ к каналу в форматах Atom и RSS</span><span class="sxs-lookup"><span data-stu-id="101e8-116">How to: Expose a Feed as Both Atom and RSS</span></span>](../../../../docs/framework/wcf/feature-details/how-to-expose-a-feed-as-both-atom-and-rss.md)  
 <span data-ttu-id="101e8-117">Создание службы, которая предоставляет доступ к одному и тому же каналу в форматах ATOM и RSS.</span><span class="sxs-lookup"><span data-stu-id="101e8-117">Shows how to create a service that makes the same feed available with ATOM and RSS.</span></span>  
  
 [<span data-ttu-id="101e8-118">Расширяемость синдикации</span><span class="sxs-lookup"><span data-stu-id="101e8-118">Syndication Extensibility</span></span>](../../../../docs/framework/wcf/feature-details/syndication-extensibility.md)  
 <span data-ttu-id="101e8-119">Описание методов добавления в канал синдикации пользовательских элементов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="101e8-119">Describes the methods of adding custom elements and attributes to a syndication feed.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="101e8-120">Ссылка</span><span class="sxs-lookup"><span data-stu-id="101e8-120">Reference</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="101e8-121">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="101e8-121">Related Sections</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="101e8-122">См. также</span><span class="sxs-lookup"><span data-stu-id="101e8-122">See Also</span></span>  
 [<span data-ttu-id="101e8-123">Модель программирования WCF Web HTTP</span><span class="sxs-lookup"><span data-stu-id="101e8-123">WCF Web HTTP Programming Model</span></span>](../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)  
 [<span data-ttu-id="101e8-124">Частичное доверие</span><span class="sxs-lookup"><span data-stu-id="101e8-124">Partial Trust</span></span>](../../../../docs/framework/wcf/feature-details/partial-trust.md)
