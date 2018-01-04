---
title: "Практическое руководство. Удаление элемента ToolStripMenuItem из меню MDI-приложения (Windows Forms)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- menu items [Windows Forms], removing from MDI drop-down menus
- MenuStrip control [Windows Forms], merging
- MenuStrip control [Windows Forms], removing
- MDI [Windows Forms], merging menu items
ms.assetid: bdafe60d-82ee-45bc-97fe-eeefca6e54c1
caps.latest.revision: "12"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 4ef6927c56e18f74e04648c541f8cff4d29167cc
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-remove-a-toolstripmenuitem-from-an-mdi-drop-down-menu-windows-forms"></a><span data-ttu-id="b19fa-102">Практическое руководство. Удаление элемента ToolStripMenuItem из меню MDI-приложения (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="b19fa-102">How to: Remove a ToolStripMenuItem from an MDI Drop-Down Menu (Windows Forms)</span></span>
<span data-ttu-id="b19fa-103">В некоторых приложениях вид дочернего окна многодокументного интерфейса (MDI) может отличаться от родительского окна MDI.</span><span class="sxs-lookup"><span data-stu-id="b19fa-103">In some applications, the kind of a multiple-document interface (MDI) child window can be different from the MDI parent window.</span></span> <span data-ttu-id="b19fa-104">Например, родительским окном MDI может быть электронная таблица, а дочерним окном MDI — диаграмма.</span><span class="sxs-lookup"><span data-stu-id="b19fa-104">For example, the MDI parent might be a spreadsheet, and the MDI child might be a chart.</span></span> <span data-ttu-id="b19fa-105">В этом случае может потребоваться дополнить содержимое меню родительского окна MDI содержимым меню дочерней MDI-формы, по мере того как активируются дочерние окна MDI различных типов.</span><span class="sxs-lookup"><span data-stu-id="b19fa-105">In that case, you want to update the contents of the MDI parent's menu with the contents of the MDI child's menu as MDI child windows of different kinds are activated.</span></span>  
  
 <span data-ttu-id="b19fa-106">В следующей процедуре используется <xref:System.Windows.Forms.Form.IsMdiContainer%2A>, <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A>, <xref:System.Windows.Forms.MergeAction>, и <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> свойств, чтобы удалить элемент меню из раскрывающегося списка части родительского меню MDI.</span><span class="sxs-lookup"><span data-stu-id="b19fa-106">The following procedure uses the <xref:System.Windows.Forms.Form.IsMdiContainer%2A>, <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A>, <xref:System.Windows.Forms.MergeAction>, and <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> properties to remove a menu item from the drop-down part of the MDI parent menu.</span></span> <span data-ttu-id="b19fa-107">Восстановление удаленных пунктов меню родительского меню MDI закрытии дочернего окна MDI.</span><span class="sxs-lookup"><span data-stu-id="b19fa-107">Closing the MDI child window restores the removed menu items to the MDI parent menu.</span></span>  
  
### <a name="to-remove-a-menustrip-from-an-mdi-drop-down-menu"></a><span data-ttu-id="b19fa-108">Чтобы удалить объект MenuStrip из раскрывающегося меню MDI</span><span class="sxs-lookup"><span data-stu-id="b19fa-108">To remove a MenuStrip from an MDI drop-down menu</span></span>  
  
1.  <span data-ttu-id="b19fa-109">Создайте форму и присвойте ее свойству <xref:System.Windows.Forms.Form.IsMdiContainer%2A> значение `true`.</span><span class="sxs-lookup"><span data-stu-id="b19fa-109">Create a form and set its <xref:System.Windows.Forms.Form.IsMdiContainer%2A> property to `true`.</span></span>  
  
2.  <span data-ttu-id="b19fa-110">Добавьте <xref:System.Windows.Forms.MenuStrip> на `Form1` и присвойте свойству <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> для элемента <xref:System.Windows.Forms.MenuStrip> значение `true`.</span><span class="sxs-lookup"><span data-stu-id="b19fa-110">Add a <xref:System.Windows.Forms.MenuStrip> to `Form1` and set the <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> property of the <xref:System.Windows.Forms.MenuStrip> to `true`.</span></span>  
  
3.  <span data-ttu-id="b19fa-111">Добавьте пункт меню верхнего уровня в `Form1`<xref:System.Windows.Forms.MenuStrip> и присвойте его свойству <xref:System.Windows.Forms.Control.Text%2A> значение `&File`.</span><span class="sxs-lookup"><span data-stu-id="b19fa-111">Add a top-level menu item to the `Form1`<xref:System.Windows.Forms.MenuStrip> and set its <xref:System.Windows.Forms.Control.Text%2A> property to `&File`.</span></span>  
  
4.  <span data-ttu-id="b19fa-112">Добавьте три подменю `&File` меню и присвойте их <xref:System.Windows.Forms.ToolStripItem.Text%2A> свойства `&Open`, `&Import from`, и `E&xit`.</span><span class="sxs-lookup"><span data-stu-id="b19fa-112">Add three submenu items to the `&File` menu item and set their <xref:System.Windows.Forms.ToolStripItem.Text%2A> properties to `&Open`, `&Import from`, and `E&xit`.</span></span>  
  
5.  <span data-ttu-id="b19fa-113">Добавьте два подменю к `&Import from` подменю и задайте их <xref:System.Windows.Forms.ToolStripItem.Text%2A> свойства `&Word` и `&Excel`.</span><span class="sxs-lookup"><span data-stu-id="b19fa-113">Add two submenu items to the `&Import from` submenu item and set their <xref:System.Windows.Forms.ToolStripItem.Text%2A> properties to `&Word` and `&Excel`.</span></span>  
  
6.  <span data-ttu-id="b19fa-114">Добавьте в проект форму, добавьте <xref:System.Windows.Forms.MenuStrip> на форму и присвойте его свойству <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> элемента `Form2`<xref:System.Windows.Forms.MenuStrip> значение `true`.</span><span class="sxs-lookup"><span data-stu-id="b19fa-114">Add a form to the project, add a <xref:System.Windows.Forms.MenuStrip> to the form, and set the <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> property of the `Form2`<xref:System.Windows.Forms.MenuStrip> to `true`.</span></span>  
  
7.  <span data-ttu-id="b19fa-115">Добавьте пункт меню верхнего уровня в `Form2`<xref:System.Windows.Forms.MenuStrip> и присвойте его свойству <xref:System.Windows.Forms.ToolStripItem.Text%2A> значение `&File`.</span><span class="sxs-lookup"><span data-stu-id="b19fa-115">Add a top-level menu item to the `Form2`<xref:System.Windows.Forms.MenuStrip> and set its <xref:System.Windows.Forms.ToolStripItem.Text%2A> property to `&File`.</span></span>  
  
8.  <span data-ttu-id="b19fa-116">Добавить `&Import from` пункт подменю `&File` меню `Form2`и добавьте `&Word` пункт подменю `&File` меню.</span><span class="sxs-lookup"><span data-stu-id="b19fa-116">Add an `&Import from` submenu item to the `&File` menu of `Form2`, and add an `&Word` submenu item to the `&File` menu.</span></span>  
  
9. <span data-ttu-id="b19fa-117">Задать <xref:System.Windows.Forms.MergeAction> и <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> свойства `Form2` элементы меню, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b19fa-117">Set the <xref:System.Windows.Forms.MergeAction> and <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> properties of the `Form2` menu items as shown in the following table.</span></span>  
  
    |<span data-ttu-id="b19fa-118">Пункт меню Form2</span><span class="sxs-lookup"><span data-stu-id="b19fa-118">Form2 menu item</span></span>|<span data-ttu-id="b19fa-119">Значение MergeAction</span><span class="sxs-lookup"><span data-stu-id="b19fa-119">MergeAction value</span></span>|<span data-ttu-id="b19fa-120">Значение MergeIndex</span><span class="sxs-lookup"><span data-stu-id="b19fa-120">MergeIndex value</span></span>|  
    |---------------------|-----------------------|----------------------|  
    |<span data-ttu-id="b19fa-121">Файл</span><span class="sxs-lookup"><span data-stu-id="b19fa-121">File</span></span>|<span data-ttu-id="b19fa-122">MatchOnly</span><span class="sxs-lookup"><span data-stu-id="b19fa-122">MatchOnly</span></span>|<span data-ttu-id="b19fa-123">-1</span><span class="sxs-lookup"><span data-stu-id="b19fa-123">-1</span></span>|  
    |<span data-ttu-id="b19fa-124">Импорт из</span><span class="sxs-lookup"><span data-stu-id="b19fa-124">Import from</span></span>|<span data-ttu-id="b19fa-125">MatchOnly</span><span class="sxs-lookup"><span data-stu-id="b19fa-125">MatchOnly</span></span>|<span data-ttu-id="b19fa-126">-1</span><span class="sxs-lookup"><span data-stu-id="b19fa-126">-1</span></span>|  
    |<span data-ttu-id="b19fa-127">Слово</span><span class="sxs-lookup"><span data-stu-id="b19fa-127">Word</span></span>|<span data-ttu-id="b19fa-128">Удалить</span><span class="sxs-lookup"><span data-stu-id="b19fa-128">Remove</span></span>|<span data-ttu-id="b19fa-129">-1</span><span class="sxs-lookup"><span data-stu-id="b19fa-129">-1</span></span>|  
  
10. <span data-ttu-id="b19fa-130">В `Form1`, создайте обработчик событий для <xref:System.Windows.Forms.Control.Click> событие `&Open` <xref:System.Windows.Forms.ToolStripMenuItem>.</span><span class="sxs-lookup"><span data-stu-id="b19fa-130">In `Form1`, create an event handler for the <xref:System.Windows.Forms.Control.Click> event of the `&Open`<xref:System.Windows.Forms.ToolStripMenuItem>.</span></span>  
  
11. <span data-ttu-id="b19fa-131">В обработчик событий вставьте код, аналогичный приведенному в следующем примере кода для создания и отображения новых экземпляров `Form2` как дочерних окон MDI `Form1`:</span><span class="sxs-lookup"><span data-stu-id="b19fa-131">Within the event handler, insert code similar to the following code example to create and display new instances of `Form2` as MDI children of `Form1`:</span></span>  
  
    ```vb  
    Private Sub openToolStripMenuItem_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles openToolStripMenuItem.Click  
        Dim NewMDIChild As New Form2()  
        'Set the parent form of the child window.  
            NewMDIChild.MdiParent = Me  
        'Display the new form.  
            NewMDIChild.Show()  
    End Sub  
    ```  
  
    ```csharp  
    private void openToolStripMenuItem_Click(object sender, EventArgs e)  
    {  
        Form2 newMDIChild = new Form2();  
        // Set the parent form of the child window.  
            newMDIChild.MdiParent = this;  
        // Display the new form.  
            newMDIChild.Show();  
    }  
    ```  
  
12. <span data-ttu-id="b19fa-132">Поместите код, аналогичный приведенному в следующем примере, в `&Open`<xref:System.Windows.Forms.ToolStripMenuItem>, для регистрации обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="b19fa-132">Place code similar to the following code example in the `&Open`<xref:System.Windows.Forms.ToolStripMenuItem> to register the event handler.</span></span>  
  
    ```vb  
    Private Sub openToolStripMenuItem_Click(sender As Object, e As _  
    EventArgs) Handles openToolStripMenuItem.Click  
    ```  
  
    ```csharp  
    this.openToolStripMenuItem.Click += new _  
    System.EventHandler(this.openToolStripMenuItem_Click);  
    ```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="b19fa-133">Компиляция кода</span><span class="sxs-lookup"><span data-stu-id="b19fa-133">Compiling the Code</span></span>  
 <span data-ttu-id="b19fa-134">Для этого примера требуются:</span><span class="sxs-lookup"><span data-stu-id="b19fa-134">This example requires:</span></span>  
  
-   <span data-ttu-id="b19fa-135">два элемента управления <xref:System.Windows.Forms.Form> с именами `Form1` и `Form2`;</span><span class="sxs-lookup"><span data-stu-id="b19fa-135">Two <xref:System.Windows.Forms.Form> controls named `Form1` and `Form2`.</span></span>  
  
-   <span data-ttu-id="b19fa-136">элемент управления <xref:System.Windows.Forms.MenuStrip> на `Form1` с именем `menuStrip1` и элемент управления <xref:System.Windows.Forms.MenuStrip> на `Form2` с именем `menuStrip2`;</span><span class="sxs-lookup"><span data-stu-id="b19fa-136">A <xref:System.Windows.Forms.MenuStrip> control on `Form1` named `menuStrip1`, and a <xref:System.Windows.Forms.MenuStrip> control on `Form2` named `menuStrip2`.</span></span>  
  
-   <span data-ttu-id="b19fa-137">ссылки на сборки <xref:System?displayProperty=nameWithType> и <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="b19fa-137">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b19fa-138">См. также</span><span class="sxs-lookup"><span data-stu-id="b19fa-138">See Also</span></span>  
 [<span data-ttu-id="b19fa-139">Практическое руководство. Создание родительских MDI-форм</span><span class="sxs-lookup"><span data-stu-id="b19fa-139">How to: Create MDI Parent Forms</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-mdi-parent-forms.md)  
 [<span data-ttu-id="b19fa-140">Практическое руководство. Создание дочерних MDI-форм</span><span class="sxs-lookup"><span data-stu-id="b19fa-140">How to: Create MDI Child Forms</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-mdi-child-forms.md)  
 [<span data-ttu-id="b19fa-141">Общие сведения об элементе управления MenuStrip</span><span class="sxs-lookup"><span data-stu-id="b19fa-141">MenuStrip Control Overview</span></span>](../../../../docs/framework/winforms/controls/menustrip-control-overview-windows-forms.md)
