---
title: Ссылка <reference> на дружественную сборку является недопустимой
ms.date: 07/20/2015
f1_keywords:
- vbc31535
- bc31535
helpviewer_keywords:
- BC31535
ms.assetid: 6540c1d0-bb19-4051-a579-2e4f9094585e
ms.openlocfilehash: 0966cea26c5dde8f116081c7a6411b4275e50f40
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2019
ms.locfileid: "58817049"
---
# <a name="friend-assembly-reference-reference-is-invalid"></a>Ссылка на дружественную сборку \<ссылку > является недопустимым
Ссылка на дружественную сборку \<ссылку > является недопустимым. Для сборок, подписанных строгим именем, в объявлении InternalsVisibleTo должен быть указан открытый ключ.  
  
 Имя сборки, передаваемое <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> конструктор атрибута идентифицирует сборку со строгим именем, но он не включает `PublicKey` атрибута.  
  
 **Идентификатор ошибки:** BC31535  
  
## <a name="to-correct-this-error"></a>Исправление ошибки  
  
1.  Определите открытый ключ для строгое имя дружественной сборки. Поместить открытый ключ как часть имени сборки, передаваемый в <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> конструктор атрибута с помощью `PublicKey` атрибута.  
  
## <a name="see-also"></a>См. также

- <xref:System.Reflection.AssemblyName>
- [Дружественные сборки](../../../standard/assembly/friend-assemblies.md)
