---
title: 在專案型合約服務內容中建立發票排程 - 精簡
description: 本主題提供有關建立發票排程與里程碑的資訊。
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 548858f6d2257343a632657ca386da03f1f330a9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003216"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a><span data-ttu-id="3d1b6-103">在專案型合約服務內容中建立發票排程 - 精簡</span><span class="sxs-lookup"><span data-stu-id="3d1b6-103">Create invoice schedules on a project-based contract line - lite</span></span>

<span data-ttu-id="3d1b6-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="3d1b6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3d1b6-105">您可以在專案型合約服務內容上附加發票排程。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-105">You can attach an invoice schedule on a project-based contract line.</span></span> <span data-ttu-id="3d1b6-106">只有在贏得合約以建立專案合約之後，才允許開立發票。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-106">Invoicing is only allowed after the contract is won to create a Project contract.</span></span> <span data-ttu-id="3d1b6-107">發票排程允許自動建立專案型合約服務內容的草稿發票。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-107">Invoice schedules allow draft invoices for a project-based contract line to be created automatically.</span></span> <span data-ttu-id="3d1b6-108">如果您打算始終都以手動方式建立發票，則可以略過建立專案型合約服務內容或合約服務內容的發票排程。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-108">If you plan to always create invoices manually, you can skip creating invoice schedules on a project-based contract line or a contract line.</span></span>

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a><span data-ttu-id="3d1b6-109">建立專案型合約服務內容的時間和材料發票排程</span><span class="sxs-lookup"><span data-stu-id="3d1b6-109">Create a time and material invoice schedule for a project-based contract line</span></span>

<span data-ttu-id="3d1b6-110">專案型合約服務內容使用 [時間和材料] 的帳務方式時，您可以建立基於日期的發票排程。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-110">When a project-based contract line has a time and material billing method, you can create a date-based invoice schedule.</span></span> <span data-ttu-id="3d1b6-111">若要讓系統自動產生基於日期的發票排程，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-111">To automatically generate a date-based invoice schedule, complete the following steps.</span></span>

1. <span data-ttu-id="3d1b6-112">移至 **設定** > **發票週期**，以設定開立發票的頻率。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-112">Go to **Settings** > **Invoice Frequencies** to set up invoice frequency.</span></span>
2. <span data-ttu-id="3d1b6-113">開啟專案合約，並在 **摘要** 索引標籤中設定要求的交付日期。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-113">Open the project contract and on the **Summary** tab, set the requested delivery date.</span></span>
3. <span data-ttu-id="3d1b6-114">開啟需要建立基於日期之發票排程的時間和材料合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-114">Open the time and material contract line that you want to create a date-based invoice schedule for.</span></span> 
4. <span data-ttu-id="3d1b6-115">在 **發票排程** 索引標籤中，選取帳單開始日期和發票週期。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-115">On the **Invoice Schedule** tab, select a billing start date and the invoice frequency.</span></span> 
5. <span data-ttu-id="3d1b6-116">在子格上，選取 **產生發票排程**。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-116">On the subgrid, select **Generate Invoice Schedule**.</span></span>

    <span data-ttu-id="3d1b6-117">系統會使用下列欄位資訊來產生發票排程：</span><span class="sxs-lookup"><span data-stu-id="3d1b6-117">The system generates the invoice schedule with the following field information:</span></span>

    - <span data-ttu-id="3d1b6-118">**發票執行日期** 會設定為以發票週期為基準的日期。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-118">**Invoice Run Date** is set to the date based on the invoice frequency.</span></span>
    - <span data-ttu-id="3d1b6-119">**交易截止日期** 會設定為 **發票執行日期** 的前一天。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-119">**Transaction Cut-off Date** is set to the day before the **Invoice Run Date**.</span></span>
    - <span data-ttu-id="3d1b6-120">**執行狀態** 會自動設為 **未執行**。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-120">**Run Status** is automatically set to **Not Run**.</span></span> <span data-ttu-id="3d1b6-121">自動發票建立作業針對特定 **發票執行日期** 執行時，此欄位會更新為 **執行成功** 或 **執行失敗**。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-121">When the automatic invoice creation job runs for a certain **Invoice Run Date**, this field is updated to **Run Successful** or **Run Failed**.</span></span>

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a><span data-ttu-id="3d1b6-122">建立專案型合約服務內容的固定價格發票排程</span><span class="sxs-lookup"><span data-stu-id="3d1b6-122">Create a fixed price invoice schedule for a project-based contract line</span></span>

<span data-ttu-id="3d1b6-123">專案型合約服務內容採用固定價格帳務方式時，您可以建立基於里程碑的發票排程。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-123">When a project-based contract line has a fixed price billing method, you can create a milestone-based invoice schedule.</span></span> <span data-ttu-id="3d1b6-124">完成下列步驟，讓系統自動為固定一組平均分佈在行事曆期間的里程碑產生基於里程碑的發票排程。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-124">Complete the following steps to automatically generate a milestone-based invoice schedule for a fixed set of milestones that distribute equally for the calendar period.</span></span>

1. <span data-ttu-id="3d1b6-125">移至 **設定** > **發票週期**，以設定開立發票的頻率。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-125">Go to **Settings** > **Invoice Frequencies** to set up invoice frequency.</span></span>
2. <span data-ttu-id="3d1b6-126">開啟專案合約，並在 **摘要** 索引標籤中設定要求的交付日期。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-126">Open the project contract and on the **Summary** tab, set the requested delivery date.</span></span>
3. <span data-ttu-id="3d1b6-127">開啟需要建立里程碑排程的固定價格合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-127">Open the fixed price contract line on which you need to create a milestone schedule.</span></span> 
4. <span data-ttu-id="3d1b6-128">在 **發票排程 (帳單里程碑)** 索引標籤中，選取帳單開始日期和發票週期。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-128">On the **Invoice Schedule (Billing Milestones)** tab, select the billing start date and the invoice frequency.</span></span> 
5. <span data-ttu-id="3d1b6-129">在子格上，選取 **產生定期里程碑**。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-129">On the subgrid, select **Generate Periodic Milestones**.</span></span>

    <span data-ttu-id="3d1b6-130">系統會使用下列里程碑資訊來產生發票排程。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-130">The system generates the invoice schedule with the following milestone information.</span></span>

    - <span data-ttu-id="3d1b6-131">**里程碑名稱** 會設定為取決於發票週期的日期。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-131">**Milestone Name** is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="3d1b6-132">**里程碑日期** 會設定為取決於發票週期的日期。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-132">**Milestone Date** is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="3d1b6-133">**里程碑金額** 的計算方式是，將專案型合約服務內容上的合約金額除以由開票頻率、帳單開始日期和要求交付日期所決定的里程碑數目。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-133">**Milestone Amount** is calculated by dividing the contract amount on the project-based contract line by the number of milestones as dictated by the frequency, billing start, and requested delivery dates.</span></span>
    - <span data-ttu-id="3d1b6-134">如果合約服務內容在 **估計稅額** 欄位中有值，則此欄位也會在產生定期里程碑時，平均分攤到每個里程碑。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-134">If the contract line has a value in the **Estimated Tax Amount** field, this field is also apportioned to each milestone equally when generating periodic milestones.</span></span>

<span data-ttu-id="3d1b6-135">帳單里程碑應等於專案型合約服務內容的值。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-135">Billing milestones should equal the contracted value of the project-based contract line.</span></span> <span data-ttu-id="3d1b6-136">如果不相等，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-136">If they aren't equal, an error occurs.</span></span> <span data-ttu-id="3d1b6-137">您可以透過建立、編輯或刪除里程碑的方式，確認帳單個里程碑是否已總計合約服務內容的合約值，藉此修正該錯誤。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-137">You can fix that error by verifying that the billing milestones total the contracted value of the line by either creating, editing, or deleting milestones.</span></span> <span data-ttu-id="3d1b6-138">進行變更之後，請重新整理頁面。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-138">After the changes are made, refresh the page.</span></span>

### <a name="manually-create-milestones"></a><span data-ttu-id="3d1b6-139">手動建立里程碑</span><span class="sxs-lookup"><span data-stu-id="3d1b6-139">Manually create milestones</span></span>

<span data-ttu-id="3d1b6-140">固定價格里程碑不會定期進行分割時，您可以手動產生這些里程碑。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-140">Fixed price milestones can be generated manually when they aren't periodically split.</span></span> <span data-ttu-id="3d1b6-141">若要手動建立里程碑，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-141">To create a milestone manually, complete the following steps.</span></span>

1. <span data-ttu-id="3d1b6-142">開啟需要建立里程碑的固定價格合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-142">Open the fixed price contract line on which you want to create a milestone.</span></span> 
2. <span data-ttu-id="3d1b6-143">在 **發票排程** 索引標籤的子格中，選取 **+ 建立新的合約服務內容里程碑**。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-143">On the **Invoice Schedule** tab, on the subgrid, select **+ Create new Contract line milestone**.</span></span>
3. <span data-ttu-id="3d1b6-144">在 **里程碑建立** 表單上，根據下表輸入所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-144">On the **Milestone Creation** form, enter the required information based on the following table.</span></span> 

| <span data-ttu-id="3d1b6-145">欄位</span><span class="sxs-lookup"><span data-stu-id="3d1b6-145">Field</span></span> | <span data-ttu-id="3d1b6-146">地點</span><span class="sxs-lookup"><span data-stu-id="3d1b6-146">Location</span></span> | <span data-ttu-id="3d1b6-147">描述</span><span class="sxs-lookup"><span data-stu-id="3d1b6-147">Description</span></span> | <span data-ttu-id="3d1b6-148">下游影響</span><span class="sxs-lookup"><span data-stu-id="3d1b6-148">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="3d1b6-149">里程碑名稱</span><span class="sxs-lookup"><span data-stu-id="3d1b6-149">Milestone Name</span></span> | <span data-ttu-id="3d1b6-150">快速建立</span><span class="sxs-lookup"><span data-stu-id="3d1b6-150">Quick Create</span></span> | <span data-ttu-id="3d1b6-151">里程碑名稱的文字欄位。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-151">Text field for the name of the milestone.</span></span> | <span data-ttu-id="3d1b6-152">此欄位已包含在專案合約服務內容里程碑和發票中。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-152">This field is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="3d1b6-153">專案工作</span><span class="sxs-lookup"><span data-stu-id="3d1b6-153">Project Task</span></span> | <span data-ttu-id="3d1b6-154">快速建立</span><span class="sxs-lookup"><span data-stu-id="3d1b6-154">Quick Create</span></span> | <span data-ttu-id="3d1b6-155">如果里程碑已繫結至專案工作，請使用此參考來新增自訂邏輯，並根據工作狀態設定里程碑狀態。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-155">If the milestone is tied to a project task, use this reference to add custom logic and set the milestone status based on the task status.</span></span> | <span data-ttu-id="3d1b6-156">此參考對工作沒有任何下游影響。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-156">There is no downstream impact of this reference to a task.</span></span> |
| <span data-ttu-id="3d1b6-157">里程碑日期</span><span class="sxs-lookup"><span data-stu-id="3d1b6-157">Milestone Date</span></span> | <span data-ttu-id="3d1b6-158">快速建立</span><span class="sxs-lookup"><span data-stu-id="3d1b6-158">Quick Create</span></span> | <span data-ttu-id="3d1b6-159">自動發票建立程序應查看此里程碑狀態據以考慮開立發票的日期。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-159">The date on which the automatic invoice creation process should look for the status of this milestone to consider it for invoicing.</span></span> | <span data-ttu-id="3d1b6-160">這已包含在專案合約服務內容里程碑和發票中。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-160">This is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="3d1b6-161">發票狀態</span><span class="sxs-lookup"><span data-stu-id="3d1b6-161">Invoice Status</span></span> | <span data-ttu-id="3d1b6-162">快速建立</span><span class="sxs-lookup"><span data-stu-id="3d1b6-162">Quick Create</span></span> | <span data-ttu-id="3d1b6-163">建立里程碑時，此狀態一律設定為 **尚未準備好開立發票** 或 **未開始**。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-163">When the milestone is created, this status is always set to **Not ready for invoicing** or **Not started**.</span></span> | <span data-ttu-id="3d1b6-164">這已包含在專案合約服務內容里程碑和發票中。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-164">This is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="3d1b6-165">明細金額</span><span class="sxs-lookup"><span data-stu-id="3d1b6-165">Line Amount</span></span> | <span data-ttu-id="3d1b6-166">快速建立</span><span class="sxs-lookup"><span data-stu-id="3d1b6-166">Quick Create</span></span> | <span data-ttu-id="3d1b6-167">要向客戶開立發票的里程碑金額或值。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-167">The amount or value of the milestone that will be invoiced to the customer.</span></span> | <span data-ttu-id="3d1b6-168">此欄位已包含在專案合約服務內容里程碑和發票中，</span><span class="sxs-lookup"><span data-stu-id="3d1b6-168">This field is included on the project contract line milestone and the invoice,</span></span> |
| <span data-ttu-id="3d1b6-169">稅額</span><span class="sxs-lookup"><span data-stu-id="3d1b6-169">Tax</span></span> | <span data-ttu-id="3d1b6-170">快速建立</span><span class="sxs-lookup"><span data-stu-id="3d1b6-170">Quick Create</span></span> | <span data-ttu-id="3d1b6-171">套用在里程碑上的稅額。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-171">The tax amount applied on the milestone.</span></span> | <span data-ttu-id="3d1b6-172">這已包含在專案合約服務內容里程碑和發票中。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-172">This is included on the project contract line milestone and the invoice.</span></span> |

4. <span data-ttu-id="3d1b6-173">選取 **儲存後關閉**。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-173">Select **Save and Close**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]