---
title: 專案型報價明細
description: 本主題提供有關將專案型報價明細用於專案工作的資訊。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072863"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="1a92a-103">專案型報價明細</span><span class="sxs-lookup"><span data-stu-id="1a92a-103">Project-based quote lines</span></span>

<span data-ttu-id="1a92a-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="1a92a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1a92a-105">專案型報價明細是為了協助在業務開發上估計專案工作而設計。</span><span class="sxs-lookup"><span data-stu-id="1a92a-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="1a92a-106">專案型報價明細的結構已運用下列概念針對專案估計值進行擴充：</span><span class="sxs-lookup"><span data-stu-id="1a92a-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="1a92a-107">計費方式</span><span class="sxs-lookup"><span data-stu-id="1a92a-107">Billing Method</span></span>
- <span data-ttu-id="1a92a-108">專案對應</span><span class="sxs-lookup"><span data-stu-id="1a92a-108">Project Mapping</span></span>
- <span data-ttu-id="1a92a-109">已包含交易分類</span><span class="sxs-lookup"><span data-stu-id="1a92a-109">Included Transaction classes</span></span>
- <span data-ttu-id="1a92a-110">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="1a92a-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="1a92a-111">可收費率設定</span><span class="sxs-lookup"><span data-stu-id="1a92a-111">Chargeability setup</span></span>
- <span data-ttu-id="1a92a-112">使用報價明細詳細資料的估計</span><span class="sxs-lookup"><span data-stu-id="1a92a-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="1a92a-113">報價明細客戶</span><span class="sxs-lookup"><span data-stu-id="1a92a-113">Quote line Customers</span></span>

<span data-ttu-id="1a92a-114">下表提供有關專案型報價明細的 **一般** 索引標籤上的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="1a92a-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="1a92a-115">這些欄位可協助為專案工作設定詳細的全新估計基礎。</span><span class="sxs-lookup"><span data-stu-id="1a92a-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="1a92a-116">**欄位**</span><span class="sxs-lookup"><span data-stu-id="1a92a-116">**Field**</span></span> | <span data-ttu-id="1a92a-117">**關聯性、目的和指引**</span><span class="sxs-lookup"><span data-stu-id="1a92a-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="1a92a-118">**下游影響**</span><span class="sxs-lookup"><span data-stu-id="1a92a-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1a92a-119">名字</span><span class="sxs-lookup"><span data-stu-id="1a92a-119">Name</span></span> | <span data-ttu-id="1a92a-120">報價明細的名稱，應可協助您找出估計中報價的分立元件。</span><span class="sxs-lookup"><span data-stu-id="1a92a-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="1a92a-121">已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a92a-122">計費方式</span><span class="sxs-lookup"><span data-stu-id="1a92a-122">Billing Method</span></span> | <span data-ttu-id="1a92a-123">在根據商機所建立的報價上，此值是從商機明細的對應欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="1a92a-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="1a92a-124">此欄位包含 Dynamics 365 Project Operations 所支援的兩個主要合約模型：</span><span class="sxs-lookup"><span data-stu-id="1a92a-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="1a92a-125">- 固定價格</span><span class="sxs-lookup"><span data-stu-id="1a92a-125">- Fixed price</span></span></br><span data-ttu-id="1a92a-126">- 時間和材料。</span><span class="sxs-lookup"><span data-stu-id="1a92a-126">- Time and material.</span></span>| <span data-ttu-id="1a92a-127">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a92a-128">Project</span><span class="sxs-lookup"><span data-stu-id="1a92a-128">Project</span></span> | <span data-ttu-id="1a92a-129">使用此選用欄位來找出將在此業務開發上用來交付工作的專案。</span><span class="sxs-lookup"><span data-stu-id="1a92a-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="1a92a-130">將專案對應至報價明細時，不僅有助於設定應收費工作，而且還可協助將專案型估計值提供給報價明細做為報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1a92a-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="1a92a-131">未將專案對應至專案型報價明細時，應藉由建立每個報價明細詳細資料，手動建立估計值。</span><span class="sxs-lookup"><span data-stu-id="1a92a-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="1a92a-132">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a92a-133">包括時間</span><span class="sxs-lookup"><span data-stu-id="1a92a-133">Include Time</span></span> | <span data-ttu-id="1a92a-134">**是**/**否** 旗標指示所選專案的時間交易或人力成本是否會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a92a-135">**否** 值表示時間交易或人力成本不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a92a-136">**是** 值表示時間交易或人力成本會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a92a-137">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a92a-138">包括費用</span><span class="sxs-lookup"><span data-stu-id="1a92a-138">Include Expense</span></span> | <span data-ttu-id="1a92a-139">**是**/**否** 旗標指示所選專案的費用成本是否會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a92a-140">**否** 值表示費用成本不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a92a-141">**是** 值表示費用成本會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a92a-142">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a92a-143">包括服務費</span><span class="sxs-lookup"><span data-stu-id="1a92a-143">Include Fee</span></span> | <span data-ttu-id="1a92a-144">**是**/**否** 旗標指示所選專案的服務費是否會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a92a-145">**否** 值表示服務費不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a92a-146">**是** 值表示服務費會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a92a-147">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a92a-148">報價金額</span><span class="sxs-lookup"><span data-stu-id="1a92a-148">Quoted Amount</span></span> | <span data-ttu-id="1a92a-149">這是針對所有為此專案型報價明細預測之工作，報價給客戶的金額。</span><span class="sxs-lookup"><span data-stu-id="1a92a-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="1a92a-150">在根據商機所建立的報價上，此值是從商機明細的 **客戶預算** 欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="1a92a-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="1a92a-151">專案型報價明細含有明細詳細資料時，此欄位會遭鎖定而無法加以編輯，並且會彙總列出報價明細詳細資料上的金額。</span><span class="sxs-lookup"><span data-stu-id="1a92a-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="1a92a-152">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a92a-153">估計稅額</span><span class="sxs-lookup"><span data-stu-id="1a92a-153">Estimated Tax</span></span> | <span data-ttu-id="1a92a-154">這是可編輯的欄位，以供使用者在報價明細上新增估計稅金。</span><span class="sxs-lookup"><span data-stu-id="1a92a-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="1a92a-155">專案型報價明細含有明細詳細資料時，此欄位會遭鎖定而無法加以編輯，並且會彙總列出報價明細詳細資料上的稅額。</span><span class="sxs-lookup"><span data-stu-id="1a92a-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="1a92a-156">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a92a-157">稅後報價金額</span><span class="sxs-lookup"><span data-stu-id="1a92a-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="1a92a-158">此欄位是稅後報價明細金額，並且為唯讀。</span><span class="sxs-lookup"><span data-stu-id="1a92a-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="1a92a-159">此欄位中的金額是以 *報價金額 + 稅金* 計算而得。</span><span class="sxs-lookup"><span data-stu-id="1a92a-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="1a92a-160">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a92a-161">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="1a92a-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="1a92a-162">此欄位是可編輯的欄位，只能在帳務方式為 **時間和材料** 的專案型報價明細上使用。</span><span class="sxs-lookup"><span data-stu-id="1a92a-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="1a92a-163">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a92a-164">客戶預算</span><span class="sxs-lookup"><span data-stu-id="1a92a-164">Customer Budget</span></span> | <span data-ttu-id="1a92a-165">此欄位是可編輯的欄位，如果報價是根據商機所建立，則該欄位是從商機明細的對應欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="1a92a-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="1a92a-166">此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="1a92a-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="1a92a-167">專案型報價明細的 [一般] 索引標籤上的欄位驗證規則</span><span class="sxs-lookup"><span data-stu-id="1a92a-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="1a92a-168">**規則 1** ：所選專案上的特定交易分類只能包含在報價的一個專案型報價明細中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-168">**Rule 1** : A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="1a92a-169">**規則 2** ：如果商機有多個報價，則可以有來自各種全都參考相同專案且包含相同交易分類之不同報價的報價明細。</span><span class="sxs-lookup"><span data-stu-id="1a92a-169">**Rule 2** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="1a92a-170">**規則 3** ：如果報價不屬於同一個商機，則不能包含相同的專案和交易分類。</span><span class="sxs-lookup"><span data-stu-id="1a92a-170">**Rule 3** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="1a92a-171">
                    <strong>商機</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a92a-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="1a92a-172">
                    <strong>報價</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a92a-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1a92a-173">
                    <strong>報價明細</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a92a-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1a92a-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a92a-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1a92a-175">
                    <strong>包含時間</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a92a-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1a92a-176">
                    <strong>包含費用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a92a-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1a92a-177">
                    <strong>包括</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a92a-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="1a92a-178">
                    <strong>服務費</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a92a-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="1a92a-179">
                    <strong>有效/無效</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a92a-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="1a92a-180">
                    <strong>原因</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a92a-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-181">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-182">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-183">QL1</span><span class="sxs-lookup"><span data-stu-id="1a92a-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-184">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-185">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-186">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-187">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a92a-188">無效</span><span class="sxs-lookup"><span data-stu-id="1a92a-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a92a-189">違反規則 #1。</span><span class="sxs-lookup"><span data-stu-id="1a92a-189">Violation of Rule #1.</span></span> <span data-ttu-id="1a92a-190">P1 專案上的時間、費用和服務費已包含在報價明細 QL1 與 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-191">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-192">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-193">QL2</span><span class="sxs-lookup"><span data-stu-id="1a92a-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-194">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-195">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-196">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-197">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-198">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-199">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-200">QL1</span><span class="sxs-lookup"><span data-stu-id="1a92a-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-201">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-202">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-203">無</span><span class="sxs-lookup"><span data-stu-id="1a92a-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-204">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a92a-205">無效</span><span class="sxs-lookup"><span data-stu-id="1a92a-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a92a-206">違反規則 #1。</span><span class="sxs-lookup"><span data-stu-id="1a92a-206">Violation of Rule #1.</span></span> <span data-ttu-id="1a92a-207">P1 專案上的時間和服務費已包含在報價明細 QL1 與 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-208">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-209">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-210">QL2</span><span class="sxs-lookup"><span data-stu-id="1a92a-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-211">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-212">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-213">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-214">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-215">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-216">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-217">QL1</span><span class="sxs-lookup"><span data-stu-id="1a92a-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-218">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-219">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-220">無</span><span class="sxs-lookup"><span data-stu-id="1a92a-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-221">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a92a-222">有效</span><span class="sxs-lookup"><span data-stu-id="1a92a-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="1a92a-223">P1 專案上的時間和服務費已包含在 QL1 中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="1a92a-224">P1 專案上的費用已包含在 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="1a92a-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="1a92a-225">要包含在每個報價明細的項目中沒有重疊，因此有效。</span><span class="sxs-lookup"><span data-stu-id="1a92a-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-226">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-227">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-228">QL2</span><span class="sxs-lookup"><span data-stu-id="1a92a-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-229">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-230">無</span><span class="sxs-lookup"><span data-stu-id="1a92a-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-231">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-232">無</span><span class="sxs-lookup"><span data-stu-id="1a92a-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-233">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-234">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-235">QL1</span><span class="sxs-lookup"><span data-stu-id="1a92a-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-236">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-237">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-238">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-239">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a92a-240">無效</span><span class="sxs-lookup"><span data-stu-id="1a92a-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a92a-241">違反上述規則 #1</span><span class="sxs-lookup"><span data-stu-id="1a92a-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="1a92a-242">Q1 包含整個專案 P1 的時間、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="1a92a-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1a92a-243">QL2 包含整個專案 P1 的時間、費用和服務費，並與 Q1 中包含的項目重疊。</span><span class="sxs-lookup"><span data-stu-id="1a92a-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-244">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-245">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-246">QL2</span><span class="sxs-lookup"><span data-stu-id="1a92a-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-247">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-248">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-249">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-250">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-251">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-252">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-253">QL1</span><span class="sxs-lookup"><span data-stu-id="1a92a-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-254">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-255">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-256">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-257">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1a92a-258">有效</span><span class="sxs-lookup"><span data-stu-id="1a92a-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a92a-259">根據規則 #2，Q1 和 Q2 是同一個商機上的兩個報價，因此都可以對專案的相同元件進行估計。</span><span class="sxs-lookup"><span data-stu-id="1a92a-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-260">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-261">第 2 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-262">第 2 季的 QL1</span><span class="sxs-lookup"><span data-stu-id="1a92a-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-263">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-264">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-265">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-266">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-267">O1</span><span class="sxs-lookup"><span data-stu-id="1a92a-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-268">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-269">QL1</span><span class="sxs-lookup"><span data-stu-id="1a92a-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-270">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-271">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-272">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-273">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1a92a-274">有效</span><span class="sxs-lookup"><span data-stu-id="1a92a-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a92a-275">根據規則 #3，Q1 和 Q2 是兩個各在不同商機上的報價，因此無法對相同專案的相同元件進行估計。</span><span class="sxs-lookup"><span data-stu-id="1a92a-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a92a-276">O2</span><span class="sxs-lookup"><span data-stu-id="1a92a-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a92a-277">第 1 季</span><span class="sxs-lookup"><span data-stu-id="1a92a-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-278">QL1</span><span class="sxs-lookup"><span data-stu-id="1a92a-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-279">P1</span><span class="sxs-lookup"><span data-stu-id="1a92a-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-280">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a92a-281">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a92a-282">.是</span><span class="sxs-lookup"><span data-stu-id="1a92a-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1a92a-283">無效</span><span class="sxs-lookup"><span data-stu-id="1a92a-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

