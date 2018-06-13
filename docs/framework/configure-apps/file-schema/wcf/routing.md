---
title: '&lt;Маршрутизация&gt;'
ms.date: 03/30/2017
ms.assetid: a210c209-3940-4288-9a8e-39b1e62606bc
ms.openlocfilehash: 1771d8a2603a8f61af6ba6e2acf6243d2fd073f7
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2018
ms.locfileid: "32747731"
---
# <a name="ltroutinggt"></a><span data-ttu-id="820bd-102">&lt;Маршрутизация&gt;</span><span class="sxs-lookup"><span data-stu-id="820bd-102">&lt;routing&gt;</span></span>

<span data-ttu-id="820bd-103">Представляет раздел конфигурации для определения набора фильтров маршрутизации, которые определяют тип Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> для использования при вычислении входящих сообщений, а также маршрутизацию таблиц, определяющих целевые конечные точки для Отправка сообщений при соответствии критериям фильтра.</span><span class="sxs-lookup"><span data-stu-id="820bd-103">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span>

<span data-ttu-id="820bd-104">[**\<system.serviceModel >**](system-servicemodel.md) </span><span class="sxs-lookup"><span data-stu-id="820bd-104">[**\<system.serviceModel>**](system-servicemodel.md) </span></span>  
<span data-ttu-id="820bd-105">&nbsp;&nbsp;**\<Маршрутизация >**</span><span class="sxs-lookup"><span data-stu-id="820bd-105">&nbsp;&nbsp;**\<routing>**</span></span>

## <a name="syntax"></a><span data-ttu-id="820bd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="820bd-106">Syntax</span></span>

```xml
<system.serviceModel>
  <routing>
    <filters>
      <filter customType="String" 
              filterData="String" 
              filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath" 
              name="String" />
    </filters>
    <routingTables>
      <table name="String">
        <entries>
          <add endpoint="String" 
               filterName="String" 
               priority="Integer" />
        </entries>
      </table>
    </routingTables>
  </routing>
</system.serviceModel>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="820bd-107">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="820bd-107">Attributes and elements</span></span>

<span data-ttu-id="820bd-108">В следующих разделах описаны атрибуты, дочерние и родительские элементы.</span><span class="sxs-lookup"><span data-stu-id="820bd-108">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="820bd-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="820bd-109">Attributes</span></span>

<span data-ttu-id="820bd-110">Нет</span><span class="sxs-lookup"><span data-stu-id="820bd-110">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="820bd-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="820bd-111">Child elements</span></span>

|     | <span data-ttu-id="820bd-112">Описание</span><span class="sxs-lookup"><span data-stu-id="820bd-112">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="820bd-113">**\<Фильтры >**</span><span class="sxs-lookup"><span data-stu-id="820bd-113">**\<filters>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md) | <span data-ttu-id="820bd-114">Содержит набор фильтров маршрутизации, которые определяют тип MessageFilter Windows Communication Foundation (WCF) будет использоваться при вычислении входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="820bd-114">Contains a set of routing filters that determine the type of Windows Communication Foundation (WCF) MessageFilter will be used when evaluating incoming messages.</span></span> |
| [<span data-ttu-id="820bd-115">**\<filterTables >**</span><span class="sxs-lookup"><span data-stu-id="820bd-115">**\<filterTables>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertables.md) | <span data-ttu-id="820bd-116">Содержит сопоставление между фильтрами маршрутизации и целевыми конечными точками для определения того, какие конечные точки будут использоваться при совпадении с критериями фильтра.</span><span class="sxs-lookup"><span data-stu-id="820bd-116">Contains mappings between the routing filters and the target endpoints to specify which endpoint to use when the filter matches.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="820bd-117">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="820bd-117">Parent elements</span></span>

|     | <span data-ttu-id="820bd-118">Описание</span><span class="sxs-lookup"><span data-stu-id="820bd-118">Description</span></span> |
| --- | ----------- |
| <span data-ttu-id="820bd-119">**\<система. ServiceModel >**</span><span class="sxs-lookup"><span data-stu-id="820bd-119">**\<system.ServiceModel>**</span></span> | <span data-ttu-id="820bd-120">Корневой элемент всех элементов конфигурации WCF.</span><span class="sxs-lookup"><span data-stu-id="820bd-120">The root element of all WCF configuration elements.</span></span> |

## <a name="see-also"></a><span data-ttu-id="820bd-121">См. также</span><span class="sxs-lookup"><span data-stu-id="820bd-121">See also</span></span>

<xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
