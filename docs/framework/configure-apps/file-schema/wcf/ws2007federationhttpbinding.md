---
title: '&lt;ws2007FederationHttpBinding&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 9af4ec79-cdef-457e-9dca-09d5eb821594
caps.latest.revision: "14"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: b1f85d4cc45075f82035fa5b8c0c95341ba142d6
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/19/2018
---
# <a name="ltws2007federationhttpbindinggt"></a><span data-ttu-id="7798b-102">&lt;ws2007FederationHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="7798b-102">&lt;ws2007FederationHttpBinding&gt;</span></span>
<span data-ttu-id="7798b-103">Безопасная привязка, производный от [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) и поддерживает федеративную безопасность.</span><span class="sxs-lookup"><span data-stu-id="7798b-103">A secure and interoperable binding that derives from [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md) and supports federated security.</span></span>  
  
 <span data-ttu-id="7798b-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="7798b-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="7798b-105">\<привязки ></span><span class="sxs-lookup"><span data-stu-id="7798b-105">\<bindings></span></span>  
<span data-ttu-id="7798b-106">\<ws2007FederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="7798b-106">\<ws2007FederationHttpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7798b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7798b-107">Syntax</span></span>  
  
```xml  
<ws2007FederationHttpBinding>  
    <binding   
        bypassProxyOnLocal="Boolean"  
        closeTimeout="TimeSpan"   
        hostNameComparisonMode="StrongWildcard/Exact/WeakWildcard"  
        maxBufferPoolSize="integer"  
        maxReceivedMessageSize="integer"  
        messageEncoding="Text/Mtom"   
                name="string"  
        openTimeout="TimeSpan"   
        privacyNoticeAt="Uri"  
        privacyNoticeVersion="Integer"  
        proxyAddress="Uri"   
        receiveTimeout="TimeSpan"  
        sendTimeout="TimeSpan"  
        textEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding"  
        transactionFlow="Boolean"  
        useDefaultWebProxy="Boolean">  
        <security mode="None/Message/TransportWithMessageCredential">  
           <message negotiateServiceCredential="Boolean"  
                algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
                issuedTokenType="string"  
                issuedKeyType="SymmetricKey/PublicKey"  
           </message>  
        </security>  
        <reliableSession ordered="Boolean"  
           inactivityTimeout="TimeSpan"  
           enabled="Boolean" />  
       <readerQuotas             maxArrayLength="Integer"            maxBytesPerRead="Integer"            maxDepth="Integer"             maxNameTableCharCount="Integer"                     maxStringContentLength="Integer" />    </binding>  
</ws2007FederationHttpBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7798b-108">Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="7798b-108">Attributes and Elements</span></span>  
 <span data-ttu-id="7798b-109">В следующих разделах описаны атрибуты, дочерние и родительские элементы.</span><span class="sxs-lookup"><span data-stu-id="7798b-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7798b-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7798b-110">Attributes</span></span>  
  
|<span data-ttu-id="7798b-111">Атрибут</span><span class="sxs-lookup"><span data-stu-id="7798b-111">Attribute</span></span>|<span data-ttu-id="7798b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7798b-112">Description</span></span>|  
|---------------|-----------------|  
|`bypassProxyOnLocal`|<span data-ttu-id="7798b-113">Значение, определяющее, будет ли выполняться обход прокси-сервера для локальных адресов.</span><span class="sxs-lookup"><span data-stu-id="7798b-113">A value that indicates whether to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="7798b-114">Значение по умолчанию — `false`.</span><span class="sxs-lookup"><span data-stu-id="7798b-114">The default is `false`.</span></span>|  
|`closeTimeout`|<span data-ttu-id="7798b-115">Значение <xref:System.TimeSpan>, которое задает длительность времени ожидания для завершения операции закрытия.</span><span class="sxs-lookup"><span data-stu-id="7798b-115">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="7798b-116">Это значение должно быть больше или равно <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="7798b-116">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="7798b-117">Значение по умолчанию - 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="7798b-117">The default is 00:01:00.</span></span>|  
|`hostnameComparisonMode`|<span data-ttu-id="7798b-118">Задает режим сравнения имен узлов HTTP для анализа универсальных кодов ресурсов (URI).</span><span class="sxs-lookup"><span data-stu-id="7798b-118">Specifies the HTTP hostname comparison mode used to parse URIs.</span></span> <span data-ttu-id="7798b-119">Это атрибут типа <xref:System.ServiceModel.HostNameComparisonMode>, который указывает, используется ли имя узла для доступа к службе при сравнении по универсальному коду ресурсов (URI).</span><span class="sxs-lookup"><span data-stu-id="7798b-119">This attribute is of type <xref:System.ServiceModel.HostNameComparisonMode>, which indicates whether the hostname is used to reach the service when matching on the URI.</span></span> <span data-ttu-id="7798b-120">Значение по умолчанию — <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, при котором имя узла в найденном соответствии не используется.</span><span class="sxs-lookup"><span data-stu-id="7798b-120">The default value is <xref:System.ServiceModel.HostNameComparisonMode.StrongWildcard>, which ignores the hostname in the match.</span></span>|  
|`maxBufferPoolSize`|<span data-ttu-id="7798b-121">Максимальный размер буферного пула для этой привязки.</span><span class="sxs-lookup"><span data-stu-id="7798b-121">The maximum buffer pool size for this binding.</span></span> <span data-ttu-id="7798b-122">Значение по умолчанию - 524 288 байт (512 \* 1024).</span><span class="sxs-lookup"><span data-stu-id="7798b-122">The default is 524,288 bytes (512 \* 1024).</span></span> <span data-ttu-id="7798b-123">Многие элементы [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] используют буферы.</span><span class="sxs-lookup"><span data-stu-id="7798b-123">Many parts of [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] use buffers.</span></span> <span data-ttu-id="7798b-124">При создании буферов и их уничтожении после каждого использования расходуется слишком много ресурсов; при сборке мусора для буферов также расходуется слишком много ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7798b-124">Creating and destroying buffers each time they are used is expensive, and garbage collection for buffers is also expensive.</span></span> <span data-ttu-id="7798b-125">Буферные пулы позволяют брать буфер из пула, использовать его, а затем возвращать обратно, когда он больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="7798b-125">With buffer pools, you can take a buffer from the pool, use it, and return it to the pool once you are done.</span></span> <span data-ttu-id="7798b-126">Это позволяет избежать излишней нагрузки, связанной с созданием и уничтожением буферов.</span><span class="sxs-lookup"><span data-stu-id="7798b-126">Thus the overhead in creating and destroying buffers is avoided.</span></span>|  
|`maxReceivedMessageSize`|<span data-ttu-id="7798b-127">Максимальный размер сообщения (в байтах), включая заголовки, которое можно получить по каналу, настроенному с использованием этой привязки.</span><span class="sxs-lookup"><span data-stu-id="7798b-127">The maximum message size, in bytes, including headers, that can be received on a channel configured with this binding.</span></span> <span data-ttu-id="7798b-128">Отправитель сообщения, которое превысит это ограничение, получает ошибку SOAP.</span><span class="sxs-lookup"><span data-stu-id="7798b-128">The sender of a message that exceeds this limit receives a SOAP fault.</span></span> <span data-ttu-id="7798b-129">Получатель отклоняет сообщение и создает запись о событии в журнале трассировки.</span><span class="sxs-lookup"><span data-stu-id="7798b-129">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="7798b-130">Значение по умолчанию — 65536.</span><span class="sxs-lookup"><span data-stu-id="7798b-130">The default is 65536.</span></span>|  
|`messageEncoding`|<span data-ttu-id="7798b-131">Определяет кодировщик, используемый для кодировки сообщения.</span><span class="sxs-lookup"><span data-stu-id="7798b-131">Defines the encoder used to encode the message.</span></span> <span data-ttu-id="7798b-132">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7798b-132">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="7798b-133">-Text: Используется кодировщик текстовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="7798b-133">-   Text: Use a text message encoder.</span></span><br /><span data-ttu-id="7798b-134">-Mtom: Используется кодировщик передачи сообщений организации 1.0 (MTOM).</span><span class="sxs-lookup"><span data-stu-id="7798b-134">-   Mtom: Use a Message Transmission Organization Mechanism 1.0 (MTOM) encoder.</span></span><br /><br /> <span data-ttu-id="7798b-135">Значение по умолчанию - Text.</span><span class="sxs-lookup"><span data-stu-id="7798b-135">The default is Text.</span></span><br /><br /> <span data-ttu-id="7798b-136">Это атрибут типа <xref:System.ServiceModel.WSMessageEncoding>.</span><span class="sxs-lookup"><span data-stu-id="7798b-136">This attribute is of type <xref:System.ServiceModel.WSMessageEncoding>.</span></span>|  
|`name`|<span data-ttu-id="7798b-137">Имя конфигурации привязки.</span><span class="sxs-lookup"><span data-stu-id="7798b-137">The configuration name of the binding.</span></span> <span data-ttu-id="7798b-138">Это значение должно быть уникальным, поскольку оно используется в качестве идентификатора привязки.</span><span class="sxs-lookup"><span data-stu-id="7798b-138">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="7798b-139">Начиная с версии [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] для привязок и поведений необязательно задавать имена.</span><span class="sxs-lookup"><span data-stu-id="7798b-139">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="7798b-140">Дополнительные сведения о конфигурации по умолчанию и безымянные привязок и поведений см. в разделе [упрощенной конфигурации](../../../../../docs/framework/wcf/simplified-configuration.md) и [упрощенной конфигурации для служб WCF](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="7798b-140">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="7798b-141">Значение <xref:System.TimeSpan>, которое задает длительность времени ожидания для завершения операции открытия.</span><span class="sxs-lookup"><span data-stu-id="7798b-141">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="7798b-142">Это значение должно быть больше или равно <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="7798b-142">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="7798b-143">Значение по умолчанию - 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="7798b-143">The default is 00:01:00.</span></span>|  
|`privactyNoticeAt`|<span data-ttu-id="7798b-144">Универсальный код ресурса (URI), определяющий расположение примечания о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="7798b-144">A URI at which the privacy notice is located.</span></span>|  
|`privactyNoticeVersion`|<span data-ttu-id="7798b-145">Версия текущего примечания о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="7798b-145">The version of the current privacy notice.</span></span>|  
|`proxyAddress`|<span data-ttu-id="7798b-146">Универсальный код ресурса (URI), задающий адрес прокси-сервера HTTP.</span><span class="sxs-lookup"><span data-stu-id="7798b-146">A URI that specifies the address of the HTTP proxy.</span></span> <span data-ttu-id="7798b-147">Если параметр `useDefaultWebProxy` имеет значение `true`, данный параметр должен иметь значение `null`.</span><span class="sxs-lookup"><span data-stu-id="7798b-147">If `useDefaultWebProxy` is `true`, this setting must be `null`.</span></span> <span data-ttu-id="7798b-148">Значение по умолчанию — `null`.</span><span class="sxs-lookup"><span data-stu-id="7798b-148">The default is `null`.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="7798b-149">Значение <xref:System.TimeSpan>, которое задает длительность времени ожидания для завершения операции получения.</span><span class="sxs-lookup"><span data-stu-id="7798b-149">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="7798b-150">Это значение должно быть больше или равно <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="7798b-150">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="7798b-151">Значение по умолчанию - 00:10:00.</span><span class="sxs-lookup"><span data-stu-id="7798b-151">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="7798b-152">Значение <xref:System.TimeSpan>, которое задает длительность времени ожидания для завершения операции отправки.</span><span class="sxs-lookup"><span data-stu-id="7798b-152">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="7798b-153">Это значение должно быть больше или равно <xref:System.TimeSpan.Zero>.</span><span class="sxs-lookup"><span data-stu-id="7798b-153">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="7798b-154">Значение по умолчанию - 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="7798b-154">The default is 00:01:00.</span></span>|  
|`textEncoding`|<span data-ttu-id="7798b-155">Задает кодировку, используемую при отправке сообщений через привязку.</span><span class="sxs-lookup"><span data-stu-id="7798b-155">Sets the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="7798b-156">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7798b-156">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="7798b-157">-BigEndianUnicode: Big Endian кодировку Юникод.</span><span class="sxs-lookup"><span data-stu-id="7798b-157">-   BigEndianUnicode: Unicode Big Endian encoding.</span></span><br /><span data-ttu-id="7798b-158">-Unicode: 16-разрядная кодировка.</span><span class="sxs-lookup"><span data-stu-id="7798b-158">-   Unicode: 16-bit encoding.</span></span><br /><span data-ttu-id="7798b-159">-UTF8: 8-разрядная кодировка.</span><span class="sxs-lookup"><span data-stu-id="7798b-159">-   UTF8: 8-bit encoding.</span></span><br /><br /> <span data-ttu-id="7798b-160">Значение по умолчанию - UTF8.</span><span class="sxs-lookup"><span data-stu-id="7798b-160">The default is UTF8.</span></span> <span data-ttu-id="7798b-161">Это атрибут типа <xref:System.Text.Encoding>.</span><span class="sxs-lookup"><span data-stu-id="7798b-161">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
|`transactionFlow`|<span data-ttu-id="7798b-162">Значение, определяющее, поддерживает ли привязка потоки WS-Transactions.</span><span class="sxs-lookup"><span data-stu-id="7798b-162">A value that specifies whether the binding supports flowing WS-Transactions.</span></span> <span data-ttu-id="7798b-163">Значение по умолчанию — `false`.</span><span class="sxs-lookup"><span data-stu-id="7798b-163">The default is `false`.</span></span>|  
|`useDefaultWebProxy`|<span data-ttu-id="7798b-164">Значение, указывающее, должен ли использоваться автоматически настроенный системный прокси-сервер HTTP.</span><span class="sxs-lookup"><span data-stu-id="7798b-164">A value that indicates whether the system’s auto-configured HTTP proxy is used.</span></span> <span data-ttu-id="7798b-165">Если данный атрибут имеет значение `null`, прокси-адрес должен быть равен `true` (то есть не задан).</span><span class="sxs-lookup"><span data-stu-id="7798b-165">The proxy address must be `null` (that is, not set) if this attribute is `true`.</span></span> <span data-ttu-id="7798b-166">Значение по умолчанию — `true`.</span><span class="sxs-lookup"><span data-stu-id="7798b-166">The default is `true`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7798b-167">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7798b-167">Child Elements</span></span>  
  
|<span data-ttu-id="7798b-168">Элемент</span><span class="sxs-lookup"><span data-stu-id="7798b-168">Element</span></span>|<span data-ttu-id="7798b-169">Описание:</span><span class="sxs-lookup"><span data-stu-id="7798b-169">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7798b-170">\<Безопасность ></span><span class="sxs-lookup"><span data-stu-id="7798b-170">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wsfederationhttpbinding.md)|<span data-ttu-id="7798b-171">Определяет параметры безопасности сообщения.</span><span class="sxs-lookup"><span data-stu-id="7798b-171">Defines the security settings for the message.</span></span> <span data-ttu-id="7798b-172">Это элемент типа <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="7798b-172">This element is of type <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement>.</span></span>|  
|[<span data-ttu-id="7798b-173">\<readerQuotas></span><span class="sxs-lookup"><span data-stu-id="7798b-173">\<readerQuotas></span></span>](http://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|<span data-ttu-id="7798b-174">Определяет ограничения по сложности сообщений SOAP, которые могут обрабатываться конечными точками, настроенными с использованием этой привязки.</span><span class="sxs-lookup"><span data-stu-id="7798b-174">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="7798b-175">Это элемент типа <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span><span class="sxs-lookup"><span data-stu-id="7798b-175">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
|[<span data-ttu-id="7798b-176">reliableSession</span><span class="sxs-lookup"><span data-stu-id="7798b-176">reliableSession</span></span>](http://msdn.microsoft.com/library/9c93818a-7dfa-43d5-b3a1-1aafccf3a00b)|<span data-ttu-id="7798b-177">Указывает, устанавливаются ли между конечными точками канала надежные сеансы.</span><span class="sxs-lookup"><span data-stu-id="7798b-177">Specifies whether reliable sessions are established between channel endpoints.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="7798b-178">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7798b-178">Parent Elements</span></span>  
  
|<span data-ttu-id="7798b-179">Элемент</span><span class="sxs-lookup"><span data-stu-id="7798b-179">Element</span></span>|<span data-ttu-id="7798b-180">Описание:</span><span class="sxs-lookup"><span data-stu-id="7798b-180">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7798b-181">\<bindings></span><span class="sxs-lookup"><span data-stu-id="7798b-181">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="7798b-182">Этот элемент содержит коллекцию стандартных и пользовательских привязок.</span><span class="sxs-lookup"><span data-stu-id="7798b-182">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7798b-183">Примечания</span><span class="sxs-lookup"><span data-stu-id="7798b-183">Remarks</span></span>  
 <span data-ttu-id="7798b-184">Федерация - это возможность совместного использования удостоверений между несколькими предприятиями или доверенными доменами в целях проверки подлинности и авторизации.</span><span class="sxs-lookup"><span data-stu-id="7798b-184">Federation is the ability to share identities across multiple enterprises or trust domains for authentication and authorization.</span></span> <span data-ttu-id="7798b-185">Для сопоставления представления идентификации между доверенными доменами используется протокол WS-Trust.</span><span class="sxs-lookup"><span data-stu-id="7798b-185">It uses the WS-Trust protocol to map the identity representation from one trust domain to another.</span></span> <span data-ttu-id="7798b-186">Федеративная привязка HTTP поддерживает безопасность SOAP, а также безопасность в смешанном режиме, но она не поддерживает безопасность транспорта.</span><span class="sxs-lookup"><span data-stu-id="7798b-186">Federated HTTP binding supports SOAP security as well as mixed-mode security, but it does not support transport security.</span></span> <span data-ttu-id="7798b-187">Службы, настроенные с использованием этой привязки, должны использовать транспорт HTTP.</span><span class="sxs-lookup"><span data-stu-id="7798b-187">Services configured with this binding must use the HTTP transport.</span></span> [!INCLUDE[crdefault](../../../../../includes/crdefault-md.md)]<span data-ttu-id="7798b-188">[ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="7798b-188"> [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="7798b-189">Пример</span><span class="sxs-lookup"><span data-stu-id="7798b-189">Example</span></span>  
  
```xml  
<configuration>  
<system.ServiceModel>  
<bindings>  
<ws2007FederationHttpBinding>  
    <binding   
        bypassProxyOnLocal="false"  
        transactionFlow="false"  
        hostNameComparisonMode="WeakWildcard"  
        maxReceivedMessageSize="1000"  
        messageEncoding="Mtom"   
        proxyAddress="http://www.contoso.com"   
        textEncoding="Utf16TextEncoding"  
        useDefaultWebProxy="false">  
        <reliableSession ordered="false"  
            inactivityTimeout="00:02:00" enabled="true" />  
        <security mode="None">  
           <message negotiateServiceCredential="false"  
                algorithmSuite="Aes128"  
                issuedTokenType="http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAMLV1.1"   
                issuedKeyType="PublicKey">  
               <issuer address="http://localhost/Sts" />  
           </message>  
        </security>  
    </binding>  
</ws2007FederationBinding>  
</bindings>  
</system.ServiceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="7798b-190">См. также</span><span class="sxs-lookup"><span data-stu-id="7798b-190">See Also</span></span>  
 <xref:System.ServiceModel.WS2007FederationHttpBinding>  
 <xref:System.ServiceModel.Configuration.WS2007FederationHttpBindingElement>  
 [<span data-ttu-id="7798b-191">\<wsFederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="7798b-191">\<wsFederationHttpBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md)  
 [<span data-ttu-id="7798b-192">Привязки</span><span class="sxs-lookup"><span data-stu-id="7798b-192">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="7798b-193">Настройка привязок, предоставляемых системой</span><span class="sxs-lookup"><span data-stu-id="7798b-193">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="7798b-194">Использование привязок для настройки служб Windows Communication Foundation и клиентов</span><span class="sxs-lookup"><span data-stu-id="7798b-194">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](http://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="7798b-195">\<Привязка ></span><span class="sxs-lookup"><span data-stu-id="7798b-195">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
