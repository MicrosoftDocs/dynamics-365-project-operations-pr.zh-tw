---
title: 專案投入量追蹤
description: 本主題提供有關如何追蹤專案投入量和工作進度的資訊。
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3fdf7787f0144dace84852a0442406085bdc1639
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010866"
---
# <a name="project-effort-tracking"></a><span data-ttu-id="33f8f-103">專案投入量追蹤</span><span class="sxs-lookup"><span data-stu-id="33f8f-103">Project effort tracking</span></span>

<span data-ttu-id="33f8f-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="33f8f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33f8f-105">對照排程追蹤進度的需求會因行業不同而有所不同。</span><span class="sxs-lookup"><span data-stu-id="33f8f-105">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="33f8f-106">有些行業以細微等級進行追蹤，而其他行業則以較粗略等級進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="33f8f-106">Some industries track at a granular level, where other industries track at a higher level.</span></span> <span data-ttu-id="33f8f-107">本主題說明如何進行排程以符合您組織的需求。</span><span class="sxs-lookup"><span data-stu-id="33f8f-107">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="33f8f-108">投入量追蹤檢視表</span><span class="sxs-lookup"><span data-stu-id="33f8f-108">Effort tracking view</span></span>

<span data-ttu-id="33f8f-109">**投入量追蹤** 檢視表會追蹤排程中工作的進度，方法是將花費在工作的實際努力時數，與工作的計劃努力時數進行比較。</span><span class="sxs-lookup"><span data-stu-id="33f8f-109">The **Effort tracking** view tracks the progress of tasks in the schedule by comparing the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="33f8f-110">Dynamics 365 Project Operations 使用下列公式來計算追蹤計量：</span><span class="sxs-lookup"><span data-stu-id="33f8f-110">Dynamics 365 Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="33f8f-111">**進度百分比**：目前為止已花費實際投入量 ÷ 完工估計值 (EAC)</span><span class="sxs-lookup"><span data-stu-id="33f8f-111">**Progress percentage**: Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="33f8f-112">**剩餘投入量**：完工估計投入量 – 目前為止已花費實際投入量</span><span class="sxs-lookup"><span data-stu-id="33f8f-112">**Remaining Effort**: Estimated effort at complete – Actual effort spent to date</span></span> 
- <span data-ttu-id="33f8f-113">**EAC**：剩餘未完成投入量 + 目前為止已花費實際投入量</span><span class="sxs-lookup"><span data-stu-id="33f8f-113">**EAC**: Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="33f8f-114">**預計投入量差異**：計劃投入量 – EAC</span><span class="sxs-lookup"><span data-stu-id="33f8f-114">**Projected effort variance**: Planned effort – EAC</span></span>

<span data-ttu-id="33f8f-115">Project Operations 會顯示對工作的投入量差異預測。</span><span class="sxs-lookup"><span data-stu-id="33f8f-115">Project Operations shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="33f8f-116">如果 EAC 大於計劃投入量，則推測任務需要比原先規劃還要多的時間，並且進度落後於排程。</span><span class="sxs-lookup"><span data-stu-id="33f8f-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned and is behind schedule.</span></span> <span data-ttu-id="33f8f-117">如果 EAC 小於計劃投入量，則推測任務需要比原先規劃還要少的時間，並且進度較排程提前。</span><span class="sxs-lookup"><span data-stu-id="33f8f-117">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned and is ahead schedule.</span></span>

## <a name="reprojecting-effort-on-leaf-node-tasks"></a><span data-ttu-id="33f8f-118">重新推估分葉節點工作的投入量</span><span class="sxs-lookup"><span data-stu-id="33f8f-118">Reprojecting effort on leaf node tasks</span></span>

<span data-ttu-id="33f8f-119">專案經理經常會修訂工作的原始預估值。</span><span class="sxs-lookup"><span data-stu-id="33f8f-119">Project managers often revise the original estimates on a task.</span></span> <span data-ttu-id="33f8f-120">專案重新推測是專案經理在專案目前狀態的考量下，對估計值所產生的看法。</span><span class="sxs-lookup"><span data-stu-id="33f8f-120">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="33f8f-121">但是，我們不建議專案經理變更計劃投入量數字。</span><span class="sxs-lookup"><span data-stu-id="33f8f-121">However, we don't recommend that project managers change the planned effort numbers.</span></span> <span data-ttu-id="33f8f-122">這是因為專案計劃投入量代表專案排程和成本估計值的既定事實原始資料，這是所有專案利害關係人都同意的。</span><span class="sxs-lookup"><span data-stu-id="33f8f-122">This is because the project planned effort represents the established source of truth for the project schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="33f8f-123">專案經理可以將預設 **剩餘投入量** 更新為工作的新估計值，藉此重新推估工作的投入量。</span><span class="sxs-lookup"><span data-stu-id="33f8f-123">A project manager can reproject effort on tasks by updating the default **Remaining Effort** with a new estimate on the task.</span></span> <span data-ttu-id="33f8f-124">這項更新會導致重新計算工作的完工估計值 (EAC)、進度百分比以及工作的預計投入量差異。</span><span class="sxs-lookup"><span data-stu-id="33f8f-124">This update causes a recalculation of the task's estimate at complete (EAC), progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="33f8f-125">也會重新計算摘要工作的 EAC、ETC 和進度百分比，並產生最新的投入量差異預測。</span><span class="sxs-lookup"><span data-stu-id="33f8f-125">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="33f8f-126">重新推測摘要工作的投入量</span><span class="sxs-lookup"><span data-stu-id="33f8f-126">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="33f8f-127">您可以重新推測摘要工作或容器工作的投入量。</span><span class="sxs-lookup"><span data-stu-id="33f8f-127">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="33f8f-128">專案經理可以更新摘要工作的剩餘投入量。</span><span class="sxs-lookup"><span data-stu-id="33f8f-128">Project managers can update remaining effort on the summary tasks.</span></span> <span data-ttu-id="33f8f-129">更新剩餘投入量會在應用程式中觸發下列這組計算：</span><span class="sxs-lookup"><span data-stu-id="33f8f-129">Updating the remaining effort triggers the following set of calculations in the application:</span></span>

- <span data-ttu-id="33f8f-130">計算工作的 EAC 和進度百分比。</span><span class="sxs-lookup"><span data-stu-id="33f8f-130">The EAC and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="33f8f-131">按照與工作上原始 EAC 相同的比例，將新的 EAC 分佈到下層工作。</span><span class="sxs-lookup"><span data-stu-id="33f8f-131">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="33f8f-132">對下至分葉節點工作的每一項個別工作計算新的 EAC。</span><span class="sxs-lookup"><span data-stu-id="33f8f-132">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="33f8f-133">根據 EAC 值，對下至分葉節點的下層受影響工作重新計算其剩餘投入量和進度百分比。</span><span class="sxs-lookup"><span data-stu-id="33f8f-133">The affected child tasks down to the leaf nodes have their remaining effort and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="33f8f-134">這會產生對工作投入量差異的新預測。</span><span class="sxs-lookup"><span data-stu-id="33f8f-134">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="33f8f-135">重新計算從摘要工作一直到根節點的 EAC。</span><span class="sxs-lookup"><span data-stu-id="33f8f-135">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>


## <a name="project-status-summary"></a><span data-ttu-id="33f8f-136">專案狀態摘要</span><span class="sxs-lookup"><span data-stu-id="33f8f-136">Project status summary</span></span>

<span data-ttu-id="33f8f-137">追蹤 **投入量追蹤** 和 **成本追蹤** 檢視表中的資料時，會顯示專案根節點、摘要工作和分葉節點工作層級上的進度和成本耗用量。</span><span class="sxs-lookup"><span data-stu-id="33f8f-137">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="33f8f-138">專案 **實體** 頁面上的 **狀態** 區段會顯示專案層級狀態的摘要。</span><span class="sxs-lookup"><span data-stu-id="33f8f-138">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="33f8f-139">狀態摘要欄位</span><span class="sxs-lookup"><span data-stu-id="33f8f-139">Status summary fields</span></span>

<span data-ttu-id="33f8f-140">**整體專案狀態** 欄位是顯示專案整體狀態的可編輯欄位。</span><span class="sxs-lookup"><span data-stu-id="33f8f-140">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="33f8f-141">此欄位會使用色彩代碼 (例如綠色、黃色和紅色) 來表示風險增加。</span><span class="sxs-lookup"><span data-stu-id="33f8f-141">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="33f8f-142">**註解** 欄位可讓專案經理輸入關於狀態的特定註解。</span><span class="sxs-lookup"><span data-stu-id="33f8f-142">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="33f8f-143">**狀態更新時間** 欄位不可編輯的欄位，其值是指示狀態上次更新時的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="33f8f-143">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="33f8f-144">**排程效能** 和 **成本績效** 欄位是從追蹤日期開始設定。</span><span class="sxs-lookup"><span data-stu-id="33f8f-144">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="33f8f-145">當 **投入量追蹤** 檢視表中根節點的排程與成本差異為正值時，您可以將這些欄位設定為 **提前**。</span><span class="sxs-lookup"><span data-stu-id="33f8f-145">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="33f8f-146">當根節點的排程與成本差異是負值時，您可以將其設定為 **落後**。</span><span class="sxs-lookup"><span data-stu-id="33f8f-146">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
