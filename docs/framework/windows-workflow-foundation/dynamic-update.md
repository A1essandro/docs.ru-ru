---
title: Динамическое обновление
ms.date: 03/30/2017
ms.assetid: 8b6ef19b-9691-4b4b-824c-3c651a9db96e
ms.openlocfilehash: e28a34e500034eec6cf250d94cf7631ca85a7d40
ms.sourcegitcommit: 15ab532fd5e1f8073a4b678922d93b68b521bfa0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653890"
---
# <a name="dynamic-update"></a>Динамическое обновление

Динамическое обновление предоставляет разработчикам приложений рабочих процессов механизм обновления определения рабочего процесса для сохраненного экземпляра рабочего процесса. Это позволяет реализовать исправление ошибки, внедрить новые требования и внести непредвиденные изменения. В этом разделе приведены общие сведения о функциях динамического обновления, введенных в [!INCLUDE[net_v45](../../../includes/net-v45-md.md)].

## <a name="dynamic-update"></a>Динамическое обновление

Для применения динамического обновления к сохраненному экземпляру рабочего процесса создается схема <xref:System.Activities.DynamicUpdate.DynamicUpdateMap>, которая содержит инструкции времени выполнения, описывающие, как следует изменить сохраненный экземпляр рабочего процесса, чтобы он отражал требуемые изменения. После создания схема обновления применяется к выбранным экземплярам рабочего процесса. Сразу после применения динамического обновления экземпляр рабочего процесса может быть возобновлен уже с новыми, обновленными определениями рабочего процесса. Создание и применение схемы обновления происходит в четыре этапа.

1. [Подготовка определения рабочего процесса для динамического обновления](dynamic-update.md#Prepare)

2. [Обновление определения рабочего процесса для отражения требуемых изменений](dynamic-update.md#Update)

3. [Создание схемы обновления](dynamic-update.md#Create)

4. [Применение схемы обновления к требуемой сохраненные экземпляры рабочих процессов](dynamic-update.md#Apply)

> [!NOTE]
> Обратите внимание, что шаги 1–3, которые охватывают создание схемы обновления, могут быть выполнены независимо от применения обновления. Распространенный сценарий, что разработчик рабочего процесса будет создавать сопоставление обновления в автономном режиме, и затем администратор применяет обновление позже.

В этом разделе приведены общие сведения о процессе динамического обновления с добавлением нового действия, которое добавляется к сохраненному экземпляру скомпилированного рабочего процесса языка XAML.

### <a name="Prepare"></a> Подготовка определения рабочего процесса для динамического обновления

Первый шаг в процессе динамического обновления - подготовка требуемого определения рабочего процесса к обновлению. Это можно сделать, вызвав метод <xref:System.Activities.DynamicUpdate.DynamicUpdateServices.PrepareForUpdate%2A?displayProperty=nameWithType> и передав ему определение изменяемого рабочего процесса . Этот метод проверяет, а затем обходит дерево рабочего процесса для определения всех объектов, таких как открытые переменные и действия, которые необходимо отметить тегами для сравнения в дальнейшем с объектами в измененном определении рабочего процесса. По завершении этой операции дерево рабочего процесса клонируется и присоединяется к исходному определению рабочего процесса. При создании схемы обновленная версия определения рабочего процесса сравнивается с исходным определением рабочего процесса и схема создается на основе различий между ними.

Чтобы подготовить рабочий процесс языка XAML для динамического обновления, его можно загрузить в <xref:System.Activities.ActivityBuilder>, а затем передать <xref:System.Activities.ActivityBuilder> в <xref:System.Activities.DynamicUpdate.DynamicUpdateServices.PrepareForUpdate%2A?displayProperty=nameWithType>.

> [!NOTE]
> Дополнительные сведения о работе с сериализованными рабочими процессами и <xref:System.Activities.ActivityBuilder>, см. в разделе [сериализация рабочих процессов и действий в и из XAML](serializing-workflows-and-activities-to-and-from-xaml.md).

В следующем примере определение `MortgageWorkflow` (состоящее из <xref:System.Activities.Statements.Sequence> с несколькими дочерними действиями) загружается в <xref:System.Activities.ActivityBuilder>, а затем подготавливается для динамического обновления. После возврата из метода <xref:System.Activities.ActivityBuilder> содержит исходное определение рабочего процесса и копию.

```csharp
// Load the MortgageWorkflow definition from Xaml into
// an ActivityBuilder.
XamlXmlReaderSettings readerSettings = new XamlXmlReaderSettings()
{
    LocalAssembly = Assembly.GetExecutingAssembly()
};

XamlXmlReader xamlReader = new XamlXmlReader(@"C:\WorkflowDefinitions\MortgageWorkflow.xaml",
    readerSettings);

ActivityBuilder ab = XamlServices.Load(
    ActivityXamlServices.CreateBuilderReader(xamlReader)) as ActivityBuilder;

// Prepare the workflow definition for dynamic update.
DynamicUpdateServices.PrepareForUpdate(ab);
```

> [!NOTE]
> Чтобы загрузить пример кода, используемый в этом разделе, см. в разделе [пример кода динамического обновления](https://go.microsoft.com/fwlink/?LinkId=227905).

### <a name="Update"></a> Обновление определения рабочего процесса для отражения требуемых изменений

После того как определение рабочего процесса будет подготовлено к изменениям, можно внести необходимые желаемые изменения. Вы можете добавлять или удалять действия, добавлять, изменять или удалять открытые переменные, добавлять или удалять аргументы и вносить изменения в сигнатуру делегатов действий. Нельзя удалить выполняемое действие или изменить сигнатуру выполняемого делегата. Эти изменения можно внести из кода или в повторно размещенном конструкторе рабочих процессов. В следующем примере настраиваемое действие `VerifyAppraisal` добавляется в последовательность, представляющую основу `MortgageWorkflow` из предыдущего примера.

```csharp
// Make desired changes to the definition. In this example, we are
// inserting a new VerifyAppraisal activity as the 3rd child of the root Sequence.
VerifyAppraisal va = new VerifyAppraisal
{
    Result = new VisualBasicReference<bool>("LoanCriteria")
};

// Get the Sequence that makes up the body of the workflow.
Sequence s = ab.Implementation as Sequence;

// Insert the new activity into the Sequence.
s.Activities.Insert(2, va);
```

### <a name="Create"></a> Создание схемы обновления

После изменения подготовленного к обновлению определения рабочего процесса можно создать схему обновления. Для создания схемы динамического обновления вызывается метод <xref:System.Activities.DynamicUpdate.DynamicUpdateServices.CreateUpdateMap%2A?displayProperty=nameWithType>. Этот метод возвращает <xref:System.Activities.DynamicUpdate.DynamicUpdateMap> - объект, содержащий сведения, необходимые среде выполнения для изменения сохраненного экземпляра рабочего процесса, чтобы тот можно было загрузить и возобновить вместе с новым определением рабочего процесса. В следующем примере создается динамическая схема для измененного определения `MortgageWorkflow` из предыдущего примера.

```csharp
// Create the update map.
DynamicUpdateMap map = DynamicUpdateServices.CreateUpdateMap(ab);
```

Эту схему обновления можно сразу же использовать для изменения сохраненных экземпляров рабочего процесса или сохранить ее и применить обновления позже. Один из способов сохранить схему обновления - это сериализовать ее в файл, как показано в следующем примере.

```csharp
// Serialize the update map to a file.
DataContractSerializer serializer = new DataContractSerializer(typeof(DynamicUpdateMap));
using (FileStream fs = System.IO.File.Open(@"C:\WorkflowDefinitions\MortgageWorkflow.map", FileMode.Create))
{
    serializer.WriteObject(fs, map);
}
```

Когда <xref:System.Activities.DynamicUpdate.DynamicUpdateServices.CreateUpdateMap%2A?displayProperty=nameWithType> возвращает управление, скопированное определение рабочего процесса и другая информация о динамическом обновлении, добавленная при вызове <xref:System.Activities.DynamicUpdate.DynamicUpdateServices.PrepareForUpdate%2A?displayProperty=nameWithType>, удаляются, а измененное определение рабочего процесса готово к сохранению, после чего его можно будет использовать при восстановлении обновленных экземпляров рабочего процесса. В следующем примере определение измененного рабочего процесса сохраняется в `MortgageWorkflow_v1.1.xaml`.

```csharp
// Save the modified workflow definition.
StreamWriter sw = File.CreateText(@"C:\WorkflowDefinitions\MortgageWorkflow_v1.1.xaml");
XamlWriter xw = ActivityXamlServices.CreateBuilderWriter(new XamlXmlWriter(sw, new XamlSchemaContext()));
XamlServices.Save(xw, ab);
sw.Close();
```

### <a name="Apply"></a> Применение схемы обновления к требуемой сохраненные экземпляры рабочих процессов

Применение схемы обновления можно выполнить в любое время после ее создания. Это можно сделать немедленно с помощью экземпляра <xref:System.Activities.DynamicUpdate.DynamicUpdateMap>, который был возвращен методом <xref:System.Activities.DynamicUpdate.DynamicUpdateServices.CreateUpdateMap%2A?displayProperty=nameWithType>, или позднее с помощью сохраненной копии схемы обновления. Для обновления экземпляра рабочего процесса загрузите его в объект <xref:System.Activities.WorkflowApplicationInstance> с помощью метода <xref:System.Activities.WorkflowApplication.GetInstance%2A?displayProperty=nameWithType>. Далее создайте <xref:System.Activities.WorkflowApplication> с помощью обновленного определения рабочего процесса и нужного метода <xref:System.Activities.WorkflowIdentity>. Этот идентификатор <xref:System.Activities.WorkflowIdentity> может отличаться от того, что был использован для сохранения исходного рабочего процесса, и, как правило, это делается для отражения того, что сохраненный экземпляр был изменен. Сразу после создания <xref:System.Activities.WorkflowApplication> загружается с помощью перегрузки <xref:System.Activities.WorkflowApplication.Load%2A?displayProperty=nameWithType>, принимающей <xref:System.Activities.DynamicUpdate.DynamicUpdateMap>, затем выгружается посредством вызова <xref:System.Activities.WorkflowApplication.Unload%2A?displayProperty=nameWithType>. При этом будет произведено динамическое обновление и обновленный экземпляр рабочего процесса будет сохранен.

```csharp
// Load the serialized update map.
DynamicUpdateMap map;
using (FileStream fs = File.Open(@"C:\WorkflowDefinitions\MortgageWorkflow.map", FileMode.Open))
{
    DataContractSerializer serializer = new DataContractSerializer(typeof(DynamicUpdateMap));
    object updateMap = serializer.ReadObject(fs);
    if (updateMap == null)
    {
        throw new ApplicationException("DynamicUpdateMap is null.");
    }

    map = (DynamicUpdateMap)updateMap;
}

// Retrieve a list of workflow instance ids that corresponds to the
// workflow instances to update. This step is the responsibility of
// the application developer.
List<Guid> ids = GetPersistedWorkflowIds();
foreach (Guid id in ids)
{
    // Get a proxy to the persisted workflow instance.
    SqlWorkflowInstanceStore store = new SqlWorkflowInstanceStore(connectionString);
    WorkflowApplicationInstance instance = WorkflowApplication.GetInstance(id, store);

    // If desired, you can inspect the WorkflowIdentity of the instance
    // using the DefinitionIdentity property to determine whether to apply
    // the update.
    Console.WriteLine(instance.DefinitionIdentity);

    // Create a workflow application. You must specify the updated workflow definition, and
    // you may provide an updated WorkflowIdentity if desired to reflect the update.
    WorkflowIdentity identity = new WorkflowIdentity
    {
        Name = "MortgageWorkflow v1.1",
        Version = new Version(1, 1, 0, 0)
    };

    // Load the persisted workflow instance using the updated workflow definition
    // and with an updated WorkflowIdentity. In this example the MortgageWorkflow class
    // contains the updated definition.
    WorkflowApplication wfApp = new WorkflowApplication(new MortgageWorkflow(), identity);

    // Apply the dynamic update on the loaded instance.
    wfApp.Load(instance, map);

    // Unload the updated instance.
    wfApp.Unload();
}
```

### <a name="resuming-an-updated-workflow-instance"></a>Возобновление работы обновленного экземпляра рабочего процесса

Сразу после применения динамического обновления можно возобновлять работу экземпляра рабочего процесса. Обратите внимание, что следует использовать новое обновленное определение и <xref:System.Activities.WorkflowIdentity>.

> [!NOTE]
> Дополнительные сведения о работе с <xref:System.Activities.WorkflowApplication> и <xref:System.Activities.WorkflowIdentity>, см. в разделе [с помощью WorkflowIdentity и управления версиями](using-workflowidentity-and-versioning.md).

В следующем примере рабочий процесс `MortgageWorkflow_v1.1.xaml` из предыдущего примера был скомпилирован, и он загружается и возобновляется с помощью обновленного определения рабочего процесса.

```csharp
// Load the persisted workflow instance using the updated workflow definition
// and updated WorkflowIdentity.
WorkflowIdentity identity = new WorkflowIdentity
{
    Name = "MortgageWorkflow v1.1",
    Version = new Version(1, 1, 0, 0)
};

WorkflowApplication wfApp = new WorkflowApplication(new MortgageWorkflow(), identity);

// Configure persistence and desired workflow event handlers.
// (Omitted for brevity.)
ConfigureWorkflowApplication(wfApp);

// Load the persisted workflow instance.
wfApp.Load(InstanceId);

// Resume the workflow.
// wfApp.ResumeBookmark(...);
```

> [!NOTE]
> Чтобы загрузить пример кода, используемый в этом разделе, см. в разделе [пример кода динамического обновления](https://go.microsoft.com/fwlink/?LinkId=227905).
