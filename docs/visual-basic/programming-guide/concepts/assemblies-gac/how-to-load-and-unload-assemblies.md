---
title: Практическое руководство. Загрузка и выгрузка сборок (Visual Basic)
ms.date: 07/20/2015
ms.assetid: bbc84236-04b6-4c1b-9672-52773f65a5dc
ms.openlocfilehash: 07c8370d7aeb5171f991ddf24bf473f787408f2d
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2019
ms.locfileid: "58838772"
---
# <a name="how-to-load-and-unload-assemblies-visual-basic"></a>Практическое руководство. Загрузка и выгрузка сборок (Visual Basic)
Сборки, на которые ссылается программа, загружаются автоматически во время построения, но в текущий домен приложения можно также загрузить конкретные сборки во время выполнения. Дополнительные сведения см. в разделе [Как Загрузка сборок в домен приложения](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md).  
  
 Отдельную сборку нельзя выгрузить, не выгрузив все домены приложений, в которых она содержится. Даже если сборка не входит в область, фактический файл сборки остается загруженным до тех пор, пока не будут выгружены домены приложений с этой сборкой.  
  
 Если необходимо выгрузить только часть сборок, создайте новый домен приложения, выполните код внутри этого домена, а затем выгрузите этот домен приложения. Дополнительные сведения см. в разделе [Как Выгрузка домена приложения](../../../../framework/app-domains/how-to-unload-an-application-domain.md).  
  
### <a name="to-load-an-assembly-into-an-application-domain"></a>Загрузка сборки в домен приложения  
  
1.  Используйте один из нескольких методов загрузки, содержащихся в классах <xref:System.AppDomain> и <xref:System.Reflection>. Дополнительные сведения см. в разделе [Как Загрузка сборок в домен приложения](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md).  
  
### <a name="to-unload-an-application-domain"></a>Выгрузка домена приложения  
  
1.  Отдельную сборку нельзя выгрузить, не выгрузив все домены приложений, в которых она содержится. Используйте метод `Unload` из <xref:System.AppDomain> для выгрузки доменов приложений. Дополнительные сведения см. в разделе [Как Выгрузка домена приложения](../../../../framework/app-domains/how-to-unload-an-application-domain.md).  
  
## <a name="see-also"></a>См. также

- [Основные понятия программирования](../../../../visual-basic/programming-guide/concepts/index.md)
- [Сборки в .NET](../../../../standard/assembly/index.md)
- [Практическое руководство. Загрузка сборок в домен приложения](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md)
