---
title: Практическое руководство. Запрос данных с помощью класса WebRequest
ms.date: 03/21/2019
dev_langs:
- csharp
- vb
helpviewer_keywords:
- downloading Internet resources, steps
- requesting data from Internet, steps
- WebRequest class, receiving data
- receiving data, using WebRequest class
- Internet, requesting data
ms.assetid: 368b8d0f-dc5e-4469-a8b8-b2adbf5dd800
ms.openlocfilehash: 1b71327d007e66cc217f6d69e11122c481e5118f
ms.sourcegitcommit: d938c39afb9216db377d0f0ecdaa53936a851059
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58634041"
---
# <a name="how-to-request-data-by-using-the-webrequest-class"></a>Практическое руководство. Запрос данных с помощью класса WebRequest
Следующая процедура описывает шаги для запроса ресурсов, например веб-страницы или файла, с сервера. Ресурс должен быть определен универсальным кодом ресурса (URI).  
  
## <a name="to-request-data-from-a-host-server"></a>Запрос данных с сервера узла  
  
1.  Создайте экземпляр <xref:System.Net.WebRequest> путем вызова <xref:System.Net.WebRequest.Create%2A?displayProperty=nameWithType> с URI ресурса. Например: 
  
    ```csharp  
    WebRequest request = WebRequest.Create("http://www.contoso.com/default.html");  
    ```  
  
    ```vb  
    Dim request as WebRequest = WebRequest.Create("http://www.contoso.com/default.html")  
    ```  
  
    > [!NOTE]
    > Платформа .NET Framework предоставляет связанные с определенным протоколом классы, производные от классов <xref:System.Net.WebRequest> и <xref:System.Net.WebResponse>, для URI, которые начинаются с *http:*, *https:*, *ftp:* и *file:*.
    Если нужно задать или считать связанные с определенным протоколом свойства, следует привести объект <xref:System.Net.WebRequest> или <xref:System.Net.WebResponse> к типу объекта, связанному с определенным протоколом. Дополнительные сведения см. в разделе [Программирование подключаемых протоколов](programming-pluggable-protocols.md). 
  
2.  Укажите все необходимые значения свойств в объекте `WebRequest`. Например, чтобы включить проверку подлинности, установите для свойства <xref:System.Net.WebRequest.Credentials%2A?displayProperty=nameWithType> значение экземпляра класса <xref:System.Net.NetworkCredential>:  
  
    ```csharp  
    request.Credentials = CredentialCache.DefaultCredentials;  
    ```  
  
    ```vb  
    request.Credentials = CredentialCache.DefaultCredentials  
    ```  
  
3.  Отправьте запрос на сервер, вызвав метод <xref:System.Net.WebRequest.GetResponse%2A?displayProperty=nameWithType>. Этот метод возвращает объект, содержащий ответ сервера. Тип возвращенного объекта <xref:System.Net.WebResponse> определяется с помощью схемы URI запроса. Например:
  
    ```csharp  
    WebResponse response = request.GetResponse();  
    ```  
  
    ```vb  
    Dim response As WebResponse = request.GetResponse()  
    ```  
  
4.  Вы можете получить доступ к свойствам объекта `WebResponse` или привести этот объект к связанному с определенным протоколом экземпляру для считывания свойств для определенного протокола. 

    Например, чтобы получить доступ к свойствам, связанным с протоколом HTTP, для <xref:System.Net.HttpWebResponse>, приведите объект `WebResponse` к ссылке `HttpWebResponse`. В следующем примере кода показано, как отобразить свойство <xref:System.Net.HttpWebResponse.StatusDescription%2A?displayProperty=nameWithType>, связанное с протоколом HTTP, которое было отправлено в ответе:
  
    ```csharp  
    Console.WriteLine (((HttpWebResponse)response).StatusDescription);  
    ```  
  
    ```vb  
    Console.WriteLine(CType(response,HttpWebResponse).StatusDescription)  
    ```  
  
5.  Чтобы получить поток, содержащий данные ответа, отправленные сервером, вызовите метод <xref:System.Net.WebResponse.GetResponseStream%2A?displayProperty=nameWithType>. Например:  
  
    ```csharp  
    Stream dataStream = response.GetResponseStream();  
    ```  
  
    ```vb  
    Dim dataStream As Stream = response.GetResponseStream()  
    ```  
  
6.  После считывания данных из объекта ответа закройте его с помощью метода <xref:System.Net.WebResponse.Close%2A?displayProperty=nameWithType> или закройте поток ответа с помощью метода <xref:System.IO.Stream.Close%2A?displayProperty=nameWithType>. Если не закрыть объект ответа или поток, у приложения могут закончиться подключения к серверу и оно может оказаться неспособным обрабатывать новые запросы. Так как при закрытии ответа метод `WebResponse.Close` вызывает `Stream.Close`, вызывать `Close` для объектов как потока, так и ответа не требуется (при этом выполнение такой операции не приведет к негативным последствиям). Например:
  
    ```csharp  
    response.Close();  
    ```  
  
    ```vb  
    response.Close()  
    ```  
  
## <a name="example"></a>Пример  

В следующем примере кода показано создание запроса к веб-серверу и считывание данных в ответе:  
  
```csharp  
using System;  
using System.IO;  
using System.Net;  
using System.Text;  
  
namespace Examples.System.Net  
{  
    public class WebRequestGetExample  
    {  
        public static void Main()  
        {  
            // Create a request for the URL.   
            WebRequest request = WebRequest.Create(  
              "http://www.contoso.com/default.html");  
            // If required by the server, set the credentials.  
            request.Credentials = CredentialCache.DefaultCredentials;  

            // Get the response.  
            WebResponse response = request.GetResponse();  
            // Display the status.  
            Console.WriteLine (((HttpWebResponse)response).StatusDescription);  

            // Get the stream containing content returned by the server.  
            Stream dataStream = response.GetResponseStream();  
            // Open the stream by using a StreamReader for easy access.  
            StreamReader reader = new StreamReader(dataStream);  

            // Read the content.  
            string responseFromServer = reader.ReadToEnd();  
            // Display the content.  
            Console.WriteLine(responseFromServer);  

            // Clean up the response.  
            reader.Close();  
            response.Close();  
        }  
    }  
}  
```  
  
```vb  
Imports System  
Imports System.IO  
Imports System.Net  
Imports System.Text  

Namespace Examples.System.Net 

    Public Class WebRequestGetExample  

        Public Shared Sub Main()  

            ' Create a request for the URL.   
            Dim request As WebRequest = _  
              WebRequest.Create("http://www.contoso.com/default.html")  
            ' If required by the server, set the credentials.  
            request.Credentials = CredentialCache.DefaultCredentials  

            ' Get the response.  
            Dim response As WebResponse = request.GetResponse()  
            ' Display the status.  
            Console.WriteLine(CType(response,HttpWebResponse).StatusDescription)  

            ' Get the stream containing content returned by the server.  
            Dim dataStream As Stream = response.GetResponseStream()  
            ' Open the stream by using a StreamReader for easy access.  
            Dim reader As New StreamReader(dataStream)  

            ' Read the content.  
            Dim responseFromServer As String = reader.ReadToEnd()  
            ' Display the content.  
            Console.WriteLine(responseFromServer)  

            ' Clean up the response.  
            reader.Close()  
            response.Close() 

        End Sub   

    End Class  
 
End Namespace  
```  
  
## <a name="see-also"></a>См. также
- [Создание интернет-запросов](creating-internet-requests.md)
- [Использование потоков в сети](using-streams-on-the-network.md)
- [Доступ к Интернету через прокси-сервер](accessing-the-internet-through-a-proxy.md)
- [Запрос данных](requesting-data.md)
- [Практическое руководство. Отправка данных с помощью класса WebRequest](how-to-send-data-using-the-webrequest-class.md)
