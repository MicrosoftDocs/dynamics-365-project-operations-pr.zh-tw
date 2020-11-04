---
title: 設定和使用背靠背式供應商付款
description: 本主題說明如何建立背靠背 (Pay-When-Paid，PWP) 條款，讓您可以根據客戶付款，發放部分支付供應商的款項。
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072975"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a><span data-ttu-id="ce058-103">設定和使用背靠背式供應商付款</span><span class="sxs-lookup"><span data-stu-id="ce058-103">Set up and use pay-when-paid vendor payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce058-104">核准供應商以轉包商身分承攬工作時，您可能需要扣留支付供應商的款項，直到客戶付款給您這個專案為止。</span><span class="sxs-lookup"><span data-stu-id="ce058-104">When you approve a vendor to work as a subcontractor, you might want to withhold payment to the vendor until your customer pays you for the project.</span></span> <span data-ttu-id="ce058-105">若要支援這種案例，您可以在與供應商設定採購單 (PO) 時，設定背靠背 (PWP) 條款。</span><span class="sxs-lookup"><span data-stu-id="ce058-105">To support this scenario, you can set up pay-when-paid (PWP) terms when you set up the purchase order (PO) with the vendor.</span></span>

<span data-ttu-id="ce058-106">例如，當客戶按照專案發票的金額付款時，您可以發放部分或全部供應商發票金額。</span><span class="sxs-lookup"><span data-stu-id="ce058-106">For example, when a customer pays an amount on a project invoice, you can release some or all of the vendor invoice amount.</span></span> <span data-ttu-id="ce058-107">只需設定 PWP 條款即可，這些條款明確規定供應商要在您收到客戶支付特定百分比的相關款項之後，才會獲得付款。</span><span class="sxs-lookup"><span data-stu-id="ce058-107">Just set up PWP terms that specify that the vendor will be paid after you receive a percentage of the related payment from the customer.</span></span> <span data-ttu-id="ce058-108">如果您收到客戶部分的付款，您可以手動放行一些相關供應商發票來進行付款。</span><span class="sxs-lookup"><span data-stu-id="ce058-108">If you receive partial payment from a customer, you can manually release some of the related vendor invoices for payment.</span></span>

<span data-ttu-id="ce058-109">下列範例概述使用 PWP 條款時的程序。</span><span class="sxs-lookup"><span data-stu-id="ce058-109">The following example outlines the process when PWP terms are used.</span></span>

## <a name="example"></a><span data-ttu-id="ce058-110">範例</span><span class="sxs-lookup"><span data-stu-id="ce058-110">Example</span></span>

<span data-ttu-id="ce058-111">您的組織同意供應客戶 100 台已安裝軟體的電腦，價格為每台電腦 150.00 美元 (USD)。</span><span class="sxs-lookup"><span data-stu-id="ce058-111">Your organization agrees to provide a customer with 100 computers that have software installed, for a price of 150.00 US dollars (USD) per computer.</span></span> <span data-ttu-id="ce058-112">您接著雇用供應商，為您提供已安裝軟體的電腦。</span><span class="sxs-lookup"><span data-stu-id="ce058-112">You then hire a vendor to provide you with the computers that have software installed.</span></span> <span data-ttu-id="ce058-113">根據合約，客戶必須先認可電腦的品質，才會向您的組織付款。</span><span class="sxs-lookup"><span data-stu-id="ce058-113">According to the agreement, the customer must approve the quality of the computers before it pays your organization.</span></span> <span data-ttu-id="ce058-114">組織的原則是要在客戶付款給您以前，扣留支付供應商的款項不放。</span><span class="sxs-lookup"><span data-stu-id="ce058-114">Your organization's policy is to withhold payment to vendors until the customer has paid you.</span></span> <span data-ttu-id="ce058-115">因此，您設定專案，採用 100% 做為其 PWP 百分比。</span><span class="sxs-lookup"><span data-stu-id="ce058-115">Therefore, you set up the project so that it has a PWP percentage of 100 percent.</span></span>

<span data-ttu-id="ce058-116">供應商送交 100 台已安裝軟體的電腦給您，並附上 10,000.00 美元的發票。</span><span class="sxs-lookup"><span data-stu-id="ce058-116">The vendor sends you the 100 computers that have software installed, together with an invoice for 10,000.00 USD.</span></span> <span data-ttu-id="ce058-117">由於您的專案已設定 PWP 條款，因此您不會在收到電腦時付款給供應商。</span><span class="sxs-lookup"><span data-stu-id="ce058-117">Because PWP terms are set up for your project, you don't pay the vendor upon receipt of the computers.</span></span> <span data-ttu-id="ce058-118">反而是，您會將電腦連同 15,000.00 美元的發票一併送交客戶。</span><span class="sxs-lookup"><span data-stu-id="ce058-118">Instead, you send the computers to the customer, together with an invoice for 15,000.00.</span></span> <span data-ttu-id="ce058-119">客戶檢查電腦，並核准整筆專案發票金額。</span><span class="sxs-lookup"><span data-stu-id="ce058-119">The customer inspects the computers and approves the full amount of the project invoice.</span></span>

<span data-ttu-id="ce058-120">收到客戶的全部付款之後，您支付供應商 10,000.00 美元，即供應商發票的全額。</span><span class="sxs-lookup"><span data-stu-id="ce058-120">After you receive the full payment from the customer, you pay the vendor 10,000.00, the full amount of the vendor invoice.</span></span>

## <a name="set-up-pwp-terms-for-a-project"></a><span data-ttu-id="ce058-121">設定專案的 PWP 條款</span><span class="sxs-lookup"><span data-stu-id="ce058-121">Set up PWP terms for a project</span></span>

<span data-ttu-id="ce058-122">為專案設定 PWP 條款時，您必須以百分比指定供應商在獲得您付款之前，必須先就此專案支付給您的最低金額。</span><span class="sxs-lookup"><span data-stu-id="ce058-122">When you set up PWP terms for a project, you must specify, as a percentage, the minimum amount that a customer must pay you for the project before you will pay the vendor.</span></span> <span data-ttu-id="ce058-123">系統會在專案的客戶發票上自動計算閾值金額。</span><span class="sxs-lookup"><span data-stu-id="ce058-123">The threshold amount is automatically calculated on the customer invoices for the project.</span></span> <span data-ttu-id="ce058-124">依照下列步驟，設定 PWP 條款的閾值百分比。</span><span class="sxs-lookup"><span data-stu-id="ce058-124">Follow these steps to set up the threshold percentage for PWP terms.</span></span>

1. <span data-ttu-id="ce058-125">移至 **專案管理與會計** \> **專案** \> **所有專案** 。</span><span class="sxs-lookup"><span data-stu-id="ce058-125">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="ce058-126">尋找並開啟需要設定 PWP 條款的專案。</span><span class="sxs-lookup"><span data-stu-id="ce058-126">Find and open the project that you want to set up PWP terms for.</span></span>
3. <span data-ttu-id="ce058-127">在 **供應商合約** 快速分頁中，選取 **新增明細** 。</span><span class="sxs-lookup"><span data-stu-id="ce058-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="ce058-128">在 **客戶代碼** 欄位中，選取下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="ce058-128">In the **Account code** field, select one of the following options:</span></span>

    - <span data-ttu-id="ce058-129">**表格** – PWP 條款適用於單一供應商。</span><span class="sxs-lookup"><span data-stu-id="ce058-129">**Table** – The PWP terms apply to a single vendor.</span></span>
    - <span data-ttu-id="ce058-130">**群組** – PWP 條款適用於供應商群組中的所有供應商。</span><span class="sxs-lookup"><span data-stu-id="ce058-130">**Group** – The PWP terms apply to all vendors in a vendor group.</span></span>
    - <span data-ttu-id="ce058-131">**全部** – PWP 條款適用於所有供應商。</span><span class="sxs-lookup"><span data-stu-id="ce058-131">**All** – The PWP terms apply to all vendors.</span></span>

4. <span data-ttu-id="ce058-132">如果您在上一個步驟中選取 **表格** 或 **群組** ，請在 **供應商/供應商群組** 欄位中，選取適用 PWP 條款的供應商或供應商群組。</span><span class="sxs-lookup"><span data-stu-id="ce058-132">If you selected **Table** or **Group** in the previous step, in the **Vendor/Vendor group** field, select the vendor or vendor group that the PWP terms apply to.</span></span> <span data-ttu-id="ce058-133">如果在上一個步驟中選取 **全部** ，則無法編輯 **供應商/供應商群組** 欄位。</span><span class="sxs-lookup"><span data-stu-id="ce058-133">If you selected **All** in the previous step, the **Vendor/Vendor group** field can't be edited.</span></span>
5. <span data-ttu-id="ce058-134">如果專案中的供應商已設定供應商保留條款，請在 **供應商保留條款** 欄位中，選取保留條款的規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce058-134">If vendor retention terms are set up for the vendor in the project, in the **Vendor retention terms** field, select the rule ID for the retention terms.</span></span>
6. <span data-ttu-id="ce058-135">在 **PWP 閾值百分比** 欄位中，輸入專案的閾值百分比。</span><span class="sxs-lookup"><span data-stu-id="ce058-135">In the **PWP threshold percentage** field, enter the threshold percentage for the project.</span></span> <span data-ttu-id="ce058-136">您為專案輸入的百分比會定義客戶在您付款給供應商之前，必須先支付給您的最低金額。</span><span class="sxs-lookup"><span data-stu-id="ce058-136">The percentage that you enter for the project defines the minimum amount that the customer must pay you before you will pay the vendor.</span></span>

## <a name="create-a-po-that-has-pwp-terms"></a><span data-ttu-id="ce058-137">建立有 PWP 條款的 PO</span><span class="sxs-lookup"><span data-stu-id="ce058-137">Create a PO that has PWP terms</span></span>

<span data-ttu-id="ce058-138">當您將供應商的發票過帳時，如果此供應商須遵守 PWP 條款，這些條款就會顯示在 PO 明細上。</span><span class="sxs-lookup"><span data-stu-id="ce058-138">When you post an invoice from a vendor, if the vendor is subject to PWP terms, those terms are shown on the PO lines.</span></span> <span data-ttu-id="ce058-139">若要建立有 PWP 條款的 PO，請依照下列步驟進行。</span><span class="sxs-lookup"><span data-stu-id="ce058-139">To create a PO that has PWP terms, follow these steps.</span></span>

1. <span data-ttu-id="ce058-140">移至 **採購和委外** \> **採購單** \> **所有採購單** 。</span><span class="sxs-lookup"><span data-stu-id="ce058-140">Go to **Procurement and sourcing** \> **Purchase orders** \> **All purchase orders**.</span></span>
2. <span data-ttu-id="ce058-141">在動作窗格上，選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="ce058-141">On the Action Pane, select **New**.</span></span> <span data-ttu-id="ce058-142">接著在 **建立採購單** 對話方塊中輸入必要資訊，然後選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="ce058-142">Then, in the **Create purchase order** dialog box, enter the required information, and select **OK**.</span></span>

    <span data-ttu-id="ce058-143">或者，開啟 **所有採購單** 清單頁面上現有的 PO。</span><span class="sxs-lookup"><span data-stu-id="ce058-143">Alternatively, open an existing PO on the **All purchase orders** list page.</span></span>

4. <span data-ttu-id="ce058-144">在 **採購單** 頁面的 **採購單明細** 快速分頁上，檢閱供應商的採購單明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ce058-144">On the **Purchase order** page, on the **Purchase order lines** FastTab, review the details of the PO line for the vendor.</span></span> <span data-ttu-id="ce058-145">系統會自動選取 **背靠背** 選項，並且自動從 **專案** 頁面的 **PWP 閾值百分比** 欄位複製 **PWP 閾值百分比** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="ce058-145">The **Pay when paid** option is automatically selected, and the value in the **PWP threshold percentage** field is automatically copied from the **PWP threshold percentage** field on the **Projects** page.</span></span>
6. <span data-ttu-id="ce058-146">如果不想要將 PWP 條款套用至 PO 明細的供應商，請清除 **背靠背** 選項。</span><span class="sxs-lookup"><span data-stu-id="ce058-146">If you don't want to apply PWP terms to the vendor for a PO line, clear the **Pay when paid** option.</span></span> <span data-ttu-id="ce058-147">在這種情況下，PO 明細的 **PWP 閾值百分比** 欄位會重設為 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="ce058-147">In this case, the **PWP threshold percentage** field for the PO line will be reset to 0 (zero).</span></span>

## <a name="update-a-customer-payment-and-pay-the-vendor"></a><span data-ttu-id="ce058-148">更新客戶付款並支付供應商款項</span><span class="sxs-lookup"><span data-stu-id="ce058-148">Update a customer payment and pay the vendor</span></span>

<span data-ttu-id="ce058-149">當供應商完成專案的工作並傳送發票給您時，您必須審查專案狀態和客戶發票，以判斷是否已符合專案的 PWP 條款。</span><span class="sxs-lookup"><span data-stu-id="ce058-149">When a vendor completes its work on a project and sends you an invoice, you must review the project status and customer invoices to determine whether the PWP terms have been met for the project.</span></span> <span data-ttu-id="ce058-150">如果供應商已符合 PWP 條款，您可以根據專案的客戶付款，判斷要支付供應商發票上的哪些明細。</span><span class="sxs-lookup"><span data-stu-id="ce058-150">If the PWP terms for the vendor were met, you can determine which lines on the vendor invoice to pay, based on the customer payments for the project.</span></span> <span data-ttu-id="ce058-151">如果您決定即使未符合 PWP 條款，也要支付供應商款項，則可以在 **背靠背式供應商發票** 頁面上覆寫 PWP 條款。</span><span class="sxs-lookup"><span data-stu-id="ce058-151">If you decide to pay the vendor even though the PWP terms weren't met, you can override the PWP terms on the **Vendor invoice with pay when paid** page.</span></span>

1. <span data-ttu-id="ce058-152">移至 **專案管理與會計** \> **查詢與報表** \> **保留額查詢** \> **背靠背式供應商發票** 。</span><span class="sxs-lookup"><span data-stu-id="ce058-152">Go to **Project management and accounting** \> **Inquiries and reports** \> **Retention inquiries** \> **Vendor invoice with pay when paid**.</span></span>
2. <span data-ttu-id="ce058-153">在 **背靠背式供應商發票** 頁面的搜尋欄位中，輸入值以尋找您要審查的供應商發票，然後選取 **搜尋** 。</span><span class="sxs-lookup"><span data-stu-id="ce058-153">On the **Vendor invoices with pay when paid** page, in the search field, enter values to find the vendor invoice that you want to review, and then select **Search**.</span></span>
3. <span data-ttu-id="ce058-154">在 **供應商發票明細** 快速分頁上，選取您要變更的明細。</span><span class="sxs-lookup"><span data-stu-id="ce058-154">On the **Vendor invoice lines** FastTab, select the lines that you want to change.</span></span>
4. <span data-ttu-id="ce058-155">如果符合發票明細的 **背靠背** 條件，請選取 **發放支付供應商的款項** 。</span><span class="sxs-lookup"><span data-stu-id="ce058-155">If the **Pay when paid** conditions are met for the invoice line, select **Release vendor payment**.</span></span> <span data-ttu-id="ce058-156">**背靠背** 選項已清除，且 **付款準備就緒** 欄位的值已變更為 **是** 。</span><span class="sxs-lookup"><span data-stu-id="ce058-156">The **Pay when paid** option is cleared, and the value of the **Ready for payment** field is changed to **Yes**.</span></span>
