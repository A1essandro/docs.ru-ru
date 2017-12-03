---
title: "Кэширование канала и операция Send"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e69a2502-25cb-43bf-b8d2-95fbdecb41cb
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 7f8a11397fe161edad6f726c1d6df9ed09dad54a
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2017
---
# <a name="channel-caching-with-send"></a><span data-ttu-id="695dc-102">Кэширование канала и операция Send</span><span class="sxs-lookup"><span data-stu-id="695dc-102">Channel Caching with Send</span></span>
<span data-ttu-id="695dc-103">Объект <xref:System.ServiceModel.Activities.SendMessageChannelCache> позволяет пользователям использовать различные уровни кэширования канала для действий <xref:System.ServiceModel.Activities.Send> и <xref:System.ServiceModel.Activities.SendParametersContent>.</span><span class="sxs-lookup"><span data-stu-id="695dc-103">The <xref:System.ServiceModel.Activities.SendMessageChannelCache> enables users to have different levels of channel caching with <xref:System.ServiceModel.Activities.Send> and <xref:System.ServiceModel.Activities.SendParametersContent> activities.</span></span> <span data-ttu-id="695dc-104">Кэширование на уровне экземпляра включено по умолчанию. Данный образец иллюстрирует перечисленные далее возможности.</span><span class="sxs-lookup"><span data-stu-id="695dc-104">Instance-level caching is enabled by default and this sample demonstrates the following features:</span></span>  
  
1.  <span data-ttu-id="695dc-105">Совместное использование <xref:System.ServiceModel.Activities.SendMessageChannelCache> в домене приложений.</span><span class="sxs-lookup"><span data-stu-id="695dc-105">Share a <xref:System.ServiceModel.Activities.SendMessageChannelCache> across an application domain.</span></span>  
  
2.  <span data-ttu-id="695dc-106">Отключение кэширования канала.</span><span class="sxs-lookup"><span data-stu-id="695dc-106">Disable channel caching.</span></span>  
  
3.  <span data-ttu-id="695dc-107">Совместное использование <xref:System.ServiceModel.Activities.SendMessageChannelCache> экземплярами рабочих процессов на узле <xref:System.ServiceModel.Activities.WorkflowServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="695dc-107">Share a <xref:System.ServiceModel.Activities.SendMessageChannelCache> among workflow instances in a <xref:System.ServiceModel.Activities.WorkflowServiceHost>.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="695dc-108">Демонстрации</span><span class="sxs-lookup"><span data-stu-id="695dc-108">Demonstrates</span></span>  
 <span data-ttu-id="695dc-109">Расширение <xref:System.ServiceModel.Activities.SendMessageChannelCache>, действия <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.ReceiveContent> и <xref:System.ServiceModel.Activities.SendReply>.</span><span class="sxs-lookup"><span data-stu-id="695dc-109"><xref:System.ServiceModel.Activities.SendMessageChannelCache> extension, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.ReceiveContent> and <xref:System.ServiceModel.Activities.SendReply> activities.</span></span>  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="695dc-110">Настройка, сборка и выполнение образца</span><span class="sxs-lookup"><span data-stu-id="695dc-110">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="695dc-111">Загрузите решение проекта в среду [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] и постройте проект.</span><span class="sxs-lookup"><span data-stu-id="695dc-111">Load the project solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] and build the project.</span></span>  
  
2.  <span data-ttu-id="695dc-112">Запустите приложение EchoWorkflowService, созданное в папке «\EchoWorkflowService\bin\debug».</span><span class="sxs-lookup"><span data-stu-id="695dc-112">Run the EchoWorkflowService application generated in \EchoWorkflowService\bin\debug.</span></span>  
  
3.  <span data-ttu-id="695dc-113">Запустите приложение EchoWorkflowClient, созданное в папке «.\EchoWorkflowClient\bin\debug».</span><span class="sxs-lookup"><span data-stu-id="695dc-113">Run the EchoWorkflowClient application generated in .\EchoWorkflowClient\bin\debug.</span></span>  
  
4.  <span data-ttu-id="695dc-114">Клиент вызывает операцию Echo применительно к службе и печатает результаты.</span><span class="sxs-lookup"><span data-stu-id="695dc-114">The client calls the Echo operation on the service and prints the results.</span></span> <span data-ttu-id="695dc-115">После того как результаты распечатаны, нажмите клавишу ВВОД, чтобы закрыть клиент и службу.</span><span class="sxs-lookup"><span data-stu-id="695dc-115">When the results have been printed, press ENTER to exit the client and the service.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="695dc-116">Образцы уже могут быть установлены на компьютере.</span><span class="sxs-lookup"><span data-stu-id="695dc-116">The samples may already be installed on your machine.</span></span> <span data-ttu-id="695dc-117">Перед продолжением проверьте следующий каталог (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="695dc-117">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="695dc-118">Если этот каталог не существует, перейдите на страницу [Примеры Windows Communication Foundation (WCF) и Windows Workflow Foundation (WF) для .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) , чтобы скачать все примеры [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] и [!INCLUDE[wf1](../../../../includes/wf1-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="695dc-118">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="695dc-119">Этот образец расположен в следующем каталоге.</span><span class="sxs-lookup"><span data-stu-id="695dc-119">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\ChannelCache`
