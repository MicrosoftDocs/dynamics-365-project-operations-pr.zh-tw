---
title: 管理營收估計值
description: 此主題提供有關如何使用專案的營收估計值的資訊。
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278993"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="abdfb-103">管理營收估計值</span><span class="sxs-lookup"><span data-stu-id="abdfb-103">Manage revenue estimates</span></span>

<span data-ttu-id="abdfb-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="abdfb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="abdfb-105">您可以建立、計算、過帳、沖銷或減少營收估計值。</span><span class="sxs-lookup"><span data-stu-id="abdfb-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="abdfb-106">您可以手動或使用週期程序來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="abdfb-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="abdfb-107">此主題提供有關如何使用專案的營收估計值的資訊。</span><span class="sxs-lookup"><span data-stu-id="abdfb-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="abdfb-108">手動管理營收估計值</span><span class="sxs-lookup"><span data-stu-id="abdfb-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="abdfb-109">在固定價格營收估計值專案或 **估計值查詢** 頁面（**專案管理與會計** > **報表和查詢** > **估計值查詢及報表**）中，選取 **估計值**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="abdfb-110">使用週期程序管理營收估計值</span><span class="sxs-lookup"><span data-stu-id="abdfb-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="abdfb-111">移至 **專案管理和會計** > **週期性** > **估計值**，然後選取對應的程序。</span><span class="sxs-lookup"><span data-stu-id="abdfb-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="abdfb-112">建立營收估計值</span><span class="sxs-lookup"><span data-stu-id="abdfb-112">Create a revenue estimate</span></span>

<span data-ttu-id="abdfb-113">完成下列步驟以建立營收估計值。</span><span class="sxs-lookup"><span data-stu-id="abdfb-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="abdfb-114">移至 **專案管理與會計** > **週期性** > **估計值**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="abdfb-115">選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-115">Select **New**.</span></span> <span data-ttu-id="abdfb-116">在 **估計值建立** 頁面上，選取下列參數：</span><span class="sxs-lookup"><span data-stu-id="abdfb-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="abdfb-117">**期間代碼**：此代碼可判斷過帳估計值的頻率。</span><span class="sxs-lookup"><span data-stu-id="abdfb-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="abdfb-118">**估計日期**：處理估計值的日期。</span><span class="sxs-lookup"><span data-stu-id="abdfb-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="abdfb-119">**持續**：選取此核取方塊，僅在前一期間已過帳評估時，或者如果估計值是所建立的第一個評估時，才建立估計值。</span><span class="sxs-lookup"><span data-stu-id="abdfb-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="abdfb-120">如果未選取此選項，則即使尚未在前一個期間過帳評估，也會建立評估。</span><span class="sxs-lookup"><span data-stu-id="abdfb-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="abdfb-121">**完工成本法**：定義如何評估剩餘的專案工作。</span><span class="sxs-lookup"><span data-stu-id="abdfb-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="abdfb-122">如需詳細資訊，請參閱[完工成本法](cost-complete-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="abdfb-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="abdfb-123">**完成方法**：從下列選項中選取完成方法：</span><span class="sxs-lookup"><span data-stu-id="abdfb-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="abdfb-124">**自動**：完成百分比是根據計算中包括的成本線自動計算。</span><span class="sxs-lookup"><span data-stu-id="abdfb-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="abdfb-125">成本範本會定義所包括的成本線。</span><span class="sxs-lookup"><span data-stu-id="abdfb-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="abdfb-126">**手動**：完成百分比等於上次評估的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="abdfb-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="abdfb-127">建立評估之後，您可以在 **估計值** 頁面上變更 **手動計算**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="abdfb-128">**來自成本範本**：自動與手動方法的組合。</span><span class="sxs-lookup"><span data-stu-id="abdfb-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="abdfb-129">此選項會根據成本範本中的預設值而自動或手動設定。</span><span class="sxs-lookup"><span data-stu-id="abdfb-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="abdfb-130">**預測模型**：選取估計值的預測模型。</span><span class="sxs-lookup"><span data-stu-id="abdfb-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="abdfb-131">**列印估計值清單**：建立和顯示估計值清單。</span><span class="sxs-lookup"><span data-stu-id="abdfb-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="abdfb-132">清單包含目前函數的狀態。</span><span class="sxs-lookup"><span data-stu-id="abdfb-132">The list contains the status of the current function.</span></span> <span data-ttu-id="abdfb-133">您可以在報表上列印關於估計值的任何警告。</span><span class="sxs-lookup"><span data-stu-id="abdfb-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="abdfb-134">下列條件會導致估計值清單中出現警告：</span><span class="sxs-lookup"><span data-stu-id="abdfb-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="abdfb-135">超過 100% 的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="abdfb-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="abdfb-136">完成百分比小於零百分比。</span><span class="sxs-lookup"><span data-stu-id="abdfb-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="abdfb-137">**至完成** 欄中的負值金額。</span><span class="sxs-lookup"><span data-stu-id="abdfb-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="abdfb-138">無對應合約金額的估計值。</span><span class="sxs-lookup"><span data-stu-id="abdfb-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="abdfb-139">未附加成本估計值的估計值。</span><span class="sxs-lookup"><span data-stu-id="abdfb-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="abdfb-140">**顯示 Infolog**：選取此選項以接收訊息，其中包含有關工作執行時所處理之估計值專案的資訊。</span><span class="sxs-lookup"><span data-stu-id="abdfb-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="abdfb-141">過帳 WIP 或應計值</span><span class="sxs-lookup"><span data-stu-id="abdfb-141">Post WIP or accruals</span></span>

<span data-ttu-id="abdfb-142">評估估計值之後，會進行維護、減少或增加。</span><span class="sxs-lookup"><span data-stu-id="abdfb-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="abdfb-143">當您使用 **完成的合約** 評估原則時，您可以過帳 WIP，或是在您使用 **已完成百分比** 評估原則時過帳應計值。</span><span class="sxs-lookup"><span data-stu-id="abdfb-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="abdfb-144">估計值期間狀態從 **已建立** 變更為 **已過帳**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="abdfb-145">沖銷 WIP 或應計值</span><span class="sxs-lookup"><span data-stu-id="abdfb-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="abdfb-146">使用沖銷選項來貸記已過帳的 WIP 或應計值，然後建立期間的估計值。</span><span class="sxs-lookup"><span data-stu-id="abdfb-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="abdfb-147">若要沖銷在其他期間中的期間，請沖銷必要的估計值期間，然後重新過帳它們。</span><span class="sxs-lookup"><span data-stu-id="abdfb-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="abdfb-148">因為所有後續期間都是根據先前期間的估計值而定，所以不要略過任何期間。</span><span class="sxs-lookup"><span data-stu-id="abdfb-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="abdfb-149">消除估計值專案並完成專案</span><span class="sxs-lookup"><span data-stu-id="abdfb-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="abdfb-150">估計值程序的最後一個步驟是消除估計值專案，並在完成百分比達到 100% 時結束固定價格專案。</span><span class="sxs-lookup"><span data-stu-id="abdfb-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="abdfb-151">當您執行消除時，會發生下列事件：</span><span class="sxs-lookup"><span data-stu-id="abdfb-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="abdfb-152">對於具有已完成合約的固定價格專案，WIP 值會從餘額帳戶中清除並過帳到損益表。</span><span class="sxs-lookup"><span data-stu-id="abdfb-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="abdfb-153">對於具有已完成百分比的固定價格專案，則會從損益表中移除該應計值。</span><span class="sxs-lookup"><span data-stu-id="abdfb-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="abdfb-154">估計值會將狀態變更為 **已消除**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="abdfb-155">在特殊案例中，百分比可以延伸超過 100%。</span><span class="sxs-lookup"><span data-stu-id="abdfb-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="abdfb-156">發生這種情況時，請使用 **將完工成本設定為零方法** 減少完成百分比，以達到 100%。</span><span class="sxs-lookup"><span data-stu-id="abdfb-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="abdfb-157">沖銷消除</span><span class="sxs-lookup"><span data-stu-id="abdfb-157">Reverse elimination</span></span>

1. <span data-ttu-id="abdfb-158">移至 **專案管理與會計** > **週期** > **估計值** > **沖銷消除**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="abdfb-159">在動作窗格的 **程序** 索引標籤的 **維護** 群組中，選取 **估計值**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="abdfb-160">選取 **沖銷消除**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="abdfb-161">您可以使用此頁面，將指定估計日期和消除狀態為 **已消除** 的所有消除項目進行沖銷。</span><span class="sxs-lookup"><span data-stu-id="abdfb-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="abdfb-162">當您選取適當的欄位後，交易記錄狀態會變更。</span><span class="sxs-lookup"><span data-stu-id="abdfb-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="abdfb-163">這也會在專案階段設定為已完成時，自動將專案狀態變更為 **處理中**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="abdfb-164">專案期間的估計狀態會變更回 **已過帳**。</span><span class="sxs-lookup"><span data-stu-id="abdfb-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]