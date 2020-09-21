---
title: 定價和成本維度首頁
description: 本主題提供定價維度的概觀。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749896"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="81e46-103">定價和成本維度首頁</span><span class="sxs-lookup"><span data-stu-id="81e46-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="81e46-104">設定人力資源所用定價及成本的維度分為兩個類別：</span><span class="sxs-lookup"><span data-stu-id="81e46-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="81e46-105">人員</span><span class="sxs-lookup"><span data-stu-id="81e46-105">People</span></span>
- <span data-ttu-id="81e46-106">計劃的工作</span><span class="sxs-lookup"><span data-stu-id="81e46-106">Planned work</span></span>

<span data-ttu-id="81e46-107">因此，Project Service Automation (PSA) 中提供兩種類型的定價維度值：</span><span class="sxs-lookup"><span data-stu-id="81e46-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="81e46-108">**選項組** - 本身是一組固定列舉值的維度。</span><span class="sxs-lookup"><span data-stu-id="81e46-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="81e46-109">**以實體為準的值** - 本身可以是各不相同值集的維度。</span><span class="sxs-lookup"><span data-stu-id="81e46-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="81e46-110">定價維度</span><span class="sxs-lookup"><span data-stu-id="81e46-110">Pricing dimensions</span></span>

<span data-ttu-id="81e46-111">PSA 隨附一組預設定價維度。</span><span class="sxs-lookup"><span data-stu-id="81e46-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="81e46-112">您可以移至 **Project Service** > **參數**來檢視這些維度。</span><span class="sxs-lookup"><span data-stu-id="81e46-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="81e46-113">在參數記錄的**以金額為準的定價維度**索引標籤上，確認角色 **msdyn_resourcecategory** 和資源分配單位 **msdyn_organizationalunit** 的**適用於銷售**及**適用於成本**欄位已設定為**是**。</span><span class="sxs-lookup"><span data-stu-id="81e46-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="81e46-114">這可讓您設定每個角色與組織單位組合的價格和成本。</span><span class="sxs-lookup"><span data-stu-id="81e46-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![反白顯示「適用於銷售」的 Project Service 參數螢幕擷取畫面](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="81e46-116">如果您在 PSA 版本 3 之前一直都使用角色和組織單位的預設欄位做為定價維度，就不會有任何看得出的變更。</span><span class="sxs-lookup"><span data-stu-id="81e46-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="81e46-117">您可以繼續照常使用 Project Service。</span><span class="sxs-lookup"><span data-stu-id="81e46-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="81e46-118">如果您需要使用其他屬性來為資源定訂價格或估算成本，則可以建立自訂欄位、實體和維度。</span><span class="sxs-lookup"><span data-stu-id="81e46-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="81e46-119">如需詳細資訊，請參閱下列主題，但請注意，您必須依照下列順序完成程序：</span><span class="sxs-lookup"><span data-stu-id="81e46-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="81e46-120">建立自訂欄位和實體</span><span class="sxs-lookup"><span data-stu-id="81e46-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="81e46-121">將自訂欄位新增至價格設定與交易實體</span><span class="sxs-lookup"><span data-stu-id="81e46-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="81e46-122">將自訂欄位設定為定價維度</span><span class="sxs-lookup"><span data-stu-id="81e46-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="81e46-123">更新外掛程式屬性以包含新的定價維度</span><span class="sxs-lookup"><span data-stu-id="81e46-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="81e46-124">定訂人力資源時間價格</span><span class="sxs-lookup"><span data-stu-id="81e46-124">Pricing human resource time</span></span>
<span data-ttu-id="81e46-125">組織對人力資源時間的定價方式通常是直接影響組織獲利能力的重要策略考量。</span><span class="sxs-lookup"><span data-stu-id="81e46-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="81e46-126">當您的組織準備好要確定其設定人力資源時間帳單及成本費率所需的方式時，請與財務團隊和執業負責人合作。</span><span class="sxs-lookup"><span data-stu-id="81e46-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="81e46-127">其他定價考量包括是否要重複使用並非目前定價維度但套用做為組織定價維度的欄位或實體。</span><span class="sxs-lookup"><span data-stu-id="81e46-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="81e46-128">像**交易類別** (**msdyn_transactioncategory**) 和**可預約資源** (**bookableresource**) 等欄位即是候選維度的範例。</span><span class="sxs-lookup"><span data-stu-id="81e46-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="81e46-129">您也應該考慮定價維度要使用的是表格還是選項組。</span><span class="sxs-lookup"><span data-stu-id="81e46-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="81e46-130">如果您預料維度值的變動會超過 10 或 12，而您在這些值上需要其他屬性時，您可以建立實體，而不是選項組。</span><span class="sxs-lookup"><span data-stu-id="81e46-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="81e46-131">維護選項組 (例如新增或移除值) 時，需要系統管理員或開發人員，而將新的列新增至表格則可由大多數使用者來完成。</span><span class="sxs-lookup"><span data-stu-id="81e46-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="81e46-132">下列範例顯示根據角色以及資源所隸屬資源分配組織單位所設定的帳單費率。</span><span class="sxs-lookup"><span data-stu-id="81e46-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="81e46-133">成本費率通常是根據員工的薪資範圍以及他們所屬組織單位來設定。</span><span class="sxs-lookup"><span data-stu-id="81e46-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="81e46-134">在此範例中，帳單費率表和成本費率表看起來如下。</span><span class="sxs-lookup"><span data-stu-id="81e46-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="81e46-135">**範例帳單費率**</span><span class="sxs-lookup"><span data-stu-id="81e46-135">**Sample bill rates**</span></span>

| <span data-ttu-id="81e46-136">角色</span><span class="sxs-lookup"><span data-stu-id="81e46-136">Role</span></span>        | <span data-ttu-id="81e46-137">組織單位</span><span class="sxs-lookup"><span data-stu-id="81e46-137">Org Unit</span></span>    |<span data-ttu-id="81e46-138">單位</span><span class="sxs-lookup"><span data-stu-id="81e46-138">Unit</span></span>      |<span data-ttu-id="81e46-139">價格</span><span class="sxs-lookup"><span data-stu-id="81e46-139">Price</span></span>      |<span data-ttu-id="81e46-140">貨幣</span><span class="sxs-lookup"><span data-stu-id="81e46-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="81e46-141">開發人員</span><span class="sxs-lookup"><span data-stu-id="81e46-141">Developer</span></span>   | <span data-ttu-id="81e46-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="81e46-142">Contoso US</span></span>  |<span data-ttu-id="81e46-143">Hour</span><span class="sxs-lookup"><span data-stu-id="81e46-143">Hour</span></span> | <span data-ttu-id="81e46-144">200</span><span class="sxs-lookup"><span data-stu-id="81e46-144">200</span></span>|<span data-ttu-id="81e46-145">USD</span><span class="sxs-lookup"><span data-stu-id="81e46-145">USD</span></span>     |
| <span data-ttu-id="81e46-146">開發人員</span><span class="sxs-lookup"><span data-stu-id="81e46-146">Developer</span></span>   | <span data-ttu-id="81e46-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="81e46-147">Contoso India</span></span> |<span data-ttu-id="81e46-148">Hour</span><span class="sxs-lookup"><span data-stu-id="81e46-148">Hour</span></span>|   <span data-ttu-id="81e46-149">112</span><span class="sxs-lookup"><span data-stu-id="81e46-149">112</span></span>|<span data-ttu-id="81e46-150">USD</span><span class="sxs-lookup"><span data-stu-id="81e46-150">USD</span></span>     |


<span data-ttu-id="81e46-151">**範例成本費率**</span><span class="sxs-lookup"><span data-stu-id="81e46-151">**Sample cost rates**</span></span>

| <span data-ttu-id="81e46-152">薪資範圍</span><span class="sxs-lookup"><span data-stu-id="81e46-152">Salary Band</span></span>     | <span data-ttu-id="81e46-153">組織單位</span><span class="sxs-lookup"><span data-stu-id="81e46-153">Org Unit</span></span>    |<span data-ttu-id="81e46-154">單位</span><span class="sxs-lookup"><span data-stu-id="81e46-154">Unit</span></span>      |<span data-ttu-id="81e46-155">價格</span><span class="sxs-lookup"><span data-stu-id="81e46-155">Price</span></span>      |<span data-ttu-id="81e46-156">貨幣</span><span class="sxs-lookup"><span data-stu-id="81e46-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="81e46-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="81e46-157">My company_Band1</span></span> | <span data-ttu-id="81e46-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="81e46-158">Contoso US</span></span>  |<span data-ttu-id="81e46-159">Hour</span><span class="sxs-lookup"><span data-stu-id="81e46-159">Hour</span></span> | <span data-ttu-id="81e46-160">145</span><span class="sxs-lookup"><span data-stu-id="81e46-160">145</span></span>|<span data-ttu-id="81e46-161">USD</span><span class="sxs-lookup"><span data-stu-id="81e46-161">USD</span></span>     |
| <span data-ttu-id="81e46-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="81e46-162">My company_Band2</span></span> | <span data-ttu-id="81e46-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="81e46-163">Contoso India</span></span> |<span data-ttu-id="81e46-164">Hour</span><span class="sxs-lookup"><span data-stu-id="81e46-164">Hour</span></span>|   <span data-ttu-id="81e46-165">67</span><span class="sxs-lookup"><span data-stu-id="81e46-165">67</span></span>|<span data-ttu-id="81e46-166">USD</span><span class="sxs-lookup"><span data-stu-id="81e46-166">USD</span></span>     |
