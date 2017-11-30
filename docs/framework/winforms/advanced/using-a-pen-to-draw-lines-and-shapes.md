---
title: "Рисование линий и фигур с помощью пера"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- pens
- examples [Windows Forms], drawing lines and shapes
- examples [Windows Forms], pens
- drawing
ms.assetid: 8a7542ab-3e9e-443f-8405-2d6053528e20
caps.latest.revision: "14"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 0913dc2745e1b244e4b03c0e6b946441a401c5b1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="38639-102">Рисование линий и фигур с помощью пера</span><span class="sxs-lookup"><span data-stu-id="38639-102">Using a Pen to Draw Lines and Shapes</span></span>
<span data-ttu-id="38639-103">Используйте [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] `Pen` объектов для рисования линейных сегментов, кривых и контуров фигур.</span><span class="sxs-lookup"><span data-stu-id="38639-103">Use [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] `Pen` objects to draw line segments, curves, and the outlines of shapes.</span></span> <span data-ttu-id="38639-104">В этом разделе *строки* ссылается на любой из них, если не указано означает сегмент линии.</span><span class="sxs-lookup"><span data-stu-id="38639-104">In this section, *line* refers to any of these, unless specified to mean only a line segment.</span></span> <span data-ttu-id="38639-105">Настройка параметров пера для управления цвет, ширину, выравнивание и стиль линий, нарисованных при помощи этого пера.</span><span class="sxs-lookup"><span data-stu-id="38639-105">Set the properties of a pen to control the color, width, alignment, and style of lines drawn with that pen.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="38639-106">Содержание</span><span class="sxs-lookup"><span data-stu-id="38639-106">In This Section</span></span>  
 [<span data-ttu-id="38639-107">Практическое руководство. Рисование линий с помощью пера</span><span class="sxs-lookup"><span data-stu-id="38639-107">How to: Use a Pen to Draw Lines</span></span>](../../../../docs/framework/winforms/advanced/how-to-use-a-pen-to-draw-lines.md)  
 <span data-ttu-id="38639-108">Описываются способы рисования линий.</span><span class="sxs-lookup"><span data-stu-id="38639-108">Explains how to draw lines.</span></span>  
  
 [<span data-ttu-id="38639-109">Практическое руководство. Рисование прямоугольников с помощью пера</span><span class="sxs-lookup"><span data-stu-id="38639-109">How to: Use a Pen to Draw Rectangles</span></span>](../../../../docs/framework/winforms/advanced/how-to-use-a-pen-to-draw-rectangles.md)  
 <span data-ttu-id="38639-110">Описывает, как Рисование прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="38639-110">Describes how to draw rectangles.</span></span>  
  
 [<span data-ttu-id="38639-111">Практическое руководство. Задание толщины и выравнивания пера</span><span class="sxs-lookup"><span data-stu-id="38639-111">How to: Set Pen Width and Alignment</span></span>](../../../../docs/framework/winforms/advanced/how-to-set-pen-width-and-alignment.md)  
 <span data-ttu-id="38639-112">Объясняется, как изменить ширину и выравнивание `Pen` объекта.</span><span class="sxs-lookup"><span data-stu-id="38639-112">Explains how to change the width and alignment of a `Pen` object.</span></span>  
  
 [<span data-ttu-id="38639-113">Практическое руководство. Рисование линий с наконечниками</span><span class="sxs-lookup"><span data-stu-id="38639-113">How to: Draw a Line with Line Caps</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-a-line-with-line-caps.md)  
 <span data-ttu-id="38639-114">Описывает добавление оконечных линиям.</span><span class="sxs-lookup"><span data-stu-id="38639-114">Describes how to add end caps when drawing a line.</span></span>  
  
 [<span data-ttu-id="38639-115">Практическое руководство. Соединение линий</span><span class="sxs-lookup"><span data-stu-id="38639-115">How to: Join Lines</span></span>](../../../../docs/framework/winforms/advanced/how-to-join-lines.md)  
 <span data-ttu-id="38639-116">Показано, как соединить две строки.</span><span class="sxs-lookup"><span data-stu-id="38639-116">Shows how to join two lines.</span></span>  
  
 [<span data-ttu-id="38639-117">Практическое руководство. Рисование пользовательских пунктирных линий</span><span class="sxs-lookup"><span data-stu-id="38639-117">How to: Draw a Custom Dashed Line</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-a-custom-dashed-line.md)  
 <span data-ttu-id="38639-118">Описывает способ рисования пунктирной линией.</span><span class="sxs-lookup"><span data-stu-id="38639-118">Describes how to draw a dashed line.</span></span>  
  
 [<span data-ttu-id="38639-119">Практическое руководство. Рисование линии с текстурным заполнением</span><span class="sxs-lookup"><span data-stu-id="38639-119">How to: Draw a Line Filled with a Texture</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-a-line-filled-with-a-texture.md)  
 <span data-ttu-id="38639-120">Объясняет, как рисование линии с текстурным заполнением.</span><span class="sxs-lookup"><span data-stu-id="38639-120">Explains how to draw a texture-filled line.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="38639-121">Ссылка</span><span class="sxs-lookup"><span data-stu-id="38639-121">Reference</span></span>  
 <xref:System.Drawing.Pen>  
 <span data-ttu-id="38639-122">Описание класса и ссылки на все его члены.</span><span class="sxs-lookup"><span data-stu-id="38639-122">Describes this class and has links to all its members.</span></span>
