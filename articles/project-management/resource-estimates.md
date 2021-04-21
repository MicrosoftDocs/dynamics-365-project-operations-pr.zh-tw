---
title: 專案的資源時間財務估計值
description: 本主題提供有關如何計算時間財務估計值的資訊。
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91156c5cf79af8c66c12b84a6d2b17aa7fe09ed1
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701816"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a><span data-ttu-id="955e9-103">專案的資源時間財務估計值</span><span class="sxs-lookup"><span data-stu-id="955e9-103">Financial estimates for resource time on projects</span></span>

<span data-ttu-id="955e9-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="955e9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="955e9-105">根據三個因素計算時間財務估計值：</span><span class="sxs-lookup"><span data-stu-id="955e9-105">Financial estimates for time are calculated based on three factors:</span></span> 

- <span data-ttu-id="955e9-106">指派至專案計劃中每個分葉節點工作之一般或具名團隊成員的類型。</span><span class="sxs-lookup"><span data-stu-id="955e9-106">The type of generic or named team member assigned to each leaf node task on the project plan.</span></span> 
- <span data-ttu-id="955e9-107">工作的類型或複雜度。</span><span class="sxs-lookup"><span data-stu-id="955e9-107">The type or complexity of work.</span></span>
- <span data-ttu-id="955e9-108">資源指派在工作上分攤的投入量。</span><span class="sxs-lookup"><span data-stu-id="955e9-108">The spread of effort for the resource's assignment on the task.</span></span> 

<span data-ttu-id="955e9-109">前兩個因素會影響資源指派的單位成本或帳單費率。</span><span class="sxs-lookup"><span data-stu-id="955e9-109">The first two factors influence the unit cost or bill rate of a resource's assignment.</span></span> <span data-ttu-id="955e9-110">資源指派的單位成本或帳單費率是由已指派資源的屬性所決定。</span><span class="sxs-lookup"><span data-stu-id="955e9-110">The unit cost or bill rate of a resource assignment is determined by the attributes of the resource assigned.</span></span> <span data-ttu-id="955e9-111">這些屬性包括資源所屬的組織單位和資源的標準角色。</span><span class="sxs-lookup"><span data-stu-id="955e9-111">These attributes include the organizational unit to which the resource belongs and the standard role of the resource.</span></span> <span data-ttu-id="955e9-112">您也可以新增與資源業務的相關自訂屬性 (例如標準職稱或經驗等級)，並讓這些屬性影響指派的單位成本或帳單費率。</span><span class="sxs-lookup"><span data-stu-id="955e9-112">You can also add custom attributes relevant to your business for the resource, like standard title or experience level, and have them influence the unit cost or bill rate of the assignment.</span></span>
<span data-ttu-id="955e9-113">除了資源的屬性之外，工作的屬性 (例如任務) 也會影響指派的單位帳單費率或成本費率。</span><span class="sxs-lookup"><span data-stu-id="955e9-113">In addition to the attributes of the resource, attributes of work, such as the task, can also influence the unit bill rate or cost rate of the assignment.</span></span> <span data-ttu-id="955e9-114">例如，特定工作較為複雜時，資源在這些特定工作中的指派會產生比複雜度較低工作還要高的單位成本或帳單費率。</span><span class="sxs-lookup"><span data-stu-id="955e9-114">For example, when certain tasks are more complex, the resource's assignment to those specific tasks result in a higher unit cost or bill rate than tasks that are less complex.</span></span>   

<span data-ttu-id="955e9-115">第三個因素按照該費率提供時數。</span><span class="sxs-lookup"><span data-stu-id="955e9-115">The third factor provides the quantity of hours at that rate.</span></span> <span data-ttu-id="955e9-116">在工作涵蓋兩個價格期間的情況下，該工作的資源指派的第一部分可能會在成本計算和定價方式上與工作的第二部分不同。</span><span class="sxs-lookup"><span data-stu-id="955e9-116">In cases where a task covers two price periods, it is likely that the first part of the resource assignment for that task is costed and priced differently than the second portion of the task.</span></span> <span data-ttu-id="955e9-117">每個資源指派上的投入量估計值是以每天投入量的每日分佈來儲存的複雜值。</span><span class="sxs-lookup"><span data-stu-id="955e9-117">The effort estimate on each resource assignment is a complex value stored with the daily distribution of effort per day.</span></span>

<span data-ttu-id="955e9-118">如需有關如何將工作和資源的自訂屬性設定為定價和成本計算維度的詳細指示，請參閱[定價維度概觀](../pricing-costing/pricing-dimensions-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="955e9-118">For detailed instructions about how to set up custom attributes of work and resources as pricing and costing dimensions, see [Pricing Dimensions overview](../pricing-costing/pricing-dimensions-overview.md).</span></span>

<span data-ttu-id="955e9-119">每個資源指派的財務估計值是以 **指派的每小時費率乘以時數** 的方式進行計算。</span><span class="sxs-lookup"><span data-stu-id="955e9-119">The financial estimate on each resource assignment is calculated as **rate/hr for the assignment multiplied by the number of hours.**</span></span>  <span data-ttu-id="955e9-120">與投入量估計類似，每個資源指派的成本和收入財務估計值都是以每天貨幣金額的每日分佈來儲存的複雜值。</span><span class="sxs-lookup"><span data-stu-id="955e9-120">Similar to the effort estimate, the financial estimate for cost and revenue for each resource assignment is a complex value stored with the daily distribution of monetary amount per day.</span></span> 

## <a name="summarizing-financial-estimates-for-time"></a><span data-ttu-id="955e9-121">彙總時間的財務估計值</span><span class="sxs-lookup"><span data-stu-id="955e9-121">Summarizing financial estimates for time</span></span>
<span data-ttu-id="955e9-122">分葉節點工作的時間財務估計值即是該工作所有資源指派的財務估計值加總。</span><span class="sxs-lookup"><span data-stu-id="955e9-122">A financial estimate for time on a leaf node task is the sum of the financial estimates on all resource assignments for that task.</span></span>

<span data-ttu-id="955e9-123">摘要或上層工作的時間財務估計值則是其所有下層工作的財務估計值加總。</span><span class="sxs-lookup"><span data-stu-id="955e9-123">A financial estimate for time on a summary or parent task is the sum of the financial estimates on all of its child tasks.</span></span> <span data-ttu-id="955e9-124">這是專案的估計人力成本。</span><span class="sxs-lookup"><span data-stu-id="955e9-124">This is the estimated labor cost on the project.</span></span> 

![資源估計值](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="955e9-126">預設成本價與成本貨幣</span><span class="sxs-lookup"><span data-stu-id="955e9-126">Default cost price and cost currency</span></span>

<span data-ttu-id="955e9-127">預設成本價來自附加至專案合約單位的價目表。</span><span class="sxs-lookup"><span data-stu-id="955e9-127">The default cost price comes from the price lists attached to the contracting unit of the project.</span></span> <span data-ttu-id="955e9-128">專案的成本貨幣永遠是專案合約單位的貨幣。</span><span class="sxs-lookup"><span data-stu-id="955e9-128">The cost currency of a project is always the currency of the contracting unit of the project.</span></span> <span data-ttu-id="955e9-129">在資源指派上，成本的財務估計值是以專案的成本貨幣來儲存。</span><span class="sxs-lookup"><span data-stu-id="955e9-129">On a resource assignment, the financial estimate for cost is stored in the cost currency of the project.</span></span> <span data-ttu-id="955e9-130">價目表中設定成本費率所用的貨幣有時與專案的成本貨幣不同。</span><span class="sxs-lookup"><span data-stu-id="955e9-130">Sometimes, the currency in which the cost rate is set up in the price list is different from the project's cost currency.</span></span> <span data-ttu-id="955e9-131">在這些情況下，應用程式會轉換專案貨幣設定成本價所用的貨幣。</span><span class="sxs-lookup"><span data-stu-id="955e9-131">In these cases, the application converts the currency in which the cost price is set up for the currency of the project.</span></span> <span data-ttu-id="955e9-132">在 **估計值** 網格中，所有成本估計值都是以專案的成本貨幣來顯示和彙總。</span><span class="sxs-lookup"><span data-stu-id="955e9-132">On the **Estimates** grid, all cost estimates are displayed and summarized in the project's cost currency.</span></span> 

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="955e9-133">預設帳單費率與銷售貨幣</span><span class="sxs-lookup"><span data-stu-id="955e9-133">Default bill rate and sales currency</span></span>

<span data-ttu-id="955e9-134">預設銷售價來自附加至相關專案合約的專案價目表 (如果交易已成交)，或來自相關專案報價 (如果交易仍在售前階段中)。</span><span class="sxs-lookup"><span data-stu-id="955e9-134">The default sales price comes from the project price lists attached to the related project contract if the deal is won, or from the related project quote if the deal is still in the pre-sales stage.</span></span> <span data-ttu-id="955e9-135">專案的銷售貨幣永遠是專案報價或專案合約的貨幣。</span><span class="sxs-lookup"><span data-stu-id="955e9-135">The sales currency of the project is always the currency of the project quote or the project contract.</span></span> <span data-ttu-id="955e9-136">在資源指派上，銷售的財務估計值是以專案的銷售貨幣來儲存。</span><span class="sxs-lookup"><span data-stu-id="955e9-136">On a resource assignment, the financial estimate for sales is stored in the sales currency of the project.</span></span> <span data-ttu-id="955e9-137">與成本不同的是，價目表中設定的銷售價永遠不會與專案的銷售貨幣不同。</span><span class="sxs-lookup"><span data-stu-id="955e9-137">Unlike cost, the sales price that is set up in the price list can never be different from the project's sales currency.</span></span> <span data-ttu-id="955e9-138">沒有任何需要進行貨幣轉換的案例。</span><span class="sxs-lookup"><span data-stu-id="955e9-138">There is no scenario where currency conversion is needed.</span></span> <span data-ttu-id="955e9-139">在 **估計值** 網格中，所有銷售估計值都是以專案的銷售貨幣來顯示和彙總。</span><span class="sxs-lookup"><span data-stu-id="955e9-139">On the **Estimates** grid, all sales estimates are displayed and summarized in the project's sales currency.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
