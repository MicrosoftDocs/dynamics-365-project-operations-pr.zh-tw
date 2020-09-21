---
title: 專案進度及成本耗用
description: 本主題提供有關如何追蹤專案進度和成本耗用的資訊。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749973"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="f759a-103">專案進度及成本耗用</span><span class="sxs-lookup"><span data-stu-id="f759a-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f759a-104">對照排程追蹤進度的需求會因行業不同而有所不同。</span><span class="sxs-lookup"><span data-stu-id="f759a-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="f759a-105">有些行業以細微等級進行追蹤，而其他行業則以較粗略等級進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="f759a-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="f759a-106">本主題說明如何進行排程以符合您組織的需求。</span><span class="sxs-lookup"><span data-stu-id="f759a-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="f759a-107">投入量追蹤檢視表</span><span class="sxs-lookup"><span data-stu-id="f759a-107">Effort tracking view</span></span>

<span data-ttu-id="f759a-108">**投入量追蹤**檢視表會追蹤排程中工作的進度。</span><span class="sxs-lookup"><span data-stu-id="f759a-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="f759a-109">此檢視表會將花費在工作上的實際投入時數，與該工作的計劃投入時數進行比較。</span><span class="sxs-lookup"><span data-stu-id="f759a-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="f759a-110">PSA 使用下列公式來計算追蹤計量：</span><span class="sxs-lookup"><span data-stu-id="f759a-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="f759a-111">進度百分比 = 目前為止已花費實際投入量 ÷ 工作的計劃投入量</span><span class="sxs-lookup"><span data-stu-id="f759a-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="f759a-112">尚未完工估計值 (ETC) = 計劃投入量 – 目前為止已花費實際投入量</span><span class="sxs-lookup"><span data-stu-id="f759a-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="f759a-113">完工估計值 (EAC) = 剩餘未完成投入量 + 目前為止已花費實際投入量</span><span class="sxs-lookup"><span data-stu-id="f759a-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="f759a-114">預計投入量差異 = 計畫投入量 – EAC</span><span class="sxs-lookup"><span data-stu-id="f759a-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="f759a-115">PSA 會顯示對工作的投入量差異預測。</span><span class="sxs-lookup"><span data-stu-id="f759a-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="f759a-116">如果 EAC 大於計劃投入量，則推測工作需要比原先規劃還要多的時間。</span><span class="sxs-lookup"><span data-stu-id="f759a-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="f759a-117">因此，進度落後於排程。</span><span class="sxs-lookup"><span data-stu-id="f759a-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="f759a-118">如果 EAC 小於計劃投入量，則推測工作需要比原先規劃還要少的時間。</span><span class="sxs-lookup"><span data-stu-id="f759a-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="f759a-119">因此，進度較排程提前。</span><span class="sxs-lookup"><span data-stu-id="f759a-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="f759a-120">重新預測投入量</span><span class="sxs-lookup"><span data-stu-id="f759a-120">Re-projecting effort</span></span>

<span data-ttu-id="f759a-121">修訂工作的原始預估值，對專案經理來說很平常。</span><span class="sxs-lookup"><span data-stu-id="f759a-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="f759a-122">專案重新預測是專案經理考慮到專案的目前狀態，而對估計值產生的看法。</span><span class="sxs-lookup"><span data-stu-id="f759a-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="f759a-123">然而，我們不建議專案經理變更基準數字，因為專案基準代表專案排程和成本預估值的既定事實原始資料，這是所有專案利害關係人都同意的。</span><span class="sxs-lookup"><span data-stu-id="f759a-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="f759a-124">有兩種專案經理可用來重新預測工作投入量的方法：</span><span class="sxs-lookup"><span data-stu-id="f759a-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="f759a-125">以新的對工作實際剩餘未完成投入量的估計值覆寫預設 ETC。</span><span class="sxs-lookup"><span data-stu-id="f759a-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="f759a-126">以新的對工作實際進度的估計值覆寫預設進行百分比。</span><span class="sxs-lookup"><span data-stu-id="f759a-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="f759a-127">上述每一種方法都會導致重新計算工作的 ETC、EAC 和進度百分比，以及工作的預計投入量差異。</span><span class="sxs-lookup"><span data-stu-id="f759a-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="f759a-128">也會重新計算摘要工作的 EAC、ETC 和進度百分比，並產生最新的投入量差異預測。</span><span class="sxs-lookup"><span data-stu-id="f759a-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="f759a-129">摘要工作的投入量重新預測</span><span class="sxs-lookup"><span data-stu-id="f759a-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="f759a-130">您可以重新預測摘要工作或容器工作的投入量。</span><span class="sxs-lookup"><span data-stu-id="f759a-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="f759a-131">不論使用者用於重新預測的是摘要工作的剩餘未完成投入量還是進度百分比，下列這組計算都會開始：</span><span class="sxs-lookup"><span data-stu-id="f759a-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="f759a-132">計算工作的 EAC、ETC 和進度百分比。</span><span class="sxs-lookup"><span data-stu-id="f759a-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="f759a-133">按照與工作上原始 EAC 相同的比例，將新的 EAC 分佈到下層工作。</span><span class="sxs-lookup"><span data-stu-id="f759a-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="f759a-134">對下至分葉節點工作的每一項個別工作計算新的 EAC。</span><span class="sxs-lookup"><span data-stu-id="f759a-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="f759a-135">根據 EAC 值，對下至分葉節點的下層受影響工作重新計算其 ETC 和進度百分比。</span><span class="sxs-lookup"><span data-stu-id="f759a-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="f759a-136">這會產生對工作投入量差異的新預測。</span><span class="sxs-lookup"><span data-stu-id="f759a-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="f759a-137">重新計算從摘要工作一直到根節點的 EAC。</span><span class="sxs-lookup"><span data-stu-id="f759a-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="f759a-138">成本追蹤檢視表</span><span class="sxs-lookup"><span data-stu-id="f759a-138">Cost tracking view</span></span> 

<span data-ttu-id="f759a-139">**成本追蹤**檢視表會將工作已花費的實際成本與工作的計劃成本進行比較。</span><span class="sxs-lookup"><span data-stu-id="f759a-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="f759a-140">此檢視表僅顯示人力成本，並不包含來自費用估計的成本。</span><span class="sxs-lookup"><span data-stu-id="f759a-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="f759a-141">PSA 使用下列公式來計算追蹤計量：</span><span class="sxs-lookup"><span data-stu-id="f759a-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="f759a-142">成本耗用百分比 = 目前為止已花費實際成本 ÷ 工作的計劃成本</span><span class="sxs-lookup"><span data-stu-id="f759a-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="f759a-143">尚未完工成本 (CTC) = 計劃成本 – 目前為止已花費實際成本</span><span class="sxs-lookup"><span data-stu-id="f759a-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="f759a-144">EAC = CTC + 目前為止已花費實際成本</span><span class="sxs-lookup"><span data-stu-id="f759a-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="f759a-145">預計成本差異 = 計劃成本 – EAC</span><span class="sxs-lookup"><span data-stu-id="f759a-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="f759a-146">成本差異預測會顯示在工作上。</span><span class="sxs-lookup"><span data-stu-id="f759a-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="f759a-147">如果 EAC 大於計劃成本，則推測工作耗用比原先規劃還要多的成本。</span><span class="sxs-lookup"><span data-stu-id="f759a-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="f759a-148">因此，有預算超支的趨勢。</span><span class="sxs-lookup"><span data-stu-id="f759a-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="f759a-149">如果 EAC 小於計劃成本，則推測工作耗用比原先規劃還要小的成本。</span><span class="sxs-lookup"><span data-stu-id="f759a-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="f759a-150">因此，有維持在預算內的趨勢。</span><span class="sxs-lookup"><span data-stu-id="f759a-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="f759a-151">專案經理對成本的重新預測</span><span class="sxs-lookup"><span data-stu-id="f759a-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="f759a-152">重新預測投入量時，CTC、EAC、成本耗用百分比和預計成本差異全都會在**成本追蹤**檢視表中重新計算。</span><span class="sxs-lookup"><span data-stu-id="f759a-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="f759a-153">專案狀態摘要</span><span class="sxs-lookup"><span data-stu-id="f759a-153">Project status summary</span></span>

<span data-ttu-id="f759a-154">追蹤**投入量追蹤**和**成本追蹤**檢視表中的資料時，會顯示專案根節點、摘要工作和分葉節點工作層級上的進度和成本耗用量。</span><span class="sxs-lookup"><span data-stu-id="f759a-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="f759a-155">專案**實體**頁面上的**狀態**區段會顯示專案層級狀態的摘要。</span><span class="sxs-lookup"><span data-stu-id="f759a-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="f759a-156">狀態摘要欄位</span><span class="sxs-lookup"><span data-stu-id="f759a-156">Status summary fields</span></span>

<span data-ttu-id="f759a-157">**整體專案狀態**欄位是顯示專案整體狀態的可編輯欄位。</span><span class="sxs-lookup"><span data-stu-id="f759a-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="f759a-158">此欄位會使用色彩代碼 (例如綠色、黃色和紅色) 來表示風險增加。</span><span class="sxs-lookup"><span data-stu-id="f759a-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="f759a-159">**註解**欄位可讓專案經理輸入關於狀態的特定註解。</span><span class="sxs-lookup"><span data-stu-id="f759a-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="f759a-160">**狀態更新時間**欄位不可編輯的欄位，其值是指示狀態上次更新時的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f759a-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="f759a-161">**排程效能**和**成本績效**欄位是從追蹤日期開始設定。</span><span class="sxs-lookup"><span data-stu-id="f759a-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="f759a-162">當**投入量追蹤**檢視表中根節點的排程與成本差異為正值時，您可以將這些欄位設定為**提前**。</span><span class="sxs-lookup"><span data-stu-id="f759a-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="f759a-163">當根節點的排程與成本差異是負值時，您可以將其設定為**落後**。</span><span class="sxs-lookup"><span data-stu-id="f759a-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
