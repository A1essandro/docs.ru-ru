---
title: "Директива using (Справочник по C#)"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- using directive [C#]
ms.assetid: b42b8e61-5e7e-439c-bb71-370094b44ae8
caps.latest.revision: 31
author: BillWagner
ms.author: wiwagn
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 1129efd8a1c4058a9648eab61f98cdcef7e9f2f7
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="using-directive-c-reference"></a><span data-ttu-id="1dbae-102">Директива using (Справочник по C#)</span><span class="sxs-lookup"><span data-stu-id="1dbae-102">using Directive (C# Reference)</span></span>
<span data-ttu-id="1dbae-103">Директива `using` используется в следующих трех целях.</span><span class="sxs-lookup"><span data-stu-id="1dbae-103">The `using` directive has three uses:</span></span>  
  
-   <span data-ttu-id="1dbae-104">Для разрешения использования типов в пространстве имен, чтобы не нужно было квалифицировать использование типа в этом пространстве имен:</span><span class="sxs-lookup"><span data-stu-id="1dbae-104">To allow the use of types in a namespace so that you do not have to qualify the use of a type in that namespace:</span></span>  
  
    ```csharp  
    using System.Text;  
    ```  
  
-   <span data-ttu-id="1dbae-105">Для разрешения доступа к статическим членам типа без необходимости квалификации доступа с помощью имени типа:</span><span class="sxs-lookup"><span data-stu-id="1dbae-105">To allow you to access static members of a type without having to qualify the access with the type name.</span></span> 
  
    ```csharp  
    using static System.Math;  
    ```  
     
    <span data-ttu-id="1dbae-106">Дополнительные сведения см. в разделе [Директива using static](using-static.md).</span><span class="sxs-lookup"><span data-stu-id="1dbae-106">For more information, see the [using static directive](using-static.md).</span></span>

-   <span data-ttu-id="1dbae-107">Чтобы создать псевдоним для пространства имен или типа.</span><span class="sxs-lookup"><span data-stu-id="1dbae-107">To create an alias for a namespace or a type.</span></span> <span data-ttu-id="1dbae-108">Это называется *директивой using static*.</span><span class="sxs-lookup"><span data-stu-id="1dbae-108">This is called a *using alias directive*.</span></span>  
  
    ```csharp  
    using Project = PC.MyCompany.Project;  
    ```  
  
 <span data-ttu-id="1dbae-109">Ключевое слово `using` также используется для создания *операторов using*, которые помогают обеспечить правильную обработку объектов <xref:System.IDisposable>, таких как файлы и шрифты.</span><span class="sxs-lookup"><span data-stu-id="1dbae-109">The `using` keyword is also used to create *using statements*, which help ensure that <xref:System.IDisposable> objects such as files and fonts are handled correctly.</span></span> <span data-ttu-id="1dbae-110">Дополнительные сведения см. в разделе [Оператор using](../../../csharp/language-reference/keywords/using-statement.md).</span><span class="sxs-lookup"><span data-stu-id="1dbae-110">See [using Statement](../../../csharp/language-reference/keywords/using-statement.md) for more information.</span></span>  
  
## <a name="using-static-type"></a><span data-ttu-id="1dbae-111">Использование статического типа</span><span class="sxs-lookup"><span data-stu-id="1dbae-111">Using Static Type</span></span>  
 <span data-ttu-id="1dbae-112">Вы можете обращаться к статическим членам типа без необходимости квалификации доступа с помощью имени типа:</span><span class="sxs-lookup"><span data-stu-id="1dbae-112">You can access static members of a type without having to qualify the access with the type name:</span></span>  
  
```csharp  
using static System.Console;   
using static System.Math;  
class Program   
{   
    static void Main()   
    {   
        WriteLine(Sqrt(3*3 + 4*4));   
    }   
}  
```  
  
## <a name="remarks"></a><span data-ttu-id="1dbae-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="1dbae-113">Remarks</span></span>  
 <span data-ttu-id="1dbae-114">Область директивы `using` ограничена файлом, в котором она находится.</span><span class="sxs-lookup"><span data-stu-id="1dbae-114">The scope of a `using` directive is limited to the file in which it appears.</span></span>  
  
 <span data-ttu-id="1dbae-115">Создайте псевдоним `using`, чтобы упростить квалификацию идентификатора для пространства имен или типа.</span><span class="sxs-lookup"><span data-stu-id="1dbae-115">Create a `using` alias to make it easier to qualify an identifier to a namespace or type.</span></span> <span data-ttu-id="1dbae-116">Правая часть директивы псевдонима using всегда должна быть полным типом независимо от директив using до нее.</span><span class="sxs-lookup"><span data-stu-id="1dbae-116">The right side of a using alias directive must always be a fully-qualified type regardless of the using directives that come before it.</span></span>  
  
 <span data-ttu-id="1dbae-117">Создайте директиву `using`, чтобы использовать типы в пространстве имен без необходимости указания этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1dbae-117">Create a `using` directive to use the types in a namespace without having to specify the namespace.</span></span> <span data-ttu-id="1dbae-118">Директива `using` не предоставляет доступ к пространствам имен, вложенным в указанное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="1dbae-118">A `using` directive does not give you access to any namespaces that are nested in the namespace you specify.</span></span>  
  
 <span data-ttu-id="1dbae-119">Пространства имен делятся на две категории: пользовательские и системные.</span><span class="sxs-lookup"><span data-stu-id="1dbae-119">Namespaces come in two categories: user-defined and system-defined.</span></span> <span data-ttu-id="1dbae-120">Пользовательские пространства имен задаются в вашем коде.</span><span class="sxs-lookup"><span data-stu-id="1dbae-120">User-defined namespaces are namespaces defined in your code.</span></span> <span data-ttu-id="1dbae-121">Список системных пространств имен см. в разделе [Библиотека классов .NET Framework](http://go.microsoft.com/fwlink/?LinkID=227195).</span><span class="sxs-lookup"><span data-stu-id="1dbae-121">For a list of the system-defined namespaces, see [.NET Framework Class Library](http://go.microsoft.com/fwlink/?LinkID=227195).</span></span>  
  
 <span data-ttu-id="1dbae-122">Примеры ссылочных методов в других сборках см. в разделе [Создание и использование библиотек DLL C#](http://msdn.microsoft.com/library/70f65026-3687-4e9c-ab79-c18b97dd8be4).</span><span class="sxs-lookup"><span data-stu-id="1dbae-122">For examples on referencing methods in other assemblies, see [Creating and Using C# DLLs](http://msdn.microsoft.com/library/70f65026-3687-4e9c-ab79-c18b97dd8be4).</span></span>  
  
## <a name="example-1"></a><span data-ttu-id="1dbae-123">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1dbae-123">Example 1</span></span>  
  
 <span data-ttu-id="1dbae-124">В следующем примере показано, как задать и использовать псевдоним `using` для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1dbae-124">The following example shows how to define and use a `using` alias for a namespace:</span></span>  
  
 <span data-ttu-id="1dbae-125">[!code-cs[csrefKeywordsNamespace#8](../../../csharp/language-reference/keywords/codesnippet/CSharp/using-directive_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="1dbae-125">[!code-cs[csrefKeywordsNamespace#8](../../../csharp/language-reference/keywords/codesnippet/CSharp/using-directive_1.cs)]</span></span>  
  
 <span data-ttu-id="1dbae-126">Псевдоним using не может иметь открытый универсальный тип с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="1dbae-126">A using alias directive cannot have an open generic type on the right hand side.</span></span> <span data-ttu-id="1dbae-127">Например, нельзя создать псевдоним using для List\<T>, но можно создать его для List\<int>.</span><span class="sxs-lookup"><span data-stu-id="1dbae-127">For example, you cannot create a using alias for a List\<T>, but you can create one for a List\<int>.</span></span>  
  
## <a name="example-2"></a><span data-ttu-id="1dbae-128">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1dbae-128">Example 2</span></span>  
  
 <span data-ttu-id="1dbae-129">В следующем примере показано, как задать директиву `using` и псевдоним `using` для класса.</span><span class="sxs-lookup"><span data-stu-id="1dbae-129">The following example shows how to define a `using` directive and a `using` alias for a class:</span></span>  
  
 <span data-ttu-id="1dbae-130">[!code-cs[csrefKeywordsNamespace#9](../../../csharp/language-reference/keywords/codesnippet/CSharp/using-directive_2.cs)]</span><span class="sxs-lookup"><span data-stu-id="1dbae-130">[!code-cs[csrefKeywordsNamespace#9](../../../csharp/language-reference/keywords/codesnippet/CSharp/using-directive_2.cs)]</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="1dbae-131">Спецификация языка C#</span><span class="sxs-lookup"><span data-stu-id="1dbae-131">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1dbae-132">См. также</span><span class="sxs-lookup"><span data-stu-id="1dbae-132">See Also</span></span>  
 <span data-ttu-id="1dbae-133">[Справочник по C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="1dbae-133">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="1dbae-134">[Руководство по программированию на C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="1dbae-134">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="1dbae-135">[Использование пространств имен](../../../csharp/programming-guide/namespaces/using-namespaces.md) </span><span class="sxs-lookup"><span data-stu-id="1dbae-135">[Using Namespaces](../../../csharp/programming-guide/namespaces/using-namespaces.md) </span></span>  
 <span data-ttu-id="1dbae-136">[Ключевые слова в C#](../../../csharp/language-reference/keywords/index.md) </span><span class="sxs-lookup"><span data-stu-id="1dbae-136">[C# Keywords](../../../csharp/language-reference/keywords/index.md) </span></span>  
 <span data-ttu-id="1dbae-137">[Ключевые слова, используемые для пространств имен](../../../csharp/language-reference/keywords/namespace-keywords.md) </span><span class="sxs-lookup"><span data-stu-id="1dbae-137">[Namespace Keywords](../../../csharp/language-reference/keywords/namespace-keywords.md) </span></span>  
 <span data-ttu-id="1dbae-138">[Пространства имен](../../../csharp/programming-guide/namespaces/index.md) </span><span class="sxs-lookup"><span data-stu-id="1dbae-138">[Namespaces](../../../csharp/programming-guide/namespaces/index.md) </span></span>  
 [<span data-ttu-id="1dbae-139">Оператор using</span><span class="sxs-lookup"><span data-stu-id="1dbae-139">using Statement</span></span>](../../../csharp/language-reference/keywords/using-statement.md)

