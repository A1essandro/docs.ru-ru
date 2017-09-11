---
title: "Инструменты Visual Studio для Docker"
description: "Использование инструментов Visual Studio для Docker"
keywords: .NET, .NET Core, Docker, ASP.NET Core, Visual Studio
author: spboyer
ms.author: shboyer
ms.date: 04/27/2017
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-docker
ms.devlang: dotnet
ms.assetid: 1f3b9a68-4dea-4b60-8cb3-f46164eedbbf
ms.translationtype: HT
ms.sourcegitcommit: 318bf7a77748dfcee5f28243409d31e8d3e5c9ff
ms.openlocfilehash: 8e0fd8db2810c36358a7bcf94f4bc5e7d2aa399e
ms.contentlocale: ru-ru
ms.lasthandoff: 08/03/2017

---

# <a name="visual-studio-tools-for-docker"></a><span data-ttu-id="0a358-104">Инструменты Visual Studio для Docker</span><span class="sxs-lookup"><span data-stu-id="0a358-104">Visual Studio Tools for Docker</span></span>

<span data-ttu-id="0a358-105">[Microsoft Visual Studio 2017](https://www.visualstudio.com/) с [Docker для Windows](https://docs.docker.com/docker-for-windows/install/) поддерживает сборку, отладку и выполнение веб-приложений и консольных приложений .NET Framework и .NET Core с использованием контейнеров Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="0a358-105">[Microsoft Visual Studio 2017](https://www.visualstudio.com/) with [Docker for Windows](https://docs.docker.com/docker-for-windows/install/) supports building, debugging, and running .NET Framework and .NET Core web and console applications using Windows and Linux containers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0a358-106">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="0a358-106">Prerequisites</span></span>

- [<span data-ttu-id="0a358-107">Microsoft Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="0a358-107">Microsoft Visual Studio 2017</span></span>](https://www.visualstudio.com/)
- [<span data-ttu-id="0a358-108">Docker для Windows</span><span class="sxs-lookup"><span data-stu-id="0a358-108">Docker for Windows</span></span>](https://docs.docker.com/docker-for-windows/install/)

## <a name="installation-and-setup"></a><span data-ttu-id="0a358-109">Установка и настройка</span><span class="sxs-lookup"><span data-stu-id="0a358-109">Installation and setup</span></span>

<span data-ttu-id="0a358-110">Установите [Microsoft Visual Studio 2017](https://www.visualstudio.com/) с рабочей нагрузкой .NET Core.</span><span class="sxs-lookup"><span data-stu-id="0a358-110">Install [Microsoft Visual Studio 2017](https://www.visualstudio.com/) with the .NET Core workload.</span></span> <span data-ttu-id="0a358-111">Ознакомьтесь с разделом [Docker для Windows: что следует знать перед установкой](https://docs.docker.com/docker-for-windows/install/#what-to-know-before-you-install) и установите [Docker для Windows](https://docs.docker.com/docker-for-windows/install/).</span><span class="sxs-lookup"><span data-stu-id="0a358-111">Review the information at [Docker for Windows: What to know before you install](https://docs.docker.com/docker-for-windows/install/#what-to-know-before-you-install) and install [Docker For Windows](https://docs.docker.com/docker-for-windows/install/).</span></span>

<span data-ttu-id="0a358-112">Обязательная конфигурация Docker для Windows предполагает настройку **[общих дисков](https://docs.docker.com/docker-for-windows/#shared-drives)**.</span><span class="sxs-lookup"><span data-stu-id="0a358-112">A required configuration is to setup **[Shared Drives](https://docs.docker.com/docker-for-windows/#shared-drives)** in Docker for Windows.</span></span> <span data-ttu-id="0a358-113">Этот параметр необходим для поддержки сопоставления и отладки томов.</span><span class="sxs-lookup"><span data-stu-id="0a358-113">The setting is required for the volume mapping and debugging support.</span></span>

<span data-ttu-id="0a358-114">Щелкните правой кнопкой мыши значок Docker в области уведомлений, выберите пункт **Параметры**, а затем **Общие диски**.</span><span class="sxs-lookup"><span data-stu-id="0a358-114">Right click the Docker icon in the System Tray, click **Settings** and select **Shared Drives**.</span></span> <span data-ttu-id="0a358-115">Выберите диск, на котором Docker будет хранить файлы, и примените эти изменения.</span><span class="sxs-lookup"><span data-stu-id="0a358-115">Select the drive where Docker will store your files and apply changes.</span></span>

![Общие диски](./media/visual-studio-tools-for-docker/settings-shared-drives-win.png)

## <a name="create-an-aspnet-web-application-and-add-docker-support"></a><span data-ttu-id="0a358-117">Создание веб-приложения ASP.NET и добавление поддержки Docker</span><span class="sxs-lookup"><span data-stu-id="0a358-117">Create an ASP.NET Web Application and add Docker Support</span></span>

<span data-ttu-id="0a358-118">С помощью Visual Studio создайте веб-приложение ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="0a358-118">Using Visual Studio, create a new ASP.NET Core Web Application.</span></span> <span data-ttu-id="0a358-119">После загрузки приложения выберите пункт **Добавить поддержку Docker** в меню **Проект** или щелкните проект правой кнопкой мыши в обозревателе решений и выберите пункт **Добавить** > **Поддержка Docker**.</span><span class="sxs-lookup"><span data-stu-id="0a358-119">When the application is loaded, either select **Add Docker Support** from the **Project Menu** or right click the project from the Solution Explorer and select **Add** > **Docker Support**.</span></span>

<span data-ttu-id="0a358-120">Меню "Проект"</span><span class="sxs-lookup"><span data-stu-id="0a358-120">Project Menu</span></span>

!["Проект" > "Поддержка Docker"](./media/visual-studio-tools-for-docker/project-add-docker-support.png)

<span data-ttu-id="0a358-122">Контекстное меню проекта</span><span class="sxs-lookup"><span data-stu-id="0a358-122">Project Context Menu</span></span>

![Щелкните правой кнопкой мыши и выберите пункт "Добавить" > "Поддержка Docker".](./media/visual-studio-tools-for-docker/right-click-add-docker-support.png)

<span data-ttu-id="0a358-124">При добавлении в проект поддержки Docker можно выбрать контейнеры Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="0a358-124">When you add Docker support to your project, you can choose either Windows or Linux containers.</span></span> <span data-ttu-id="0a358-125">(Узел Docker должен работать на контейнерах такого же типа.</span><span class="sxs-lookup"><span data-stu-id="0a358-125">(The Docker host must be running the same container type.</span></span> <span data-ttu-id="0a358-126">Если вам нужно изменить тип контейнера для работающего экземпляра Docker, щелкните правой кнопкой мыши значок **Docker** в области уведомлений и выберите **Switch to Windows containers** (Переключить на контейнеры Windows) или **Switch to Linux containers** (Переключить на контейнеры Linux).</span><span class="sxs-lookup"><span data-stu-id="0a358-126">If you need change the container type in the running Docker instance, right click the **Docker** icon in the System Tray, and choose **Switch to Windows containers** or **Switch to Linux containers**.)</span></span> 

<span data-ttu-id="0a358-127">В проект будут добавлены указанные ниже файлы.</span><span class="sxs-lookup"><span data-stu-id="0a358-127">The following files are added to the project.</span></span>

- <span data-ttu-id="0a358-128">**Dockerfile**. Файл Docker для приложений ASP.NET Core основан на образе [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore).</span><span class="sxs-lookup"><span data-stu-id="0a358-128">**Dockerfile**: the Docker file for ASP.NET Core applications is based on the [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore) image.</span></span> <span data-ttu-id="0a358-129">Этот образ включает пакеты NuGet платформы ASP.NET Core, которые были предварительно скомпилированы JIT-компилятором для повышения производительности запуска.</span><span class="sxs-lookup"><span data-stu-id="0a358-129">This image includes the ASP.NET Core NuGet packages, which have been pre-jitted improving startup performance.</span></span> <span data-ttu-id="0a358-130">При создании консольных приложений .NET Core инструкция FROM в файле Dockerfile ссылается на самую последнюю версию образа [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet).</span><span class="sxs-lookup"><span data-stu-id="0a358-130">When building .NET Core Console Applications, the Dockerfile FROM will reference the most recent [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet) image.</span></span>   
- <span data-ttu-id="0a358-131">**docker-compose.yml**. Базовый файл Compose в Docker, который служит для определения коллекции образов, сборка и выполнение которых будут выполняться с помощью команд docker-compose build и run.</span><span class="sxs-lookup"><span data-stu-id="0a358-131">**docker-compose.yml**: base Docker Compose file used to define the collection of images to be built and run with docker-compose build/run.</span></span>   
- <span data-ttu-id="0a358-132">**docker-compose.dev.debug.yml**. Дополнительный файл docker-compose с итеративными изменениями, применяемыми в конфигурации отладки.</span><span class="sxs-lookup"><span data-stu-id="0a358-132">**docker-compose.dev.debug.yml**: additional docker-compose file with for iterative changes when your configuration is set to debug.</span></span> <span data-ttu-id="0a358-133">Для их объединения среда Visual Studio вызывает команду -f docker-compose.yml -f docker-compose.dev.debug.yml.</span><span class="sxs-lookup"><span data-stu-id="0a358-133">Visual Studio will call -f docker-compose.yml -f docker-compose.dev.debug.yml to merge these together.</span></span> <span data-ttu-id="0a358-134">Этот файл Compose используется средствами разработки Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0a358-134">This compose file is used by Visual Studio development tools.</span></span>   
- <span data-ttu-id="0a358-135">**docker-compose.dev.release.yml**. Дополнительный файл Compose в Docker для отладки определения выпуска.</span><span class="sxs-lookup"><span data-stu-id="0a358-135">**docker-compose.dev.release.yml**: additional Docker Compose file to debug your release definition.</span></span> <span data-ttu-id="0a358-136">Этот файл подключает отладчик к тому, чтобы он не менял содержимое рабочего образа.</span><span class="sxs-lookup"><span data-stu-id="0a358-136">It will volume mount the debugger so it doesn't change the contents of the production image.</span></span>  

<span data-ttu-id="0a358-137">Файл docker-compose.yml содержит имя образа, создаваемого при выполнении проекта.</span><span class="sxs-lookup"><span data-stu-id="0a358-137">The docker-compose.yml file contains the name of the image that is created when project is run.</span></span> 

```
version '2'

services:
  hellodockertools:
    image:  user/hellodockertools${TAG}
    build:
      context: .
      dockerfile: Dockerfile
    ports:
      - "80"
``` 

<span data-ttu-id="0a358-138">В этом примере `image: user/hellodockertools${TAG}` создает образ `user/hellodockertools:dev`, когда приложение выполняется в режиме **отладки**, и образ `user/hellodockertools:latest`, когда оно выполняется в режиме **выпуска**.</span><span class="sxs-lookup"><span data-stu-id="0a358-138">In this example, `image: user/hellodockertools${TAG}` generates the image `user/hellodockertools:dev` when the application is run in **Debug** mode and `user/hellodockertools:latest` in **Release** mode respectively.</span></span> 

<span data-ttu-id="0a358-139">Если вы планируете помещать образ в реестр, значение `user` необходимо изменить на имя пользователя Docker Hub.</span><span class="sxs-lookup"><span data-stu-id="0a358-139">You will want to change the `user` to your Docker Hub username if you plan to push the image to the registry.</span></span> <span data-ttu-id="0a358-140">Например, измените его на `spboyer/hellodockertools` или на URL-адрес своего закрытого реестра `privateregistry.domain.com/` в зависимости от конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0a358-140">For example, `spboyer/hellodockertools`, or change to your private registry url `privateregistry.domain.com/` depending on your configuration.</span></span>

### <a name="debugging"></a><span data-ttu-id="0a358-141">Отладка</span><span class="sxs-lookup"><span data-stu-id="0a358-141">Debugging</span></span>

<span data-ttu-id="0a358-142">Выберите пункт **Docker** в раскрывающемся списке отладки на панели инструментов и нажмите клавишу F5, чтобы начать отладку приложения.</span><span class="sxs-lookup"><span data-stu-id="0a358-142">Select **Docker** from the debug dropdown in the toolbar and use F5 to start debugging the application.</span></span> 

- <span data-ttu-id="0a358-143">Будет получен образ microsoft/aspnetcore (если его еще нет в вашем кэше).</span><span class="sxs-lookup"><span data-stu-id="0a358-143">The microsoft/aspnetcore image is acquired (if not already in your cache)</span></span>
- <span data-ttu-id="0a358-144">Переменной ASPNETCORE_ENVIRONMENT в контейнере будет присвоено значение Development.</span><span class="sxs-lookup"><span data-stu-id="0a358-144">ASPNETCORE_ENVIRONMENT is set to Development within the container</span></span>
- <span data-ttu-id="0a358-145">Порт 80 будет открыт и сопоставлен с динамически назначаемым портом для localhost.</span><span class="sxs-lookup"><span data-stu-id="0a358-145">PORT 80 is EXPOSED and mapped to a dynamically assigned port for localhost.</span></span> <span data-ttu-id="0a358-146">Порт определяется узлом Docker и может запрашиваться с помощью команды docker ps.</span><span class="sxs-lookup"><span data-stu-id="0a358-146">The port is determined by the docker host and can be queried with docker ps.</span></span> 
- <span data-ttu-id="0a358-147">Приложение будет скопировано в контейнер.</span><span class="sxs-lookup"><span data-stu-id="0a358-147">Your application is copied to the container</span></span>
- <span data-ttu-id="0a358-148">Браузер по умолчанию запустится с подключенным к контейнеру отладчиком с использованием динамически назначаемого порта.</span><span class="sxs-lookup"><span data-stu-id="0a358-148">Default browser is launched with the debugger attached to the container, using the dynamically assigned port.</span></span> 

<span data-ttu-id="0a358-149">В результате сборки образа Docker будет получен образ `dev` приложения с образами `microsoft/aspnetcore` в качестве базового образа.</span><span class="sxs-lookup"><span data-stu-id="0a358-149">The resulting Docker image built is the `dev` image of your application with the `microsoft/aspnetcore` images as the base image.</span></span>
<span data-ttu-id="0a358-150">Примечание. В образе dev нет содержимого приложения, так как конфигурации отладки используют подключение тома для обеспечения итеративности процесса.</span><span class="sxs-lookup"><span data-stu-id="0a358-150">Note: the dev image is empty of your app contents as Debug confgurations use volume mounting to provide the iterative experience.</span></span> <span data-ttu-id="0a358-151">Чтобы отправить образ, используйте конфигурацию выпуска.</span><span class="sxs-lookup"><span data-stu-id="0a358-151">To push an image, use the Release configuration.</span></span>

```console
REPOSITORY                  TAG         IMAGE ID            CREATED         SIZE
spboyer/hellodockertools    dev         0b6e2e44b3df        4 minutes ago   268.9 MB
microsoft/aspnetcore        1.0.1       189ad4312ce7        5 days ago      268.9 MB
```

<span data-ttu-id="0a358-152">Приложение выполняется с помощью контейнера, который можно увидеть, выполнив команду `docker ps`.</span><span class="sxs-lookup"><span data-stu-id="0a358-152">The application is running using the container which you can see by running the `docker ps` command.</span></span>

```console
CONTAINER ID        IMAGE                          COMMAND               CREATED             STATUS              PORTS                   NAMES
3f240cf686c9        spboyer/hellodockertools:dev   "tail -f /dev/null"   4 minutes ago       Up 4 minutes        0.0.0.0:32769->80/tcp   hellodockertools_hellodockertools_1
```

### <a name="edit-and-continue"></a><span data-ttu-id="0a358-153">Изменить и продолжить</span><span class="sxs-lookup"><span data-stu-id="0a358-153">Edit and Continue</span></span>

<span data-ttu-id="0a358-154">Изменения статических полей и файлов шаблонов Razor (CSHTML) применяются автоматически без необходимости выполнять этап компиляции.</span><span class="sxs-lookup"><span data-stu-id="0a358-154">Changes to static files and/or razor template files (.cshtml) are automatically updated without the need of a compilation step.</span></span> <span data-ttu-id="0a358-155">Внесите изменение, сохраните его и нажмите кнопку "Обновить" в браузере, чтобы увидеть обновление.</span><span class="sxs-lookup"><span data-stu-id="0a358-155">Make the change, save and tap refresh in the browser to view the update.</span></span>  

<span data-ttu-id="0a358-156">Для внесения изменений в файлы кода требуются компиляция и перезапуск Kestrel в контейнере.</span><span class="sxs-lookup"><span data-stu-id="0a358-156">Modifications to code files require compiling and a restart of Kestrel within the container.</span></span> <span data-ttu-id="0a358-157">После внесения изменения нажмите клавиши CTRL+F5, чтобы выполнить процесс и запустить приложение без контейнера.</span><span class="sxs-lookup"><span data-stu-id="0a358-157">After making the change, use CTRL + F5 to perform the process and start the application within the container.</span></span> <span data-ttu-id="0a358-158">Повторная сборка или остановка контейнера Docker не производится. Выполнив команду `docker ps` в командной строке, можно увидеть, что исходный контейнер по-прежнему выполняется, как и 10 минут назад.</span><span class="sxs-lookup"><span data-stu-id="0a358-158">The Docker container is not rebuilt or stopped; using `docker ps` in the command line you can see that the original container is still running as of 10 minutes ago.</span></span> 

```console
CONTAINER ID        IMAGE                          COMMAND               CREATED             STATUS              PORTS                   NAMES
3f240cf686c9        spboyer/hellodockertools:dev   "tail -f /dev/null"   10 minutes ago      Up 10 minutes       0.0.0.0:32769->80/tcp   hellodockertools_hellodockertools_1
```

### <a name="publishing-docker-images"></a><span data-ttu-id="0a358-159">Публикация образов Docker</span><span class="sxs-lookup"><span data-stu-id="0a358-159">Publishing Docker images</span></span>

<span data-ttu-id="0a358-160">После завершения цикла разработки и отладки приложения инструменты Visual Studio для Docker помогут вам создать рабочий образ приложения.</span><span class="sxs-lookup"><span data-stu-id="0a358-160">Once you have completed the develop and debug cycle of your application, the Visual Studio Tools for Docker will help you create the production image of your application.</span></span> <span data-ttu-id="0a358-161">Выберите в раскрывающемся списке отладки значение **Выпуск** и выполните сборку приложения.</span><span class="sxs-lookup"><span data-stu-id="0a358-161">Change the debug dropdown to **Release** and build the application.</span></span> <span data-ttu-id="0a358-162">Инструментарий создаст образ с тегом `:latest`, который можно отправить в закрытый реестр или в Docker Hub.</span><span class="sxs-lookup"><span data-stu-id="0a358-162">The tooling will produce the image with the `:latest` tag which you can push to your private registry or Docker Hub.</span></span> 

<span data-ttu-id="0a358-163">С помощью команды `docker images` можно получить список образов.</span><span class="sxs-lookup"><span data-stu-id="0a358-163">Using the `docker images` you can see the list of images.</span></span>

```console
REPOSITORY                 TAG                 IMAGE ID            CREATED             SIZE
spboyer/hellodockertools   latest              8184ae38ba91        5 seconds ago       278.4 MB
spboyer/hellodockertools   dev                 0b6e2e44b3df        About an hour ago   268.9 MB
microsoft/aspnetcore       1.0.1               189ad4312ce7        5 days ago          268.9 MB
```

<span data-ttu-id="0a358-164">Вы могли ожидать, что рабочий образ или образ выпуска будет иметь меньший размер, чем образ **dev**. Однако из-за использования сопоставления томов отладчик и приложение на самом деле выполнялись с локального компьютера, а не в контейнере.</span><span class="sxs-lookup"><span data-stu-id="0a358-164">There may be an expectation for the production or release image to be smaller in size by comparison to the **dev** image, however through the use of the volume mapping; the debugger and application were actually being run from your local machine and not within the container.</span></span> <span data-ttu-id="0a358-165">В образ **latest** был упакован весь код приложения, необходимый для его выполнения на компьютере узла, поэтому эта разница соответствует размеру кода приложения.</span><span class="sxs-lookup"><span data-stu-id="0a358-165">The **latest** image has packaged the entire application code needed to run the application on a host machine, therefore the delta is the size of your application code.</span></span>

