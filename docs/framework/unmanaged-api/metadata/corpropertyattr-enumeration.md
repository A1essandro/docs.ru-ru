---
title: "Перечисление CorPropertyAttr"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorPropertyAttr
api_location: mscoree.dll
api_type: COM
f1_keywords: CorPropertyAttr
helpviewer_keywords: CorPropertyAttr enumeration [.NET Framework metadata]
ms.assetid: 58ac8202-854d-4efd-acfb-d2da8b446e12
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: a87676064f39dc01d04e881bbf46476fb12a1c65
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="corpropertyattr-enumeration"></a>Перечисление CorPropertyAttr
Содержит значения, описывающие метаданные свойства.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
typedef enum CorPropertyAttr {  
  
    prSpecialName           =   0x0200,   
    prReservedMask          =   0xf400,  
    prRTSpecialName         =   0x0400,  
    prHasDefault            =   0x1000,  
    prUnused                =   0xe9ff  
  
} CorPropertyAttr;  
```  
  
## <a name="members"></a>Члены  
  
|Член|Описание|  
|------------|-----------------|  
|`prSpecialName`|Указывает, что это свойство является особым, и указывает его имя как.|  
|`prReservedMask`|Зарезервировано для внутреннего использования средой CLR.|  
|`prRTSpecialName`|Указывает, что внутренние API метаданных среды CLR должны проверить кодировку имени свойства.|  
|`prHasDefault`|Указывает, что свойство имеет значение по умолчанию.|  
|`prUnused`|Не используется.|  
  
## <a name="requirements"></a>Требования  
 **Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок:** CorHdr.h  
  
 **Версии платформы .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>См. также  
 [Перечисления метаданных](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
