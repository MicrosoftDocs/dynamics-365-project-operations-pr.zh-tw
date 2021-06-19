---
title: 使用排程 API 對排程實體執行作業
description: 本主題提供有關使用排程 API 的資訊與範例。
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116787"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="c0339-103">使用排程 API 對排程實體執行作業</span><span class="sxs-lookup"><span data-stu-id="c0339-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="c0339-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="c0339-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="c0339-105">本文中提到的部分或所有功能可做為預覽版本的一部分。</span><span class="sxs-lookup"><span data-stu-id="c0339-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="c0339-106">內容和功能隨時可能變更。</span><span class="sxs-lookup"><span data-stu-id="c0339-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="c0339-107">排程實體</span><span class="sxs-lookup"><span data-stu-id="c0339-107">Scheduling entities</span></span>

<span data-ttu-id="c0339-108">排程 API 提供對 **排程實體** 執行建立、更新和刪除作業的功能。</span><span class="sxs-lookup"><span data-stu-id="c0339-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="c0339-109">這些實體是透過 Project for the Web 中的排程引擎進行管理。</span><span class="sxs-lookup"><span data-stu-id="c0339-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="c0339-110">對 **排程實體** 的建立、更新及刪除作業在先前的 Dynamics 365 Project Operations 版本中受到限制。</span><span class="sxs-lookup"><span data-stu-id="c0339-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="c0339-111">下表提供 **排程實體** 的完整清單。</span><span class="sxs-lookup"><span data-stu-id="c0339-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="c0339-112">實體名稱</span><span class="sxs-lookup"><span data-stu-id="c0339-112">Entity name</span></span>  | <span data-ttu-id="c0339-113">實體邏輯名稱</span><span class="sxs-lookup"><span data-stu-id="c0339-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="c0339-114">Project</span><span class="sxs-lookup"><span data-stu-id="c0339-114">Project</span></span> | <span data-ttu-id="c0339-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="c0339-115">msdyn_project</span></span> |
| <span data-ttu-id="c0339-116">專案工作</span><span class="sxs-lookup"><span data-stu-id="c0339-116">Project Task</span></span>  | <span data-ttu-id="c0339-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="c0339-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="c0339-118">專案工作相依性</span><span class="sxs-lookup"><span data-stu-id="c0339-118">Project Task Dependency</span></span>  | <span data-ttu-id="c0339-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="c0339-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="c0339-120">資源指派</span><span class="sxs-lookup"><span data-stu-id="c0339-120">Resource Assignment</span></span> | <span data-ttu-id="c0339-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="c0339-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="c0339-122">專案貯體</span><span class="sxs-lookup"><span data-stu-id="c0339-122">Project Bucket</span></span>  | <span data-ttu-id="c0339-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="c0339-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="c0339-124">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="c0339-124">Project Team Member</span></span> | <span data-ttu-id="c0339-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="c0339-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="c0339-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="c0339-126">OperationSet</span></span>

<span data-ttu-id="c0339-127">OperationSet 是工作單位模式，當交易中有數個必須處理的排程影響要求時，可以使用此模式。</span><span class="sxs-lookup"><span data-stu-id="c0339-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="c0339-128">排程 API</span><span class="sxs-lookup"><span data-stu-id="c0339-128">Schedule APIs</span></span>

<span data-ttu-id="c0339-129">以下是最新排程 API 的清單。</span><span class="sxs-lookup"><span data-stu-id="c0339-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="c0339-130">**msdyn_CreateProjectV1**：此 API 可以用來建立專案。</span><span class="sxs-lookup"><span data-stu-id="c0339-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="c0339-131">專案和預設專案貯體會立即建立。</span><span class="sxs-lookup"><span data-stu-id="c0339-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="c0339-132">**msdyn_CreateTeamMemberV1**：此 API 可以用來建立專案團隊成員。</span><span class="sxs-lookup"><span data-stu-id="c0339-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="c0339-133">團隊成員記錄會立即建立。</span><span class="sxs-lookup"><span data-stu-id="c0339-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="c0339-134">**msdyn_CreateOperationSetV1**：此 API 可用來排定數個必須在交易中執行的要求。</span><span class="sxs-lookup"><span data-stu-id="c0339-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="c0339-135">**msdyn_PSSCreateV1**：此 API 可以用來建立實體。</span><span class="sxs-lookup"><span data-stu-id="c0339-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="c0339-136">實體可以是任何支援建立作業的排程實體。</span><span class="sxs-lookup"><span data-stu-id="c0339-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="c0339-137">**msdyn_PSSUpdateV1**：此 API 可以用來更新實體。</span><span class="sxs-lookup"><span data-stu-id="c0339-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="c0339-138">實體可以是任何支援更新作業的排程實體。</span><span class="sxs-lookup"><span data-stu-id="c0339-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="c0339-139">**msdyn_PSSDeleteV1**：此 API 可以用來刪除實體。</span><span class="sxs-lookup"><span data-stu-id="c0339-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="c0339-140">實體可以是任何支援刪除作業的排程實體。</span><span class="sxs-lookup"><span data-stu-id="c0339-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="c0339-141">**msdyn_ExecuteOperationSetV1**：此 API 是用來執行指定作業集中所有的作業。</span><span class="sxs-lookup"><span data-stu-id="c0339-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="c0339-142">將排程 API 與 OperationSet 搭配使用</span><span class="sxs-lookup"><span data-stu-id="c0339-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="c0339-143">因為會立即建立同時包含 **CreateProjectV1** 和 **CreateTeamMemberV1** 的記錄，這些 API 無法直接在 **OperationSet** 中使用。</span><span class="sxs-lookup"><span data-stu-id="c0339-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="c0339-144">不過，您可以使用 API 建立所需的記錄、建立 **OperationSet**，然後在 **OperationSet** 中使用這些預先建立的記錄。</span><span class="sxs-lookup"><span data-stu-id="c0339-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="c0339-145">支援的作業</span><span class="sxs-lookup"><span data-stu-id="c0339-145">Supported operations</span></span>

| <span data-ttu-id="c0339-146">排程實體</span><span class="sxs-lookup"><span data-stu-id="c0339-146">Scheduling entity</span></span> | <span data-ttu-id="c0339-147">建立​​</span><span class="sxs-lookup"><span data-stu-id="c0339-147">Create</span></span> | <span data-ttu-id="c0339-148">更新</span><span class="sxs-lookup"><span data-stu-id="c0339-148">Update</span></span> | <span data-ttu-id="c0339-149">Delete</span><span class="sxs-lookup"><span data-stu-id="c0339-149">Delete</span></span> | <span data-ttu-id="c0339-150">重要考量</span><span class="sxs-lookup"><span data-stu-id="c0339-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="c0339-151">專案工作</span><span class="sxs-lookup"><span data-stu-id="c0339-151">Project task</span></span> | <span data-ttu-id="c0339-152">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-152">Yes</span></span> | <span data-ttu-id="c0339-153">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-153">Yes</span></span> | <span data-ttu-id="c0339-154">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-154">Yes</span></span> | <span data-ttu-id="c0339-155">無​​</span><span class="sxs-lookup"><span data-stu-id="c0339-155">None</span></span> |
| <span data-ttu-id="c0339-156">專案工作相依性</span><span class="sxs-lookup"><span data-stu-id="c0339-156">Project task dependency</span></span> | <span data-ttu-id="c0339-157">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-157">Yes</span></span> | <span data-ttu-id="c0339-158">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-158">Yes</span></span> | | <span data-ttu-id="c0339-159">不會更新專案工作相依性記錄。</span><span class="sxs-lookup"><span data-stu-id="c0339-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="c0339-160">相反地，可以刪除舊記錄，也可以建立新記錄。</span><span class="sxs-lookup"><span data-stu-id="c0339-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="c0339-161">資源指派</span><span class="sxs-lookup"><span data-stu-id="c0339-161">Resource assignment</span></span> | <span data-ttu-id="c0339-162">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-162">Yes</span></span> | <span data-ttu-id="c0339-163">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-163">Yes</span></span> | | <span data-ttu-id="c0339-164">不支援對下列欄位的作業：**BookableResourceID**、**投入量**、**EffortCompleted**、**EffortRemaining** 和 **PlannedWork**。</span><span class="sxs-lookup"><span data-stu-id="c0339-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="c0339-165">不會更新資源指派記錄。</span><span class="sxs-lookup"><span data-stu-id="c0339-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="c0339-166">相反地，可以刪除舊記錄，也可以建立新記錄。</span><span class="sxs-lookup"><span data-stu-id="c0339-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="c0339-167">專案貯體</span><span class="sxs-lookup"><span data-stu-id="c0339-167">Project bucket</span></span> | <span data-ttu-id="c0339-168">無法使用</span><span class="sxs-lookup"><span data-stu-id="c0339-168">N/A</span></span> | <span data-ttu-id="c0339-169">無法使用</span><span class="sxs-lookup"><span data-stu-id="c0339-169">N/A</span></span> | <span data-ttu-id="c0339-170">無法使用</span><span class="sxs-lookup"><span data-stu-id="c0339-170">N/A</span></span> | <span data-ttu-id="c0339-171">預設貯體是使用 **CreateProjectV1** API 所建立。</span><span class="sxs-lookup"><span data-stu-id="c0339-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="c0339-172">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="c0339-172">Project team member</span></span> | <span data-ttu-id="c0339-173">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-173">Yes</span></span> | <span data-ttu-id="c0339-174">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-174">Yes</span></span> | <span data-ttu-id="c0339-175">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-175">Yes</span></span> | <span data-ttu-id="c0339-176">如果是建立作業，請使用 **CreateTeamMemberV1** API。</span><span class="sxs-lookup"><span data-stu-id="c0339-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="c0339-177">Project</span><span class="sxs-lookup"><span data-stu-id="c0339-177">Project</span></span> | <span data-ttu-id="c0339-178">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-178">Yes</span></span> | <span data-ttu-id="c0339-179">.是</span><span class="sxs-lookup"><span data-stu-id="c0339-179">Yes</span></span> | <span data-ttu-id="c0339-180">無法使用</span><span class="sxs-lookup"><span data-stu-id="c0339-180">N/A</span></span> | <span data-ttu-id="c0339-181">不支援對下列欄位的作業：**StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、**CalendarID**、**投入量**、**EffortCompleted**、**EffortRemaining**、**進度**、**完成**、**TaskEarliestStart** 和 **期間**。</span><span class="sxs-lookup"><span data-stu-id="c0339-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="c0339-182">可以透過包含自訂欄位的實體物件呼叫這些 API。</span><span class="sxs-lookup"><span data-stu-id="c0339-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="c0339-183">識別碼屬性可選用。</span><span class="sxs-lookup"><span data-stu-id="c0339-183">The ID property is optional.</span></span> <span data-ttu-id="c0339-184">如果已提供，則系統會嘗試使用，並在無法使用時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c0339-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="c0339-185">如果未提供，則系統會產生此屬性。</span><span class="sxs-lookup"><span data-stu-id="c0339-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="c0339-186">受限制的欄位</span><span class="sxs-lookup"><span data-stu-id="c0339-186">Restricted fields</span></span>

<span data-ttu-id="c0339-187">下表定義受限制無法 **建立** 和 **編輯** 的欄位。</span><span class="sxs-lookup"><span data-stu-id="c0339-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="c0339-188">專案工作</span><span class="sxs-lookup"><span data-stu-id="c0339-188">Project task</span></span>

| <span data-ttu-id="c0339-189">**邏輯名稱**</span><span class="sxs-lookup"><span data-stu-id="c0339-189">**Logical name**</span></span>                       | <span data-ttu-id="c0339-190">**可以建立**</span><span class="sxs-lookup"><span data-stu-id="c0339-190">**Can create**</span></span> | <span data-ttu-id="c0339-191">**可以編輯**</span><span class="sxs-lookup"><span data-stu-id="c0339-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="c0339-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="c0339-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="c0339-193">否</span><span class="sxs-lookup"><span data-stu-id="c0339-193">no</span></span>             | <span data-ttu-id="c0339-194">否</span><span class="sxs-lookup"><span data-stu-id="c0339-194">no</span></span>               |
| <span data-ttu-id="c0339-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="c0339-196">否</span><span class="sxs-lookup"><span data-stu-id="c0339-196">no</span></span>             | <span data-ttu-id="c0339-197">否</span><span class="sxs-lookup"><span data-stu-id="c0339-197">no</span></span>               |
| <span data-ttu-id="c0339-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="c0339-198">msdyn_actualend</span></span>                        | <span data-ttu-id="c0339-199">否</span><span class="sxs-lookup"><span data-stu-id="c0339-199">no</span></span>             | <span data-ttu-id="c0339-200">否</span><span class="sxs-lookup"><span data-stu-id="c0339-200">no</span></span>               |
| <span data-ttu-id="c0339-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="c0339-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="c0339-202">否</span><span class="sxs-lookup"><span data-stu-id="c0339-202">no</span></span>             | <span data-ttu-id="c0339-203">否</span><span class="sxs-lookup"><span data-stu-id="c0339-203">no</span></span>               |
| <span data-ttu-id="c0339-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="c0339-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="c0339-205">否</span><span class="sxs-lookup"><span data-stu-id="c0339-205">no</span></span>             | <span data-ttu-id="c0339-206">否</span><span class="sxs-lookup"><span data-stu-id="c0339-206">no</span></span>               |
| <span data-ttu-id="c0339-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="c0339-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="c0339-208">否</span><span class="sxs-lookup"><span data-stu-id="c0339-208">no</span></span>             | <span data-ttu-id="c0339-209">否</span><span class="sxs-lookup"><span data-stu-id="c0339-209">no</span></span>               |
| <span data-ttu-id="c0339-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="c0339-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="c0339-211">否</span><span class="sxs-lookup"><span data-stu-id="c0339-211">no</span></span>             | <span data-ttu-id="c0339-212">否</span><span class="sxs-lookup"><span data-stu-id="c0339-212">no</span></span>               |
| <span data-ttu-id="c0339-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="c0339-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="c0339-214">否</span><span class="sxs-lookup"><span data-stu-id="c0339-214">no</span></span>             | <span data-ttu-id="c0339-215">否</span><span class="sxs-lookup"><span data-stu-id="c0339-215">no</span></span>               |
| <span data-ttu-id="c0339-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="c0339-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="c0339-217">否</span><span class="sxs-lookup"><span data-stu-id="c0339-217">no</span></span>             | <span data-ttu-id="c0339-218">否</span><span class="sxs-lookup"><span data-stu-id="c0339-218">no</span></span>               |
| <span data-ttu-id="c0339-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="c0339-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="c0339-220">否</span><span class="sxs-lookup"><span data-stu-id="c0339-220">no</span></span>             | <span data-ttu-id="c0339-221">否</span><span class="sxs-lookup"><span data-stu-id="c0339-221">no</span></span>               |
| <span data-ttu-id="c0339-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="c0339-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="c0339-223">否</span><span class="sxs-lookup"><span data-stu-id="c0339-223">no</span></span>             | <span data-ttu-id="c0339-224">否</span><span class="sxs-lookup"><span data-stu-id="c0339-224">no</span></span>               |
| <span data-ttu-id="c0339-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="c0339-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="c0339-226">否</span><span class="sxs-lookup"><span data-stu-id="c0339-226">no</span></span>             | <span data-ttu-id="c0339-227">否</span><span class="sxs-lookup"><span data-stu-id="c0339-227">no</span></span>               |
| <span data-ttu-id="c0339-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="c0339-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="c0339-229">否</span><span class="sxs-lookup"><span data-stu-id="c0339-229">no</span></span>             | <span data-ttu-id="c0339-230">否</span><span class="sxs-lookup"><span data-stu-id="c0339-230">no</span></span>               |
| <span data-ttu-id="c0339-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="c0339-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="c0339-232">否</span><span class="sxs-lookup"><span data-stu-id="c0339-232">no</span></span>             | <span data-ttu-id="c0339-233">否</span><span class="sxs-lookup"><span data-stu-id="c0339-233">no</span></span>               |
| <span data-ttu-id="c0339-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="c0339-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="c0339-235">否</span><span class="sxs-lookup"><span data-stu-id="c0339-235">no</span></span>             | <span data-ttu-id="c0339-236">否</span><span class="sxs-lookup"><span data-stu-id="c0339-236">no</span></span>               |
| <span data-ttu-id="c0339-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="c0339-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="c0339-238">否</span><span class="sxs-lookup"><span data-stu-id="c0339-238">no</span></span>             | <span data-ttu-id="c0339-239">否</span><span class="sxs-lookup"><span data-stu-id="c0339-239">no</span></span>               |
| <span data-ttu-id="c0339-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="c0339-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="c0339-241">否</span><span class="sxs-lookup"><span data-stu-id="c0339-241">no</span></span>             | <span data-ttu-id="c0339-242">否</span><span class="sxs-lookup"><span data-stu-id="c0339-242">no</span></span>               |
| <span data-ttu-id="c0339-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="c0339-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="c0339-244">否</span><span class="sxs-lookup"><span data-stu-id="c0339-244">no</span></span>             | <span data-ttu-id="c0339-245">否</span><span class="sxs-lookup"><span data-stu-id="c0339-245">no</span></span>               |
| <span data-ttu-id="c0339-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="c0339-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="c0339-247">否</span><span class="sxs-lookup"><span data-stu-id="c0339-247">no</span></span>             | <span data-ttu-id="c0339-248">否</span><span class="sxs-lookup"><span data-stu-id="c0339-248">no</span></span>               |
| <span data-ttu-id="c0339-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="c0339-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="c0339-250">否</span><span class="sxs-lookup"><span data-stu-id="c0339-250">no</span></span>             | <span data-ttu-id="c0339-251">否</span><span class="sxs-lookup"><span data-stu-id="c0339-251">no</span></span>               |
| <span data-ttu-id="c0339-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="c0339-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="c0339-253">否</span><span class="sxs-lookup"><span data-stu-id="c0339-253">no</span></span>             | <span data-ttu-id="c0339-254">否</span><span class="sxs-lookup"><span data-stu-id="c0339-254">no</span></span>               |
| <span data-ttu-id="c0339-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="c0339-256">否</span><span class="sxs-lookup"><span data-stu-id="c0339-256">no</span></span>             | <span data-ttu-id="c0339-257">否</span><span class="sxs-lookup"><span data-stu-id="c0339-257">no</span></span>               |
| <span data-ttu-id="c0339-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="c0339-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="c0339-259">否</span><span class="sxs-lookup"><span data-stu-id="c0339-259">no</span></span>             | <span data-ttu-id="c0339-260">否</span><span class="sxs-lookup"><span data-stu-id="c0339-260">no</span></span>               |
| <span data-ttu-id="c0339-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="c0339-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="c0339-262">否</span><span class="sxs-lookup"><span data-stu-id="c0339-262">no</span></span>             | <span data-ttu-id="c0339-263">否</span><span class="sxs-lookup"><span data-stu-id="c0339-263">no</span></span>               |
| <span data-ttu-id="c0339-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="c0339-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="c0339-265">否</span><span class="sxs-lookup"><span data-stu-id="c0339-265">no</span></span>             | <span data-ttu-id="c0339-266">否</span><span class="sxs-lookup"><span data-stu-id="c0339-266">no</span></span>               |
| <span data-ttu-id="c0339-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="c0339-267">msdyn_progress</span></span>                         | <span data-ttu-id="c0339-268">否</span><span class="sxs-lookup"><span data-stu-id="c0339-268">no</span></span>             | <span data-ttu-id="c0339-269">否 (對 P4W 則是)</span><span class="sxs-lookup"><span data-stu-id="c0339-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="c0339-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="c0339-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="c0339-271">否</span><span class="sxs-lookup"><span data-stu-id="c0339-271">no</span></span>             | <span data-ttu-id="c0339-272">否</span><span class="sxs-lookup"><span data-stu-id="c0339-272">no</span></span>               |
| <span data-ttu-id="c0339-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="c0339-274">否</span><span class="sxs-lookup"><span data-stu-id="c0339-274">no</span></span>             | <span data-ttu-id="c0339-275">否</span><span class="sxs-lookup"><span data-stu-id="c0339-275">no</span></span>               |
| <span data-ttu-id="c0339-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="c0339-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="c0339-277">否</span><span class="sxs-lookup"><span data-stu-id="c0339-277">no</span></span>             | <span data-ttu-id="c0339-278">否</span><span class="sxs-lookup"><span data-stu-id="c0339-278">no</span></span>               |
| <span data-ttu-id="c0339-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="c0339-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="c0339-280">否</span><span class="sxs-lookup"><span data-stu-id="c0339-280">no</span></span>             | <span data-ttu-id="c0339-281">否</span><span class="sxs-lookup"><span data-stu-id="c0339-281">no</span></span>               |
| <span data-ttu-id="c0339-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="c0339-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="c0339-283">否</span><span class="sxs-lookup"><span data-stu-id="c0339-283">no</span></span>             | <span data-ttu-id="c0339-284">否</span><span class="sxs-lookup"><span data-stu-id="c0339-284">no</span></span>               |
| <span data-ttu-id="c0339-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="c0339-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="c0339-286">否</span><span class="sxs-lookup"><span data-stu-id="c0339-286">no</span></span>             | <span data-ttu-id="c0339-287">否</span><span class="sxs-lookup"><span data-stu-id="c0339-287">no</span></span>               |
| <span data-ttu-id="c0339-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="c0339-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="c0339-289">否</span><span class="sxs-lookup"><span data-stu-id="c0339-289">no</span></span>             | <span data-ttu-id="c0339-290">否</span><span class="sxs-lookup"><span data-stu-id="c0339-290">no</span></span>               |
| <span data-ttu-id="c0339-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="c0339-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="c0339-292">否</span><span class="sxs-lookup"><span data-stu-id="c0339-292">no</span></span>             | <span data-ttu-id="c0339-293">否</span><span class="sxs-lookup"><span data-stu-id="c0339-293">no</span></span>               |
| <span data-ttu-id="c0339-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="c0339-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="c0339-295">否</span><span class="sxs-lookup"><span data-stu-id="c0339-295">no</span></span>             | <span data-ttu-id="c0339-296">否</span><span class="sxs-lookup"><span data-stu-id="c0339-296">no</span></span>               |
| <span data-ttu-id="c0339-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="c0339-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="c0339-298">否</span><span class="sxs-lookup"><span data-stu-id="c0339-298">no</span></span>             | <span data-ttu-id="c0339-299">否</span><span class="sxs-lookup"><span data-stu-id="c0339-299">no</span></span>               |
| <span data-ttu-id="c0339-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="c0339-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="c0339-301">否</span><span class="sxs-lookup"><span data-stu-id="c0339-301">no</span></span>             | <span data-ttu-id="c0339-302">否</span><span class="sxs-lookup"><span data-stu-id="c0339-302">no</span></span>               |
| <span data-ttu-id="c0339-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="c0339-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="c0339-304">否</span><span class="sxs-lookup"><span data-stu-id="c0339-304">no</span></span>             | <span data-ttu-id="c0339-305">否</span><span class="sxs-lookup"><span data-stu-id="c0339-305">no</span></span>               |
| <span data-ttu-id="c0339-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="c0339-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="c0339-307">否</span><span class="sxs-lookup"><span data-stu-id="c0339-307">no</span></span>             | <span data-ttu-id="c0339-308">否</span><span class="sxs-lookup"><span data-stu-id="c0339-308">no</span></span>               |
| <span data-ttu-id="c0339-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="c0339-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="c0339-310">否</span><span class="sxs-lookup"><span data-stu-id="c0339-310">no</span></span>             | <span data-ttu-id="c0339-311">否</span><span class="sxs-lookup"><span data-stu-id="c0339-311">no</span></span>               |
| <span data-ttu-id="c0339-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="c0339-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="c0339-313">否</span><span class="sxs-lookup"><span data-stu-id="c0339-313">no</span></span>             | <span data-ttu-id="c0339-314">否</span><span class="sxs-lookup"><span data-stu-id="c0339-314">no</span></span>               |
| <span data-ttu-id="c0339-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="c0339-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="c0339-316">否</span><span class="sxs-lookup"><span data-stu-id="c0339-316">no</span></span>             | <span data-ttu-id="c0339-317">否</span><span class="sxs-lookup"><span data-stu-id="c0339-317">no</span></span>               |
| <span data-ttu-id="c0339-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="c0339-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="c0339-319">否</span><span class="sxs-lookup"><span data-stu-id="c0339-319">no</span></span>             | <span data-ttu-id="c0339-320">否</span><span class="sxs-lookup"><span data-stu-id="c0339-320">no</span></span>               |
| <span data-ttu-id="c0339-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="c0339-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="c0339-322">否</span><span class="sxs-lookup"><span data-stu-id="c0339-322">no</span></span>             | <span data-ttu-id="c0339-323">否</span><span class="sxs-lookup"><span data-stu-id="c0339-323">no</span></span>               |
| <span data-ttu-id="c0339-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="c0339-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="c0339-325">否</span><span class="sxs-lookup"><span data-stu-id="c0339-325">no</span></span>             | <span data-ttu-id="c0339-326">否</span><span class="sxs-lookup"><span data-stu-id="c0339-326">no</span></span>               |
| <span data-ttu-id="c0339-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="c0339-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="c0339-328">否</span><span class="sxs-lookup"><span data-stu-id="c0339-328">no</span></span>             | <span data-ttu-id="c0339-329">否</span><span class="sxs-lookup"><span data-stu-id="c0339-329">no</span></span>               |
| <span data-ttu-id="c0339-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="c0339-330">msdyn_summary</span></span>                          | <span data-ttu-id="c0339-331">否</span><span class="sxs-lookup"><span data-stu-id="c0339-331">no</span></span>             | <span data-ttu-id="c0339-332">否</span><span class="sxs-lookup"><span data-stu-id="c0339-332">no</span></span>               |
| <span data-ttu-id="c0339-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="c0339-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="c0339-334">否</span><span class="sxs-lookup"><span data-stu-id="c0339-334">no</span></span>             | <span data-ttu-id="c0339-335">否</span><span class="sxs-lookup"><span data-stu-id="c0339-335">no</span></span>               |
| <span data-ttu-id="c0339-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="c0339-337">否</span><span class="sxs-lookup"><span data-stu-id="c0339-337">no</span></span>             | <span data-ttu-id="c0339-338">否</span><span class="sxs-lookup"><span data-stu-id="c0339-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="c0339-339">專案工作相依性</span><span class="sxs-lookup"><span data-stu-id="c0339-339">Project task dependency</span></span>

| <span data-ttu-id="c0339-340">**邏輯名稱**</span><span class="sxs-lookup"><span data-stu-id="c0339-340">**Logical name**</span></span>              | <span data-ttu-id="c0339-341">**可以建立**</span><span class="sxs-lookup"><span data-stu-id="c0339-341">**Can create**</span></span> | <span data-ttu-id="c0339-342">**可以編輯**</span><span class="sxs-lookup"><span data-stu-id="c0339-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="c0339-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="c0339-343">msdyn_linktype</span></span>                | <span data-ttu-id="c0339-344">否</span><span class="sxs-lookup"><span data-stu-id="c0339-344">no</span></span>             | <span data-ttu-id="c0339-345">否</span><span class="sxs-lookup"><span data-stu-id="c0339-345">no</span></span>           |
| <span data-ttu-id="c0339-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="c0339-346">msdyn_linktypename</span></span>            | <span data-ttu-id="c0339-347">否</span><span class="sxs-lookup"><span data-stu-id="c0339-347">no</span></span>             | <span data-ttu-id="c0339-348">否</span><span class="sxs-lookup"><span data-stu-id="c0339-348">no</span></span>           |
| <span data-ttu-id="c0339-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="c0339-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="c0339-350">是</span><span class="sxs-lookup"><span data-stu-id="c0339-350">yes</span></span>            | <span data-ttu-id="c0339-351">否</span><span class="sxs-lookup"><span data-stu-id="c0339-351">no</span></span>           |
| <span data-ttu-id="c0339-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="c0339-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="c0339-353">是</span><span class="sxs-lookup"><span data-stu-id="c0339-353">yes</span></span>            | <span data-ttu-id="c0339-354">否</span><span class="sxs-lookup"><span data-stu-id="c0339-354">no</span></span>           |
| <span data-ttu-id="c0339-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="c0339-355">msdyn_project</span></span>                 | <span data-ttu-id="c0339-356">是</span><span class="sxs-lookup"><span data-stu-id="c0339-356">yes</span></span>            | <span data-ttu-id="c0339-357">否</span><span class="sxs-lookup"><span data-stu-id="c0339-357">no</span></span>           |
| <span data-ttu-id="c0339-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="c0339-358">msdyn_projectname</span></span>             | <span data-ttu-id="c0339-359">是</span><span class="sxs-lookup"><span data-stu-id="c0339-359">yes</span></span>            | <span data-ttu-id="c0339-360">否</span><span class="sxs-lookup"><span data-stu-id="c0339-360">no</span></span>           |
| <span data-ttu-id="c0339-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="c0339-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="c0339-362">是</span><span class="sxs-lookup"><span data-stu-id="c0339-362">yes</span></span>            | <span data-ttu-id="c0339-363">否</span><span class="sxs-lookup"><span data-stu-id="c0339-363">no</span></span>           |
| <span data-ttu-id="c0339-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="c0339-364">msdyn_successortask</span></span>           | <span data-ttu-id="c0339-365">是</span><span class="sxs-lookup"><span data-stu-id="c0339-365">yes</span></span>            | <span data-ttu-id="c0339-366">否</span><span class="sxs-lookup"><span data-stu-id="c0339-366">no</span></span>           |
| <span data-ttu-id="c0339-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="c0339-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="c0339-368">是</span><span class="sxs-lookup"><span data-stu-id="c0339-368">yes</span></span>            | <span data-ttu-id="c0339-369">否</span><span class="sxs-lookup"><span data-stu-id="c0339-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="c0339-370">資源指派</span><span class="sxs-lookup"><span data-stu-id="c0339-370">Resource assignment</span></span>

| <span data-ttu-id="c0339-371">**邏輯名稱**</span><span class="sxs-lookup"><span data-stu-id="c0339-371">**Logical name**</span></span>             | <span data-ttu-id="c0339-372">**可以建立**</span><span class="sxs-lookup"><span data-stu-id="c0339-372">**Can create**</span></span> | <span data-ttu-id="c0339-373">**可以編輯**</span><span class="sxs-lookup"><span data-stu-id="c0339-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="c0339-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="c0339-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="c0339-375">是</span><span class="sxs-lookup"><span data-stu-id="c0339-375">yes</span></span>            | <span data-ttu-id="c0339-376">否</span><span class="sxs-lookup"><span data-stu-id="c0339-376">no</span></span>           |
| <span data-ttu-id="c0339-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="c0339-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="c0339-378">是</span><span class="sxs-lookup"><span data-stu-id="c0339-378">yes</span></span>            | <span data-ttu-id="c0339-379">否</span><span class="sxs-lookup"><span data-stu-id="c0339-379">no</span></span>           |
| <span data-ttu-id="c0339-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="c0339-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="c0339-381">否</span><span class="sxs-lookup"><span data-stu-id="c0339-381">no</span></span>             | <span data-ttu-id="c0339-382">否</span><span class="sxs-lookup"><span data-stu-id="c0339-382">no</span></span>           |
| <span data-ttu-id="c0339-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="c0339-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="c0339-384">否</span><span class="sxs-lookup"><span data-stu-id="c0339-384">no</span></span>             | <span data-ttu-id="c0339-385">否</span><span class="sxs-lookup"><span data-stu-id="c0339-385">no</span></span>           |
| <span data-ttu-id="c0339-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="c0339-386">msdyn_committype</span></span>             | <span data-ttu-id="c0339-387">否</span><span class="sxs-lookup"><span data-stu-id="c0339-387">no</span></span>             | <span data-ttu-id="c0339-388">否</span><span class="sxs-lookup"><span data-stu-id="c0339-388">no</span></span>           |
| <span data-ttu-id="c0339-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="c0339-389">msdyn_committypename</span></span>         | <span data-ttu-id="c0339-390">否</span><span class="sxs-lookup"><span data-stu-id="c0339-390">no</span></span>             | <span data-ttu-id="c0339-391">否</span><span class="sxs-lookup"><span data-stu-id="c0339-391">no</span></span>           |
| <span data-ttu-id="c0339-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="c0339-392">msdyn_effort</span></span>                 | <span data-ttu-id="c0339-393">否</span><span class="sxs-lookup"><span data-stu-id="c0339-393">no</span></span>             | <span data-ttu-id="c0339-394">否</span><span class="sxs-lookup"><span data-stu-id="c0339-394">no</span></span>           |
| <span data-ttu-id="c0339-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="c0339-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="c0339-396">否</span><span class="sxs-lookup"><span data-stu-id="c0339-396">no</span></span>             | <span data-ttu-id="c0339-397">否</span><span class="sxs-lookup"><span data-stu-id="c0339-397">no</span></span>           |
| <span data-ttu-id="c0339-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="c0339-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="c0339-399">否</span><span class="sxs-lookup"><span data-stu-id="c0339-399">no</span></span>             | <span data-ttu-id="c0339-400">否</span><span class="sxs-lookup"><span data-stu-id="c0339-400">no</span></span>           |
| <span data-ttu-id="c0339-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="c0339-401">msdyn_finish</span></span>                 | <span data-ttu-id="c0339-402">否</span><span class="sxs-lookup"><span data-stu-id="c0339-402">no</span></span>             | <span data-ttu-id="c0339-403">否</span><span class="sxs-lookup"><span data-stu-id="c0339-403">no</span></span>           |
| <span data-ttu-id="c0339-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="c0339-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="c0339-405">否</span><span class="sxs-lookup"><span data-stu-id="c0339-405">no</span></span>             | <span data-ttu-id="c0339-406">否</span><span class="sxs-lookup"><span data-stu-id="c0339-406">no</span></span>           |
| <span data-ttu-id="c0339-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="c0339-408">否</span><span class="sxs-lookup"><span data-stu-id="c0339-408">no</span></span>             | <span data-ttu-id="c0339-409">否</span><span class="sxs-lookup"><span data-stu-id="c0339-409">no</span></span>           |
| <span data-ttu-id="c0339-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="c0339-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="c0339-411">否</span><span class="sxs-lookup"><span data-stu-id="c0339-411">no</span></span>             | <span data-ttu-id="c0339-412">否</span><span class="sxs-lookup"><span data-stu-id="c0339-412">no</span></span>           |
| <span data-ttu-id="c0339-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="c0339-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="c0339-414">否</span><span class="sxs-lookup"><span data-stu-id="c0339-414">no</span></span>             | <span data-ttu-id="c0339-415">否</span><span class="sxs-lookup"><span data-stu-id="c0339-415">no</span></span>           |
| <span data-ttu-id="c0339-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="c0339-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="c0339-417">否</span><span class="sxs-lookup"><span data-stu-id="c0339-417">no</span></span>             | <span data-ttu-id="c0339-418">否</span><span class="sxs-lookup"><span data-stu-id="c0339-418">no</span></span>           |
| <span data-ttu-id="c0339-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="c0339-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="c0339-420">否</span><span class="sxs-lookup"><span data-stu-id="c0339-420">no</span></span>             | <span data-ttu-id="c0339-421">否</span><span class="sxs-lookup"><span data-stu-id="c0339-421">no</span></span>           |
| <span data-ttu-id="c0339-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="c0339-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="c0339-423">否</span><span class="sxs-lookup"><span data-stu-id="c0339-423">no</span></span>             | <span data-ttu-id="c0339-424">否</span><span class="sxs-lookup"><span data-stu-id="c0339-424">no</span></span>           |
| <span data-ttu-id="c0339-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="c0339-425">msdyn_projectid</span></span>              | <span data-ttu-id="c0339-426">是</span><span class="sxs-lookup"><span data-stu-id="c0339-426">yes</span></span>            | <span data-ttu-id="c0339-427">否</span><span class="sxs-lookup"><span data-stu-id="c0339-427">no</span></span>           |
| <span data-ttu-id="c0339-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="c0339-428">msdyn_projectidname</span></span>          | <span data-ttu-id="c0339-429">否</span><span class="sxs-lookup"><span data-stu-id="c0339-429">no</span></span>             | <span data-ttu-id="c0339-430">否</span><span class="sxs-lookup"><span data-stu-id="c0339-430">no</span></span>           |
| <span data-ttu-id="c0339-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="c0339-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="c0339-432">否</span><span class="sxs-lookup"><span data-stu-id="c0339-432">no</span></span>             | <span data-ttu-id="c0339-433">否</span><span class="sxs-lookup"><span data-stu-id="c0339-433">no</span></span>           |
| <span data-ttu-id="c0339-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="c0339-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="c0339-435">否</span><span class="sxs-lookup"><span data-stu-id="c0339-435">no</span></span>             | <span data-ttu-id="c0339-436">否</span><span class="sxs-lookup"><span data-stu-id="c0339-436">no</span></span>           |
| <span data-ttu-id="c0339-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="c0339-437">msdyn_start</span></span>                  | <span data-ttu-id="c0339-438">否</span><span class="sxs-lookup"><span data-stu-id="c0339-438">no</span></span>             | <span data-ttu-id="c0339-439">否</span><span class="sxs-lookup"><span data-stu-id="c0339-439">no</span></span>           |
| <span data-ttu-id="c0339-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="c0339-440">msdyn_taskid</span></span>                 | <span data-ttu-id="c0339-441">否</span><span class="sxs-lookup"><span data-stu-id="c0339-441">no</span></span>             | <span data-ttu-id="c0339-442">否</span><span class="sxs-lookup"><span data-stu-id="c0339-442">no</span></span>           |
| <span data-ttu-id="c0339-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="c0339-443">msdyn_taskidname</span></span>             | <span data-ttu-id="c0339-444">否</span><span class="sxs-lookup"><span data-stu-id="c0339-444">no</span></span>             | <span data-ttu-id="c0339-445">否</span><span class="sxs-lookup"><span data-stu-id="c0339-445">no</span></span>           |
| <span data-ttu-id="c0339-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="c0339-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="c0339-447">否</span><span class="sxs-lookup"><span data-stu-id="c0339-447">no</span></span>             | <span data-ttu-id="c0339-448">否</span><span class="sxs-lookup"><span data-stu-id="c0339-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="c0339-449">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="c0339-449">Project team member</span></span>

| <span data-ttu-id="c0339-450">**邏輯名稱**</span><span class="sxs-lookup"><span data-stu-id="c0339-450">**Logical name**</span></span>                                 | <span data-ttu-id="c0339-451">**可以建立**</span><span class="sxs-lookup"><span data-stu-id="c0339-451">**Can create**</span></span> | <span data-ttu-id="c0339-452">**可以編輯**</span><span class="sxs-lookup"><span data-stu-id="c0339-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="c0339-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="c0339-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="c0339-454">否</span><span class="sxs-lookup"><span data-stu-id="c0339-454">no</span></span>             | <span data-ttu-id="c0339-455">否</span><span class="sxs-lookup"><span data-stu-id="c0339-455">no</span></span>           |
| <span data-ttu-id="c0339-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="c0339-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="c0339-457">否</span><span class="sxs-lookup"><span data-stu-id="c0339-457">no</span></span>             | <span data-ttu-id="c0339-458">否</span><span class="sxs-lookup"><span data-stu-id="c0339-458">no</span></span>           |
| <span data-ttu-id="c0339-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="c0339-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="c0339-460">否</span><span class="sxs-lookup"><span data-stu-id="c0339-460">no</span></span>             | <span data-ttu-id="c0339-461">否</span><span class="sxs-lookup"><span data-stu-id="c0339-461">no</span></span>           |
| <span data-ttu-id="c0339-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="c0339-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="c0339-463">否</span><span class="sxs-lookup"><span data-stu-id="c0339-463">no</span></span>             | <span data-ttu-id="c0339-464">否</span><span class="sxs-lookup"><span data-stu-id="c0339-464">no</span></span>           |
| <span data-ttu-id="c0339-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="c0339-465">msdyn_effort</span></span>                                     | <span data-ttu-id="c0339-466">否</span><span class="sxs-lookup"><span data-stu-id="c0339-466">no</span></span>             | <span data-ttu-id="c0339-467">否</span><span class="sxs-lookup"><span data-stu-id="c0339-467">no</span></span>           |
| <span data-ttu-id="c0339-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="c0339-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="c0339-469">否</span><span class="sxs-lookup"><span data-stu-id="c0339-469">no</span></span>             | <span data-ttu-id="c0339-470">否</span><span class="sxs-lookup"><span data-stu-id="c0339-470">no</span></span>           |
| <span data-ttu-id="c0339-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="c0339-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="c0339-472">否</span><span class="sxs-lookup"><span data-stu-id="c0339-472">no</span></span>             | <span data-ttu-id="c0339-473">否</span><span class="sxs-lookup"><span data-stu-id="c0339-473">no</span></span>           |
| <span data-ttu-id="c0339-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="c0339-474">msdyn_finish</span></span>                                     | <span data-ttu-id="c0339-475">否</span><span class="sxs-lookup"><span data-stu-id="c0339-475">no</span></span>             | <span data-ttu-id="c0339-476">否</span><span class="sxs-lookup"><span data-stu-id="c0339-476">no</span></span>           |
| <span data-ttu-id="c0339-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="c0339-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="c0339-478">否</span><span class="sxs-lookup"><span data-stu-id="c0339-478">no</span></span>             | <span data-ttu-id="c0339-479">否</span><span class="sxs-lookup"><span data-stu-id="c0339-479">no</span></span>           |
| <span data-ttu-id="c0339-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="c0339-480">msdyn_hours</span></span>                                      | <span data-ttu-id="c0339-481">否</span><span class="sxs-lookup"><span data-stu-id="c0339-481">no</span></span>             | <span data-ttu-id="c0339-482">否</span><span class="sxs-lookup"><span data-stu-id="c0339-482">no</span></span>           |
| <span data-ttu-id="c0339-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="c0339-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="c0339-484">否</span><span class="sxs-lookup"><span data-stu-id="c0339-484">no</span></span>             | <span data-ttu-id="c0339-485">否</span><span class="sxs-lookup"><span data-stu-id="c0339-485">no</span></span>           |
| <span data-ttu-id="c0339-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="c0339-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="c0339-487">否</span><span class="sxs-lookup"><span data-stu-id="c0339-487">no</span></span>             | <span data-ttu-id="c0339-488">否</span><span class="sxs-lookup"><span data-stu-id="c0339-488">no</span></span>           |
| <span data-ttu-id="c0339-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="c0339-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="c0339-490">否</span><span class="sxs-lookup"><span data-stu-id="c0339-490">no</span></span>             | <span data-ttu-id="c0339-491">否</span><span class="sxs-lookup"><span data-stu-id="c0339-491">no</span></span>           |
| <span data-ttu-id="c0339-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="c0339-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="c0339-493">否</span><span class="sxs-lookup"><span data-stu-id="c0339-493">no</span></span>             | <span data-ttu-id="c0339-494">否</span><span class="sxs-lookup"><span data-stu-id="c0339-494">no</span></span>           |
| <span data-ttu-id="c0339-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="c0339-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="c0339-496">否</span><span class="sxs-lookup"><span data-stu-id="c0339-496">no</span></span>             | <span data-ttu-id="c0339-497">否</span><span class="sxs-lookup"><span data-stu-id="c0339-497">no</span></span>           |
| <span data-ttu-id="c0339-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="c0339-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="c0339-499">否</span><span class="sxs-lookup"><span data-stu-id="c0339-499">no</span></span>             | <span data-ttu-id="c0339-500">否</span><span class="sxs-lookup"><span data-stu-id="c0339-500">no</span></span>           |
| <span data-ttu-id="c0339-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="c0339-501">msdyn_start</span></span>                                      | <span data-ttu-id="c0339-502">否</span><span class="sxs-lookup"><span data-stu-id="c0339-502">no</span></span>             | <span data-ttu-id="c0339-503">否</span><span class="sxs-lookup"><span data-stu-id="c0339-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="c0339-504">Project</span><span class="sxs-lookup"><span data-stu-id="c0339-504">Project</span></span>

| <span data-ttu-id="c0339-505">**邏輯名稱**</span><span class="sxs-lookup"><span data-stu-id="c0339-505">**Logical name**</span></span>                       | <span data-ttu-id="c0339-506">**可以建立**</span><span class="sxs-lookup"><span data-stu-id="c0339-506">**Can create**</span></span> | <span data-ttu-id="c0339-507">**可以編輯**</span><span class="sxs-lookup"><span data-stu-id="c0339-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="c0339-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="c0339-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="c0339-509">否</span><span class="sxs-lookup"><span data-stu-id="c0339-509">no</span></span>             | <span data-ttu-id="c0339-510">否</span><span class="sxs-lookup"><span data-stu-id="c0339-510">no</span></span>           |
| <span data-ttu-id="c0339-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="c0339-512">否</span><span class="sxs-lookup"><span data-stu-id="c0339-512">no</span></span>             | <span data-ttu-id="c0339-513">否</span><span class="sxs-lookup"><span data-stu-id="c0339-513">no</span></span>           |
| <span data-ttu-id="c0339-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="c0339-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="c0339-515">否</span><span class="sxs-lookup"><span data-stu-id="c0339-515">no</span></span>             | <span data-ttu-id="c0339-516">否</span><span class="sxs-lookup"><span data-stu-id="c0339-516">no</span></span>           |
| <span data-ttu-id="c0339-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="c0339-518">否</span><span class="sxs-lookup"><span data-stu-id="c0339-518">no</span></span>             | <span data-ttu-id="c0339-519">否</span><span class="sxs-lookup"><span data-stu-id="c0339-519">no</span></span>           |
| <span data-ttu-id="c0339-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="c0339-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="c0339-521">否</span><span class="sxs-lookup"><span data-stu-id="c0339-521">no</span></span>             | <span data-ttu-id="c0339-522">否</span><span class="sxs-lookup"><span data-stu-id="c0339-522">no</span></span>           |
| <span data-ttu-id="c0339-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="c0339-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="c0339-524">否</span><span class="sxs-lookup"><span data-stu-id="c0339-524">no</span></span>             | <span data-ttu-id="c0339-525">否</span><span class="sxs-lookup"><span data-stu-id="c0339-525">no</span></span>           |
| <span data-ttu-id="c0339-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="c0339-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="c0339-527">是</span><span class="sxs-lookup"><span data-stu-id="c0339-527">yes</span></span>            | <span data-ttu-id="c0339-528">否</span><span class="sxs-lookup"><span data-stu-id="c0339-528">no</span></span>           |
| <span data-ttu-id="c0339-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="c0339-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="c0339-530">是</span><span class="sxs-lookup"><span data-stu-id="c0339-530">yes</span></span>            | <span data-ttu-id="c0339-531">否</span><span class="sxs-lookup"><span data-stu-id="c0339-531">no</span></span>           |
| <span data-ttu-id="c0339-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="c0339-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="c0339-533">是</span><span class="sxs-lookup"><span data-stu-id="c0339-533">yes</span></span>            | <span data-ttu-id="c0339-534">否</span><span class="sxs-lookup"><span data-stu-id="c0339-534">no</span></span>           |
| <span data-ttu-id="c0339-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="c0339-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="c0339-536">否</span><span class="sxs-lookup"><span data-stu-id="c0339-536">no</span></span>             | <span data-ttu-id="c0339-537">否</span><span class="sxs-lookup"><span data-stu-id="c0339-537">no</span></span>           |
| <span data-ttu-id="c0339-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="c0339-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="c0339-539">否</span><span class="sxs-lookup"><span data-stu-id="c0339-539">no</span></span>             | <span data-ttu-id="c0339-540">否</span><span class="sxs-lookup"><span data-stu-id="c0339-540">no</span></span>           |
| <span data-ttu-id="c0339-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="c0339-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="c0339-542">否</span><span class="sxs-lookup"><span data-stu-id="c0339-542">no</span></span>             | <span data-ttu-id="c0339-543">否</span><span class="sxs-lookup"><span data-stu-id="c0339-543">no</span></span>           |
| <span data-ttu-id="c0339-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="c0339-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="c0339-545">否</span><span class="sxs-lookup"><span data-stu-id="c0339-545">no</span></span>             | <span data-ttu-id="c0339-546">否</span><span class="sxs-lookup"><span data-stu-id="c0339-546">no</span></span>           |
| <span data-ttu-id="c0339-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="c0339-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="c0339-548">否</span><span class="sxs-lookup"><span data-stu-id="c0339-548">no</span></span>             | <span data-ttu-id="c0339-549">否</span><span class="sxs-lookup"><span data-stu-id="c0339-549">no</span></span>           |
| <span data-ttu-id="c0339-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="c0339-550">msdyn_duration</span></span>                         | <span data-ttu-id="c0339-551">否</span><span class="sxs-lookup"><span data-stu-id="c0339-551">no</span></span>             | <span data-ttu-id="c0339-552">否</span><span class="sxs-lookup"><span data-stu-id="c0339-552">no</span></span>           |
| <span data-ttu-id="c0339-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="c0339-553">msdyn_effort</span></span>                           | <span data-ttu-id="c0339-554">否</span><span class="sxs-lookup"><span data-stu-id="c0339-554">no</span></span>             | <span data-ttu-id="c0339-555">否</span><span class="sxs-lookup"><span data-stu-id="c0339-555">no</span></span>           |
| <span data-ttu-id="c0339-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="c0339-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="c0339-557">否</span><span class="sxs-lookup"><span data-stu-id="c0339-557">no</span></span>             | <span data-ttu-id="c0339-558">否</span><span class="sxs-lookup"><span data-stu-id="c0339-558">no</span></span>           |
| <span data-ttu-id="c0339-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="c0339-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="c0339-560">否</span><span class="sxs-lookup"><span data-stu-id="c0339-560">no</span></span>             | <span data-ttu-id="c0339-561">否</span><span class="sxs-lookup"><span data-stu-id="c0339-561">no</span></span>           |
| <span data-ttu-id="c0339-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="c0339-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="c0339-563">否</span><span class="sxs-lookup"><span data-stu-id="c0339-563">no</span></span>             | <span data-ttu-id="c0339-564">否</span><span class="sxs-lookup"><span data-stu-id="c0339-564">no</span></span>           |
| <span data-ttu-id="c0339-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="c0339-565">msdyn_finish</span></span>                           | <span data-ttu-id="c0339-566">是</span><span class="sxs-lookup"><span data-stu-id="c0339-566">yes</span></span>            | <span data-ttu-id="c0339-567">是</span><span class="sxs-lookup"><span data-stu-id="c0339-567">yes</span></span>          |
| <span data-ttu-id="c0339-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="c0339-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="c0339-569">否</span><span class="sxs-lookup"><span data-stu-id="c0339-569">no</span></span>             | <span data-ttu-id="c0339-570">否</span><span class="sxs-lookup"><span data-stu-id="c0339-570">no</span></span>           |
| <span data-ttu-id="c0339-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="c0339-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="c0339-572">否</span><span class="sxs-lookup"><span data-stu-id="c0339-572">no</span></span>             | <span data-ttu-id="c0339-573">否</span><span class="sxs-lookup"><span data-stu-id="c0339-573">no</span></span>           |
| <span data-ttu-id="c0339-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="c0339-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="c0339-575">否</span><span class="sxs-lookup"><span data-stu-id="c0339-575">no</span></span>             | <span data-ttu-id="c0339-576">否</span><span class="sxs-lookup"><span data-stu-id="c0339-576">no</span></span>           |
| <span data-ttu-id="c0339-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="c0339-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="c0339-578">否</span><span class="sxs-lookup"><span data-stu-id="c0339-578">no</span></span>             | <span data-ttu-id="c0339-579">否</span><span class="sxs-lookup"><span data-stu-id="c0339-579">no</span></span>           |
| <span data-ttu-id="c0339-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="c0339-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="c0339-581">否</span><span class="sxs-lookup"><span data-stu-id="c0339-581">no</span></span>             | <span data-ttu-id="c0339-582">否</span><span class="sxs-lookup"><span data-stu-id="c0339-582">no</span></span>           |
| <span data-ttu-id="c0339-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="c0339-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="c0339-584">否</span><span class="sxs-lookup"><span data-stu-id="c0339-584">no</span></span>             | <span data-ttu-id="c0339-585">否</span><span class="sxs-lookup"><span data-stu-id="c0339-585">no</span></span>           |
| <span data-ttu-id="c0339-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="c0339-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="c0339-587">否</span><span class="sxs-lookup"><span data-stu-id="c0339-587">no</span></span>             | <span data-ttu-id="c0339-588">否</span><span class="sxs-lookup"><span data-stu-id="c0339-588">no</span></span>           |
| <span data-ttu-id="c0339-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="c0339-590">否</span><span class="sxs-lookup"><span data-stu-id="c0339-590">no</span></span>             | <span data-ttu-id="c0339-591">否</span><span class="sxs-lookup"><span data-stu-id="c0339-591">no</span></span>           |
| <span data-ttu-id="c0339-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="c0339-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="c0339-593">否</span><span class="sxs-lookup"><span data-stu-id="c0339-593">no</span></span>             | <span data-ttu-id="c0339-594">否</span><span class="sxs-lookup"><span data-stu-id="c0339-594">no</span></span>           |
| <span data-ttu-id="c0339-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="c0339-596">否</span><span class="sxs-lookup"><span data-stu-id="c0339-596">no</span></span>             | <span data-ttu-id="c0339-597">否</span><span class="sxs-lookup"><span data-stu-id="c0339-597">no</span></span>           |
| <span data-ttu-id="c0339-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="c0339-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="c0339-599">否</span><span class="sxs-lookup"><span data-stu-id="c0339-599">no</span></span>             | <span data-ttu-id="c0339-600">否</span><span class="sxs-lookup"><span data-stu-id="c0339-600">no</span></span>           |
| <span data-ttu-id="c0339-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="c0339-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="c0339-602">否</span><span class="sxs-lookup"><span data-stu-id="c0339-602">no</span></span>             | <span data-ttu-id="c0339-603">否</span><span class="sxs-lookup"><span data-stu-id="c0339-603">no</span></span>           |
| <span data-ttu-id="c0339-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="c0339-604">msdyn_progress</span></span>                         | <span data-ttu-id="c0339-605">否</span><span class="sxs-lookup"><span data-stu-id="c0339-605">no</span></span>             | <span data-ttu-id="c0339-606">否</span><span class="sxs-lookup"><span data-stu-id="c0339-606">no</span></span>           |
| <span data-ttu-id="c0339-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="c0339-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="c0339-608">否</span><span class="sxs-lookup"><span data-stu-id="c0339-608">no</span></span>             | <span data-ttu-id="c0339-609">否</span><span class="sxs-lookup"><span data-stu-id="c0339-609">no</span></span>           |
| <span data-ttu-id="c0339-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="c0339-611">否</span><span class="sxs-lookup"><span data-stu-id="c0339-611">no</span></span>             | <span data-ttu-id="c0339-612">否</span><span class="sxs-lookup"><span data-stu-id="c0339-612">no</span></span>           |
| <span data-ttu-id="c0339-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="c0339-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="c0339-614">否</span><span class="sxs-lookup"><span data-stu-id="c0339-614">no</span></span>             | <span data-ttu-id="c0339-615">否</span><span class="sxs-lookup"><span data-stu-id="c0339-615">no</span></span>           |
| <span data-ttu-id="c0339-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="c0339-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="c0339-617">否</span><span class="sxs-lookup"><span data-stu-id="c0339-617">no</span></span>             | <span data-ttu-id="c0339-618">否</span><span class="sxs-lookup"><span data-stu-id="c0339-618">no</span></span>           |
| <span data-ttu-id="c0339-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="c0339-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="c0339-620">否</span><span class="sxs-lookup"><span data-stu-id="c0339-620">no</span></span>             | <span data-ttu-id="c0339-621">否</span><span class="sxs-lookup"><span data-stu-id="c0339-621">no</span></span>           |
| <span data-ttu-id="c0339-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="c0339-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="c0339-623">否</span><span class="sxs-lookup"><span data-stu-id="c0339-623">no</span></span>             | <span data-ttu-id="c0339-624">否</span><span class="sxs-lookup"><span data-stu-id="c0339-624">no</span></span>           |
| <span data-ttu-id="c0339-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="c0339-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="c0339-626">否</span><span class="sxs-lookup"><span data-stu-id="c0339-626">no</span></span>             | <span data-ttu-id="c0339-627">否</span><span class="sxs-lookup"><span data-stu-id="c0339-627">no</span></span>           |
| <span data-ttu-id="c0339-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="c0339-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="c0339-629">否</span><span class="sxs-lookup"><span data-stu-id="c0339-629">no</span></span>             | <span data-ttu-id="c0339-630">否</span><span class="sxs-lookup"><span data-stu-id="c0339-630">no</span></span>           |
| <span data-ttu-id="c0339-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="c0339-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="c0339-632">否</span><span class="sxs-lookup"><span data-stu-id="c0339-632">no</span></span>             | <span data-ttu-id="c0339-633">否</span><span class="sxs-lookup"><span data-stu-id="c0339-633">no</span></span>           |
| <span data-ttu-id="c0339-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="c0339-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="c0339-635">否</span><span class="sxs-lookup"><span data-stu-id="c0339-635">no</span></span>             | <span data-ttu-id="c0339-636">否</span><span class="sxs-lookup"><span data-stu-id="c0339-636">no</span></span>           |
| <span data-ttu-id="c0339-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="c0339-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="c0339-638">否</span><span class="sxs-lookup"><span data-stu-id="c0339-638">no</span></span>             | <span data-ttu-id="c0339-639">否</span><span class="sxs-lookup"><span data-stu-id="c0339-639">no</span></span>           |
| <span data-ttu-id="c0339-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="c0339-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="c0339-641">否</span><span class="sxs-lookup"><span data-stu-id="c0339-641">no</span></span>             | <span data-ttu-id="c0339-642">否</span><span class="sxs-lookup"><span data-stu-id="c0339-642">no</span></span>           |
| <span data-ttu-id="c0339-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="c0339-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="c0339-644">否</span><span class="sxs-lookup"><span data-stu-id="c0339-644">no</span></span>             | <span data-ttu-id="c0339-645">否</span><span class="sxs-lookup"><span data-stu-id="c0339-645">no</span></span>           |
| <span data-ttu-id="c0339-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="c0339-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="c0339-647">否</span><span class="sxs-lookup"><span data-stu-id="c0339-647">no</span></span>             | <span data-ttu-id="c0339-648">否</span><span class="sxs-lookup"><span data-stu-id="c0339-648">no</span></span>           |
| <span data-ttu-id="c0339-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="c0339-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="c0339-650">否</span><span class="sxs-lookup"><span data-stu-id="c0339-650">no</span></span>             | <span data-ttu-id="c0339-651">否</span><span class="sxs-lookup"><span data-stu-id="c0339-651">no</span></span>           |
| <span data-ttu-id="c0339-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="c0339-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="c0339-653">否</span><span class="sxs-lookup"><span data-stu-id="c0339-653">no</span></span>             | <span data-ttu-id="c0339-654">否</span><span class="sxs-lookup"><span data-stu-id="c0339-654">no</span></span>           |
| <span data-ttu-id="c0339-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="c0339-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="c0339-656">否</span><span class="sxs-lookup"><span data-stu-id="c0339-656">no</span></span>             | <span data-ttu-id="c0339-657">否</span><span class="sxs-lookup"><span data-stu-id="c0339-657">no</span></span>           |
| <span data-ttu-id="c0339-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="c0339-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="c0339-659">否</span><span class="sxs-lookup"><span data-stu-id="c0339-659">no</span></span>             | <span data-ttu-id="c0339-660">否</span><span class="sxs-lookup"><span data-stu-id="c0339-660">no</span></span>           |
| <span data-ttu-id="c0339-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="c0339-662">否</span><span class="sxs-lookup"><span data-stu-id="c0339-662">no</span></span>             | <span data-ttu-id="c0339-663">否</span><span class="sxs-lookup"><span data-stu-id="c0339-663">no</span></span>           |
| <span data-ttu-id="c0339-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="c0339-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="c0339-665">否</span><span class="sxs-lookup"><span data-stu-id="c0339-665">no</span></span>             | <span data-ttu-id="c0339-666">否</span><span class="sxs-lookup"><span data-stu-id="c0339-666">no</span></span>           |
| <span data-ttu-id="c0339-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="c0339-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="c0339-668">否</span><span class="sxs-lookup"><span data-stu-id="c0339-668">no</span></span>             | <span data-ttu-id="c0339-669">否</span><span class="sxs-lookup"><span data-stu-id="c0339-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="c0339-670">限制和已知問題</span><span class="sxs-lookup"><span data-stu-id="c0339-670">Limitations and known issues</span></span>
<span data-ttu-id="c0339-671">以下是限制和已知問題的清單：</span><span class="sxs-lookup"><span data-stu-id="c0339-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="c0339-672">只有 **擁有 Microsoft Project 授權的使用者** 才可以使用排程 API。</span><span class="sxs-lookup"><span data-stu-id="c0339-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="c0339-673">無法供下列使用者使用：</span><span class="sxs-lookup"><span data-stu-id="c0339-673">They can't be used by:</span></span>
    - <span data-ttu-id="c0339-674">應用程式使用者</span><span class="sxs-lookup"><span data-stu-id="c0339-674">Application users</span></span>
    - <span data-ttu-id="c0339-675">系統使用者</span><span class="sxs-lookup"><span data-stu-id="c0339-675">System users</span></span>
    - <span data-ttu-id="c0339-676">整合使用者</span><span class="sxs-lookup"><span data-stu-id="c0339-676">Integration users</span></span>
    - <span data-ttu-id="c0339-677">其他沒有必要授權的使用者</span><span class="sxs-lookup"><span data-stu-id="c0339-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="c0339-678">每個 **OperationSet** 最多只能有 100 項作業。</span><span class="sxs-lookup"><span data-stu-id="c0339-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="c0339-679">每個使用者最多只能有 10 個已開啟的 **OperationSet**。</span><span class="sxs-lookup"><span data-stu-id="c0339-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="c0339-680">Project Operations 目前在專案中最多支援總計 500 個工作。</span><span class="sxs-lookup"><span data-stu-id="c0339-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="c0339-681">**OperationSet** 失敗狀態和失敗記錄目前未提供。</span><span class="sxs-lookup"><span data-stu-id="c0339-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="c0339-682">專案和工作的限制與界限</span><span class="sxs-lookup"><span data-stu-id="c0339-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="c0339-683">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="c0339-683">Error handling</span></span>

   - <span data-ttu-id="c0339-684">若要檢閱由作業集所產生的錯誤，請移至 **設定** \> **排程整合** \> **作業集**。</span><span class="sxs-lookup"><span data-stu-id="c0339-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="c0339-685">若要檢閱專案排程服務所產生的錯誤，請移至 **設定** \> **排程整合** \> **PSS 錯誤記錄**。</span><span class="sxs-lookup"><span data-stu-id="c0339-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="c0339-686">範例案例</span><span class="sxs-lookup"><span data-stu-id="c0339-686">Sample scenario</span></span>

<span data-ttu-id="c0339-687">在此案例中，您將會建立專案、團隊成員、四個工作和兩個資源指派。</span><span class="sxs-lookup"><span data-stu-id="c0339-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="c0339-688">接下來，會更新一項工作、更新專案、刪除一項工作、刪除一個資源指派，以及建立工作相依性。</span><span class="sxs-lookup"><span data-stu-id="c0339-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="c0339-689">其他範例</span><span class="sxs-lookup"><span data-stu-id="c0339-689">Additional samples</span></span>

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
    task["msdyn_progress"] = 0.34m;
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
