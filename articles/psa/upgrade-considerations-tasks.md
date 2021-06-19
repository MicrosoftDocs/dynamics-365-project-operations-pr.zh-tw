---
title: 分工結構圖升級考量
description: 本主題提供有關將 Project Service Automation 2.x 的分工結構圖升級至 3.x 的資訊。
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 868b0daadaf6cf96ca7bf847914bca8014412f26
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005601"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="f20db-103">分工結構圖升級考量</span><span class="sxs-lookup"><span data-stu-id="f20db-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f20db-104">本主題提供有關將 Project Service Automation 2.x 的分工結構圖升級至 3.x 的資訊。</span><span class="sxs-lookup"><span data-stu-id="f20db-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="f20db-105">本主題定義 Project Service Automation (PSA) 中專案成功升級所需的健全狀況。</span><span class="sxs-lookup"><span data-stu-id="f20db-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="f20db-106">此外，還提供有關導致升級失敗之常見阻礙情況的資訊。</span><span class="sxs-lookup"><span data-stu-id="f20db-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="f20db-107">如需有關在專案排程中定義專案工作及其功能的詳細資訊，請參閱[專案排程](project-creating.md)。</span><span class="sxs-lookup"><span data-stu-id="f20db-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="f20db-108">主要實體</span><span class="sxs-lookup"><span data-stu-id="f20db-108">Key entities</span></span>
<span data-ttu-id="f20db-109">已載入資源的正確分工結構圖需要下列實體：</span><span class="sxs-lookup"><span data-stu-id="f20db-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="f20db-110">計畫</span><span class="sxs-lookup"><span data-stu-id="f20db-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="f20db-111">專案團隊</span><span class="sxs-lookup"><span data-stu-id="f20db-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="f20db-112">專案工作</span><span class="sxs-lookup"><span data-stu-id="f20db-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="f20db-113">資源指派</span><span class="sxs-lookup"><span data-stu-id="f20db-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="f20db-114">專案工作相依性</span><span class="sxs-lookup"><span data-stu-id="f20db-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="f20db-115">可預約資源</span><span class="sxs-lookup"><span data-stu-id="f20db-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="f20db-116">若要定義資源已載入的分工結構圖，您必須完成下列步驟：</span><span class="sxs-lookup"><span data-stu-id="f20db-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="f20db-117">建立新專案：</span><span class="sxs-lookup"><span data-stu-id="f20db-117">Create a new project.</span></span> <span data-ttu-id="f20db-118">如需有關如何建立新專案的詳細資訊，請參閱 [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)。</span><span class="sxs-lookup"><span data-stu-id="f20db-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="f20db-119">建立一個或多個工作。</span><span class="sxs-lookup"><span data-stu-id="f20db-119">Create one or more tasks.</span></span> <span data-ttu-id="f20db-120">如需有關如何建立工作的詳細資訊，請參閱 [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)。</span><span class="sxs-lookup"><span data-stu-id="f20db-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="f20db-121">定義工作相依性。</span><span class="sxs-lookup"><span data-stu-id="f20db-121">Define the task dependencies.</span></span> <span data-ttu-id="f20db-122">如需詳細資訊，請參閱[專案工作相依性](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)。</span><span class="sxs-lookup"><span data-stu-id="f20db-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="f20db-123">將專案團隊成員指派給專案。</span><span class="sxs-lookup"><span data-stu-id="f20db-123">Assign project team members to the project.</span></span> <span data-ttu-id="f20db-124">如需詳細資訊，請參閱 [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)。</span><span class="sxs-lookup"><span data-stu-id="f20db-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="f20db-125">將專案團隊成員指派給工作。</span><span class="sxs-lookup"><span data-stu-id="f20db-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="f20db-126">如需詳細資訊，請參閱 [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)。</span><span class="sxs-lookup"><span data-stu-id="f20db-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="f20db-127">專案團隊關聯</span><span class="sxs-lookup"><span data-stu-id="f20db-127">Project team relationships</span></span>

<span data-ttu-id="f20db-128">為了確保升級成功，必須正確維護下列關聯：</span><span class="sxs-lookup"><span data-stu-id="f20db-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="f20db-129">所有的專案團隊成員都必須與可預約資源有關聯。</span><span class="sxs-lookup"><span data-stu-id="f20db-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="f20db-130">所有的專案團隊成員都必須與相同的專案有關聯。</span><span class="sxs-lookup"><span data-stu-id="f20db-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="f20db-131">專案工作關聯</span><span class="sxs-lookup"><span data-stu-id="f20db-131">Project task relationships</span></span>
<span data-ttu-id="f20db-132">為了確保升級成功，必須正確維護下列關聯：</span><span class="sxs-lookup"><span data-stu-id="f20db-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="f20db-133">任何相關工作都必須與相同的專案有關聯。</span><span class="sxs-lookup"><span data-stu-id="f20db-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="f20db-134">每項明細工作都必須有上層工作。</span><span class="sxs-lookup"><span data-stu-id="f20db-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="f20db-135">每項工作都必須有上層專案。</span><span class="sxs-lookup"><span data-stu-id="f20db-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="f20db-136">有效條件</span><span class="sxs-lookup"><span data-stu-id="f20db-136">Valid conditions</span></span>

- <span data-ttu-id="f20db-137">所有工作期間都必須大於或等於 (>=) 1 個小時且小於 1,800,000 分鐘 (1,250 天)。\*</span><span class="sxs-lookup"><span data-stu-id="f20db-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="f20db-138">所有工作的開始日期都必須有早於 2000/01/01。\*</span><span class="sxs-lookup"><span data-stu-id="f20db-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="f20db-139">所有工作的開始日期都不得晚於今天起算 17 年之後。\*</span><span class="sxs-lookup"><span data-stu-id="f20db-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="f20db-140">所有工作的開始日期都必須早於或等於其完成日期。</span><span class="sxs-lookup"><span data-stu-id="f20db-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="f20db-141">分類 (費用、材料、稅金和時間)上所有的交易類型都必須有 **預設單位** 及 **單位群組** 的值。</span><span class="sxs-lookup"><span data-stu-id="f20db-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="f20db-142">應避免使用含字母的日期格式。</span><span class="sxs-lookup"><span data-stu-id="f20db-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="f20db-143">可能的風險降低步驟</span><span class="sxs-lookup"><span data-stu-id="f20db-143">Potential mitigation steps</span></span>
- <span data-ttu-id="f20db-144">使用 [進階尋找] 找出沒有包含專案識別碼的專案工作。</span><span class="sxs-lookup"><span data-stu-id="f20db-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="f20db-145">使用 [進階尋找] 找出排程期間大於 > 1,800,000 的專案工作。</span><span class="sxs-lookup"><span data-stu-id="f20db-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="f20db-146">在進行任何資料變更之前，必須先調查任何與實體相關聯的自訂，這個實體可能已致使資料進入錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="f20db-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="f20db-147">您必須先處理這些自訂，才能繼續進行任何資料相關更新。</span><span class="sxs-lookup"><span data-stu-id="f20db-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="f20db-148">對於找出的已孤立工作，如果這些工作是不需要的，或是必須與正確的上層專案建立關聯，請考慮加以刪除。</span><span class="sxs-lookup"><span data-stu-id="f20db-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="f20db-149">對於任何大於 1,250 天期間的工作，請考慮新增多個工作來表示總期間 (如果可行)。</span><span class="sxs-lookup"><span data-stu-id="f20db-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="f20db-150">標示有星號 (\*) 的項目因客戶關係管理 (CRM) 僅支援 7,320 週期擴充而有限制。</span><span class="sxs-lookup"><span data-stu-id="f20db-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="f20db-151">您必須保持在此限制之下。</span><span class="sxs-lookup"><span data-stu-id="f20db-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="f20db-152">資源指派關聯</span><span class="sxs-lookup"><span data-stu-id="f20db-152">Resource Assignment relationships</span></span>
<span data-ttu-id="f20db-153">為了確保升級成功，必須正確維護下列關聯：</span><span class="sxs-lookup"><span data-stu-id="f20db-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="f20db-154">分工結構圖中所有的資源指派都必須與同一個專案相關聯。</span><span class="sxs-lookup"><span data-stu-id="f20db-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="f20db-155">分工結構圖中所有的資源指派都必須與同一個專案中的專案團隊成員建立關聯。</span><span class="sxs-lookup"><span data-stu-id="f20db-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="f20db-156">可能的風險降低步驟</span><span class="sxs-lookup"><span data-stu-id="f20db-156">Potential mitigation steps</span></span>
- <span data-ttu-id="f20db-157">找出所有不在上述條件範圍內的工作。</span><span class="sxs-lookup"><span data-stu-id="f20db-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="f20db-158">任何不再有效的資源指派都必須加以刪除。</span><span class="sxs-lookup"><span data-stu-id="f20db-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="f20db-159">專案工作相依性關聯</span><span class="sxs-lookup"><span data-stu-id="f20db-159">Project task dependency relationships</span></span>
<span data-ttu-id="f20db-160">為了確保升級成功，必須正確維護下列關聯：</span><span class="sxs-lookup"><span data-stu-id="f20db-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="f20db-161">所有專案工作相依性都必須與相同的專案相關聯。</span><span class="sxs-lookup"><span data-stu-id="f20db-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="f20db-162">工作不能有參照多次的相同相依性。</span><span class="sxs-lookup"><span data-stu-id="f20db-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]