---
title: 專案型報價明細概觀
description: 本主題提供有關將專案型報價明細用於專案工作的資訊。
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369861"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="5dbdd-103">專案型報價明細概觀</span><span class="sxs-lookup"><span data-stu-id="5dbdd-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="5dbdd-104">_**適用於：** 精簡部署 - 交易至開立預估發票、資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="5dbdd-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5dbdd-105">專案型報價明細是為了協助在業務開發上估計專案工作而設計。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="5dbdd-106">專案型報價明細的結構已運用下列概念針對專案估計值進行擴充：</span><span class="sxs-lookup"><span data-stu-id="5dbdd-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="5dbdd-107">計費方式</span><span class="sxs-lookup"><span data-stu-id="5dbdd-107">Billing Method</span></span>
- <span data-ttu-id="5dbdd-108">專案和工作對應</span><span class="sxs-lookup"><span data-stu-id="5dbdd-108">Project and Task Mapping</span></span>
- <span data-ttu-id="5dbdd-109">已包含交易分類</span><span class="sxs-lookup"><span data-stu-id="5dbdd-109">Included Transaction classes</span></span>
- <span data-ttu-id="5dbdd-110">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="5dbdd-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="5dbdd-111">可收費率設定</span><span class="sxs-lookup"><span data-stu-id="5dbdd-111">Chargeability setup</span></span>
- <span data-ttu-id="5dbdd-112">使用報價明細詳細資料的估計</span><span class="sxs-lookup"><span data-stu-id="5dbdd-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="5dbdd-113">報價明細客戶</span><span class="sxs-lookup"><span data-stu-id="5dbdd-113">Quote line Customers</span></span>

<span data-ttu-id="5dbdd-114">下表提供有關專案型報價明細的 **一般** 索引標籤上的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="5dbdd-115">這些欄位可協助為專案工作設定詳細的全新估計基礎。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="5dbdd-116">**欄位**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-116">**Field**</span></span> | <span data-ttu-id="5dbdd-117">**描述**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-117">**Description**</span></span> | <span data-ttu-id="5dbdd-118">**下游影響**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5dbdd-119">名字</span><span class="sxs-lookup"><span data-stu-id="5dbdd-119">Name</span></span> | <span data-ttu-id="5dbdd-120">報價明細的名稱，可協助您找出估計中報價的分立元件。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="5dbdd-121">已複製到報價成交時從此報價明細中建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-122">計費方式</span><span class="sxs-lookup"><span data-stu-id="5dbdd-122">Billing Method</span></span> | <span data-ttu-id="5dbdd-123">在根據商機所建立的報價上，此值是從商機明細的對應欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="5dbdd-124">此欄位包含 Dynamics 365 Project Operations 支援的兩個主要合約模型：</span><span class="sxs-lookup"><span data-stu-id="5dbdd-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="5dbdd-125">- 固定價格</span><span class="sxs-lookup"><span data-stu-id="5dbdd-125">- Fixed price</span></span></br><span data-ttu-id="5dbdd-126">- 時間和材料。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-126">- Time and material.</span></span>| <span data-ttu-id="5dbdd-127">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-128">Project</span><span class="sxs-lookup"><span data-stu-id="5dbdd-128">Project</span></span> | <span data-ttu-id="5dbdd-129">使用此選用欄位來找出將在此業務開發上用來交付工作的專案。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="5dbdd-130">將專案對應至報價明細時，不僅有助於設定應收費工作，而且還可協助將專案型估計值提供給報價明細做為報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="5dbdd-131">未將專案對應至專案型報價明細時，應藉由建立每個報價明細詳細資料，手動建立估計值。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="5dbdd-132">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="5dbdd-133">包含的工作</span><span class="sxs-lookup"><span data-stu-id="5dbdd-133">Included Tasks</span></span> | <span data-ttu-id="5dbdd-134">指示是否將此報價明細用於所選專案的所有或部分專案工作。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="5dbdd-135">此欄位有下列可能值：</span><span class="sxs-lookup"><span data-stu-id="5dbdd-135">This field has the following possible values:</span></span></br><span data-ttu-id="5dbdd-136">- 所有專案工作</span><span class="sxs-lookup"><span data-stu-id="5dbdd-136">- All project tasks</span></span></br><span data-ttu-id="5dbdd-137">- 僅限選取的專案工作</span><span class="sxs-lookup"><span data-stu-id="5dbdd-137">- Selected project tasks only</span></span></br><span data-ttu-id="5dbdd-138">此欄位值為空白就相當於 **所有專案工作** 選項。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="5dbdd-139">在專案頁面上選取 **僅限選取的專案工作** 時，**工作帳單設定** 索引標籤允許您選取特定工作，將其與此報價明細建立關聯。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="5dbdd-140">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-141">包括時間</span><span class="sxs-lookup"><span data-stu-id="5dbdd-141">Include Time</span></span> | <span data-ttu-id="5dbdd-142">**是**/**否** 值表示此報價明細的估計值中是否包含所選專案的時間交易或人力成本。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5dbdd-143">**否** 值表示時間交易或人力成本不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5dbdd-144">**是** 值表示時間交易或人力成本會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5dbdd-145">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-146">包括費用</span><span class="sxs-lookup"><span data-stu-id="5dbdd-146">Include Expense</span></span> | <span data-ttu-id="5dbdd-147">**是**/**否** 值表示此報價明細的估計值中是否包含所選專案的費用成本。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5dbdd-148">**否** 值表示費用成本不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5dbdd-149">**是** 值表示費用成本會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5dbdd-150">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-151">包括材料</span><span class="sxs-lookup"><span data-stu-id="5dbdd-151">Include Material</span></span> | <span data-ttu-id="5dbdd-152">**是**/**否** 值表示此報價明細的估計值中是否包含所選專案的材料成本。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5dbdd-153">**否** 值表示此報價明細的估計值中將不包含所選專案的材料成本。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5dbdd-154">**是** 值表示此報價明細的估計值中將會包含所選專案的材料成本。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5dbdd-155">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-156">包括服務費</span><span class="sxs-lookup"><span data-stu-id="5dbdd-156">Include Fee</span></span> | <span data-ttu-id="5dbdd-157">**是**/**否** 值表示此報價明細的估計值中是否包含所選專案的服務費成本。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5dbdd-158">**否** 值表示服務費不會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5dbdd-159">**是** 值表示服務費會包含在此報價明細的估計值中。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5dbdd-160">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-161">報價金額</span><span class="sxs-lookup"><span data-stu-id="5dbdd-161">Quoted Amount</span></span> | <span data-ttu-id="5dbdd-162">這是針對所有在此專案型報價明細中預測的工作，向客戶提出報價的金額。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="5dbdd-163">在根據商機所建立的報價上，此值是從商機明細的 **客戶預算** 欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="5dbdd-164">專案型報價明細含有明細詳細資料時，此欄位會遭鎖定而無法加以編輯，並且會彙總列出報價明細詳細資料上的金額。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="5dbdd-165">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-166">估計稅額</span><span class="sxs-lookup"><span data-stu-id="5dbdd-166">Estimated Tax</span></span> | <span data-ttu-id="5dbdd-167">這是可編輯的欄位，以供使用者在報價明細上新增估計稅金。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="5dbdd-168">專案型報價明細含有明細詳細資料時，此欄位會遭鎖定而無法加以編輯，並且會彙總列出報價明細詳細資料上的稅額。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="5dbdd-169">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-170">稅後報價金額</span><span class="sxs-lookup"><span data-stu-id="5dbdd-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="5dbdd-171">此欄位是稅後報價明細金額，並且為唯讀。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="5dbdd-172">此欄位中的金額是以 *報價金額 + 稅金* 計算而得。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="5dbdd-173">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-174">不得超過限制</span><span class="sxs-lookup"><span data-stu-id="5dbdd-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="5dbdd-175">此欄位是可編輯的欄位，只能在帳務方式為 **時間和材料** 的專案型報價明細上使用。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="5dbdd-176">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5dbdd-177">客戶預算</span><span class="sxs-lookup"><span data-stu-id="5dbdd-177">Customer Budget</span></span> | <span data-ttu-id="5dbdd-178">此欄位是可編輯的欄位，如果報價是根據商機所建立，則該欄位是從商機明細的對應欄位複製而來。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="5dbdd-179">此值會複製到報價成交時從此報價明細所建立的專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="5dbdd-180">專案型報價明細的 [一般] 索引標籤上的欄位驗證規則</span><span class="sxs-lookup"><span data-stu-id="5dbdd-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="5dbdd-181">**規則 1**：如果 **包含的工作** 欄位為空白，或者已設定為 **所有專案工作**，則會在報價明細中包含專案。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="5dbdd-182">**規則 2**：如果 **包含的工作** 欄位為空白，或者已設定為 **所有專案工作**，則只能將專案及特定交易分類包含在報價的專案型報價明細中。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="5dbdd-183">**規則 3**：如果 **包含的工作** 欄位已設定為 **僅限選取的專案工作**，則可以將專案及特定交易分類包含在報價的多個專案型報價明細中。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="5dbdd-184">**規則 4**：如果商機有多個報價，則可以有來自各種全都參考相同專案且包含相同交易分類之不同報價的報價明細。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="5dbdd-185">**規則 5**：如果報價不屬於同一個商機，則不能包含相同的專案和交易分類。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="5dbdd-186">
                    <strong>商機</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="5dbdd-187">
                    <strong>報價</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="5dbdd-188">
                    <strong>報價明細</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="5dbdd-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="5dbdd-190">
                    <strong>包含的工作</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="5dbdd-191">
                    <strong>包括時間</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="5dbdd-192">
                    <strong>包括費用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="5dbdd-193">
                    <strong>包括材料</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="5dbdd-194">
                    <strong>包括​​</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="5dbdd-195">
                    <strong>費用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="5dbdd-196">
                    <strong>有效/無效</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="5dbdd-197">
                    <strong>原因</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5dbdd-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-198">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-199">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-200">QL1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-201">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-202">空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-203">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-204">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-205">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-206">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-207">無效</span><span class="sxs-lookup"><span data-stu-id="5dbdd-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-208">違反規則 #2。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-208">Violation of Rule #2.</span></span> <span data-ttu-id="5dbdd-209">P1 專案上的時間、費用和服務費已包含在報價明細 QL1 及 QL2 中</span><span class="sxs-lookup"><span data-stu-id="5dbdd-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-210">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-211">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-212">QL2</span><span class="sxs-lookup"><span data-stu-id="5dbdd-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-213">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-214">空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-215">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-216">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-217">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-218">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-219">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-220">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-221">QL1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-222">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-223">空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-224">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-225">無</span><span class="sxs-lookup"><span data-stu-id="5dbdd-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-226">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-227">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-228">無效</span><span class="sxs-lookup"><span data-stu-id="5dbdd-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-229">違反規則 #2。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-229">Violation of Rule #2.</span></span> <span data-ttu-id="5dbdd-230">P1 專案上的時間、材料和服務費已包含在報價明細 QL1 及 QL2 中</span><span class="sxs-lookup"><span data-stu-id="5dbdd-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-231">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-232">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-233">QL2</span><span class="sxs-lookup"><span data-stu-id="5dbdd-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-234">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-235">空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-236">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-237">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-238">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-239">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-240">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-241">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-242">QL1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-243">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-244">空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-245">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-246">無</span><span class="sxs-lookup"><span data-stu-id="5dbdd-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-247">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-248">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-249">有效</span><span class="sxs-lookup"><span data-stu-id="5dbdd-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-250">P1 專案的時間、材料和服務費已包含在 QL1 中</span><span class="sxs-lookup"><span data-stu-id="5dbdd-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="5dbdd-251">P1 專案上的費用已包含在 QL2 中</span><span class="sxs-lookup"><span data-stu-id="5dbdd-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="5dbdd-252">每個報價明細所包含的內容之間沒有任何重疊，因此有效。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-253">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-254">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-255">QL2</span><span class="sxs-lookup"><span data-stu-id="5dbdd-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-256">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-257">空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-258">無</span><span class="sxs-lookup"><span data-stu-id="5dbdd-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-259">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-260">無</span><span class="sxs-lookup"><span data-stu-id="5dbdd-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-261">無</span><span class="sxs-lookup"><span data-stu-id="5dbdd-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-262">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-263">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-264">QL1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-265">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-266">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="5dbdd-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-267">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-268">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-269">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-270">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-271">無效</span><span class="sxs-lookup"><span data-stu-id="5dbdd-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-272">違反規則 #2</span><span class="sxs-lookup"><span data-stu-id="5dbdd-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="5dbdd-273">Q1 包含專案 P1 上工作子集的時間、材料、費用和服務費</span><span class="sxs-lookup"><span data-stu-id="5dbdd-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="5dbdd-274">QL2 包含整個專案 P1 的時間、費用和服務費，因此與 Q1 中所包含的內容重疊。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-275">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-276">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-277">QL2</span><span class="sxs-lookup"><span data-stu-id="5dbdd-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-278">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-279">空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-280">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-281">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-282">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-283">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-284">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-285">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-286">QL1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-287">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-288">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="5dbdd-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-289">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-290">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-291">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-292">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-293">有效</span><span class="sxs-lookup"><span data-stu-id="5dbdd-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-294">根據規則 #3，</span><span class="sxs-lookup"><span data-stu-id="5dbdd-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="5dbdd-295">Q1 包含專案 P1 上工作子集的時間、材料、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5dbdd-296">QL2 包含專案 P1 的工作子集的時間、材料、費用和服務費。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5dbdd-297">唯一的額外驗證是要求 QL1 上的工作子集與 QL2 上的工作子集不同，以確保其間沒有任何重疊。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="5dbdd-298">建立與工作的關聯時，系統會完成此作業。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-299">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-300">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-301">QL2</span><span class="sxs-lookup"><span data-stu-id="5dbdd-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-302">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-303">僅限選取的工作</span><span class="sxs-lookup"><span data-stu-id="5dbdd-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-304">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-305">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-306">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-307">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-308">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-309">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-310">QL1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-311">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-312">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-313">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-314">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-315">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-316">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-317">有效</span><span class="sxs-lookup"><span data-stu-id="5dbdd-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-318">根據規則 #5，Q1 和 Q2 是兩個位於相同商機的報價，因此兩者都可以對專案的相同元件進行估計。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-319">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-320">第 2 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-321">QL1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-322">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-323">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-324">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-325">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-326">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-327">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-328">O1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-329">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-330">QL1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-331">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-332">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-333">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-334">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-335">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-336">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-337">無效</span><span class="sxs-lookup"><span data-stu-id="5dbdd-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5dbdd-338">根據規則 #4，Q1 和 Q2 是兩個位於不同商機的報價，因此無法對同一個專案的相同元件進行估計。</span><span class="sxs-lookup"><span data-stu-id="5dbdd-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5dbdd-339">O2</span><span class="sxs-lookup"><span data-stu-id="5dbdd-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5dbdd-340">第 1 季</span><span class="sxs-lookup"><span data-stu-id="5dbdd-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5dbdd-341">QL1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-342">P1</span><span class="sxs-lookup"><span data-stu-id="5dbdd-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5dbdd-343">所有專案工作或空白</span><span class="sxs-lookup"><span data-stu-id="5dbdd-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5dbdd-344">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5dbdd-345">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5dbdd-346">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5dbdd-347">.是</span><span class="sxs-lookup"><span data-stu-id="5dbdd-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
