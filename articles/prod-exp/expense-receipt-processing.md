---
title: 費用收據處理
description: 本主題提供有關使用光學字元辨識 (OCR) 處理收據的資訊。 此功能是專為改善使用者在 Microsoft Dynamics 365 Finance 中建立費用報表時的體驗而設計。
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073154"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="6639c-104">費用收據處理</span><span class="sxs-lookup"><span data-stu-id="6639c-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6639c-105">費用項目因採用光學字元辨識 (OCR) 處理收據而有所增強。</span><span class="sxs-lookup"><span data-stu-id="6639c-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="6639c-106">此功能是專為改善使用者建立費用報表時的體驗而設計。</span><span class="sxs-lookup"><span data-stu-id="6639c-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="6639c-107">主要功能</span><span class="sxs-lookup"><span data-stu-id="6639c-107">Key features</span></span>

- <span data-ttu-id="6639c-108">系統會從收據中擷取商家名稱、日期和總金額。</span><span class="sxs-lookup"><span data-stu-id="6639c-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="6639c-109">此功能會嘗試將未附加的收據與未附加的費用交易進行比對。</span><span class="sxs-lookup"><span data-stu-id="6639c-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="6639c-110">使用者可以從收據建立手動輸入的費用交易。</span><span class="sxs-lookup"><span data-stu-id="6639c-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="6639c-111">用法範例</span><span class="sxs-lookup"><span data-stu-id="6639c-111">Usage examples</span></span>

<span data-ttu-id="6639c-112">若要在建立費用報表時自動附加包含信用卡交易的收據，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="6639c-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="6639c-113">開啟 **費用管理** 工作區。</span><span class="sxs-lookup"><span data-stu-id="6639c-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="6639c-114">在 **收據** 索引標籤上，確認是否存在未附加的收據。</span><span class="sxs-lookup"><span data-stu-id="6639c-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="6639c-115">您也可以在 **收據** 索引標籤中上傳收據。</span><span class="sxs-lookup"><span data-stu-id="6639c-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="6639c-116">在 **費用** 索引標籤上，確認是否存在未附加的費用。</span><span class="sxs-lookup"><span data-stu-id="6639c-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="6639c-117">費用管理員通常會從信用卡提供者匯入這些費用。</span><span class="sxs-lookup"><span data-stu-id="6639c-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="6639c-118">選取 **新增費用報表** 。</span><span class="sxs-lookup"><span data-stu-id="6639c-118">Select **New expense report**.</span></span> <span data-ttu-id="6639c-119">請注意，現在也可以在建立費用報表時，包含費用和收據。</span><span class="sxs-lookup"><span data-stu-id="6639c-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="6639c-120">如果同時新增費用和收據，就會觸發收據與費用的自動比對。</span><span class="sxs-lookup"><span data-stu-id="6639c-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="6639c-121">若要建立費用，或從收據中比對費用，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="6639c-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="6639c-122">在費用報表的 **收據** 索引標籤上，選取 **新增收據** 以附加收據。</span><span class="sxs-lookup"><span data-stu-id="6639c-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="6639c-123">在收據的已上傳影像下方，注意 **建立** 與 **比對** 選項。</span><span class="sxs-lookup"><span data-stu-id="6639c-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="6639c-124">選取 **建立** 以建立手動輸入的費用交易，並填入從收據擷取的值。</span><span class="sxs-lookup"><span data-stu-id="6639c-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="6639c-125">如果您選取 **比對** ，系統就會嘗試將現有的費用與收據進行比對。</span><span class="sxs-lookup"><span data-stu-id="6639c-125">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="6639c-126">安裝</span><span class="sxs-lookup"><span data-stu-id="6639c-126">Installation</span></span>

<span data-ttu-id="6639c-127">此功能可與 **顛覆想像的費用報表** 功能搭配用來協助簡化費用體驗。</span><span class="sxs-lookup"><span data-stu-id="6639c-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="6639c-128">此功能僅適用於本身是沙箱與生產環境的第 2 層以上環境。</span><span class="sxs-lookup"><span data-stu-id="6639c-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="6639c-129">若要使用這些進階費用功能，請安裝 Microsoft Dynamics 365 Finance 的費用管理服務增益集，並在您的執行個體中開啟這些功能。</span><span class="sxs-lookup"><span data-stu-id="6639c-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="6639c-130">您可以從 Microsoft Dynamics Lifecycle Services (LCS) 的專案中存取增益集。</span><span class="sxs-lookup"><span data-stu-id="6639c-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="6639c-131">登入 LCS，並開啟所需的環境。</span><span class="sxs-lookup"><span data-stu-id="6639c-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="6639c-132">移至 **完整詳細資料** 。</span><span class="sxs-lookup"><span data-stu-id="6639c-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="6639c-133">選取 **維護** ，或向下捲動至 **環境增益集** 快速分頁。</span><span class="sxs-lookup"><span data-stu-id="6639c-133">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="6639c-134">選取 **安裝新的增益集** 。</span><span class="sxs-lookup"><span data-stu-id="6639c-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="6639c-135">選取 **費用管理服務** 。</span><span class="sxs-lookup"><span data-stu-id="6639c-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="6639c-136">遵循安裝指南，並同意條款及條件。</span><span class="sxs-lookup"><span data-stu-id="6639c-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="6639c-137">選取 **安裝** 。</span><span class="sxs-lookup"><span data-stu-id="6639c-137">Select **Install**.</span></span>

<span data-ttu-id="6639c-138">在 **功能管理** 工作區中，開啟下列功能：</span><span class="sxs-lookup"><span data-stu-id="6639c-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="6639c-139">重新設計的費用報表</span><span class="sxs-lookup"><span data-stu-id="6639c-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="6639c-140">自動比對並從收據建立費用</span><span class="sxs-lookup"><span data-stu-id="6639c-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="6639c-141">下列動作會在您開啟這些功能時發生：</span><span class="sxs-lookup"><span data-stu-id="6639c-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="6639c-142">現有的 **費用管理** 工作區會用新的工作區來取代。</span><span class="sxs-lookup"><span data-stu-id="6639c-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="6639c-143">新增費用欄位顯示性的新功能表項目。</span><span class="sxs-lookup"><span data-stu-id="6639c-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="6639c-144">您仍然可以開啟先前的 **費用報表** 頁面，方法是移至 **費用管理 > 我的費用 > 費用報表** 。</span><span class="sxs-lookup"><span data-stu-id="6639c-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="6639c-145">工作流程和任何核准仍會帶您進入現有的費用報表頁面。</span><span class="sxs-lookup"><span data-stu-id="6639c-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="6639c-146">收據將會透過 Microsoft Azure Cognitive Services 進行處理，並擷取和新增中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6639c-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="6639c-147">已新增選項，這個選項可讓您建立包含比對相符之未附加收據的費用報表。</span><span class="sxs-lookup"><span data-stu-id="6639c-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="6639c-148">新增至費用報表的選項會讓您從收據建立費用明細，或是會嘗試將現有收據與現有費用明細進行比對。</span><span class="sxs-lookup"><span data-stu-id="6639c-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="6639c-149">如需有關顛覆想像的費用報表功能的詳細資訊，請參閱[顛覆想像的費用報表](ExpenseWorkspaceNew.md)。</span><span class="sxs-lookup"><span data-stu-id="6639c-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6639c-150">常見問題集</span><span class="sxs-lookup"><span data-stu-id="6639c-150">Frequently asked questions</span></span>

<span data-ttu-id="6639c-151">**Microsoft 是否會將我的資料用於其模型？**</span><span class="sxs-lookup"><span data-stu-id="6639c-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="6639c-152">否，Microsoft 已經建立其收據處理服務的一般機器學習模型。</span><span class="sxs-lookup"><span data-stu-id="6639c-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="6639c-153">此模型並非根據您上傳的收據所建立。</span><span class="sxs-lookup"><span data-stu-id="6639c-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="6639c-154">**什麼地方會提供並處理此功能？**</span><span class="sxs-lookup"><span data-stu-id="6639c-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="6639c-155">目前支援美國地區。</span><span class="sxs-lookup"><span data-stu-id="6639c-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="6639c-156">**我的收據哪裡去了？**</span><span class="sxs-lookup"><span data-stu-id="6639c-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="6639c-157">Finance 會連絡 Cognitive Services 來擷取欄位資料。</span><span class="sxs-lookup"><span data-stu-id="6639c-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="6639c-158">進行處理時，Cognitive Services 會保留您的收據複本最長 24 小時。</span><span class="sxs-lookup"><span data-stu-id="6639c-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="6639c-159">完成處理後，Cognitive Services 將會移除收據。</span><span class="sxs-lookup"><span data-stu-id="6639c-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="6639c-160">收據仍然儲存在 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="6639c-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="6639c-161">如需詳細資訊，請參閱[使用表單辨識器的新功能來啟用收據瞭解](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)。</span><span class="sxs-lookup"><span data-stu-id="6639c-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
