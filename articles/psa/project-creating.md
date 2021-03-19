---
title: 專案排程
description: 本主題提供有關如何建立排程的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8f1a0b0ed610ade094546782a1fa517682a390e4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283972"
---
# <a name="project-schedules"></a><span data-ttu-id="43b90-103">專案排程</span><span class="sxs-lookup"><span data-stu-id="43b90-103">Project schedules</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="43b90-104">專案排程會溝通哪些工作必須完成，哪些資源將執行這些工作，以及必須完成工作的時間。</span><span class="sxs-lookup"><span data-stu-id="43b90-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe that the work must be finished in.</span></span> <span data-ttu-id="43b90-105">它會反映所有與按時交付專案相關的工作。</span><span class="sxs-lookup"><span data-stu-id="43b90-105">It reflects all the work that is associated with delivering the project on time.</span></span> <span data-ttu-id="43b90-106">在 Dynamics 365 Project Service Automation 中，您可以建立專案排程，作法是將作業細分為易於管理的工作、估計完成每項工作所需的時間、設定工作相依性、設定工作期間，以及估計執行這些工作的一般資源。</span><span class="sxs-lookup"><span data-stu-id="43b90-106">In Dynamics 365 Project Service Automation, you create a project schedule by breaking the work down into manageable tasks, estimating the time that is required to do each task, setting task dependencies, setting task durations, and estimating the generic resources that will do the tasks.</span></span> <span data-ttu-id="43b90-107">專案排程是透過專案頁面的 **排程** 索引標籤來建立。</span><span class="sxs-lookup"><span data-stu-id="43b90-107">The project schedule is created on the **Schedule** tab of the project page.</span></span>
 
## <a name="tasks"></a><span data-ttu-id="43b90-108">工作</span><span class="sxs-lookup"><span data-stu-id="43b90-108">Tasks</span></span>

<span data-ttu-id="43b90-109">建立專案排程的第一個步驟是將作業細分為易於管理的部分。</span><span class="sxs-lookup"><span data-stu-id="43b90-109">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="43b90-110">PSA 中的排程支援下列功能：</span><span class="sxs-lookup"><span data-stu-id="43b90-110">The schedule in PSA supports the following features:</span></span>

- <span data-ttu-id="43b90-111">專案根節點</span><span class="sxs-lookup"><span data-stu-id="43b90-111">Project root node</span></span>
- <span data-ttu-id="43b90-112">摘要或容器工作</span><span class="sxs-lookup"><span data-stu-id="43b90-112">Summary or container tasks</span></span>
- <span data-ttu-id="43b90-113">分葉節點工作</span><span class="sxs-lookup"><span data-stu-id="43b90-113">Leaf node tasks</span></span>

### <a name="project-root-node"></a><span data-ttu-id="43b90-114">專案根節點</span><span class="sxs-lookup"><span data-stu-id="43b90-114">Project root node</span></span>

<span data-ttu-id="43b90-115">專案根節點是專案的最上層摘要工作。</span><span class="sxs-lookup"><span data-stu-id="43b90-115">The project root node is the top-level summary task for the project.</span></span> <span data-ttu-id="43b90-116">所有其他專案工作都會在它底下建立。</span><span class="sxs-lookup"><span data-stu-id="43b90-116">All other project tasks are created under it.</span></span> <span data-ttu-id="43b90-117">根節點的名稱一律設定為專案名稱。</span><span class="sxs-lookup"><span data-stu-id="43b90-117">The name of the root node is always set to the project name.</span></span> <span data-ttu-id="43b90-118">根節點的投入量、日期和期間是根據其底下階層的值摘要列出。</span><span class="sxs-lookup"><span data-stu-id="43b90-118">The effort, dates, and duration of the root node are summarized based on the values in the hierarchy below it.</span></span> <span data-ttu-id="43b90-119">您無法編輯根節點的屬性。</span><span class="sxs-lookup"><span data-stu-id="43b90-119">You can't edit the properties of the root node.</span></span> <span data-ttu-id="43b90-120">您也無法刪除根節點。</span><span class="sxs-lookup"><span data-stu-id="43b90-120">You also can't delete the root node.</span></span>

### <a name="summary-or-container-tasks"></a><span data-ttu-id="43b90-121">摘要或容器工作</span><span class="sxs-lookup"><span data-stu-id="43b90-121">Summary or container tasks</span></span> 

<span data-ttu-id="43b90-122">摘要工作在其底下有子工作或容器工作。</span><span class="sxs-lookup"><span data-stu-id="43b90-122">Summary tasks have sub-tasks or container tasks under them.</span></span> <span data-ttu-id="43b90-123">這些工作沒有其本身的作業投入量或成本。</span><span class="sxs-lookup"><span data-stu-id="43b90-123">They have no work effort or cost of their own.</span></span> <span data-ttu-id="43b90-124">相反的，其作業投入量和成本是其容器工作之作業投入量與成本的彙總。</span><span class="sxs-lookup"><span data-stu-id="43b90-124">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="43b90-125">摘要工作的開始日期是容器工作的開始日期，而結束日期是容器工作的結束日期。</span><span class="sxs-lookup"><span data-stu-id="43b90-125">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="43b90-126">您可以編輯摘要工作的名稱，但是無法編輯排程屬性 (投入量、日期和期間)。</span><span class="sxs-lookup"><span data-stu-id="43b90-126">The name of a summary task can be edited, but scheduling properties (effort, dates, and duration) can't be edited.</span></span> <span data-ttu-id="43b90-127">若刪除摘要工作，也會刪除其所有的容器工作。</span><span class="sxs-lookup"><span data-stu-id="43b90-127">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="43b90-128">分葉節點工作</span><span class="sxs-lookup"><span data-stu-id="43b90-128">Leaf node tasks</span></span>

<span data-ttu-id="43b90-129">分葉節點工作表示專案中最細微的作業。</span><span class="sxs-lookup"><span data-stu-id="43b90-129">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="43b90-130">這些工作有估計投入量、資源、規劃開始和結束日期，以及期間。</span><span class="sxs-lookup"><span data-stu-id="43b90-130">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>
 
## <a name="creating-a-task-hierarchy"></a><span data-ttu-id="43b90-131">建立工作階層</span><span class="sxs-lookup"><span data-stu-id="43b90-131">Creating a task hierarchy</span></span>

<span data-ttu-id="43b90-132">您可以使用下列選項建立工作階層：</span><span class="sxs-lookup"><span data-stu-id="43b90-132">You can create a task hierarchy by using the following options:</span></span>

- <span data-ttu-id="43b90-133">**新增工作** 按鈕</span><span class="sxs-lookup"><span data-stu-id="43b90-133">**Add task** button</span></span>
- <span data-ttu-id="43b90-134">**縮排工作** 按鈕</span><span class="sxs-lookup"><span data-stu-id="43b90-134">**Indent task** button</span></span>
- <span data-ttu-id="43b90-135">**凸排工作** 按鈕</span><span class="sxs-lookup"><span data-stu-id="43b90-135">**Outdent task** button</span></span>
- <span data-ttu-id="43b90-136">**上移** 和 **下移** 按鈕</span><span class="sxs-lookup"><span data-stu-id="43b90-136">**Move up** and **Move down** buttons</span></span>
- <span data-ttu-id="43b90-137">協助工具和鍵盤快速鍵</span><span class="sxs-lookup"><span data-stu-id="43b90-137">Accessibility and keyboard shortcuts</span></span>

### <a name="add-task"></a><span data-ttu-id="43b90-138">新增工作</span><span class="sxs-lookup"><span data-stu-id="43b90-138">Add task</span></span>

<span data-ttu-id="43b90-139">**新增工作** 按鈕可讓您在階層中建立新工作。</span><span class="sxs-lookup"><span data-stu-id="43b90-139">The **Add task** button lets you create a new task in the hierarchy.</span></span> <span data-ttu-id="43b90-140">如果未選取位置，此工作會在結尾插入。</span><span class="sxs-lookup"><span data-stu-id="43b90-140">If you don't select a position, the task is inserted at the end.</span></span> 

<span data-ttu-id="43b90-141">排程識別碼會指派給每一項工作。</span><span class="sxs-lookup"><span data-stu-id="43b90-141">A schedule ID is assigned to every task.</span></span> <span data-ttu-id="43b90-142">排程識別碼表示工作在階層中的深度和位置。</span><span class="sxs-lookup"><span data-stu-id="43b90-142">The schedule ID represents the task's depth and position in the hierarchy.</span></span> <span data-ttu-id="43b90-143">它使用大綱編號系統。</span><span class="sxs-lookup"><span data-stu-id="43b90-143">It uses outline numbering.</span></span> <span data-ttu-id="43b90-144">專案根節點底下第一層工作會使用 1、2、3 (依此類推) 的編號配置。</span><span class="sxs-lookup"><span data-stu-id="43b90-144">For tasks in the first level under the project root node, a numbering scheme of 1, 2, 3, and so on, is used.</span></span> <span data-ttu-id="43b90-145">第一層底下的工作使用 1.1、1.2、1.3 (依此類推) 的編號配置。</span><span class="sxs-lookup"><span data-stu-id="43b90-145">For tasks under the first level, a numbering scheme of 1.1, 1.2, 1.3, and so on, is used.</span></span>

### <a name="indent-task"></a><span data-ttu-id="43b90-146">縮排工作</span><span class="sxs-lookup"><span data-stu-id="43b90-146">Indent task</span></span>

<span data-ttu-id="43b90-147">工作縮排時，此工作會變成其上方緊鄰工作的下層。</span><span class="sxs-lookup"><span data-stu-id="43b90-147">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="43b90-148">接著會重新計算工作的排程識別碼，使其識別碼以其新上層的排程識別碼為基準，並遵循大綱編號配置。</span><span class="sxs-lookup"><span data-stu-id="43b90-148">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="43b90-149">上層工作現在是摘要工作或容器工作。</span><span class="sxs-lookup"><span data-stu-id="43b90-149">The parent task is now a summary task or a container task.</span></span> <span data-ttu-id="43b90-150">因此會變成其下層工作的彙總。</span><span class="sxs-lookup"><span data-stu-id="43b90-150">Therefore, it becomes a rollup of its child tasks.</span></span>

### <a name="outdent-task"></a><span data-ttu-id="43b90-151">凸排工作</span><span class="sxs-lookup"><span data-stu-id="43b90-151">Outdent task</span></span> 

<span data-ttu-id="43b90-152">工作凸排時，此工作就不再是其原先上層工作的下層。</span><span class="sxs-lookup"><span data-stu-id="43b90-152">When a task is outdented, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="43b90-153">接著會重新計算排程識別碼，使其反映該工作在階層中的已更新深度和位置。</span><span class="sxs-lookup"><span data-stu-id="43b90-153">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="43b90-154">也會重新計算先前上層工作的投入量、成本和日期，這樣就不會包含在此工作中。</span><span class="sxs-lookup"><span data-stu-id="43b90-154">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

### <a name="move-up-and-move-down"></a><span data-ttu-id="43b90-155">上移和下移</span><span class="sxs-lookup"><span data-stu-id="43b90-155">Move up and Move down</span></span> 

<span data-ttu-id="43b90-156">**上移** 和 **下移** 按鈕會變更工作在其上層階層中的位置。</span><span class="sxs-lookup"><span data-stu-id="43b90-156">The **Move up** and **Move down** buttons change the position of a task within its parent hierarchy.</span></span> <span data-ttu-id="43b90-157">此類型的變更不會影響工作的投入量、成本、日期或期間。</span><span class="sxs-lookup"><span data-stu-id="43b90-157">Changes of this type don't affect the task's effort, cost, dates, or duration.</span></span> <span data-ttu-id="43b90-158">只有工作的排程識別碼受到影響。</span><span class="sxs-lookup"><span data-stu-id="43b90-158">Only the task's schedule ID is affected.</span></span> <span data-ttu-id="43b90-159">將會重新計算排程識別碼，使其反映該工作在上層之下層工作清單中的新位置。</span><span class="sxs-lookup"><span data-stu-id="43b90-159">The schedule ID is recalculated so that it reflects the task's new position in the parent's list of child tasks.</span></span>

### <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="43b90-160">協助工具和鍵盤快速鍵</span><span class="sxs-lookup"><span data-stu-id="43b90-160">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="43b90-161">**排程** 網格完全可供存取，並且可與朗讀程式、JAWS 或 NVDA 等螢幕助讀程式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="43b90-161">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="43b90-162">您可以使用方向鍵在網格區域中穿行 (如同在 Microsoft Excel 中)、可以使用 Tab 鍵前進通過各個互動式 UI 元素，並且可以使用向下鍵、Enter 鍵或空格鍵來選取和叫用下拉式功能表。</span><span class="sxs-lookup"><span data-stu-id="43b90-162">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive UI elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and invoke the drop-down menus.</span></span> <span data-ttu-id="43b90-163">欄標題也是互動式的。</span><span class="sxs-lookup"><span data-stu-id="43b90-163">The column headers are also interactive.</span></span> <span data-ttu-id="43b90-164">您可以隱藏和顯示各欄、使用 Tab 鍵和方向鍵移動通過各個欄標題，以及使用工具列上的動作按鈕。</span><span class="sxs-lookup"><span data-stu-id="43b90-164">You can hide and show columns, use the Tab key and arrow keys to move through the column headers, and use the action buttons on the toolbar.</span></span> <span data-ttu-id="43b90-165">此外，可以使用下列鍵盤快速鍵：</span><span class="sxs-lookup"><span data-stu-id="43b90-165">In addition, you can use the following keyboard shortcuts:</span></span>

- <span data-ttu-id="43b90-166">**重新整理**：ALT+SHIFT+F5</span><span class="sxs-lookup"><span data-stu-id="43b90-166">**Refresh**: ALT+SHIFT+F5</span></span>
- <span data-ttu-id="43b90-167">**新增**：ALT+SHIFT+Insert</span><span class="sxs-lookup"><span data-stu-id="43b90-167">**Add**: ALT+SHIFT+Insert</span></span>
- <span data-ttu-id="43b90-168">**刪除**：ALT+SHIFT+Delete</span><span class="sxs-lookup"><span data-stu-id="43b90-168">**Delete**: ALT+SHIFT+Delete</span></span>
- <span data-ttu-id="43b90-169">**上移/下移**：ALT+SHIFT+向上鍵/向下鍵</span><span class="sxs-lookup"><span data-stu-id="43b90-169">**Move up/down**: ALT+SHIFT+Up/Down arrows</span></span>
- <span data-ttu-id="43b90-170">**縮排/凸排**：ALT_SHIFT+向左鍵/向右鍵</span><span class="sxs-lookup"><span data-stu-id="43b90-170">**Indent/Outdent**: ALT_SHIFT+Left/Right arrows</span></span>
- <span data-ttu-id="43b90-171">**展開/摺疊階段**：ALT+SHIFT+加號/減號鍵</span><span class="sxs-lookup"><span data-stu-id="43b90-171">**Expand/Collapse Hierarchies**: ALT+SHIFT+Plus/Minus keys</span></span>

## <a name="task-attributes"></a><span data-ttu-id="43b90-172">工作屬性</span><span class="sxs-lookup"><span data-stu-id="43b90-172">Task attributes</span></span>

<span data-ttu-id="43b90-173">工作的名稱描述必須完成的作業。</span><span class="sxs-lookup"><span data-stu-id="43b90-173">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="43b90-174">在 PSA 中，與工作相關聯的屬性會描述工作的排程及其人員配置需求。</span><span class="sxs-lookup"><span data-stu-id="43b90-174">In PSA, the attributes that are associated with a task describe the schedule of the task and its staffing requirements.</span></span>

> ![工作屬性](media/project-2.png)
 
### <a name="schedule-attributes"></a><span data-ttu-id="43b90-176">排程屬性</span><span class="sxs-lookup"><span data-stu-id="43b90-176">Schedule attributes</span></span>

<span data-ttu-id="43b90-177">**投入量**、**開始日期**、**結束日期** 和 **期間** 屬性會定義工作的排程。</span><span class="sxs-lookup"><span data-stu-id="43b90-177">The **Effort**, **Start date**, **End date**, and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="43b90-178">其他排程屬性包括：</span><span class="sxs-lookup"><span data-stu-id="43b90-178">Additional schedule attributes include:</span></span>

- <span data-ttu-id="43b90-179">**投入時數**：輸入完成工作所需的時數估計。</span><span class="sxs-lookup"><span data-stu-id="43b90-179">**Effort hours**: Enter an estimate of the hours that are required to complete the task.</span></span> 
- <span data-ttu-id="43b90-180">**期間**：指定完成工作所需的工作日數。</span><span class="sxs-lookup"><span data-stu-id="43b90-180">**Duration**: Specify the number of workdays that are required to complete the task.</span></span>
- <span data-ttu-id="43b90-181">**排程識別碼**：這個自動產生的識別碼是用來排序階層中的工作。</span><span class="sxs-lookup"><span data-stu-id="43b90-181">**Schedule ID**: This automatically generated ID is used to order tasks in the hierarchy.</span></span> <span data-ttu-id="43b90-182">工作之間的相依性可管理處理工作所依照的實際順序。</span><span class="sxs-lookup"><span data-stu-id="43b90-182">Dependencies between the tasks manage the actual order in which the tasks are worked on.</span></span>
 
### <a name="staffing-attributes"></a><span data-ttu-id="43b90-183">人員配置屬性</span><span class="sxs-lookup"><span data-stu-id="43b90-183">Staffing attributes</span></span>

<span data-ttu-id="43b90-184">人員配置屬性可以透過排程中的 **資源** 欄位來存取。</span><span class="sxs-lookup"><span data-stu-id="43b90-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="43b90-185">您可以搜尋現有的資源，或者按一下 **快速建立** 窗格中的 **建立**，將專案團隊成員新增為新資源。</span><span class="sxs-lookup"><span data-stu-id="43b90-185">You can either search for an existing resource, or click **Create** and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="43b90-186">**角色**、**資源分配單位** 和 **職位名稱** 欄位可用來描述工作的人員配置需求。</span><span class="sxs-lookup"><span data-stu-id="43b90-186">The **Role**, **Resourcing Unit**, and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="43b90-187">這些人員配置屬性與工作排程一起用來尋找可執行此工作的適當資源。</span><span class="sxs-lookup"><span data-stu-id="43b90-187">These staffing attributes together with the task schedule are used to find available resources to do this task.</span></span>

<span data-ttu-id="43b90-188">**角色** - 指定執行工作所需的資源類型。</span><span class="sxs-lookup"><span data-stu-id="43b90-188">**Role** - Specify the type of resource that is required to do the task.</span></span>

<span data-ttu-id="43b90-189">**資源分配單位** - 指定應指派資源給工作的來源單位。</span><span class="sxs-lookup"><span data-stu-id="43b90-189">**Resourcing unit** - Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="43b90-190">如果資源的成本和帳單費率是根據資源分配單位所設定，此屬性就會影響工作的成本和銷售估計。</span><span class="sxs-lookup"><span data-stu-id="43b90-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>

<span data-ttu-id="43b90-191">**職位名稱** – 可輸入一般資源的易記名稱，做為最終執行工作之資源的預留位置。</span><span class="sxs-lookup"><span data-stu-id="43b90-191">**Position name** – Enter a friendly name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="43b90-192">**資源** 欄位會在找到一般資源或具名資源時保存其職位名稱。</span><span class="sxs-lookup"><span data-stu-id="43b90-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="43b90-193">**類別** 欄位會保存表示工作可分組歸入的更廣泛作業類型的值。</span><span class="sxs-lookup"><span data-stu-id="43b90-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="43b90-194">此欄位不會影響排程或人員配置。</span><span class="sxs-lookup"><span data-stu-id="43b90-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="43b90-195">只是用於報表。</span><span class="sxs-lookup"><span data-stu-id="43b90-195">It's used only for reporting.</span></span>

### <a name="task-dependencies"></a><span data-ttu-id="43b90-196">工作相依性</span><span class="sxs-lookup"><span data-stu-id="43b90-196">Task dependencies</span></span> 

<span data-ttu-id="43b90-197">您可以使用 PSA 中的排程，建立工作之間的前置任務關聯。</span><span class="sxs-lookup"><span data-stu-id="43b90-197">You can use the schedule in PSA to create predecessor relationships between tasks.</span></span> <span data-ttu-id="43b90-198">**工作** 底下的 **前置任務** 欄位接受一個或多個值來表示工作所依存的工作。</span><span class="sxs-lookup"><span data-stu-id="43b90-198">The **Predecessor** field under **Tasks** takes one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="43b90-199">將前置任務值指派至工作時，該工作只能在所有的前置任務工作都已完成後開始。</span><span class="sxs-lookup"><span data-stu-id="43b90-199">When predecessor values are assigned to a task, the task can start only after all the predecessor tasks have been completed.</span></span> <span data-ttu-id="43b90-200">由於此相依性，工作的規劃開始日期會重設為完成前置任務工作的日期。</span><span class="sxs-lookup"><span data-stu-id="43b90-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="43b90-201">工作模式對於前置任務/相依工作的開始和結束日期已進行的更新沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="43b90-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="task-mode"></a><span data-ttu-id="43b90-202">工作模式</span><span class="sxs-lookup"><span data-stu-id="43b90-202">Task mode</span></span> 

<span data-ttu-id="43b90-203">工作模式決定分葉節點工作的排程。</span><span class="sxs-lookup"><span data-stu-id="43b90-203">The task mode determines the scheduling of leaf node tasks.</span></span> <span data-ttu-id="43b90-204">PSA 為每個工作支援兩種工作模式：自動排程和手動排程。</span><span class="sxs-lookup"><span data-stu-id="43b90-204">PSA supports two task modes for every task: automatic scheduling and manual scheduling.</span></span>

### <a name="auto-scheduling"></a><span data-ttu-id="43b90-205">自動排程</span><span class="sxs-lookup"><span data-stu-id="43b90-205">Auto-scheduling</span></span> 
 
<span data-ttu-id="43b90-206">將工作的工作模式設定為 **自動排程** 時，工作排程引擎會對下列工作屬性使用工作排程規則以決定工作的排程。</span><span class="sxs-lookup"><span data-stu-id="43b90-206">When task mode is set to **Automatically Scheduled** for a task, the task scheduling engine uses the scheduling rules on task attributes to determine the schedule for the task.</span></span>

#### <a name="scheduling-rules"></a><span data-ttu-id="43b90-207">排程規則</span><span class="sxs-lookup"><span data-stu-id="43b90-207">Scheduling rules</span></span>

<span data-ttu-id="43b90-208">根據預設，如果分葉節點工作沒有前置任務，其開始日期會設定為專案的排定開始日期。</span><span class="sxs-lookup"><span data-stu-id="43b90-208">By default, if a leaf node task doesn't have predecessors, its start date is set to the project's scheduled start date.</span></span> <span data-ttu-id="43b90-209">分葉節點工作的期間一律計算為開始和結束日期之間的工作天數。</span><span class="sxs-lookup"><span data-stu-id="43b90-209">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="43b90-210">自動排程工作時，排程引擎會遵循下列規則：</span><span class="sxs-lookup"><span data-stu-id="43b90-210">When a task is automatically scheduled, the scheduling engine follows these rules:</span></span>

- <span data-ttu-id="43b90-211">工作的開始與結束日期根據專案的排程行事曆，必須是工作日。</span><span class="sxs-lookup"><span data-stu-id="43b90-211">The start and end dates of the task must be working days, according to the project's scheduling calendar.</span></span> 
- <span data-ttu-id="43b90-212">任何有前置任務工作的工作，其開始日期自動設定為其前置任務的最後結束日期</span><span class="sxs-lookup"><span data-stu-id="43b90-212">For any task that has predecessor tasks, the start date is automatically set to the latest end date of its predecessors.</span></span>
- <span data-ttu-id="43b90-213">投入量使用此公式計算：人數 × 期間 × 專案行事曆的標準工作日中的時數。</span><span class="sxs-lookup"><span data-stu-id="43b90-213">Effort is calculated by using this formula: Number of people × Duration × Hours in a standard workday in the project calendar.</span></span>

### <a name="manual-scheduling"></a><span data-ttu-id="43b90-214">手動排程</span><span class="sxs-lookup"><span data-stu-id="43b90-214">Manual scheduling</span></span>

<span data-ttu-id="43b90-215">如果自動排程的規則不符合您的需求，您可以將工作的工作模式設定為 **手動排程**。</span><span class="sxs-lookup"><span data-stu-id="43b90-215">If the rules of automatic scheduling don't meet your requirements, you can set the task mode for the task to **Manually Scheduled**.</span></span> <span data-ttu-id="43b90-216">此設定會停止排程引擎計算其他排程屬性的值。</span><span class="sxs-lookup"><span data-stu-id="43b90-216">This setting stops the scheduling engine from calculating the values of other scheduling attributes.</span></span> <span data-ttu-id="43b90-217">不論工作模式如何，如果將前置任務設定在工作上，永遠都會影響相依工作的開始日期。</span><span class="sxs-lookup"><span data-stu-id="43b90-217">Regardless of the task mode, if you set predecessors on tasks, you always affect the dependent task's start date.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]