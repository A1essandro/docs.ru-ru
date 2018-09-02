---
title: Практическое руководство. Печать клиентской и неклиентской области формы (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- title bar [Visual Basic], printing
- printing
- borders [Visual Basic], printing
- entire form
- non-client area [Visual Basic], printing
ms.assetid: 856bb0e4-dbc3-47e2-81cd-4b376cf07757
ms.openlocfilehash: 5109993146a8d53d5cbeebcc52c018a6f0f57ed5
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2018
ms.locfileid: "43408443"
---
# <a name="how-to-print-client-and-non-client-areas-of-a-form-visual-basic"></a><span data-ttu-id="6d24a-102">Практическое руководство. Печать клиентской и неклиентской области формы (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6d24a-102">How to: Print Client and Non-Client Areas of a Form (Visual Basic)</span></span>
<span data-ttu-id="6d24a-103">Компонент <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> позволяет быстро напечатать изображение формы точно, как на экране, без использования компонента <xref:System.Drawing.Printing.PrintDocument> .</span><span class="sxs-lookup"><span data-stu-id="6d24a-103">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component enables you to quickly print an image of a form exactly as it appears on screen without using a <xref:System.Drawing.Printing.PrintDocument> component.</span></span> <span data-ttu-id="6d24a-104">Следующая процедура описывает печать формы, включая клиентскую и неклиентскую области.</span><span class="sxs-lookup"><span data-stu-id="6d24a-104">The following procedure shows how to print a form, including both the client area and the non-client area.</span></span> <span data-ttu-id="6d24a-105">Неклиентская область включает строку заголовка, границы и полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="6d24a-105">The non-client area includes the title bar, borders, and scroll bars.</span></span>  
  
 <span data-ttu-id="6d24a-106">Элементы управления PowerPack больше не включены в Visual Studio, но их можно скачать [центра загрузки](https://www.microsoft.com/en-us/download/details.aspx?id=25169).</span><span class="sxs-lookup"><span data-stu-id="6d24a-106">The PowerPack controls are no longer included in Visual Studio, but you can download them from the [Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=25169).</span></span>  
  
### <a name="to-print-both-the-client-and-the-non-client-areas-of-a-form"></a><span data-ttu-id="6d24a-107">Печать клиентской и неклиентской областей формы</span><span class="sxs-lookup"><span data-stu-id="6d24a-107">To print both the client and the non-client areas of a form</span></span>  
  
1.  <span data-ttu-id="6d24a-108">В **панели элементов**щелкните вкладку **Visual Basic PowerPacks** , а затем перетащите компонент <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> в форму.</span><span class="sxs-lookup"><span data-stu-id="6d24a-108">In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component onto the form.</span></span>  
  
     <span data-ttu-id="6d24a-109">Компонент <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> будет добавлен в область компонентов.</span><span class="sxs-lookup"><span data-stu-id="6d24a-109">The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component is added to the component tray.</span></span>  
  
2.  <span data-ttu-id="6d24a-110">В окне **Свойства** присвойте свойству <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> значение <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>.</span><span class="sxs-lookup"><span data-stu-id="6d24a-110">In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> property to <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>.</span></span>  
  
3.  <span data-ttu-id="6d24a-111">Добавьте следующий код в соответствующий обработчик событий (например, в обработчик событий `Click` для Print `Button`).</span><span class="sxs-lookup"><span data-stu-id="6d24a-111">Add the following code in the appropriate event handler (for example, in the `Click` event handler for a Print `Button`).</span></span>  
  
    ```  
    PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.FullWindow)  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="6d24a-112">В некоторых операционных системах текст или графика, нарисованная с использованием метода <xref:System.Drawing.Graphics> , могут быть напечатаны неправильно.</span><span class="sxs-lookup"><span data-stu-id="6d24a-112">On some operating systems, text or graphics drawn by <xref:System.Drawing.Graphics> methods may not print correctly.</span></span> <span data-ttu-id="6d24a-113">В этом случае используйте совместимый метод печати: `PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.CompatibleModeFullWindow`).</span><span class="sxs-lookup"><span data-stu-id="6d24a-113">In this case, use the compatible printing method: `PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.CompatibleModeFullWindow`).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d24a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="6d24a-114">See Also</span></span>  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A>  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.Print%2A>  
 [<span data-ttu-id="6d24a-115">Компонент PrintForm</span><span class="sxs-lookup"><span data-stu-id="6d24a-115">PrintForm Component</span></span>](../../../visual-basic/developing-apps/printing/printform-component.md)  
 [<span data-ttu-id="6d24a-116">Практическое руководство. Печать прокручиваемой формы</span><span class="sxs-lookup"><span data-stu-id="6d24a-116">How to: Print a Scrollable Form</span></span>](../../../visual-basic/developing-apps/printing/how-to-print-a-scrollable-form.md)
