---
title: "VbStrConv.SimplifiedChinese и VbStrConv.TraditionalChinese не могут использоваться вместе"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords: vbrArgument_StrConvSCandTC
ms.assetid: d8e6a11b-f549-43b5-8337-0594340e1325
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 602f375eece2d79eb2f839b220b7774ebc3a847e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="simplifiedchinese-and-vbstrconvtraditionalchinese-cannot-be-combined"></a><span data-ttu-id="b65be-102">VbStrConv.SimplifiedChinese и VbStrConv.TraditionalChinese не могут использоваться вместе</span><span class="sxs-lookup"><span data-stu-id="b65be-102">SimplifiedChinese and VbStrConv.TraditionalChinese cannot be combined</span></span>
<span data-ttu-id="b65be-103">Приложение пытается объединить взаимоисключающие элементы `VbStrConv` и `SimplifiedChinese` , являющиеся членами перечисления `TraditionalChinese`.</span><span class="sxs-lookup"><span data-stu-id="b65be-103">Your application is attempting to combine the `VbStrConv` enumeration members `SimplifiedChinese` and `TraditionalChinese`, which are mutually exclusive.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b65be-104">Исправление ошибки</span><span class="sxs-lookup"><span data-stu-id="b65be-104">To correct this error</span></span>  
  
-   <span data-ttu-id="b65be-105">Удалите `VbStrConv.SimplifiedChinese` или `VbStrConv.TraditionalChinese`.</span><span class="sxs-lookup"><span data-stu-id="b65be-105">Remove either `VbStrConv.SimplifiedChinese` or `VbStrConv.TraditionalChinese`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b65be-106">См. также</span><span class="sxs-lookup"><span data-stu-id="b65be-106">See Also</span></span>  
 <xref:System.Globalization>  
 [<span data-ttu-id="b65be-107">НЕ В СБОРКЕ. Перечисление VbStrConv</span><span class="sxs-lookup"><span data-stu-id="b65be-107">NOTINBUILD VbStrConv Enumeration</span></span>](http://msdn.microsoft.com/en-us/59f83dd9-6361-47df-a836-02ba9d4cb936)  
 [<span data-ttu-id="b65be-108">Знакомство с международными приложениями на платформе .NET Framework</span><span class="sxs-lookup"><span data-stu-id="b65be-108">Introduction to International Applications Based on the .NET Framework</span></span>](/visualstudio/ide/introduction-to-international-applications-based-on-the-dotnet-framework)
