---
title: Организация проектов для .NET Framework и .NET Core
description: Эта статья поможет владельцам проектов, которые хотят скомпилировать свое решение одновременно для .NET Framework и .NET Core.
author: conniey
ms.date: 12/07/2018
ms.custom: seodec18
ms.openlocfilehash: ab484ccc2c5b51b2ee1dca57df51669d288f3e6b
ms.sourcegitcommit: 462dc41a13942e467984e48f4018d1f79ae67346
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "58186069"
---
# <a name="organize-your-project-to-support-both-net-framework-and-net-core"></a>Организация проекта для параллельной поддержки .NET Framework и .NET Core

Узнайте, как создать решение, которое выполняет параллельную сборку для .NET Framework и .NET Core. Изучите несколько вариантов организации проектов, которые могут помочь вам достичь этой цели. Ниже приводится несколько типичных сценариев, которые следует принять во внимание при выборе способа компоновки проекта с помощью .NET Core. Этот список может охватывать не все необходимые случаи. Устанавливайте приоритеты в зависимости от потребностей вашего проекта.

* [**Объединение существующих проектов и проектов .NET Core в единые проекты**](#replace-existing-projects-with-a-multi-targeted-net-core-project)

  *Преимущества*
  * Упрощение процесса сборки благодаря компиляции одного, а не нескольких проектов, каждый из которых предназначен для отдельной версии .NET Framework или платформы.
  * Упрощение управления файлами исходного кода для проектов, предназначенных для различных платформ, благодаря тому, что вам приходится управлять только одним файлом проекта. При использовании альтернативных подходов добавление и удаление файлов исходного кода требует синхронизации этих изменений с другими проектами вручную.
  * Простое создание пакета NuGet для использования.
  * Позволяет писать код для конкретной версии .NET Framework в библиотеках посредством директив компилятора.

  *Неподдерживаемые сценарии*
  * Для открытия существующих проектов разработчики должны использовать Visual Studio 2017. Для поддержки предыдущих версий Visual Studio лучше [хранить файлы проектов в разных папках](#support-vs).

* <a name="support-vs"></a>[**Разделение существующих и новых проектов .NET Core**](#keep-existing-projects-and-create-a-net-core-project)

  *Преимущества*
  * Продолжение работы над существующими проектами для разработчиков и участников, у которых нет Visual Studio 2017.
  * Снижение вероятности появления новых ошибок в существующих проектах, так как не требуется обработка кода.

## <a name="example"></a>Пример

Рассмотрим показанный ниже репозиторий.

![Существующий проект](./media/project-structure/existing-project-structure.png)

[**Исходный код**](https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library/)

В зависимости от ограничений и сложности существующих проектов добавить поддержку .NET Core для этого репозитория можно несколькими способами, которые описаны ниже.

## <a name="replace-existing-projects-with-a-multi-targeted-net-core-project"></a>Замена существующих проектов на проект .NET Core, предназначенный для нескольких платформ

Измените файлы в репозитории, удалив все существующие файлы *\*.csproj* и создав единственный файл *\*.csproj*, предназначенный для нескольких платформ. Это удобно по той причине, что один проект можно компилировать для разных платформ. Это также позволяет управлять различными параметрами компиляции и зависимостями для каждой целевой платформы.

![Создание файла CSPROJ, предназначенного для нескольких платформ](./media/project-structure/multi-targeted-project.png)

[**Исходный код**](https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library-csproj/)

Обратите внимание на следующие изменения:

* Замена файлов *packages.config* и *\*.csproj* на новый файл [.NET Core*\*.csproj*](https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library-csproj/src/Car/Car.csproj). Пакеты NuGet указываются с помощью `<PackageReference> ItemGroup`.

## <a name="keep-existing-projects-and-create-a-net-core-project"></a>Сохранение существующих проектов и создание проекта .NET Core

При наличии существующих проектов, предназначенных для более старых платформ, можно оставить эти проекты без изменения и использовать проект .NET Core для новых платформ.

![Проект .NET Core с существующим проектом в другой папке](./media/project-structure/separate-projects-same-source.png)

[**Исходный код**](https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library-csproj-keep-existing/)

Обратите внимание на следующие изменения:

* Проект .NET Core и существующие проекты хранятся в разных папках.
  * Размещение проектов в разных папках позволяет обойтись без Visual Studio 2017. Вы можете создать отдельное решение, которое открывает только старые проекты.

## <a name="see-also"></a>См. также

Дополнительные указания по переходу на .NET Core см. в [документации по переходу на .NET Core](index.md).
