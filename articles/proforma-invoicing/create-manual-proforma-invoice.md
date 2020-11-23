---
title: 建立手動預估發票
description: 本主題提供有關建立預估發票的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d3c84664f1b0701db17f0c05654e0c99bb6c640
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128047"
---
# <a name="create-a-manual-proforma-invoice"></a><span data-ttu-id="97944-103">建立手動預估發票</span><span class="sxs-lookup"><span data-stu-id="97944-103">Create a manual proforma invoice</span></span>

<span data-ttu-id="97944-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="97944-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="97944-105">開立發票可讓專案經理在為客戶建立發票前有另一層級的核准。</span><span class="sxs-lookup"><span data-stu-id="97944-105">Invoicing gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="97944-106">第一層核准是在專案團隊成員送出的時間和費用項目經過核准時完成。</span><span class="sxs-lookup"><span data-stu-id="97944-106">The first level of approval is completed when the time and expense entries that project team members submit are approved.</span></span>

<span data-ttu-id="97944-107">Dynamics 365 Project Operations 不是為了產生客戶面向發票而設計，原因如下：</span><span class="sxs-lookup"><span data-stu-id="97944-107">Dynamics 365 Project Operations isn't designed to generate customer-facing invoices, for the following reasons:</span></span>

- <span data-ttu-id="97944-108">其中未包含稅務資訊。</span><span class="sxs-lookup"><span data-stu-id="97944-108">It doesn't contain tax information.</span></span>
- <span data-ttu-id="97944-109">無法使用正確設定的匯率，將其他貨幣轉換為發票貨幣。</span><span class="sxs-lookup"><span data-stu-id="97944-109">It can't convert other currencies to the invoicing currency by using correctly configured exchange rates.</span></span>
- <span data-ttu-id="97944-110">無法正確格式化發票，以供列印。</span><span class="sxs-lookup"><span data-stu-id="97944-110">It can't correctly format invoices so that they can be printed.</span></span>

<span data-ttu-id="97944-111">但您可以改用財務或會計系統來建立使用發票提案所產生之資訊的客戶面向發票。</span><span class="sxs-lookup"><span data-stu-id="97944-111">Instead, you can use a financial or accounting system to create customer-facing invoices that use the information from generated invoice proposals.</span></span>

## <a name="creating-project-invoices"></a><span data-ttu-id="97944-112">建立專案發票</span><span class="sxs-lookup"><span data-stu-id="97944-112">Creating project invoices</span></span>

<span data-ttu-id="97944-113">您可以一次建立一份專案發票，或是大量建立。</span><span class="sxs-lookup"><span data-stu-id="97944-113">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="97944-114">您可以手動建立專案發票，也可以進行設定以便在自動執行中產生。</span><span class="sxs-lookup"><span data-stu-id="97944-114">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices"></a><span data-ttu-id="97944-115">手動建立專案發票</span><span class="sxs-lookup"><span data-stu-id="97944-115">Manually create project invoices</span></span> 

<span data-ttu-id="97944-116">從 **專案合約** 清單頁面，您可以分別為每個專案合約建立專案發票，或者可以為多個專案合約大量建立發票。</span><span class="sxs-lookup"><span data-stu-id="97944-116">From the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

<span data-ttu-id="97944-117">依照此步驟，建立特定專案合約的發票。</span><span class="sxs-lookup"><span data-stu-id="97944-117">Follow this step to create an invoice for a specific project contract.</span></span>

- <span data-ttu-id="97944-118">在 **專案合約** 清單頁面上，開啟專案合約，然後選取 **建立發票**。</span><span class="sxs-lookup"><span data-stu-id="97944-118">On the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

    <span data-ttu-id="97944-119">發票會針對狀態為 **已準備好開立發票** 的所選專案合約的所有交易來產生。</span><span class="sxs-lookup"><span data-stu-id="97944-119">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="97944-120">這些交易包括時間、費用、里程碑和產品型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="97944-120">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

<span data-ttu-id="97944-121">請依照下列步驟大量建立發票。</span><span class="sxs-lookup"><span data-stu-id="97944-121">Follow these steps to create invoices in bulk.</span></span>

1. <span data-ttu-id="97944-122">在 **專案合約** 清單頁面上，選取一個或多個您必須為其建立發票的專案合約，然後選取 **建立專案發票**。</span><span class="sxs-lookup"><span data-stu-id="97944-122">On the **Project Contracts** list page, select one or more project contracts that you must create an invoice for, and then select **Create Project Invoices**.</span></span>

    <span data-ttu-id="97944-123">出現一則警告訊息通知您，建立發票之前可能會有一段延遲。</span><span class="sxs-lookup"><span data-stu-id="97944-123">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="97944-124">也會顯示程序。</span><span class="sxs-lookup"><span data-stu-id="97944-124">The process is also shown.</span></span>

2. <span data-ttu-id="97944-125">選取 **確定** 以關閉訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="97944-125">Select **OK** to close the message box.</span></span>

    <span data-ttu-id="97944-126">發票會針對狀態為 **已準備好開立發票** 的合約服務內容的所有交易來產生。</span><span class="sxs-lookup"><span data-stu-id="97944-126">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="97944-127">這些交易包括時間、費用、里程碑和產品型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="97944-127">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

3. <span data-ttu-id="97944-128">若要檢視已產生的發票，請移至 **銷售**\>**帳務**\>**發票**。</span><span class="sxs-lookup"><span data-stu-id="97944-128">To view the invoices that are generated, go to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="97944-129">您會看到每個專案合約的一份發票。</span><span class="sxs-lookup"><span data-stu-id="97944-129">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices"></a><span data-ttu-id="97944-130">設定自動建立專案發票</span><span class="sxs-lookup"><span data-stu-id="97944-130">Set up automated creation of project invoices</span></span> 

<span data-ttu-id="97944-131">依照下列步驟設定自動化發票執行。</span><span class="sxs-lookup"><span data-stu-id="97944-131">Follow these steps to configure an automated invoice run.</span></span>

1. <span data-ttu-id="97944-132">移至 **設定** \> **批次工作**。</span><span class="sxs-lookup"><span data-stu-id="97944-132">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="97944-133">建立批次工作，並將其命名為 **Project Operations 建立發票**。</span><span class="sxs-lookup"><span data-stu-id="97944-133">Create a batch job, and name it **Project Operations Create Invoices**.</span></span> <span data-ttu-id="97944-134">批次工作的名稱必須包含「建立發票」一詞。</span><span class="sxs-lookup"><span data-stu-id="97944-134">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="97944-135">在 **工作類型** 欄位中，選取 **無**。</span><span class="sxs-lookup"><span data-stu-id="97944-135">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="97944-136">**每日頻率** 和 **使用中** 選項預設會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="97944-136">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="97944-137">選取 **執行工作流程**。</span><span class="sxs-lookup"><span data-stu-id="97944-137">Select **Run Workflow**.</span></span> <span data-ttu-id="97944-138">在 **查詢記錄** 對話方塊中，您會看到三個工作流程：</span><span class="sxs-lookup"><span data-stu-id="97944-138">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="97944-139">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="97944-139">ProcessRunCaller</span></span>
    - <span data-ttu-id="97944-140">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="97944-140">ProcessRunner</span></span>
    - <span data-ttu-id="97944-141">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="97944-141">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="97944-142">選取 **ProcessRunCaller**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="97944-142">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="97944-143">在下一個對話方塊中選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="97944-143">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="97944-144">**睡眠** 工作流程後面會跟著 **程序** 工作流程。</span><span class="sxs-lookup"><span data-stu-id="97944-144">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="97944-145">您也可以選取步驟 5 中的 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="97944-145">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="97944-146">然後，當您選取 **確定** 時，**程序** 工作流程後面會接著 **睡眠** 工作流程。</span><span class="sxs-lookup"><span data-stu-id="97944-146">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="97944-147">**ProcessRunCaller** 和 **ProcessRunner** 工作流程會建立發票。</span><span class="sxs-lookup"><span data-stu-id="97944-147">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="97944-148">**ProcessRunCaller** 會呼叫 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="97944-148">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="97944-149">**ProcessRunner** 是實際建立發票的工作流程。</span><span class="sxs-lookup"><span data-stu-id="97944-149">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="97944-150">它會處理所有需要建立發票的合約服務內容，然後為這些服務內容建立發票。</span><span class="sxs-lookup"><span data-stu-id="97944-150">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="97944-151">為了確定必須建立其發票的合約服務內容，工作會查看合約服務內容的發票執行日期。</span><span class="sxs-lookup"><span data-stu-id="97944-151">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="97944-152">如果屬於一個合約的合約服務內容具有相同的發票執行日期，則會將交易合併成一個有兩個發票明細的發票。</span><span class="sxs-lookup"><span data-stu-id="97944-152">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="97944-153">如果沒有要要建立其發票的交易，則工作會跳過發票建立作業。</span><span class="sxs-lookup"><span data-stu-id="97944-153">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="97944-154">**ProcessRunner** 執行完畢後，會呼叫 **ProcessRunCaller**、提供結束時間，然後關閉。</span><span class="sxs-lookup"><span data-stu-id="97944-154">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="97944-155">**ProcessRunCaller** 接著啟動計時器，從指定的結束時間開始執行 24 小時。</span><span class="sxs-lookup"><span data-stu-id="97944-155">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="97944-156">計時器結束時，會關閉 **ProcessRunCaller**。</span><span class="sxs-lookup"><span data-stu-id="97944-156">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="97944-157">用於建立發票的批次處理工作是週期性工作。</span><span class="sxs-lookup"><span data-stu-id="97944-157">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="97944-158">如果此批次處理已執行多次，就會建立工作的多個執行個體，並造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="97944-158">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="97944-159">因此，您只能啟動批次處理一次，並且只有在其停止執行時才要重新啟動此工作。</span><span class="sxs-lookup"><span data-stu-id="97944-159">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="97944-160">批次開立發票只會對發票排程所設定的專案合約服務內容來執行。</span><span class="sxs-lookup"><span data-stu-id="97944-160">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="97944-161">使用固定價格計費方式的合約服務內容必須已設定里程碑。</span><span class="sxs-lookup"><span data-stu-id="97944-161">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="97944-162">使用時間和材料計費方式的專案合約服務內容必須設定以日期為依據的發票排程。</span><span class="sxs-lookup"><span data-stu-id="97944-162">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="97944-163">這同樣適用於專案型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="97944-163">The same applies to a project-based contract line.</span></span>      
 
### <a name="edit-a-draft-invoice"></a><span data-ttu-id="97944-164">編輯草稿發票</span><span class="sxs-lookup"><span data-stu-id="97944-164">Edit a draft invoice</span></span>

<span data-ttu-id="97944-165">建立草稿專案發票時，所有在時間及費用項目獲核准時建立的未開單銷售交易都會提取到發票上。</span><span class="sxs-lookup"><span data-stu-id="97944-165">When you create a draft project invoice, all unbilled sales transactions that were created when the time and expense entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="97944-166">發票仍處於草稿階段時，您可以進行下列調整：</span><span class="sxs-lookup"><span data-stu-id="97944-166">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="97944-167">刪除或編輯發票明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="97944-167">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="97944-168">編輯和調整數量與帳單類型。</span><span class="sxs-lookup"><span data-stu-id="97944-168">Edit and adjust the quantity and billing type.</span></span>
- <span data-ttu-id="97944-169">直接將時間、費用和服務費新增為發票上的交易。</span><span class="sxs-lookup"><span data-stu-id="97944-169">Directly add time, expense, and fees as transactions on the invoice.</span></span> <span data-ttu-id="97944-170">如果發票明細對應至允許這些交易分類的合約服務內容，您可以使用此功能。</span><span class="sxs-lookup"><span data-stu-id="97944-170">You can use this feature if the invoice line is mapped to a contract line that allows for these transaction classes.</span></span>

<span data-ttu-id="97944-171">選取 **確認** 以確認發票。</span><span class="sxs-lookup"><span data-stu-id="97944-171">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="97944-172">確認動作是單向動作。</span><span class="sxs-lookup"><span data-stu-id="97944-172">The Confirm action is a one-way action.</span></span> <span data-ttu-id="97944-173">選取 **確認** 時，系統會設定發票為唯讀，並從每個發票明細的每個發票明細詳細資料建立已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="97944-173">When you select **Confirm**, the system makes the invoice read-only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="97944-174">如果發票明細詳細資料參照未開單銷售，則系統還會沖回未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="97944-174">If the invoice line detail references an unbilled sales actual, the system also reverses the unbilled sales actual.</span></span> <span data-ttu-id="97944-175">(任何從時間或費用項目建立的發票明細詳細資料都會參照未開單銷售實際值)。總帳整合系統可以使用此沖回來反轉專案進行中工作 (WIP) 以作會計用途。</span><span class="sxs-lookup"><span data-stu-id="97944-175">(Any invoice line detail that was created from a time or expense entry will reference an unbilled sales actual.) General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-invoice"></a><span data-ttu-id="97944-176">更正已確認的發票</span><span class="sxs-lookup"><span data-stu-id="97944-176">Correct a confirmed invoice</span></span>

<span data-ttu-id="97944-177">您可以編輯 (更正) 已確認的發票。</span><span class="sxs-lookup"><span data-stu-id="97944-177">Confirmed invoices can be edited (corrected).</span></span> <span data-ttu-id="97944-178">更正已確認發票時，會建立新的草稿更正發票。</span><span class="sxs-lookup"><span data-stu-id="97944-178">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="97944-179">因為假設您要從原始發票中沖回所有交易和數量，此更正發票會包含原始發票中的所有交易，而其上所有數量皆為 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="97944-179">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are 0 (zero).</span></span>

<span data-ttu-id="97944-180">如果任何交易都不需要更正，您可以從草稿更正發票移除這些交易。</span><span class="sxs-lookup"><span data-stu-id="97944-180">If any transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="97944-181">如果您想要沖回或回復部分數量，則可以編輯明細詳細資料上的 **數量** 欄位。</span><span class="sxs-lookup"><span data-stu-id="97944-181">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="97944-182">如果開啟發票明細詳細資料，您可以查看原始發票數量。</span><span class="sxs-lookup"><span data-stu-id="97944-182">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="97944-183">然後就可以編輯目前發票數量，使其小於或等於原始發票數量。</span><span class="sxs-lookup"><span data-stu-id="97944-183">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="97944-184">確認更正發票時，會沖回原始已開單銷售實際值，並建立新的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="97944-184">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="97944-185">如果數量已減少，則差額也會導致建立新的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="97944-185">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="97944-186">例如，如果原始已開單銷售是八小時，且更正發票明細詳細資料的數量已減少為六小時，則會沖回原始已開單銷售明細，並建立兩個新的實際值：</span><span class="sxs-lookup"><span data-stu-id="97944-186">For example, if the original billed sale was for eight hours, and the corrective invoice line detail has a reduced quantity of six hours, the original billed sales line is reversed and two new actuals are created:</span></span>

- <span data-ttu-id="97944-187">六小時的已開單銷售實際。</span><span class="sxs-lookup"><span data-stu-id="97944-187">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="97944-188">剩餘兩個小時的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="97944-188">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="97944-189">依據與客戶的協商，此交易可以稍後再開帳單，或標示為不應收費。</span><span class="sxs-lookup"><span data-stu-id="97944-189">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
