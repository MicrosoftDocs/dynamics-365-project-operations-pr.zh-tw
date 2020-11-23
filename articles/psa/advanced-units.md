---
title: 單位群組和單位
description: 本主題提供有關單位群組和單位的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 58ce821d11d729f6e2c33e5a50344458e395db4d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130568"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="c008a-103">單位群組和單位</span><span class="sxs-lookup"><span data-stu-id="c008a-103">Unit groups and units</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c008a-104">單位群組和單位是 Microsoft Dynamics 365 中的基本實體。</span><span class="sxs-lookup"><span data-stu-id="c008a-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="c008a-105">單位是量值的單一單位，您可以將多個單位分組成單位群組。</span><span class="sxs-lookup"><span data-stu-id="c008a-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="c008a-106">單位群組有時會稱為 Dynamics 365 使用者介面 (UI) 中的單位排程。</span><span class="sxs-lookup"><span data-stu-id="c008a-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="c008a-107">以下是一些單位與單位群組的範例：</span><span class="sxs-lookup"><span data-stu-id="c008a-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="c008a-108">**單位群組**：距離</span><span class="sxs-lookup"><span data-stu-id="c008a-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="c008a-109">**單位**：英里、公里及其他。</span><span class="sxs-lookup"><span data-stu-id="c008a-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="c008a-110">**單位群組**：時間</span><span class="sxs-lookup"><span data-stu-id="c008a-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="c008a-111">**單位**：小時、天、週及其他。</span><span class="sxs-lookup"><span data-stu-id="c008a-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="c008a-112">在單位群組中設定多個單位時，您也必須設定這些單位之間的轉換因數，方法是將您設定的第一個單位指定為單位群組預設或主要單位。</span><span class="sxs-lookup"><span data-stu-id="c008a-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="c008a-113">例如，在 **時間** 單位群組中，如果您將 **小時** 設定為第一個單位，系統就會將 **小時** 指定為預設單位。</span><span class="sxs-lookup"><span data-stu-id="c008a-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="c008a-114">如果您設定的下一個單位是 **天**，此必須將 **天** 的轉換因數設定為 **小時**。</span><span class="sxs-lookup"><span data-stu-id="c008a-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="c008a-115">如果接著將 **週** 新增為第三個單位，則必須根據 **天** 或 **小時** 設定 **週** 的轉換因數。</span><span class="sxs-lookup"><span data-stu-id="c008a-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="c008a-116">下圖顯示 **天** 單位 (其中 **數量** 欄位顯示一天的小時數) 和 **週** 單位 (其中 **數量** 欄位顯示一週的天數) 的範例設定。</span><span class="sxs-lookup"><span data-stu-id="c008a-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![單位群組：資訊頁面](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="c008a-118">使用單位與單位群組</span><span class="sxs-lookup"><span data-stu-id="c008a-118">Using units and unit groups</span></span>

<span data-ttu-id="c008a-119">Dynamics 365 Project Service Automation 使用單位與單位群組來處理費用及時間的估計和分錄。</span><span class="sxs-lookup"><span data-stu-id="c008a-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="c008a-120">如果是費用，每個費用類別都有預設單位群組和單位。</span><span class="sxs-lookup"><span data-stu-id="c008a-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="c008a-121">這些值會輸入為費用類別價目表項目的預設值。</span><span class="sxs-lookup"><span data-stu-id="c008a-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="c008a-122">例如，您有一個名為 **里程** 的費用類別。</span><span class="sxs-lookup"><span data-stu-id="c008a-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="c008a-123">其單位群組命名為 **距離**，而預設單位則命名為 **英里**。</span><span class="sxs-lookup"><span data-stu-id="c008a-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="c008a-124">如果您設定 **距離** 單位群組，使之有兩個單位 (**英里** 和 **公里**) 時，您可以在一個價目表中為 **里程** 類別設定兩個價格：每英里價格和每公里價格。</span><span class="sxs-lookup"><span data-stu-id="c008a-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="c008a-125">費用類別</span><span class="sxs-lookup"><span data-stu-id="c008a-125">Expense category</span></span>  | <span data-ttu-id="c008a-126">單位群組</span><span class="sxs-lookup"><span data-stu-id="c008a-126">Unit group</span></span>  | <span data-ttu-id="c008a-127">單位</span><span class="sxs-lookup"><span data-stu-id="c008a-127">Unit</span></span>      | <span data-ttu-id="c008a-128">定價方式</span><span class="sxs-lookup"><span data-stu-id="c008a-128">Pricing method</span></span>  | <span data-ttu-id="c008a-129">單價</span><span class="sxs-lookup"><span data-stu-id="c008a-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="c008a-130">里程</span><span class="sxs-lookup"><span data-stu-id="c008a-130">Mileage</span></span>           | <span data-ttu-id="c008a-131">距離</span><span class="sxs-lookup"><span data-stu-id="c008a-131">Distance</span></span>      | <span data-ttu-id="c008a-132">英里</span><span class="sxs-lookup"><span data-stu-id="c008a-132">Mile</span></span>      | <span data-ttu-id="c008a-133">單價</span><span class="sxs-lookup"><span data-stu-id="c008a-133">Price per unit</span></span>    | <span data-ttu-id="c008a-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="c008a-134">10 USD</span></span>            |
| <span data-ttu-id="c008a-135">里程</span><span class="sxs-lookup"><span data-stu-id="c008a-135">Mileage</span></span>           | <span data-ttu-id="c008a-136">距離</span><span class="sxs-lookup"><span data-stu-id="c008a-136">Distance</span></span>      | <span data-ttu-id="c008a-137">公里</span><span class="sxs-lookup"><span data-stu-id="c008a-137">Kilometer</span></span> | <span data-ttu-id="c008a-138">單價</span><span class="sxs-lookup"><span data-stu-id="c008a-138">Price per unit</span></span>    |  <span data-ttu-id="c008a-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="c008a-139">6 USD</span></span>            |

<span data-ttu-id="c008a-140">在專案中輸入費用時，系統會透過費用的類別與單位組合來決定價格。</span><span class="sxs-lookup"><span data-stu-id="c008a-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="c008a-141">費用描述</span><span class="sxs-lookup"><span data-stu-id="c008a-141">Expense description</span></span>        | <span data-ttu-id="c008a-142">費用類別</span><span class="sxs-lookup"><span data-stu-id="c008a-142">Expense category</span></span>  | <span data-ttu-id="c008a-143">單位</span><span class="sxs-lookup"><span data-stu-id="c008a-143">Unit</span></span>  | <span data-ttu-id="c008a-144">數量</span><span class="sxs-lookup"><span data-stu-id="c008a-144">Quantity</span></span>  | <span data-ttu-id="c008a-145">單價</span><span class="sxs-lookup"><span data-stu-id="c008a-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="c008a-146">行駛至客戶地點</span><span class="sxs-lookup"><span data-stu-id="c008a-146">Drive to client location</span></span> | <span data-ttu-id="c008a-147">里程</span><span class="sxs-lookup"><span data-stu-id="c008a-147">Mileage</span></span>             | <span data-ttu-id="c008a-148">英里</span><span class="sxs-lookup"><span data-stu-id="c008a-148">Mile</span></span>  | <span data-ttu-id="c008a-149">10</span><span class="sxs-lookup"><span data-stu-id="c008a-149">10</span></span>        | <span data-ttu-id="c008a-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="c008a-150">10 USD</span></span>         |

<span data-ttu-id="c008a-151">至於時間，每個價目表標題都有 **預設時間單位** 欄位。</span><span class="sxs-lookup"><span data-stu-id="c008a-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="c008a-152">此值在您建立價目表標頭時已設定。</span><span class="sxs-lookup"><span data-stu-id="c008a-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="c008a-153">這個單位會接著用來設定該價目表上所有的角色型價格。</span><span class="sxs-lookup"><span data-stu-id="c008a-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="c008a-154">**時間報價** 欄位的估計明細可以用任何時間單位來表示。</span><span class="sxs-lookup"><span data-stu-id="c008a-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="c008a-155">不過，專案估計明細和專案時間項目只能使用 **小時** 時間單位。</span><span class="sxs-lookup"><span data-stu-id="c008a-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="c008a-156">如果時間項目和估計明細的單位與該角色價目表明細的單位不相符，則系統會將價格轉換為專案估計或專案實際交易中定義的單位。</span><span class="sxs-lookup"><span data-stu-id="c008a-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="c008a-157">下列範例顯示 PSA 如何使用單位群組、單位及轉換因數。</span><span class="sxs-lookup"><span data-stu-id="c008a-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="c008a-158">Units</span><span class="sxs-lookup"><span data-stu-id="c008a-158">Units</span></span>

   - <span data-ttu-id="c008a-159">**單位群組**：時間</span><span class="sxs-lookup"><span data-stu-id="c008a-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="c008a-160">**單位**：小時</span><span class="sxs-lookup"><span data-stu-id="c008a-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="c008a-161">**天** - 轉算因數：8 小時</span><span class="sxs-lookup"><span data-stu-id="c008a-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="c008a-162">**週** - 轉算因數：40 小時</span><span class="sxs-lookup"><span data-stu-id="c008a-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="c008a-163">專案 A 上的價目表設定：</span><span class="sxs-lookup"><span data-stu-id="c008a-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="c008a-164">**名稱**：2016 年英國銷售價格</span><span class="sxs-lookup"><span data-stu-id="c008a-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="c008a-165">**預設時間單位**：天</span><span class="sxs-lookup"><span data-stu-id="c008a-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="c008a-166">**貨幣**：GBP</span><span class="sxs-lookup"><span data-stu-id="c008a-166">**Currency**: GBP</span></span>

| <span data-ttu-id="c008a-167">角色</span><span class="sxs-lookup"><span data-stu-id="c008a-167">Role</span></span>      | <span data-ttu-id="c008a-168">單位群組</span><span class="sxs-lookup"><span data-stu-id="c008a-168">Unit group</span></span> | <span data-ttu-id="c008a-169">單位</span><span class="sxs-lookup"><span data-stu-id="c008a-169">Unit</span></span> | <span data-ttu-id="c008a-170">組織單位</span><span class="sxs-lookup"><span data-stu-id="c008a-170">Organizational unit</span></span> | <span data-ttu-id="c008a-171">價格</span><span class="sxs-lookup"><span data-stu-id="c008a-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="c008a-172">開發人員</span><span class="sxs-lookup"><span data-stu-id="c008a-172">Developer</span></span> | <span data-ttu-id="c008a-173">Time</span><span class="sxs-lookup"><span data-stu-id="c008a-173">Time</span></span>       | <span data-ttu-id="c008a-174">Day</span><span class="sxs-lookup"><span data-stu-id="c008a-174">Day</span></span>  | <span data-ttu-id="c008a-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="c008a-175">Contoso UK</span></span>          | <span data-ttu-id="c008a-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="c008a-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="c008a-177">時間項目</span><span class="sxs-lookup"><span data-stu-id="c008a-177">Time entry</span></span>

<span data-ttu-id="c008a-178">下表顯示所產生由 PSA 為一個三小時專案建立的銷售端交易。</span><span class="sxs-lookup"><span data-stu-id="c008a-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="c008a-179">計畫</span><span class="sxs-lookup"><span data-stu-id="c008a-179">Project</span></span>   | <span data-ttu-id="c008a-180">工作</span><span class="sxs-lookup"><span data-stu-id="c008a-180">Task</span></span>    | <span data-ttu-id="c008a-181">角色</span><span class="sxs-lookup"><span data-stu-id="c008a-181">Role</span></span>      | <span data-ttu-id="c008a-182">數量</span><span class="sxs-lookup"><span data-stu-id="c008a-182">Quantity</span></span> | <span data-ttu-id="c008a-183">單位</span><span class="sxs-lookup"><span data-stu-id="c008a-183">Unit</span></span>  | <span data-ttu-id="c008a-184">單價</span><span class="sxs-lookup"><span data-stu-id="c008a-184">Unit price</span></span> | <span data-ttu-id="c008a-185">未開單銷售金額</span><span class="sxs-lookup"><span data-stu-id="c008a-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="c008a-186">專案 A</span><span class="sxs-lookup"><span data-stu-id="c008a-186">Project A</span></span> | <span data-ttu-id="c008a-187">設計</span><span class="sxs-lookup"><span data-stu-id="c008a-187">Design</span></span>  | <span data-ttu-id="c008a-188">開發人員</span><span class="sxs-lookup"><span data-stu-id="c008a-188">Developer</span></span> | <span data-ttu-id="c008a-189">3</span><span class="sxs-lookup"><span data-stu-id="c008a-189">3</span></span>        | <span data-ttu-id="c008a-190">Hour</span><span class="sxs-lookup"><span data-stu-id="c008a-190">Hour</span></span>  | <span data-ttu-id="c008a-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="c008a-191">100 GBP</span></span>    | <span data-ttu-id="c008a-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="c008a-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="c008a-193">時間單位常見問題集</span><span class="sxs-lookup"><span data-stu-id="c008a-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="c008a-194">就費用來說，PSA 是否會轉換成不同的單位？</span><span class="sxs-lookup"><span data-stu-id="c008a-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="c008a-195">編號</span><span class="sxs-lookup"><span data-stu-id="c008a-195">No.</span></span> <span data-ttu-id="c008a-196">單位轉換只適用於時間。</span><span class="sxs-lookup"><span data-stu-id="c008a-196">Unit conversion works only for time.</span></span> <span data-ttu-id="c008a-197">對於費用，如果系統找不到費用類別與單位組合的價格，預設會將價格設定為 0.00。</span><span class="sxs-lookup"><span data-stu-id="c008a-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="c008a-198">PSA 為什麼會轉換時間單位？</span><span class="sxs-lookup"><span data-stu-id="c008a-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="c008a-199">在某些國家/地區，有一項以天為單位來設定帳單費率的法律規定。</span><span class="sxs-lookup"><span data-stu-id="c008a-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="c008a-200">報價週期中的價格交涉和折扣是藉由使用每個計費角色的日費率來完成。</span><span class="sxs-lookup"><span data-stu-id="c008a-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="c008a-201">排程估計和時間項目是以小時為單位完成。</span><span class="sxs-lookup"><span data-stu-id="c008a-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="c008a-202">為了支援時間單位的這種差異，PSA 會轉換時間單位。</span><span class="sxs-lookup"><span data-stu-id="c008a-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="c008a-203">是否可以變更專案估計的時間單位？</span><span class="sxs-lookup"><span data-stu-id="c008a-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="c008a-204">編號</span><span class="sxs-lookup"><span data-stu-id="c008a-204">No.</span></span> <span data-ttu-id="c008a-205">排程估計目前限制為小時，無法加以變更。</span><span class="sxs-lookup"><span data-stu-id="c008a-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="c008a-206">是否可以編輯、刪除和新增單位與單位群組？</span><span class="sxs-lookup"><span data-stu-id="c008a-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="c008a-207">是的。</span><span class="sxs-lookup"><span data-stu-id="c008a-207">Yes.</span></span> <span data-ttu-id="c008a-208">除了 **時間** 單位群組和 **小時** 單位之外，所有單位都可刪除或編輯，而且新單位也可以新增。</span><span class="sxs-lookup"><span data-stu-id="c008a-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="c008a-209">在 PSA 中，無法刪除 **時間** 單位群組和 **小時** 單位。</span><span class="sxs-lookup"><span data-stu-id="c008a-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="c008a-210">不過，您可以使用 **名稱** 欄位的翻譯文字來更新它們。</span><span class="sxs-lookup"><span data-stu-id="c008a-210">However, they can be updated with a translated text for the **Name** field.</span></span>
