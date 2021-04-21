---
title: 使用排程 API 對排程實體執行作業
description: 本主題提供有關使用排程 API 的資訊與範例。
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868119"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>使用排程 API 對排程實體執行作業

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

> [!IMPORTANT] 
> 本文中提到的部分或所有功能可做為預覽版本的一部分。 內容和功能隨時可能變更。 

## <a name="scheduling-entities"></a>排程實體

排程 API 提供對 **排程實體** 執行建立、更新和刪除作業的功能。 這些實體是透過 Project for the Web 中的排程引擎進行管理。 對 **排程實體** 的建立、更新及刪除作業在先前的 Dynamics 365 Project Operations 版本中受到限制。

下表提供 **排程實體** 的完整清單。

| 實體名稱  | 實體邏輯名稱 |
| --- | --- |
| Project | msdyn_project |
| 專案工作  | msdyn_projecttask  |
| 專案工作相依性  | msdyn_projecttaskdependency  |
| 資源指派 | msdyn_resourceassignment |
| 專案貯體  | msdyn_projectbucket |
| 專案團隊成員 | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet 是工作單位模式，當交易中有數個必須處理的排程影響要求時，可以使用此模式。

## <a name="schedule-apis"></a>排程 API

以下是最新排程 API 的清單。

- **msdyn_CreateProjectV1**：此 API 可以用來建立專案。 專案和預設專案貯體會立即建立。
- **msdyn_CreateTeamMemberV1**：此 API 可以用來建立專案團隊成員。 團隊成員記錄會立即建立。
- **msdyn_CreateOperationSetV1**：此 API 可用來排定數個必須在交易中執行的要求。
- **msdyn_PSSCreateV1**：此 API 可以用來建立實體。 實體可以是任何支援建立作業的排程實體。
- **msdyn_PSSUpdateV1**：此 API 可以用來更新實體。 實體可以是任何支援更新作業的排程實體。
- **msdyn_PSSDeleteV1**：此 API 可以用來刪除實體。 實體可以是任何支援刪除作業的排程實體。
- **msdyn_ExecuteOperationSetV1**：此 API 是用來執行指定作業集中所有的作業。

## <a name="using-schedule-apis-with-operationset"></a>將排程 API 與 OperationSet 搭配使用

因為會立即建立同時包含 **CreateProjectV1** 和 **CreateTeamMemberV1** 的記錄，這些 API 無法直接在 **OperationSet** 中使用。 不過，您可以使用 API 建立所需的記錄、建立 **OperationSet**，然後在 **OperationSet** 中使用這些預先建立的記錄。

## <a name="supported-operations"></a>支援的作業

| 排程實體 | 建立​​ | 更新 | Delete | 重要考量 |
| --- | --- | --- | --- | --- |
專案工作 | .是 | .是 | .是 | 無​​ |
| 專案工作相依性 | .是 | .是 | | 不會更新專案工作相依性記錄。 相反地，可以刪除舊記錄，也可以建立新記錄。 |
| 資源指派 | .是 | .是 | | 不支援對下列欄位的作業：**BookableResourceID**、**投入量**、**EffortCompleted**、**EffortRemaining** 和 **PlannedWork**。 不會更新資源指派記錄。 相反地，可以刪除舊記錄，也可以建立新記錄。 |
| 專案貯體 | 無法使用 | 無法使用 | 無法使用 | 預設貯體是使用 **CreateProjectV1** API 所建立。 |
| 專案團隊成員 | .是 | .是 | .是 | 如果是建立作業，請使用 **CreateTeamMemberV1** API。 |
| Project | .是 | .是 | 無法使用 | 不支援對下列欄位的作業：**StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、**CalendarID**、**投入量**、**EffortCompleted**、**EffortRemaining**、**進度**、**完成**、**TaskEarliestStart** 和 **期間**。 |

可以透過包含自訂欄位的實體物件呼叫這些 API。

識別碼屬性可選用。 如果已提供，則系統會嘗試使用，並在無法使用時擲回例外狀況。 如果未提供，則系統會產生此屬性。

## <a name="limitations-and-known-issues"></a>限制和已知問題
以下是限制和已知問題的清單：

- 只有 **擁有 Microsoft Project 授權的使用者** 才可以使用排程 API。 無法供下列使用者使用：
    - 應用程式使用者
    - 系統使用者
    - 整合使用者
    - 其他沒有必要授權的使用者
- 每個 **OperationSet** 最多只能有 100 項作業。
- 每個使用者最多只能有 10 個已開啟的 **OperationSet**。
- Project Operations 目前在專案中最多支援總計 500 個工作。
- **OperationSet** 失敗狀態和失敗記錄目前未提供。
- 排程 API 開放公開預覽。 Microsoft 不支援在生產環境中使用這些 API。

## <a name="sample-scenario"></a>範例案例

在此案例中，您將會建立專案、團隊成員、四個工作和兩個資源指派。 接下來，會更新一項工作、更新專案、刪除一項工作、刪除一個資源指派，以及建立工作相依性。

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>其他範例

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
