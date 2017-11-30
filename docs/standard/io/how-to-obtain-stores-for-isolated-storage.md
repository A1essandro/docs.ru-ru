---
title: "Практическое руководство. Получение хранилищ для изолированного хранения"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- stores, obtaining
- storing data using isolated storage, obtaining stores
- isolated storage, obtaining stores
- data stores, obtaining
- data storage using isolated storage, obtaining stores
ms.assetid: fcb6b178-d526-47c4-b029-e946f880f9db
caps.latest.revision: "19"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: bb0b877aa0f4cee36bd1f8c1cea624cf9368fbaa
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-obtain-stores-for-isolated-storage"></a><span data-ttu-id="859b1-102">Практическое руководство. Получение хранилищ для изолированного хранения</span><span class="sxs-lookup"><span data-stu-id="859b1-102">How to: Obtain Stores for Isolated Storage</span></span>
<span data-ttu-id="859b1-103">Изолированное хранилище предоставляет виртуальную файловую систему в ячейке данных.</span><span class="sxs-lookup"><span data-stu-id="859b1-103">An isolated store exposes a virtual file system within a data compartment.</span></span> <span data-ttu-id="859b1-104"><xref:System.IO.IsolatedStorage.IsolatedStorageFile> Класс предоставляет ряд методов для взаимодействия с помощью изолированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="859b1-104">The <xref:System.IO.IsolatedStorage.IsolatedStorageFile> class supplies a number of methods for interacting with an isolated store.</span></span> <span data-ttu-id="859b1-105">Для создания и получения хранилищ <xref:System.IO.IsolatedStorage.IsolatedStorageFile> содержит три статических методов:</span><span class="sxs-lookup"><span data-stu-id="859b1-105">To create and retrieve stores, <xref:System.IO.IsolatedStorage.IsolatedStorageFile> provides three static methods:</span></span>  
  
-   <span data-ttu-id="859b1-106"><xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForAssembly%2A>Возвращает хранилища, изолированного по пользователю и сборке.</span><span class="sxs-lookup"><span data-stu-id="859b1-106"><xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForAssembly%2A> returns storage that is isolated by user and assembly.</span></span>  
  
-   <span data-ttu-id="859b1-107"><xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForDomain%2A>Возвращает хранилища, в котором изолирована, домена и сборки.</span><span class="sxs-lookup"><span data-stu-id="859b1-107"><xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForDomain%2A> returns storage that is isolated by domain and assembly.</span></span>  
  
     <span data-ttu-id="859b1-108">Оба метода получения хранилища, к которому принадлежит код, из которого они вызываются.</span><span class="sxs-lookup"><span data-stu-id="859b1-108">Both methods retrieve a store that belongs to the code from which they are called.</span></span>  
  
-   <span data-ttu-id="859b1-109">Статический метод <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> Возвращает изолированное хранилище, указанное посредством передачи в комбинации параметров области.</span><span class="sxs-lookup"><span data-stu-id="859b1-109">The static method <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> returns an isolated store that is specified by passing in a combination of scope parameters.</span></span>  
  
 <span data-ttu-id="859b1-110">Следующий код возвращает хранилища, изолированного по пользователю, сборке и домену.</span><span class="sxs-lookup"><span data-stu-id="859b1-110">The following code returns a store that is isolated by user, assembly, and domain.</span></span>  
  
 [!code-cpp[Conceptual.IsolatedStorage#6](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.isolatedstorage/cpp/source6.cpp#6)]
 [!code-csharp[Conceptual.IsolatedStorage#6](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.isolatedstorage/cs/source6.cs#6)]
 [!code-vb[Conceptual.IsolatedStorage#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.isolatedstorage/vb/source6.vb#6)]  
  
 <span data-ttu-id="859b1-111">Можно использовать <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> метод, чтобы указать, что хранилище должно перемещаться вместе с перемещаемым профилем пользователя.</span><span class="sxs-lookup"><span data-stu-id="859b1-111">You can use the <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> method to specify that a store should roam with a roaming user profile.</span></span> <span data-ttu-id="859b1-112">Дополнительные сведения о том, как настроить эту функцию, в разделе [типа изоляции](../../../docs/standard/io/types-of-isolation.md).</span><span class="sxs-lookup"><span data-stu-id="859b1-112">For details on how to set this up, see [Types of Isolation](../../../docs/standard/io/types-of-isolation.md).</span></span>  
  
 <span data-ttu-id="859b1-113">Изолированные хранилища, полученные из разных сборок, по умолчанию, различные хранилища.</span><span class="sxs-lookup"><span data-stu-id="859b1-113">Isolated stores obtained from within different assemblies are, by default, different stores.</span></span> <span data-ttu-id="859b1-114">Можно использовать хранилище другой сборки или домена путем передачи в свидетельство сборки или домена в параметрах <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> метод.</span><span class="sxs-lookup"><span data-stu-id="859b1-114">You can access the store of a different assembly or domain by passing in the assembly or domain evidence in the parameters of the <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> method.</span></span> <span data-ttu-id="859b1-115">Это разрешение для доступа к изолированному хранилищу по идентификатору домена приложения.</span><span class="sxs-lookup"><span data-stu-id="859b1-115">This requires permission to access isolated storage by application domain identity.</span></span> <span data-ttu-id="859b1-116">Дополнительные сведения см. в разделе <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> перегруженных версий метода.</span><span class="sxs-lookup"><span data-stu-id="859b1-116">For more information, see the <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> method overloads.</span></span>  
  
 <span data-ttu-id="859b1-117"><xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForAssembly%2A>, <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForDomain%2A>, И <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> методы возвращают <xref:System.IO.IsolatedStorage.IsolatedStorageFile> объекта.</span><span class="sxs-lookup"><span data-stu-id="859b1-117">The <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForAssembly%2A>, <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForDomain%2A>, and <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> methods return an <xref:System.IO.IsolatedStorage.IsolatedStorageFile> object.</span></span> <span data-ttu-id="859b1-118">Сведения о выборе типа изоляции лучше всего подходит для конкретной ситуации, в разделе [типа изоляции](../../../docs/standard/io/types-of-isolation.md).</span><span class="sxs-lookup"><span data-stu-id="859b1-118">To help you decide which isolation type is most appropriate for your situation, see [Types of Isolation](../../../docs/standard/io/types-of-isolation.md).</span></span> <span data-ttu-id="859b1-119">При наличии объект файла изолированного хранилища, можно использовать методы изолированного хранилища для чтения, записи, создания и удаления файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="859b1-119">When you have an isolated storage file object, you can use the isolated storage methods to read, write, create, and delete files and directories.</span></span>  
  
 <span data-ttu-id="859b1-120">Отсутствует механизм предотвращения передачи кодом <xref:System.IO.IsolatedStorage.IsolatedStorageFile> объект на код, который не имеет необходимых прав доступа для получения само хранилище.</span><span class="sxs-lookup"><span data-stu-id="859b1-120">There is no mechanism that prevents code from passing an <xref:System.IO.IsolatedStorage.IsolatedStorageFile> object to code that does not have sufficient access to get the store itself.</span></span> <span data-ttu-id="859b1-121">Идентификаторы доменов и сборок и разрешения изолированного хранения проверяются только при получении ссылки на <xref:System.IO.IsolatedStorage.IsolatedStorage> будет получен, обычно в <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForAssembly%2A>, <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForDomain%2A>, или <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> метод.</span><span class="sxs-lookup"><span data-stu-id="859b1-121">Domain and assembly identities and isolated storage permissions are checked only when a reference to an <xref:System.IO.IsolatedStorage.IsolatedStorage> object is obtained, typically in the <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForAssembly%2A>, <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetUserStoreForDomain%2A>, or <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> method.</span></span> <span data-ttu-id="859b1-122">Защиту ссылок на <xref:System.IO.IsolatedStorage.IsolatedStorageFile> объектов отвечает, поэтому код, использующий эти ссылки.</span><span class="sxs-lookup"><span data-stu-id="859b1-122">Protecting references to <xref:System.IO.IsolatedStorage.IsolatedStorageFile> objects is, therefore, the responsibility of the code that uses these references.</span></span>  
  
## <a name="example"></a><span data-ttu-id="859b1-123">Пример</span><span class="sxs-lookup"><span data-stu-id="859b1-123">Example</span></span>  
 <span data-ttu-id="859b1-124">Ниже приведен простой пример получения классом хранилища, изолированного по пользователю и сборке.</span><span class="sxs-lookup"><span data-stu-id="859b1-124">The following code provides a simple example of a class obtaining a store that is isolated by user and assembly.</span></span> <span data-ttu-id="859b1-125">Код может быть изменен для получения хранилища, изолированного по пользователю, домену и сборке, путем добавления <xref:System.IO.IsolatedStorage.IsolatedStorageScope.Domain?displayProperty=nameWithType> к аргументам, <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> метод передает.</span><span class="sxs-lookup"><span data-stu-id="859b1-125">The code can be changed to retrieve a store that is isolated by user, domain, and assembly by adding <xref:System.IO.IsolatedStorage.IsolatedStorageScope.Domain?displayProperty=nameWithType> to the arguments that the <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetStore%2A> method passes.</span></span>  
  
 <span data-ttu-id="859b1-126">После выполнения кода можно убедиться, что хранилище создано, введя **StoreAdm/LIST** из командной строки.</span><span class="sxs-lookup"><span data-stu-id="859b1-126">After you run the code, you can confirm that a store was created by typing **StoreAdm /LIST** at the command line.</span></span> <span data-ttu-id="859b1-127">Эта процедура выполняется [средство изолированного хранилища (Storeadm.exe)](../../../docs/framework/tools/storeadm-exe-isolated-storage-tool.md) и выводит все текущие изолированные хранилища для пользователя.</span><span class="sxs-lookup"><span data-stu-id="859b1-127">This runs the [Isolated Storage tool (Storeadm.exe)](../../../docs/framework/tools/storeadm-exe-isolated-storage-tool.md) and lists all the current isolated stores for the user.</span></span>  
  
 [!code-cpp[Conceptual.IsolatedStorage#7](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.isolatedstorage/cpp/source6.cpp#7)]
 [!code-csharp[Conceptual.IsolatedStorage#7](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.isolatedstorage/cs/source6.cs#7)]
 [!code-vb[Conceptual.IsolatedStorage#7](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.isolatedstorage/vb/source6.vb#7)]  
  
## <a name="see-also"></a><span data-ttu-id="859b1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="859b1-128">See Also</span></span>  
 <xref:System.IO.IsolatedStorage.IsolatedStorageFile>  
 <xref:System.IO.IsolatedStorage.IsolatedStorageScope>  
 [<span data-ttu-id="859b1-129">Изолированное хранилище</span><span class="sxs-lookup"><span data-stu-id="859b1-129">Isolated Storage</span></span>](../../../docs/standard/io/isolated-storage.md)  
 [<span data-ttu-id="859b1-130">Типы изоляции</span><span class="sxs-lookup"><span data-stu-id="859b1-130">Types of Isolation</span></span>](../../../docs/standard/io/types-of-isolation.md)  
 [<span data-ttu-id="859b1-131">Сборки в среде CLR</span><span class="sxs-lookup"><span data-stu-id="859b1-131">Assemblies in the Common Language Runtime</span></span>](../../../docs/framework/app-domains/assemblies-in-the-common-language-runtime.md)
