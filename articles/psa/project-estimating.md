---
title: 專案成本和營收
description: 此主題提供有關評估專案成本和營收的資訊。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 9862b6c69596f5b998cf40691f8478bb87251583
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073026"
---
# <a name="project-costs-and-revenue"></a><span data-ttu-id="19ead-103">專案成本和營收</span><span class="sxs-lookup"><span data-stu-id="19ead-103">Project costs and revenue</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="19ead-104">專案預估值為專案排程中預估和排程的作業提供財務檢視表。</span><span class="sxs-lookup"><span data-stu-id="19ead-104">Project estimates provide the financial view for work that is estimated and scheduled in the project schedule.</span></span> <span data-ttu-id="19ead-105">**專案** 頁面上的 **估計值** 索引標籤會顯示您規劃中作業的成本與營收影響。</span><span class="sxs-lookup"><span data-stu-id="19ead-105">The **Estimates** tab on the **Projects** page shows the cost and revenue impact of the work that you’re planning.</span></span> <span data-ttu-id="19ead-106">其中也提供許多預先定義維度的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="19ead-106">It also provides information about many predefined dimensions.</span></span> 

> ![[估計值] 索引標籤](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a><span data-ttu-id="19ead-108">專案的成本和銷售值</span><span class="sxs-lookup"><span data-stu-id="19ead-108">Cost and sales values of the project</span></span>

<span data-ttu-id="19ead-109">價目表定義專案中角色的成本與帳單費率。</span><span class="sxs-lookup"><span data-stu-id="19ead-109">Price lists define the cost and bill rates for roles in a project.</span></span> <span data-ttu-id="19ead-110">您可以根據與指派至工作之職位名稱及具名資源相關的角色，判斷作業的成本與營收影響。</span><span class="sxs-lookup"><span data-stu-id="19ead-110">You can determine the cost and revenue impact of the work, based on the roles that are associated with the position name and the named resource that is assigned to a task.</span></span> <span data-ttu-id="19ead-111">如果存在未有任何指派 (一般或具名) 的工作，則無法取得成本或銷售估計。</span><span class="sxs-lookup"><span data-stu-id="19ead-111">If there are tasks that don't have any assignments (generic or named), you can’t get cost or sales estimates.</span></span> <span data-ttu-id="19ead-112">成本與銷售值會考慮價目表中定義的日期。</span><span class="sxs-lookup"><span data-stu-id="19ead-112">Cost and sales values consider the date that is defined in the price lists.</span></span>

### <a name="default-cost-price"></a><span data-ttu-id="19ead-113">預設成本價</span><span class="sxs-lookup"><span data-stu-id="19ead-113">Default cost price</span></span>  

<span data-ttu-id="19ead-114">每個專案都屬於某個組織。</span><span class="sxs-lookup"><span data-stu-id="19ead-114">Every project belongs to an organization.</span></span> <span data-ttu-id="19ead-115">此組織會顯示在專案的 **承包單位** 欄位中。</span><span class="sxs-lookup"><span data-stu-id="19ead-115">This organization is shown in the **Contracting Unit** field in the project.</span></span> <span data-ttu-id="19ead-116">與承包單位相關的價目表會用來決定單位成本價。</span><span class="sxs-lookup"><span data-stu-id="19ead-116">The price list that is associated with the contracting unit is used to determine the unit cost price.</span></span> <span data-ttu-id="19ead-117">若要針對估計明細所定義的日期決定角色的正確成本價，請在成本價目表中搜尋角色、單位和組織單位的組合。</span><span class="sxs-lookup"><span data-stu-id="19ead-117">To determine the correct cost prices on roles for the date that is defined on estimate lines, search for the combination of role, unit, and organizational unit in the cost price list.</span></span> 

<span data-ttu-id="19ead-118">因此，您必須將所有工作都指派給資源，才能計算其成本價。</span><span class="sxs-lookup"><span data-stu-id="19ead-118">So that their cost prices can be calculated, all tasks must be assigned to a resource.</span></span> <span data-ttu-id="19ead-119">任何未指派工作都將有 0.00 的成本價。</span><span class="sxs-lookup"><span data-stu-id="19ead-119">Any uwnassigned tasks will have a cost price of 0.00.</span></span>

<span data-ttu-id="19ead-120">如果角色、單位和組織單位的組合沒有從承包單位的價目表傳回成本價，則系統會忽略單位。</span><span class="sxs-lookup"><span data-stu-id="19ead-120">If the combination of role, unit, and organizational unit doesn't return a cost price from the contracting unit's price list, the system ignores the unit.</span></span> <span data-ttu-id="19ead-121">而是只會搜尋角色與組織單位的組合。</span><span class="sxs-lookup"><span data-stu-id="19ead-121">Instead, it searches for the combination of just role and organizational unit.</span></span> <span data-ttu-id="19ead-122">如果找到成本價，則使用轉換因數將其轉換為您在估計明細上所選取的單位。</span><span class="sxs-lookup"><span data-stu-id="19ead-122">If a cost price is found, conversion factors are used to convert it to the unit that you selected on the estimate line.</span></span>

<span data-ttu-id="19ead-123">如果角色和組織單位的組合沒有從承包單位的價目表傳回成本價，則系統會忽略組織單位。</span><span class="sxs-lookup"><span data-stu-id="19ead-123">If the combination of role and organizational unit doesn't return a cost price, the system ignores the organizational unit.</span></span> <span data-ttu-id="19ead-124">而是搜尋角色和單位的組合，以設定預設價格 (在套用任何轉換之後)。</span><span class="sxs-lookup"><span data-stu-id="19ead-124">Instead, it searches for the combination of role and unit to set the default price (after any conversion is applied).</span></span>

<span data-ttu-id="19ead-125">如果系統未找到角色的價格，則估計明細中的成本價會設定為 **0.00** 的預設值。</span><span class="sxs-lookup"><span data-stu-id="19ead-125">If the system doesn't find a price for the role, the cost price on the estimate line is set to a default value of **0.00**.</span></span> <span data-ttu-id="19ead-126">在專案成本估計明細上的所有成本金額都是使用承包單位的貨幣來記錄。</span><span class="sxs-lookup"><span data-stu-id="19ead-126">All cost amounts on the project cost estimate lines are recorded in the currency of the contracting unit.</span></span>

> [!NOTE]
> <span data-ttu-id="19ead-127">根據預設，Microsoft Dynamics 365 會以基準貨幣儲存成本金額。</span><span class="sxs-lookup"><span data-stu-id="19ead-127">By default, Microsoft Dynamics 365 stores cost amounts in your base currency.</span></span> <span data-ttu-id="19ead-128">不過， **估計值** 索引標籤上顯示的成本金額是以承包單位的貨幣來表示。</span><span class="sxs-lookup"><span data-stu-id="19ead-128">However, the cost amounts that are shown on the **Estimates** tab are in the currency of the contracting unit.</span></span>  

### <a name="default-sales-price"></a><span data-ttu-id="19ead-129">預設售價</span><span class="sxs-lookup"><span data-stu-id="19ead-129">Default sales price</span></span> 

<span data-ttu-id="19ead-130">銷售價目表是由專案所附加至的銷售實體或專案客戶所決定。</span><span class="sxs-lookup"><span data-stu-id="19ead-130">The sales price list is determined by either the sales entity that the project is attached to or the project customer.</span></span> <span data-ttu-id="19ead-131">當銷售實體 (例如商機、報價或合約) 與專案產生關聯時，銷售實體的銷售價是由與報價或合約相關聯的價目表所決定。</span><span class="sxs-lookup"><span data-stu-id="19ead-131">When a sales entity, such as opportunity, quote, or contract, is associated with the project, the sales entity's sales price is determined by the price list that is associated with the quote or contract.</span></span> <span data-ttu-id="19ead-132">如果報價或合約有自訂價目表，則使用該價目表做為專案估計值的預設銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="19ead-132">If the quote or contract has a custom price list, that price list is used as the default sales price list for project estimates.</span></span> <span data-ttu-id="19ead-133">如果不存在與銷售實體的關聯，則使用參數中的預設銷售價目表做為與專案所定義客戶貨幣相符的專案預設銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="19ead-133">If there is no association with sales entities, the default sales price list from the parameters is used as the project's default sales price list matched by the customer currency that is defined on the project.</span></span>

<span data-ttu-id="19ead-134">每個評估明細都有一個可與之關聯的資源分配單位。</span><span class="sxs-lookup"><span data-stu-id="19ead-134">Each estimate line has a resourcing unit that is associated with it.</span></span> <span data-ttu-id="19ead-135">資源分配單位表示為了完成工作而從中預約資源的組織單位。</span><span class="sxs-lookup"><span data-stu-id="19ead-135">The resourcing unit indicates the organizational unit that resources are booked from to complete the task.</span></span> <span data-ttu-id="19ead-136">若要決定相關聯角色的銷售價，請在銷售價目表中搜尋角色、單位和資源分配單位的組合。</span><span class="sxs-lookup"><span data-stu-id="19ead-136">To determine the sales price for the associated roles, search for the combination of role, unit, and resourcing unit in the sales price list.</span></span> <span data-ttu-id="19ead-137">如果工作上沒有任何指派，工作的銷售價就是 0.00。</span><span class="sxs-lookup"><span data-stu-id="19ead-137">If there are no assignments on the task, the sales price for the task is 0.00.</span></span>

<span data-ttu-id="19ead-138">如果角色、單位和資源分配單位的組合沒有從銷售價目表傳回銷售價，則系統會忽略單位。</span><span class="sxs-lookup"><span data-stu-id="19ead-138">If the combination of role, unit, and resourcing unit doesn't return a sales price from the sales price list, the system ignores the unit.</span></span> <span data-ttu-id="19ead-139">而是只會搜尋角色與資源分配單位的組合。</span><span class="sxs-lookup"><span data-stu-id="19ead-139">Instead, it searches for the combination of just role and resourcing unit.</span></span> <span data-ttu-id="19ead-140">如果找到銷售價，則使用轉換因數將其轉換為您在銷售估計明細上所選取的單位。</span><span class="sxs-lookup"><span data-stu-id="19ead-140">If a sales price is found, conversion factors are used to convert it to the unit that you selected on the sales estimate line.</span></span> 

<span data-ttu-id="19ead-141">如果角色和資源分配單位的組合沒有從銷售價目表傳回銷售價，則系統會忽略資源分配單位。</span><span class="sxs-lookup"><span data-stu-id="19ead-141">If the combination of role and resourcing unit doesn't return a sales price from the sales price list, the system ignores the resourcing unit.</span></span> <span data-ttu-id="19ead-142">而是搜尋角色和單位的組合，以設定預設價格 (在套用任何轉換之後)。</span><span class="sxs-lookup"><span data-stu-id="19ead-142">Instead, it searches for the combination of role and unit to set the default price (after any conversion is applied).</span></span>

<span data-ttu-id="19ead-143">如果系統未找到角色的價格，則估計明細中的銷售價會設定為 **0.00** 的預設值。</span><span class="sxs-lookup"><span data-stu-id="19ead-143">If the system doesn't find a price for the role, the sales price on the estimate line is set to a default value of **0.00**.</span></span>

<span data-ttu-id="19ead-144">**估計值** 索引標籤有一個顯示估計明細的網格檢視表。</span><span class="sxs-lookup"><span data-stu-id="19ead-144">The **Estimates** tab has a grid view that shows estimate lines.</span></span> <span data-ttu-id="19ead-145">網格包含單位、總成本價和總銷售價各欄，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="19ead-145">The grid includes columns for the unit, total cost price, and total sales price, as shown in the following illustration.</span></span> 

> ![[估計值] 索引標籤上的網格檢視表](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a><span data-ttu-id="19ead-147">專案估計值的分時期檢視表</span><span class="sxs-lookup"><span data-stu-id="19ead-147">Time-phased view of project estimates</span></span>

<span data-ttu-id="19ead-148">專案估計值的分時期檢視表顯示來自網格檢視表、散佈在所選時幅之時間表上的估計資料。</span><span class="sxs-lookup"><span data-stu-id="19ead-148">The time-phased view of project estimates shows the estimate data from the grid view across the timeline, in a time scale that you select.</span></span> <span data-ttu-id="19ead-149">估計資料預設依據 **角色** 維度進行樞紐分析。</span><span class="sxs-lookup"><span data-stu-id="19ead-149">By default, the estimate data is pivoted on the **Role** dimension.</span></span>

> ![專案估計值的分時期檢視表](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a><span data-ttu-id="19ead-151">根據工作模式配置估計投入量</span><span class="sxs-lookup"><span data-stu-id="19ead-151">Allocating estimated effort based on the task mode</span></span>

<span data-ttu-id="19ead-152">在分時期檢視表中，您可以藉由配置每單位時段 (以所選時幅表示) 的投入時數，分佈工作估計的總投入量。</span><span class="sxs-lookup"><span data-stu-id="19ead-152">In the time-phased view, you distribute the total effort that is estimated for the task by allocating effort hours per unit time period in the selected time scale.</span></span> <span data-ttu-id="19ead-153">工作模式決定投入量在工作期間的配置方式。</span><span class="sxs-lookup"><span data-stu-id="19ead-153">The task mode determines how effort is allocated across the duration of the task.</span></span> <span data-ttu-id="19ead-154">兩種配置方式分別是 **平均** 和 **根據工作時數** 。</span><span class="sxs-lookup"><span data-stu-id="19ead-154">The two kinds of allocation are **Even** and **Work hours–based**.</span></span>

### <a name="work-hours-based-allocation"></a><span data-ttu-id="19ead-155">根據工作時數配置</span><span class="sxs-lookup"><span data-stu-id="19ead-155">Work hours-based allocation</span></span>
 
<span data-ttu-id="19ead-156">在自動排程工作模式下，工作資源的每日預設工作時數是以完整工時費率來設定。</span><span class="sxs-lookup"><span data-stu-id="19ead-156">In auto-scheduling task mode, the daily default hours for task resources are set at the full work hour rate.</span></span> <span data-ttu-id="19ead-157">當投入量分透過在分時期檢視表中將其割到整個工作期間的方式進行配置時，適用此行為。</span><span class="sxs-lookup"><span data-stu-id="19ead-157">This behavior applies when effort is allocated by splitting it across the duration of the task in the time-phased view.</span></span> <span data-ttu-id="19ead-158">例如，如果您估計工作會由一個以 **天** 時幅計量的資源來完成，則每天配置的投入量不會超過專案行事曆中定義的每天工作時數。</span><span class="sxs-lookup"><span data-stu-id="19ead-158">For example, if you estimate that a task will be completed by one resource in the **Day** time scale, the effort that is allocated per day won't exceed the work hours per day that are defined in the project calendar.</span></span> <span data-ttu-id="19ead-159">因此，投入量配置永遠確保資源是估計要整天使用。</span><span class="sxs-lookup"><span data-stu-id="19ead-159">Therefore, the effort allocation always makes sure that the resources are estimated to be used for the full day.</span></span>

### <a name="even-allocation"></a><span data-ttu-id="19ead-160">平均配置</span><span class="sxs-lookup"><span data-stu-id="19ead-160">Even allocation</span></span>

<span data-ttu-id="19ead-161">在手動排程工作模式下，不會使用專案行事曆中的工作時數。</span><span class="sxs-lookup"><span data-stu-id="19ead-161">In manually scheduled task mode, the work hours from the project calendar aren't used.</span></span> <span data-ttu-id="19ead-162">而是工作排程根據使用者輸入來使用。</span><span class="sxs-lookup"><span data-stu-id="19ead-162">Instead, the task schedule is based on user input.</span></span> <span data-ttu-id="19ead-163">對於這些工作，以所選時幅計量的每單位時段投入量配置沒有任何限制因素。</span><span class="sxs-lookup"><span data-stu-id="19ead-163">For these tasks, the effort allocation per unit time period in the selected time scale doesn't have any limiting factor.</span></span> <span data-ttu-id="19ead-164">工作的總投入量會均等分割，並配置給以所選時幅計量的每單位時段。</span><span class="sxs-lookup"><span data-stu-id="19ead-164">The total effort on the task is equally split and allocated for each unit time period in the selected time scale.</span></span> <span data-ttu-id="19ead-165">因此，工作上定義的工作模式會決定分時期估計值中，每單位時段的投入量分佈 (或投入量配置)。</span><span class="sxs-lookup"><span data-stu-id="19ead-165">Therefore, the task mode that is defined on the task determines the effort distribution, or the allocation of effort per unit time period in time-phased estimates.</span></span>

## <a name="grouping-and-time-phasing-options"></a><span data-ttu-id="19ead-166">分組和分時期選項</span><span class="sxs-lookup"><span data-stu-id="19ead-166">Grouping and time-phasing options</span></span>

<span data-ttu-id="19ead-167">分時期檢視表會顯示每天、每週、每月或每年的投入量、成本和銷售估計值的分佈。</span><span class="sxs-lookup"><span data-stu-id="19ead-167">The time-phased view shows the distribution of the effort, cost, and sales estimates on a daily, weekly, monthly, or yearly basis.</span></span> <span data-ttu-id="19ead-168">估計資料預設依據 **角色** 維度進行樞紐分析。</span><span class="sxs-lookup"><span data-stu-id="19ead-168">By default, the estimate data is pivoted on the **Role** dimension.</span></span> <span data-ttu-id="19ead-169">不過，您可以使用 **分組依據** 選項，在另外兩個維度上進行 樞紐分析： **類別** 和 **資源** 。</span><span class="sxs-lookup"><span data-stu-id="19ead-169">However, you can use the **Group By** option to pivot on two other dimensions: **Category** and **Resource**.</span></span>

<span data-ttu-id="19ead-170">在網格和分時期檢視表中，您可以選擇顯示哪些欄位。</span><span class="sxs-lookup"><span data-stu-id="19ead-170">In both the grid view and the time-phased view, you can select which fields are shown.</span></span> <span data-ttu-id="19ead-171">每個時間塊的總計都會顯示在專案下方。</span><span class="sxs-lookup"><span data-stu-id="19ead-171">Totals for each time block are shown at the bottom of the project.</span></span> <span data-ttu-id="19ead-172">這些總計會顯示日、週、月或年的總估計投入量、成本和銷售。</span><span class="sxs-lookup"><span data-stu-id="19ead-172">They show the total estimated effort, cost, and sales for the day, week, month, or year.</span></span> <span data-ttu-id="19ead-173">預設成本價和銷售價是有生效日期。</span><span class="sxs-lookup"><span data-stu-id="19ead-173">The default cost price and sales price are date-effective.</span></span> <span data-ttu-id="19ead-174">換句話說，這些價格會根據您所選取的分時期檢視表來針對每個資源變更。</span><span class="sxs-lookup"><span data-stu-id="19ead-174">In other words, they change for each resource, based on the time-phased view that you select.</span></span>

## <a name="expense-estimates"></a><span data-ttu-id="19ead-175">費用估計值</span><span class="sxs-lookup"><span data-stu-id="19ead-175">Expense estimates</span></span>

<span data-ttu-id="19ead-176">網格檢視表中的 **新增費用估計值** 按鈕可讓您記錄任何在專案中發生的費用，但不與人力直接關聯。</span><span class="sxs-lookup"><span data-stu-id="19ead-176">The **Add a New Expense Estimate** button in the grid view lets you record any expenses that are incurred in the project, but that aren't directly related to labor.</span></span> <span data-ttu-id="19ead-177">您可以記錄特定工作或整個專案的費用估計值。</span><span class="sxs-lookup"><span data-stu-id="19ead-177">You can record the expense estimates for a specific task or for the entire project.</span></span> <span data-ttu-id="19ead-178">選取您預期要產生費用時的費用類別和暫定日期。</span><span class="sxs-lookup"><span data-stu-id="19ead-178">Select expense categories and the tentative date when you expect to incur the expense.</span></span> <span data-ttu-id="19ead-179">如果相關聯的成本價目表和銷售價目表有預設的價格 (或針對費用類別定義的加成百分比)，當發生關聯時，這些價格會自動在估計明細上輸入。</span><span class="sxs-lookup"><span data-stu-id="19ead-179">If the associated cost price list and sales price list have default prices (or if markup percentages are defined for expense categories), they are automatically entered on the estimate line when the association occurs.</span></span>
