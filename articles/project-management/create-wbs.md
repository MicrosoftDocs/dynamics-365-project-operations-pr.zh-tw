---
title: 建立分工結構圖
description: 本主題說明如何在新的排程介面中建立包含基本控制項的分工結構圖 (WBS)。
author: ruhercul
ms.date: 01/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ac3facacd95e5e677635cb037d0d3458da612410
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005691"
---
# <a name="create-a-work-breakdown-structure-wbs"></a><span data-ttu-id="bf078-103">建立分工結構圖 (WBS)</span><span class="sxs-lookup"><span data-stu-id="bf078-103">Create a work breakdown structure (WBS)</span></span>

<span data-ttu-id="bf078-104">專案排程會溝通必須完成什麼作業、哪些資源將執行此作業，以及必須完成作業的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="bf078-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe in which the work must be completed.</span></span> <span data-ttu-id="bf078-105">排程會反映所有與按時交付專案相關的作業。</span><span class="sxs-lookup"><span data-stu-id="bf078-105">The schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="bf078-106">在 Dynamics 365 Project Operations 中，您可以透過下列方式建立專案排程：</span><span class="sxs-lookup"><span data-stu-id="bf078-106">In Dynamics 365 Project Operations, you create a project schedule by:</span></span>

  - <span data-ttu-id="bf078-107">將作業細分成易於管理的工作。</span><span class="sxs-lookup"><span data-stu-id="bf078-107">Breaking the work down into manageable tasks.</span></span>
  - <span data-ttu-id="bf078-108">估計完成每個工作所需的時間。</span><span class="sxs-lookup"><span data-stu-id="bf078-108">Estimating the time that is required to do each task.</span></span>
  - <span data-ttu-id="bf078-109">設定工作相依性。</span><span class="sxs-lookup"><span data-stu-id="bf078-109">Setting task dependencies.</span></span>
  - <span data-ttu-id="bf078-110">設定工作期間。</span><span class="sxs-lookup"><span data-stu-id="bf078-110">Setting task durations.</span></span>
  - <span data-ttu-id="bf078-111">估計會執行這些工作的一般資源。</span><span class="sxs-lookup"><span data-stu-id="bf078-111">Estimating the generic resources that will do the tasks.</span></span> 

<span data-ttu-id="bf078-112">專案排程是透過 **專案** 頁面上的 **排程** 索引標籤來建立。</span><span class="sxs-lookup"><span data-stu-id="bf078-112">The project schedule is created on the **Schedule** tab on the **Project** page.</span></span>

## <a name="tasks"></a><span data-ttu-id="bf078-113">工作</span><span class="sxs-lookup"><span data-stu-id="bf078-113">Tasks</span></span>

<span data-ttu-id="bf078-114">建立專案排程的第一個步驟是將作業細分為易於管理的部分。</span><span class="sxs-lookup"><span data-stu-id="bf078-114">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="bf078-115">Project Operations 中的排程支援下列功能：</span><span class="sxs-lookup"><span data-stu-id="bf078-115">The schedule in Project Operations supports the following features:</span></span>

- <span data-ttu-id="bf078-116">摘要或容器工作</span><span class="sxs-lookup"><span data-stu-id="bf078-116">Summary or container tasks</span></span>
- <span data-ttu-id="bf078-117">分葉節點工作</span><span class="sxs-lookup"><span data-stu-id="bf078-117">Leaf node tasks</span></span>

### <a name="summary-tasks"></a><span data-ttu-id="bf078-118">摘要工作</span><span class="sxs-lookup"><span data-stu-id="bf078-118">Summary tasks</span></span>

<span data-ttu-id="bf078-119">摘要工作可以儲存其他摘要工作或分葉節點工作。</span><span class="sxs-lookup"><span data-stu-id="bf078-119">Summary tasks can store other summary tasks or leaf node tasks.</span></span> <span data-ttu-id="bf078-120">這些工作沒有其本身的作業投入量或成本。</span><span class="sxs-lookup"><span data-stu-id="bf078-120">They have no work effort or cost of their own.</span></span> <span data-ttu-id="bf078-121">相反的，其作業投入量和成本是其容器工作之作業投入量與成本的彙總。</span><span class="sxs-lookup"><span data-stu-id="bf078-121">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="bf078-122">摘要工作的開始日期是容器工作的開始日期，而結束日期是容器工作的結束日期。</span><span class="sxs-lookup"><span data-stu-id="bf078-122">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="bf078-123">您可以編輯摘要工作的名稱，但是無法編輯排程屬性，包括投入量、日期和期間。</span><span class="sxs-lookup"><span data-stu-id="bf078-123">The name of a summary task can be edited, but scheduling properties, including effort, dates, and duration, can't be edited.</span></span> <span data-ttu-id="bf078-124">若刪除摘要工作，也會刪除其所有的容器工作。</span><span class="sxs-lookup"><span data-stu-id="bf078-124">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="bf078-125">分葉節點工作</span><span class="sxs-lookup"><span data-stu-id="bf078-125">Leaf node tasks</span></span>

<span data-ttu-id="bf078-126">分葉節點工作表示專案中最細微的作業。</span><span class="sxs-lookup"><span data-stu-id="bf078-126">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="bf078-127">這些工作有估計投入量、資源、規劃開始和結束日期，以及期間。</span><span class="sxs-lookup"><span data-stu-id="bf078-127">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>

## <a name="create-a-task-hierarchy"></a><span data-ttu-id="bf078-128">建立工作階層</span><span class="sxs-lookup"><span data-stu-id="bf078-128">Create a task hierarchy</span></span>

### <a name="add-a-task"></a><span data-ttu-id="bf078-129">新增工作</span><span class="sxs-lookup"><span data-stu-id="bf078-129">Add a task</span></span>

<span data-ttu-id="bf078-130">完成下列步驟以新增一個或多個工作。</span><span class="sxs-lookup"><span data-stu-id="bf078-130">Complete the following steps to add one or more tasks.</span></span>

1. <span data-ttu-id="bf078-131">移至 **專案**，然後選取並開啟需要建立排程的專案記錄。</span><span class="sxs-lookup"><span data-stu-id="bf078-131">Go to **Projects** and select and open the project record for which you want to create a schedule.</span></span> 
2. <span data-ttu-id="bf078-132">選取 **工作** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="bf078-132">Select the **Tasks** tab.</span></span> 
3. <span data-ttu-id="bf078-133">選取 **新增工作**、輸入工作的名稱，然後按 Enter。</span><span class="sxs-lookup"><span data-stu-id="bf078-133">Select **Add new task**, enter a name for the task, and then press Enter.</span></span>
2. <span data-ttu-id="bf078-134">輸入另一個工作名稱，然後再按一次 Enter，直到有完整的工作清單為止。</span><span class="sxs-lookup"><span data-stu-id="bf078-134">Enter another task name and press Enter again until you have a full list of tasks.</span></span>

### <a name="manage-hierarchy-of-a-task"></a><span data-ttu-id="bf078-135">管理工作的階層</span><span class="sxs-lookup"><span data-stu-id="bf078-135">Manage hierarchy of a task</span></span>

<span data-ttu-id="bf078-136">工作縮排時，此工作會變成其上方緊鄰工作的下層。</span><span class="sxs-lookup"><span data-stu-id="bf078-136">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="bf078-137">接著會重新計算工作的排程識別碼，使其識別碼以其新上層的排程識別碼為基準，並遵循大綱編號配置。</span><span class="sxs-lookup"><span data-stu-id="bf078-137">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="bf078-138">上層工作現在是摘要工作。</span><span class="sxs-lookup"><span data-stu-id="bf078-138">The parent task is now a summary task.</span></span> <span data-ttu-id="bf078-139">因此會變成其下層工作的彙總。</span><span class="sxs-lookup"><span data-stu-id="bf078-139">Therefore, it becomes a rollup of its child tasks.</span></span> <span data-ttu-id="bf078-140">將工作升階時，此工作就不再是其原先上層工作的下層。</span><span class="sxs-lookup"><span data-stu-id="bf078-140">When a task is promoted, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="bf078-141">接著會重新計算排程識別碼，使其反映該工作在階層中的已更新深度和位置。</span><span class="sxs-lookup"><span data-stu-id="bf078-141">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="bf078-142">也會重新計算先前上層工作的投入量、成本和日期，這樣就不會包含在此工作中。</span><span class="sxs-lookup"><span data-stu-id="bf078-142">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

<span data-ttu-id="bf078-143">完成下列步驟將工作縮排或升階。</span><span class="sxs-lookup"><span data-stu-id="bf078-143">Complete the following steps to indent or promote a task.</span></span>

1. <span data-ttu-id="bf078-144">在 **專案** 頁面 **工作** 提交的 **摘要工作** 底下，選取工作名稱旁的三個垂直圓點，然後選取 **建立子工作**。</span><span class="sxs-lookup"><span data-stu-id="bf078-144">On the **Project** page, on the **Tasks** tab, under **Summary tasks**, select the three vertical dots by the task name, and then select **Make subtask**.</span></span> 
2. <span data-ttu-id="bf078-145">選取要縮排或升階的工作。</span><span class="sxs-lookup"><span data-stu-id="bf078-145">Select the task to indent or promote.</span></span> <span data-ttu-id="bf078-146">若要選取多個工作，請選取一個工作並按住 Ctrl，然後再選取另一個工作。</span><span class="sxs-lookup"><span data-stu-id="bf078-146">To select more than one task, select a task, press and hold Ctrl, and then select additional tasks.</span></span>
2. <span data-ttu-id="bf078-147">選取 **縮排** 或 **升階子工作**，可將工作移到摘要工作底下或從其下移出。</span><span class="sxs-lookup"><span data-stu-id="bf078-147">Select **Indent** or **Promote subtask**  to move tasks under or out from under summary tasks.</span></span>

### <a name="move-tasks-up-and-down"></a><span data-ttu-id="bf078-148">將工作上移和下移</span><span class="sxs-lookup"><span data-stu-id="bf078-148">Move tasks up and down</span></span>

<span data-ttu-id="bf078-149">工作可以透過下列兩種方式之一移到分工結構圖中的任何層級：</span><span class="sxs-lookup"><span data-stu-id="bf078-149">Tasks can me moved to any level in the work breakdown structure in one of two ways:</span></span>

- <span data-ttu-id="bf078-150">選取一個或多個工作，並將這些工作拖曳至所需的位置。</span><span class="sxs-lookup"><span data-stu-id="bf078-150">Select one more tasks and drag them to the desired location.</span></span>
- <span data-ttu-id="bf078-151">選取一個或多個工作、按滑鼠右鍵並選取 **剪下**、選取排程中的目的地儲存格，然後按滑鼠右鍵並選取 **貼上**。</span><span class="sxs-lookup"><span data-stu-id="bf078-151">Select one or more tasks, right-click and select **Cut**, select the destination cell in the schedule, and then right-click and select **Paste**.</span></span>

## <a name="task-attributes"></a><span data-ttu-id="bf078-152">工作屬性</span><span class="sxs-lookup"><span data-stu-id="bf078-152">Task attributes</span></span>

<span data-ttu-id="bf078-153">工作的名稱描述必須完成的作業。</span><span class="sxs-lookup"><span data-stu-id="bf078-153">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="bf078-154">在 Project Operations 中，與工作相關聯的屬性會描述工作的排程及其人員配置需求。</span><span class="sxs-lookup"><span data-stu-id="bf078-154">In Project Operations, the attributes associated with a task describe the schedule of the task and its staffing requirements.</span></span>

## <a name="schedule-attributes"></a><span data-ttu-id="bf078-155">排程屬性</span><span class="sxs-lookup"><span data-stu-id="bf078-155">Schedule attributes</span></span>

<span data-ttu-id="bf078-156">**投入量**、**開始日期**、**結束日期** 和 **期間** 屬性會定義工作的排程。</span><span class="sxs-lookup"><span data-stu-id="bf078-156">The **Effort**, **Start date**, **End date**, and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="bf078-157">下表顯示其他排程屬性。</span><span class="sxs-lookup"><span data-stu-id="bf078-157">The following table shows additional schedule attributes.</span></span>

| <span data-ttu-id="bf078-158">**最終顯示名稱**</span><span class="sxs-lookup"><span data-stu-id="bf078-158">**Final display name**</span></span> | <span data-ttu-id="bf078-159">**最終描述**</span><span class="sxs-lookup"><span data-stu-id="bf078-159">**Final description**</span></span> |
| --- | --- |
| <span data-ttu-id="bf078-160">完成的投入 (小時)</span><span class="sxs-lookup"><span data-stu-id="bf078-160">Effort Completed (Hours)</span></span> | <span data-ttu-id="bf078-161">工作的已完成工時 (小時)。</span><span class="sxs-lookup"><span data-stu-id="bf078-161">Completed work for the task in hours.</span></span> |
| <span data-ttu-id="bf078-162">持續時間</span><span class="sxs-lookup"><span data-stu-id="bf078-162">Duration</span></span> | <span data-ttu-id="bf078-163">顯示工作的期間 (以天計)。</span><span class="sxs-lookup"><span data-stu-id="bf078-163">Displays the duration in days for the task.</span></span> |
| <span data-ttu-id="bf078-164">總投入</span><span class="sxs-lookup"><span data-stu-id="bf078-164">Total Effort</span></span> | <span data-ttu-id="bf078-165">工作的總工時 (小時)。</span><span class="sxs-lookup"><span data-stu-id="bf078-165">Total work for the task in hours.</span></span> |
| <span data-ttu-id="bf078-166">結束</span><span class="sxs-lookup"><span data-stu-id="bf078-166">Finish</span></span> | <span data-ttu-id="bf078-167">完成日期與時間。</span><span class="sxs-lookup"><span data-stu-id="bf078-167">Finish date and time.</span></span> |
| <span data-ttu-id="bf078-168">完成百分比</span><span class="sxs-lookup"><span data-stu-id="bf078-168">% Complete</span></span> | <span data-ttu-id="bf078-169">工作的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="bf078-169">The percentage of the task that is complete.</span></span> |
| <span data-ttu-id="bf078-170">專案貯體</span><span class="sxs-lookup"><span data-stu-id="bf078-170">Project Bucket</span></span> | <span data-ttu-id="bf078-171">工作面板可依貯體分組，因此每個貯體都有自己的欄。</span><span class="sxs-lookup"><span data-stu-id="bf078-171">The task board can be grouped by bucket so each bucket has its own column.</span></span> |
| <span data-ttu-id="bf078-172">剩餘未完成投入 (小時)</span><span class="sxs-lookup"><span data-stu-id="bf078-172">Effort Remaining (Hours)</span></span> | <span data-ttu-id="bf078-173">工作的剩餘工時 (小時)。</span><span class="sxs-lookup"><span data-stu-id="bf078-173">The remaining work for the task in hours.</span></span> |
| <span data-ttu-id="bf078-174">開始時間</span><span class="sxs-lookup"><span data-stu-id="bf078-174">Start</span></span> | <span data-ttu-id="bf078-175">開始日期與時間。</span><span class="sxs-lookup"><span data-stu-id="bf078-175">Start date and time.</span></span> |
| <span data-ttu-id="bf078-176">名字</span><span class="sxs-lookup"><span data-stu-id="bf078-176">Name</span></span> | <span data-ttu-id="bf078-177">工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf078-177">The name of the task.</span></span> |
| <span data-ttu-id="bf078-178">識別碼</span><span class="sxs-lookup"><span data-stu-id="bf078-178">ID</span></span> | <span data-ttu-id="bf078-179">分工結構圖中工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf078-179">The ID of the task in the work breakdown structure.</span></span> |

<span data-ttu-id="bf078-180">身為管理員，您可以在工作實體上定義自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="bf078-180">As an administrator, you can define custom fields on the task entity.</span></span> <span data-ttu-id="bf078-181">不過，這些欄位無法顯示在排程網格上。</span><span class="sxs-lookup"><span data-stu-id="bf078-181">However the fields can't be displayed on the schedule grid.</span></span> <span data-ttu-id="bf078-182">若要查看您的自訂欄位，請將其新增至 **專案工作** 詳細資料頁面。</span><span class="sxs-lookup"><span data-stu-id="bf078-182">To see your custom fields, add them to the **Project Task** details page.</span></span>

## <a name="staffing-attributes"></a><span data-ttu-id="bf078-183">人員配置屬性</span><span class="sxs-lookup"><span data-stu-id="bf078-183">Staffing attributes</span></span>

<span data-ttu-id="bf078-184">人員配置屬性可以透過排程中的 **資源** 欄位來存取。</span><span class="sxs-lookup"><span data-stu-id="bf078-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="bf078-185">您可以搜尋現有的資源，或者選取 **快速建立** 窗格中的 **建立**，將專案團隊成員新增為新資源。</span><span class="sxs-lookup"><span data-stu-id="bf078-185">You can either search for an existing resource, or select **Create**, and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="bf078-186">**角色**、**資源分配單位** 和 **職位名稱** 欄位可用來描述工作的人員配置需求。</span><span class="sxs-lookup"><span data-stu-id="bf078-186">The **Role**, **Resourcing Unit**, and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="bf078-187">這些人員配置屬性會與工作排程一起用來尋找可執行此工作的適當資源。</span><span class="sxs-lookup"><span data-stu-id="bf078-187">These staffing attributes, together with the task schedule are used to find available resources to do this task.</span></span>

   - <span data-ttu-id="bf078-188">**角色**：指定執行工作所需的資源類型。</span><span class="sxs-lookup"><span data-stu-id="bf078-188">**Role**: Specify the type of resource that is required to do the task.</span></span>
   - <span data-ttu-id="bf078-189">**資源分配單位**：指定應指派資源給工作的來源單位。</span><span class="sxs-lookup"><span data-stu-id="bf078-189">**Resourcing unit**: Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="bf078-190">如果資源的成本和帳單費率是根據資源分配單位所設定，此屬性就會影響工作的成本和銷售估計。</span><span class="sxs-lookup"><span data-stu-id="bf078-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>
   - <span data-ttu-id="bf078-191">**職位名稱**：可輸入一般資源的易記名稱，做為最終執行工作之資源的預留位置。</span><span class="sxs-lookup"><span data-stu-id="bf078-191">**Position name**: Enter a name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="bf078-192">**資源** 欄位會在找到一般資源或具名資源時保存其職位名稱。</span><span class="sxs-lookup"><span data-stu-id="bf078-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="bf078-193">**類別** 欄位會保存表示工作可分組歸入的更廣泛作業類型的值。</span><span class="sxs-lookup"><span data-stu-id="bf078-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="bf078-194">此欄位不會影響排程或人員配置。</span><span class="sxs-lookup"><span data-stu-id="bf078-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="bf078-195">反而只會將此欄位用於報表。</span><span class="sxs-lookup"><span data-stu-id="bf078-195">Instead, the field is used only for reporting.</span></span>

## <a name="task-dependencies"></a><span data-ttu-id="bf078-196">工作相依性</span><span class="sxs-lookup"><span data-stu-id="bf078-196">Task dependencies</span></span>

<span data-ttu-id="bf078-197">您可以使用 Project Operations 中的排程，建立工作之間的前置任務關聯。</span><span class="sxs-lookup"><span data-stu-id="bf078-197">You can use the schedule in Project Operations to create predecessor relationships between tasks.</span></span> <span data-ttu-id="bf078-198">**前置任務** 欄位使用一個或多個值來表示工作所依存的工作。</span><span class="sxs-lookup"><span data-stu-id="bf078-198">The **Predecessor** field uses one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="bf078-199">將前置任務值指派給工作時，該工作只能在所有的前置任務工作都已完成後開始。</span><span class="sxs-lookup"><span data-stu-id="bf078-199">When predecessor values are assigned to a task, the task can start only after all of the predecessor tasks have been completed.</span></span> <span data-ttu-id="bf078-200">由於此相依性，工作的規劃開始日期會重設為完成前置任務工作的日期。</span><span class="sxs-lookup"><span data-stu-id="bf078-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="bf078-201">工作模式對於前置任務/相依工作的開始和結束日期已進行的更新沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="bf078-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="bf078-202">協助工具和鍵盤快速鍵</span><span class="sxs-lookup"><span data-stu-id="bf078-202">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="bf078-203">**排程** 網格完全可供存取，並且可與朗讀程式、JAWS 或 NVDA 等螢幕助讀程式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="bf078-203">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="bf078-204">您可以使用方向鍵在網格區域中穿行 (如同在 Microsoft Excel 中)、可以使用 Tab 鍵前進通過互動式使用者介面元素，並且可以使用向下鍵、Enter 鍵或空格鍵來選取和開啟下拉式功能表。</span><span class="sxs-lookup"><span data-stu-id="bf078-204">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive user interface elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and open the drop-down menus.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]