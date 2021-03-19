---
title: 設定費用管理
description: 本文說明在 Microsoft Dynamics 365 Finance 中設定費用管理之前，您必須在規劃過程中進行的考量與決策。
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271343"
---
# <a name="configure-expense-management"></a><span data-ttu-id="e0bdd-103">設定費用管理</span><span class="sxs-lookup"><span data-stu-id="e0bdd-103">Configure expense management</span></span>

<span data-ttu-id="e0bdd-104">本主題說明設定費用管理之前，您必須在規劃過程中進行的考量和決策。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="e0bdd-105">在費用管理中，您可以儲存付款方式、差旅申請、費用報表、原則等相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="e0bdd-106">因為在規劃費用管理設定時所做的許多決策是根據組織的階層和財務結構而定，您必須參考這些區域的計劃文件。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="e0bdd-107">公司間費用</span><span class="sxs-lookup"><span data-stu-id="e0bdd-107">Intercompany expenses</span></span>

<span data-ttu-id="e0bdd-108">啟用公司間費用時，您可以允許法律實體和員工代表其他法律實體承擔費用，並收取該法律實體支付組織內雇用的款項。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="e0bdd-109">例如，法律實體 A 中的員工為法律實體 B 完成專案，而此專案產生差旅相關的費用。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="e0bdd-110">如果啟用公司間費用，員工就可以提出會將費用過帳至法律實體 B 的費用報表，而且該費用必須由法律實體 A 支付。如果您的組織沒有多個法律實體，則不需要啟用公司間費用。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="e0bdd-111">**決策：** 是否要啟用公司間費用？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="e0bdd-112">財務管理</span><span class="sxs-lookup"><span data-stu-id="e0bdd-112">Financial management</span></span>

<span data-ttu-id="e0bdd-113">費用管理與組織的財務管理緊密整合在一起。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="e0bdd-114">費用管理的許多設定都會依據您所做關於組織財務的決策而定。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="e0bdd-115">下列各節說明各個需要根據組織財務決策和領導團隊指導進行規劃和決策的領域。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="e0bdd-116">每日津貼</span><span class="sxs-lookup"><span data-stu-id="e0bdd-116">Per diems</span></span>

<span data-ttu-id="e0bdd-117">您必須定義組織提供給員工的每日津貼。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="e0bdd-118">因為每日津貼通常用來抵補餐費、住宿費和其他雜項費用等開支，您可以為組織所提供的差旅津貼補助建立規則。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="e0bdd-119">每日津貼費率可以根據一年時節、出差地點或兩者來定。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="e0bdd-120">定義每日津貼規則時，您可以指定如果工作者獲得免費贈送的餐飲或服務時，每日津貼費率會扣留的百分比。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="e0bdd-121">您也可以每日津貼費率分級來設定每日津貼費率可套用至工作者差旅的最小及最大時數。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="e0bdd-122">**決策：**</span><span class="sxs-lookup"><span data-stu-id="e0bdd-122">**Decisions:**</span></span>

- <span data-ttu-id="e0bdd-123">第一天和最後一天的預設每日津貼規則：</span><span class="sxs-lookup"><span data-stu-id="e0bdd-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="e0bdd-124">員工可報銷不足一天的時數，而仍將收到足額每日津貼的最少時數為何？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="e0bdd-125">是否會扣減已提供的第一天與最後一天餐費金額？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="e0bdd-126">如果有扣減，扣減百分比為何？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="e0bdd-127">是否會扣減已提供的第一天與最後一天住宿金額？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="e0bdd-128">如果有扣減，扣減百分比為何？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="e0bdd-129">是否會扣減已提供的第一天與最後一天費用開支金額？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="e0bdd-130">如果有扣減，扣減百分比為何？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="e0bdd-131">預設每日津貼規則：</span><span class="sxs-lookup"><span data-stu-id="e0bdd-131">Default per diem rules:</span></span>

    - <span data-ttu-id="e0bdd-132">如果說出差員工享有免費供餐，是否會從每餐的每日津貼補助中扣減一定的百分比？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="e0bdd-133">如果有扣減，每餐的扣減百分比為何？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="e0bdd-134">餐費扣減是按每日、每趟差旅還是每天用餐次數來計算？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="e0bdd-135">每日津貼金額是依照一般的四捨五入方式還是向上捨入？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="e0bdd-136">每日津貼是按照 24小時週期還是日曆日進行計算？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="e0bdd-137">根據地點而定的每日津貼規則：</span><span class="sxs-lookup"><span data-stu-id="e0bdd-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="e0bdd-138">每日津貼費率是否會依據地點而有所不同？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="e0bdd-139">包括哪些地點？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-139">What locations are included?</span></span>
    - <span data-ttu-id="e0bdd-140">如果每日津貼費率依地點而不同，則對於每個地點，下列費用類型提供的百分比金額為何：</span><span class="sxs-lookup"><span data-stu-id="e0bdd-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="e0bdd-141">餐費</span><span class="sxs-lookup"><span data-stu-id="e0bdd-141">Meals</span></span>
        - <span data-ttu-id="e0bdd-142">飯店</span><span class="sxs-lookup"><span data-stu-id="e0bdd-142">Hotel</span></span>
        - <span data-ttu-id="e0bdd-143">其他費用</span><span class="sxs-lookup"><span data-stu-id="e0bdd-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="e0bdd-144">費用管理日記帳和科目</span><span class="sxs-lookup"><span data-stu-id="e0bdd-144">Expense management journals and accounts</span></span>

<span data-ttu-id="e0bdd-145">費用管理要求您必須使用多個日記帳和科目。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="e0bdd-146">例如，您必須決定是否要將相同的科目用於預付現金和信用卡紛爭。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="e0bdd-147">**決策：**</span><span class="sxs-lookup"><span data-stu-id="e0bdd-147">**Decisions:**</span></span>

- <span data-ttu-id="e0bdd-148">已核准的費用報表會過帳到哪些總帳日記帳？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="e0bdd-149">預付現金要使用哪一個科目？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="e0bdd-150">預付現金是否應立即過帳？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="e0bdd-151">付款方式</span><span class="sxs-lookup"><span data-stu-id="e0bdd-151">Payment methods</span></span>

<span data-ttu-id="e0bdd-152">允許員工代表公司開支費用時，您必須定義員工可以使用的付款方式。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="e0bdd-153">例如，您可能會允許員工使用現金或公司信用卡來支付。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="e0bdd-154">您可能也會允許員工先用個人信用卡支付，然後您再補償員工。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="e0bdd-155">您必須對每個您所允許的付款方式做出下列決策。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="e0bdd-156">**決策：**</span><span class="sxs-lookup"><span data-stu-id="e0bdd-156">**Decisions:**</span></span>

- <span data-ttu-id="e0bdd-157">允許使用哪些付款方式？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="e0bdd-158">誰負責付款方式費用？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="e0bdd-159">是否有抵銷科目類型？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-159">Is there an offset account type?</span></span> <span data-ttu-id="e0bdd-160">如果有抵銷科目類型，是什麼類型？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="e0bdd-161">如果有抵銷科目，是什麼科目？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="e0bdd-162">如果付款方式為信用卡，付款方式只能用於匯入交易嗎？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="e0bdd-163">費用類別和共用類別</span><span class="sxs-lookup"><span data-stu-id="e0bdd-163">Expense categories and shared categories</span></span>

<span data-ttu-id="e0bdd-164">員工建立費用報表時，他們記錄的每項費用都必須與費用類別有關聯。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="e0bdd-165">費用類別是從可在您組織中所有法律實體之間共用的共用類別衍生而來。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="e0bdd-166">視組織的定義方式而定，也可以在 [專案管理與會計] 中共用這些類別。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="e0bdd-167">請根據組織的定義和實作團隊的指引，判斷費用管理中使用的類別是否僅限在 [費用管理] 中使用，或是否應在 [專案管理與會計] 與 [費用管理] 之間共用。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="e0bdd-168">請注意，這些類別可以在 [專案] 與 [費用] 之間或 [專案] 與 [生產] 之間共用，但無法在 [費用] 與 [生產] 之間共用。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="e0bdd-169">您必須對每個費用類別做出下列決策。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="e0bdd-170">**決策：**</span><span class="sxs-lookup"><span data-stu-id="e0bdd-170">**Decisions:**</span></span>

- <span data-ttu-id="e0bdd-171">什麼是費用類別？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-171">What is the expense category?</span></span> <span data-ttu-id="e0bdd-172">範例包括航班、住宿或里程等類別。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="e0bdd-173">費用類別也可以用於 [專案管理與會計] 嗎？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="e0bdd-174">什麼是費用類型？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-174">What is the expense type?</span></span>
- <span data-ttu-id="e0bdd-175">什麼是費用類別的預設付款方式？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="e0bdd-176">費用類別中的費用是否必須逐條列舉？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="e0bdd-177">什麼是費用類別的主要預設科目？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="e0bdd-178">什麼是費用類別的預設項目銷售課稅群組？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="e0bdd-179">費用類別是否允許其他付款方式？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="e0bdd-180">如果允許其他付款方式，是哪些方式？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="e0bdd-181">此費用類別中是否有子類別？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="e0bdd-182">如果有子類別，您還必須做出下列決定：</span><span class="sxs-lookup"><span data-stu-id="e0bdd-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="e0bdd-183">是否有任何子類別不在稅金退還之列？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="e0bdd-184">什麼是子類別的項目銷售課稅群組？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="e0bdd-185">如果也會在 [專案管理與會計] 中使用費用類別，請回答剩下的問題。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="e0bdd-186">否則，請移至下一個區段。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="e0bdd-187">下列費用會使用哪個成本科目？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="e0bdd-188">成本</span><span class="sxs-lookup"><span data-stu-id="e0bdd-188">Cost</span></span>
    - <span data-ttu-id="e0bdd-189">薪資分攤</span><span class="sxs-lookup"><span data-stu-id="e0bdd-189">Payroll allocation</span></span>
    - <span data-ttu-id="e0bdd-190">WIP 成本值</span><span class="sxs-lookup"><span data-stu-id="e0bdd-190">WIP-cost value</span></span>
    - <span data-ttu-id="e0bdd-191">成本項目</span><span class="sxs-lookup"><span data-stu-id="e0bdd-191">Cost-item</span></span>
    - <span data-ttu-id="e0bdd-192">WIP 成本值項目</span><span class="sxs-lookup"><span data-stu-id="e0bdd-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="e0bdd-193">應計損失</span><span class="sxs-lookup"><span data-stu-id="e0bdd-193">Accrued loss</span></span>
    - <span data-ttu-id="e0bdd-194">WIP 應計損失</span><span class="sxs-lookup"><span data-stu-id="e0bdd-194">WIP-accrued loss</span></span>

- <span data-ttu-id="e0bdd-195">下列各項會使用哪個收入科目？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="e0bdd-196">已開發票營收</span><span class="sxs-lookup"><span data-stu-id="e0bdd-196">Invoiced revenue</span></span>
    - <span data-ttu-id="e0bdd-197">應計收入 - 銷售值</span><span class="sxs-lookup"><span data-stu-id="e0bdd-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="e0bdd-198">WIP - 銷售值</span><span class="sxs-lookup"><span data-stu-id="e0bdd-198">WIP-sales value</span></span>
    - <span data-ttu-id="e0bdd-199">應計收入 - 生產</span><span class="sxs-lookup"><span data-stu-id="e0bdd-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="e0bdd-200">WIP - 生產</span><span class="sxs-lookup"><span data-stu-id="e0bdd-200">WIP-production</span></span>
    - <span data-ttu-id="e0bdd-201">應計收入 - 利潤</span><span class="sxs-lookup"><span data-stu-id="e0bdd-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="e0bdd-202">WIP - 利潤</span><span class="sxs-lookup"><span data-stu-id="e0bdd-202">WIP-profit</span></span>
    - <span data-ttu-id="e0bdd-203">應計收入 - 訂閱</span><span class="sxs-lookup"><span data-stu-id="e0bdd-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="e0bdd-204">WIP - 訂閱</span><span class="sxs-lookup"><span data-stu-id="e0bdd-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="e0bdd-205">稅金</span><span class="sxs-lookup"><span data-stu-id="e0bdd-205">Taxes</span></span>

<span data-ttu-id="e0bdd-206">對於費用相關稅金，您必須判斷費用報表中所包含或啟用的項目。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="e0bdd-207">**決策：**</span><span class="sxs-lookup"><span data-stu-id="e0bdd-207">**Decisions:**</span></span>

- <span data-ttu-id="e0bdd-208">銷售稅是否包含在費用金額中？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="e0bdd-209">是否應在費用上啟用稅金退還？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0bdd-210">規劃總帳當時，如果您已決定套用美國銷售稅並使用課稅規則，則無法在費用上啟用稅金退還。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="e0bdd-211">(若要套用美國銷售稅並使用課稅規則，請將 **套用銷售稅課稅規則** 選項設定為 **是**)。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="e0bdd-212">原則</span><span class="sxs-lookup"><span data-stu-id="e0bdd-212">Policies</span></span>

<span data-ttu-id="e0bdd-213">您可以建立費用報表原則，協助組織在員工代表其開支費用時節省時間和金錢。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="e0bdd-214">原則有助於保證員工不超出預算、提供所有必要資訊，並且只在需要時花費資金。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="e0bdd-215">您必須對每個費用報表原則以及每個您所建立的費用報表核准原則做出下列決定。</span><span class="sxs-lookup"><span data-stu-id="e0bdd-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="e0bdd-216">**決策：**</span><span class="sxs-lookup"><span data-stu-id="e0bdd-216">**Decisions:**</span></span>

- <span data-ttu-id="e0bdd-217">原則的名稱是什麼？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-217">What is the name of the policy?</span></span>
- <span data-ttu-id="e0bdd-218">費用原則的目的是什麼？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-218">What is the expense policy for?</span></span>
- <span data-ttu-id="e0bdd-219">如果先前已決定要啟用公司間費用，您組織中的哪些公司將會套用此原則？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="e0bdd-220">原則何時生效？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-220">When does the policy become effective?</span></span>
- <span data-ttu-id="e0bdd-221">原則何時到期？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-221">When does the policy expire?</span></span>
- <span data-ttu-id="e0bdd-222">什麼是原則規則？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-222">What is the policy rule?</span></span>
- <span data-ttu-id="e0bdd-223">原則規則的結果是什麼？</span><span class="sxs-lookup"><span data-stu-id="e0bdd-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]