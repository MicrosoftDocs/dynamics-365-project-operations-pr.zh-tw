---
title: 定價和成本維度首頁
description: 本主題提供定價維度的概觀。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 65516784c6787fa5f3c08297f4d161d52c2ea4a9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151288"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="4503c-103">定價和成本維度首頁</span><span class="sxs-lookup"><span data-stu-id="4503c-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4503c-104">在專案型組織中用來設定人力定價和成本估算的維度，受到下列屬性影響：</span><span class="sxs-lookup"><span data-stu-id="4503c-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="4503c-105">從事與其經驗、角色或地理區域類似之工作的人員</span><span class="sxs-lookup"><span data-stu-id="4503c-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="4503c-106">要以類似其複雜度或每天時間來執行的工作</span><span class="sxs-lookup"><span data-stu-id="4503c-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="4503c-107">考慮到工作的這些屬性的獨特性質以及執行工作所需的人員，Project Service Automation 有兩種類型的定價維度值可供使用：</span><span class="sxs-lookup"><span data-stu-id="4503c-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="4503c-108">**選項組** - 本身是一組固定列舉值的屬性。</span><span class="sxs-lookup"><span data-stu-id="4503c-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="4503c-109">**以實體為準的值** - 本身可以包含有限但可能隨時間變更之各不相同值集的屬性。</span><span class="sxs-lookup"><span data-stu-id="4503c-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="4503c-110">定價維度</span><span class="sxs-lookup"><span data-stu-id="4503c-110">Pricing dimensions</span></span>

<span data-ttu-id="4503c-111">PSA 隨附一組預設定價維度。</span><span class="sxs-lookup"><span data-stu-id="4503c-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="4503c-112">您可以移至 **Project Service** > **參數** 來檢視這些維度。</span><span class="sxs-lookup"><span data-stu-id="4503c-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="4503c-113">在參數記錄的 **以金額為準的定價維度** 索引標籤上，確認角色 **msdyn_resourcecategory** 和資源分配單位 **msdyn_organizationalunit** 的 **適用於銷售** 及 **適用於成本** 欄位已設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="4503c-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="4503c-114">這可讓您設定每個角色與組織單位組合的價格和成本。</span><span class="sxs-lookup"><span data-stu-id="4503c-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![反白顯示「適用於銷售」的 Project Service 參數螢幕擷取畫面](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="4503c-116">如果您在 PSA 版本 3 之前一直都使用角色和組織單位的預設欄位做為定價維度，就不會有任何看得出的變更。</span><span class="sxs-lookup"><span data-stu-id="4503c-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="4503c-117">您可以繼續照常使用 Project Service。</span><span class="sxs-lookup"><span data-stu-id="4503c-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="4503c-118">如果您需要使用其他屬性來為資源定訂價格或估算成本，則可以建立自訂欄位、實體和維度。</span><span class="sxs-lookup"><span data-stu-id="4503c-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="4503c-119">如需詳細資訊，請參閱下列主題，但請注意，您必須依照下列順序完成程序：</span><span class="sxs-lookup"><span data-stu-id="4503c-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="4503c-120">建立自訂欄位和實體</span><span class="sxs-lookup"><span data-stu-id="4503c-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="4503c-121">將自訂欄位新增至價格設定與交易實體</span><span class="sxs-lookup"><span data-stu-id="4503c-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="4503c-122">將自訂欄位設定為定價維度</span><span class="sxs-lookup"><span data-stu-id="4503c-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="4503c-123">更新外掛程式屬性以包含新的定價維度</span><span class="sxs-lookup"><span data-stu-id="4503c-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="4503c-124">定訂人力資源時間價格</span><span class="sxs-lookup"><span data-stu-id="4503c-124">Pricing human resource time</span></span>
<span data-ttu-id="4503c-125">組織對人力資源時間的定價方式通常是直接影響組織獲利能力的重要策略考量。</span><span class="sxs-lookup"><span data-stu-id="4503c-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="4503c-126">當您的組織準備好要確定其設定人力資源時間帳單及成本費率所需的方式時，請與財務團隊和執業負責人合作。</span><span class="sxs-lookup"><span data-stu-id="4503c-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="4503c-127">其他定價考量包括是否要重複使用並非目前定價維度但套用做為組織定價維度的欄位或實體。</span><span class="sxs-lookup"><span data-stu-id="4503c-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="4503c-128">像 **交易類別** (**msdyn_transactioncategory**) 和 **可預約資源** (**bookableresource**) 等欄位即是候選維度的範例。</span><span class="sxs-lookup"><span data-stu-id="4503c-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="4503c-129">考慮定價維度要使用的是表格還是選項組。</span><span class="sxs-lookup"><span data-stu-id="4503c-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="4503c-130">如果您預料維度值的變動會超過 10 或 12，而您在這些值上需要其他屬性時，請建立實體，而不是選項組。</span><span class="sxs-lookup"><span data-stu-id="4503c-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="4503c-131">維護選項組 (例如新增或移除值) 時，需要系統管理員或開發人員，而將新的列新增至表格則可由大多數商務使用者來完成。</span><span class="sxs-lookup"><span data-stu-id="4503c-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="4503c-132">下列範例顯示根據角色以及資源所隸屬資源分配組織單位所設定的帳單費率。</span><span class="sxs-lookup"><span data-stu-id="4503c-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="4503c-133">成本費率通常是根據員工的薪資範圍以及他們所屬組織單位來設定。</span><span class="sxs-lookup"><span data-stu-id="4503c-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="4503c-134">在此範例中，帳單費率表和成本費率表看起來如下。</span><span class="sxs-lookup"><span data-stu-id="4503c-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="4503c-135">**範例帳單費率**</span><span class="sxs-lookup"><span data-stu-id="4503c-135">**Sample bill rates**</span></span>

| <span data-ttu-id="4503c-136">角色</span><span class="sxs-lookup"><span data-stu-id="4503c-136">Role</span></span>        | <span data-ttu-id="4503c-137">組織單位</span><span class="sxs-lookup"><span data-stu-id="4503c-137">Org Unit</span></span>    |<span data-ttu-id="4503c-138">單位</span><span class="sxs-lookup"><span data-stu-id="4503c-138">Unit</span></span>      |<span data-ttu-id="4503c-139">價格</span><span class="sxs-lookup"><span data-stu-id="4503c-139">Price</span></span>      |<span data-ttu-id="4503c-140">貨幣</span><span class="sxs-lookup"><span data-stu-id="4503c-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="4503c-141">開發人員</span><span class="sxs-lookup"><span data-stu-id="4503c-141">Developer</span></span>   | <span data-ttu-id="4503c-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4503c-142">Contoso US</span></span>  |<span data-ttu-id="4503c-143">Hour</span><span class="sxs-lookup"><span data-stu-id="4503c-143">Hour</span></span> | <span data-ttu-id="4503c-144">200</span><span class="sxs-lookup"><span data-stu-id="4503c-144">200</span></span>|<span data-ttu-id="4503c-145">USD</span><span class="sxs-lookup"><span data-stu-id="4503c-145">USD</span></span>     |
| <span data-ttu-id="4503c-146">開發人員</span><span class="sxs-lookup"><span data-stu-id="4503c-146">Developer</span></span>   | <span data-ttu-id="4503c-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="4503c-147">Contoso India</span></span> |<span data-ttu-id="4503c-148">Hour</span><span class="sxs-lookup"><span data-stu-id="4503c-148">Hour</span></span>|   <span data-ttu-id="4503c-149">112</span><span class="sxs-lookup"><span data-stu-id="4503c-149">112</span></span>|<span data-ttu-id="4503c-150">USD</span><span class="sxs-lookup"><span data-stu-id="4503c-150">USD</span></span>     |


<span data-ttu-id="4503c-151">**範例成本費率**</span><span class="sxs-lookup"><span data-stu-id="4503c-151">**Sample cost rates**</span></span>

| <span data-ttu-id="4503c-152">薪資範圍</span><span class="sxs-lookup"><span data-stu-id="4503c-152">Salary Band</span></span>     | <span data-ttu-id="4503c-153">組織單位</span><span class="sxs-lookup"><span data-stu-id="4503c-153">Org Unit</span></span>    |<span data-ttu-id="4503c-154">單位</span><span class="sxs-lookup"><span data-stu-id="4503c-154">Unit</span></span>      |<span data-ttu-id="4503c-155">價格</span><span class="sxs-lookup"><span data-stu-id="4503c-155">Price</span></span>      |<span data-ttu-id="4503c-156">貨幣</span><span class="sxs-lookup"><span data-stu-id="4503c-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="4503c-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="4503c-157">My company_Band1</span></span> | <span data-ttu-id="4503c-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4503c-158">Contoso US</span></span>  |<span data-ttu-id="4503c-159">Hour</span><span class="sxs-lookup"><span data-stu-id="4503c-159">Hour</span></span> | <span data-ttu-id="4503c-160">145</span><span class="sxs-lookup"><span data-stu-id="4503c-160">145</span></span>|<span data-ttu-id="4503c-161">USD</span><span class="sxs-lookup"><span data-stu-id="4503c-161">USD</span></span>     |
| <span data-ttu-id="4503c-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="4503c-162">My company_Band2</span></span> | <span data-ttu-id="4503c-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="4503c-163">Contoso India</span></span> |<span data-ttu-id="4503c-164">Hour</span><span class="sxs-lookup"><span data-stu-id="4503c-164">Hour</span></span>|   <span data-ttu-id="4503c-165">67</span><span class="sxs-lookup"><span data-stu-id="4503c-165">67</span></span>|<span data-ttu-id="4503c-166">USD</span><span class="sxs-lookup"><span data-stu-id="4503c-166">USD</span></span>     |
