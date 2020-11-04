---
title: 費用項目 (精簡)
description: 本主題提供有關如何在精簡部署中處理費用項目的資訊。
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072880"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="e665d-103">費用項目 (精簡)</span><span class="sxs-lookup"><span data-stu-id="e665d-103">Expense entry (lite)</span></span>

<span data-ttu-id="e665d-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="e665d-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e665d-105">基本 (或精簡) 費用管理是用於記錄簡單費用的功能。</span><span class="sxs-lookup"><span data-stu-id="e665d-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="e665d-106">您可以針對專案來記錄費用，然後專案核准者會審查並核准這些費用。</span><span class="sxs-lookup"><span data-stu-id="e665d-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="e665d-107">如需 Dynamics 365 Project Operations 中費用功能的詳細資訊，請參閱[費用概觀](expense-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="e665d-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="e665d-108">擷取基本費用</span><span class="sxs-lookup"><span data-stu-id="e665d-108">Capture a basic expense</span></span>

<span data-ttu-id="e665d-109">您可以擷取您的費用，以便將其提交給核准者。</span><span class="sxs-lookup"><span data-stu-id="e665d-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="e665d-110">移至 **費用** ，然後選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="e665d-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="e665d-111">在 **新增費用** 頁面上，輸入必要的費用資訊，然後選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="e665d-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="e665d-112">提交基本費用</span><span class="sxs-lookup"><span data-stu-id="e665d-112">Submit a basic expense</span></span>

<span data-ttu-id="e665d-113">完成擷取所有的費用，且已準備好進行核准之後，您必須提交這些費用。</span><span class="sxs-lookup"><span data-stu-id="e665d-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="e665d-114">移至 **費用** ，然後選取費用。</span><span class="sxs-lookup"><span data-stu-id="e665d-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="e665d-115">或者，使用標題上的核取方塊來選取所有的費用。</span><span class="sxs-lookup"><span data-stu-id="e665d-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="e665d-116">選取 **送出** 。</span><span class="sxs-lookup"><span data-stu-id="e665d-116">Select **Submit**.</span></span> <span data-ttu-id="e665d-117">系統會處理選取的項目，然後建立費用核准要求。</span><span class="sxs-lookup"><span data-stu-id="e665d-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="e665d-118">回收基本費用</span><span class="sxs-lookup"><span data-stu-id="e665d-118">Recall a basic expense</span></span>

<span data-ttu-id="e665d-119">錯誤提交費用時，您可以將其回收。</span><span class="sxs-lookup"><span data-stu-id="e665d-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="e665d-120">回收費用項目所需的時間取決於其核准階段。</span><span class="sxs-lookup"><span data-stu-id="e665d-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="e665d-121">如果核准者尚未核准該項目，回收就會立即進行。</span><span class="sxs-lookup"><span data-stu-id="e665d-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="e665d-122">不過，如果項目已獲核准，則會要求核准者核准回收並沖銷交易。</span><span class="sxs-lookup"><span data-stu-id="e665d-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="e665d-123">移至 **費用** ，然後在費用清單中，選取要回收的費用。</span><span class="sxs-lookup"><span data-stu-id="e665d-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="e665d-124">選取 **回收** 。</span><span class="sxs-lookup"><span data-stu-id="e665d-124">Select **Recall**.</span></span> <span data-ttu-id="e665d-125">如果費用項目尚未獲核准，系統會立即將其回收。</span><span class="sxs-lookup"><span data-stu-id="e665d-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="e665d-126">如果費用項目已核准，則會建立回收要求以通知核准者您要沖銷費用。</span><span class="sxs-lookup"><span data-stu-id="e665d-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="e665d-127">核准者會接著確認他可以完成沖銷，並將該項目退回。</span><span class="sxs-lookup"><span data-stu-id="e665d-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="e665d-128">刪除基本費用</span><span class="sxs-lookup"><span data-stu-id="e665d-128">Delete a basic expense</span></span>

<span data-ttu-id="e665d-129">您可以刪除尚未提交的費用。</span><span class="sxs-lookup"><span data-stu-id="e665d-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="e665d-130">若要刪除已提交的費用，您必須先將其回收。</span><span class="sxs-lookup"><span data-stu-id="e665d-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="e665d-131">請參閱</span><span class="sxs-lookup"><span data-stu-id="e665d-131">See also</span></span>

- [<span data-ttu-id="e665d-132">核准概觀</span><span class="sxs-lookup"><span data-stu-id="e665d-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
