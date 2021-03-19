---
title: 專案合約
description: 本主題提供您可為各種類型專案和資金來源建立的專案合約範例，以及如何管理合約和開具專案發票給客戶的方式。
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53eb6ff3f98e7efc3d6b997cd4d877025225936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289539"
---
# <a name="project-contracts"></a><span data-ttu-id="0a724-103">專案合約</span><span class="sxs-lookup"><span data-stu-id="0a724-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a724-104">本文提供您可為各種類型專案和資金來源建立的專案合約範例，以及如何管理合約和開具專案發票給客戶的方式。</span><span class="sxs-lookup"><span data-stu-id="0a724-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="0a724-105">您為專案合約建立的專案類型，決定用來向專案客戶開立發票的方法。</span><span class="sxs-lookup"><span data-stu-id="0a724-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="0a724-106">您可以變更專案合約及相關專案，但是不能變更專案類型。</span><span class="sxs-lookup"><span data-stu-id="0a724-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="0a724-107">您可以使用專案合約，同時開立一個或多個專案的發票。</span><span class="sxs-lookup"><span data-stu-id="0a724-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="0a724-108">專案合約也有助於保證專案結構中的每個子專案都有一致的發票開立程序。</span><span class="sxs-lookup"><span data-stu-id="0a724-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="0a724-109">每個要開發票的專案都必須與專案合約相關聯。</span><span class="sxs-lookup"><span data-stu-id="0a724-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="0a724-110">專案合約的設定會套用至所有與該專案合約相關聯的專案和子專案。</span><span class="sxs-lookup"><span data-stu-id="0a724-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="0a724-111">專案合約可以指定一個或多個資金來源。</span><span class="sxs-lookup"><span data-stu-id="0a724-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="0a724-112">因此，您可以在多個出資者之間分攤帳單、設定資金限制 (以免向資金來源收取超過特定金額的款項)，以及設定收取費用的資金規則。</span><span class="sxs-lookup"><span data-stu-id="0a724-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="0a724-113">專案合約的資金</span><span class="sxs-lookup"><span data-stu-id="0a724-113">Funding for project contracts</span></span>
<span data-ttu-id="0a724-114">有些專案合約會指定多個當事人共同承擔提供專案成本資金的責任。</span><span class="sxs-lookup"><span data-stu-id="0a724-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="0a724-115">以下列出一些範例：</span><span class="sxs-lookup"><span data-stu-id="0a724-115">Here are some examples:</span></span>

-   <span data-ttu-id="0a724-116">具有多個部門的大型客戶要求專案資金依部門進行分攤。</span><span class="sxs-lookup"><span data-stu-id="0a724-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="0a724-117">您的公司與外部組織共同分攤大型專案的成本。</span><span class="sxs-lookup"><span data-stu-id="0a724-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="0a724-118">道路專案由兩個城市共同出資。</span><span class="sxs-lookup"><span data-stu-id="0a724-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="0a724-119">橋樑專案由政府補助款與私營公司來資助。</span><span class="sxs-lookup"><span data-stu-id="0a724-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="0a724-120">在 Dynamics 365 Finance 中，您可以在多個客戶、補助計劃或組織間，分攤單一交易或整個專案的帳單。</span><span class="sxs-lookup"><span data-stu-id="0a724-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="0a724-121">在有多個出資者的專案中，所有參與事前籌資專案的出資當事人都會稱為資金來源。</span><span class="sxs-lookup"><span data-stu-id="0a724-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="0a724-122">將客戶、組織或補助計劃定義為資金來源後，即可將其指派至一個或多個資金規則。</span><span class="sxs-lookup"><span data-stu-id="0a724-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="0a724-123">資金規則包含的準則決定如何將費用配置到專案的各個不同資金來源。</span><span class="sxs-lookup"><span data-stu-id="0a724-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="0a724-124">因為庫存項目 (例如在請購單和採購單上出現的項目) 無法分攤，分佈時無法在多個資金來源之間分攤成本金額。</span><span class="sxs-lookup"><span data-stu-id="0a724-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="0a724-125">因此，將庫存發放過帳之前，資金來源值會一直保持為 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="0a724-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="0a724-126">將庫存發放過帳時，成本金額會根據專案的帳戶分配規則來分攤。</span><span class="sxs-lookup"><span data-stu-id="0a724-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="0a724-127">以下是一些您可採行來讓帳單更易於在多個資金來源之間分攤的步驟：</span><span class="sxs-lookup"><span data-stu-id="0a724-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="0a724-128">指定所有為專案輸入的交易都要使用與專案合約相同的銷售貨幣。</span><span class="sxs-lookup"><span data-stu-id="0a724-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="0a724-129">設定資金限制，以免向資金來源開發票請領超過特定金額的專案款項。</span><span class="sxs-lookup"><span data-stu-id="0a724-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="0a724-130">設定每個工作者、項目、類別、類別群組和交易類型 (或所有交易類型) 的資金規則和資金限制。</span><span class="sxs-lookup"><span data-stu-id="0a724-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="0a724-131">選取選擇性開始日期及結束日期，以定義每項資金規則的有效期間。</span><span class="sxs-lookup"><span data-stu-id="0a724-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="0a724-132">指定每個資金來源負責的百分比。</span><span class="sxs-lookup"><span data-stu-id="0a724-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="0a724-133">指定負責資金配置計算所產生捨入差額的資金來源。</span><span class="sxs-lookup"><span data-stu-id="0a724-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="0a724-134">設定規則，決定如何開立專案成本的發票給外部客戶，以及向內部組織收費。</span><span class="sxs-lookup"><span data-stu-id="0a724-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="0a724-135">將交易記錄在保留資金帳戶中，直到可以取得其他資金，或您決定內部承擔成本為止。</span><span class="sxs-lookup"><span data-stu-id="0a724-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="0a724-136">若要判斷與交易有關聯的課稅群組，請在專案中搜尋課稅群組指派。</span><span class="sxs-lookup"><span data-stu-id="0a724-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="0a724-137">如果未在專案層級指派任何課稅群組，則會搜尋專案合約。</span><span class="sxs-lookup"><span data-stu-id="0a724-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="0a724-138">範例：多個資金來源 (簡單)</span><span class="sxs-lookup"><span data-stu-id="0a724-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="0a724-139">下表提供在多個資金來源中管理資金配置的案例。</span><span class="sxs-lookup"><span data-stu-id="0a724-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="0a724-140">這些案例以下列假設為依據：</span><span class="sxs-lookup"><span data-stu-id="0a724-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="0a724-141">資金配置先考慮優先順序設定，再套用其他資金規則準則。</span><span class="sxs-lookup"><span data-stu-id="0a724-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="0a724-142">尚未指定日期範圍來定義資金規則的有效期間。</span><span class="sxs-lookup"><span data-stu-id="0a724-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a724-143"><strong>案例</strong></span><span class="sxs-lookup"><span data-stu-id="0a724-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="0a724-144"><strong>資金來源</strong></span><span class="sxs-lookup"><span data-stu-id="0a724-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="0a724-145"><strong>配置百分比</strong></span><span class="sxs-lookup"><span data-stu-id="0a724-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="0a724-146"><strong>配置優先順序</strong></span><span class="sxs-lookup"><span data-stu-id="0a724-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a724-147">您想要將成本配置到一個資金來源直到資金用完為止，再將成本配置到二個資金來源直到資金用完為止，最後將剩餘成本配置到第三個資金來源。</span><span class="sxs-lookup"><span data-stu-id="0a724-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="0a724-148">資金來源 1</span><span class="sxs-lookup"><span data-stu-id="0a724-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="0a724-149">資金來源 2</span><span class="sxs-lookup"><span data-stu-id="0a724-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="0a724-150">資金來源 3</span><span class="sxs-lookup"><span data-stu-id="0a724-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a724-151">100%</span><span class="sxs-lookup"><span data-stu-id="0a724-151">100%</span></span></li>
<li><span data-ttu-id="0a724-152">100%</span><span class="sxs-lookup"><span data-stu-id="0a724-152">100%</span></span></li>
<li><span data-ttu-id="0a724-153">100%</span><span class="sxs-lookup"><span data-stu-id="0a724-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a724-154">7</span><span class="sxs-lookup"><span data-stu-id="0a724-154">1</span></span></li>
<li><span data-ttu-id="0a724-155">2</span><span class="sxs-lookup"><span data-stu-id="0a724-155">2</span></span></li>
<li><span data-ttu-id="0a724-156">3</span><span class="sxs-lookup"><span data-stu-id="0a724-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a724-157">您想要將 75% 的成本配置到一個資金來源，並將 25% 配置到另一個資金來源。</span><span class="sxs-lookup"><span data-stu-id="0a724-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="0a724-158">當這任一資金來源用盡時，您想要透過第三個資金來源支付剩餘成本。</span><span class="sxs-lookup"><span data-stu-id="0a724-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="0a724-159">資金來源 1</span><span class="sxs-lookup"><span data-stu-id="0a724-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="0a724-160">資金來源 2</span><span class="sxs-lookup"><span data-stu-id="0a724-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="0a724-161">資金來源 3</span><span class="sxs-lookup"><span data-stu-id="0a724-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a724-162">75%</span><span class="sxs-lookup"><span data-stu-id="0a724-162">75%</span></span></li>
<li><span data-ttu-id="0a724-163">25%</span><span class="sxs-lookup"><span data-stu-id="0a724-163">25%</span></span></li>
<li><span data-ttu-id="0a724-164">100%</span><span class="sxs-lookup"><span data-stu-id="0a724-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a724-165">7</span><span class="sxs-lookup"><span data-stu-id="0a724-165">1</span></span></li>
<li><span data-ttu-id="0a724-166">7</span><span class="sxs-lookup"><span data-stu-id="0a724-166">1</span></span></li>
<li><span data-ttu-id="0a724-167">2</span><span class="sxs-lookup"><span data-stu-id="0a724-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a724-168">您想要將 75% 的成本配置到一個資金來源，並將 25% 配置到另一個資金來源。</span><span class="sxs-lookup"><span data-stu-id="0a724-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="0a724-169">當這任一資金來源用盡時，您想要在第三個資金來源與第四個資金來源之間分攤剩餘成本。</span><span class="sxs-lookup"><span data-stu-id="0a724-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="0a724-170">資金來源 1</span><span class="sxs-lookup"><span data-stu-id="0a724-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="0a724-171">資金來源 2</span><span class="sxs-lookup"><span data-stu-id="0a724-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="0a724-172">資金來源 3</span><span class="sxs-lookup"><span data-stu-id="0a724-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="0a724-173">資金來源 4</span><span class="sxs-lookup"><span data-stu-id="0a724-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a724-174">75%</span><span class="sxs-lookup"><span data-stu-id="0a724-174">75%</span></span></li>
<li><span data-ttu-id="0a724-175">25%</span><span class="sxs-lookup"><span data-stu-id="0a724-175">25%</span></span></li>
<li><span data-ttu-id="0a724-176">50%</span><span class="sxs-lookup"><span data-stu-id="0a724-176">50%</span></span></li>
<li><span data-ttu-id="0a724-177">50%</span><span class="sxs-lookup"><span data-stu-id="0a724-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a724-178">7</span><span class="sxs-lookup"><span data-stu-id="0a724-178">1</span></span></li>
<li><span data-ttu-id="0a724-179">7</span><span class="sxs-lookup"><span data-stu-id="0a724-179">1</span></span></li>
<li><span data-ttu-id="0a724-180">2</span><span class="sxs-lookup"><span data-stu-id="0a724-180">2</span></span></li>
<li><span data-ttu-id="0a724-181">2</span><span class="sxs-lookup"><span data-stu-id="0a724-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a724-182">您想要將前 25% 的成本配置到一個資金來源，再將剩餘成本配置到另一個資金來源。</span><span class="sxs-lookup"><span data-stu-id="0a724-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="0a724-183">資金來源 1</span><span class="sxs-lookup"><span data-stu-id="0a724-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="0a724-184">資金來源 2</span><span class="sxs-lookup"><span data-stu-id="0a724-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a724-185">25%</span><span class="sxs-lookup"><span data-stu-id="0a724-185">25%</span></span></li>
<li><span data-ttu-id="0a724-186">100%</span><span class="sxs-lookup"><span data-stu-id="0a724-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a724-187">7</span><span class="sxs-lookup"><span data-stu-id="0a724-187">1</span></span></li>
<li><span data-ttu-id="0a724-188">2</span><span class="sxs-lookup"><span data-stu-id="0a724-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="0a724-189">範例：多個資金來源 (複雜)</span><span class="sxs-lookup"><span data-stu-id="0a724-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="0a724-190">您有三個要依下列順序使用的資金來源：</span><span class="sxs-lookup"><span data-stu-id="0a724-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="0a724-191">均等使用資金來源 2 和資金來源 3，直到資金來源 2 用盡為止。</span><span class="sxs-lookup"><span data-stu-id="0a724-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="0a724-192">繼續使用資金來源 3，直到其用盡為止。</span><span class="sxs-lookup"><span data-stu-id="0a724-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="0a724-193">在資金來源 3 用盡後，使用資金來源 1。</span><span class="sxs-lookup"><span data-stu-id="0a724-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="0a724-194">若要達成此目標，您必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="0a724-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="0a724-195">針對資金來源 2 和資金來源 3 各自的金額，分別設定其資金限制。</span><span class="sxs-lookup"><span data-stu-id="0a724-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="0a724-196">建立下列資金規則：</span><span class="sxs-lookup"><span data-stu-id="0a724-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="0a724-197">規則 1 (優先順序 1)：將 50% 的交易配置到資金來源 2，並將 50% 配置到資金來源 3。</span><span class="sxs-lookup"><span data-stu-id="0a724-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="0a724-198">規則 2 (優先順序 2)：將 100% 的交易配置到資金來源 3。</span><span class="sxs-lookup"><span data-stu-id="0a724-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="0a724-199">規則 3 (優先順序 3)：將 100% 的交易配置到資金來源 1。</span><span class="sxs-lookup"><span data-stu-id="0a724-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="0a724-200">此設定會有作用，因為已依據規則和限制對交易進行檢查，以判斷是否有其中任一項套用至交易。</span><span class="sxs-lookup"><span data-stu-id="0a724-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="0a724-201">如果沒有特定規則或限制套用至交易，則會套用所有交易規則。</span><span class="sxs-lookup"><span data-stu-id="0a724-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="0a724-202">所有交易規則會比對所有交易。</span><span class="sxs-lookup"><span data-stu-id="0a724-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="0a724-203">如果找到與交易適配的規則，就會先套用在該規則中已配置的百分比，但是只有在根據任何已設定的限制檢查了適配的規則時才會進行套用。</span><span class="sxs-lookup"><span data-stu-id="0a724-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="0a724-204">如果已符合限制，且資金來源的資金已用盡，則會忽略與資金限制相關聯的資金規則，而且此程式會檢查是否有下一個適用的規則。</span><span class="sxs-lookup"><span data-stu-id="0a724-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="0a724-205">在某些情況下，只有一部分交易可以根據規則進行配置。</span><span class="sxs-lookup"><span data-stu-id="0a724-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="0a724-206">此情況可能會因為配置交易時已達限制而發生。</span><span class="sxs-lookup"><span data-stu-id="0a724-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="0a724-207">在這種情況下，只會根據該規則配置特定金額，例如將 50% 配置到每個資金來源。</span><span class="sxs-lookup"><span data-stu-id="0a724-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="0a724-208">這是規則 1 中的案例，本節稍早已做說明。</span><span class="sxs-lookup"><span data-stu-id="0a724-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="0a724-209">剩餘部分會根據順序中的下一個規則進行配置。</span><span class="sxs-lookup"><span data-stu-id="0a724-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="0a724-210">下表更加詳細地研究此案例。</span><span class="sxs-lookup"><span data-stu-id="0a724-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a724-211"><strong>焦點</strong></span><span class="sxs-lookup"><span data-stu-id="0a724-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="0a724-212"><strong>詳細資料</strong></span><span class="sxs-lookup"><span data-stu-id="0a724-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a724-213">資金規則</span><span class="sxs-lookup"><span data-stu-id="0a724-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="0a724-214">規則 1 (優先順序 1)：所有交易。</span><span class="sxs-lookup"><span data-stu-id="0a724-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="0a724-215">以 50% 配置資金來源 2，並以 50% 配置資金來源 3。</span><span class="sxs-lookup"><span data-stu-id="0a724-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="0a724-216">規則 2 (優先順序 2)：所有交易。</span><span class="sxs-lookup"><span data-stu-id="0a724-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="0a724-217">以 100% 配置資金來源 3。</span><span class="sxs-lookup"><span data-stu-id="0a724-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="0a724-218">規則 3 (優先順序 2)：所有交易。</span><span class="sxs-lookup"><span data-stu-id="0a724-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="0a724-219">以 100% 配置資金來源 1。</span><span class="sxs-lookup"><span data-stu-id="0a724-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a724-220">資金限制</span><span class="sxs-lookup"><span data-stu-id="0a724-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="0a724-221">資金來源 1 限制 = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="0a724-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="0a724-222">資金來源 2 限制 = 500.00</span><span class="sxs-lookup"><span data-stu-id="0a724-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="0a724-223">資金來源 3 限制 = 750.00</span><span class="sxs-lookup"><span data-stu-id="0a724-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a724-224">交易 1</span><span class="sxs-lookup"><span data-stu-id="0a724-224">Transaction 1</span></span></td>
<td><span data-ttu-id="0a724-225"><strong>交易金額：</strong>100.00<strong>資金：</strong>僅根據規則 1 支付此交易，因為套用規則 1 之後，交易就會獲得全額支付。</span><span class="sxs-lookup"><span data-stu-id="0a724-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="0a724-226">此交易會獲得資金來源 2 與資金來源 3 之間的均等資助。</span><span class="sxs-lookup"><span data-stu-id="0a724-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="0a724-227">資金來源 2：50.00</span><span class="sxs-lookup"><span data-stu-id="0a724-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="0a724-228">資金來源 3：50.00</span><span class="sxs-lookup"><span data-stu-id="0a724-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a724-229">交易 2</span><span class="sxs-lookup"><span data-stu-id="0a724-229">Transaction 2</span></span></td>
<td><span data-ttu-id="0a724-230"><strong>交易金額：</strong>5,000.00 <strong>資金：</strong>根據這全部三個規則支付此交易。</span><span class="sxs-lookup"><span data-stu-id="0a724-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="0a724-231"><strong>規則 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="0a724-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="0a724-232">資金來源 2：450.00</span><span class="sxs-lookup"><span data-stu-id="0a724-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="0a724-233">資金來源 3：450.00</span><span class="sxs-lookup"><span data-stu-id="0a724-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="0a724-234">
<strong>規則 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="0a724-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="0a724-235">資金來源 3：250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="0a724-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="0a724-236">
<strong>規則 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="0a724-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="0a724-237">資金來源 1：3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="0a724-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a724-238">每個資金來源分佈的總金額</span><span class="sxs-lookup"><span data-stu-id="0a724-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="0a724-239">資金來源 1：3,850.00</span><span class="sxs-lookup"><span data-stu-id="0a724-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="0a724-240">資金來源 2：500.00</span><span class="sxs-lookup"><span data-stu-id="0a724-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="0a724-241">資金來源 3：750.00</span><span class="sxs-lookup"><span data-stu-id="0a724-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="0a724-242">帳單規則</span><span class="sxs-lookup"><span data-stu-id="0a724-242">Billing rules</span></span>
<span data-ttu-id="0a724-243">與客戶交涉專案合約時，您可以定義如何及何時可以為專案上的工作開立發票。</span><span class="sxs-lookup"><span data-stu-id="0a724-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="0a724-244">設定專案合約與專案之後，您可以設定專案的帳單規則。</span><span class="sxs-lookup"><span data-stu-id="0a724-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="0a724-245">帳單規則是根據專案合約中指定的專案條款而定。</span><span class="sxs-lookup"><span data-stu-id="0a724-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="0a724-246">您可以建立的帳單規則，取決於專案合約的條款以及與帳單規則建立關聯的專案類型 (例如時間與材料或固定價格)。</span><span class="sxs-lookup"><span data-stu-id="0a724-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="0a724-247">您可以為專案合約建立多個帳單規則。</span><span class="sxs-lookup"><span data-stu-id="0a724-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="0a724-248">您也可以將帳單規則指派至多個與相同專案合約有關聯且有類似帳務條款的專案。</span><span class="sxs-lookup"><span data-stu-id="0a724-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="0a724-249">您可以設定下列類型的帳單規則：</span><span class="sxs-lookup"><span data-stu-id="0a724-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="0a724-250">**交貨單位** – 完成一個單位的交貨時，向客戶開立發票。</span><span class="sxs-lookup"><span data-stu-id="0a724-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="0a724-251">您可以在合約中定義交貨單位。</span><span class="sxs-lookup"><span data-stu-id="0a724-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="0a724-252">**進度** – 完成指定百分比的專案部分時，向客戶開立發票。</span><span class="sxs-lookup"><span data-stu-id="0a724-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="0a724-253">您可以設定讓帳單規則自動計算已完成工作的百分比，也可以手動計算已完成工作的百分比以及要向客戶開發票請款的金額。</span><span class="sxs-lookup"><span data-stu-id="0a724-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="0a724-254">**里程碑** – 達到里程碑時，向客戶開立請領專案里程碑全部金額的發票。</span><span class="sxs-lookup"><span data-stu-id="0a724-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="0a724-255">**服務費** – 向客戶開立請領您的服務加上管理費的發票，這通常是服務成本的某個百分比金額。</span><span class="sxs-lookup"><span data-stu-id="0a724-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="0a724-256">**時間與材料** – 向客戶開立請領專案上所使用時間與材料價值的發票。</span><span class="sxs-lookup"><span data-stu-id="0a724-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="0a724-257">對於所有類型的帳單規則，您可以指定在專案達到一致同意的階段之前，從客戶發票扣減的保留百分比。</span><span class="sxs-lookup"><span data-stu-id="0a724-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="0a724-258">在專案合約中指定付款保留百分比。</span><span class="sxs-lookup"><span data-stu-id="0a724-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="0a724-259">此金額是根據客戶發票中的明細總值所計算，並從該總值中減去。</span><span class="sxs-lookup"><span data-stu-id="0a724-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="0a724-260">對於 **時間與材料** 及 **進度** 帳單規則，您可以指派應收費的類別。</span><span class="sxs-lookup"><span data-stu-id="0a724-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="0a724-261">應收費類別指示應包含在客戶發票中的交易。</span><span class="sxs-lookup"><span data-stu-id="0a724-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="0a724-262">當您準備好開發票向客戶請款時，專案的發票金額是根據帳單規則來計算，並且會產生專案發票提案。</span><span class="sxs-lookup"><span data-stu-id="0a724-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="0a724-263">下列各節提供範例，說明如何設定和管理專案的帳單規則。</span><span class="sxs-lookup"><span data-stu-id="0a724-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="0a724-264">範例：建立根據交貨單位數量的帳單規則</span><span class="sxs-lookup"><span data-stu-id="0a724-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="0a724-265">您的組織簽訂一份合約，以每堂訓練課程 10,000 的成本來為客戶的員工提供總計五堂訓練課程。</span><span class="sxs-lookup"><span data-stu-id="0a724-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="0a724-266">您在每次訓練課程後，開立發票向該客戶請款。</span><span class="sxs-lookup"><span data-stu-id="0a724-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="0a724-267">當您設定合約的帳單規則時，請使用下列值：</span><span class="sxs-lookup"><span data-stu-id="0a724-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="0a724-268">交貨單位是一堂訓練課程。</span><span class="sxs-lookup"><span data-stu-id="0a724-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="0a724-269">每堂訓練課程的單價為 10,000。</span><span class="sxs-lookup"><span data-stu-id="0a724-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="0a724-270">總單位數是五堂訓練課程。</span><span class="sxs-lookup"><span data-stu-id="0a724-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="0a724-271">當您完成一堂訓練課程時，就可以為第一個交貨單位建立金額 10,000 的發票，然後將發票傳送給客戶。</span><span class="sxs-lookup"><span data-stu-id="0a724-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="0a724-272">範例：建立根據指定專案完成百分比的帳單規則 (手動計算)</span><span class="sxs-lookup"><span data-stu-id="0a724-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="0a724-273">您的組織 (軟體諮詢公司) 與客戶簽訂合約，要開發客戶正在開發中的一部分產品。</span><span class="sxs-lookup"><span data-stu-id="0a724-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="0a724-274">您的組織同意在六個月的期間內交付軟體程式碼。</span><span class="sxs-lookup"><span data-stu-id="0a724-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="0a724-275">客戶同意向您的組織支付總計 100,000 的工作費用。</span><span class="sxs-lookup"><span data-stu-id="0a724-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="0a724-276">您依照合約的規定，建立要根據專案完成的工作百分比向客戶開票請款的帳單規則。</span><span class="sxs-lookup"><span data-stu-id="0a724-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="0a724-277">第一個月結束時，您與客戶會面來確定已完成工作的百分比。</span><span class="sxs-lookup"><span data-stu-id="0a724-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="0a724-278">您與客戶一起審查專案之後，您判定專案已完成 15%。</span><span class="sxs-lookup"><span data-stu-id="0a724-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="0a724-279">您可以建立金額為 15,000 (100,000 的 15%) 的發票，並將其傳送給客戶。</span><span class="sxs-lookup"><span data-stu-id="0a724-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="0a724-280">範例：建立根據指定專案完成百分比的帳單規則 (自動計算)</span><span class="sxs-lookup"><span data-stu-id="0a724-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="0a724-281">您的組織 (軟體開發公司) 同意以 30,000 的費用為客戶開發薪資會計套件。</span><span class="sxs-lookup"><span data-stu-id="0a724-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="0a724-282">客戶同意按照工作完成的百分比向您的組織支付費用。</span><span class="sxs-lookup"><span data-stu-id="0a724-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="0a724-283">您估計專案成本為 20,000。</span><span class="sxs-lookup"><span data-stu-id="0a724-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="0a724-284">專案合約會指定您在帳務程序中使用的工作類別。</span><span class="sxs-lookup"><span data-stu-id="0a724-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="0a724-285">您設定的帳單規則會自動為每個類別所完成的工作百分比計算發票金額。</span><span class="sxs-lookup"><span data-stu-id="0a724-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="0a724-286">您為每個類別設定預算：</span><span class="sxs-lookup"><span data-stu-id="0a724-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="0a724-287">**開發** – 15,000 的成本和 20,000 的營收</span><span class="sxs-lookup"><span data-stu-id="0a724-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="0a724-288">**安裝** – 5,000 的成本和 10,000 的營收</span><span class="sxs-lookup"><span data-stu-id="0a724-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="0a724-289">第一次建立客戶發票時，發票金額根據下列資訊自動進行計算：</span><span class="sxs-lookup"><span data-stu-id="0a724-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="0a724-290">一個月之後，專案的工作者會提交專案的時程表。</span><span class="sxs-lookup"><span data-stu-id="0a724-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="0a724-291">工作者的工時成本，在開發時為 5,000，而在安裝時為 1,000。</span><span class="sxs-lookup"><span data-stu-id="0a724-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="0a724-292">開發工作已完成 33% (5,000 實際成本/15,000 預算成本)，而安裝工作已完成 20% (1,000 實際成本/5,000 預算成本)。</span><span class="sxs-lookup"><span data-stu-id="0a724-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="0a724-293">自動計算 8,667 的發票金額 (20,000 的 33% + 10,000 的 20%)。</span><span class="sxs-lookup"><span data-stu-id="0a724-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="0a724-294">您可以建立金額為 8,667 的發票，並將其傳送給客戶。</span><span class="sxs-lookup"><span data-stu-id="0a724-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="0a724-295">範例：建立根據商定里程碑的帳單規則</span><span class="sxs-lookup"><span data-stu-id="0a724-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="0a724-296">您的組織 (管理諮詢公司) 同意為客戶計劃銷售的消費型產品進行市場研究。</span><span class="sxs-lookup"><span data-stu-id="0a724-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="0a724-297">客戶同意從 3 月起使用您的服務，為期三個月，並同意向您的組織支付 50,000 的費用。</span><span class="sxs-lookup"><span data-stu-id="0a724-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="0a724-298">專案有三個里程碑：</span><span class="sxs-lookup"><span data-stu-id="0a724-298">The project has three milestones:</span></span>

-   <span data-ttu-id="0a724-299">里程碑 1：收集消費者資料 – 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0a724-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="0a724-300">里程碑 2：分析消費者資料 – 4 月 30 日</span><span class="sxs-lookup"><span data-stu-id="0a724-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="0a724-301">里程碑 3：提供產品可行性提案 – 5 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0a724-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="0a724-302">客戶同意向您的組織支付第一個里程碑 10,000、第二個里程碑 20,000，以及第三個里程碑 20,000 的費用。</span><span class="sxs-lookup"><span data-stu-id="0a724-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="0a724-303">設定專案合約時，您同意根據完成的里程碑來向客戶開單請款。</span><span class="sxs-lookup"><span data-stu-id="0a724-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="0a724-304">帳單規則設定包括下列步驟：</span><span class="sxs-lookup"><span data-stu-id="0a724-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="0a724-305">定義專案里程碑。</span><span class="sxs-lookup"><span data-stu-id="0a724-305">Define the project milestones.</span></span>
-   <span data-ttu-id="0a724-306">定義每個里程碑完成時，向客戶開發票請款的金額。</span><span class="sxs-lookup"><span data-stu-id="0a724-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="0a724-307">於 3 月 31 日完成第一個里程碑時，您將里程碑標示為已完成，然後建立金額為 10,000 的發票，並將其傳送給客戶。</span><span class="sxs-lookup"><span data-stu-id="0a724-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="0a724-308">您必須先將里程碑標示為已完成，才能建立里程碑的發票。</span><span class="sxs-lookup"><span data-stu-id="0a724-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="0a724-309">範例：建立根據服務加上管理費的帳單規則</span><span class="sxs-lookup"><span data-stu-id="0a724-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="0a724-310">您的組織 (管理諮詢公司) 同意進行市場研究，以評估客戶 (零售業公司) 所開發產品的可行性。</span><span class="sxs-lookup"><span data-stu-id="0a724-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="0a724-311">合約的條款規定您提供最熱門的三個管理顧問的服務，這些顧問會根據時間與材料進行研究。</span><span class="sxs-lookup"><span data-stu-id="0a724-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="0a724-312">客戶同意支付每小時 100 的費用，加上針對諮詢時間向專案收取的 10% 管理費。</span><span class="sxs-lookup"><span data-stu-id="0a724-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="0a724-313">設定專案合約時，您建立帳單規則，以將 10% 的管理費加到向專案收取的諮詢時間。</span><span class="sxs-lookup"><span data-stu-id="0a724-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="0a724-314">建立客戶的發票時，您會向客戶開單請領 10% 的管理費用加上諮詢時間的成本。</span><span class="sxs-lookup"><span data-stu-id="0a724-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="0a724-315">例如，如果三個顧問在專案上工作了總計 200 小時，則會根據下列計算建立金額為 22,000 的發票：</span><span class="sxs-lookup"><span data-stu-id="0a724-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="0a724-316">200 小時 (每小時 100) = 20,000</span><span class="sxs-lookup"><span data-stu-id="0a724-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="0a724-317">10% 管理費 = 2,000</span><span class="sxs-lookup"><span data-stu-id="0a724-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="0a724-318">總發票金額 = 22,000</span><span class="sxs-lookup"><span data-stu-id="0a724-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="0a724-319">如果費用應向客戶課稅，且您在專案合約中選取銷售課稅群組時，費用的帳單規則中會自動輸入銷售課稅群組。</span><span class="sxs-lookup"><span data-stu-id="0a724-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="0a724-320">範例：建立時間與材料值的帳單規則</span><span class="sxs-lookup"><span data-stu-id="0a724-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="0a724-321">您的組織 (軟體諮詢公司) 同意在未來六個月為客戶提供五個技術顧問來處理軟體開發專案。</span><span class="sxs-lookup"><span data-stu-id="0a724-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="0a724-322">客戶同意每個諮詢小時支付 150，加上辦公用品成本的費用。</span><span class="sxs-lookup"><span data-stu-id="0a724-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="0a724-323">您的組織會在每個月底傳送發票給客戶。</span><span class="sxs-lookup"><span data-stu-id="0a724-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="0a724-324">設定專案合約時，您同意針專案的時間與材料向客戶開單請領每個月的費用。</span><span class="sxs-lookup"><span data-stu-id="0a724-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="0a724-325">您建立包含下列資訊的帳單規則：</span><span class="sxs-lookup"><span data-stu-id="0a724-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="0a724-326">合約期間為六個月。</span><span class="sxs-lookup"><span data-stu-id="0a724-326">The contract period is six months.</span></span>
-   <span data-ttu-id="0a724-327">諮詢時間是以每小時 150 的費率進行計算。</span><span class="sxs-lookup"><span data-stu-id="0a724-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="0a724-328">辦公用品是以成本來開發票，而且專案的總成本不得超過 10,000。</span><span class="sxs-lookup"><span data-stu-id="0a724-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="0a724-329">在專案執行期間，您可以在每個行事曆月底建立客戶發票。</span><span class="sxs-lookup"><span data-stu-id="0a724-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="0a724-330">在第一個月期間，專案顧問在專案上記錄總計 800 小時。</span><span class="sxs-lookup"><span data-stu-id="0a724-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="0a724-331">已向專案收費的辦公用品成本為 2000。</span><span class="sxs-lookup"><span data-stu-id="0a724-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="0a724-332">因此，您在月底建立金額為 122,000 的發票，其計算為 800 小時 (每小時 150)，加上辦公用品 2,000。</span><span class="sxs-lookup"><span data-stu-id="0a724-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]