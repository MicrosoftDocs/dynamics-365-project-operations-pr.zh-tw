---
title: 報價 - 重要概念 - 精簡
description: 本主題提供有關在 Project Operations 中使用專案報價的資訊。
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bd225bfea6e04839b57dfcc9436315fe1cd6a204
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994262"
---
# <a name="concepts-unique-to-project-quotes"></a><span data-ttu-id="8a2f9-103">專案報價獨有的概念</span><span class="sxs-lookup"><span data-stu-id="8a2f9-103">Concepts unique to Project quotes</span></span>

<span data-ttu-id="8a2f9-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="8a2f9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="8a2f9-105">以下是在 Dynamics 365 Project Operations 中開始使用專案報價之前，需注意的重要概念：</span><span class="sxs-lookup"><span data-stu-id="8a2f9-105">The following are key concepts to be aware of before you begin using project quotes in Dynamics 365 Project Operations:</span></span>

## <a name="contracting-unit"></a><span data-ttu-id="8a2f9-106">合約單位</span><span class="sxs-lookup"><span data-stu-id="8a2f9-106">Contracting unit</span></span>

<span data-ttu-id="8a2f9-107">合約單位代表負責專案交付的部門或業務單位。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-107">The contracting unit represents the division or practice that owns the project delivery.</span></span> <span data-ttu-id="8a2f9-108">您可以設定每個合約單位的資源成本。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-108">You can set up resource costs for each contracting unit.</span></span> <span data-ttu-id="8a2f9-109">指定合約單位資源的資源成本時，您也可以為此合約單位所借用的資源，或是企業中的其他部門或業務單位設定不同的成本費率。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-109">When you specify resource cost for a resource in the contracting unit, you will also be able to set up different cost rates for resources that this contracting unit borrows from, or other division or practices within the enterprise.</span></span> <span data-ttu-id="8a2f9-110">這些即稱為轉撥價格、資源借用或借調價格。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-110">These are referred to as transfer prices, resource borrowing, or exchange prices.</span></span> <span data-ttu-id="8a2f9-111">設定從其他部門借用資源的成本時，您也可以選擇以出借部門的貨幣來設定這些成本費率。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-111">When you set up the cost of borrowing resources from other divisions, you can also choose to set up those cost rates in the currency of the lending division.</span></span>

## <a name="cost-currency"></a><span data-ttu-id="8a2f9-112">成本貨幣</span><span class="sxs-lookup"><span data-stu-id="8a2f9-112">Cost currency</span></span>

<span data-ttu-id="8a2f9-113">Project Operations 中的成本貨幣是用來報告成本的貨幣。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-113">Cost currency in Project Operations is the currency in which costs are reported.</span></span> <span data-ttu-id="8a2f9-114">此貨幣是取自報價、合約及專案上附加至 **合約單位** 欄位的貨幣。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-114">This currency is derived from the currency attached to the **Contracting unit** field on the quote, contract, and project.</span></span> <span data-ttu-id="8a2f9-115">您可以在專案上使用任何貨幣來記錄成本。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-115">Costs can be logged in any currency against a project.</span></span> <span data-ttu-id="8a2f9-116">不過，從記錄成本所用貨幣到專案的成本貨幣之間會發生貨幣轉換。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-116">However, there is currency conversion from the currency costs were recorded in, to the cost currency of the project.</span></span>

<span data-ttu-id="8a2f9-117">因為 CDS 平台中的匯率無法即日生效，如果您更新貨幣匯率，畫面上的總計成本可能會隨時間改變。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-117">Because of the exchange rates in the CDS platform can't be date-effective, the on-screen totals for cost may change over time if you update currency exchange rates.</span></span> <span data-ttu-id="8a2f9-118">不過，在資料庫中記錄的成本仍會保持不變，因為金額是以其開支的貨幣來儲存。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-118">However, costs recorded in the database remain unchanged because the amounts are stored in the currency that they were incurred in.</span></span>

## <a name="sales-currency"></a><span data-ttu-id="8a2f9-119">銷售貨幣</span><span class="sxs-lookup"><span data-stu-id="8a2f9-119">Sales currency</span></span>

<span data-ttu-id="8a2f9-120">Project Operations 中的銷售貨幣是記錄和顯示估計及實際銷售金額所用的貨幣。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-120">Sales currency in Project Operations is the currency in which the estimated and actual sales amounts are recorded and shown.</span></span> <span data-ttu-id="8a2f9-121">這也是開立交易發票給客戶所用的貨幣。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-121">It is also the currency in which the customer is invoiced for the deal.</span></span> <span data-ttu-id="8a2f9-122">在專案報價上，預設會使用客戶或客戶記錄的銷售貨幣，而且可以在建立報價時變更。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-122">On a project quote, the sales currency defaults from the customer or account record and can be changed when the quote is created.</span></span> <span data-ttu-id="8a2f9-123">儲存報價後，就無法變更銷售貨幣。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-123">After the quote is saved, the sales currency can't be changed.</span></span> <span data-ttu-id="8a2f9-124">產品及專案價目表會根據報價的銷售貨幣設定預設值。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-124">Product and project price lists default based on the sales currency of the quote.</span></span>

<span data-ttu-id="8a2f9-125">與成本不同，銷售值只能以銷售貨幣來記錄。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-125">Unlike costs, sales values can only be recorded in the Sales currency.</span></span>

## <a name="billing-method"></a><span data-ttu-id="8a2f9-126">帳務方式</span><span class="sxs-lookup"><span data-stu-id="8a2f9-126">Billing method</span></span>

<span data-ttu-id="8a2f9-127">專案通常有基於固定費用和耗用量的合約模型。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-127">Projects typically have fixed fee and consumption-based contracting models.</span></span> <span data-ttu-id="8a2f9-128">這在 Project Operations 中以 **帳務方式** 來表示，並且有兩個值，即 [時間和材料] 與 [固定價格]。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-128">This is represented in Project Operations as **Billing Method** and has two values, time and material and fixed price.</span></span>

- <span data-ttu-id="8a2f9-129">**時間和材料：** 這是基於耗用量的合約模型，其中產生每項成本都對應的營收為背景來源。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-129">**Time and material:** This is a consumption-based contract model where each cost incurred is backed by corresponding revenue.</span></span> <span data-ttu-id="8a2f9-130">當您估計或產生更多成本時，對應的估計和實際銷售也會增加。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-130">As you estimate or incur more costs, the corresponding estimated and actual sales will also increase.</span></span> <span data-ttu-id="8a2f9-131">您可以在使用此帳務方式的報價明細上指定不得超過的限制。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-131">You can specify not-to-exceed limits on quote lines that have this billing method.</span></span> <span data-ttu-id="8a2f9-132">這會設定實際營收的上限。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-132">This will cap off the actual revenue.</span></span> <span data-ttu-id="8a2f9-133">估計的營收不受不得超過的限制所影響。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-133">Estimated revenue is not impacted by not-to-exceed limits.</span></span>
- <span data-ttu-id="8a2f9-134">**固定價格：** 這是固定費用合約模型，表示銷售值將與產生的成本無關。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-134">**Fixed price:** This is a fixed fee contract model that indicates the sales values will be independent of the costs incurred.</span></span> <span data-ttu-id="8a2f9-135">銷售值已固定，不會因為您估計或產生更多成本而改變。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-135">The sales value is fixed and does not change as you estimate or incur more costs.</span></span>

## <a name="project-price-lists"></a><span data-ttu-id="8a2f9-136">專案價目表</span><span class="sxs-lookup"><span data-stu-id="8a2f9-136">Project price lists</span></span>

<span data-ttu-id="8a2f9-137">專案價目表是用來設定時間、費用及其他專案相關元件預設價格 (不是預設成本費率) 的價目表。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-137">Project price lists are price lists that are used to default prices, not cost rates, for time, expense, and other project-related components.</span></span> <span data-ttu-id="8a2f9-138">可以有多份價目表，而每一份價目表都可以為個別專案報價提供其本身的有效日期範圍。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-138">There can be multiple prices lists, and each list can have its own date effectivity for each project quote.</span></span> <span data-ttu-id="8a2f9-139">Project Operations 不支援專案價目表的有效日期範圍重疊。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-139">Overlapping date effectivity on project price lists is not supported in Project Operations.</span></span>

## <a name="product-price-lists"></a><span data-ttu-id="8a2f9-140">產品價目表</span><span class="sxs-lookup"><span data-stu-id="8a2f9-140">Product price lists</span></span>

<span data-ttu-id="8a2f9-141">產品價目表是在報價上用來設定產品型明細預設價格 (而不是預設成本費率) 的價目表。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-141">Product price lists are price lists that are used to default prices, not cost rates, for product-based lines on a quote.</span></span> <span data-ttu-id="8a2f9-142">每個報價只有一份產品價目表。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-142">There is only one product price list per quote.</span></span>

## <a name="transaction-classes"></a><span data-ttu-id="8a2f9-143">交易分類</span><span class="sxs-lookup"><span data-stu-id="8a2f9-143">Transaction classes</span></span>

<span data-ttu-id="8a2f9-144">Project Operations 支援四種類型的交易分類：</span><span class="sxs-lookup"><span data-stu-id="8a2f9-144">Project Operations supports four types of transaction classes:</span></span>

- <span data-ttu-id="8a2f9-145">時間</span><span class="sxs-lookup"><span data-stu-id="8a2f9-145">Time</span></span>
- <span data-ttu-id="8a2f9-146">費用</span><span class="sxs-lookup"><span data-stu-id="8a2f9-146">Expense</span></span>
- <span data-ttu-id="8a2f9-147">資料</span><span class="sxs-lookup"><span data-stu-id="8a2f9-147">Material</span></span>
- <span data-ttu-id="8a2f9-148">費用</span><span class="sxs-lookup"><span data-stu-id="8a2f9-148">Fee</span></span>

<span data-ttu-id="8a2f9-149">成本值和銷售值可以在 [時間]、[費用] 和 [材料] 交易分類上進行估計和列計。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-149">Cost and sales values can be estimated and incurred on Time, Expense, and Material transaction classes.</span></span> <span data-ttu-id="8a2f9-150">服務費是營收專屬交易分類。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-150">Fee is a revenue only class of transactions.</span></span>

## <a name="work-entities-and-billing-entities"></a><span data-ttu-id="8a2f9-151">工作實體和帳單實體</span><span class="sxs-lookup"><span data-stu-id="8a2f9-151">Work entities and billing entities</span></span>

<span data-ttu-id="8a2f9-152">代表工作的實體是 [專案] 和 [工作]。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-152">Entities that represent work are Projects and Tasks.</span></span> <span data-ttu-id="8a2f9-153">代表帳單的實體是 [報價明細] 和 [合約服務內容]。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-153">Entities that represent billing are Quote lines and Contract lines.</span></span> <span data-ttu-id="8a2f9-154">您可以建立將不同工作實體與 [報價明細] 及 [合約服務內容] 的關聯，藉此將這些實體連結至帳單選項。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-154">You can link different work entities to billing options by associating them with Quote or Contract lines.</span></span>

## <a name="multi-customer-deals"></a><span data-ttu-id="8a2f9-155">多客戶交易</span><span class="sxs-lookup"><span data-stu-id="8a2f9-155">Multi-customer deals</span></span>

<span data-ttu-id="8a2f9-156">有多個客戶要開立發票時，就會發生多客戶交易。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-156">Multi-customer deals occur are when there is more than one customer to invoice.</span></span> <span data-ttu-id="8a2f9-157">常見的範例包括：</span><span class="sxs-lookup"><span data-stu-id="8a2f9-157">Common examples of this include:</span></span>

- <span data-ttu-id="8a2f9-158">**OEM 企業及其合作夥伴：** 合作夥伴和轉銷商會搭配加值服務來銷售產品。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-158">**OEM Enterprises and their partners:** Partners and resellers sell a product with value-added services.</span></span> <span data-ttu-id="8a2f9-159">這通常是與客戶進行特定交易時，OEM 要提供部分專案資金的案例。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-159">This is usually a scenario where during a particular deal with a customer, the OEM offers to finance a portion of the project.</span></span> 

- <span data-ttu-id="8a2f9-160">**公共事業專案：** 多個當地政府部門同意資助專案，並依據先前議定的分攤額度來開立發票。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-160">**Public sector projects:** Multiple departments of a local government agree to fund a project and are invoiced according to a previously agreed split.</span></span> <span data-ttu-id="8a2f9-161">例如，學區和城市或當地政府部門同意資助興建游泳池。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-161">For example, a school district and the city or local government department agree to fund the building of a swimming pool.</span></span>

## <a name="invoice-schedules"></a><span data-ttu-id="8a2f9-162">發票排程</span><span class="sxs-lookup"><span data-stu-id="8a2f9-162">Invoice schedules</span></span>

<span data-ttu-id="8a2f9-163">發票排程是每個報價明細特定的排程，而且也是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-163">Invoice schedules are specific to each quote line and are also optional.</span></span> <span data-ttu-id="8a2f9-164">發票排程是根據特定開始和完成日期以及發票週期所建立。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-164">Invoice schedules are created based on certain start and finish dates and invoice frequency.</span></span> <span data-ttu-id="8a2f9-165">設定自動發票建立程序時，會在合約階段中使用發票排程。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-165">Invoice schedules are used in the contract stage when the automatic invoice creation process is configured.</span></span> <span data-ttu-id="8a2f9-166">在報價階段中，排程是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-166">In the quote stage, the schedules are optional.</span></span> <span data-ttu-id="8a2f9-167">在 **報價** 階段建立發票排程時，這些排程會複製到專案報價成交時所建立的專案合約。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-167">When invoice schedules are created in the **Quote** stage, they are copied to the project contract that is created when a project quote is won.</span></span>

## <a name="changes-from-dynamics-365-sales-quote"></a><span data-ttu-id="8a2f9-168">Dynamics 365 Sales 報價發生的變更：</span><span class="sxs-lookup"><span data-stu-id="8a2f9-168">Changes from Dynamics 365 Sales quote:</span></span>

<span data-ttu-id="8a2f9-169">Project Operations 報價是建立在 Dynamics 365 Sales 報價的基礎上。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-169">Project Operations quotes are built on the Dynamics 365 Sales quotes.</span></span> <span data-ttu-id="8a2f9-170">不過，您會在功能上注意到一些重要差異：</span><span class="sxs-lookup"><span data-stu-id="8a2f9-170">However, there are some important differences in functionality that you should be aware of:</span></span>

- <span data-ttu-id="8a2f9-171">不支援 **修訂** 和 **啟用** 動作。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-171">The **Revise** and **Activate** actions are not supported.</span></span>
- <span data-ttu-id="8a2f9-172">Project Operations 報價有兩種不同類型的明細。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-172">Project Operations quotes have two different types of lines.</span></span> <span data-ttu-id="8a2f9-173">一個用於專案，另一個用於產品。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-173">One is for projects and the other is for products.</span></span>
- <span data-ttu-id="8a2f9-174">Project Operations 報價有其本身的表單以及 UI 元素、商務規則、外掛程式中的商務規則，以及使其與 Sales 報價有所不同的用戶端指令碼。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-174">Project Operations quotes have their own form and UI elements, business rules, business logic in plug-ins, and client-side scripts that make them unique from Sales quotes.</span></span>

<span data-ttu-id="8a2f9-175">因此，不建議互換使用 Sales 報價與 Project Operations 報價。</span><span class="sxs-lookup"><span data-stu-id="8a2f9-175">For these reasons, it is not recommended to use a Sales quote and a Project Operations quote interchangeably.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
