---
title: 回收核准的時間或費用項目
description: 本主題提供有關如何回收先前核准的時間或費用交易的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147823"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="2ed2d-103">回收核准的時間或費用項目</span><span class="sxs-lookup"><span data-stu-id="2ed2d-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2ed2d-104">專案團隊成員或其他提交時間或費用項目的人員，可在其獲得核准後回收該項目。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="2ed2d-105">回收已核准時間或費用項目的程序有兩個步驟：</span><span class="sxs-lookup"><span data-stu-id="2ed2d-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="2ed2d-106">提交者要求回收。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="2ed2d-107">核准者核准回收。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="2ed2d-108">要求回收</span><span class="sxs-lookup"><span data-stu-id="2ed2d-108">Request a recall</span></span>

<span data-ttu-id="2ed2d-109">依照下列步驟，要求回收已核准的時間或費用項目。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="2ed2d-110">若為時間項目，移至 **專案** \> **我的工作** \> **時間項目**。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="2ed2d-111">-或-</span><span class="sxs-lookup"><span data-stu-id="2ed2d-111">–or–</span></span>

    <span data-ttu-id="2ed2d-112">若為費用項目，移至 **專案** \> **我的工作** \> **費用**。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="2ed2d-113">針對時間項目，選取專案與工作特定組合的所有時間項目。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="2ed2d-114">或者在網格中，選取特定專案特定日期的個別時間儲存格。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="2ed2d-115">-或-</span><span class="sxs-lookup"><span data-stu-id="2ed2d-115">–or–</span></span>

    <span data-ttu-id="2ed2d-116">針對費用項目，選取要回收的費用項目。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="2ed2d-117">選取 **回收**。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-117">Select **Recall**.</span></span> <span data-ttu-id="2ed2d-118">確認對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="2ed2d-119">如果選取的時間或費用項目已獲核准，系統會提示您輸入回收原因。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="2ed2d-120">輸入回收的原因，然後選取 **確定** 以確認操作。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="2ed2d-121">系統會傳送要求給核准項目的人員以請求核准回收。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="2ed2d-122">雖然可以回收已核准的時間和費用項目，但若已核准的時間或費用項目已開發票給客戶，就無法建立回收要求。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="2ed2d-123">嘗試建立回收要求的使用者將會收到訊息，指出該時間或費用項目因為已開發票而無法撤回。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="2ed2d-124">核准或拒絕回收要求</span><span class="sxs-lookup"><span data-stu-id="2ed2d-124">Approve or reject a recall request</span></span>

<span data-ttu-id="2ed2d-125">請依照下列步驟核准或拒絕回收要求。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="2ed2d-126">移至 **專案** \> **我的工作** \> **核准**。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="2ed2d-127">在 **核准** 清單頁面上，將檢視表變更到 **回收核准要求**。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="2ed2d-128">隨即顯示已送出的回收要求清單。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="2ed2d-129">選取一個或多個項目，然後選取 **核准** 或 **拒絕**。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="2ed2d-130">如果選取了 **核准**，您會收到警告訊息，解釋核准的影響。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="2ed2d-131">選取 **確定** 以確認操作。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="2ed2d-132">回收要求已核准。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-132">The recall request is approved.</span></span>

    <span data-ttu-id="2ed2d-133">-或-</span><span class="sxs-lookup"><span data-stu-id="2ed2d-133">–or–</span></span>

    <span data-ttu-id="2ed2d-134">如果選取 **拒絕**，則會拒絕回收要求。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="2ed2d-135">要求回收時、回收獲核准時，系統會檢查時間或費用項目是否有任何開立發票活動。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="2ed2d-136">如果項目已開具發票，或已記入草稿發票，則該核准者將收到錯誤訊息，指出因為已開發票而無法核准回收該時間或費用。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="2ed2d-137">回收要求的影響</span><span class="sxs-lookup"><span data-stu-id="2ed2d-137">Impact of a recall request</span></span>

<span data-ttu-id="2ed2d-138">回收核准時，會產生營運影響和財務影響。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="2ed2d-139">營運影響</span><span class="sxs-lookup"><span data-stu-id="2ed2d-139">Operational impact</span></span>

<span data-ttu-id="2ed2d-140">如果回收要求獲核准，則會將核准記錄標示為 **已拒絕**。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="2ed2d-141">項目的狀態會變更為 **已退回** 或 **已拒絕**，取決於它是時間項目還是費用項目。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="2ed2d-142">專案團隊成員可以檢視項目、編輯項目，然後重新將其送出或整個刪除。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="2ed2d-143">如果回收要求遭拒絕，該項目的狀態會保持 **已核准**，且專案團隊成員或專案核准者無法加以編輯。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="2ed2d-144">財務影響</span><span class="sxs-lookup"><span data-stu-id="2ed2d-144">Financial impact</span></span>

<span data-ttu-id="2ed2d-145">如果回收要求獲核准，成本和銷售的對應實際值會以下列方式更新：</span><span class="sxs-lookup"><span data-stu-id="2ed2d-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="2ed2d-146">**調整狀態** 欄位會更新為 **已調整**。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="2ed2d-147">**帳單狀態** 欄位會更新為 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="2ed2d-148">接下來，在 [實際值] 表格中建立沖回分錄。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="2ed2d-149">為了建立沖回分錄，系統複製原始實際值中的欄位值。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="2ed2d-150">唯一未複製的值是數量值。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="2ed2d-151">這些值反而是進行沖回。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-151">These values are reversed instead.</span></span> <span data-ttu-id="2ed2d-152">**成本** 與 **未開單銷售** 實際值都會建立已沖回的實際值。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="2ed2d-153">已沖回實際值的 **調整狀態** 欄位會設定為 **不可調整**，且 **帳單狀態** 欄位會設定為 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="2ed2d-154">由於有這些變更，專案中的已記錄支出和營收積存將不會再有這些實際值所占的金額。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="2ed2d-155">如果回收要求遭拒絕，就不會對專案造成任何財務影響。</span><span class="sxs-lookup"><span data-stu-id="2ed2d-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="2ed2d-156">對時間項目記錄的變更</span><span class="sxs-lookup"><span data-stu-id="2ed2d-156">Changes to time entry records</span></span>

<span data-ttu-id="2ed2d-157">下圖顯示已核准時間項目在其被回收時發生的變更</span><span class="sxs-lookup"><span data-stu-id="2ed2d-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![時間項目狀態轉換](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="2ed2d-159">對費用項目記錄的變更</span><span class="sxs-lookup"><span data-stu-id="2ed2d-159">Changes to expense entry records</span></span>

<span data-ttu-id="2ed2d-160">下圖顯示已核准費用項目在其被回收時發生的變更</span><span class="sxs-lookup"><span data-stu-id="2ed2d-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![費用項目狀態轉換](media/ExpenseEntryStateTransitions.png)
