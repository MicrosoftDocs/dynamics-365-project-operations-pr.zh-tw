---
title: 確認預估發票 - 精簡
description: 本主題提供有關在 Project Operations 中確認預估發票的資訊。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274268"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="836a8-103">確認預估發票 - 精簡</span><span class="sxs-lookup"><span data-stu-id="836a8-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="836a8-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="836a8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="836a8-105">確認預估發票之後，專案發票的狀態會更新為 **已確認**。</span><span class="sxs-lookup"><span data-stu-id="836a8-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="836a8-106">確認發票時，它會變成唯讀。</span><span class="sxs-lookup"><span data-stu-id="836a8-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="836a8-107">從現在開始，發票僅於有任何客戶提議更正或賒帳，或是將發票標示為已付款時，才能進行更正。</span><span class="sxs-lookup"><span data-stu-id="836a8-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="836a8-108">下表列出系統所建立的實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="836a8-109">這些實際值是在確認草稿專案發票前對其執行特定作業時所建立。</span><span class="sxs-lookup"><span data-stu-id="836a8-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="836a8-110">
                    <strong>案例</strong>
                </span><span class="sxs-lookup"><span data-stu-id="836a8-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="836a8-111">
                    <strong>確認時建立的實際值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="836a8-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="836a8-112">開立預付金 (或定額保留後隨用即扣型付款) 的發票</span><span class="sxs-lookup"><span data-stu-id="836a8-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-113">類型為<strong>保留款</strong>的已開單銷售實際值是針對預付金 (或定額保留後隨用即扣型付款) 的金額所建立。</span><span class="sxs-lookup"><span data-stu-id="836a8-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-114">要用於協調對帳差異之金額為負值的保留款或預付金未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="836a8-115">在發票上將保留款或預付金的差異完全協調之後。</span><span class="sxs-lookup"><span data-stu-id="836a8-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-116">為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="836a8-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="836a8-117">此金額為正值，因為這是要用來抵消開立保留款或預付金發票時所建立的負值金額。</span><span class="sxs-lookup"><span data-stu-id="836a8-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-118">此發票金額的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="836a8-119">在發票上將保留款或預付金的差異部分協調之後。</span><span class="sxs-lookup"><span data-stu-id="836a8-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-120">為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="836a8-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="836a8-121">此金額為正值，因為這是要用來抵消開立保留款或預付金發票時所建立的負值金額。</span><span class="sxs-lookup"><span data-stu-id="836a8-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-122">此發票金額的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-123">要在未來發票上用於協調對帳差異之保留款或預付金剩餘金額的負數未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="836a8-124">不對草稿發票進行任何編輯，即開立時間交易發票。</span><span class="sxs-lookup"><span data-stu-id="836a8-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-125">原始時間核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="836a8-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-126">原始時間核准上的時數及金額的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="836a8-127">開立減少數量時所編輯之時間交易的發票。</span><span class="sxs-lookup"><span data-stu-id="836a8-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-128">原始時間核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="836a8-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-129">應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-130">不應對已編輯發票明細詳細資料在扣除更正過數字後剩餘時數及金額收費的新增未開單銷售實際值、銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="836a8-131">開立增加數量時所編輯之時間交易的發票。</span><span class="sxs-lookup"><span data-stu-id="836a8-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-132">原始時間核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="836a8-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-133">應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="836a8-134">不對草稿發票進行任何編輯，即開立費用交易發票。</span><span class="sxs-lookup"><span data-stu-id="836a8-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-135">原始費用核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="836a8-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-136">原始費用核准上的數量及金額的已開單銷售實際值</span><span class="sxs-lookup"><span data-stu-id="836a8-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="836a8-137">開立減少數量時所編輯之費用交易的發票。</span><span class="sxs-lookup"><span data-stu-id="836a8-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-138">原始費用核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="836a8-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-139">應按照編輯後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-140">不應對已編輯發票明細詳細資料在扣除更正過數字後剩餘數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="836a8-141">開立增加數量時所編輯之費用交易的發票。</span><span class="sxs-lookup"><span data-stu-id="836a8-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-142">原始費用核准上的時數及金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="836a8-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-143">應按照編輯後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="836a8-144">開立服務費發票。</span><span class="sxs-lookup"><span data-stu-id="836a8-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-145">原始帳目明細上的服務費金額的未開單銷售沖銷。</span><span class="sxs-lookup"><span data-stu-id="836a8-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-146">原始費用帳目明細上的數量及金額的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="836a8-147">開立里程碑發票。</span><span class="sxs-lookup"><span data-stu-id="836a8-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-148">原始里程碑在專案合約服務內容上的里程碑金額已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="836a8-149">開立產品型合約服務內容的發票。</span><span class="sxs-lookup"><span data-stu-id="836a8-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="836a8-150">其數量和金額來自產品型合約服務內容的產品明細已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="836a8-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]