---
title: "Изменения системы безопасности в .NET Framework"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Allow Partially Trusted Callers attribute
- .NET Framework 4, security changes
- .NET Framework security
- security-transparent code
- security-critical code
- code access security, changes
ms.assetid: 5e87881c-9c13-4b52-8ad1-e34bb46e8aaa
caps.latest.revision: "52"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c1a96e30527aa3da4274ed55059b24aa5a7eeb47
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="security-changes-in-the-net-framework"></a><span data-ttu-id="fc36e-102">Изменения системы безопасности в .NET Framework</span><span class="sxs-lookup"><span data-stu-id="fc36e-102">Security Changes in the .NET Framework</span></span>
<span data-ttu-id="fc36e-103">Самое важное изменение в отношении безопасности в [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] — это строгое именование.</span><span class="sxs-lookup"><span data-stu-id="fc36e-103">The most important change to security in the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] is in strong naming.</span></span> <span data-ttu-id="fc36e-104">Описание этих изменений см. в разделе [Enhanced Strong Naming](../../../docs/framework/app-domains/enhanced-strong-naming.md) .</span><span class="sxs-lookup"><span data-stu-id="fc36e-104">See [Enhanced Strong Naming](../../../docs/framework/app-domains/enhanced-strong-naming.md) for a description of those changes.</span></span>  
  
 <span data-ttu-id="fc36e-105">В NET Framework предусмотрена двухуровневая модель безопасности для управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="fc36e-105">The .NET Framework provides a two-tier security model for managed applications.</span></span> <span data-ttu-id="fc36e-106">Приложения[!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] работают в контейнере безопасности Windows, ограничивающем доступ к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="fc36e-106">[!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] apps run in a Windows security container that limits access to resources.</span></span> <span data-ttu-id="fc36e-107">Внутри этого контейнера управляемые приложения работают с полным доверием.</span><span class="sxs-lookup"><span data-stu-id="fc36e-107">Within that container, managed applications run fully trusted.</span></span> <span data-ttu-id="fc36e-108">С точки зрения управления доступом для кода разработчик ничего не может сделать для повышения прав доступа.</span><span class="sxs-lookup"><span data-stu-id="fc36e-108">From a code access security (CAS) perspective, there is nothing a developer can do to elevate privileges.</span></span> <span data-ttu-id="fc36e-109">Сведения о привилегиях, предоставляемых операционной системой Windows, см. в разделе [Объявления характеристик приложения (приложения Магазина Windows)](http://go.microsoft.com/fwlink/?LinkId=230436) в Центре разработки для Windows.</span><span class="sxs-lookup"><span data-stu-id="fc36e-109">For information about the privileges granted by Windows, see [App capability declarations (Windows Store apps)](http://go.microsoft.com/fwlink/?LinkId=230436) in the Windows Dev Center.</span></span> <span data-ttu-id="fc36e-110">Сведения о создании приложения [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] см. в разделе [Создание первого приложения для Магазина Windows на C# или Visual Basic](http://go.microsoft.com/fwlink/?LinkId=230461).</span><span class="sxs-lookup"><span data-stu-id="fc36e-110">For information about creating a [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] app, see [Create your first Windows Store app using C# or Visual Basic](http://go.microsoft.com/fwlink/?LinkId=230461).</span></span>
