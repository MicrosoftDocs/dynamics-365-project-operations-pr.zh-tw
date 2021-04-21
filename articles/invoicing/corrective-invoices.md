---
title: 建立專案型更正發票
description: 本主題提供有關在 Project Operations 中更正發票的資訊。
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788838"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="efa20-103">建立專案型更正發票</span><span class="sxs-lookup"><span data-stu-id="efa20-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="efa20-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="efa20-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="efa20-105">確認過的專案發票可進行更正以處理與客戶及專案經理議定的變更或貸記。</span><span class="sxs-lookup"><span data-stu-id="efa20-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="efa20-106">若要對已確認的發票進行編輯，請開啟已確認的發票，然後選取 **更正此發票**。</span><span class="sxs-lookup"><span data-stu-id="efa20-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="efa20-107">除非專案發票已確認，否則不提供此選取項目。</span><span class="sxs-lookup"><span data-stu-id="efa20-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="efa20-108">新的草稿發票會從已確認的發票中建立。</span><span class="sxs-lookup"><span data-stu-id="efa20-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="efa20-109">所有來自先前已確認發票的發票明細詳細資料都會複製到新的草稿中。</span><span class="sxs-lookup"><span data-stu-id="efa20-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="efa20-110">以下是一些要點，有助於深入了解新的更正發票上的明細詳細資料：</span><span class="sxs-lookup"><span data-stu-id="efa20-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="efa20-111">所有數量都會更新為零。</span><span class="sxs-lookup"><span data-stu-id="efa20-111">All quantities are updated to zero.</span></span> <span data-ttu-id="efa20-112">這假設所有已開立發票的項目都已全額貸記。</span><span class="sxs-lookup"><span data-stu-id="efa20-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="efa20-113">如有需要，您可以手動更新這些數量以反映要開立發票的數量，而不是貸記的數量。</span><span class="sxs-lookup"><span data-stu-id="efa20-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="efa20-114">應用程式會根據您輸入的數量，計算貸記的數量。</span><span class="sxs-lookup"><span data-stu-id="efa20-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="efa20-115">此金額會反映在確認更正後發票時所建立的實際值中。</span><span class="sxs-lookup"><span data-stu-id="efa20-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="efa20-116">如果您要對稅金金額進行變更，就必須輸入正確的稅額，而不是貸記的稅額。</span><span class="sxs-lookup"><span data-stu-id="efa20-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="efa20-117">里程碑更正一律以完全貸記的方式處理。</span><span class="sxs-lookup"><span data-stu-id="efa20-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="efa20-118">如果開立了金額不正確的發票給客戶，則可以更正保留款或預付金的金額。</span><span class="sxs-lookup"><span data-stu-id="efa20-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="efa20-119">如果使用了不正確的金額對先前已確認發票上的收費進行協調，則可以更正保留款及預付金的對帳單。</span><span class="sxs-lookup"><span data-stu-id="efa20-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="efa20-120">做為對其他已開發票收費之更正的發票明細詳細資料，會將 **更正** 欄位設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="efa20-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="efa20-121">已更正發票明細詳細資料的發票具有名為 **有更正** 的欄位，此欄位也會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="efa20-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="efa20-122">在確認更正發票時所建立的實際值</span><span class="sxs-lookup"><span data-stu-id="efa20-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="efa20-123">下表列出在確認更正發票時所建立的實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="efa20-124">
                    <strong>案例</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efa20-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="efa20-125">
                    <strong>確認時建立的實際值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efa20-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="efa20-126">確認已開發票預付金或保留款的更正。<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efa20-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-127">為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="efa20-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="efa20-128">此金額為正數，因為這是要用來抵消開立保留款或預付金發票時所建立的負數金額。</span><span class="sxs-lookup"><span data-stu-id="efa20-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-129">已開單銷售沖銷是針對保留款或預付金的金額建立來沖銷原始已開單銷售。</span><span class="sxs-lookup"><span data-stu-id="efa20-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-130">新的已開單銷售實際值是針對根據保留款或預付金更正之發票明細的更正金額所建立。</span><span class="sxs-lookup"><span data-stu-id="efa20-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-131">根據保留款或預付金更正之發票明細金額為負數的未開單銷售實際值，用於協調對帳差異。</span><span class="sxs-lookup"><span data-stu-id="efa20-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="efa20-132">對先前已協調保留款或預付金的更正確認。</span><span class="sxs-lookup"><span data-stu-id="efa20-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-133">為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="efa20-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="efa20-134">此金額為正數，要用來抵消先前進行對帳差異協調時所建立的負數金額。</span><span class="sxs-lookup"><span data-stu-id="efa20-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-135">先前發票金額的已開單銷售沖銷實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-136">套用於更正後發票之已更正保留款金額的新開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-137">更正後剩餘保留款或預付金為負數金額的未開單銷售實際值，這會用來對後來的發票進行對帳差異協調。</span><span class="sxs-lookup"><span data-stu-id="efa20-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="efa20-138">對先前已開發票的時間交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="efa20-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-139">原始時間發票明細詳細資料上時數及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="efa20-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-140">原始時間發票明細詳細資料上時數及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="efa20-141">對時間交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="efa20-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-142">原始時間發票明細詳細資料上已開發票時數及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="efa20-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-143">應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-144">應按照扣減發票明細詳細資料上已更正數字後剩餘時數及金額收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="efa20-145">對先前已開發票的費用交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="efa20-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-146">原始費用發票明細詳細資料上數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="efa20-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-147">原始費用發票明細詳細資料上數量及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="efa20-148">對先前已開發票的費用交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="efa20-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-149">原始費用發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="efa20-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-150">應按照更正後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-151">應按照扣減發票明細詳細資料上已更正數字後剩餘數量及金額收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="efa20-152">對先前已開發票的服務費交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="efa20-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-153">原始服務費發票明細詳細資料上數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="efa20-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-154">原始服務費發票明細詳細資料上數量及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="efa20-155">對先前已開發票的服務費交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="efa20-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-156">原始服務費發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="efa20-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-157">應按照編輯後更正發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="efa20-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="efa20-158">對先前已開發票的里程碑交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="efa20-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-159">原始里程碑發票明細詳細資料上金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="efa20-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="efa20-160">里程碑上的發票狀態已從<b>客戶發票已過帳</b>更新為<b>已準備好開立發票</b>。</span><span class="sxs-lookup"><span data-stu-id="efa20-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="efa20-161">對先前已開發票的里程碑交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="efa20-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efa20-162">不支援</span><span class="sxs-lookup"><span data-stu-id="efa20-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
