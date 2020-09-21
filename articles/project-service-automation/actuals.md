---
title: 實際值
description: 本主題提供有關專案實際值的資訊。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749977"
---
# <a name="actuals"></a><span data-ttu-id="045c1-103">實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="045c1-104">實際值是專案中已完成的工作量。</span><span class="sxs-lookup"><span data-stu-id="045c1-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="045c1-105">專案實際值可以追溯至其原始憑證。</span><span class="sxs-lookup"><span data-stu-id="045c1-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="045c1-106">這些原始憑證包括時間項目、費用項目與帳目分錄以及發票。</span><span class="sxs-lookup"><span data-stu-id="045c1-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![如何將專案實際值追蹤至原始憑證](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="045c1-108">送出時間項目</span><span class="sxs-lookup"><span data-stu-id="045c1-108">Submitting a time entry</span></span>

<span data-ttu-id="045c1-109">在 PSA 中，將對應至時間及材料合約服務內容之專案的時間項目送出時，會建立兩個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="045c1-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="045c1-110">一項明細用於成本，而另一項用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="045c1-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="045c1-111">將對應至固定價格合約服務內容之專案的時間項目送出時，只會建立成本的帳目明細。</span><span class="sxs-lookup"><span data-stu-id="045c1-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="045c1-112">輸入預設價格的邏輯會存在於帳目明細。</span><span class="sxs-lookup"><span data-stu-id="045c1-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="045c1-113">時間項目中的所有欄位值都會複製到帳目明細。</span><span class="sxs-lookup"><span data-stu-id="045c1-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="045c1-114">這些欄位包括交易的日期、專案所對應至的合約服務內容，以及適當價目表中的貨幣結果。</span><span class="sxs-lookup"><span data-stu-id="045c1-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="045c1-115">影響預設價格的欄位 (例如**角色**和**組織單位**) 會產生要在帳目明細上依預設輸入的適當價格。</span><span class="sxs-lookup"><span data-stu-id="045c1-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="045c1-116">如果在時間項目上新增自訂欄位，而且您想要讓欄位值傳播至實際值，請在實際值實體上建立欄位，並使用欄位對應將欄位從時間項目複製到實際值。</span><span class="sxs-lookup"><span data-stu-id="045c1-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="045c1-117">送出費用項目</span><span class="sxs-lookup"><span data-stu-id="045c1-117">Submitting an expense entry</span></span>

<span data-ttu-id="045c1-118">在 PSA 中，將對應至時間及材料合約服務內容之專案的費用項目送出時，會建立兩個帳目明細。</span><span class="sxs-lookup"><span data-stu-id="045c1-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="045c1-119">一項明細用於成本，而另一項用於未開單銷售。</span><span class="sxs-lookup"><span data-stu-id="045c1-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="045c1-120">將對應至固定價格合約服務內容之專案的費用項目送出時，只會建立成本的帳目明細。</span><span class="sxs-lookup"><span data-stu-id="045c1-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="045c1-121">輸入費用預設價格的邏輯是根據您在**費用項目**頁面上選取的費用類別。</span><span class="sxs-lookup"><span data-stu-id="045c1-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="045c1-122">交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。</span><span class="sxs-lookup"><span data-stu-id="045c1-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="045c1-123">不過，就價格本身而言，使用者輸入的金額預設會直接設定在成本和銷售的相關費用帳目明細上。</span><span class="sxs-lookup"><span data-stu-id="045c1-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="045c1-124">在目前的 PSA 版本中，依類別輸入的每單位預設價格無法在費用項目上使用。</span><span class="sxs-lookup"><span data-stu-id="045c1-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="045c1-125">使用帳目來記錄成本</span><span class="sxs-lookup"><span data-stu-id="045c1-125">Using journals to record costs</span></span>

<span data-ttu-id="045c1-126">在 PSA 中，您可以使用帳目來記錄材料、費用、時間、支出或稅務交易分類中的成本或營收。</span><span class="sxs-lookup"><span data-stu-id="045c1-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="045c1-127">帳目有標題、明細和**確認**動作。</span><span class="sxs-lookup"><span data-stu-id="045c1-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="045c1-128">以下是一些您可能會使用帳目的情況：</span><span class="sxs-lookup"><span data-stu-id="045c1-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="045c1-129">您必須在專案上記錄材料實際成本和銷售。</span><span class="sxs-lookup"><span data-stu-id="045c1-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="045c1-130">您必須將交易實際值從其他系統移至 PSA。</span><span class="sxs-lookup"><span data-stu-id="045c1-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="045c1-131">您必須記錄其他系統中發生的成本 (例如採購或轉承包成本)。</span><span class="sxs-lookup"><span data-stu-id="045c1-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="045c1-132">根據專案事件記錄實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-132">Recording actuals based on project events</span></span>

<span data-ttu-id="045c1-133">PSA 會記錄專案期間發生的財務交易。</span><span class="sxs-lookup"><span data-stu-id="045c1-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="045c1-134">這些交易記錄會以**實際值**來記錄。</span><span class="sxs-lookup"><span data-stu-id="045c1-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="045c1-135">下表顯示根據專案是時間及材料專案還是固定價格專案、是否在售前階段，或是否為內部專案，所建立的不同類型實際值。</span><span class="sxs-lookup"><span data-stu-id="045c1-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="045c1-136">**資源隸屬於與專案承包單位相同的組織單位**</span><span class="sxs-lookup"><span data-stu-id="045c1-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="045c1-137">Event</span><span class="sxs-lookup"><span data-stu-id="045c1-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="045c1-138">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="045c1-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="045c1-139">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="045c1-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="045c1-140">內部專案</span><span class="sxs-lookup"><span data-stu-id="045c1-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="045c1-141">時間及材料</span><span class="sxs-lookup"><span data-stu-id="045c1-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="045c1-142">固定價格</span><span class="sxs-lookup"><span data-stu-id="045c1-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="045c1-143">實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-143">Actuals</span></span></th>
<th><span data-ttu-id="045c1-144">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-144">Transaction currency</span></span></th>
<th><span data-ttu-id="045c1-145">固定價格</span><span class="sxs-lookup"><span data-stu-id="045c1-145">Fixed price</span></span></th>
<th><span data-ttu-id="045c1-146">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="045c1-147">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="045c1-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="045c1-148">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="045c1-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-149">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="045c1-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="045c1-150">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="045c1-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="045c1-151">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="045c1-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="045c1-152">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-152">Cost actual</span></span></td>
<td><span data-ttu-id="045c1-153">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-154">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-155">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="045c1-156">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-157">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-158">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="045c1-159">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="045c1-160">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="045c1-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="045c1-161">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-161">Cost actual</span></span></td>
<td><span data-ttu-id="045c1-162">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-163">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-164">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-165">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-166">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-167">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="045c1-168">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-169">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="045c1-170">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="045c1-171">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="045c1-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="045c1-172">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="045c1-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="045c1-173">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-174">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="045c1-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-175">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-176">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-177">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-178">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="045c1-178">Billed sales</span></span></td>
<td><span data-ttu-id="045c1-179">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="045c1-180">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="045c1-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="045c1-181">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="045c1-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="045c1-182">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-183">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-184">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-185">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-186">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-187">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="045c1-188">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-189">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="045c1-190">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="045c1-191">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="045c1-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="045c1-192">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="045c1-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="045c1-193">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="045c1-194">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="045c1-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="045c1-195">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="045c1-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="045c1-196">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="045c1-197">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="045c1-198">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-199">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="045c1-199">Billed sales</span></span></td>
<td><span data-ttu-id="045c1-200">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="045c1-201">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="045c1-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="045c1-202">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="045c1-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="045c1-203">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-204">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="045c1-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="045c1-205">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-206">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="045c1-207">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="045c1-208">**資源隸屬於與專案承包單位不同的組織單位**</span><span class="sxs-lookup"><span data-stu-id="045c1-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="045c1-209">Event</span><span class="sxs-lookup"><span data-stu-id="045c1-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="045c1-210">計費或已售出專案</span><span class="sxs-lookup"><span data-stu-id="045c1-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="045c1-211">在售前階段的專案</span><span class="sxs-lookup"><span data-stu-id="045c1-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="045c1-212">內部專案</span><span class="sxs-lookup"><span data-stu-id="045c1-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="045c1-213">時間及材料</span><span class="sxs-lookup"><span data-stu-id="045c1-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="045c1-214">固定價格</span><span class="sxs-lookup"><span data-stu-id="045c1-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="045c1-215">實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-215">Actuals</span></span></th>
<th><span data-ttu-id="045c1-216">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-216">Transaction currency</span></span></th>
<th><span data-ttu-id="045c1-217">固定價格</span><span class="sxs-lookup"><span data-stu-id="045c1-217">Fixed price</span></span></th>
<th><span data-ttu-id="045c1-218">交易貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="045c1-219">時間項目已建立。</span><span class="sxs-lookup"><span data-stu-id="045c1-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="045c1-220">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="045c1-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-221">時間項目已送出。</span><span class="sxs-lookup"><span data-stu-id="045c1-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="045c1-222">實際值實體中沒有活動</span><span class="sxs-lookup"><span data-stu-id="045c1-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="045c1-223">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="045c1-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="045c1-224">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-224">Cost actual</span></span></td>
<td><span data-ttu-id="045c1-225">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="045c1-226">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="045c1-227">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="045c1-228">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="045c1-229">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-230">未開單銷售實際值 – 應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="045c1-231">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-232">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="045c1-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="045c1-233">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-234">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="045c1-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="045c1-235">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="045c1-236">時間已核准，且核准期間發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="045c1-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="045c1-237">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-237">Cost actual</span></span></td>
<td><span data-ttu-id="045c1-238">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="045c1-239">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="045c1-240">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="045c1-241">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="045c1-242">成本實際值</span><span class="sxs-lookup"><span data-stu-id="045c1-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-243">資源分配單位成本</span><span class="sxs-lookup"><span data-stu-id="045c1-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="045c1-244">資源分配單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-245">跨組織銷售</span><span class="sxs-lookup"><span data-stu-id="045c1-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="045c1-246">承包單位貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-247">未開單銷售實際值 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="045c1-248">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-249">未開單銷售實際值 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="045c1-250">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="045c1-251">發票已確認，且發生的計費時數沒有任何變更或增加。</span><span class="sxs-lookup"><span data-stu-id="045c1-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="045c1-252">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="045c1-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="045c1-253">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-254">里程碑已開單銷售</span><span class="sxs-lookup"><span data-stu-id="045c1-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-255">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-256">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="045c1-257">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-258">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="045c1-258">Billed sales</span></span></td>
<td><span data-ttu-id="045c1-259">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="045c1-260">發票已確認，且發生的計費時數有減少。</span><span class="sxs-lookup"><span data-stu-id="045c1-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="045c1-261">未開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="045c1-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="045c1-262">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-263">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-264">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-265">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="045c1-266">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-267">已開單銷售 – 新數量應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="045c1-268">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-269">已開單銷售 – 差異不應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="045c1-270">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="045c1-271">已更正發票以增加應收費數量。</span><span class="sxs-lookup"><span data-stu-id="045c1-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="045c1-272">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="045c1-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="045c1-273">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="045c1-274">里程碑已開單銷售沖回</span><span class="sxs-lookup"><span data-stu-id="045c1-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="045c1-275">里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</span><span class="sxs-lookup"><span data-stu-id="045c1-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="045c1-276">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="045c1-277">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="045c1-278">不適用</span><span class="sxs-lookup"><span data-stu-id="045c1-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-279">已開單銷售</span><span class="sxs-lookup"><span data-stu-id="045c1-279">Billed sales</span></span></td>
<td><span data-ttu-id="045c1-280">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="045c1-281">已更正發票以減少應收費數量。</span><span class="sxs-lookup"><span data-stu-id="045c1-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="045c1-282">已開單銷售 – 沖回</span><span class="sxs-lookup"><span data-stu-id="045c1-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="045c1-283">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-284">新數量已開單銷售</span><span class="sxs-lookup"><span data-stu-id="045c1-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="045c1-285">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="045c1-286">未開單銷售 – 差異應收費</span><span class="sxs-lookup"><span data-stu-id="045c1-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="045c1-287">專案合約貨幣</span><span class="sxs-lookup"><span data-stu-id="045c1-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
