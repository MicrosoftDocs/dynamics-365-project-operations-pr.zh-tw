---
title: 資源管理變更 (Project Service Automation 3.x)
description: 本主題提供有關資源管理區域變更的資訊。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749932"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="d7ba6-103">資源管理變更 (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="d7ba6-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="d7ba6-104">本主題的各節提供有關已對 Dynamics 365 Project Service Automation 3.x 版資源管理區域所做變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="d7ba6-105">專案估計值</span><span class="sxs-lookup"><span data-stu-id="d7ba6-105">Project estimates</span></span>

<span data-ttu-id="d7ba6-106">專案估計值所根據的不是 **msdyn\_projecttask** entity (**Project Task**)，而是 **msdyn\_resourceassignment** entity (**Resource Assignment**)。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="d7ba6-107">資源指派已成為工作排程和定價的「事實原始資料」。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="d7ba6-108">明細工作</span><span class="sxs-lookup"><span data-stu-id="d7ba6-108">Line tasks</span></span>

<span data-ttu-id="d7ba6-109">在 PSA 3.x 中，明細工作已淘汰 (已被取代)。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="d7ba6-110">指派現在會指向整個工作，而不是明細工作。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="d7ba6-111">下列範例顯示名為「測試工作」的工作在舊版 PSA 以及 PSA 3.x 中如何指派給團隊成員 A 和 B。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="d7ba6-112">**在 PSA 3.x 之前：**</span><span class="sxs-lookup"><span data-stu-id="d7ba6-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="d7ba6-113">測試工作</span><span class="sxs-lookup"><span data-stu-id="d7ba6-113">Test task</span></span>

        - <span data-ttu-id="d7ba6-114">測試工作 – 明細工作 1</span><span class="sxs-lookup"><span data-stu-id="d7ba6-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="d7ba6-115">指派給 A</span><span class="sxs-lookup"><span data-stu-id="d7ba6-115">Assignment to A</span></span>

        - <span data-ttu-id="d7ba6-116">測試工作 – 明細工作 2</span><span class="sxs-lookup"><span data-stu-id="d7ba6-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="d7ba6-117">指派給 B</span><span class="sxs-lookup"><span data-stu-id="d7ba6-117">Assignment to B</span></span>

- <span data-ttu-id="d7ba6-118">**PSA 3.x：**</span><span class="sxs-lookup"><span data-stu-id="d7ba6-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="d7ba6-119">測試工作</span><span class="sxs-lookup"><span data-stu-id="d7ba6-119">Test task</span></span>

        - <span data-ttu-id="d7ba6-120">指派給 A</span><span class="sxs-lookup"><span data-stu-id="d7ba6-120">Assignment to A</span></span>
        - <span data-ttu-id="d7ba6-121">指派給 B</span><span class="sxs-lookup"><span data-stu-id="d7ba6-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="d7ba6-122">未分派指派</span><span class="sxs-lookup"><span data-stu-id="d7ba6-122">Unassigned assignment</span></span>

<span data-ttu-id="d7ba6-123">在 PSA 3.x 中，未分派指派是指派給 **Null** 團隊成員和 **Null** 資源的指派。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="d7ba6-124">未分派指派可能會在幾個案例中發生：</span><span class="sxs-lookup"><span data-stu-id="d7ba6-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="d7ba6-125">如果已建立工作，但尚未將其指派給任何團隊成員，則一律會建立未分派指派。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="d7ba6-126">如果將工作上的所有被指定者移除，就會為該工作重新建立未分派指派。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="d7ba6-127">專案工作實體的排程欄位</span><span class="sxs-lookup"><span data-stu-id="d7ba6-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="d7ba6-128">**msdyn\_projecttask** 實體的欄位已被取代或已移到 **msdyn\_resourceassignment** 實體，或者現在是從 **msdyn\_projectteam** 實體 (**專案團隊成員**) 中參照這些實體。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="d7ba6-129">msdyn\_projecttask (專案工作) 上已被取代的欄位</span><span class="sxs-lookup"><span data-stu-id="d7ba6-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="d7ba6-130">msdyn\_resourceassignment (資源指派) 上的新欄位</span><span class="sxs-lookup"><span data-stu-id="d7ba6-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="d7ba6-131">註解</span><span class="sxs-lookup"><span data-stu-id="d7ba6-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="d7ba6-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="d7ba6-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="d7ba6-133">無</span><span class="sxs-lookup"><span data-stu-id="d7ba6-133">None</span></span> | |
| <span data-ttu-id="d7ba6-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="d7ba6-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="d7ba6-135">無</span><span class="sxs-lookup"><span data-stu-id="d7ba6-135">None</span></span> | |
| <span data-ttu-id="d7ba6-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="d7ba6-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="d7ba6-137">無</span><span class="sxs-lookup"><span data-stu-id="d7ba6-137">None</span></span> | |
| <span data-ttu-id="d7ba6-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="d7ba6-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="d7ba6-139">無</span><span class="sxs-lookup"><span data-stu-id="d7ba6-139">None</span></span> | |
| <span data-ttu-id="d7ba6-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="d7ba6-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="d7ba6-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="d7ba6-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="d7ba6-142">欄位中所儲存 JavaScript 物件標記法 (JSON) 資料結構的格式已變更。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="d7ba6-143">排程分佈</span><span class="sxs-lookup"><span data-stu-id="d7ba6-143">Schedule contour</span></span>

<span data-ttu-id="d7ba6-144">排程分佈是儲存在每個**資源指派**實體 (**msdyn\_resourceassignment**) 的**計劃的工作**欄位 (**msdyn\_plannedwork**)。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="d7ba6-145">結構</span><span class="sxs-lookup"><span data-stu-id="d7ba6-145">Structure</span></span>

<span data-ttu-id="d7ba6-146">排程分佈的新結構由針對排程中每一天定義的彈性時間配量所組成。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="d7ba6-147">每個時間配量都有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="d7ba6-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="d7ba6-148">**開始** – 根據專案行事曆，當天工作時數的開始時間。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="d7ba6-149">**結束** – 根據專案行事曆，當天工作時數的結束時間。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="d7ba6-150">**時數** – 指派的當天時數。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="d7ba6-151">**範例**</span><span class="sxs-lookup"><span data-stu-id="d7ba6-151">**Example**</span></span>

<span data-ttu-id="d7ba6-152">此範例使用專案行事曆，其中工作日為 UTC-8 時區上午 9 點到下午 5 點。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="d7ba6-153">自動排程和手動排程</span><span class="sxs-lookup"><span data-stu-id="d7ba6-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="d7ba6-154">如果工作是自動排程，則以前重後輕方式分配時數，而且工作期間可能會減少。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="d7ba6-155">**範例**</span><span class="sxs-lookup"><span data-stu-id="d7ba6-155">**Example**</span></span>

<span data-ttu-id="d7ba6-156">下列工作自動排程在三天 (2018 年 12 月 3 日到 2018 年 12 月 5 日) 期間的 18 個小時。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="d7ba6-157">如果手動排程工作，則時數會平均分佈到所有日期。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="d7ba6-158">**範例**</span><span class="sxs-lookup"><span data-stu-id="d7ba6-158">**Example**</span></span>

<span data-ttu-id="d7ba6-159">下列工作手動排程在三天 (2018 年 12 月 3 日到 2018 年 12 月 5 日) 期間的 18 個小時。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="d7ba6-160">指派單位</span><span class="sxs-lookup"><span data-stu-id="d7ba6-160">Assignment unit</span></span>

<span data-ttu-id="d7ba6-161">指派單位在 PSA 3.x 中已被取代。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="d7ba6-162">工作投入時數現在會在所有指派的資源中按天數均分。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="d7ba6-163">**範例**</span><span class="sxs-lookup"><span data-stu-id="d7ba6-163">**Example**</span></span>

<span data-ttu-id="d7ba6-164">在此範例中，工作已指派給兩個資源，且自動排程在三天 (2018 年 12 月 3 日到 2018 年 12 月 5 日) 期間的 36 個小時。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="d7ba6-165">指派 1：</span><span class="sxs-lookup"><span data-stu-id="d7ba6-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="d7ba6-166">指派 2：</span><span class="sxs-lookup"><span data-stu-id="d7ba6-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="d7ba6-167">定價維度</span><span class="sxs-lookup"><span data-stu-id="d7ba6-167">Pricing dimensions</span></span>

<span data-ttu-id="d7ba6-168">在 PSA 3.x 中，資源特有定價維度欄位 (例如**角色**和**組織單位**) 已從**msdyn\_projecttask** 實體中移除。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="d7ba6-169">這些欄位目前可以在產生專案估計值時，從資源指派 (**msdyn\_resourceassignment**) 的對應專案團隊成員 (**msdyn\_projectteam**) 中擷取。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="d7ba6-170">新的欄位 **msdyn\_organizationalunit** 已新增至 **msdyn\_projectteam** 實體。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="d7ba6-171">msdyn\_projecttask (專案工作) 上已被取代的欄位</span><span class="sxs-lookup"><span data-stu-id="d7ba6-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="d7ba6-172">改用的 msdyn\_projectteam (專案團隊成員) 中的欄位。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="d7ba6-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="d7ba6-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="d7ba6-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="d7ba6-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="d7ba6-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="d7ba6-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="d7ba6-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="d7ba6-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="d7ba6-177">分佈</span><span class="sxs-lookup"><span data-stu-id="d7ba6-177">Contours</span></span>

<span data-ttu-id="d7ba6-178">定價與估計分佈欄位在 **msdyn\_projecttask** 實體上已被取代。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="d7ba6-179">這些欄位已移到 **msdyn\_resourceassignment** 實體。</span><span class="sxs-lookup"><span data-stu-id="d7ba6-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="d7ba6-180">msdyn\_projecttask (專案工作) 上已被取代的欄位</span><span class="sxs-lookup"><span data-stu-id="d7ba6-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="d7ba6-181">msdyn\_resourceassignment (資源指派) 上的新欄位</span><span class="sxs-lookup"><span data-stu-id="d7ba6-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="d7ba6-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="d7ba6-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="d7ba6-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="d7ba6-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="d7ba6-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="d7ba6-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="d7ba6-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="d7ba6-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="d7ba6-186">下列欄位已新增至 **msdyn\_resourceassignment** 實體：</span><span class="sxs-lookup"><span data-stu-id="d7ba6-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="d7ba6-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d7ba6-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="d7ba6-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d7ba6-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="d7ba6-189">下列規劃、實際和剩餘成本與銷售的欄位在 **msdyn\_projecttask** 實體上保持不變：</span><span class="sxs-lookup"><span data-stu-id="d7ba6-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="d7ba6-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d7ba6-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="d7ba6-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d7ba6-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="d7ba6-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="d7ba6-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="d7ba6-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="d7ba6-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="d7ba6-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="d7ba6-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="d7ba6-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="d7ba6-195">msdyn\_remainingsales</span></span>
