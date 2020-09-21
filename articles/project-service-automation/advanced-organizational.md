---
title: 組織單位
description: 本主題提供有關 Dynamics 365 Project Service Automation 中組織單位的資訊。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 47855fdd-befa-4203-856d-4e917ecfc16d
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7282b83516e9234b5717b0b5d82d6650bc70f9d2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750009"
---
# <a name="organizational-units"></a><span data-ttu-id="50f6e-103">組織單位</span><span class="sxs-lookup"><span data-stu-id="50f6e-103">Organizational units</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="50f6e-104">在 Dynamics 365 Project Service Automation 中，組織單位是專業服務公司的不同群組或部門，雇用有成本費率的計費資源。</span><span class="sxs-lookup"><span data-stu-id="50f6e-104">Dynamics 365 Project Service Automation, an organizational unit is a distinct group or division in a professional services company that employs billable resources that have cost rates.</span></span>

<span data-ttu-id="50f6e-105">對雇用各種業務範圍或行業別中技術資源的專業服務公司來說，在不同業務範圍或行業別中填補職能角色所需付出的成本可能會各不相同。</span><span class="sxs-lookup"><span data-stu-id="50f6e-105">For professional services companies that employ technical resources in various practice areas or business lines, the cost to fill a role in one practice area or business line might differ from the cost to fill a role in another practice area or business line.</span></span> <span data-ttu-id="50f6e-106">組織單位這個概念在此案例中有其用處，提供了一種可在公司賦予這些角色不同成本結構的部門中將一組計費角色設為群組的方法</span><span class="sxs-lookup"><span data-stu-id="50f6e-106">The concept  organizational units helps in this scenario by providing a way to group a set of billable roles in a division of a company that has a distinct cost structure for these roles.</span></span>

## <a name="key-attributes-and-associations-of-organizational-units"></a><span data-ttu-id="50f6e-107">組織單位的主要屬性與關聯</span><span class="sxs-lookup"><span data-stu-id="50f6e-107">Key attributes and associations of organizational units</span></span>

<span data-ttu-id="50f6e-108">在 PSA 中，PSA 的組織單位有特定貨幣和特定成本價目表。</span><span class="sxs-lookup"><span data-stu-id="50f6e-108">In PSA, an organizational unit in PSA has a specific currency and specific cost price lists.</span></span>

<span data-ttu-id="50f6e-109">組織單位的貨幣是用來追蹤成本的主要貨幣。</span><span class="sxs-lookup"><span data-stu-id="50f6e-109">The currency of an organizational unit is the primary currency that is used to track costs.</span></span>

<span data-ttu-id="50f6e-110">可以將一個或多個成本價目表附加至每個組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-110">One or more cost price lists can be attached to each organizational unit.</span></span> <span data-ttu-id="50f6e-111">PSA 對於可附加至組織單位的價目表施加下列限制：</span><span class="sxs-lookup"><span data-stu-id="50f6e-111">PSA puts the following limitations on the price lists that can be attached to an organizational unit:</span></span>

- <span data-ttu-id="50f6e-112">價目表必須以組織單位的貨幣計價</span><span class="sxs-lookup"><span data-stu-id="50f6e-112">Price lists must be in the currency of the organizational unit</span></span>
- <span data-ttu-id="50f6e-113">價目表必須是成本價目表</span><span class="sxs-lookup"><span data-stu-id="50f6e-113">Price lists must be of cost price lists</span></span>

<span data-ttu-id="50f6e-114">此外，資源實體上還有組織單位專用的屬性。</span><span class="sxs-lookup"><span data-stu-id="50f6e-114">In addition, there is an attribute for the organizational unit on the Resource entity.</span></span> <span data-ttu-id="50f6e-115">每個資源只能指派至一個組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-115">Each resource can be assigned to one organizational unit.</span></span>

## <a name="roles-of-organizational-units"></a><span data-ttu-id="50f6e-116">組織單位中的角色</span><span class="sxs-lookup"><span data-stu-id="50f6e-116">Roles of organizational units</span></span>

<span data-ttu-id="50f6e-117">組織單位在 PSA 中扮演兩種角色：</span><span class="sxs-lookup"><span data-stu-id="50f6e-117">The organizational unit plays two roles in PSA:</span></span>

- <span data-ttu-id="50f6e-118">**承包單位** – 代表公司中主要負責贏得銷售和管理客戶工作與服務交付之群組或部門的組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-118">**Contracting unit** – The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> <span data-ttu-id="50f6e-119">承包單位是依據**商機**、**報價**、**專案合約**及**專案**頁面標頭區段中的**承包單位**欄位來識別。</span><span class="sxs-lookup"><span data-stu-id="50f6e-119">The contracting unit is identified by the **Contracting Unit** field in the header section of the **Opportunity**, **Quote**, **Project Contract**, and **Project** pages.</span></span>
- <span data-ttu-id="50f6e-120">**資源分配單位** – 資源所隸屬於或指派至的組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-120">**Resourcing unit** – The organizational unit that a resource belongs to or is assigned to.</span></span> <span data-ttu-id="50f6e-121">此組織單位可以為工作說明書 (SOW) 上的一些角色以及承包單位負責的專案提供其資源。</span><span class="sxs-lookup"><span data-stu-id="50f6e-121">This organizational unit can provide its resources for some roles on statements of work (SOWs) and projects that are owned by the contracting unit.</span></span>

> ![承包單位和資源分配單位](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a><span data-ttu-id="50f6e-123">組織單位常見問題集</span><span class="sxs-lookup"><span data-stu-id="50f6e-123">Organizational unit FAQs</span></span>

<span data-ttu-id="50f6e-124">以下是一些有關組織單位的最常見問題。</span><span class="sxs-lookup"><span data-stu-id="50f6e-124">Here are some of the most frequently asked questions about organizational units.</span></span>

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a><span data-ttu-id="50f6e-125">PSA 中的組織單位實體與 Dynamics 365 中既存的組織實體有什麼關聯？</span><span class="sxs-lookup"><span data-stu-id="50f6e-125">How is the Organizational Unit entity in PSA related to the Organization entity that already exists in Dynamics 365?</span></span>

<span data-ttu-id="50f6e-126">Microsoft Dynamics 365 中的組織實體代表全域 Dynamics 365 執行個體的名稱。</span><span class="sxs-lookup"><span data-stu-id="50f6e-126">The Organization entity in Microsoft Dynamics 365 represents the name of a global Dynamics 365 instance.</span></span> <span data-ttu-id="50f6e-127">此名稱通常是全域企業的名稱。</span><span class="sxs-lookup"><span data-stu-id="50f6e-127">This name is usually the name of the global enterprise.</span></span>

<span data-ttu-id="50f6e-128">組織單位實體代表全域企業中的群組或部門。</span><span class="sxs-lookup"><span data-stu-id="50f6e-128">The Organizational Unit entity represents a group or division in the global enterprise.</span></span> <span data-ttu-id="50f6e-129">此群組或部門有一組角色以及這些角色專用的成本價目表，而這些角色及價目表與企業中其他群組或部門的角色及價目表不同。</span><span class="sxs-lookup"><span data-stu-id="50f6e-129">This group or division has a set of roles and a cost price list for those roles, and those roles and price list differ from the roles and price list of other groups or divisions in the enterprise.</span></span>

<span data-ttu-id="50f6e-130">安裝 PSA 時，會根據組織建立預設組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-130">When PSA is installed, a default organizational unit is created based on the organization.</span></span> <span data-ttu-id="50f6e-131">所有現有資源都會指派至預設組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-131">All existing resources are assigned to the default organizational unit.</span></span> <span data-ttu-id="50f6e-132">如果將任何新的 Active Directory 使用者或資源匯入 Dynamics 365，則使用者匯入程序會將其指派給 PSA 中的預設組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-132">If any new Active Directory users or resources are imported into Dynamics 365, the user import process assigns them to the default organizational unit in PSA.</span></span>
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a><span data-ttu-id="50f6e-133">組織單位實體與業務單位實體有何不同？</span><span class="sxs-lookup"><span data-stu-id="50f6e-133">How does the organizational unit entity differ from the business unit entity?</span></span>

<span data-ttu-id="50f6e-134">在 Dynamics 365 中，業務單位實體是一個安全性建構。</span><span class="sxs-lookup"><span data-stu-id="50f6e-134">In Dynamics 365, the Business Unit entity is a security construct.</span></span> <span data-ttu-id="50f6e-135">使用者與業務單位的關聯決定使用者有權存取的實體和實體記錄。</span><span class="sxs-lookup"><span data-stu-id="50f6e-135">The association of a user with a business unit determines the entities and entity records that the user has access to.</span></span> <span data-ttu-id="50f6e-136">此關聯也決定了使用者對這些實體記錄所擁有的權限 (建立、讀取、寫入、刪除、附加、附加至、指派或共用)。</span><span class="sxs-lookup"><span data-stu-id="50f6e-136">It also determines the permissions (Create, Read, Write, Delete, Append, Append To, Assign, or Share) that the user has for those entity records.</span></span>

<span data-ttu-id="50f6e-137">組織單位實體代表將不同成本費率賦予指派至此實體之員工的公司群組或部門。</span><span class="sxs-lookup"><span data-stu-id="50f6e-137">The Organizational Unit entity represents a company group or division that has distinct cost rates for employees that are assigned to it.</span></span> <span data-ttu-id="50f6e-138">資源與組織單位的關聯決定資源的專案業務開發成本。</span><span class="sxs-lookup"><span data-stu-id="50f6e-138">The association of a resource with an organizational unit determines the resource's cost to a project engagement.</span></span>

<span data-ttu-id="50f6e-139">實作 Dynamics 365 時，請最佳化業務單位階層的安全性授權以及對業務單位的使用者指派。</span><span class="sxs-lookup"><span data-stu-id="50f6e-139">When you implement Dynamics 365, optimize security authorization for the hierarchy of business units and the assignment of users to business units.</span></span> <span data-ttu-id="50f6e-140">將所有通常必須存取同一組記錄的使用者指派給相同的業務單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-140">Assign all users who must typically access the same set of records to the same business unit.</span></span> <span data-ttu-id="50f6e-141">組織單位對安全性授權或存取權沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="50f6e-141">The organizational unit has no effect on security authorization or access.</span></span>

#### <a name="example-of-organizational-units-and-business-units"></a><span data-ttu-id="50f6e-142">組織單位和業務單位的範例</span><span class="sxs-lookup"><span data-stu-id="50f6e-142">Example of organizational units and business units</span></span>

<span data-ttu-id="50f6e-143">Contoso, Ltd. 有業績興旺的 Microsoft 技術業務營運。</span><span class="sxs-lookup"><span data-stu-id="50f6e-143">Contoso, Ltd. has a thriving Microsoft technology practice.</span></span> <span data-ttu-id="50f6e-144">允章和美玲都是 C\# 開發人員，但是美玲在美國，而允章在印度。</span><span class="sxs-lookup"><span data-stu-id="50f6e-144">Prakash and Tricia are both C\# developers, but Tricia is in the United States, whereas Prakash is in India.</span></span> <span data-ttu-id="50f6e-145">大部分專案業務開發都需要來自 Contoso India 和 Contoso US 的資源，而允章和美玲對此業務範圍中的專案需要相同的安全性存取層級。</span><span class="sxs-lookup"><span data-stu-id="50f6e-145">Most of the project engagements require resources from Contoso India and Contoso US, and Prakash and Tricia require the same level of security access to projects in this practice area.</span></span> <span data-ttu-id="50f6e-146">不過，Contoso India 的開發人員成本與 Contoso US 的開發人員成本明顯不同。</span><span class="sxs-lookup"><span data-stu-id="50f6e-146">However, the cost of developers from Contoso India differs significantly from the cost of developers from Contoso US.</span></span>

<span data-ttu-id="50f6e-147">以下是使用 Dynamics 365 和 PSA 設計此案例的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="50f6e-147">Here is an optimal way to design for this scenario by using Dynamics 365 and PSA.</span></span>

1. <span data-ttu-id="50f6e-148">建立 Microsoft 技術業務營運做為業務單位，並建立允章及美玲與其之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="50f6e-148">Create the Microsoft technology practice as a business unit, and associate Prakash and Tricia with it.</span></span> <span data-ttu-id="50f6e-149">如此一來，就有助於保證這兩位員工對該業務範圍中的任何專案都有相同的安全性存取層級。</span><span class="sxs-lookup"><span data-stu-id="50f6e-149">In this way, you help guarantee that both employees have the same level of security access to any projects in that practice area.</span></span> <span data-ttu-id="50f6e-150">他們都可以檢查進度並報告時間、費用及工作更新。</span><span class="sxs-lookup"><span data-stu-id="50f6e-150">They both will be able to check progress and report time, expenses, and task updates.</span></span> 
2. <span data-ttu-id="50f6e-151">建立兩個組織單位以保證正確反映專案的成本。</span><span class="sxs-lookup"><span data-stu-id="50f6e-151">Create two organizational units to hel guarantee that the cost to the project is correctly reflected.</span></span> 
3. <span data-ttu-id="50f6e-152">將美玲與 Contoso US 建立關聯，並將允章與 Contoso India 建立關聯。</span><span class="sxs-lookup"><span data-stu-id="50f6e-152">Associate Tricia wtih Contoso US and associate Prakash with Contoso India.</span></span>
4. <span data-ttu-id="50f6e-153">將適當的成本價目表指派給這兩個組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-153">Assign appropriate cost price lists to both organizational units.</span></span> <span data-ttu-id="50f6e-154">如此一來，就有助於保證允章和美玲專案中記錄的成本準確反映 Contoso US 與 Contoso India 之間的成本差異。</span><span class="sxs-lookup"><span data-stu-id="50f6e-154">TIn this way, you help guarantee that the costs that are recorded on the project for Prakash and Tricia accurately reflect the difference in costs between Contoso US and Contoso India.</span></span>

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a><span data-ttu-id="50f6e-155">組織單位與 Dynamics 365 中的銷售領域有關聯嗎？</span><span class="sxs-lookup"><span data-stu-id="50f6e-155">Are organizational units related to sales territories in Dynamics 365?</span></span>

<span data-ttu-id="50f6e-156">銷售領域與組織單位之間不存在關聯或關係。</span><span class="sxs-lookup"><span data-stu-id="50f6e-156">There is no association or relationship between sales territories and organizational units.</span></span> <span data-ttu-id="50f6e-157">銷售領域通常是進行銷售的地理區域。</span><span class="sxs-lookup"><span data-stu-id="50f6e-157">A sales territory is typically a geographical area where sales occur.</span></span> <span data-ttu-id="50f6e-158">銷售價目表可以與每個銷售領域產生關聯。</span><span class="sxs-lookup"><span data-stu-id="50f6e-158">A sales price list can be associated with each sales territory.</span></span>

<span data-ttu-id="50f6e-159">組織單位是公司的內部群組或部門，會追蹤其出售一組角色給其他部目或外部客戶的成本。</span><span class="sxs-lookup"><span data-stu-id="50f6e-159">An organizational unit is an internal group or division in the company that tracks costs for a set of roles that it sells to other divisions or to external customers.</span></span>

#### <a name="example-of-organizational-units-and-sales-territories"></a><span data-ttu-id="50f6e-160">組織單位和銷售領域的範例</span><span class="sxs-lookup"><span data-stu-id="50f6e-160">Example of organizational units and sales territories</span></span>

<span data-ttu-id="50f6e-161">Contoso, Ltd. 有兩個開發中心：Contoso US 和 Contoso India。</span><span class="sxs-lookup"><span data-stu-id="50f6e-161">Contoso, Ltd. has two development centers: Contoso US and Contoso India.</span></span> <span data-ttu-id="50f6e-162">這兩個開發中心之間的資源成本大幅不同。</span><span class="sxs-lookup"><span data-stu-id="50f6e-162">Costs of resources differ greatly between these two development centers.</span></span>

<span data-ttu-id="50f6e-163">Contoso 在許多國際市場上銷售其 IT 服務，例如拉丁美洲、北美洲、亞太地區、西歐和中東。</span><span class="sxs-lookup"><span data-stu-id="50f6e-163">Contoso sells its IT services in many international markets, such as Latin America, North America, Asia-Pacific, Western Europe, and the Middle East.</span></span> <span data-ttu-id="50f6e-164">相同專案角色的帳單費率在這些不同市場上可能會有很大變化。</span><span class="sxs-lookup"><span data-stu-id="50f6e-164">Bill rates for the same project roles can vary widely across these markets.</span></span>

<span data-ttu-id="50f6e-165">您應將 Contoso US 和 Contoso India 設定為組織單位，而且每個組織單位都必須有其本身的成本價目表。</span><span class="sxs-lookup"><span data-stu-id="50f6e-165">Contoso US and Contoso India should be set up as organizational units, and each organizational unit should have its own cost price list.</span></span> <span data-ttu-id="50f6e-166">亞太地區、拉丁美洲、北美洲、西歐和中東地區應設定為銷售領域，而且每個銷售領域都必須有其本身的銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="50f6e-166">Asia-Pacific, Latin America, North America, Western Europe, and the Middle East should be set up as sales territories, and each sales territory should have its own sales price list.</span></span>

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a><span data-ttu-id="50f6e-167">為什麼價目表與組織單位的關聯會有限制？</span><span class="sxs-lookup"><span data-stu-id="50f6e-167">Why is there a restriction on the association of price lists with organizational units?</span></span> 

<span data-ttu-id="50f6e-168">銷售定價通常是售出服務的目標地理區域或市場所獨有。</span><span class="sxs-lookup"><span data-stu-id="50f6e-168">Sales pricing is usually unique to the geographical areas or markets where services are sold.</span></span> <span data-ttu-id="50f6e-169">公司的內部部門對相同類型的服務，通常不會有其本身的銷售定價。</span><span class="sxs-lookup"><span data-stu-id="50f6e-169">Internal divisions of a company don't usually have their own sales pricing for the same type of services.</span></span> <span data-ttu-id="50f6e-170">不過，內部部門會有不同的銷貨成本 (COGS)，取決於他們所雇用人員的技能以及其營業所在地區的勞動條件。</span><span class="sxs-lookup"><span data-stu-id="50f6e-170">However, internal divisions have a different cost of goods sold (COGS), depending on the skills of the people that they employ and the labor conditions of the region where they operate.</span></span> <span data-ttu-id="50f6e-171">由於組織單位以公司內部部門為模型，因此只能有成本價目表。</span><span class="sxs-lookup"><span data-stu-id="50f6e-171">Because organizational units are modeled as internal divisions of a company, they can have only cost price lists.</span></span>

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a><span data-ttu-id="50f6e-172">為什麼無法將銷售價目表與組織單位建立關聯？</span><span class="sxs-lookup"><span data-stu-id="50f6e-172">Why can’t we associate sales price lists to organizational units?</span></span>

<span data-ttu-id="50f6e-173">在 PSA 中，銷售價目表可以與客戶及銷售領域產生關聯。</span><span class="sxs-lookup"><span data-stu-id="50f6e-173">In PSA, sales price lists can be associated with customers and sales territories.</span></span> <span data-ttu-id="50f6e-174">商機、報價、專案合約和專案等交易實體會使用附加至客戶帳戶或銷售領域的銷售價目表，來判斷專案業務開發的帳單費率和可能營收。</span><span class="sxs-lookup"><span data-stu-id="50f6e-174">Transactional entities like Opportunity, Quote, Project Contract, and Project use sales price lists that are attached to the customer account or the sales territory to determine bill rates and potential revenue on the project engagement.</span></span>

<span data-ttu-id="50f6e-175">成本價目表與組織單位產生關聯。</span><span class="sxs-lookup"><span data-stu-id="50f6e-175">Cost price lists are associated with organizational units.</span></span> <span data-ttu-id="50f6e-176">商機、報價、專案合約和專案等交易實體會使用會使用附加至承包單位的成本價目表，來判斷專案業務開發的成本。</span><span class="sxs-lookup"><span data-stu-id="50f6e-176">Transactional entities like Opportunity, Quote, Project Contract, and Project use cost price lists that are attached to the contracting unit to determine costs to a project engagement.</span></span>

### <a name="are-organizational-units-hierarchical-in-psa"></a><span data-ttu-id="50f6e-177">PSA 中的組織單位是階層式嗎？</span><span class="sxs-lookup"><span data-stu-id="50f6e-177">Are organizational units hierarchical in PSA?</span></span>

<span data-ttu-id="50f6e-178">編號</span><span class="sxs-lookup"><span data-stu-id="50f6e-178">No.</span></span> <span data-ttu-id="50f6e-179">在目前的 PSA 版本中，組織單位不是階層式。</span><span class="sxs-lookup"><span data-stu-id="50f6e-179">In the current release of PSA, organizational units are not hierarchical.</span></span> <span data-ttu-id="50f6e-180">這表示您無法執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="50f6e-180">This means that you can’t:</span></span>

- <span data-ttu-id="50f6e-181">設定用於預設成本價、向上周遊階層的模式。</span><span class="sxs-lookup"><span data-stu-id="50f6e-181">Configure a pattern for defaulting cost prices that traverses up a hierarchy.</span></span> 
- <span data-ttu-id="50f6e-182">報告組織單位階層在不同層級上彙總的營收或成本。</span><span class="sxs-lookup"><span data-stu-id="50f6e-182">Report revenue or cost rolled up at different levels of the organizational unit hierarchy.</span></span>

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a><span data-ttu-id="50f6e-183">我們是一家大型跨國公司，有複雜的多級階層成本中心、部門和帳務辦公室。</span><span class="sxs-lookup"><span data-stu-id="50f6e-183">We're a big multinational firm with a complex, multilevel hierarchy of cost centers, divisions, and billing offices.</span></span> <span data-ttu-id="50f6e-184">如何充分利用此版本 Project Service 應用程式中的組織單位概念？</span><span class="sxs-lookup"><span data-stu-id="50f6e-184">How can we make the best use of the organizational unit concept in this version of the Project Service app?</span></span>

<span data-ttu-id="50f6e-185">當您有階層複雜的成本中心、部門、帳務辦公室及其他時，請將該階層的分葉節點設定為不同的組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-185">When you have a complex hierarchy of cost centers, divisions, billing offices, etc., set up the leaf nodes of that hierarchy as distinct organizational units.</span></span>
<span data-ttu-id="50f6e-186">下列範例顯示一般的階層：</span><span class="sxs-lookup"><span data-stu-id="50f6e-186">The following example shows a typical hierarchy:</span></span>

<span data-ttu-id="50f6e-187">**Contoso India**</span><span class="sxs-lookup"><span data-stu-id="50f6e-187">**Contoso India**</span></span>

  - <span data-ttu-id="50f6e-188">SAP 業務營運</span><span class="sxs-lookup"><span data-stu-id="50f6e-188">SAP Practice</span></span> 

    - <span data-ttu-id="50f6e-189">技術顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-189">Technical Consultants</span></span> 
    - <span data-ttu-id="50f6e-190">職能顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-190">Functional Consultants</span></span> 
    
  - <span data-ttu-id="50f6e-191">Microsoft 技術業務營運</span><span class="sxs-lookup"><span data-stu-id="50f6e-191">Microsoft Technology Practice</span></span> 

    - <span data-ttu-id="50f6e-192">技術顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-192">Technical Consultants</span></span>
    - <span data-ttu-id="50f6e-193">職能顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-193">Functional Consultants</span></span> 
    
<span data-ttu-id="50f6e-194">**Contoso US**</span><span class="sxs-lookup"><span data-stu-id="50f6e-194">**Contoso US**</span></span>

 - <span data-ttu-id="50f6e-195">SAP 業務營運</span><span class="sxs-lookup"><span data-stu-id="50f6e-195">SAP Practice</span></span> 

    - <span data-ttu-id="50f6e-196">技術顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-196">Technical Consultants</span></span> 
    - <span data-ttu-id="50f6e-197">職能顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-197">Functional Consultants</span></span> 
    
 - <span data-ttu-id="50f6e-198">Microsoft 技術業務營運</span><span class="sxs-lookup"><span data-stu-id="50f6e-198">Microsoft Technology Practice</span></span> 

    - <span data-ttu-id="50f6e-199">技術顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-199">Technical Consultants</span></span> 
    - <span data-ttu-id="50f6e-200">職能顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-200">Functional Consultants</span></span> 
 
<span data-ttu-id="50f6e-201">如果您的階層也類似，您必須將其設定為一般清單，如下所示：</span><span class="sxs-lookup"><span data-stu-id="50f6e-201">If your hierarchy is similar, you must set it up as a flat list, as shown here:</span></span>
- <span data-ttu-id="50f6e-202">Contoso India - SAP 業務營運 - 技術顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-202">Contoso India - SAP Practice - Technical Consultants</span></span> 
- <span data-ttu-id="50f6e-203">Contoso India - SAP 業務營運 - 職能顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-203">Contoso India - SAP Practice - Functional Consultants</span></span>       
- <span data-ttu-id="50f6e-204">Contoso India - Microsoft 技術業務營運 - 職能顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-204">Contoso India - Microsoft Technology Practice Functional Consultants</span></span> 
- <span data-ttu-id="50f6e-205">Contoso India - Microsoft 技術業務營運 - 職能顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-205">Contoso India - Microsoft Technology Practice Functional Consultants</span></span> 
- <span data-ttu-id="50f6e-206">Contoso US - SAP 業務營運 - 技術顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-206">Contoso US - SAP Practice - Technical Consultants</span></span>  
- <span data-ttu-id="50f6e-207">Contoso US - SAP 業務營運 - 職能顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-207">Contoso US - SAP Practice - Functional Consultants</span></span>  
- <span data-ttu-id="50f6e-208">Contoso US - Microsoft 技術業務營運 - 技術顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-208">Contoso US - Microsoft Technology Practice - Technical Consultants</span></span> 
- <span data-ttu-id="50f6e-209">Contoso US - Microsoft 技術業務營運 - 職能顧問</span><span class="sxs-lookup"><span data-stu-id="50f6e-209">Contoso US - Microsoft Technology Practice - Functional Consultants</span></span>

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a><span data-ttu-id="50f6e-210">我們是一家只以一個部門來營運的小型專業服務公司。</span><span class="sxs-lookup"><span data-stu-id="50f6e-210">We're a small professional services company that operates as only one division.</span></span> <span data-ttu-id="50f6e-211">如何妥善運用最新 PSA 版本中的組織單位概念？</span><span class="sxs-lookup"><span data-stu-id="50f6e-211">How can we best use the organizational unit concept in the current version of PSA?</span></span>

<span data-ttu-id="50f6e-212">如果您公司只以一個有一份成本價目表的單位來營運，則不需要設定任何組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-212">If your company operates as one unit that has one cost price list, you don't have to set up any organizational units.</span></span> <span data-ttu-id="50f6e-213">進行 PSA 安裝時，Dynamics 365 會建立一個與組織同名的預設組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-213">During PSA installation, Dynamics 365 creates one default organizational unit that has the same name as the organization.</span></span> <span data-ttu-id="50f6e-214">所有使用者預設都會指派至此組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-214">By default, all users are assigned to this organizational unit.</span></span> <span data-ttu-id="50f6e-215">每當系統要求選取組織單位時，預設都會選取此組織單位。</span><span class="sxs-lookup"><span data-stu-id="50f6e-215">Whenever the system requires that an organizational unit be selected, this organizational unit is selected by default.</span></span>

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a><span data-ttu-id="50f6e-216">從報價或專案合約服務內容建立專案時，預設承包單位來自報價或專案合約。</span><span class="sxs-lookup"><span data-stu-id="50f6e-216">When a project is created from a quote or project contract line, the default contracting unit comes from the quote or project contract.</span></span> <span data-ttu-id="50f6e-217">如果在銷售實體 (例如報價或專案合約) 之前建立專案，預設承包單位是什麼？</span><span class="sxs-lookup"><span data-stu-id="50f6e-217">If a project is created before sales entities such as quote or project contract, what is the default contracting unit?</span></span>

<span data-ttu-id="50f6e-218">自行建立專案時，專案的預設承包單位是以建立該專案的使用者為準。</span><span class="sxs-lookup"><span data-stu-id="50f6e-218">When a project is created on its own, the default contracting unit of the project is based on the user who creates it.</span></span> <span data-ttu-id="50f6e-219">該使用者也是預設專案經理。</span><span class="sxs-lookup"><span data-stu-id="50f6e-219">That user is also the default project manager.</span></span> <span data-ttu-id="50f6e-220">如果專案已對應至銷售實體 (例如報價或專案合約)，則專案的承包單位改以銷售實體為準。</span><span class="sxs-lookup"><span data-stu-id="50f6e-220">If the project is mapped to a sales entity such as a quote or project contract, the contracting unit on the project is based on the sales entity instead.</span></span> <span data-ttu-id="50f6e-221">在此案例中，可能會重新計算專案估計值，因為如果承包單位已變更，則會使用成本價目表來計算成本估計變更。</span><span class="sxs-lookup"><span data-stu-id="50f6e-221">In this case, project estimates might be recalculated, because the cost price list is used to calculate the cost estimate changes if the contracting unit is changed.</span></span> <span data-ttu-id="50f6e-222">銷售價目表會用來計算為了與報價相關專案價目表同步而變更的銷售估計。</span><span class="sxs-lookup"><span data-stu-id="50f6e-222">The sales price list is used to calculate the sales estimates that will be changed so that they are in sync with the project price list on the quote.</span></span>

<span data-ttu-id="50f6e-223">專案的**承包單位**和**貨幣**欄位已鎖定，無法編輯，因為這些欄位必須與專案所對應至銷售實體 (報價或專案合約) 的值同步。</span><span class="sxs-lookup"><span data-stu-id="50f6e-223">The **Contracting Unit** and **Currency** fields on the project are locked for editing, because they must be in sync with the values on the sales entity (quote or project contract) that the project is mapped to.</span></span>
