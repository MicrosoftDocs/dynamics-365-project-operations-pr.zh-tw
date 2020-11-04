---
title: 根據進度扣款的預付型合約
description: 本主題說明如何建立專案合約，讓您可以根據已完成工作的百分比產生客戶的發票。
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073125"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="56692-103">根據進度扣款的預付型合約</span><span class="sxs-lookup"><span data-stu-id="56692-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="56692-104">本主題說明如何建立專案合約，讓您可以根據已完成工作的百分比建立客戶的發票。</span><span class="sxs-lookup"><span data-stu-id="56692-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="56692-105">系統會針對您為專案設定之工作的預算類別自動計算發票金額。</span><span class="sxs-lookup"><span data-stu-id="56692-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="56692-106">當您與客戶議定專案合約時，會設定開立發票的時機。</span><span class="sxs-lookup"><span data-stu-id="56692-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="56692-107">請使用此主題中的程序，來設定合約、相關聯專案以及針對您為專案設定之工作預算類別計算發票金額的帳單規則。</span><span class="sxs-lookup"><span data-stu-id="56692-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="56692-108">建立合約與專案之後，您可以設定專案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="56692-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="56692-109">例如，您可以定義活動，並將工作者指派至專案。</span><span class="sxs-lookup"><span data-stu-id="56692-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="56692-110">範例</span><span class="sxs-lookup"><span data-stu-id="56692-110">Example</span></span>

<span data-ttu-id="56692-111">您的組織是軟體開發公司。</span><span class="sxs-lookup"><span data-stu-id="56692-111">Your organization is a software development firm.</span></span> <span data-ttu-id="56692-112">您同意為客戶開發薪資會計套件，總計服務費為 20,000 美元 (USD)。</span><span class="sxs-lookup"><span data-stu-id="56692-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="56692-113">您的組織同意在您完成專案的特定百分比時，向客戶開立發票。</span><span class="sxs-lookup"><span data-stu-id="56692-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="56692-114">您為工作設定下列專案類別，以便用於帳單處理程序：</span><span class="sxs-lookup"><span data-stu-id="56692-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="56692-115">諮詢</span><span class="sxs-lookup"><span data-stu-id="56692-115">Consulting</span></span>
- <span data-ttu-id="56692-116">設計</span><span class="sxs-lookup"><span data-stu-id="56692-116">Design</span></span>
- <span data-ttu-id="56692-117">安裝</span><span class="sxs-lookup"><span data-stu-id="56692-117">Installation</span></span>

<span data-ttu-id="56692-118">您還設定了帳單規則，這些規則會自動針對每個類別中已完成的專案工作百分比計算發票金額。</span><span class="sxs-lookup"><span data-stu-id="56692-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="56692-119">預算經理會為專案類別建立預算。</span><span class="sxs-lookup"><span data-stu-id="56692-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="56692-120">已完成工作的金額是依照實際工作相對於預算金額的百分比自動計算得出。</span><span class="sxs-lookup"><span data-stu-id="56692-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="56692-121">先決條件</span><span class="sxs-lookup"><span data-stu-id="56692-121">Prerequisites</span></span>

<span data-ttu-id="56692-122">建立使用帳單規則的專案之前，您必須設定帳單規則的編號序列，以及用於過帳按進度扣款帳單的服務費日記帳。</span><span class="sxs-lookup"><span data-stu-id="56692-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="56692-123">移至 **專案管理與會計** \> **設定** \> **專案管理與會計參數** 。</span><span class="sxs-lookup"><span data-stu-id="56692-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="56692-124">在 **專案管理與會計參數** 頁面的 **編號序列** 索引標籤中，設定您要在建立帳單規則時使用的編號序列。</span><span class="sxs-lookup"><span data-stu-id="56692-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="56692-125">移至 **專案管理與會計** \> **帳目** \> **服務費** 。</span><span class="sxs-lookup"><span data-stu-id="56692-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="56692-126">在 **服務費日記帳** 頁面上，選取 **新增** ，然後輸入日記帳名稱。</span><span class="sxs-lookup"><span data-stu-id="56692-126">On the **Fee journal** page, select **New** , and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="56692-127">建立按進度扣款帳單的合約</span><span class="sxs-lookup"><span data-stu-id="56692-127">Create a contract for progress billings</span></span>

<span data-ttu-id="56692-128">使用此程序來建立固定價格專案的專案合約。</span><span class="sxs-lookup"><span data-stu-id="56692-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="56692-129">您會在專案上已完成的工作達到指定的百分比時建立專案發票。</span><span class="sxs-lookup"><span data-stu-id="56692-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="56692-130">移至 **專案管理與會計** \> **專案** \> **專案合約** 。</span><span class="sxs-lookup"><span data-stu-id="56692-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="56692-131">在 **專案合約** 頁面上，選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="56692-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="56692-132">在 **新增專案合約** 對話方塊中，設定下列欄位：</span><span class="sxs-lookup"><span data-stu-id="56692-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="56692-133">**名稱**</span><span class="sxs-lookup"><span data-stu-id="56692-133">**Name**</span></span>
    - <span data-ttu-id="56692-134">**資金類型**</span><span class="sxs-lookup"><span data-stu-id="56692-134">**Funding type**</span></span>
    - <span data-ttu-id="56692-135">**資金來源**</span><span class="sxs-lookup"><span data-stu-id="56692-135">**Funding source**</span></span>
    - <span data-ttu-id="56692-136">**銷售貨幣** – 與專案合約相關聯的客戶發票預設會此貨幣。</span><span class="sxs-lookup"><span data-stu-id="56692-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="56692-137">不過，您可以變更特定客戶發票上使用的銷售貨幣。</span><span class="sxs-lookup"><span data-stu-id="56692-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="56692-138">選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="56692-138">Select **OK**.</span></span> <span data-ttu-id="56692-139">此資訊會複製到 **專案合約** 頁面的標題中。</span><span class="sxs-lookup"><span data-stu-id="56692-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="56692-140">在 **專案合約** 頁面上，填入專案其餘的必要資訊。</span><span class="sxs-lookup"><span data-stu-id="56692-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="56692-141">建立按進度扣款帳單的專案</span><span class="sxs-lookup"><span data-stu-id="56692-141">Create a project for progress billings</span></span>

<span data-ttu-id="56692-142">依照下列步驟建立專案，以及任何與專案合約相關聯的子專案。</span><span class="sxs-lookup"><span data-stu-id="56692-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="56692-143">移至 **專案管理與會計** \> **專案** \> **所有專案** 。</span><span class="sxs-lookup"><span data-stu-id="56692-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="56692-144">在 **所有專案** 頁面上，選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="56692-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="56692-145">在 **新增專案** 對話方塊的 **專案類型** 欄位中，選取 **時間和材料** 。</span><span class="sxs-lookup"><span data-stu-id="56692-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="56692-146">選取專案群組。</span><span class="sxs-lookup"><span data-stu-id="56692-146">Select a project group.</span></span> <span data-ttu-id="56692-147">專案群組定義指派至群組之專案的過帳資訊。</span><span class="sxs-lookup"><span data-stu-id="56692-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="56692-148">選取 **建立專案** 。</span><span class="sxs-lookup"><span data-stu-id="56692-148">Select **Create project**.</span></span>
6. <span data-ttu-id="56692-149">建立專案之後，將專案階段設定為 **進行中** 。</span><span class="sxs-lookup"><span data-stu-id="56692-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="56692-150">建立專案的預算</span><span class="sxs-lookup"><span data-stu-id="56692-150">Create a budget for a project</span></span>

<span data-ttu-id="56692-151">預算類別會用來自動針對每個類別所完成的工作百分比計算發票金額。</span><span class="sxs-lookup"><span data-stu-id="56692-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="56692-152">依照下列步驟，建立估計成本的預算類別。</span><span class="sxs-lookup"><span data-stu-id="56692-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="56692-153">移至 **專案管理與會計** \> **專案** \> **所有專案** 。</span><span class="sxs-lookup"><span data-stu-id="56692-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="56692-154">在 **所有專案** 頁面上，選取並開啟您想要的專案。</span><span class="sxs-lookup"><span data-stu-id="56692-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="56692-155">在 **專案** 頁面動作窗格的 **計畫** 索引標籤上，選取 **預算** 群組中的 **專案預算** 。</span><span class="sxs-lookup"><span data-stu-id="56692-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="56692-156">在 **專案預算** 頁面上，輸入專案中每個類別的估計成本。</span><span class="sxs-lookup"><span data-stu-id="56692-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="56692-157">建立按進度扣款帳單的帳單規則</span><span class="sxs-lookup"><span data-stu-id="56692-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="56692-158">移至 **專案管理與會計** \> **專案** \> **專案合約** 。</span><span class="sxs-lookup"><span data-stu-id="56692-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="56692-159">在 **專案合約** 頁面上，選取並開啟專案合約。</span><span class="sxs-lookup"><span data-stu-id="56692-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="56692-160">在該專案合約頁面的 **帳單規則** 快速分頁中，選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="56692-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="56692-161">在 **帳單規則** 頁面的 **明細類型** 欄位中，選取 **進度** 。</span><span class="sxs-lookup"><span data-stu-id="56692-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="56692-162">在 **帳單規則明細詳細資料** 快速分頁的 **合約值** 欄位中，輸入合約的總值。</span><span class="sxs-lookup"><span data-stu-id="56692-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="56692-163">在 **類別** 欄位中，選取要將服務費交易過帳到的類別。</span><span class="sxs-lookup"><span data-stu-id="56692-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="56692-164">在 **專案** 欄位中，選取使用此帳單規則的專案。</span><span class="sxs-lookup"><span data-stu-id="56692-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="56692-165">選用：將帳單規則另外指派至其他專案。</span><span class="sxs-lookup"><span data-stu-id="56692-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="56692-166">在 **專案** 快速分頁的 **可用專案** 區段中，選取專案，然後選取向右箭頭按鈕以將專案新增至 **選取的專案** 區段中。</span><span class="sxs-lookup"><span data-stu-id="56692-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="56692-167">選用：計算客戶從發票支付款項扣留的百分比金額。</span><span class="sxs-lookup"><span data-stu-id="56692-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="56692-168">在 **付款保留條款** 快速分頁中，選取資金來源，然後在 **保留百分比** 欄位中輸入保留百分比。</span><span class="sxs-lookup"><span data-stu-id="56692-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="56692-169">重複上述步驟，建立專案合約的其他帳單規則。</span><span class="sxs-lookup"><span data-stu-id="56692-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
