---
title: Технологии .NET Framework, недоступные в .NET Core
description: Узнайте о технологиях .NET Framework, недоступных в .NET Core
author: cartermp
ms.author: mairaw
ms.date: 12/07/2018
ms.openlocfilehash: be55cd1d1c67b0542c8474d1b2e47f6752f658a2
ms.sourcegitcommit: 462dc41a13942e467984e48f4018d1f79ae67346
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "58185809"
---
# <a name="net-framework-technologies-unavailable-on-net-core"></a>Технологии .NET Framework, недоступные в .NET Core

Некоторые технологии для библиотек .NET Framework недоступны для использования с .NET Core, например домены приложений, удаленное взаимодействие, управление доступом для кода (CAS) и прозрачность безопасности. Если в библиотеках применяются такие технологии, рассмотрите альтернативные подходы, описанные ниже. Дополнительные сведения о совместимости API см. в [списке изменений поведения и нарушений совместимости, а также нерекомендуемых и устаревших API-интерфейсов](https://github.com/dotnet/corefx/wiki/ApiCompat), представленном командой CoreFX на сайте GitHub.

Тот факт, что API или технология сейчас не реализуются, не означает, что они намеренно не поддерживаются. Сначала поищите .NET Core в репозиториях GitHub, чтобы узнать, не существует ли эта проблема намеренно. Если вы не можете ее найти, сообщите о проблеме в [проблемах репозитория dotnet/corefx](https://github.com/dotnet/corefx/issues) в GitHub, чтобы запросить определенные API и технологии. К [запросам на перенос кода на этой странице](https://github.com/dotnet/corefx/labels/port-to-core) добавляется метка `port-to-core`.

## <a name="appdomains"></a>Домены приложений

Домены приложений позволяют изолировать приложения друг от друга. Для этих доменов требуется поддержка среды выполнения и, как правило, они довольно дорого стоят. Создание дополнительных доменов приложений не поддерживается. И мы не планируем добавлять эту возможность в будущем. Вместо нее для изоляции кода мы рекомендуем использовать отдельные процессы или контейнеры. Для динамической загрузки сборок рекомендуется использовать новый класс <xref:System.Runtime.Loader.AssemblyLoadContext>.

Чтобы упростить перенос кода из .NET Framework, .NET Core предоставляет некоторые рабочие области API <xref:System.AppDomain>. Некоторые API-интерфейсы работают без изменений (например, <xref:System.AppDomain.UnhandledException?displayProperty=nameWithType>), одни элементы не выполняют никаких действий (например, <xref:System.AppDomain.SetCachePath%2A>), а другие создают исключение <xref:System.PlatformNotSupportedException> (например, <xref:System.AppDomain.CreateDomain%2A>). Просмотрите типы, используемые для [эталонного исходного кода `System.AppDomain`](https://github.com/dotnet/corefx/blob/master/src/Common/src/CoreLib/System/AppDomain.cs) в [репозитории DotNet и CoreFX на сайте GitHub](https://github.com/dotnet/corefx), и выберите ветвь, которая соответствует реализованной версии.

## <a name="remoting"></a>Удаленное взаимодействие

Архитектура удаленного взаимодействия .NET считается проблемной. Она используется для взаимодействия доменов приложений, которое больше не поддерживается. Кроме того, для удаленного взаимодействия требуется поддержка среды выполнения, обслуживание которой дорого обходится. Поэтому в .NET Core удаленное взаимодействие .NET не поддерживается, и его поддержка не планируется в будущем.

Для взаимодействия между процессами вместо удаленного взаимодействия можно применять механизмы межпроцессного взаимодействия (IPC), например пространство имен <xref:System.IO.Pipes> или класс <xref:System.IO.MemoryMappedFiles.MemoryMappedFile>.

Для взаимодействия между компьютерами в качестве альтернативы можно использовать сетевое решение, желательно протокол на основе обычного текста с низкими издержками, например HTTP. Еще один вариант — [веб-сервер Kestrel](https://docs.microsoft.com/aspnet/core/fundamentals/servers/kestrel), используемый платформой ASP.NET Core. Кроме того, для сценариев взаимодействия между компьютерами по сети можно использовать пространство имен <xref:System.Net.Sockets>. Другие варианты см. в разделе об обмене сообщениями статьи [.NET Open Source Developer Projects ](https://github.com/Microsoft/dotnet/blob/master/dotnet-developer-projects.md#messaging) (Проекты разработки с открытым кодом в .NET).

## <a name="code-access-security-cas"></a>CAS (Code Access Security — безопасность доступа кода)

Песочница ограничивает ресурсы, используемые или выполняемые в управляемых приложениях или библиотеках, на основе среды выполнения или платформы. Она [не поддерживается в .NET Framework](~/docs/framework/misc/code-access-security.md) и, следовательно, в .NET Core. Часто в .NET Framework и среде выполнения пользователи повышают привилегии, чтобы и дальше использовать CAS в качестве ограничения безопасности. Кроме того, механизм CAS усложняет реализацию и понижает производительность приложений, которые не планируется использовать.

Чтобы свести к минимуму требуемый набор прав, применяйте ограничения безопасности, предусмотренные в операционной системе, например виртуализацию, контейнеры или учетные записи пользователей.

## <a name="security-transparency"></a>Прозрачность безопасности

Аналогично CAS, прозрачность безопасности позволяет декларативно отделить изолированный код от кода, критически важного с точки зрения безопасности, но [больше не поддерживается как ограничение безопасности](~/docs/framework/misc/security-transparent-code.md). Эта функция часто используется в Silverlight. 

Чтобы свести к минимуму требуемый набор прав, применяйте ограничения безопасности, предусмотренные в операционной системе, например виртуализацию, контейнеры или учетные записи пользователей.

>[!div class="step-by-step"]
>[Вперед](third-party-deps.md)
