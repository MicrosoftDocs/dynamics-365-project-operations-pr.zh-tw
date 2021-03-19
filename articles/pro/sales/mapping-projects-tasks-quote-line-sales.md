---
title: 將專案和工作對應至專案型報價明細
description: 本主題提供有關如何將專案和工作對應至專案型工作明細的資訊。
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272738"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="a43a7-103">將專案和工作對應至專案型報價明細</span><span class="sxs-lookup"><span data-stu-id="a43a7-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="a43a7-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="a43a7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a43a7-105">在專案型報價明細上，您可以對應已經與報價明細相關聯之專案的特定工作。</span><span class="sxs-lookup"><span data-stu-id="a43a7-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="a43a7-106">將工作對應至報價明細時，您已在報價明細中定義的下列項目只會套用至這些工作：</span><span class="sxs-lookup"><span data-stu-id="a43a7-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="a43a7-107">帳務方式</span><span class="sxs-lookup"><span data-stu-id="a43a7-107">Billing method</span></span>
- <span data-ttu-id="a43a7-108">可收費率選項</span><span class="sxs-lookup"><span data-stu-id="a43a7-108">Chargeability options</span></span>
- <span data-ttu-id="a43a7-109">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="a43a7-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="a43a7-110">客戶</span><span class="sxs-lookup"><span data-stu-id="a43a7-110">Customers</span></span>

<span data-ttu-id="a43a7-111">例如，您的專案可能會一個階段是固定價格，而所有其他階段皆是時間和材料。</span><span class="sxs-lookup"><span data-stu-id="a43a7-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="a43a7-112">在這種情況下，您可以將第一個階段及其所有下層工作都關聯至該階段使用固定價格帳務方式的報價明細。</span><span class="sxs-lookup"><span data-stu-id="a43a7-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="a43a7-113">您可以接著將所有其他階段關聯至基於時間和材料的報價明細。</span><span class="sxs-lookup"><span data-stu-id="a43a7-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="a43a7-114">將工作與專案型報價明細建立關聯</span><span class="sxs-lookup"><span data-stu-id="a43a7-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="a43a7-115">您可以從下列位置，建立工作與報價明細的關聯：</span><span class="sxs-lookup"><span data-stu-id="a43a7-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="a43a7-116">**專案** 頁面 > **工作帳單** 索引標籤 (最佳)</span><span class="sxs-lookup"><span data-stu-id="a43a7-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="a43a7-117">**報價明細** 頁面 > **應收費工作** 索引標籤</span><span class="sxs-lookup"><span data-stu-id="a43a7-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="a43a7-118">從 [專案] 頁面</span><span class="sxs-lookup"><span data-stu-id="a43a7-118">From the Project page</span></span>

<span data-ttu-id="a43a7-119">**專案** 頁面提供將工作關聯至報價明細的最佳體驗。</span><span class="sxs-lookup"><span data-stu-id="a43a7-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="a43a7-120">您可以使用此頁面選取多個工作，並將所有工作 (加上其下層工作) 關聯至選取的報價明細。</span><span class="sxs-lookup"><span data-stu-id="a43a7-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="a43a7-121">在專案型報價明細的 **一般** 索引標籤上，確認是否已填寫 **專案** 欄位。</span><span class="sxs-lookup"><span data-stu-id="a43a7-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="a43a7-122">在 **包含的工作** 欄位中，選取 **僅限選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="a43a7-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="a43a7-123">儲存專案型報價明細。</span><span class="sxs-lookup"><span data-stu-id="a43a7-123">Save the project-based quote line.</span></span> <span data-ttu-id="a43a7-124">表單重新整理時，**應收費工作** 索引標籤會顯示。</span><span class="sxs-lookup"><span data-stu-id="a43a7-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="a43a7-125">在 **一般** 索引標籤上，從 **專案** 欄位選取專案的連結。</span><span class="sxs-lookup"><span data-stu-id="a43a7-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="a43a7-126">在 **專案** 頁面上，選取 **工作帳單** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="a43a7-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="a43a7-127">在第二個套用至工作特定帳單設定的網格中，選取一個或多個工作，然後選取 **關聯報價明細**。</span><span class="sxs-lookup"><span data-stu-id="a43a7-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="a43a7-128">在出現的對話方塊頁面中，選取顯示報價上專案型報價明細的報價明細。</span><span class="sxs-lookup"><span data-stu-id="a43a7-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="a43a7-129">在 **帳單類型** 欄位中，指示這些工作是應收費還不應收費。</span><span class="sxs-lookup"><span data-stu-id="a43a7-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="a43a7-130">選取核取方塊，以指示關聯是否應包括所選工作的下層工作。</span><span class="sxs-lookup"><span data-stu-id="a43a7-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="a43a7-131">勾選方塊會將所選工作的下層工作關聯至報價明細。</span><span class="sxs-lookup"><span data-stu-id="a43a7-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="a43a7-132">選取 **確定** 關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a43a7-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="a43a7-133">從 [報價明細] 頁面</span><span class="sxs-lookup"><span data-stu-id="a43a7-133">From the Quote line page</span></span>

<span data-ttu-id="a43a7-134">您可以從 **報價明細** 頁面的 **應收費工作** 索引標籤中，將專案工作關聯至報價明細。</span><span class="sxs-lookup"><span data-stu-id="a43a7-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="a43a7-135">將專案工作關聯至報價明細的最佳位置是在 **專案** 頁面的 **工作帳單** 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="a43a7-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="a43a7-136">如果您從 **報價明細** 頁面的 **應收費工作** 索引標籤建立工作關聯，則必須手動關聯每個專案。</span><span class="sxs-lookup"><span data-stu-id="a43a7-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="a43a7-137">在專案型報價明細的 **一般** 索引標籤上，確認 **專案** 欄位中是否有已選取的專案。</span><span class="sxs-lookup"><span data-stu-id="a43a7-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="a43a7-138">在 **包含的工作** 欄位中，選取 **僅限選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="a43a7-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="a43a7-139">儲存專案型報價明細。</span><span class="sxs-lookup"><span data-stu-id="a43a7-139">Save the project-based quote line.</span></span> <span data-ttu-id="a43a7-140">表單重新整理時，**應收費工作** 索引標籤會顯示。</span><span class="sxs-lookup"><span data-stu-id="a43a7-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="a43a7-141">在 **應收費工作** 索引標籤上，選取 **新增報價明細工作**。</span><span class="sxs-lookup"><span data-stu-id="a43a7-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="a43a7-142">在 **報價明細工作** 頁面的 **工作** 欄位中，選取工作，然後在 **帳單類型** 欄位中選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="a43a7-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="a43a7-143">關閉頁面。</span><span class="sxs-lookup"><span data-stu-id="a43a7-143">Close the page.</span></span> <span data-ttu-id="a43a7-144">選取的工作現已關聯至報價明細。</span><span class="sxs-lookup"><span data-stu-id="a43a7-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="a43a7-145">解除工作與專案型報價明細的關聯</span><span class="sxs-lookup"><span data-stu-id="a43a7-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="a43a7-146">從 [專案] 頁面</span><span class="sxs-lookup"><span data-stu-id="a43a7-146">From the Project page</span></span>

<span data-ttu-id="a43a7-147">此方法提供將工作與報價明細解除關聯的最佳體驗。</span><span class="sxs-lookup"><span data-stu-id="a43a7-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="a43a7-148">您可以選取多個工作，並將所有工作 (加上其下層工作) 與選取的報價明細解除關聯。</span><span class="sxs-lookup"><span data-stu-id="a43a7-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="a43a7-149">在專案型報價明細 **一般** 索引標籤的 **專案** 欄位中，選取專案連結。</span><span class="sxs-lookup"><span data-stu-id="a43a7-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="a43a7-150">在 **專案** 頁面上，選取 **工作帳單** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="a43a7-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="a43a7-151">在第二個套用至工作特定帳單設定的網格中，選取一個或多個工作，然後選取 **解除關聯報價明細**。</span><span class="sxs-lookup"><span data-stu-id="a43a7-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="a43a7-152">在出現的對話方塊頁面中，選取報價明細。</span><span class="sxs-lookup"><span data-stu-id="a43a7-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="a43a7-153">選取核取方塊，以指示關聯是否也應所選工作的下層工作移除關聯。</span><span class="sxs-lookup"><span data-stu-id="a43a7-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="a43a7-154">勾選方塊也會將所選工作的下層工作與報價明細解除關聯。</span><span class="sxs-lookup"><span data-stu-id="a43a7-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="a43a7-155">選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="a43a7-155">Select **OK**.</span></span> <span data-ttu-id="a43a7-156">警告訊息會通知您，如果移除此關聯，可能會沖銷先前在工作中記錄的任何實際值。</span><span class="sxs-lookup"><span data-stu-id="a43a7-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="a43a7-157">選取 **確定**，以繼續，並移除工作與專案型報價明細之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="a43a7-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="a43a7-158">從 [報價明細] 頁面</span><span class="sxs-lookup"><span data-stu-id="a43a7-158">From the Quote line page</span></span>

<span data-ttu-id="a43a7-159">您也可以從 **報價明細** 頁面的 **應收費工作** 索引標籤中，將專案工作與報價明細解除關聯。</span><span class="sxs-lookup"><span data-stu-id="a43a7-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="a43a7-160">在 **應收費工作** 索引標籤上，選取 **刪除報價明細工作**。</span><span class="sxs-lookup"><span data-stu-id="a43a7-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="a43a7-161">選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="a43a7-161">Select **OK**.</span></span> <span data-ttu-id="a43a7-162">警告訊息會通知您，如果移除此關聯，可能會沖銷先前在工作中記錄的任何實際值。</span><span class="sxs-lookup"><span data-stu-id="a43a7-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="a43a7-163">選取 **確定**，以繼續，並移除工作與專案型報價明細之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="a43a7-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="a43a7-164">此程序不會將工作從專案中刪除。</span><span class="sxs-lookup"><span data-stu-id="a43a7-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="a43a7-165">只是從專案型報價明細中移除工作關聯。</span><span class="sxs-lookup"><span data-stu-id="a43a7-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]