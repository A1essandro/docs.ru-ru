---
title: AssemblyAttributesGoHereSM
ms.date: 03/30/2017
api_name:
- AssemblyAttributesGoHereSM
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AssemblyAttributesGoHereSM
helpviewer_keywords:
- AssemblyAttributesGoHereSM type
- Alink API, AssemblyAttributesGoHereSM type
ms.assetid: 4cf9bf39-1527-49e0-a0e9-55e7a018bf66
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6d47ca3a9134266d1c40447cea6eb8aaf2cc9eb9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706301"
---
# <a name="assemblyattributesgoheresm"></a><span data-ttu-id="4f012-102">AssemblyAttributesGoHereSM</span><span class="sxs-lookup"><span data-stu-id="4f012-102">AssemblyAttributesGoHereSM</span></span>
<span data-ttu-id="4f012-103">Используется ALink как заполнитель для хранения сведений о пользовательских атрибутах.</span><span class="sxs-lookup"><span data-stu-id="4f012-103">Used by ALink as a placeholder to store information about custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f012-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f012-104">Syntax</span></span>  
  
```  
AssemblyAttributeGoHereSM  
```  
  
## <a name="remarks"></a><span data-ttu-id="4f012-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f012-105">Remarks</span></span>  
 <span data-ttu-id="4f012-106">Ссылки на этот тип можно включать в модули NETMODULE, источник которых содержат пользовательские атрибуты сборки.</span><span class="sxs-lookup"><span data-stu-id="4f012-106">References to this type might be embedded inside netmodules whose sources contain assembly custom attributes.</span></span> <span data-ttu-id="4f012-107">При построении манифеста сборки из одного или нескольких файлов, содержащих ссылки на эти NETMODULE, ALink использует сведения, подключенные к этим ссылкам, для выдачи фактических пользовательских атрибутов.</span><span class="sxs-lookup"><span data-stu-id="4f012-107">When building an assembly manifest from one or more netmodules that contain references to these types, ALink uses information attached to these references to emit real custom attributes.</span></span> <span data-ttu-id="4f012-108">Таким образом, экземпляр этого типа никогда не создается, а ссылки на него используются только как часть процесса сборки и бесполезны в окончательной сборке.</span><span class="sxs-lookup"><span data-stu-id="4f012-108">As such, this type is never instantiated, and references to it are used only as part of the build process and serve no purpose in the final assembly.</span></span>  
  
 <span data-ttu-id="4f012-109">Ссылки на этот тип указывают пользовательские атрибуты многократного использования, связанные с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="4f012-109">References to this type indicate custom attributes that are security related and multiple-use.</span></span>  
  
 <span data-ttu-id="4f012-110">Эти типы помечены как «внутренние» в .NET Framework и находятся в <xref:System.Runtime.CompilerServices>.</span><span class="sxs-lookup"><span data-stu-id="4f012-110">These types are marked "internal" within the .NET Framework, and are located in <xref:System.Runtime.CompilerServices>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4f012-111">Требования</span><span class="sxs-lookup"><span data-stu-id="4f012-111">Requirements</span></span>  
 <span data-ttu-id="4f012-112">mscorlib.dll</span><span class="sxs-lookup"><span data-stu-id="4f012-112">mscorlib.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f012-113">См. также</span><span class="sxs-lookup"><span data-stu-id="4f012-113">See also</span></span>
- [<span data-ttu-id="4f012-114">AssemblyAttributesGoHere</span><span class="sxs-lookup"><span data-stu-id="4f012-114">AssemblyAttributesGoHere</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgohere.md)
- [<span data-ttu-id="4f012-115">AssemblyAttributesGoHereM</span><span class="sxs-lookup"><span data-stu-id="4f012-115">AssemblyAttributesGoHereM</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoherem.md)
- [<span data-ttu-id="4f012-116">AssemblyAttributesGoHereS</span><span class="sxs-lookup"><span data-stu-id="4f012-116">AssemblyAttributesGoHereS</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoheres.md)
