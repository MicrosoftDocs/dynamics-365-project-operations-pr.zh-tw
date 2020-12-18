---
title: 費用項目 (精簡)
description: 本主題提供有關如何在精簡部署中處理費用項目的資訊。
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590936"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="1dfbd-103">費用項目 (精簡)</span><span class="sxs-lookup"><span data-stu-id="1dfbd-103">Expense entry (lite)</span></span>

<span data-ttu-id="1dfbd-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="1dfbd-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1dfbd-105">基本 (或精簡) 費用管理是用於記錄簡單費用的功能。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="1dfbd-106">您可以針對專案來記錄費用，然後專案核准者會審查並核准這些費用。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="1dfbd-107">如需有關 Dynamics 365 Project Operations 中費用功能的詳細資訊，請參閱[費用概觀](expense-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="1dfbd-108">擷取基本費用</span><span class="sxs-lookup"><span data-stu-id="1dfbd-108">Capture a basic expense</span></span>

<span data-ttu-id="1dfbd-109">您可以擷取您的費用，以便將其提交給核准者。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="1dfbd-110">移至 **費用**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="1dfbd-111">在 **新增費用** 頁面上，輸入必要的費用資訊，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="1dfbd-112">提交基本費用</span><span class="sxs-lookup"><span data-stu-id="1dfbd-112">Submit a basic expense</span></span>

<span data-ttu-id="1dfbd-113">完成擷取所有的費用，且已準備好進行核准之後，您必須提交這些費用。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="1dfbd-114">移至 **費用**，然後選取費用。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="1dfbd-115">或者，使用標題上的核取方塊來選取所有的費用。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="1dfbd-116">選取 **送出**。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-116">Select **Submit**.</span></span> <span data-ttu-id="1dfbd-117">系統會處理選取的項目，然後建立費用核准要求。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="1dfbd-118">新增附件</span><span class="sxs-lookup"><span data-stu-id="1dfbd-118">Add an attachment</span></span>

<span data-ttu-id="1dfbd-119">您可能必須為核准者提供費用的額外文件。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="1dfbd-120">您可以在費用項目的時間表中附加收據。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="1dfbd-121">選取 **編輯** 並在 **時間表** 區段中選取迴紋針圖示以附加收據。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="1dfbd-122">回收基本費用</span><span class="sxs-lookup"><span data-stu-id="1dfbd-122">Recall a basic expense</span></span>

<span data-ttu-id="1dfbd-123">錯誤提交費用時，您可以將其回收。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="1dfbd-124">回收費用項目所需的時間取決於其核准階段。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="1dfbd-125">如果核准者尚未核准該項目，回收就會立即進行。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="1dfbd-126">不過，如果項目已獲核准，則會要求核准者核准回收並沖銷交易。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="1dfbd-127">移至 **費用**，然後在費用清單中，選取要回收的費用。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="1dfbd-128">選取 **回收**。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-128">Select **Recall**.</span></span> <span data-ttu-id="1dfbd-129">如果費用項目尚未獲核准，系統會立即將其回收。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="1dfbd-130">如果費用項目已核准，則會建立回收要求以通知核准者您要沖銷費用。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="1dfbd-131">核准者會接著確認他可以完成沖銷，並將該項目退回。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="1dfbd-132">刪除基本費用</span><span class="sxs-lookup"><span data-stu-id="1dfbd-132">Delete a basic expense</span></span>

<span data-ttu-id="1dfbd-133">您可以刪除尚未提交的費用。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="1dfbd-134">若要刪除已提交的費用，您必須先將其回收。</span><span class="sxs-lookup"><span data-stu-id="1dfbd-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="1dfbd-135">請參閱</span><span class="sxs-lookup"><span data-stu-id="1dfbd-135">See also</span></span>

- [<span data-ttu-id="1dfbd-136">核准概觀</span><span class="sxs-lookup"><span data-stu-id="1dfbd-136">Approvals overview</span></span>](../approvals/approvals-overview.md)
