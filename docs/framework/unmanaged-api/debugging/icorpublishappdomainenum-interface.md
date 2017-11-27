---
title: "Интерфейс ICorPublishAppDomainEnum"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorPublishAppDomainEnum
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorPublishAppDomainEnum
helpviewer_keywords: ICorPublishAppDomainEnum interface [.NET Framework debugging]
ms.assetid: bb798c56-042e-475d-a245-b6fac36d0c07
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 8359eda5432a9b3818fd58f6adc18570e4c5f154
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="icorpublishappdomainenum-interface"></a><span data-ttu-id="13b74-102">Интерфейс ICorPublishAppDomainEnum</span><span class="sxs-lookup"><span data-stu-id="13b74-102">ICorPublishAppDomainEnum Interface</span></span>
<span data-ttu-id="13b74-103">Подкласс [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) интерфейс, предоставляющий методы для обхода коллекцию [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md) объекты, которые в настоящее время существует внутри процесса.</span><span class="sxs-lookup"><span data-stu-id="13b74-103">A subclass of the [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) interface that provides methods to traverse a collection of [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md) objects that currently exist within a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="13b74-104">Методы</span><span class="sxs-lookup"><span data-stu-id="13b74-104">Methods</span></span>  
  
|<span data-ttu-id="13b74-105">Метод</span><span class="sxs-lookup"><span data-stu-id="13b74-105">Method</span></span>|<span data-ttu-id="13b74-106">Описание</span><span class="sxs-lookup"><span data-stu-id="13b74-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="13b74-107">Метод Next</span><span class="sxs-lookup"><span data-stu-id="13b74-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-next-method.md)|<span data-ttu-id="13b74-108">Возвращает заданное число `ICorPublishAppDomain` экземпляров из коллекции, начиная с текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="13b74-108">Gets the specified number of `ICorPublishAppDomain` instances from the collection, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="13b74-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="13b74-109">Remarks</span></span>  
 <span data-ttu-id="13b74-110">`ICorPublishAppDomainEnum` Интерфейс реализует методы интерфейса абстрактным, [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).</span><span class="sxs-lookup"><span data-stu-id="13b74-110">The `ICorPublishAppDomainEnum` interface implements the methods of the abstract interface, [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="13b74-111">Требования</span><span class="sxs-lookup"><span data-stu-id="13b74-111">Requirements</span></span>  
 <span data-ttu-id="13b74-112">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="13b74-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="13b74-113">**Заголовок:** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="13b74-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="13b74-114">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="13b74-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="13b74-115">**Версии платформы .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="13b74-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13b74-116">См. также</span><span class="sxs-lookup"><span data-stu-id="13b74-116">See Also</span></span>  
 [<span data-ttu-id="13b74-117">Интерфейсы отладки</span><span class="sxs-lookup"><span data-stu-id="13b74-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="13b74-118">Компонентный класс CorpubPublish</span><span class="sxs-lookup"><span data-stu-id="13b74-118">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
