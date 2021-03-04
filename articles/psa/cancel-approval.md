---
title: 取消先前核准的時間和費用項目
description: 本主題提供有關如何取消已核准專案時間或費用交易的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150568"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="91038-103">取消先前核准的時間或費用項目</span><span class="sxs-lookup"><span data-stu-id="91038-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="91038-104">在最新版本的 Dynamics 365 Project Service Automation 中，核准者可以取消他們先前核准的時間或費用項目。</span><span class="sxs-lookup"><span data-stu-id="91038-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="91038-105">取消先前核准的時間或費用項目</span><span class="sxs-lookup"><span data-stu-id="91038-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="91038-106">依照下列步驟，取消先前已核准的時間或費用項目。</span><span class="sxs-lookup"><span data-stu-id="91038-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="91038-107">移至 **專案** \> **我的工作** \> **核准**。</span><span class="sxs-lookup"><span data-stu-id="91038-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="91038-108">在 **核准** 清單頁面上，將檢視表變更到 **我過去的核准**。</span><span class="sxs-lookup"><span data-stu-id="91038-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="91038-109">隨即顯示您先前已核准的時間和費用項目清單。</span><span class="sxs-lookup"><span data-stu-id="91038-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="91038-110">選取一個或多個項目，然後選擇 **取消核准**。</span><span class="sxs-lookup"><span data-stu-id="91038-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="91038-111">您會收到警告訊息。</span><span class="sxs-lookup"><span data-stu-id="91038-111">You receive a warning message.</span></span>
4. <span data-ttu-id="91038-112">選取 **確定** 以取消核准。</span><span class="sxs-lookup"><span data-stu-id="91038-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="91038-113">了解取消時間或費用項目核准的影響</span><span class="sxs-lookup"><span data-stu-id="91038-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="91038-114">取消核准時，會產生營運影響和財務影響。</span><span class="sxs-lookup"><span data-stu-id="91038-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="91038-115">營運影響</span><span class="sxs-lookup"><span data-stu-id="91038-115">Operational impact</span></span>

<span data-ttu-id="91038-116">在營運面，取消核准時，會將該記錄的狀態重設為 **草稿**，而且該核准已不再出現於 **我過去的核准** 檢視表中。</span><span class="sxs-lookup"><span data-stu-id="91038-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="91038-117">相反地，取消的核准會出現在 **供核准的時間項目** 檢視表或 **供核准的費用項目** 檢視表中，視其為時間項目還是費用項目而定。</span><span class="sxs-lookup"><span data-stu-id="91038-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="91038-118">此外，相關時間或費用項目的狀態會變更為 **已送出**，使相關項目與狀態為 **草稿** 的核准一致。</span><span class="sxs-lookup"><span data-stu-id="91038-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="91038-119">身為核准者，您可以編輯狀態為 **草稿** 之核准的部分欄位。</span><span class="sxs-lookup"><span data-stu-id="91038-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="91038-120">這些欄位包括 **帳單類型** 和 **時間項目計費時數**。</span><span class="sxs-lookup"><span data-stu-id="91038-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="91038-121">進行變更之後，您可以重新核准該記錄。</span><span class="sxs-lookup"><span data-stu-id="91038-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="91038-122">或者，也可以拒絕該項目。</span><span class="sxs-lookup"><span data-stu-id="91038-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="91038-123">如果您拒絕核准時間項目，該項目的狀態會變更為 **已退回**。</span><span class="sxs-lookup"><span data-stu-id="91038-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="91038-124">如果您拒絕核准費用項目，狀態會變更為 **已拒絕**。</span><span class="sxs-lookup"><span data-stu-id="91038-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="91038-125">在功能上，已退回和已拒絕項目的行為與狀態為 **草稿** 的項目相同。</span><span class="sxs-lookup"><span data-stu-id="91038-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="91038-126">專案團隊成員可以對項目進行任何必要的變更，然後重新送出供核准，或是完全刪除。</span><span class="sxs-lookup"><span data-stu-id="91038-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="91038-127">財務影響</span><span class="sxs-lookup"><span data-stu-id="91038-127">Financial impact</span></span>

<span data-ttu-id="91038-128">取消核准時，專案也會在財務上受到影響。</span><span class="sxs-lookup"><span data-stu-id="91038-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="91038-129">首先，成本和銷售的對應實際值會以下列方式更新：</span><span class="sxs-lookup"><span data-stu-id="91038-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="91038-130">調整狀態會設定為 **已調整**。</span><span class="sxs-lookup"><span data-stu-id="91038-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="91038-131">帳單狀態設定為 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="91038-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="91038-132">接下來，在 [實際值] 表格中建立沖回分錄。</span><span class="sxs-lookup"><span data-stu-id="91038-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="91038-133">為了建立沖回分錄，系統複製原始實際值中的欄位值。</span><span class="sxs-lookup"><span data-stu-id="91038-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="91038-134">唯一未複製的值是數量值。</span><span class="sxs-lookup"><span data-stu-id="91038-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="91038-135">這些值反而是進行沖回。</span><span class="sxs-lookup"><span data-stu-id="91038-135">These values are reversed instead.</span></span> <span data-ttu-id="91038-136">**成本** 與 **未開單銷售** 實際值都會建立已沖回的實際值。</span><span class="sxs-lookup"><span data-stu-id="91038-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="91038-137">已沖回實際值的 **調整狀態** 欄位會設定為 **不可調整**，且帳單狀態欄位會設定為 **已取消**。</span><span class="sxs-lookup"><span data-stu-id="91038-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="91038-138">進行這些變更之後，專案上記錄為支出的金額以及專案的營收待辦項目將不會再有這些實際值所占的金額。</span><span class="sxs-lookup"><span data-stu-id="91038-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
