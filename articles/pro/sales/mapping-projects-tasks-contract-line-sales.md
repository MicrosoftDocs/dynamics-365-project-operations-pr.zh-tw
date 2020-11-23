---
title: 將專案和工作對應至專案型合約服務內容 - 精簡
description: 此主題提供在合約服務內容中新增和移除專案及工作的資訊。
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 30a74f683a032d5bd6caed347f4d0a948376d267
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177636"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line---lite"></a><span data-ttu-id="98112-103">將專案和工作對應至專案型合約服務內容 - 精簡</span><span class="sxs-lookup"><span data-stu-id="98112-103">Map projects and tasks to a project-based contract line - lite</span></span>

<span data-ttu-id="98112-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="98112-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="98112-105">在專案型合約服務內容上，您可以將專案中的特定工作對應至合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="98112-105">On project-based contract lines, you can map specific tasks in a project to the contract line.</span></span>

<span data-ttu-id="98112-106">當您將特定工作對應至合約服務內容時，計費方式、可收費率選項、不得超過限制以及合約服務內容上定義的客戶都將只適用於這些特定工作。</span><span class="sxs-lookup"><span data-stu-id="98112-106">When you map specific tasks to a contract line, the billing method, chargeability options, Not-to-exceed limits, and the customers defined on the contract line will be applicable to those specific tasks only.</span></span>

<span data-ttu-id="98112-107">如果您有一個專案階段（例如，原型階段）是固定價格而所有其他階段都是時間和資料，則您可以使用固定價格計費方式，將原型階段與所有關聯子工作關聯至該階段的合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="98112-107">If you have a scenario where one phase of a project, for example the Prototype Phase, is fixed price and all the other phases are time and material, you will be able to associate the Prototype phase and all the associated child tasks to the contract line for that phase with a fixed price billing method.</span></span>

<span data-ttu-id="98112-108">專案分工結構圖 (WBS) 中的所有其他階段都可以與資料型合約服務內容相關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-108">All the other phases in your project work breakdown structure (WBS) can be associated to the time and material-based contract line.</span></span>

## <a name="associate-tasks-to-project-based-contract-lines"></a><span data-ttu-id="98112-109">將工作關聯至專案型合約服務內容</span><span class="sxs-lookup"><span data-stu-id="98112-109">Associate tasks to project-based contract lines</span></span>

<span data-ttu-id="98112-110">工作可從 **合約服務內容** 頁面的 **應收費工作** 索引標籤或從 **專案** 頁面的 **工作帳單** 索引標籤中，關聯至合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="98112-110">Tasks can be associated to contract lines from the **Chargeable Tasks** tab on the **Contract Line** page or from the **Task Billing** tab on the **Project** page.</span></span>

### <a name="from-the-contract-line-page"></a><span data-ttu-id="98112-111">從合約服務內容頁面</span><span class="sxs-lookup"><span data-stu-id="98112-111">From the Contract line page</span></span>

<span data-ttu-id="98112-112">從 **合約服務內容** 頁面的 **應收費工作** 索引標籤中，完成下列步驟，將專案工作關聯至合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="98112-112">Complete the following steps to associate project tasks to the contract line from the **Chargeable Tasks** tab of the **Contract Line** page.</span></span>

1. <span data-ttu-id="98112-113">在專案型合約服務內容的 **一般** 索引標籤上，確認已填入 **專案** 欄位。</span><span class="sxs-lookup"><span data-stu-id="98112-113">On the **General** tab of a project-based contract line, verify that the **Project** field is filled out.</span></span>
2. <span data-ttu-id="98112-114">在 **包含的工作** 欄位中，選取 **僅限選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="98112-114">In the **Included Tasks** field, select the **Selected Tasks Only**.</span></span>
3. <span data-ttu-id="98112-115">儲存您的變更。</span><span class="sxs-lookup"><span data-stu-id="98112-115">Save your changes.</span></span> <span data-ttu-id="98112-116">表單會重新整理，而且將會顯示 **應收費工作** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="98112-116">The form will refresh and the **Chargeable Tasks** tab will be visible.</span></span>
4. <span data-ttu-id="98112-117">選取 **應收費工作** 索引標籤，然後在子格中的，選取 **新增合約服務內容工作**。</span><span class="sxs-lookup"><span data-stu-id="98112-117">Select the **Chargeable Tasks** tab, and in the subgrid, select **Add a Contract Line Task**.</span></span>
5. <span data-ttu-id="98112-118">在 **合約服務內容工作** 頁面的 **工作** 下拉式清單中，選取工作。</span><span class="sxs-lookup"><span data-stu-id="98112-118">On the **Contract Line Tasks** page, in the **Tasks** drop-down, select the task.</span></span> 
6. <span data-ttu-id="98112-119">在 **帳單類型** 欄位中輸入資訊，然後選取 **儲存後關閉**。</span><span class="sxs-lookup"><span data-stu-id="98112-119">Enter information in the **Billing Type** field, and then select **Save and Close**.</span></span> <span data-ttu-id="98112-120">選取的工作會與合約服務內容相關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-120">The selected task is associated to the contract line.</span></span>

> [!NOTE]
> <span data-ttu-id="98112-121">這不是將專案工作關聯至合約服務內容的最佳體驗。</span><span class="sxs-lookup"><span data-stu-id="98112-121">This is not the most optimal experience for associating project tasks to contract lines.</span></span> <span data-ttu-id="98112-122">每個專案都必須在此體驗中手動建立關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-122">Each project will have to be manually associated in this experience.</span></span> <span data-ttu-id="98112-123">首選的方式是從 **專案** 頁面的 **工作帳單** 索引標籤中。</span><span class="sxs-lookup"><span data-stu-id="98112-123">The preferred way is from the **Task Billing** tab on the **Project** page.</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="98112-124">從專案頁面</span><span class="sxs-lookup"><span data-stu-id="98112-124">From the project page</span></span>

<span data-ttu-id="98112-125">這是將工作關聯到合約服務內容的最佳方法。</span><span class="sxs-lookup"><span data-stu-id="98112-125">This is the optimal method to associate tasks to contract lines.</span></span> <span data-ttu-id="98112-126">您可以選取多個工作，並將所有這些工作與其下層工作關聯至所選取的合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="98112-126">You can select multiple tasks and associate all of the them and their child tasks to the selected contract line.</span></span> <span data-ttu-id="98112-127">完成下列步驟，從 **專案** 頁面將工作與合約服務內容建立關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-127">Complete the following steps to associate tasks to the contract line from the **Project** page.</span></span>

1. <span data-ttu-id="98112-128">在專案型合約服務內容的 **一般** 索引標籤上，確認已填入 **專案** 欄位。</span><span class="sxs-lookup"><span data-stu-id="98112-128">On the **General** tab of a project-based contract line, verify that the **Project** field is filled out.</span></span>
2. <span data-ttu-id="98112-129">在 **包含的工作** 欄位中，選取 **僅限選取的工作**。</span><span class="sxs-lookup"><span data-stu-id="98112-129">On the **Included Tasks** field, select **Selected Tasks Only**.</span></span>
3. <span data-ttu-id="98112-130">儲存專案型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="98112-130">Save the project-based contract line.</span></span> <span data-ttu-id="98112-131">表單會重新整理，而且將會顯示 **應收費工作** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="98112-131">The form will refresh and the **Chargeable Tasks** tab will be visible.</span></span> <span data-ttu-id="98112-132">這只是為了驗證的目的。</span><span class="sxs-lookup"><span data-stu-id="98112-132">This is just for verification purposes only.</span></span>
4. <span data-ttu-id="98112-133">在專案型合約服務內容的 **一般** 索引標籤上，在 **專案** 欄位中選取專案連結。</span><span class="sxs-lookup"><span data-stu-id="98112-133">On the **General** tab of the project-based contract line, in the **Project** field, select the project link.</span></span>
5. <span data-ttu-id="98112-134">在 **專案** 頁面上，選取 **工作帳單設定** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="98112-134">On the **Project** page, select the **Task Billing Setup** tab.</span></span>
6. <span data-ttu-id="98112-135">有兩個網格。</span><span class="sxs-lookup"><span data-stu-id="98112-135">There are two grids.</span></span> <span data-ttu-id="98112-136">一個網格用於套用至整個專案的合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="98112-136">One grid is for contract lines that apply to the whole project.</span></span> <span data-ttu-id="98112-137">第二個網格會套用至特定工作的帳單設定。</span><span class="sxs-lookup"><span data-stu-id="98112-137">The second grid applies to task-specific billing setup.</span></span> <span data-ttu-id="98112-138">在第二個網格中，選取一或多個工作，然後選取 **關聯合約服務內容**。</span><span class="sxs-lookup"><span data-stu-id="98112-138">In the second grid, select one or more tasks, and then select **Associate Contract Lines**.</span></span>
7. <span data-ttu-id="98112-139">在開啟的對話方塊頁面中，從下拉式清單中選取合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="98112-139">In the dialog page that opens, select a contract line from the drop-down.</span></span>
8. <span data-ttu-id="98112-140">使用 **帳單類型** 下拉式清單，將工作標示為應收費或不應收費。</span><span class="sxs-lookup"><span data-stu-id="98112-140">Use the **Billing Type** drop-down to mark the tasks as chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="98112-141">選取核取方塊，以指出關聯是否也應包含所選工作的下層工作。</span><span class="sxs-lookup"><span data-stu-id="98112-141">Select the check box to indicate if the association should also include child tasks of the selected tasks.</span></span> <span data-ttu-id="98112-142">勾選方塊也會將所選工作的下層工作關聯至合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="98112-142">Checking the box will also associate the child tasks of the selected tasks to the contract line.</span></span>
10. <span data-ttu-id="98112-143">選取 **確定** 關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="98112-143">Select **OK** to close the dialog.</span></span>

## <a name="unassociate-tasks-from-project-based-contract-lines"></a><span data-ttu-id="98112-144">將工作與專案型合約服務內容解除關聯</span><span class="sxs-lookup"><span data-stu-id="98112-144">Unassociate tasks from project-based contract lines</span></span>

### <a name="from-the-contract-line-page"></a><span data-ttu-id="98112-145">從合約服務內容頁面</span><span class="sxs-lookup"><span data-stu-id="98112-145">From the contract line page</span></span>

<span data-ttu-id="98112-146">從 **合約服務內容** 頁面的 **應收費工作** 索引標籤中，完成下列步驟，將專案工作與合約服務內容解除關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-146">Complete the following steps to unassociate project tasks from the contract line on the **Chargeable Tasks** tab of the **Contract Line** page.</span></span>

1. <span data-ttu-id="98112-147">在 **應收費工作** 索引標籤上，選取 **刪除合約服務內容工作**。</span><span class="sxs-lookup"><span data-stu-id="98112-147">On the **Chargeable Tasks** tab, select **Delete a Contract Line Task**.</span></span>
2. <span data-ttu-id="98112-148">出現一則警告訊息，表示移除此關聯可能會導致逆轉先前已在工作中記錄的任何實際值。</span><span class="sxs-lookup"><span data-stu-id="98112-148">A warning message indicates that removing this association could result in reversal of any actuals previously recorded on the task.</span></span> <span data-ttu-id="98112-149">在對話方塊上選取 **確定**，移除工作與專案型合約服務內容之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-149">Select **OK** on the dialog to remove the association between the task and the project-based contract line.</span></span> 

> [!NOTE]
> <span data-ttu-id="98112-150">這並不會從專案中移除工作。</span><span class="sxs-lookup"><span data-stu-id="98112-150">This doesn't delete the task from the project.</span></span> <span data-ttu-id="98112-151">而是會從專案型合約服務內容移除工作關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-151">Instead, it removes the task association from the project-based contract line.</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="98112-152">從專案頁面</span><span class="sxs-lookup"><span data-stu-id="98112-152">From the project page</span></span>

<span data-ttu-id="98112-153">這是將專案工作與合約服務內容解除關聯的最佳體驗。</span><span class="sxs-lookup"><span data-stu-id="98112-153">This is the more optimal experience for unassociating tasks from contract lines.</span></span> <span data-ttu-id="98112-154">您可以選取多個工作，並將所有這些工作與其下層工作從所選取的合約服務內容解除關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-154">You can select multiple tasks and unassociate all of the them and their child tasks from the selected contract line.</span></span> <span data-ttu-id="98112-155">完成下列步驟，從合約服務內容解除工作的關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-155">Complete the following steps to unassociate tasks from the contract line.</span></span>

1. <span data-ttu-id="98112-156">從專案型合約服務內容的 **一般** 索引標籤，在 **專案** 欄位中，按一下專案的連結。</span><span class="sxs-lookup"><span data-stu-id="98112-156">From **General** tab of the project-based contract line, in the **Project** field, click on the link for project.</span></span>
2. <span data-ttu-id="98112-157">在 **專案** 頁面上，選取 **工作帳單設定** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="98112-157">On the **Project** page, select the **Task Billing Setup** tab.</span></span>
3. <span data-ttu-id="98112-158">頁面上有兩個網格。</span><span class="sxs-lookup"><span data-stu-id="98112-158">There are two grids on the page.</span></span> <span data-ttu-id="98112-159">一個網格用於套用至整個專案的合約服務內容，而第二個網格則套用至特定工作的帳單設定。</span><span class="sxs-lookup"><span data-stu-id="98112-159">One grid is for contract lines that apply to the whole project and the second applies to task-specific billing setup.</span></span> <span data-ttu-id="98112-160">在第二個網格中，選取一或多個工作，然後選取 **解除關聯合約服務內容**。</span><span class="sxs-lookup"><span data-stu-id="98112-160">In the second grid, select one or more tasks and the select **Disassociate Contract Lines**.</span></span>
4. <span data-ttu-id="98112-161">在開啟的對話方塊頁面中，從下拉式清單中選取合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="98112-161">In the  dialog page that opens, select a contract line from the drop-down.</span></span>
5. <span data-ttu-id="98112-162">選取核取方塊，以指出是否也應從所選工作的下層工作移除關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-162">Select the check box to indicate if the association should also be removed from any child tasks of the selected tasks.</span></span> <span data-ttu-id="98112-163">勾選方塊也會從合約服務內容解除關聯所選工作的下層工作。</span><span class="sxs-lookup"><span data-stu-id="98112-163">Checking the box will also unassociate the child tasks of the selected tasks from the contract line.</span></span>
6. <span data-ttu-id="98112-164">選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="98112-164">Select **OK**.</span></span> <span data-ttu-id="98112-165">出現一則警告訊息，表示移除此關聯可能會導致逆轉先前已在工作中記錄的任何實際值。</span><span class="sxs-lookup"><span data-stu-id="98112-165">A warning message indicates that removing this association could result in reversal of any actuals recorded on the task previously.</span></span> <span data-ttu-id="98112-166">在警告對話方塊上選取 **確定**，移除工作與專案型合約服務內容之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="98112-166">Select **OK** on the warning dialog to remove the association between the task and the project-based contract line.</span></span>
