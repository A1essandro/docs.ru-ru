---
title: Метод ISymUnmanagedDocument::GetSourceRange
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetSourceRange
helpviewer_keywords:
- ISymUnmanagedDocument::GetSourceRange method [.NET Framework debugging]
- GetSourceRange method [.NET Framework debugging]
ms.assetid: 20fefee7-1040-41ba-93dc-bd42f68b90c2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 00baed93bd9ab48c92de83dac76931c3149afc2b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424642"
---
# <a name="isymunmanageddocumentgetsourcerange-method"></a><span data-ttu-id="16075-102">Метод ISymUnmanagedDocument::GetSourceRange</span><span class="sxs-lookup"><span data-stu-id="16075-102">ISymUnmanagedDocument::GetSourceRange Method</span></span>
<span data-ttu-id="16075-103">Возвращает заданный диапазон внедренного источника в заданный буфер.</span><span class="sxs-lookup"><span data-stu-id="16075-103">Returns the specified range of the embedded source into the given buffer.</span></span> <span data-ttu-id="16075-104">Размер буфера должен быть достаточно велик для хранения источника.</span><span class="sxs-lookup"><span data-stu-id="16075-104">The buffer must be large enough to hold the source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="16075-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16075-105">Syntax</span></span>  
  
```  
HRESULT GetSourceRange(  
    [in]  ULONG32  startLine,  
    [in]  ULONG32  startColumn,  
    [in]  ULONG32  endLine,  
    [in]  ULONG32  endColumn,  
    [in]  ULONG32  cSourceBytes,  
    [out] ULONG32  *pcSourceBytes,  
    [out, size_is(cSourceBytes),  
        length_is(*pcSourceBytes)] BYTE source[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="16075-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="16075-106">Parameters</span></span>  
 `startLine`  
 <span data-ttu-id="16075-107">[in] Начальная строка текущего документа.</span><span class="sxs-lookup"><span data-stu-id="16075-107">[in] The starting line in the current document.</span></span>  
  
 `startColumn`  
 <span data-ttu-id="16075-108">[in] Начальный столбец текущего документа.</span><span class="sxs-lookup"><span data-stu-id="16075-108">[in] The starting column in the current document.</span></span>  
  
 `endLine`  
 <span data-ttu-id="16075-109">[in] Последняя строка в текущем документе.</span><span class="sxs-lookup"><span data-stu-id="16075-109">[in] The final line in the current document.</span></span>  
  
 `endColumn`  
 <span data-ttu-id="16075-110">[in] Последний столбец в текущем документе.</span><span class="sxs-lookup"><span data-stu-id="16075-110">[in] The final column in the current document.</span></span>  
  
 `cSourceBytes`  
 <span data-ttu-id="16075-111">[in] Размер источника в байтах.</span><span class="sxs-lookup"><span data-stu-id="16075-111">[in] The size of the source, in bytes.</span></span>  
  
 `pcSourceBytes`  
 <span data-ttu-id="16075-112">[out] Указатель на переменную, которая получает размер источника.</span><span class="sxs-lookup"><span data-stu-id="16075-112">[out] A pointer to a variable that receives the source size.</span></span>  
  
 `source`  
 <span data-ttu-id="16075-113">[out] Размер и длина указанного диапазона исходного документа, в байтах.</span><span class="sxs-lookup"><span data-stu-id="16075-113">[out] The size and length of the specified range of the source document, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="16075-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16075-114">Return Value</span></span>  
 <span data-ttu-id="16075-115">Значение S_OK, если метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="16075-115">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16075-116">См. также</span><span class="sxs-lookup"><span data-stu-id="16075-116">See Also</span></span>  
 [<span data-ttu-id="16075-117">Интерфейс ISymUnmanagedDocument</span><span class="sxs-lookup"><span data-stu-id="16075-117">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
