---
title: 專案預估發票
description: 本主題提供有關 Project Operations 中專案預估發票的資訊。
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1b839c3e40ddcfe1f07b0330a78c42851140d4bf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004026"
---
# <a name="proforma-project-pnvoices"></a><span data-ttu-id="a6561-103">專案預估發票</span><span class="sxs-lookup"><span data-stu-id="a6561-103">Proforma project pnvoices</span></span>

<span data-ttu-id="a6561-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="a6561-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a6561-105">開立專案預估發票讓專案經理在為客戶建立發票前有另一層級的核准。</span><span class="sxs-lookup"><span data-stu-id="a6561-105">Proforma project invoicing gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="a6561-106">第一層核准是在專案團隊成員送出的時間、費用和材料項目經過核准時完成。</span><span class="sxs-lookup"><span data-stu-id="a6561-106">The first level of approval is completed when time, expense, and material entries that project team members submit are approved.</span></span>

<span data-ttu-id="a6561-107">Dynamics 365 Project Operations 精簡部署不是為了產生客戶面向發票而設計。</span><span class="sxs-lookup"><span data-stu-id="a6561-107">Dynamics 365 Project Operations Lite Deployment isn't designed to generate customer-facing invoices.</span></span> <span data-ttu-id="a6561-108">下列清單顯示無法產生發票的原因：</span><span class="sxs-lookup"><span data-stu-id="a6561-108">The following list shows why invoices cannot be generated:</span></span>

- <span data-ttu-id="a6561-109">未包含稅務資訊。</span><span class="sxs-lookup"><span data-stu-id="a6561-109">Does not contain tax information.</span></span>
- <span data-ttu-id="a6561-110">無法將其他貨幣轉換為發票貨幣。</span><span class="sxs-lookup"><span data-stu-id="a6561-110">Cannot convert other currencies to the invoicing currency.</span></span>
- <span data-ttu-id="a6561-111">無法正確設定列印發票的格式。</span><span class="sxs-lookup"><span data-stu-id="a6561-111">Cannot correctly format invoices for printing.</span></span>

<span data-ttu-id="a6561-112">但您可以改用財務或會計系統來建立客戶面向發票，使用所產生發票提案中的資訊。</span><span class="sxs-lookup"><span data-stu-id="a6561-112">Instead, you can use a financial or accounting system to create customer-facing invoices that use the information in generated invoice proposals.</span></span>

## <a name="creating-project-invoices"></a><span data-ttu-id="a6561-113">建立專案發票</span><span class="sxs-lookup"><span data-stu-id="a6561-113">Creating project invoices</span></span>

<span data-ttu-id="a6561-114">您可以一次建立一份專案發票，或是大量建立。</span><span class="sxs-lookup"><span data-stu-id="a6561-114">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="a6561-115">您可以手動建立專案發票，也可以進行設定以便在自動執行中產生。</span><span class="sxs-lookup"><span data-stu-id="a6561-115">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices"></a><span data-ttu-id="a6561-116">手動建立專案發票</span><span class="sxs-lookup"><span data-stu-id="a6561-116">Manually create project invoices</span></span> 

<span data-ttu-id="a6561-117">在 **專案合約** 清單頁面上，您可以分別為每個專案合約建立專案發票，或者可以為多個專案合約大量建立發票。</span><span class="sxs-lookup"><span data-stu-id="a6561-117">On the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

   - <span data-ttu-id="a6561-118">若要為特定專案合約建立發票，請在 **專案合約** 清單頁面上開啟專案合約，然後選取 **建立發票**。</span><span class="sxs-lookup"><span data-stu-id="a6561-118">To create an invoice for a specific project contract, on the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

   <span data-ttu-id="a6561-119">發票會針對狀態為 **已準備好開立發票** 的所選專案合約的所有交易來產生。</span><span class="sxs-lookup"><span data-stu-id="a6561-119">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="a6561-120">這些交易包含時間、費用、材料、里程碑、產品型合約服務內容，以及其他可能已確認的未開單銷售帳目明細。</span><span class="sxs-lookup"><span data-stu-id="a6561-120">These transactions include time, expenses, materials, milestones, product-based contract lines, and other unbilled sales journal lines that may have been confirmed.</span></span>

<span data-ttu-id="a6561-121">若要大量建立發票：</span><span class="sxs-lookup"><span data-stu-id="a6561-121">To create invoices in bulk:</span></span>

1. <span data-ttu-id="a6561-122">在 **專案合約** 清單頁面上，選取一個或多個要為其建立發票的專案合約，然後選取 **建立專案發票**。</span><span class="sxs-lookup"><span data-stu-id="a6561-122">On the **Project Contracts** list page, select one or more project contracts to create an invoice for, and then select **Create Project Invoices**.</span></span>
2. <span data-ttu-id="a6561-123">出現一則警告訊息通知您，建立發票之前可能會有一段延遲。</span><span class="sxs-lookup"><span data-stu-id="a6561-123">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="a6561-124">也會顯示程序。</span><span class="sxs-lookup"><span data-stu-id="a6561-124">The process is also shown.</span></span> <span data-ttu-id="a6561-125">選取 **確定** 以關閉訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="a6561-125">Select **OK** to close the message box.</span></span>

   <span data-ttu-id="a6561-126">發票會針對狀態為 **已準備好開立發票** 的合約服務內容的所有交易來產生。</span><span class="sxs-lookup"><span data-stu-id="a6561-126">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="a6561-127">這些交易包含時間、費用、材料、里程碑、產品型合約服務內容，以及其他可能已確認的未開單銷售帳目明細。</span><span class="sxs-lookup"><span data-stu-id="a6561-127">These transactions include time, expenses, materials, milestones, product - based contract lines and other unbilled sales journal lines that may have been confirmed.</span></span>

3. <span data-ttu-id="a6561-128">移至 **銷售**\>**帳務**\>**發票**，以檢視所產生的發票。</span><span class="sxs-lookup"><span data-stu-id="a6561-128">View the invoices that are generated by going to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="a6561-129">您會看到每個專案合約的一份發票。</span><span class="sxs-lookup"><span data-stu-id="a6561-129">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices"></a><span data-ttu-id="a6561-130">設定自動建立專案發票</span><span class="sxs-lookup"><span data-stu-id="a6561-130">Set up automated creation of project invoices</span></span> 

<span data-ttu-id="a6561-131">依照下列步驟設定自動化發票執行。</span><span class="sxs-lookup"><span data-stu-id="a6561-131">Follow these steps to configure an automated invoice run.</span></span>

1. <span data-ttu-id="a6561-132">移至 **設定** \> **批次工作**。</span><span class="sxs-lookup"><span data-stu-id="a6561-132">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="a6561-133">建立批次工作，並將其命名為 **Project Operations 建立發票**。</span><span class="sxs-lookup"><span data-stu-id="a6561-133">Create a batch job, and name it **Project Operations Create Invoices**.</span></span> <span data-ttu-id="a6561-134">批次工作的名稱必須包含「建立發票」一詞。</span><span class="sxs-lookup"><span data-stu-id="a6561-134">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="a6561-135">在 **工作類型** 欄位中，選取 **無**。</span><span class="sxs-lookup"><span data-stu-id="a6561-135">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="a6561-136">**每日頻率** 和 **使用中** 選項預設會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="a6561-136">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="a6561-137">選取 **執行工作流程**。</span><span class="sxs-lookup"><span data-stu-id="a6561-137">Select **Run Workflow**.</span></span> <span data-ttu-id="a6561-138">在 **查詢記錄** 對話方塊中，您會看到下列工作流程：</span><span class="sxs-lookup"><span data-stu-id="a6561-138">In the **Look Up Record** dialog box, you will see the following workflows:</span></span>

    - <span data-ttu-id="a6561-139">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="a6561-139">ProcessRunCaller</span></span>
    - <span data-ttu-id="a6561-140">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="a6561-140">ProcessRunner</span></span>
    - <span data-ttu-id="a6561-141">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="a6561-141">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="a6561-142">選取 **ProcessRunCaller**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="a6561-142">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="a6561-143">在下一個對話方塊中選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="a6561-143">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="a6561-144">**睡眠** 工作流程後面會跟著 **程序** 工作流程。</span><span class="sxs-lookup"><span data-stu-id="a6561-144">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="a6561-145">您也可以選取步驟 5 中的 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="a6561-145">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="a6561-146">然後，當您選取 **確定** 時，**程序** 工作流程後面會接著 **睡眠** 工作流程。</span><span class="sxs-lookup"><span data-stu-id="a6561-146">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="a6561-147">**ProcessRunCaller** 和 **ProcessRunner** 工作流程會建立發票。</span><span class="sxs-lookup"><span data-stu-id="a6561-147">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="a6561-148">**ProcessRunCaller** 會呼叫 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="a6561-148">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="a6561-149">**ProcessRunner** 是建立發票的工作流程。</span><span class="sxs-lookup"><span data-stu-id="a6561-149">**ProcessRunner** is the workflow that creates the invoices.</span></span> <span data-ttu-id="a6561-150">此工作流程會處理所有需要建立發票的合約服務內容，然後建立發票。</span><span class="sxs-lookup"><span data-stu-id="a6561-150">This workflow goes through all the contract lines that invoices must be created for, and creates the invoices.</span></span> <span data-ttu-id="a6561-151">為了確定必須建立其發票的合約服務內容，工作流程會查看合約服務內容的發票執行日期。</span><span class="sxs-lookup"><span data-stu-id="a6561-151">To determine the contract lines that invoices must be created for, the workflow looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="a6561-152">如果屬於一個合約的合約服務內容具有相同的發票執行日期，則會將交易合併成一個有兩個發票明細的發票。</span><span class="sxs-lookup"><span data-stu-id="a6561-152">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="a6561-153">如果沒有要為其建立發票的交易，則不會建立任何發票。</span><span class="sxs-lookup"><span data-stu-id="a6561-153">If there are no transactions to create invoices for, no invoices are created.</span></span>

<span data-ttu-id="a6561-154">**ProcessRunner** 執行完畢後，會呼叫 **ProcessRunCaller**、提供結束時間，然後關閉。</span><span class="sxs-lookup"><span data-stu-id="a6561-154">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="a6561-155">**ProcessRunCaller** 接著啟動計時器，從指定的結束時間開始執行 24 小時。</span><span class="sxs-lookup"><span data-stu-id="a6561-155">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="a6561-156">計時器結束時，會關閉 **ProcessRunCaller**。</span><span class="sxs-lookup"><span data-stu-id="a6561-156">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="a6561-157">用於建立發票的批次處理工作是週期性工作。</span><span class="sxs-lookup"><span data-stu-id="a6561-157">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="a6561-158">如果此批次處理已執行多次，就會建立工作的多個執行個體，並且可能造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="a6561-158">If this batch process is run many times, multiple instances of the job are created and can cause errors.</span></span> <span data-ttu-id="a6561-159">若要解決此問題，您只能啟動批次處理一次，並且只有在其停止執行時才要加以重新啟動。</span><span class="sxs-lookup"><span data-stu-id="a6561-159">To work around this issue, start the batch process only one time, and only restart it if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="a6561-160">批次開立發票只會對發票排程所設定的專案合約服務內容來執行。</span><span class="sxs-lookup"><span data-stu-id="a6561-160">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="a6561-161">使用固定價格計費方式的合約服務內容必須已設定里程碑。</span><span class="sxs-lookup"><span data-stu-id="a6561-161">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="a6561-162">使用時間和材料計費方式的專案合約服務內容必須設定以日期為依據的發票排程。</span><span class="sxs-lookup"><span data-stu-id="a6561-162">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="a6561-163">這同樣適用於專案型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="a6561-163">The same applies to a project-based contract line.</span></span>      
 
### <a name="edit-a-draft-invoice"></a><span data-ttu-id="a6561-164">編輯草稿發票</span><span class="sxs-lookup"><span data-stu-id="a6561-164">Edit a draft invoice</span></span>

<span data-ttu-id="a6561-165">建立草稿專案發票時，所有在時間及費用項目獲核准時建立的未開單銷售交易都會提取到發票上。</span><span class="sxs-lookup"><span data-stu-id="a6561-165">When you create a draft project invoice, all unbilled sales transactions that were created when the time and expense entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="a6561-166">發票仍處於草稿階段時，您可以進行下列調整：</span><span class="sxs-lookup"><span data-stu-id="a6561-166">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="a6561-167">刪除或編輯發票明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a6561-167">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="a6561-168">編輯和調整數量與帳單類型。</span><span class="sxs-lookup"><span data-stu-id="a6561-168">Edit and adjust the quantity and billing type.</span></span>
- <span data-ttu-id="a6561-169">直接將時間、費用、材料和服務費新增為發票上的交易。</span><span class="sxs-lookup"><span data-stu-id="a6561-169">Directly add time, expense, material, and fees as transactions on the invoice.</span></span> <span data-ttu-id="a6561-170">如果發票明細對應至允許這些交易分類的合約服務內容，您可以使用此功能。</span><span class="sxs-lookup"><span data-stu-id="a6561-170">You can use this feature if the invoice line is mapped to a contract line that allows for these transaction classes.</span></span>

<span data-ttu-id="a6561-171">選取 **確認** 以確認發票。</span><span class="sxs-lookup"><span data-stu-id="a6561-171">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="a6561-172">此動作是單向動作。</span><span class="sxs-lookup"><span data-stu-id="a6561-172">This action is a one-way action.</span></span> <span data-ttu-id="a6561-173">選取 **確認** 時，發票會變成唯讀，並從每個發票明細的每個發票明細詳細資料建立已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a6561-173">When you select **Confirm**, the invoice becomes read only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="a6561-174">如果發票明細詳細資料參考了未開單銷售，則會沖回未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a6561-174">If the invoice line detail references an unbilled sales actual, the unbilled sales actual is reversed.</span></span> <span data-ttu-id="a6561-175">任何從時間、費用或材料使用項目建立的發票明細詳細資料，都會參考未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a6561-175">Any invoice line detail that was created from a time, expense, or material usage entry will reference an unbilled sales actual.</span></span> <span data-ttu-id="a6561-176">總帳整合系統可使用此沖銷來沖回進行中專案工作 (WIP) 以作會計用途。</span><span class="sxs-lookup"><span data-stu-id="a6561-176">General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-invoice"></a><span data-ttu-id="a6561-177">更正已確認的發票</span><span class="sxs-lookup"><span data-stu-id="a6561-177">Correct a confirmed invoice</span></span>

<span data-ttu-id="a6561-178">您可以編輯已確認的發票。</span><span class="sxs-lookup"><span data-stu-id="a6561-178">Confirmed invoices can be edited.</span></span> <span data-ttu-id="a6561-179">更正已確認發票時，會建立新的草稿更正發票。</span><span class="sxs-lookup"><span data-stu-id="a6561-179">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="a6561-180">因為假設您要從原始發票中沖回所有交易和數量，此更正發票會包含原始發票中的所有交易，而其上所有數量皆為零。</span><span class="sxs-lookup"><span data-stu-id="a6561-180">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are zero.</span></span>

<span data-ttu-id="a6561-181">如果有不需要更正的交易，您可以從草稿更正發票移除這些交易。</span><span class="sxs-lookup"><span data-stu-id="a6561-181">If there are transactions that don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="a6561-182">如果您想要沖回或回復部分數量，則可以編輯明細詳細資料上的 **數量** 欄位。</span><span class="sxs-lookup"><span data-stu-id="a6561-182">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="a6561-183">如果開啟發票明細詳細資料，您可以查看原始發票數量。</span><span class="sxs-lookup"><span data-stu-id="a6561-183">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="a6561-184">然後就可以編輯目前發票數量，使其小於或等於原始發票數量。</span><span class="sxs-lookup"><span data-stu-id="a6561-184">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="a6561-185">確認更正發票時，會沖回原始已開單銷售實際值，並建立新的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a6561-185">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="a6561-186">如果數量已扣減，則差額會導致建立新的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a6561-186">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created.</span></span> <span data-ttu-id="a6561-187">例如，如果原始已開單銷售是八小時，且更正發票明細詳細資料的數量已減少為六小時，則會沖回原始已開單銷售明細，並建立兩個新的實際值：</span><span class="sxs-lookup"><span data-stu-id="a6561-187">For example, if the original billed sale was for eight hours and the corrective invoice line detail has a reduced quantity of six hours, the original billed sales line is reversed and two new actuals are created:</span></span>

- <span data-ttu-id="a6561-188">六小時的已開單銷售實際。</span><span class="sxs-lookup"><span data-stu-id="a6561-188">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="a6561-189">剩餘兩個小時的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a6561-189">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="a6561-190">視與客戶的協商而定，此交易可以稍後再開帳單，或標示為不應收費。</span><span class="sxs-lookup"><span data-stu-id="a6561-190">This transaction can be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
