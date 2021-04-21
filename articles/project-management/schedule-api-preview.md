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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="791b1-103">使用排程 API 對排程實體執行作業</span><span class="sxs-lookup"><span data-stu-id="791b1-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="791b1-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="791b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="791b1-105">本文中提到的部分或所有功能可做為預覽版本的一部分。</span><span class="sxs-lookup"><span data-stu-id="791b1-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="791b1-106">內容和功能隨時可能變更。</span><span class="sxs-lookup"><span data-stu-id="791b1-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="791b1-107">排程實體</span><span class="sxs-lookup"><span data-stu-id="791b1-107">Scheduling entities</span></span>

<span data-ttu-id="791b1-108">排程 API 提供對 **排程實體** 執行建立、更新和刪除作業的功能。</span><span class="sxs-lookup"><span data-stu-id="791b1-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="791b1-109">這些實體是透過 Project for the Web 中的排程引擎進行管理。</span><span class="sxs-lookup"><span data-stu-id="791b1-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="791b1-110">對 **排程實體** 的建立、更新及刪除作業在先前的 Dynamics 365 Project Operations 版本中受到限制。</span><span class="sxs-lookup"><span data-stu-id="791b1-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="791b1-111">下表提供 **排程實體** 的完整清單。</span><span class="sxs-lookup"><span data-stu-id="791b1-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="791b1-112">實體名稱</span><span class="sxs-lookup"><span data-stu-id="791b1-112">Entity name</span></span>  | <span data-ttu-id="791b1-113">實體邏輯名稱</span><span class="sxs-lookup"><span data-stu-id="791b1-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="791b1-114">Project</span><span class="sxs-lookup"><span data-stu-id="791b1-114">Project</span></span> | <span data-ttu-id="791b1-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="791b1-115">msdyn_project</span></span> |
| <span data-ttu-id="791b1-116">專案工作</span><span class="sxs-lookup"><span data-stu-id="791b1-116">Project Task</span></span>  | <span data-ttu-id="791b1-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="791b1-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="791b1-118">專案工作相依性</span><span class="sxs-lookup"><span data-stu-id="791b1-118">Project Task Dependency</span></span>  | <span data-ttu-id="791b1-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="791b1-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="791b1-120">資源指派</span><span class="sxs-lookup"><span data-stu-id="791b1-120">Resource Assignment</span></span> | <span data-ttu-id="791b1-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="791b1-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="791b1-122">專案貯體</span><span class="sxs-lookup"><span data-stu-id="791b1-122">Project Bucket</span></span>  | <span data-ttu-id="791b1-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="791b1-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="791b1-124">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="791b1-124">Project Team Member</span></span> | <span data-ttu-id="791b1-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="791b1-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="791b1-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="791b1-126">OperationSet</span></span>

<span data-ttu-id="791b1-127">OperationSet 是工作單位模式，當交易中有數個必須處理的排程影響要求時，可以使用此模式。</span><span class="sxs-lookup"><span data-stu-id="791b1-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="791b1-128">排程 API</span><span class="sxs-lookup"><span data-stu-id="791b1-128">Schedule APIs</span></span>

<span data-ttu-id="791b1-129">以下是最新排程 API 的清單。</span><span class="sxs-lookup"><span data-stu-id="791b1-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="791b1-130">**msdyn_CreateProjectV1**：此 API 可以用來建立專案。</span><span class="sxs-lookup"><span data-stu-id="791b1-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="791b1-131">專案和預設專案貯體會立即建立。</span><span class="sxs-lookup"><span data-stu-id="791b1-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="791b1-132">**msdyn_CreateTeamMemberV1**：此 API 可以用來建立專案團隊成員。</span><span class="sxs-lookup"><span data-stu-id="791b1-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="791b1-133">團隊成員記錄會立即建立。</span><span class="sxs-lookup"><span data-stu-id="791b1-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="791b1-134">**msdyn_CreateOperationSetV1**：此 API 可用來排定數個必須在交易中執行的要求。</span><span class="sxs-lookup"><span data-stu-id="791b1-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="791b1-135">**msdyn_PSSCreateV1**：此 API 可以用來建立實體。</span><span class="sxs-lookup"><span data-stu-id="791b1-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="791b1-136">實體可以是任何支援建立作業的排程實體。</span><span class="sxs-lookup"><span data-stu-id="791b1-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="791b1-137">**msdyn_PSSUpdateV1**：此 API 可以用來更新實體。</span><span class="sxs-lookup"><span data-stu-id="791b1-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="791b1-138">實體可以是任何支援更新作業的排程實體。</span><span class="sxs-lookup"><span data-stu-id="791b1-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="791b1-139">**msdyn_PSSDeleteV1**：此 API 可以用來刪除實體。</span><span class="sxs-lookup"><span data-stu-id="791b1-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="791b1-140">實體可以是任何支援刪除作業的排程實體。</span><span class="sxs-lookup"><span data-stu-id="791b1-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="791b1-141">**msdyn_ExecuteOperationSetV1**：此 API 是用來執行指定作業集中所有的作業。</span><span class="sxs-lookup"><span data-stu-id="791b1-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="791b1-142">將排程 API 與 OperationSet 搭配使用</span><span class="sxs-lookup"><span data-stu-id="791b1-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="791b1-143">因為會立即建立同時包含 **CreateProjectV1** 和 **CreateTeamMemberV1** 的記錄，這些 API 無法直接在 **OperationSet** 中使用。</span><span class="sxs-lookup"><span data-stu-id="791b1-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="791b1-144">不過，您可以使用 API 建立所需的記錄、建立 **OperationSet**，然後在 **OperationSet** 中使用這些預先建立的記錄。</span><span class="sxs-lookup"><span data-stu-id="791b1-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="791b1-145">支援的作業</span><span class="sxs-lookup"><span data-stu-id="791b1-145">Supported operations</span></span>

| <span data-ttu-id="791b1-146">排程實體</span><span class="sxs-lookup"><span data-stu-id="791b1-146">Scheduling entity</span></span> | <span data-ttu-id="791b1-147">建立​​</span><span class="sxs-lookup"><span data-stu-id="791b1-147">Create</span></span> | <span data-ttu-id="791b1-148">更新</span><span class="sxs-lookup"><span data-stu-id="791b1-148">Update</span></span> | <span data-ttu-id="791b1-149">Delete</span><span class="sxs-lookup"><span data-stu-id="791b1-149">Delete</span></span> | <span data-ttu-id="791b1-150">重要考量</span><span class="sxs-lookup"><span data-stu-id="791b1-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="791b1-151">專案工作</span><span class="sxs-lookup"><span data-stu-id="791b1-151">Project task</span></span> | <span data-ttu-id="791b1-152">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-152">Yes</span></span> | <span data-ttu-id="791b1-153">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-153">Yes</span></span> | <span data-ttu-id="791b1-154">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-154">Yes</span></span> | <span data-ttu-id="791b1-155">無​​</span><span class="sxs-lookup"><span data-stu-id="791b1-155">None</span></span> |
| <span data-ttu-id="791b1-156">專案工作相依性</span><span class="sxs-lookup"><span data-stu-id="791b1-156">Project task dependency</span></span> | <span data-ttu-id="791b1-157">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-157">Yes</span></span> | <span data-ttu-id="791b1-158">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-158">Yes</span></span> | | <span data-ttu-id="791b1-159">不會更新專案工作相依性記錄。</span><span class="sxs-lookup"><span data-stu-id="791b1-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="791b1-160">相反地，可以刪除舊記錄，也可以建立新記錄。</span><span class="sxs-lookup"><span data-stu-id="791b1-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="791b1-161">資源指派</span><span class="sxs-lookup"><span data-stu-id="791b1-161">Resource assignment</span></span> | <span data-ttu-id="791b1-162">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-162">Yes</span></span> | <span data-ttu-id="791b1-163">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-163">Yes</span></span> | | <span data-ttu-id="791b1-164">不支援對下列欄位的作業：**BookableResourceID**、**投入量**、**EffortCompleted**、**EffortRemaining** 和 **PlannedWork**。</span><span class="sxs-lookup"><span data-stu-id="791b1-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="791b1-165">不會更新資源指派記錄。</span><span class="sxs-lookup"><span data-stu-id="791b1-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="791b1-166">相反地，可以刪除舊記錄，也可以建立新記錄。</span><span class="sxs-lookup"><span data-stu-id="791b1-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="791b1-167">專案貯體</span><span class="sxs-lookup"><span data-stu-id="791b1-167">Project bucket</span></span> | <span data-ttu-id="791b1-168">無法使用</span><span class="sxs-lookup"><span data-stu-id="791b1-168">N/A</span></span> | <span data-ttu-id="791b1-169">無法使用</span><span class="sxs-lookup"><span data-stu-id="791b1-169">N/A</span></span> | <span data-ttu-id="791b1-170">無法使用</span><span class="sxs-lookup"><span data-stu-id="791b1-170">N/A</span></span> | <span data-ttu-id="791b1-171">預設貯體是使用 **CreateProjectV1** API 所建立。</span><span class="sxs-lookup"><span data-stu-id="791b1-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="791b1-172">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="791b1-172">Project team member</span></span> | <span data-ttu-id="791b1-173">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-173">Yes</span></span> | <span data-ttu-id="791b1-174">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-174">Yes</span></span> | <span data-ttu-id="791b1-175">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-175">Yes</span></span> | <span data-ttu-id="791b1-176">如果是建立作業，請使用 **CreateTeamMemberV1** API。</span><span class="sxs-lookup"><span data-stu-id="791b1-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="791b1-177">Project</span><span class="sxs-lookup"><span data-stu-id="791b1-177">Project</span></span> | <span data-ttu-id="791b1-178">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-178">Yes</span></span> | <span data-ttu-id="791b1-179">.是</span><span class="sxs-lookup"><span data-stu-id="791b1-179">Yes</span></span> | <span data-ttu-id="791b1-180">無法使用</span><span class="sxs-lookup"><span data-stu-id="791b1-180">N/A</span></span> | <span data-ttu-id="791b1-181">不支援對下列欄位的作業：**StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、**CalendarID**、**投入量**、**EffortCompleted**、**EffortRemaining**、**進度**、**完成**、**TaskEarliestStart** 和 **期間**。</span><span class="sxs-lookup"><span data-stu-id="791b1-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="791b1-182">可以透過包含自訂欄位的實體物件呼叫這些 API。</span><span class="sxs-lookup"><span data-stu-id="791b1-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="791b1-183">識別碼屬性可選用。</span><span class="sxs-lookup"><span data-stu-id="791b1-183">The ID property is optional.</span></span> <span data-ttu-id="791b1-184">如果已提供，則系統會嘗試使用，並在無法使用時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="791b1-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="791b1-185">如果未提供，則系統會產生此屬性。</span><span class="sxs-lookup"><span data-stu-id="791b1-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="791b1-186">限制和已知問題</span><span class="sxs-lookup"><span data-stu-id="791b1-186">Limitations and known issues</span></span>
<span data-ttu-id="791b1-187">以下是限制和已知問題的清單：</span><span class="sxs-lookup"><span data-stu-id="791b1-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="791b1-188">只有 **擁有 Microsoft Project 授權的使用者** 才可以使用排程 API。</span><span class="sxs-lookup"><span data-stu-id="791b1-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="791b1-189">無法供下列使用者使用：</span><span class="sxs-lookup"><span data-stu-id="791b1-189">They can't be used by:</span></span>
    - <span data-ttu-id="791b1-190">應用程式使用者</span><span class="sxs-lookup"><span data-stu-id="791b1-190">Application users</span></span>
    - <span data-ttu-id="791b1-191">系統使用者</span><span class="sxs-lookup"><span data-stu-id="791b1-191">System users</span></span>
    - <span data-ttu-id="791b1-192">整合使用者</span><span class="sxs-lookup"><span data-stu-id="791b1-192">Integration users</span></span>
    - <span data-ttu-id="791b1-193">其他沒有必要授權的使用者</span><span class="sxs-lookup"><span data-stu-id="791b1-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="791b1-194">每個 **OperationSet** 最多只能有 100 項作業。</span><span class="sxs-lookup"><span data-stu-id="791b1-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="791b1-195">每個使用者最多只能有 10 個已開啟的 **OperationSet**。</span><span class="sxs-lookup"><span data-stu-id="791b1-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="791b1-196">Project Operations 目前在專案中最多支援總計 500 個工作。</span><span class="sxs-lookup"><span data-stu-id="791b1-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="791b1-197">**OperationSet** 失敗狀態和失敗記錄目前未提供。</span><span class="sxs-lookup"><span data-stu-id="791b1-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="791b1-198">排程 API 開放公開預覽。</span><span class="sxs-lookup"><span data-stu-id="791b1-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="791b1-199">Microsoft 不支援在生產環境中使用這些 API。</span><span class="sxs-lookup"><span data-stu-id="791b1-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="791b1-200">範例案例</span><span class="sxs-lookup"><span data-stu-id="791b1-200">Sample scenario</span></span>

<span data-ttu-id="791b1-201">在此案例中，您將會建立專案、團隊成員、四個工作和兩個資源指派。</span><span class="sxs-lookup"><span data-stu-id="791b1-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="791b1-202">接下來，會更新一項工作、更新專案、刪除一項工作、刪除一個資源指派，以及建立工作相依性。</span><span class="sxs-lookup"><span data-stu-id="791b1-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="791b1-203">其他範例</span><span class="sxs-lookup"><span data-stu-id="791b1-203">Additional samples</span></span>

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
