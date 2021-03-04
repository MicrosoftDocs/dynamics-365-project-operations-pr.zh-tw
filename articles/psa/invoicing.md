---
title: 在 Project Service Automation 中開立發票
description: 本主題提供有關開立發票的資訊。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0855e85c1f09d29d3ecb49ba517fd3043ae11140
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151378"
---
# <a name="invoicing-in-project-service-automation"></a><span data-ttu-id="fdcb1-103">在 Project Service Automation 中開立發票</span><span class="sxs-lookup"><span data-stu-id="fdcb1-103">Invoicing in Project Service Automation</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fdcb1-104">在 Dynamics 365 Project Service Automation 中開立發票非常有用，因為這可讓專案經理在為客戶建立發票前有另一層級的核准。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-104">Invoicing in Dynamics 365 Project Service Automation is useful because it gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="fdcb1-105">第一層核准是在專案團隊成員送出的時間和費用項目經過核准時完成。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-105">The first level of approval is completed when the time and expense entries that project team members submit are approved.</span></span>

<span data-ttu-id="fdcb1-106">PSA 不是為了產生客戶面向發票而設計，原因如下：</span><span class="sxs-lookup"><span data-stu-id="fdcb1-106">PSA isn't designed to generate customer-facing invoices, for the following reasons:</span></span>

- <span data-ttu-id="fdcb1-107">其中未包含稅務資訊。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-107">It doesn't contain tax information.</span></span>
- <span data-ttu-id="fdcb1-108">無法使用正確設定的匯率，將其他貨幣轉換為發票貨幣。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-108">It can't convert other currencies to the invoicing currency by using correctly configured exchange rates.</span></span>
- <span data-ttu-id="fdcb1-109">無法正確格式化發票，以供列印。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-109">It can't correctly format invoices so that they can be printed.</span></span>

<span data-ttu-id="fdcb1-110">但您可以改用財務或會計系統來建立客戶面向發票，使用 PSA 所產生發票提案中的資訊。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-110">Instead, you can use a financial or accounting system to create customer-facing invoices that use the information from invoice proposals that are generated in PSA.</span></span>

## <a name="creating-project-invoices-in-psa"></a><span data-ttu-id="fdcb1-111">在 PSA 中建立專案發票</span><span class="sxs-lookup"><span data-stu-id="fdcb1-111">Creating project invoices in PSA</span></span>

<span data-ttu-id="fdcb1-112">您可以一次建立一份專案發票，或是大量建立。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-112">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="fdcb1-113">您可以手動建立專案發票，也可以進行設定以便在自動執行中產生。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-113">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices-in-psa"></a><span data-ttu-id="fdcb1-114">在 PSA 中手動建立專案發票</span><span class="sxs-lookup"><span data-stu-id="fdcb1-114">Manually create project invoices in PSA</span></span>

<span data-ttu-id="fdcb1-115">從 **專案合約** 清單頁面，您可以分別為每個專案合約建立專案發票，或者可以為多個專案合約大量建立發票。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-115">From the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

<span data-ttu-id="fdcb1-116">依照此步驟，建立特定專案合約的發票。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-116">Follow this step to create an invoice for a specific project contract.</span></span>

- <span data-ttu-id="fdcb1-117">在 **專案合約** 清單頁面上，開啟專案合約，然後選取 **建立發票**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-117">On the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

    ![建立特定專案合約的專案發票](media/CreateProjectInvoicesOneByOne.png)

    <span data-ttu-id="fdcb1-119">發票會針對狀態為 **已準備好開立發票** 的所選專案合約的所有交易來產生。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-119">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="fdcb1-120">這些交易包括時間、費用、里程碑和產品型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-120">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

<span data-ttu-id="fdcb1-121">請依照下列步驟大量建立發票。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-121">Follow these steps to create invoices in bulk.</span></span>

1. <span data-ttu-id="fdcb1-122">在 **專案合約** 清單頁面上，選取一個或多個您必須為其建立發票的專案合約，然後選取 **建立專案發票**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-122">On the **Project Contracts** list page, select one or more project contracts that you must create an invoice for, and then select **Create Project Invoices**.</span></span>

    ![大量建立專案發票](media/CreateProjectInvoicesBulk.png)

    <span data-ttu-id="fdcb1-124">出現一則警告訊息通知您，建立發票之前可能會有一段延遲。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-124">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="fdcb1-125">也會顯示程序。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-125">The process is also shown.</span></span>

2. <span data-ttu-id="fdcb1-126">選取 **確定** 以關閉訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-126">Select **OK** to close the message box.</span></span>

    <span data-ttu-id="fdcb1-127">發票會針對狀態為 **已準備好開立發票** 的合約服務內容的所有交易來產生。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-127">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="fdcb1-128">這些交易包括時間、費用、里程碑和產品型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-128">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

3. <span data-ttu-id="fdcb1-129">若要檢視已產生的發票，請移至 **銷售**\>**帳務**\>**發票**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-129">To view the invoices that are generated, go to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="fdcb1-130">您會看到每個專案合約的一份發票。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-130">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a><span data-ttu-id="fdcb1-131">在 PSA 中設定自動建立專案發票</span><span class="sxs-lookup"><span data-stu-id="fdcb1-131">Set up automated creation of project invoices in PSA</span></span>

<span data-ttu-id="fdcb1-132">請依照下列步驟，在 PSA 中設定自動化發票執行。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-132">Follow these steps to configure an automated invoice run in PSA.</span></span>

1. <span data-ttu-id="fdcb1-133">移至 **Project Service** \> **設定** \> **批次工作**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-133">Go to **Project Service** \> **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="fdcb1-134">建立批次工作，並將其命名為 **PSA 建立發票**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-134">Create a batch job, and name it **PSA Create Invoices**.</span></span> <span data-ttu-id="fdcb1-135">批次工作的名稱必須包含「建立發票」一詞。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-135">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="fdcb1-136">在 **工作類型** 欄位中，選取 **無**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-136">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="fdcb1-137">**每日頻率** 和 **使用中** 選項預設會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-137">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="fdcb1-138">選取 **執行工作流程**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-138">Select **Run Workflow**.</span></span> <span data-ttu-id="fdcb1-139">在 **查詢記錄** 對話方塊中，您會看到三個工作流程：</span><span class="sxs-lookup"><span data-stu-id="fdcb1-139">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="fdcb1-140">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="fdcb1-140">ProcessRunCaller</span></span>
    - <span data-ttu-id="fdcb1-141">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="fdcb1-141">ProcessRunner</span></span>
    - <span data-ttu-id="fdcb1-142">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="fdcb1-142">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="fdcb1-143">選取 **ProcessRunCaller**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-143">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="fdcb1-144">在下一個對話方塊中選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-144">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="fdcb1-145">**睡眠** 工作流程後面會跟著 **程序** 工作流程。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-145">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="fdcb1-146">您也可以選取步驟 5 中的 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-146">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="fdcb1-147">然後，當您選取 **確定** 時，**程序** 工作流程後面會接著 **睡眠** 工作流程。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-147">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="fdcb1-148">**ProcessRunCaller** 和 **ProcessRunner** 工作流程會建立發票。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-148">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="fdcb1-149">**ProcessRunCaller** 會呼叫 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-149">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="fdcb1-150">**ProcessRunner** 是實際建立發票的工作流程。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-150">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="fdcb1-151">它會處理所有需要建立發票的合約服務內容，然後為這些服務內容建立發票。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-151">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="fdcb1-152">為了確定必須建立其發票的合約服務內容，工作會查看合約服務內容的發票執行日期。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-152">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="fdcb1-153">如果屬於一個合約的合約服務內容具有相同的發票執行日期，則會將交易合併成一個有兩個發票明細的發票。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-153">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="fdcb1-154">如果沒有要要建立其發票的交易，則工作會跳過發票建立作業。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-154">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="fdcb1-155">**ProcessRunner** 執行完畢後，會呼叫 **ProcessRunCaller**、提供結束時間，然後關閉。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-155">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="fdcb1-156">**ProcessRunCaller** 接著啟動計時器，從指定的結束時間開始執行 24 小時。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-156">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="fdcb1-157">計時器結束時，會關閉 **ProcessRunCaller**。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-157">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="fdcb1-158">用於建立發票的批次處理工作是週期性工作。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-158">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="fdcb1-159">如果此批次處理已執行多次，就會建立工作的多個執行個體，並造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-159">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="fdcb1-160">因此，您只能啟動批次處理一次，並且只有在其停止執行時才要重新啟動此工作。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-160">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="fdcb1-161">Project Service Automation 中的批次開立發票只會針對發票排程所設定的專案合約服務內容執行。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-161">Batch invoicing in Project Service Automation only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="fdcb1-162">使用固定價格計費方式的合約服務內容必須已設定里程碑。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-162">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="fdcb1-163">使用時間和材料計費方式的專案合約服務內容必須設定以日期為依據的發票排程。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-163">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="fdcb1-164">[報價和報價明細](basic-quote-lines.md#invoice-schedule)主題中已提供有關在以報價明細為根據之專案的內容中設定開立發票頻率的資訊。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-164">Information about setting up invoicing frequencies in the context of a project that is based on a quote line, is provided in the topic, [Quotes and quote lines](basic-quote-lines.md#invoice-schedule).</span></span> <span data-ttu-id="fdcb1-165">這同樣適用於專案型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-165">The same applies to a project-based contract line.</span></span>      
 
### <a name="edit-a-draft-psa-invoice"></a><span data-ttu-id="fdcb1-166">編輯草稿 PSA 發票</span><span class="sxs-lookup"><span data-stu-id="fdcb1-166">Edit a draft PSA invoice</span></span>

<span data-ttu-id="fdcb1-167">建立草稿專案發票時，所有在時間及費用項目獲核准時建立的未開單銷售交易都會提取到發票上。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-167">When you create a draft project invoice, all unbilled sales transactions that were created when the time and expense entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="fdcb1-168">發票仍處於草稿階段時，您可以進行下列調整：</span><span class="sxs-lookup"><span data-stu-id="fdcb1-168">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="fdcb1-169">刪除或編輯發票明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-169">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="fdcb1-170">編輯和調整數量與帳單類型。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-170">Edit and adjust the quantity and billing type.</span></span>
- <span data-ttu-id="fdcb1-171">直接將時間、費用和服務費新增為發票上的交易。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-171">Directly add time, expense, and fees as transactions on the invoice.</span></span> <span data-ttu-id="fdcb1-172">如果發票明細對應至允許這些交易分類的合約服務內容，您可以使用此功能。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-172">You can use this feature if the invoice line is mapped to a contract line that allows for these transaction classes.</span></span>

<span data-ttu-id="fdcb1-173">選取 **確認** 以確認發票。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-173">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="fdcb1-174">確認動作是單向動作。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-174">The Confirm action is a one-way action.</span></span> <span data-ttu-id="fdcb1-175">選取 **確認** 時，系統會設定發票為唯讀，並從每個發票明細的每個發票明細詳細資料建立已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-175">When you select **Confirm**, the system makes the invoice read-only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="fdcb1-176">如果發票明細詳細資料參照未開單銷售，則系統還會沖回未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-176">If the invoice line detail references an unbilled sales actual, the system also reverses the unbilled sales actual.</span></span> <span data-ttu-id="fdcb1-177">(任何從時間或費用項目建立的發票明細詳細資料都會參照未開單銷售實際值)。總帳整合系統可以使用此沖回來反轉專案進行中工作 (WIP) 以作會計用途。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-177">(Any invoice line detail that was created from a time or expense entry will reference an unbilled sales actual.) General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-psa-invoice"></a><span data-ttu-id="fdcb1-178">更正已確認的 PSA 發票</span><span class="sxs-lookup"><span data-stu-id="fdcb1-178">Correct a confirmed PSA invoice</span></span>

<span data-ttu-id="fdcb1-179">已確認的 PSA 發票可加以編輯 (更正)。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-179">Confirmed PSA invoices can be edited (corrected).</span></span> <span data-ttu-id="fdcb1-180">更正已確認發票時，會建立新的草稿更正發票。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-180">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="fdcb1-181">因為假設您要從原始發票中沖回所有交易和數量，此更正發票會包含原始發票中的所有交易，而其上所有數量皆為 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-181">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are 0 (zero).</span></span>

<span data-ttu-id="fdcb1-182">如果任何交易都不需要更正，您可以從草稿更正發票移除這些交易。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-182">If any transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="fdcb1-183">如果您想要沖回或回復部分數量，則可以編輯明細詳細資料上的 **數量** 欄位。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-183">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="fdcb1-184">如果開啟發票明細詳細資料，您可以查看原始發票數量。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-184">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="fdcb1-185">然後就可以編輯目前發票數量，使其小於或等於原始發票數量。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-185">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="fdcb1-186">確認更正發票時，會沖回原始已開單銷售實際值，並建立新的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-186">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="fdcb1-187">如果數量已減少，則差額也會導致建立新的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-187">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="fdcb1-188">例如，如果原始已開單銷售是八小時，且更正發票明細詳細資料的數量已減少為六小時，則 PSA 會沖回原始已開單銷售明細，並建立兩個新的實際值：</span><span class="sxs-lookup"><span data-stu-id="fdcb1-188">For example, if the original billed sales was for eight hours, and the corrective invoice line detail has a reduced quantity of six hours, PSA reverses the original billed sales line and creates two new actuals:</span></span>

- <span data-ttu-id="fdcb1-189">六小時的已開單銷售實際。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-189">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="fdcb1-190">剩餘兩個小時的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-190">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="fdcb1-191">依據與客戶的協商，此交易可以稍後再開帳單，或標示為不應收費。</span><span class="sxs-lookup"><span data-stu-id="fdcb1-191">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
