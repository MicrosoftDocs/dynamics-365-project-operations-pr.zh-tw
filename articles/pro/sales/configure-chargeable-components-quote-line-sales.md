---
title: 設定報價明細的應收費元件
description: 本主題提供有關設定專案型報價明細中應收費和不應收費元件的資訊。
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858283"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="53668-103">設定報價明細的應收費元件</span><span class="sxs-lookup"><span data-stu-id="53668-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="53668-104">_**適用於：** 精簡部署 - 交易至開立預估發票、資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="53668-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="53668-105">專案型報價明細有 *內含* 元件和 *應收費* 元件的概念。</span><span class="sxs-lookup"><span data-stu-id="53668-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="53668-106">內含元件受限於下列各項：</span><span class="sxs-lookup"><span data-stu-id="53668-106">Included components are subject to:</span></span>

  - <span data-ttu-id="53668-107">帳務方式和客戶分割</span><span class="sxs-lookup"><span data-stu-id="53668-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="53668-108">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="53668-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="53668-109">專案型報價明細上定義的發票週期設定</span><span class="sxs-lookup"><span data-stu-id="53668-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="53668-110">您可以使用 **帳單類型** 欄位將一部分內含元件標示為應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="53668-111">**帳單類型** 欄位是選項組，允許在報價明細的情境下使用下列值：</span><span class="sxs-lookup"><span data-stu-id="53668-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="53668-112">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-112">Chargeable</span></span>
  - <span data-ttu-id="53668-113">不應收費</span><span class="sxs-lookup"><span data-stu-id="53668-113">Non-chargeable</span></span>

<span data-ttu-id="53668-114">您可以在工作、角色和交易類別上定義應收費元件。</span><span class="sxs-lookup"><span data-stu-id="53668-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="53668-115">可收費率是在報價明細的工作上所定義，並套用至該明細所包含的所有交易分類。</span><span class="sxs-lookup"><span data-stu-id="53668-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="53668-116">如果 **包含工作** 欄位已設定為 **整個專案** 或保持空白，則沒有提供 **應收費工作** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="53668-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="53668-117">報價明細的角色上所定義的可收費率只能套用至 **時間** 交易分類。</span><span class="sxs-lookup"><span data-stu-id="53668-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="53668-118">如果 **包含時間** 欄位在專案報價明細上設定為 **否**，則沒有提供 **應收費角色** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="53668-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="53668-119">可收費率是在報價明細的交易類別上所定義，並且只能套用至 **費用** 交易分類。</span><span class="sxs-lookup"><span data-stu-id="53668-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="53668-120">如果 **包含費用** 欄位在專案報價明細上設定為 **否**，則沒有提供 **應收費類別** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="53668-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="53668-121">將專案工作更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="53668-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="53668-122">專案工作在能使下列設定變成可行的特定專案型報價明細內容中可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="53668-123">如果專案型報價明細包含 **時間** 和工作 **T1**，則工作會與報價明細建立應收費關聯。</span><span class="sxs-lookup"><span data-stu-id="53668-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="53668-124">如果有第二個報價明細，其中包含 **費用** 時，您可以將報價明細的 **T1** 工作關聯為不應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="53668-125">結果是，工作中所記錄的所有時間都是應收費的，而工作中所記錄的所有費用都是不應收費的。</span><span class="sxs-lookup"><span data-stu-id="53668-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="53668-126">工作的帳單類型可以在專案型報價明細的 **應收費工作** 索引標籤上，透過更新 **報價明細工作** 子格上的 **帳單類型** 欄位來進行設定。</span><span class="sxs-lookup"><span data-stu-id="53668-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="53668-127">或者，也可以在顯示與工作相關之報價明細的專案工作帳單設定子格的 **帳單類型** 欄位中更新專案工作的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="53668-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="53668-128">將角色更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="53668-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="53668-129">角色在特定專案型報價明細的內容中，可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="53668-130">角色的帳單類型可以在報價明細的 **應收費角色** 索引標籤上，透過更新 **應收費角色** 子格上的 **帳單類型** 欄位來進行設定。</span><span class="sxs-lookup"><span data-stu-id="53668-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="53668-131">將交易類別更新為應收費或不應收費</span><span class="sxs-lookup"><span data-stu-id="53668-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="53668-132">交易類別在特定報價明細上，可以是應收費，也可以是不應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="53668-133">交易的帳單類型可以在報價明細的 **應收費類別** 索引標籤上，透過更新 **應收費類別** 子格上的 **帳單類型** 欄位來進行設定。</span><span class="sxs-lookup"><span data-stu-id="53668-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="53668-134">解析可收費率</span><span class="sxs-lookup"><span data-stu-id="53668-134">Resolve chargeability</span></span>
<span data-ttu-id="53668-135">只有在下列情況下，才能將針對時間建立的估計值或實際值視為應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="53668-136">**時間** 已包含在報價明細中。</span><span class="sxs-lookup"><span data-stu-id="53668-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="53668-137">**角色** 已在報價明細中設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="53668-138">**包含的工作** 已在報價明細上設定為 **選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="53668-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="53668-139">如果這三種情況成立，**工作** 也會設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="53668-140">只有在下列情況下，才能將針對費用建立的估計值或實際值視為應收費：</span><span class="sxs-lookup"><span data-stu-id="53668-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="53668-141">**費用** 已包含在報價明細中。</span><span class="sxs-lookup"><span data-stu-id="53668-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="53668-142">**交易類別** 已在報價明細中設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="53668-143">**包含的工作** 已在報價明細上設定為 **選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="53668-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="53668-144">如果這三種情況成立，**工作** 也會設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="53668-145">只有在下列情況下，才能將針對材料建立的估計值或實際值視為應收費：</span><span class="sxs-lookup"><span data-stu-id="53668-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="53668-146">**材料** 已包含在報價明細中。</span><span class="sxs-lookup"><span data-stu-id="53668-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="53668-147">**包含的工作** 已在報價明細上設定為 **選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="53668-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="53668-148">如果這兩種情況成立，**工作** 也應設定為應收費。</span><span class="sxs-lookup"><span data-stu-id="53668-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="53668-149">
                    <strong>包含時間</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="53668-150">
                    <strong>包含費用</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="53668-151">
                    <strong>包含材料</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="53668-152">
                    <strong>包含的工作</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="53668-153">
                    <strong>角色</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="53668-154">
                    <strong>類別</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="53668-155">
                    <strong>工作​​</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="53668-156">
                    <strong>可收費率影響</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-157">.是</span><span class="sxs-lookup"><span data-stu-id="53668-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="53668-158">.是</span><span class="sxs-lookup"><span data-stu-id="53668-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="53668-159">.是</span><span class="sxs-lookup"><span data-stu-id="53668-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-160">整個專案</span><span class="sxs-lookup"><span data-stu-id="53668-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-161">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-162">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-163">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-164">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="53668-165">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="53668-166">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-167">.是</span><span class="sxs-lookup"><span data-stu-id="53668-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="53668-168">.是</span><span class="sxs-lookup"><span data-stu-id="53668-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="53668-169">.是</span><span class="sxs-lookup"><span data-stu-id="53668-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-170">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="53668-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-171">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-172">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-173">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-174">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="53668-175">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="53668-176">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-177">.是</span><span class="sxs-lookup"><span data-stu-id="53668-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="53668-178">.是</span><span class="sxs-lookup"><span data-stu-id="53668-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="53668-179">.是</span><span class="sxs-lookup"><span data-stu-id="53668-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-180">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="53668-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="53668-181">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-182">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-183">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-184">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-185">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="53668-186">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-187">.是</span><span class="sxs-lookup"><span data-stu-id="53668-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="53668-188">.是</span><span class="sxs-lookup"><span data-stu-id="53668-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="53668-189">.是</span><span class="sxs-lookup"><span data-stu-id="53668-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-190">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="53668-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-191">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-192">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="53668-193">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-194">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-195">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-196">材料實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-197">.是</span><span class="sxs-lookup"><span data-stu-id="53668-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="53668-198">.是</span><span class="sxs-lookup"><span data-stu-id="53668-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="53668-199">.是</span><span class="sxs-lookup"><span data-stu-id="53668-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-200">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="53668-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="53668-201">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-202">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="53668-203">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-204">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-205">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-206">材料實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-207">.是</span><span class="sxs-lookup"><span data-stu-id="53668-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="53668-208">.是</span><span class="sxs-lookup"><span data-stu-id="53668-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="53668-209">.是</span><span class="sxs-lookup"><span data-stu-id="53668-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-210">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="53668-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="53668-211">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="53668-212">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-213">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-214">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-215">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-216">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="53668-217">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="53668-218">.是</span><span class="sxs-lookup"><span data-stu-id="53668-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="53668-219">.是</span><span class="sxs-lookup"><span data-stu-id="53668-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-220">整個專案</span><span class="sxs-lookup"><span data-stu-id="53668-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-221">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="53668-222">
                    <strong>應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-223">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-224">時間實際值的帳單：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-225">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="53668-226">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="53668-227">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="53668-228">.是</span><span class="sxs-lookup"><span data-stu-id="53668-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="53668-229">.是</span><span class="sxs-lookup"><span data-stu-id="53668-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-230">整個專案</span><span class="sxs-lookup"><span data-stu-id="53668-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-231">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="53668-232">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-233">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-234">時間實際值的帳單：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-235">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-236">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-237">.是</span><span class="sxs-lookup"><span data-stu-id="53668-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="53668-238">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="53668-239">.是</span><span class="sxs-lookup"><span data-stu-id="53668-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-240">整個專案</span><span class="sxs-lookup"><span data-stu-id="53668-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-241">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-242">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-243">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-244">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="53668-245">費用實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-246">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-247">.是</span><span class="sxs-lookup"><span data-stu-id="53668-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="53668-248">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="53668-249">.是</span><span class="sxs-lookup"><span data-stu-id="53668-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-250">整個專案</span><span class="sxs-lookup"><span data-stu-id="53668-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="53668-251">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-252">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-253">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-254">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-255">費用實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-256">材料實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-257">.是</span><span class="sxs-lookup"><span data-stu-id="53668-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="53668-258">.是</span><span class="sxs-lookup"><span data-stu-id="53668-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="53668-259">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-260">整個專案</span><span class="sxs-lookup"><span data-stu-id="53668-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-261">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-262">應收費</span><span class="sxs-lookup"><span data-stu-id="53668-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-263">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-264">時間實際值的帳單：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="53668-265">費用實際值的帳單類型：應收費</span><span class="sxs-lookup"><span data-stu-id="53668-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="53668-266">材料實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="53668-267">.是</span><span class="sxs-lookup"><span data-stu-id="53668-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="53668-268">.是</span><span class="sxs-lookup"><span data-stu-id="53668-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="53668-269">
                    <strong>無</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="53668-270">整個專案</span><span class="sxs-lookup"><span data-stu-id="53668-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="53668-271">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="53668-272">
                    <strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="53668-273">無法設定</span><span class="sxs-lookup"><span data-stu-id="53668-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="53668-274">時間實際值的帳單：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-275">費用實際值的帳單類型：<strong>不應收費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="53668-276">材料實際值的帳單類型：<strong>無法使用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="53668-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
