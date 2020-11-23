---
title: 專案追蹤概觀
description: 本主題提供有關如何追蹤專案進度和成本耗用的資訊。
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f159ecac53b824ef208221bb14958923fb5da63b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127330"
---
# <a name="project-tracking-overview"></a><span data-ttu-id="d44a8-103">專案追蹤概觀</span><span class="sxs-lookup"><span data-stu-id="d44a8-103">Project tracking overview</span></span>

<span data-ttu-id="d44a8-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="d44a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d44a8-105">對照排程追蹤進度的需求會因行業不同而有所不同。</span><span class="sxs-lookup"><span data-stu-id="d44a8-105">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="d44a8-106">有些行業以細微等級進行追蹤，而其他行業則以較粗略等級進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="d44a8-106">Some industries track at a granular level, where other industries track at a higher level.</span></span> <span data-ttu-id="d44a8-107">本主題說明如何進行排程以符合您組織的需求。</span><span class="sxs-lookup"><span data-stu-id="d44a8-107">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="d44a8-108">投入量追蹤檢視表</span><span class="sxs-lookup"><span data-stu-id="d44a8-108">Effort tracking view</span></span>

<span data-ttu-id="d44a8-109">**投入量追蹤** 檢視表會追蹤排程中工作的進度，方法是將花費在工作的實際努力時數，與工作的計劃努力時數進行比較。</span><span class="sxs-lookup"><span data-stu-id="d44a8-109">The **Effort tracking** view tracks the progress of tasks in the schedule by comparing the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="d44a8-110">Dynamics 365 Project Operations 使用下列公式來計算追蹤計量：</span><span class="sxs-lookup"><span data-stu-id="d44a8-110">Dynamics 365 Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="d44a8-111">**進度百分比**：目前為止已花費實際投入量 ÷ 完工估計值 (EAC)</span><span class="sxs-lookup"><span data-stu-id="d44a8-111">**Progress percentage**: Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="d44a8-112">**尚未完工估計值 (ETC)**：計劃投入量 – 目前為止已花費實際投入量</span><span class="sxs-lookup"><span data-stu-id="d44a8-112">**Estimate to complete (ETC)**: Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="d44a8-113">**EAC**：剩餘未完成投入量 + 目前為止已花費實際投入量</span><span class="sxs-lookup"><span data-stu-id="d44a8-113">**EAC**: Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="d44a8-114">**預計投入量差異**：計劃投入量 – EAC</span><span class="sxs-lookup"><span data-stu-id="d44a8-114">**Projected effort variance**: Planned effort – EAC</span></span>

<span data-ttu-id="d44a8-115">Project Operations 會顯示對工作的投入量差異預測。</span><span class="sxs-lookup"><span data-stu-id="d44a8-115">Project Operations shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="d44a8-116">如果 EAC 大於計劃投入量，則推測任務需要比原先規劃還要多的時間，並且進度落後於排程。</span><span class="sxs-lookup"><span data-stu-id="d44a8-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned and is behind schedule.</span></span> <span data-ttu-id="d44a8-117">如果 EAC 小於計劃投入量，則推測任務需要比原先規劃還要少的時間，並且進度較排程提前。</span><span class="sxs-lookup"><span data-stu-id="d44a8-117">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned and is ahead schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="d44a8-118">重新推測投入量</span><span class="sxs-lookup"><span data-stu-id="d44a8-118">Reprojecting effort</span></span>

<span data-ttu-id="d44a8-119">專案經理經常會修訂工作的原始預估值。</span><span class="sxs-lookup"><span data-stu-id="d44a8-119">Project managers often revise the original estimates on a task.</span></span> <span data-ttu-id="d44a8-120">專案重新推測是專案經理在專案目前狀態的考量下，對估計值所產生的看法。</span><span class="sxs-lookup"><span data-stu-id="d44a8-120">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="d44a8-121">不過，我們不建議專案經理變更基準數字。</span><span class="sxs-lookup"><span data-stu-id="d44a8-121">However, we don't recommend that project managers change the baseline numbers.</span></span> <span data-ttu-id="d44a8-122">這是因為專案基準代表專案排程和成本預估值的既定事實原始資料，而且所有專案利害關係人都同意此基準。</span><span class="sxs-lookup"><span data-stu-id="d44a8-122">This is because the project baseline represents the established source of truth for the project schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="d44a8-123">有兩種專案經理可用來重新推測工作投入量的方法：</span><span class="sxs-lookup"><span data-stu-id="d44a8-123">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="d44a8-124">以新的對工作實際剩餘未完成投入量的估計值覆寫預設 ETC。</span><span class="sxs-lookup"><span data-stu-id="d44a8-124">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="d44a8-125">以新的對工作實際進度的估計值覆寫預設進行百分比。</span><span class="sxs-lookup"><span data-stu-id="d44a8-125">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="d44a8-126">每一個方法都會導致重新計算工作的 ETC、EAC、進度百分比，以及工作的預計投入量差異。</span><span class="sxs-lookup"><span data-stu-id="d44a8-126">Each approach causes a recalculation of the task's ETC, EAC, progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="d44a8-127">也會重新計算摘要工作的 EAC、ETC 和進度百分比，並產生最新的投入量差異預測。</span><span class="sxs-lookup"><span data-stu-id="d44a8-127">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="d44a8-128">重新推測摘要工作的投入量</span><span class="sxs-lookup"><span data-stu-id="d44a8-128">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="d44a8-129">您可以重新推測摘要工作或容器工作的投入量。</span><span class="sxs-lookup"><span data-stu-id="d44a8-129">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="d44a8-130">不論使用者用於重新推測的是摘要工作的剩餘未完成投入量還是進度百分比，下列這組計算都會開始：</span><span class="sxs-lookup"><span data-stu-id="d44a8-130">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="d44a8-131">計算工作的 EAC、ETC 和進度百分比。</span><span class="sxs-lookup"><span data-stu-id="d44a8-131">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="d44a8-132">按照與工作上原始 EAC 相同的比例，將新的 EAC 分佈到下層工作。</span><span class="sxs-lookup"><span data-stu-id="d44a8-132">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="d44a8-133">對下至分葉節點工作的每一項個別工作計算新的 EAC。</span><span class="sxs-lookup"><span data-stu-id="d44a8-133">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="d44a8-134">根據 EAC 值，對下至分葉節點的下層受影響工作重新計算其 ETC 和進度百分比。</span><span class="sxs-lookup"><span data-stu-id="d44a8-134">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="d44a8-135">這會產生對工作投入量差異的新預測。</span><span class="sxs-lookup"><span data-stu-id="d44a8-135">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="d44a8-136">重新計算從摘要工作一直到根節點的 EAC。</span><span class="sxs-lookup"><span data-stu-id="d44a8-136">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="d44a8-137">成本追蹤檢視表</span><span class="sxs-lookup"><span data-stu-id="d44a8-137">Cost tracking view</span></span> 

<span data-ttu-id="d44a8-138">**成本追蹤** 檢視表會將工作已花費的實際成本與工作的計劃成本進行比較。</span><span class="sxs-lookup"><span data-stu-id="d44a8-138">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="d44a8-139">此檢視表僅顯示人力成本，並不包含來自費用估計的成本。</span><span class="sxs-lookup"><span data-stu-id="d44a8-139">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> <span data-ttu-id="d44a8-140">Project Operations 使用下列公式來計算追蹤計量：</span><span class="sxs-lookup"><span data-stu-id="d44a8-140">Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="d44a8-141">**成本耗用百分比**：目前為止已花費實際成本 ÷ 完工估計成本</span><span class="sxs-lookup"><span data-stu-id="d44a8-141">**Percentage of cost consumed**: Actual cost spent to date ÷ Estimated cost at completion</span></span>
- <span data-ttu-id="d44a8-142">**尚未完工成本 (CTC)**：計劃成本 – 目前為止已花費實際成本</span><span class="sxs-lookup"><span data-stu-id="d44a8-142">**Cost to complete (CTC)**: Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="d44a8-143">**EAC**：剩餘成本 + 目前為止已花費實際成本</span><span class="sxs-lookup"><span data-stu-id="d44a8-143">**EAC**: Remaining cost + Actual cost spent to date</span></span>
- <span data-ttu-id="d44a8-144">**預計成本差異**：計劃成本 – EAC</span><span class="sxs-lookup"><span data-stu-id="d44a8-144">**Projected cost variance**: Planned cost – EAC</span></span>

<span data-ttu-id="d44a8-145">成本差異預測會顯示在工作上。</span><span class="sxs-lookup"><span data-stu-id="d44a8-145">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="d44a8-146">如果 EAC 大於計劃成本，則推測工作耗用比原先規劃還要多的成本。</span><span class="sxs-lookup"><span data-stu-id="d44a8-146">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="d44a8-147">因此，有預算超支的趨勢。</span><span class="sxs-lookup"><span data-stu-id="d44a8-147">Therefore, it's trending over budget.</span></span> <span data-ttu-id="d44a8-148">如果 EAC 小於計劃成本，則推測工作耗用比原先規劃還要小的成本。</span><span class="sxs-lookup"><span data-stu-id="d44a8-148">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="d44a8-149">因此，有維持在預算內的趨勢。</span><span class="sxs-lookup"><span data-stu-id="d44a8-149">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="d44a8-150">專案經理對成本的重新推測</span><span class="sxs-lookup"><span data-stu-id="d44a8-150">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="d44a8-151">重新推測投入量時，CTC、EAC、成本耗用百分比和預計成本差異全都會在 **成本追蹤** 檢視表中重新計算。</span><span class="sxs-lookup"><span data-stu-id="d44a8-151">When effort is reprojected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="d44a8-152">專案狀態摘要</span><span class="sxs-lookup"><span data-stu-id="d44a8-152">Project status summary</span></span>

<span data-ttu-id="d44a8-153">追蹤 **投入量追蹤** 和 **成本追蹤** 檢視表中的資料時，會顯示專案根節點、摘要工作和分葉節點工作層級上的進度和成本耗用量。</span><span class="sxs-lookup"><span data-stu-id="d44a8-153">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="d44a8-154">專案 **實體** 頁面上的 **狀態** 區段會顯示專案層級狀態的摘要。</span><span class="sxs-lookup"><span data-stu-id="d44a8-154">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="d44a8-155">狀態摘要欄位</span><span class="sxs-lookup"><span data-stu-id="d44a8-155">Status summary fields</span></span>

<span data-ttu-id="d44a8-156">**整體專案狀態** 欄位是顯示專案整體狀態的可編輯欄位。</span><span class="sxs-lookup"><span data-stu-id="d44a8-156">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="d44a8-157">此欄位會使用色彩代碼 (例如綠色、黃色和紅色) 來表示風險增加。</span><span class="sxs-lookup"><span data-stu-id="d44a8-157">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="d44a8-158">**註解** 欄位可讓專案經理輸入關於狀態的特定註解。</span><span class="sxs-lookup"><span data-stu-id="d44a8-158">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="d44a8-159">**狀態更新時間** 欄位不可編輯的欄位，其值是指示狀態上次更新時的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="d44a8-159">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="d44a8-160">**排程效能** 和 **成本績效** 欄位是從追蹤日期開始設定。</span><span class="sxs-lookup"><span data-stu-id="d44a8-160">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="d44a8-161">當 **投入量追蹤** 檢視表中根節點的排程與成本差異為正值時，您可以將這些欄位設定為 **提前**。</span><span class="sxs-lookup"><span data-stu-id="d44a8-161">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="d44a8-162">當根節點的排程與成本差異是負值時，您可以將其設定為 **落後**。</span><span class="sxs-lookup"><span data-stu-id="d44a8-162">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
