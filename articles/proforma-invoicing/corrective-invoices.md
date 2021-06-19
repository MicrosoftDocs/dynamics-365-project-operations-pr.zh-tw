---
title: 專案型更正發票
description: 本主題提供有關如何在 Project Operations 中建立和確認專案型更正發票的資訊。
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012261"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="a9feb-103">專案型更正發票</span><span class="sxs-lookup"><span data-stu-id="a9feb-103">Corrective project-based invoices</span></span>

<span data-ttu-id="a9feb-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="a9feb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a9feb-105">確認過的專案發票可進行更正以處理與客戶及專案經理議定的變更或貸記。</span><span class="sxs-lookup"><span data-stu-id="a9feb-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="a9feb-106">若要對已確認的發票進行編輯，請開啟已確認的發票，然後選取 **更正此發票**。</span><span class="sxs-lookup"><span data-stu-id="a9feb-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="a9feb-107">除非專案發票已確認，或是專案型發票有預付金和保留款或者預付金及保留款對帳差異協調，否則無法使用此選取項目。</span><span class="sxs-lookup"><span data-stu-id="a9feb-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="a9feb-108">新的草稿發票會從已確認的發票中建立。</span><span class="sxs-lookup"><span data-stu-id="a9feb-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="a9feb-109">所有來自先前已確認發票的發票明細詳細資料都會複製到新的草稿中。</span><span class="sxs-lookup"><span data-stu-id="a9feb-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="a9feb-110">以下是了解新更正發票中明細詳細資訊的一些要點：</span><span class="sxs-lookup"><span data-stu-id="a9feb-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="a9feb-111">所有數量都會更新為零。</span><span class="sxs-lookup"><span data-stu-id="a9feb-111">All quantities are updated to zero.</span></span> <span data-ttu-id="a9feb-112">Dynamics 365 Project Operations 假設所有已開立發票的項目都已完全貸記。</span><span class="sxs-lookup"><span data-stu-id="a9feb-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="a9feb-113">如有需要，您可以手動更新這些數量以反映要開立發票的數量，而不是貸記的數量。</span><span class="sxs-lookup"><span data-stu-id="a9feb-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="a9feb-114">應用程式會根據您輸入的數量，計算貸記的數量。</span><span class="sxs-lookup"><span data-stu-id="a9feb-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="a9feb-115">此金額會反映在確認更正後發票時所建立的實際值中。</span><span class="sxs-lookup"><span data-stu-id="a9feb-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="a9feb-116">如果您要對稅金金額進行變更，就必須輸入正確的稅額，而不是貸記的稅額。</span><span class="sxs-lookup"><span data-stu-id="a9feb-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="a9feb-117">里程碑更正一律以完全貸記的方式處理。</span><span class="sxs-lookup"><span data-stu-id="a9feb-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="a9feb-118">對於做為對其他已開發票收費之更正的發票明細詳細資料，**更正** 欄位會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="a9feb-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="a9feb-119">對於已更正發票明細詳細資料的發票，**有更正** 欄位會設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="a9feb-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="a9feb-120">確認更正發票時所建立的實際值</span><span class="sxs-lookup"><span data-stu-id="a9feb-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="a9feb-121">下表列出在確認更正發票時所建立的實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="a9feb-122">
                    <strong>案例</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a9feb-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="a9feb-123">
                    <strong>確認時建立的實際值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a9feb-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a9feb-124">對先前已開發票的時間交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="a9feb-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-125">原始時間發票明細詳細資料上時數及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="a9feb-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-126">原始時間發票明細詳細資料上時數及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a9feb-127">對時間交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="a9feb-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-128">原始時間發票明細詳細資料上已開發票時數及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="a9feb-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-129">應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-130">應按照扣減發票明細詳細資料上已更正數字後剩餘時數及金額收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a9feb-131">對先前已開發票的費用交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="a9feb-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-132">原始費用發票明細詳細資料上數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="a9feb-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-133">原始費用發票明細詳細資料上數量及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a9feb-134">對先前已開發票的費用交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="a9feb-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-135">原始費用發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="a9feb-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-136">應按照更正後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-137">應按照扣減發票明細詳細資料上已更正數字後剩餘數量及金額收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a9feb-138">開立先前已開發票材料交易的全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="a9feb-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-139">材料原始發票明細詳細資料上數量和金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="a9feb-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-140">材料原始發票明細詳細資料上數量和金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a9feb-141">開立物料交易的部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="a9feb-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-142">材料原始發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="a9feb-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-143">對已編輯發票明細詳細資料、該項沖銷和等額已開單銷售實際值上數量和金額應收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-144">應按照扣減發票明細詳細資料上已更正數字後剩餘數量及金額收費的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a9feb-145">對先前已開發票的服務費交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="a9feb-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-146">原始服務費發票明細詳細資料上數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="a9feb-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-147">原始服務費發票明細詳細資料上數量及金額的新增未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a9feb-148">對先前已開發票的服務費交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="a9feb-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-149">原始服務費發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="a9feb-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-150">應按照編輯後更正發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a9feb-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a9feb-151">對先前已開發票的里程碑交易開立全額貸記發票。</span><span class="sxs-lookup"><span data-stu-id="a9feb-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-152">原始里程碑發票明細詳細資料上金額的已開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="a9feb-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="a9feb-153">里程碑的發票狀態已從<b>客戶發票已過帳</b>更新為<b>已準備好開立發票</b>。</span><span class="sxs-lookup"><span data-stu-id="a9feb-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a9feb-154">對先前已開發票的里程碑交易開立部分貸記發票。</span><span class="sxs-lookup"><span data-stu-id="a9feb-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a9feb-155">不支援此案例。</span><span class="sxs-lookup"><span data-stu-id="a9feb-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
