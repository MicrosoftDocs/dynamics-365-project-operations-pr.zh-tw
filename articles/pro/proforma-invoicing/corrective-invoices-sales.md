---
title: 專案更正發票
description: 本主題提供有關如何在 Project Operations 中建立和確認更正發票的資訊。
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866581"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="9b468-103">專案更正發票</span><span class="sxs-lookup"><span data-stu-id="9b468-103">Corrective project invoices</span></span>

<span data-ttu-id="9b468-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="9b468-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9b468-105">確認過的專案發票可進行更正以處理與客戶及專案經理議定的變更或貸記。</span><span class="sxs-lookup"><span data-stu-id="9b468-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="9b468-106">若要對已確認的發票進行編輯，請開啟已確認的發票，然後選取 **更正此發票**。</span><span class="sxs-lookup"><span data-stu-id="9b468-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="9b468-107">除非專案發票已確認，否則不提供此選取項目。</span><span class="sxs-lookup"><span data-stu-id="9b468-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="9b468-108">新的草稿發票會從已確認的發票中建立。</span><span class="sxs-lookup"><span data-stu-id="9b468-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="9b468-109">所有來自先前已確認發票的發票明細詳細資料都會複製到新的草稿中。</span><span class="sxs-lookup"><span data-stu-id="9b468-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="9b468-110">以下是了解新更正發票中明細詳細資訊的一些要點：</span><span class="sxs-lookup"><span data-stu-id="9b468-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="9b468-111">所有數量都會更新為零。</span><span class="sxs-lookup"><span data-stu-id="9b468-111">All quantities are updated to zero.</span></span> <span data-ttu-id="9b468-112">應用程式假設所有已開發票的項目都已完全貸記。</span><span class="sxs-lookup"><span data-stu-id="9b468-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="9b468-113">如有需要，您可以手動更新這些數量以反映要開立發票的數量，而不是貸記的數量。</span><span class="sxs-lookup"><span data-stu-id="9b468-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="9b468-114">應用程式會根據您輸入的數量，計算貸記的數量。</span><span class="sxs-lookup"><span data-stu-id="9b468-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="9b468-115">此金額會反映在確認更正後發票時所建立的實際值中。</span><span class="sxs-lookup"><span data-stu-id="9b468-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="9b468-116">如果您要對稅金金額進行變更，就必須輸入正確的稅額，而不是貸記的稅額。</span><span class="sxs-lookup"><span data-stu-id="9b468-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="9b468-117">不會複製先前已確認的產品型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="9b468-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="9b468-118">不支援處理對產品型專案發票的更正。</span><span class="sxs-lookup"><span data-stu-id="9b468-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="9b468-119">里程碑更正一律以完全貸記的方式處理。</span><span class="sxs-lookup"><span data-stu-id="9b468-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="9b468-120">如果開立了金額不正確的發票給客戶，則可以更正保留款或預付金的金額。</span><span class="sxs-lookup"><span data-stu-id="9b468-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="9b468-121">如果使用了不正確的金額對先前已確認發票上的收費進行協調，則可以更正保留款及預付金的對帳單。</span><span class="sxs-lookup"><span data-stu-id="9b468-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b468-122">對其他已開發行票的收費做更正的發票明細詳細資料，其 **更正** 欄位會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="9b468-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="9b468-123">已更正發票明細詳細資料的發票具有名為 **有更正** 的欄位，此欄位也會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="9b468-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="9b468-124">確認更正發票時所建立的實際值</span><span class="sxs-lookup"><span data-stu-id="9b468-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="9b468-125">下表列出在確認更正發票時所建立的實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9b468-126">
                    <strong>案例</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b468-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9b468-127">
                    <strong>確認時建立的實際值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b468-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="9b468-128">確認已開發票預付金或保留款的更正。<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b468-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-129">為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9b468-130">此金額為正數，因為這是要用來抵消開立保留款或預付金發票時所建立的負數金額。</span><span class="sxs-lookup"><span data-stu-id="9b468-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-131">已開單銷售沖銷是針對保留款或預付金的金額建立來沖銷原始已開單銷售。</span><span class="sxs-lookup"><span data-stu-id="9b468-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-132">新的已開單銷售實際值是針對根據保留款或預付金更正之發票明細的更正金額所建立。</span><span class="sxs-lookup"><span data-stu-id="9b468-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-133">根據保留款或預付金更正之發票明細金額為負數的未開單銷售實際值，用於協調對帳差異。</span><span class="sxs-lookup"><span data-stu-id="9b468-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="9b468-134">對先前已協調保留款或預付金的更正確認。</span><span class="sxs-lookup"><span data-stu-id="9b468-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-135">為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9b468-136">此金額為正數，要用來抵消先前進行對帳差異協調時所建立的負數金額。</span><span class="sxs-lookup"><span data-stu-id="9b468-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-137">先前發票金額的已開單銷售沖銷實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-138">套用於更正後發票之已更正保留款金額的新開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-139">更正後剩餘保留款或預付金為負數金額的未開單銷售實際值，這會用來對後來的發票進行對帳差異協調。</span><span class="sxs-lookup"><span data-stu-id="9b468-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b468-140">對先前已開發票的時間交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="9b468-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-141">原始時間發票明細詳細資料上時數及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-142">原始時間發票明細詳細資料上時數及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9b468-143">對時間交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="9b468-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-144">原始時間發票明細詳細資料上已開發票時數及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-145">應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-146">應按照扣減發票明細詳細資料上已更正數字後剩餘時數及金額收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b468-147">對先前已開發票的費用交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="9b468-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-148">原始費用發票明細詳細資料上數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-149">原始費用發票明細詳細資料上數量及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9b468-150">對先前已開發票的費用交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="9b468-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-151">原始費用發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-152">應按照更正後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-153">應按照扣減發票明細詳細資料上已更正數字後剩餘數量及金額收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b468-154">開立先前已開發票材料交易的全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="9b468-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-155">材料原始發票明細詳細資料上數量和金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-156">材料原始發票明細詳細資料上數量和金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9b468-157">開立物料交易的部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="9b468-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-158">材料原始發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-159">對已編輯發票明細詳細資料、該項沖銷和等額已開單銷售實際值上數量和金額應收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-160">應按照扣減發票明細詳細資料上已更正數字後剩餘數量及金額收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b468-161">對先前已開發票的服務費交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="9b468-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-162">原始服務費發票明細詳細資料上數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-163">原始服務費發票明細詳細資料上數量及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b468-164">對先前已開發票的服務費交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="9b468-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-165">原始服務費發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-166">應按照編輯後更正發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="9b468-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9b468-167">對先前已開發票的里程碑交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="9b468-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-168">原始里程碑發票明細詳細資料上金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="9b468-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="9b468-169">里程碑的發票狀態已從<b>客戶發票已過帳</b>更新為<b>已準備好開立發票</b>。</span><span class="sxs-lookup"><span data-stu-id="9b468-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9b468-170">對先前已開發票的里程碑交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="9b468-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-171">不支援</span><span class="sxs-lookup"><span data-stu-id="9b468-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9b468-172">先前已開發票產品型合約服務內容的貸記和更正。</span><span class="sxs-lookup"><span data-stu-id="9b468-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9b468-173">不支援</span><span class="sxs-lookup"><span data-stu-id="9b468-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
