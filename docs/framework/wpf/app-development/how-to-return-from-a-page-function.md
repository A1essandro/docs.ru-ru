---
title: "Практическое руководство. Возврат из функции страницы | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-wpf"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "функции, возврат из"
  - "страничные функции, возврат из"
  - "возврат из страничных функций"
ms.assetid: 87804905-7e8f-417b-b0e3-5622da686396
caps.latest.revision: 8
author: "dotnet-bot"
ms.author: "dotnetcontent"
manager: "wpickett"
caps.handback.revision: 5
---
# Практическое руководство. Возврат из функции страницы
В этом примере показано, как возвращать результат из функции страницы.  
  
## Пример  
 Чтобы вернуть результат из функции страницы, необходимо вызвать <xref:System.Windows.Navigation.PageFunction%601.OnReturn%2A> и передать экземпляр <xref:System.Windows.Navigation.ReturnEventArgs%601>.  
  
 [!code-xml[HOWTOPageFunctionSnippets#PageFunctionReturnAResultXAML1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/GetStringPageFunction.xaml#pagefunctionreturnaresultxaml1)]  
[!code-xml[HOWTOPageFunctionSnippets#PageFunctionReturnAResultXAML2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/GetStringPageFunction.xaml#pagefunctionreturnaresultxaml2)]  
  
 [!code-csharp[HOWTOPageFunctionSnippets#PageFunctionReturnAResultCODEBEHIND](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/GetStringPageFunction.xaml.cs#pagefunctionreturnaresultcodebehind)]
 [!code-vb[HOWTOPageFunctionSnippets#PageFunctionReturnAResultCODEBEHIND](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/VisualBasic/GetStringPageFunction.xaml.vb#pagefunctionreturnaresultcodebehind)]  
  
## См. также  
 <xref:System.Windows.Navigation.PageFunction%601>