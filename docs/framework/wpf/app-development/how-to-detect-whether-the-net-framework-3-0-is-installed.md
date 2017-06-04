---
title: "Практическое руководство. Проверка наличия установленной платформы .NET Framework 3.0 | Microsoft Docs"
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
  - "обнаружение присутствия /WPF"
  - "присутствие WPT, обнаружение"
  - "строка пользовательского агента WinFX Runtime"
ms.assetid: 7f71d652-1749-4379-945a-aa2e3994cb43
caps.latest.revision: 12
author: "dotnet-bot"
ms.author: "dotnetcontent"
manager: "wpickett"
caps.handback.revision: 12
---
# Практическое руководство. Проверка наличия установленной платформы .NET Framework 3.0
Прежде чем администраторы смогут развернуть приложения [!INCLUDE[TLA#tla_avalonwinfx](../../../../includes/tlasharptla-avalonwinfx-md.md)] в системе, необходимо убедиться в наличии исполняющей среды [!INCLUDE[TLA2#tla_avalonwinfx](../../../../includes/tla2sharptla-avalonwinfx-md.md)].  В этом разделе содержится скрипт, написанный на языке HTML\/JavaScript, который администраторы могут использовать для определения наличия [!INCLUDE[TLA2#tla_avalonwinfx](../../../../includes/tla2sharptla-avalonwinfx-md.md)] в системе.  
  
> [!NOTE]
>  Более подробные сведения по установке, развертыванию и обнаружению [!INCLUDE[TLA#tla_winfx](../../../../includes/tlasharptla-winfx-md.md)] см. раздел [Deploying Microsoft .NET Framework Version 3.0](http://go.microsoft.com/fwlink/?LinkId=96739)..  
  
<a name="content_expiration"></a>   
## Обнаружение строки агента пользователя «.NET CLR»  
 После установки [!INCLUDE[TLA2#tla_avalonwinfx](../../../../includes/tla2sharptla-avalonwinfx-md.md)] MSI добавляет «.NET CLR» и номер версии к строке UserAgent.  В следующем примере показан скрипт, встроенный в простую страницу HTML.  Скрипт просматривает строку UserAgent для определения, установлена ли платформа [!INCLUDE[TLA2#tla_avalonwinfx](../../../../includes/tla2sharptla-avalonwinfx-md.md)], и выводит статусное сообщение о результатах поиска.  
  
```  
<HTML>  
  <HEAD>  
    <TITLE>Test for the .NET Framework 3.0</TITLE>  
    <META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=utf-8" />  
    <SCRIPT LANGUAGE="JavaScript">  
    <!--  
    var dotNETRuntimeVersion = "3.0.04425.00";  
  
    function window::onload()  
    {  
      if (HasRuntimeVersion(dotNETRuntimeVersion))  
      {  
        result.innerText =   
          "This machine has the correct version of the .NET Framework 3.0: "   
          + dotNETRuntimeVersion  
      }   
      else  
      {  
        result.innerText =   
          "This machine does not have the correct version of the .NET Framework 3.0."  
      }  
      result.innerText += "\n\nThis machine's userAgent string is: " +   
        navigator.userAgent + ".";  
    }  
  
    //  
    // Retrieve the version from the user agent string and   
    // compare with the specified version.  
    //  
    function HasRuntimeVersion(versionToCheck)  
    {  
      var userAgentString =   
        navigator.userAgent.match(/.NET CLR [0-9.]+/g);  
  
      if (userAgentString != null)  
      {  
        var i;  
  
        for (i = 0; i < userAgentString.length; ++i)  
        {  
          if (CompareVersions(GetVersion(versionToCheck),   
            GetVersion(userAgentString[i])) <= 0)  
            return true;  
        }  
      }  
  
      return false;  
    }  
  
    //  
    // Extract the numeric part of the version string.  
    //  
    function GetVersion(versionString)  
    {  
      var numericString =   
        versionString.match(/([0-9]+)\.([0-9]+)\.([0-9]+)/i);  
      return numericString.slice(1);  
    }  
  
    //  
    // Compare the 2 version strings by converting them to numeric format.  
    //  
    function CompareVersions(version1, version2)  
    {  
      for (i = 0; i < version1.length; ++i)  
      {  
        var number1 = new Number(version1[i]);  
        var number2 = new Number(version2[i]);  
  
        if (number1 < number2)  
          return -1;  
  
        if (number1 > number2)  
          return 1;  
      }  
  
      return 0;  
    }  
  
    -->  
    </SCRIPT>  
  </HEAD>  
  
  <BODY>  
    <div id="result" />  
  </BODY>  
</HTML>  
  
```  
  
 Если поиск версии ".NET CLR" завершился успешно, появляется сообщение о состоянии следующего типа:  
  
 `This machine has the correct version of the .NET Framework 3.0: 3.0.04425.00`  
  
 `This machine's userAgent string is: Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 5.1; .NET CLR 1.1.4322; InfoPath.1; .NET CLR 2.0.50727; .NET CLR 3.0.04425.00).`  
  
 В противном случае появляется сообщение о состоянии следующего типа:  
  
 `This machine does not have correct version of the .NET Framework 3.0.`  
  
 `This machine's userAgent string is: Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 5.1; .NET CLR 1.1.4322; InfoPath.1; .NET CLR 2.0.50727).`