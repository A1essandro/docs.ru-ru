---
title: "this (Справочник по C#)"
description: "Ключевое слово this (справочник по C#)"
keywords: "this (C#), ключевое слово this (C#), ключевое слово this (справочник по C#), ключевое слово this (справочник по языку C#)"
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- this
- this_CSharpKeyword
dev_langs:
- CSharp
helpviewer_keywords:
- this keyword [C#]
ms.assetid: d4f827fe-4710-410b-89b8-867dad44b8a3
caps.latest.revision: 19
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
ms.openlocfilehash: 1e764bbd85d06a3b1898f6574064b2844f6d6813
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="this-c-reference"></a><span data-ttu-id="cb6d1-104">this (Справочник по C#)</span><span class="sxs-lookup"><span data-stu-id="cb6d1-104">this (C# Reference)</span></span>
<span data-ttu-id="cb6d1-105">Ключевое слово `this` ссылается на текущий экземпляр класса, а также используется в качестве модификатора первого параметра метода расширения.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-105">The `this` keyword refers to the current instance of the class and is also used as a modifier of the first parameter of an extension method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cb6d1-106">В этой статье рассматривается использование `this` с экземплярами класса.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-106">This article discusses the use of `this` with class instances.</span></span> <span data-ttu-id="cb6d1-107">Дополнительные сведения об использовании этого ключевого слова в методах расширения см. в разделе [Методы расширения](../../../csharp/programming-guide/classes-and-structs/extension-methods.md).</span><span class="sxs-lookup"><span data-stu-id="cb6d1-107">For more information about its use in extension methods, see [Extension Methods](../../../csharp/programming-guide/classes-and-structs/extension-methods.md).</span></span>  
  
 <span data-ttu-id="cb6d1-108">Ниже перечислены наиболее частые способы использования `this`.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-108">The following are common uses of `this`:</span></span>  
  
-   <span data-ttu-id="cb6d1-109">Для квалификации элементов, скрытых одинаковыми именами, например:</span><span class="sxs-lookup"><span data-stu-id="cb6d1-109">To qualify members hidden by similar names, for example:</span></span>  
  
 <span data-ttu-id="cb6d1-110">[!code-cs[csrefKeywordsAccess#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="cb6d1-110">[!code-cs[csrefKeywordsAccess#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_1.cs)]</span></span>  
  
-   <span data-ttu-id="cb6d1-111">Для передачи другим методам объекта в качестве параметра, например:</span><span class="sxs-lookup"><span data-stu-id="cb6d1-111">To pass an object as a parameter to other methods, for example:</span></span>  
  
    ```  
    CalcTax(this);  
    ```  
  
-   <span data-ttu-id="cb6d1-112">Для объявления индексаторов, например:</span><span class="sxs-lookup"><span data-stu-id="cb6d1-112">To declare indexers, for example:</span></span>  
  
 <span data-ttu-id="cb6d1-113">[!code-cs[csrefKeywordsAccess#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_2.cs)]</span><span class="sxs-lookup"><span data-stu-id="cb6d1-113">[!code-cs[csrefKeywordsAccess#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_2.cs)]</span></span>  
  
 <span data-ttu-id="cb6d1-114">У статических функций-членов нет указателя `this`, так как они существуют только на уровне класса и не являются частями объектов.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-114">Static member functions, because they exist at the class level and not as part of an object, do not have a `this` pointer.</span></span> <span data-ttu-id="cb6d1-115">Использование ссылки на `this` в статическом методе является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-115">It is an error to refer to `this` in a static method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cb6d1-116">Пример</span><span class="sxs-lookup"><span data-stu-id="cb6d1-116">Example</span></span>  
 <span data-ttu-id="cb6d1-117">В этом примере `this` используется для квалификации членов класса `Employee`, `name` и `alias`, которые скрыты одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-117">In this example, `this` is used to qualify the `Employee` class members, `name` and `alias`, which are hidden by similar names.</span></span> <span data-ttu-id="cb6d1-118">Это ключевое слово также используется для передачи объекта в метод `CalcTax`, который принадлежит другому классу.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-118">It is also used to pass an object to the method `CalcTax`, which belongs to another class.</span></span>  
  
 <span data-ttu-id="cb6d1-119">[!code-cs[csrefKeywordsAccess#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_3.cs)]</span><span class="sxs-lookup"><span data-stu-id="cb6d1-119">[!code-cs[csrefKeywordsAccess#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_3.cs)]</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="cb6d1-120">Спецификация языка C#</span><span class="sxs-lookup"><span data-stu-id="cb6d1-120">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="cb6d1-121">См. также</span><span class="sxs-lookup"><span data-stu-id="cb6d1-121">See Also</span></span>  
 <span data-ttu-id="cb6d1-122">[Справочник по C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="cb6d1-122">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="cb6d1-123">[Руководство по программированию на C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="cb6d1-123">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="cb6d1-124">[Ключевые слова в C#](../../../csharp/language-reference/keywords/index.md) </span><span class="sxs-lookup"><span data-stu-id="cb6d1-124">[C# Keywords](../../../csharp/language-reference/keywords/index.md) </span></span>  
 <span data-ttu-id="cb6d1-125">[base](../../../csharp/language-reference/keywords/base.md) </span><span class="sxs-lookup"><span data-stu-id="cb6d1-125">[base](../../../csharp/language-reference/keywords/base.md) </span></span>  
 [<span data-ttu-id="cb6d1-126">Методы</span><span class="sxs-lookup"><span data-stu-id="cb6d1-126">Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/methods.md)

