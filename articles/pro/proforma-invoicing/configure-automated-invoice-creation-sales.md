---
title: 設定自動發票建立作業 - 精簡
description: 本主題提供有關設定預估發票自動建立作業的資訊。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ce9cb9090c44762f370bf8d574d179077b6a821
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176556"
---
# <a name="configure-automatic-invoice-creation---lite"></a><span data-ttu-id="d0f0d-103">設定自動發票建立作業 - 精簡</span><span class="sxs-lookup"><span data-stu-id="d0f0d-103">Configure automatic invoice creation - lite</span></span>
 
<span data-ttu-id="d0f0d-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="d0f0d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d0f0d-105">您可以在 Dynamics 365 Project Operations 中設定自動建立發票。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-105">You can configure automatic invoice creation in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="d0f0d-106">系統會根據每個專案合約和合約服務內容的發票排程，建立草稿預估發票。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-106">The system creates a draft proforma invoice based on the invoice schedule for each project contract and contract line.</span></span> <span data-ttu-id="d0f0d-107">發票排程是在合約服務內容層級進行設定。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-107">Invoice schedules are configured at the contract line level.</span></span> <span data-ttu-id="d0f0d-108">合約的每個服務內容都可以有不同的發票排程，或者相同的發票排程可以包含在合約的所有服務內容。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-108">Each line on a contract can have a distinct invoice schedule, or the same invoice schedule can be included on every line of the contract.</span></span>

<span data-ttu-id="d0f0d-109">建立發票時，系統一律每個專案合約至少建立一個發票。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-109">When you create an invoice, the system always creates at least one invoice per project contract.</span></span> <span data-ttu-id="d0f0d-110">在某些情況下，可能會建立多個發票。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-110">In some cases, there may be multiple invoices created.</span></span>

<span data-ttu-id="d0f0d-111">例如，如果合約有多個客戶，則會建立與在該專案合約上有計費交易要開發票之客戶同樣數目的發票。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-111">For example, if the contract has multiple customers, the same number of invoices will be created as the number of customers that have billable transactions to invoice on that project contract.</span></span>

## <a name="understand-how-transactions-are-included-on-an-invoice"></a><span data-ttu-id="d0f0d-112">了解如何將交易包含在發票上</span><span class="sxs-lookup"><span data-stu-id="d0f0d-112">Understand how transactions are included on an invoice</span></span> 

<span data-ttu-id="d0f0d-113">每個專案型合約服務內容有時都會指定各自的發票排程。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-113">Sometimes, each project-based contract line specifies a separate invoice schedule.</span></span> <span data-ttu-id="d0f0d-114">例如，Adatum 合約的實作服務有下列合約服務內容：</span><span class="sxs-lookup"><span data-stu-id="d0f0d-114">For example, implementation services for the Adatum contract have the following contract lines:</span></span>

- <span data-ttu-id="d0f0d-115">包含兩個手動建立里程碑的固定價格原型工作。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-115">Prototype work that is a fixed price with two manually created milestones.</span></span>
- <span data-ttu-id="d0f0d-116">包含時間且每兩週在星期一收費的實作工作。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-116">Implementation work that includes Time and will be billed bi-weekly on Mondays.</span></span>
- <span data-ttu-id="d0f0d-117">已發生的需要在每月第一個星期一收取月費的費用。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-117">Expenses incurred that need to be billed monthly on the first Monday of each month.</span></span>

<span data-ttu-id="d0f0d-118">這兩個明細項目上各自定義的發票排程看起來如下表所示：</span><span class="sxs-lookup"><span data-stu-id="d0f0d-118">Invoice schedules defined on each of these two line items look like the following table:</span></span>

| <span data-ttu-id="d0f0d-119">合約服務內容</span><span class="sxs-lookup"><span data-stu-id="d0f0d-119">Contract line</span></span> | <span data-ttu-id="d0f0d-120">發票執行日期</span><span class="sxs-lookup"><span data-stu-id="d0f0d-120">Invoice run date</span></span> | <span data-ttu-id="d0f0d-121">交易截止日期</span><span class="sxs-lookup"><span data-stu-id="d0f0d-121">Transaction cut-off date</span></span> | <span data-ttu-id="d0f0d-122">里程碑日期</span><span class="sxs-lookup"><span data-stu-id="d0f0d-122">Milestone date</span></span> | <span data-ttu-id="d0f0d-123">里程碑金額</span><span class="sxs-lookup"><span data-stu-id="d0f0d-123">Milestone amount</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="d0f0d-124">原型工作</span><span class="sxs-lookup"><span data-stu-id="d0f0d-124">Prototype work</span></span> | <span data-ttu-id="d0f0d-125">10 月 5 日星期一</span><span class="sxs-lookup"><span data-stu-id="d0f0d-125">October 5, Monday</span></span> | - | <span data-ttu-id="d0f0d-126">10 月 5 日星期一</span><span class="sxs-lookup"><span data-stu-id="d0f0d-126">October 5, Monday</span></span> | <span data-ttu-id="d0f0d-127">5000 USD</span><span class="sxs-lookup"><span data-stu-id="d0f0d-127">5000 USD</span></span> |
| - | <span data-ttu-id="d0f0d-128">11 月 3 日星期二</span><span class="sxs-lookup"><span data-stu-id="d0f0d-128">November 3, Tuesday</span></span> | - | <span data-ttu-id="d0f0d-129">11 月 3 日星期二</span><span class="sxs-lookup"><span data-stu-id="d0f0d-129">November 3, Tuesday</span></span> | <span data-ttu-id="d0f0d-130">12,000 USD</span><span class="sxs-lookup"><span data-stu-id="d0f0d-130">12,000 USD</span></span> |
| <span data-ttu-id="d0f0d-131">實作工作</span><span class="sxs-lookup"><span data-stu-id="d0f0d-131">Implementation work</span></span> | <span data-ttu-id="d0f0d-132">10 月 5 日星期一</span><span class="sxs-lookup"><span data-stu-id="d0f0d-132">October 5, Monday</span></span> | <span data-ttu-id="d0f0d-133">10 月 4 日星期日</span><span class="sxs-lookup"><span data-stu-id="d0f0d-133">October 4, Sunday</span></span> | - | - |
| - | <span data-ttu-id="d0f0d-134">10 月 19 日星期一</span><span class="sxs-lookup"><span data-stu-id="d0f0d-134">October 19, Monday</span></span> | <span data-ttu-id="d0f0d-135">10 月 18 日星期日</span><span class="sxs-lookup"><span data-stu-id="d0f0d-135">October 18, Sunday</span></span> | - | - |
| - | <span data-ttu-id="d0f0d-136">11 月 2 日星期一</span><span class="sxs-lookup"><span data-stu-id="d0f0d-136">November 2, Monday</span></span> | <span data-ttu-id="d0f0d-137">11 月 1 日星期日</span><span class="sxs-lookup"><span data-stu-id="d0f0d-137">November 1, Sunday</span></span> | - | - |
| - | <span data-ttu-id="d0f0d-138">11 月 16 日星期一</span><span class="sxs-lookup"><span data-stu-id="d0f0d-138">November 16, Monday</span></span> | <span data-ttu-id="d0f0d-139">11 月 15 日星期日</span><span class="sxs-lookup"><span data-stu-id="d0f0d-139">November 15, Sunday</span></span> | - | - |
| <span data-ttu-id="d0f0d-140">發生的費用</span><span class="sxs-lookup"><span data-stu-id="d0f0d-140">Expenses incurred</span></span> | <span data-ttu-id="d0f0d-141">10 月 5 日星期一</span><span class="sxs-lookup"><span data-stu-id="d0f0d-141">October 5, Monday</span></span> | <span data-ttu-id="d0f0d-142">10 月 4 日星期日</span><span class="sxs-lookup"><span data-stu-id="d0f0d-142">October 4, Sunday</span></span> | - | - |
| - | <span data-ttu-id="d0f0d-143">11 月 2 日星期一</span><span class="sxs-lookup"><span data-stu-id="d0f0d-143">November 2, Monday</span></span> | <span data-ttu-id="d0f0d-144">11 月 1 日星期日</span><span class="sxs-lookup"><span data-stu-id="d0f0d-144">November 1, Sunday</span></span> | - | - |

<span data-ttu-id="d0f0d-145">在此範例中，自動發票開立功能執行時間：</span><span class="sxs-lookup"><span data-stu-id="d0f0d-145">In this example when the automatic invoicing runs on:</span></span>

- <span data-ttu-id="d0f0d-146">**10 月 4 日或任何之前的日期**：不產生此合約的發票，因為這其中每一個合約服務內容的 **發票排程** 表並未報出發票執行日期為 10 月 4 日星期日。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-146">**October 4 or any date before**: No invoice is generated for this contract because the **Invoice Schedule** table for each of these contract lines doesn't call out October 4, Sunday as an invoice run date.</span></span>
- <span data-ttu-id="d0f0d-147">**10 月 5 日星期一**：已產生下列項目的發票：</span><span class="sxs-lookup"><span data-stu-id="d0f0d-147">**October 5 Monday**: One invoice is generated for:</span></span>

    - <span data-ttu-id="d0f0d-148">原型工作，包含里程碑 (如果已標示為 **已準備好開立發票**)。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-148">Prototype work that includes the milestone, if it is marked as **Ready to Invoice**.</span></span>
    - <span data-ttu-id="d0f0d-149">實作工作，包含所有在交易截止日期 10 月 4 日星期日之前建立的時間交易 (已標示為 **已準備好開立發票**)。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-149">Implementation work that includes all Time transactions created before the transaction cut-off date of October 4, Sunday, that is marked as **Ready to Invoice**.</span></span>
    - <span data-ttu-id="d0f0d-150">發生的費用，包含所有在交易截止日期 10 月 4 日星期日之前建立的費用交易 (已標示為 **已準備好開立發票**)。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-150">Expense incurred that includes all Expense transactions created before the transaction cut-off date of October 4, Sunday, that is marked as **Ready to Invoice**.</span></span>
  
- <span data-ttu-id="d0f0d-151">**10 月 6 日或任何在 10 月 19 日之前的日期**：不產生此合約的發票，因為這其中每一個合約服務內容的 **發票排程** 表並未報出發票執行日期為 10 月 6 日或任何在 10 月 19 日之前的日期。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-151">**On October 6 or any date before October 19**: No invoice is generated for this contract since the **Invoice Schedule** table for each of these contract lines does not call out October 6 or any date before October 19 as an invoice run date.</span></span>
- <span data-ttu-id="d0f0d-152">**10 月 19 日星期一**：已為實作工作產生一個發票，此實作工作包含所有在交易截止日期 10 月 18 日星期日之前建立的時間交易 (已標示為 **已準備好開立發票**)。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-152">**October 19, Monday**: One invoice is generated for implementation work that includes all Time transactions created before the transaction cut-off date of October 18, Sunday, that is marked as **Ready to Invoice**.</span></span>
- <span data-ttu-id="d0f0d-153">**11 月 2 日星期一**：已產生下列項目的發票：</span><span class="sxs-lookup"><span data-stu-id="d0f0d-153">**November 2 Monday**: One invoice is generated for:</span></span>

    - <span data-ttu-id="d0f0d-154">實作工作，包含所有在交易截止日期 11 月 1 日星期日之前建立的時間交易 (已標示為 **已準備好開立發票**)。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-154">Implementation work that includes all Time transactions created before the transaction cut-off date of November 1, Sunday, that is marked as **Ready to Invoice**.</span></span>
    - <span data-ttu-id="d0f0d-155">發生的費用，包含所有在交易截止日期 11 月 1 日星期日之前建立的費用交易 (已標示為 **已準備好開立發票**)。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-155">Expense incurred that includes all Expense transactions created before the transaction cut-off date of November 1, Sunday, that is marked as **Ready to Invoice**.</span></span>

- <span data-ttu-id="d0f0d-156">**11 月 3 日星期二**：已為包含 12000 美元里程碑的原型工作產生一個發票 (如果已標示為 **已準備好開立發票**)。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-156">**November 3, Tuesday**: One invoice is generated for prototype work that includes the milestone for 12000 USD, if it is marked as **Ready to Invoice**.</span></span>

## <a name="configure-automatic-invoicing"></a><span data-ttu-id="d0f0d-157">設定自動發票開立</span><span class="sxs-lookup"><span data-stu-id="d0f0d-157">Configure automatic invoicing</span></span>

<span data-ttu-id="d0f0d-158">完成下列步驟以設定自動化發票執行。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-158">Complete the following steps to configure an automated invoice run.</span></span>

1. <span data-ttu-id="d0f0d-159">在 **Project Operations** 中，移至 **設定** > **週期性發票設定**。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-159">In **Project Operations**, go to **Settings** > **Recurring Invoice Setup**.</span></span>
2. <span data-ttu-id="d0f0d-160">建立批次工作，並將其命名為 **Project Operations 建立發票**。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-160">Create a batch job, and name it **rPoject Operations Create Invoices**.</span></span> <span data-ttu-id="d0f0d-161">批次工作的名稱必須包含「建立發票」一詞。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-161">The name of the batch job must include the words, "create invoices".</span></span>
3. <span data-ttu-id="d0f0d-162">在 **工作類型** 欄位中，選取 **無**。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-162">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="d0f0d-163">**每日頻率** 和 **使用中** 欄位預設會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-163">By default, the **Frequency Daily** and **Is Active** fields are set to **Yes**.</span></span>
4. <span data-ttu-id="d0f0d-164">選取 **執行工作流程**。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-164">Select **Run Workflow**.</span></span> <span data-ttu-id="d0f0d-165">在 **查詢記錄** 對話方塊中，您會看到三個工作流程：</span><span class="sxs-lookup"><span data-stu-id="d0f0d-165">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

- <span data-ttu-id="d0f0d-166">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="d0f0d-166">ProcessRunCaller</span></span>
- <span data-ttu-id="d0f0d-167">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="d0f0d-167">ProcessRunner</span></span>
- <span data-ttu-id="d0f0d-168">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="d0f0d-168">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="d0f0d-169">選取 **ProcessRunCaller**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-169">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="d0f0d-170">在下一個對話方塊中選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-170">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="d0f0d-171">**睡眠** 工作流程後面會跟著 **程序** 工作流程。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-171">A **Sleep** workflow is followed by a **Process** workflow.</span></span> 

> [!NOTE]
> <span data-ttu-id="d0f0d-172">您也可以選取步驟 5 中的 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-172">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="d0f0d-173">然後，當您選取 **確定** 時，**程序** 工作流程後面會接著 **睡眠** 工作流程。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-173">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="d0f0d-174">**ProcessRunCaller** 和 **ProcessRunner** 工作流程會建立發票。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-174">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="d0f0d-175">**ProcessRunCaller** 會呼叫 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-175">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="d0f0d-176">**ProcessRunner** 是實際建立發票的工作流程。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-176">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="d0f0d-177">工作流程會處理所有需要建立發票的合約服務內容，然後為這些服務內容建立發票。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-177">The workflow goes through all the contract lines that invoices must be created for, and creates invoices for those lines.</span></span> <span data-ttu-id="d0f0d-178">為了確定必須建立其發票的合約服務內容，工作會查看合約服務內容的發票執行日期。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-178">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="d0f0d-179">如果屬於一個合約的合約服務內容具有相同的發票執行日期，則會將交易合併成一個有兩個發票明細的發票。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-179">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="d0f0d-180">如果沒有要要建立其發票的交易，則工作會略過建立發票。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-180">If there are no transactions to create invoices for, the job skips creating an invoice.</span></span>

<span data-ttu-id="d0f0d-181">**ProcessRunner** 執行完畢後，會呼叫 **ProcessRunCaller**、提供結束時間，然後關閉。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-181">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="d0f0d-182">**ProcessRunCaller** 接著啟動計時器，從指定的結束時間開始執行 24 小時。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-182">**ProcessRunCaller** then starts a timer that runs for 24-hours from the specified end time.</span></span> <span data-ttu-id="d0f0d-183">計時器結束時，會關閉 **ProcessRunCaller**。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-183">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="d0f0d-184">用於建立發票的批次處理工作是週期性工作。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-184">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="d0f0d-185">如果此批次處理已執行多次，就會建立工作的多個執行個體，並導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-185">If this batch process is run many times, multiple instances of the job are created and causes errors.</span></span> <span data-ttu-id="d0f0d-186">因此，您只能啟動批次處理一次，然後只在其停止執行時才重新啟動此工作。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-186">Therefore, you should start the batch process only one time, and then restart only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="d0f0d-187">在 Project Operations 中批次開立發票，只會對發票排程所設定的專案合約服務內容來執行。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-187">Batch invoicing in Project Operations only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="d0f0d-188">使用固定價格計費方式的合約服務內容必須已設定里程碑。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-188">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="d0f0d-189">使用時間和材料計費方式的專案合約服務內容必須設定以日期為依據的發票排程。</span><span class="sxs-lookup"><span data-stu-id="d0f0d-189">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span>
