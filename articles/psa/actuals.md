---
title: 實際值概觀
description: 本主題提供有關專案實際值的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146113"
---
# <a name="actuals-overview"></a><span data-ttu-id="43b2b-103">實際值概觀</span><span class="sxs-lookup"><span data-stu-id="43b2b-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="43b2b-104">實際值是專案中已完成的工作量。</span><span class="sxs-lookup"><span data-stu-id="43b2b-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="43b2b-105">專案實際值可以追溯至其原始憑證。</span><span class="sxs-lookup"><span data-stu-id="43b2b-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="43b2b-106">這些原始憑證包括時間項目、費用項目與帳目分錄以及發票。</span><span class="sxs-lookup"><span data-stu-id="43b2b-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![如何將專案實際值追蹤至原始憑證](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="43b2b-108">送出時間項目</span><span class="sxs-lookup"><span data-stu-id="43b2b-108">Submitting a time entry</span></span>

<span data-ttu-id="43b2b-109">在 PSA 中，將對應至時間及材料合約服務內容之專案的時間項目送出時，會建立兩個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="43b2b-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="43b2b-110">一項明細用於成本，而另一項用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="43b2b-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="43b2b-111">將對應至固定價格合約服務內容之專案的時間項目送出時，只會建立成本的帳目明細。</span><span class="sxs-lookup"><span data-stu-id="43b2b-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="43b2b-112">輸入預設價格的邏輯會存在於帳目明細。</span><span class="sxs-lookup"><span data-stu-id="43b2b-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="43b2b-113">時間項目中的所有欄位值都會複製到帳目明細。</span><span class="sxs-lookup"><span data-stu-id="43b2b-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="43b2b-114">這些欄位包括交易的日期、專案所對應至的合約服務內容，以及適當價目表中的貨幣結果。</span><span class="sxs-lookup"><span data-stu-id="43b2b-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="43b2b-115">影響預設價格的欄位 (例如 **角色** 和 **組織單位**) 會產生要在帳目明細上依預設輸入的適當價格。</span><span class="sxs-lookup"><span data-stu-id="43b2b-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="43b2b-116">如果在時間項目上新增自訂欄位，而且您想要讓欄位值傳播至實際值，請在實際值實體上建立欄位，並使用欄位對應將欄位從時間項目複製到實際值。</span><span class="sxs-lookup"><span data-stu-id="43b2b-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="43b2b-117">送出費用項目</span><span class="sxs-lookup"><span data-stu-id="43b2b-117">Submitting an expense entry</span></span>

<span data-ttu-id="43b2b-118">在 PSA 中，將對應至時間及材料合約服務內容之專案的費用項目送出時，會建立兩個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="43b2b-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="43b2b-119">一項明細用於成本，而另一項用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="43b2b-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="43b2b-120">將對應至固定價格合約服務內容之專案的費用項目送出時，只會建立成本的帳目明細。</span><span class="sxs-lookup"><span data-stu-id="43b2b-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="43b2b-121">輸入費用預設價格的邏輯是根據您在 **費用項目** 頁面上選取的費用類別。</span><span class="sxs-lookup"><span data-stu-id="43b2b-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="43b2b-122">交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。</span><span class="sxs-lookup"><span data-stu-id="43b2b-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="43b2b-123">不過，就價格本身而言，使用者輸入的金額預設會直接設定在成本和銷售的相關費用帳目明細上。</span><span class="sxs-lookup"><span data-stu-id="43b2b-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="43b2b-124">在目前的 PSA 版本中，依類別輸入的每單位預設價格無法在費用項目上使用。</span><span class="sxs-lookup"><span data-stu-id="43b2b-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="43b2b-125">使用分錄帳目來記錄成本</span><span class="sxs-lookup"><span data-stu-id="43b2b-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="43b2b-126">在 PSA 中，您可以使用分錄帳目來記錄材料、費用、時間、支出或稅務交易分類中的成本或營收。</span><span class="sxs-lookup"><span data-stu-id="43b2b-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="43b2b-127">帳目有標題、明細和 **確認** 動作。</span><span class="sxs-lookup"><span data-stu-id="43b2b-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="43b2b-128">以下是一些您可能會使用帳目的情況：</span><span class="sxs-lookup"><span data-stu-id="43b2b-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="43b2b-129">您必須在專案上記錄材料實際成本和銷售。</span><span class="sxs-lookup"><span data-stu-id="43b2b-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="43b2b-130">您必須將交易實際值從其他系統移至 PSA。</span><span class="sxs-lookup"><span data-stu-id="43b2b-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="43b2b-131">您必須記錄其他系統中發生的成本 (例如採購或轉承包成本)。</span><span class="sxs-lookup"><span data-stu-id="43b2b-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43b2b-132">使用分錄帳目建立實際值的工作，只能由完全了解實際值對專案所產生之會計影響的使用者來完成。</span><span class="sxs-lookup"><span data-stu-id="43b2b-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="43b2b-133">這是因為應用程式不會驗證帳目明細類型，或帳目明細上所輸入的相關價格。</span><span class="sxs-lookup"><span data-stu-id="43b2b-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="43b2b-134">由於會有這種帳目類型的影響，請在授與何人建立分錄帳目的存取權限時，特別小心。</span><span class="sxs-lookup"><span data-stu-id="43b2b-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="43b2b-135">根據專案事件記錄實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-135">Recording actuals based on project events</span></span>

<span data-ttu-id="43b2b-136">PSA 會記錄專案期間發生的財務交易。</span><span class="sxs-lookup"><span data-stu-id="43b2b-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="43b2b-137">這些交易記錄會以 **實際值** 來記錄。</span><span class="sxs-lookup"><span data-stu-id="43b2b-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="43b2b-138">下表顯示根據專案是時間及材料專案還是固定價格專案、是否在售前階段，或是否為內部專案，所建立的不同類型實際值。</span><span class="sxs-lookup"><span data-stu-id="43b2b-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="43b2b-139">**資源隸屬於與專案承包單位相同的組織單位**</span><span class="sxs-lookup"><span data-stu-id="43b2b-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="43b2b-140">Event</span><span class="sxs-lookup"><span data-stu-id="43b2b-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="43b2b-141">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="43b2b-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="43b2b-142">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="43b2b-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="43b2b-143">內部專案</span><span class="sxs-lookup"><span data-stu-id="43b2b-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="43b2b-144">時間及材料</span><span class="sxs-lookup"><span data-stu-id="43b2b-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="43b2b-145">固定價格</span><span class="sxs-lookup"><span data-stu-id="43b2b-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="43b2b-146">實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-146">Actuals</span></span></th>
<th><span data-ttu-id="43b2b-147">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-147">Transaction currency</span></span></th>
<th><span data-ttu-id="43b2b-148">固定價格</span><span class="sxs-lookup"><span data-stu-id="43b2b-148">Fixed price</span></span></th>
<th><span data-ttu-id="43b2b-149">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="43b2b-150">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="43b2b-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="43b2b-151">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="43b2b-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-152">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="43b2b-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="43b2b-153">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="43b2b-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="43b2b-154">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="43b2b-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="43b2b-155">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-155">Cost actual</span></span></td>
<td><span data-ttu-id="43b2b-156">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-157">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-158">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="43b2b-159">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-160">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-161">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="43b2b-162">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="43b2b-163">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="43b2b-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="43b2b-164">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-164">Cost actual</span></span></td>
<td><span data-ttu-id="43b2b-165">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-166">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-167">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-168">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-169">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-170">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="43b2b-171">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-172">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="43b2b-173">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="43b2b-174">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="43b2b-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="43b2b-175">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="43b2b-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="43b2b-176">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-177">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="43b2b-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-178">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-179">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-180">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-181">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="43b2b-181">Billed sales</span></span></td>
<td><span data-ttu-id="43b2b-182">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="43b2b-183">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="43b2b-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="43b2b-184">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="43b2b-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="43b2b-185">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-186">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-187">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-188">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-189">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-190">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="43b2b-191">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-192">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="43b2b-193">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="43b2b-194">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="43b2b-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="43b2b-195">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="43b2b-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="43b2b-196">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="43b2b-197">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="43b2b-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="43b2b-198">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="43b2b-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="43b2b-199">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="43b2b-200">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="43b2b-201">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-202">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="43b2b-202">Billed sales</span></span></td>
<td><span data-ttu-id="43b2b-203">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="43b2b-204">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="43b2b-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="43b2b-205">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="43b2b-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="43b2b-206">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-207">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="43b2b-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="43b2b-208">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-209">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="43b2b-210">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="43b2b-211">**資源隸屬於與專案承包單位不同的組織單位**</span><span class="sxs-lookup"><span data-stu-id="43b2b-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="43b2b-212">Event</span><span class="sxs-lookup"><span data-stu-id="43b2b-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="43b2b-213">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="43b2b-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="43b2b-214">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="43b2b-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="43b2b-215">內部專案</span><span class="sxs-lookup"><span data-stu-id="43b2b-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="43b2b-216">時間及材料</span><span class="sxs-lookup"><span data-stu-id="43b2b-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="43b2b-217">固定價格</span><span class="sxs-lookup"><span data-stu-id="43b2b-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="43b2b-218">實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-218">Actuals</span></span></th>
<th><span data-ttu-id="43b2b-219">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-219">Transaction currency</span></span></th>
<th><span data-ttu-id="43b2b-220">固定價格</span><span class="sxs-lookup"><span data-stu-id="43b2b-220">Fixed price</span></span></th>
<th><span data-ttu-id="43b2b-221">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="43b2b-222">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="43b2b-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="43b2b-223">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="43b2b-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-224">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="43b2b-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="43b2b-225">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="43b2b-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="43b2b-226">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="43b2b-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="43b2b-227">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-227">Cost actual</span></span></td>
<td><span data-ttu-id="43b2b-228">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="43b2b-229">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="43b2b-230">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="43b2b-231">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="43b2b-232">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-233">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="43b2b-234">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-235">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="43b2b-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="43b2b-236">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-237">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="43b2b-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="43b2b-238">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="43b2b-239">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="43b2b-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="43b2b-240">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-240">Cost actual</span></span></td>
<td><span data-ttu-id="43b2b-241">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="43b2b-242">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="43b2b-243">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="43b2b-244">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="43b2b-245">成本實際值</span><span class="sxs-lookup"><span data-stu-id="43b2b-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-246">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="43b2b-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="43b2b-247">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-248">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="43b2b-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="43b2b-249">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-250">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="43b2b-251">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-252">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="43b2b-253">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="43b2b-254">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="43b2b-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="43b2b-255">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="43b2b-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="43b2b-256">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-257">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="43b2b-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-258">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-259">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="43b2b-260">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-261">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="43b2b-261">Billed sales</span></span></td>
<td><span data-ttu-id="43b2b-262">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="43b2b-263">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="43b2b-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="43b2b-264">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="43b2b-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="43b2b-265">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-266">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-267">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-268">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="43b2b-269">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-270">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="43b2b-271">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-272">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="43b2b-273">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="43b2b-274">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="43b2b-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="43b2b-275">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="43b2b-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="43b2b-276">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="43b2b-277">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="43b2b-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="43b2b-278">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="43b2b-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="43b2b-279">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="43b2b-280">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="43b2b-281">不適用</span><span class="sxs-lookup"><span data-stu-id="43b2b-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-282">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="43b2b-282">Billed sales</span></span></td>
<td><span data-ttu-id="43b2b-283">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="43b2b-284">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="43b2b-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="43b2b-285">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="43b2b-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="43b2b-286">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-287">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="43b2b-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="43b2b-288">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43b2b-289">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="43b2b-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="43b2b-290">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="43b2b-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
