---
title: 1148 - FlowchartSwitchCaseNotFound
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 9ee7fcee-e040-4306-968e-ed840a1cb00c
caps.latest.revision: "2"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 4fa173290b528be690b418622baaa2a12e4930cb
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2017
---
# <a name="1148---flowchartswitchcasenotfound"></a>1148 - FlowchartSwitchCaseNotFound
## <a name="properties"></a>Свойства  
  
|||  
|-|-|  
|Идентификатор|1148|  
|Ключевые слова|WFActivities|  
|Уровень|Сведения|  
|Канал|Microsoft-Windows-Application Server-Applications/Debug|  
  
## <a name="description"></a>Описание  
 Указывает, что в параметре блок-схемы не найден ни соответствующий вариант, ни вариант по умолчанию. Выполнение блок-схемы будет завершено.  
  
## <a name="message"></a>Сообщение  
 Блок-схема «%1»/FlowSwitch - не удалось найти ни действие Case, ни действие Default Case, соответствующее результату выражения Expression. Выполнение блок-схемы будет завершено.  
  
## <a name="details"></a>Подробные сведения  
  
|Имя элемента данных|Тип элемента данных|Описание|  
|--------------------|--------------------|-----------------|  
|Блок-схема|xs:string|Отображаемое имя блок-схемы.|  
|AppDomain|xs:string|Строка, возвращаемая AppDomain.CurrentDomain.FriendlyName.|
