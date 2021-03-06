---
title: Обработка ошибок веб-протокола HTTP WCF
ms.date: 03/30/2017
ms.assetid: 02891563-0fce-4c32-84dc-d794b1a5c040
ms.openlocfilehash: c331d70a69740a9830cafb5cafdfcf1de14b541b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499253"
---
# <a name="wcf-web-http-error-handling"></a>Обработка ошибок веб-протокола HTTP WCF
Обработка ошибок Web HTTP Windows Communication Foundation (WCF) позволяет возвращать ошибки из службы WCF Web HTTP, которые указывают код состояния HTTP и возвращают сведения об ошибке, используя формат операции (например, XML или JSON).  
  
## <a name="wcf-web-http-error-handling"></a>Обработка ошибок веб-протокола HTTP WCF  
 Класс <xref:System.ServiceModel.Web.WebFaultException> содержит конструктор, позволяющий указать код состояния HTTP. Затем этот код состояния возвращается клиенту. Общая версия класса <xref:System.ServiceModel.Web.WebFaultException>, <xref:System.ServiceModel.Web.WebFaultException%601> позволяет возвращать определенный пользователем тип, содержащий сведения о возникшей ошибке. Этот пользовательский объект сериализуется с помощью формата, указанного операцией и возвращенного клиенту. Следующий пример показывает, как вернуть код состояния HTTP.  
  
```  
Public string Operation1()  
{   // Operation logic  
   // ...  
   Throw new WebFaultException(HttpStatusCode.Forbidden);  
}  
```  
  
 В следующем примере показано, как вернуть код состояния HTTP и дополнительные сведения в типе, определяемом пользователем. `MyErrorDetail` - определяемый пользователем тип, который содержит дополнительные сведения о возникшей ошибке.  
  
```  
Public string Operation2()  
   // Operation logic  
   // ...   MyErrorDetail detail = new MyErrorDetail  
   {  
      Message = "Error Message",  
      ErrorCode = 123,  
   }  
   throw new WebFaultException<MyErrorDetail>(detail, HttpStatusCode.Forbidden);  
}  
```  
  
 В приведенном выше коде возвращается ответ HTTP с кодом состояния «доступ запрещен» и экземпляром объекта `MyErrorDetails` в теле ответа. Формат объекта `MyErrorDetails` определяется следующими элементами.  
  
-   Значение параметра `ResponseFormat` атрибута <xref:System.ServiceModel.Web.WebGetAttribute> или <xref:System.ServiceModel.Web.WebInvokeAttribute>, указанного в операции службы.  
  
-   Значение <xref:System.ServiceModel.Description.WebHttpBehavior.AutomaticFormatSelectionEnabled%2A>.  
  
-   Значение свойства <xref:System.ServiceModel.Web.OutgoingWebResponseContext.Format%2A> при обращении к <xref:System.ServiceModel.Web.OutgoingWebResponseContext>.  
  
 Дополнительные сведения о том, как эти значения влияют на форматирование операции см. в разделе [WCF Web HTTP форматирование](../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md).  
  
 Исключение <xref:System.ServiceModel.Web.WebFaultException> является <xref:System.ServiceModel.FaultException> и, следовательно, может быть использовано в качестве модели программирования ошибок для служб, предоставляющих конечные точки SOAP, а также сетевые конечные точки HTTP.  
  
## <a name="see-also"></a>См. также
- [Модель веб-программирования HTTP WCF](../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)
- [Форматирование веб-объектов HTTP WCF](../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md)
- [Определение и указание сбоев](../../../../docs/framework/wcf/defining-and-specifying-faults.md)
- [Обработка исключений и сбоев](../../../../docs/framework/wcf/extending/handling-exceptions-and-faults.md)
- [Сбои при отправке и получении](../../../../docs/framework/wcf/sending-and-receiving-faults.md)
