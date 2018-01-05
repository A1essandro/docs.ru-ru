---
title: "Практическое руководство. Инициирование воспроизведение мультимедиа с помощью пользовательского события"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- synchronizing media playback with events [WPF]
- playback of media [WPF], synchronizing with events
- media [WPF], synchronizing playback with events
- multimedia [WPF], synchronizing media playback with events
ms.assetid: c4dbe632-6e7f-4d7f-9df5-98737a758bc3
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: aa93b757f0af38bc6b08d87ac5485e2bf0f45a1c
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-trigger-media-playback-with-a-user-event"></a><span data-ttu-id="b33e3-102">Практическое руководство. Инициирование воспроизведение мультимедиа с помощью пользовательского события</span><span class="sxs-lookup"><span data-stu-id="b33e3-102">How to: Trigger Media Playback with a User Event</span></span>
<span data-ttu-id="b33e3-103">В этом примере показано, как синхронизировать воспроизведение мультимедиа с событием.</span><span class="sxs-lookup"><span data-stu-id="b33e3-103">This example shows how to synchronize media playback with an event.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b33e3-104">Пример</span><span class="sxs-lookup"><span data-stu-id="b33e3-104">Example</span></span>  
 <span data-ttu-id="b33e3-105">В следующем примере используется <xref:System.Windows.Controls.MediaElement> управления и <xref:System.Windows.Media.MediaTimeline> класса для воспроизведения звука, которая возникает, когда пользователь нажимает кнопку <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="b33e3-105">The following example uses the <xref:System.Windows.Controls.MediaElement> control and the <xref:System.Windows.Media.MediaTimeline> class to play a sound that occurs when the user clicks a <xref:System.Windows.Controls.Button>.</span></span>  
  
 [!code-xaml[MediaGallery_snippet#SoundFromUserEventExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snippet/CSharp/SoundFromUserEventExample.xaml#soundfromusereventexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="b33e3-106">См. также</span><span class="sxs-lookup"><span data-stu-id="b33e3-106">See Also</span></span>  
 <xref:System.Windows.Controls.MediaElement>  
 <xref:System.Windows.Media.MediaTimeline>  
 <xref:System.Windows.EventTrigger.RoutedEvent%2A>  
 <xref:System.Windows.Media.Animation.Storyboard>  
 [<span data-ttu-id="b33e3-107">Разделы практического руководства</span><span class="sxs-lookup"><span data-stu-id="b33e3-107">How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/audio-and-video-how-to-topics.md)  
 [<span data-ttu-id="b33e3-108">Графика и мультимедиа</span><span class="sxs-lookup"><span data-stu-id="b33e3-108">Graphics and Multimedia</span></span>](../../../../docs/framework/wpf/graphics-multimedia/index.md)
