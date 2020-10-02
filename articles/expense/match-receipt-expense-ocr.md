---
title: 使用 OCR 來比對收據與費用
description: 本主題提供有關使用光學字元辨識 (OCR) 處理收據的資訊。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896991"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="552e8-103">使用 OCR 來比對收據與費用</span><span class="sxs-lookup"><span data-stu-id="552e8-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="552e8-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="552e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="552e8-105">費用項目因採用光學字元辨識 (OCR) 處理收據而有所增強。</span><span class="sxs-lookup"><span data-stu-id="552e8-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="552e8-106">此功能是專為改善使用者建立費用報表時的體驗而設計。</span><span class="sxs-lookup"><span data-stu-id="552e8-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="552e8-107">主要功能</span><span class="sxs-lookup"><span data-stu-id="552e8-107">Key features</span></span>

- <span data-ttu-id="552e8-108">系統會從收據中擷取商家名稱、日期和總金額。</span><span class="sxs-lookup"><span data-stu-id="552e8-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="552e8-109">系統會嘗試將未附加的收據與未附加的費用交易進行比對。</span><span class="sxs-lookup"><span data-stu-id="552e8-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="552e8-110">您可以從收據建立手動輸入的費用交易。</span><span class="sxs-lookup"><span data-stu-id="552e8-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="552e8-111">將收據附加至費用報表</span><span class="sxs-lookup"><span data-stu-id="552e8-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="552e8-112">若要在建立費用報表時自動附加包含信用卡交易的收據，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="552e8-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="552e8-113">開啟**費用管理**工作區。</span><span class="sxs-lookup"><span data-stu-id="552e8-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="552e8-114">在**收據**索引標籤上，確認是否存在未附加的收據。</span><span class="sxs-lookup"><span data-stu-id="552e8-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="552e8-115">您也可以在**收據**索引標籤中上傳收據。</span><span class="sxs-lookup"><span data-stu-id="552e8-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="552e8-116">在**費用**索引標籤上，確認是否存在未附加的費用。</span><span class="sxs-lookup"><span data-stu-id="552e8-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="552e8-117">費用管理員通常會從信用卡提供者匯入這些費用。</span><span class="sxs-lookup"><span data-stu-id="552e8-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="552e8-118">選取**新增費用報表**。</span><span class="sxs-lookup"><span data-stu-id="552e8-118">Select **New expense report**.</span></span> <span data-ttu-id="552e8-119">請注意，現在也可以在建立費用報表時，包含費用和收據。</span><span class="sxs-lookup"><span data-stu-id="552e8-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="552e8-120">如果同時新增費用和收據，就會觸發收據與費用的自動比對。</span><span class="sxs-lookup"><span data-stu-id="552e8-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="552e8-121">建立或比對費用報表的收據</span><span class="sxs-lookup"><span data-stu-id="552e8-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="552e8-122">若要建立費用，或從收據中比對費用，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="552e8-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="552e8-123">在費用報表的**收據**索引標籤上，選取**新增收據**以附加收據。</span><span class="sxs-lookup"><span data-stu-id="552e8-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="552e8-124">在收據的已上傳影像下方，注意**建立**與**比對**選項。</span><span class="sxs-lookup"><span data-stu-id="552e8-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="552e8-125">選取**建立**以建立手動輸入的費用交易，並填入從收據擷取的值。</span><span class="sxs-lookup"><span data-stu-id="552e8-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="552e8-126">如果您選取**比對**，系統就會嘗試將現有的費用與收據進行比對。</span><span class="sxs-lookup"><span data-stu-id="552e8-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="552e8-127">安裝</span><span class="sxs-lookup"><span data-stu-id="552e8-127">Installation</span></span>

<span data-ttu-id="552e8-128">若要使用這些進階費用功能，請安裝 Microsoft Dynamics 365 Finance 的費用管理服務增益集，並在您的執行個體中開啟這些功能。</span><span class="sxs-lookup"><span data-stu-id="552e8-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="552e8-129">您可以從 Microsoft Dynamics Lifecycle Services (LCS) 的專案中存取增益集。</span><span class="sxs-lookup"><span data-stu-id="552e8-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="552e8-130">登入 LCS，並開啟所需的環境。</span><span class="sxs-lookup"><span data-stu-id="552e8-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="552e8-131">移至**完整詳細資料**。</span><span class="sxs-lookup"><span data-stu-id="552e8-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="552e8-132">選取**維護**，或向下捲動至**環境增益集**快速分頁。</span><span class="sxs-lookup"><span data-stu-id="552e8-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="552e8-133">選取**安裝新的增益集**。</span><span class="sxs-lookup"><span data-stu-id="552e8-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="552e8-134">選取**費用管理服務**。</span><span class="sxs-lookup"><span data-stu-id="552e8-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="552e8-135">遵循安裝指南，並同意條款及條件。</span><span class="sxs-lookup"><span data-stu-id="552e8-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="552e8-136">選取**安裝**。</span><span class="sxs-lookup"><span data-stu-id="552e8-136">Select **Install**.</span></span>

<span data-ttu-id="552e8-137">在**功能管理**工作區中，開啟下列功能：</span><span class="sxs-lookup"><span data-stu-id="552e8-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="552e8-138">重新設計的費用報表</span><span class="sxs-lookup"><span data-stu-id="552e8-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="552e8-139">自動比對並從收據建立費用</span><span class="sxs-lookup"><span data-stu-id="552e8-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="552e8-140">下列動作會在您開啟這些功能時發生：</span><span class="sxs-lookup"><span data-stu-id="552e8-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="552e8-141">現有的**費用管理**工作區會用新的工作區來取代。</span><span class="sxs-lookup"><span data-stu-id="552e8-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="552e8-142">新增費用欄位顯示性的新功能表項目。</span><span class="sxs-lookup"><span data-stu-id="552e8-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="552e8-143">您仍然可以開啟先前的**費用報表**頁面，方法是移至**費用管理 > 我的費用 > 費用報表**。</span><span class="sxs-lookup"><span data-stu-id="552e8-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="552e8-144">工作流程和任何核准仍會帶您進入現有的費用報表頁面。</span><span class="sxs-lookup"><span data-stu-id="552e8-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="552e8-145">收據將會透過 Microsoft Azure Cognitive Services 進行處理，並擷取和新增中繼資料。</span><span class="sxs-lookup"><span data-stu-id="552e8-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="552e8-146">已新增選項，這個選項可讓您建立包含比對相符之未附加收據的費用報表。</span><span class="sxs-lookup"><span data-stu-id="552e8-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="552e8-147">新增至費用報表的選項會讓您從收據建立費用明細，或是會嘗試將現有收據與現有費用明細進行比對。</span><span class="sxs-lookup"><span data-stu-id="552e8-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="552e8-148">常見問題集</span><span class="sxs-lookup"><span data-stu-id="552e8-148">Frequently asked questions</span></span>

<span data-ttu-id="552e8-149">**Microsoft 是否會將我的資料用於其模型？**</span><span class="sxs-lookup"><span data-stu-id="552e8-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="552e8-150">否，Microsoft 已經建立其收據處理服務的一般機器學習模型。</span><span class="sxs-lookup"><span data-stu-id="552e8-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="552e8-151">此模型並非根據您上傳的收據所建立。</span><span class="sxs-lookup"><span data-stu-id="552e8-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="552e8-152">**什麼地方會提供並處理此功能？**</span><span class="sxs-lookup"><span data-stu-id="552e8-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="552e8-153">目前支援美國地區。</span><span class="sxs-lookup"><span data-stu-id="552e8-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="552e8-154">**我的收據哪裡去了？**</span><span class="sxs-lookup"><span data-stu-id="552e8-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="552e8-155">Finance 會連絡 Cognitive Services 來擷取欄位資料。</span><span class="sxs-lookup"><span data-stu-id="552e8-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="552e8-156">進行處理時，Cognitive Services 會保留您的收據複本最長 24 小時。</span><span class="sxs-lookup"><span data-stu-id="552e8-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="552e8-157">完成處理後，Cognitive Services 將會移除收據。</span><span class="sxs-lookup"><span data-stu-id="552e8-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="552e8-158">收據仍然儲存在 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="552e8-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="552e8-159">如需詳細資訊，請參閱[使用表單辨識器的新功能來啟用收據瞭解](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)。</span><span class="sxs-lookup"><span data-stu-id="552e8-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
