---
title: 使用專案排程 API 以對排程實體執行作業
description: 本文提供有關使用專案排程 API 的資訊與範例。
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541114"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>使用專案排程 API 以對排程實體執行作業

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_


**排程實體**

專案排程 API 提供對 **排程實體** 執行建立、更新和刪除作業的功能。 這些實體是透過 Project for the Web 中的排程引擎進行管理。 對 **排程實體** 的建立、更新及刪除作業在先前的 Dynamics 365 Project Operations 版本中受到限制。

下表提供專案排程實體的完整清單。

| **實體名稱**         | **實體邏輯名稱**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| 專案工作            | msdyn_projecttask           |
| 專案工作相依性 | msdyn_projecttaskdependency |
| 資源指派     | msdyn_resourceassignment    |
| 專案貯體          | msdyn_projectbucket         |
| 專案團隊成員     | msdyn_projectteam           |
| 專案檢查清單      | msdyn_projectchecklist      |
| 專案標籤           | msdyn_projectlabel          |
| 專案工作與標籤   | msdyn_projecttasktolabel    |
| 專案短期衝刺          | msdyn_projectsprint         |

**OperationSet**

OperationSet 是工作單位模式，當交易中有數個必須處理的排程影響要求時，可以使用此模式。

**專案排程 API**

以下是目前專案排程 API 的清單。

| **API**                                 | 名描述                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | 此 API 是用來建立專案的。 專案和預設專案貯體會立即建立。                         |
| **msdyn_CreateTeamMemberV1**            | 此 API 是用來建立團隊成員的。 團隊成員記錄會立即建立。                                  |
| **msdyn_CreateOperationSetV1**          | 此 API 是用來排定數個必須在交易中執行的要求。                                        |
| **msdyn_PssCreateV1**                   | 此 API 是用來建立實體的。 實體可以是任何支援建立作業的專案排程實體。 |
| **msdyn_PssUpdateV1**                   | 此 API 是用來更新實體的。 實體可以是任何支援更新作業的專案排程實體  |
| **msdyn_PssDeleteV1**                   | 此 API 是用來刪除實體的。 實體可以是任何支援刪除作業的專案排程實體。 |
| **msdyn_ExecuteOperationSetV1**         | 此 API 是用來執行指定作業集中所有的作業。                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | 此 API 是用來更新資源指派計畫作業分佈。                                                        |



**與 OperationSet 搭配使用專案排程 API**

因為會立即建立同時包含 **CreateProjectV1** 和 **CreateTeamMemberV1** 的記錄，這些 API 無法直接在 **OperationSet** 中使用。 不過，您可以使用 API 建立所需的記錄、建立 **OperationSet**，然後在 **OperationSet** 中使用這些預先建立的記錄。

**支援的作業**

| **排程實體**   | **建立** | **Update** | **删除** | **重要考量**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 專案工作            | .是        | .是        | .是        | 您可以在 Project for the Web 中編輯 **進度**、**EffortCompleted** 及 **EffortRemaining** 欄位，但無法在 Project Operations 中編輯這些欄位。                                                                                                                                                                                             |
| 專案工作相依性 | .是        | 無         | .是        | 不會更新專案工作相依性記錄。 相反地，可以刪除舊記錄，也可以建立新記錄。                                                                                                                                                                                                                                 |
| 資源指派     | .是        | 是\*      | .是        | 不支援對下列欄位的作業：**BookableResourceID**、**投入量**、**EffortCompleted**、**EffortRemaining** 和 **PlannedWork**。 不會更新資源指派記錄。 相反地，可以刪除舊記錄，也可以建立新記錄。 提供單獨的 API 來更新資源指派分佈。 |
| 專案貯體          | .是        | .是        | .是        | 預設貯體是使用 **CreateProjectV1** API 所建立。 更新版本 16 中已新增對建立和刪除專案貯體的支援。                                                                                                                                                                                                   |
| 專案團隊成員     | .是        | .是        | .是        | 如果是建立作業，請使用 **CreateTeamMemberV1** API。                                                                                                                                                                                                                                                                                           |
| 專案                 | .是        | .是        |            | 不支援對下列欄位的作業：**StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、**CalendarID**、**投入量**、**EffortCompleted**、**EffortRemaining**、**進度**、**完成**、**TaskEarliestStart** 和 **期間**。                                                                                       |
| 專案檢查清單      | .是        | .是        | .是        |                                                                                                                                                                                                                                                                                                                                                         |
| 專案標籤           | 無         | .是        | 無         | 標籤名稱可以變更。 此功能僅適用於 Project for the Web                                                                                                                                                                                                                                                                      |
| 專案工作與標籤   | .是        | 無         | .是        | 此功能僅適用於 Project for the Web                                                                                                                                                                                                                                                                                                  |
| 專案短期衝刺          | .是        | .是        | .是        | **起始** 欄位的日期必須早於 **結束** 欄位。 同一專案的短期衝刺不能相互重疊。 此功能僅適用於 Project for the Web                                                                                                                                                                    |




識別碼屬性可選用。 如果已提供，則系統會嘗試使用，並在無法使用時擲回例外狀況。 如果未提供，則系統會產生此屬性。

**限制和已知問題**

以下是限制和已知問題的清單：

-   只有 **擁有 Microsoft Project 授權的使用者** 才能使用專案排程 API。 無法供下列使用者使用：
    -   應用程式使用者
    -   系統使用者
    -   整合使用者
    -   其他沒有必要授權的使用者
-   每個 **OperationSet** 最多只能有 100 項作業。
-   每個使用者最多只能有 10 個已開啟的 **OperationSet**。
-   Project Operations 目前在專案中最多支援總計 500 個工作。
-   每個更新資源指派分佈作業都計為單一作業。
-   每個更新的分佈清單最多可以包含 100 個時間配量。
-   **OperationSet** 失敗狀態和失敗記錄目前未提供。
-   每個專案最多可有 400 個短期衝刺。
-   [專案和工作的限制與界限](/project-for-the-web/project-for-the-web-limits-and-boundaries)。
-   標籤目前僅適用於 Project for the Web。

**錯誤處理**

-   若要檢閱由作業集所產生的錯誤，請移至 **設定** \> **排程整合** \> **作業集**。
-   若要檢閱專案排程服務所產生的錯誤，請移至 **設定** \> **排程整合** \> **PSS 錯誤記錄**。

**編輯資源指派分佈**

與更新實體的所有其他專案排程 API 不同，資源指派分佈 API 只負責更新單一實體 msydn_resourceassignment 上的單一欄位 msdyn_plannedwork。

指定的排程模式為：

-   **固定單位**
-   專案行事曆為 9-5p 為 9 5pst、週一、週二、週四、週五 (週三無工作)
-   資源行事曆為太平洋標準時間週一至週五 9-1p

這項指派時間為一週，一天四小時。 這是因為資源行事曆是從太平洋標準時間 9 點到 1 點開始的，即每天四個小時。

| &nbsp;     | 工作 | 開始日期 | 結束日期  | 數量 | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 工作人員 |  T1  | 6/13/2022  | 6/17/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

例如，如果您希望工作人員本週每天只工作三個小時，並為其他工作留出一小時。

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours 範例承載：

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

這是更新分佈排程 API 執行後的指派。

| &nbsp;     | 工作 | 開始日期 | 結束日期  | 數量 | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 工作人員 | T1   | 6/13/2022  | 6/17/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**範例案例**

在此案例中，您將會建立專案、團隊成員、四個工作和兩個資源指派。 接下來，會更新一項工作、更新專案、刪除一項工作、刪除一個資源指派，以及建立工作相依性。

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

** 其他範例

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
