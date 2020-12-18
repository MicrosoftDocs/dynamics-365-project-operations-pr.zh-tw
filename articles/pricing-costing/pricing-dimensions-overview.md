---
title: 定價維度概觀
description: 本主題提供有關 Dynamics 365 Project Operations 中定價維度的資訊。
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 33f55976eafedd046fba952ab6381c297ab4e271
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650175"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="89a35-103">定價維度概觀</span><span class="sxs-lookup"><span data-stu-id="89a35-103">Pricing dimensions overview</span></span>

<span data-ttu-id="89a35-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="89a35-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="89a35-105">設定人力資源所用定價及成本的維度分為兩個類別：</span><span class="sxs-lookup"><span data-stu-id="89a35-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="89a35-106">人員</span><span class="sxs-lookup"><span data-stu-id="89a35-106">People</span></span>
- <span data-ttu-id="89a35-107">計劃的工作</span><span class="sxs-lookup"><span data-stu-id="89a35-107">Planned work</span></span>

<span data-ttu-id="89a35-108">因此，有兩種類型的定價維度值可用：</span><span class="sxs-lookup"><span data-stu-id="89a35-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="89a35-109">**選項組**：本身是一組固定列舉值的維度。</span><span class="sxs-lookup"><span data-stu-id="89a35-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="89a35-110">**以實體為準的值**：本身可以是各不相同值集的維度。</span><span class="sxs-lookup"><span data-stu-id="89a35-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="89a35-111">定價維度</span><span class="sxs-lookup"><span data-stu-id="89a35-111">Pricing dimensions</span></span>

<span data-ttu-id="89a35-112">Dynamics 365 Project Operations 隨附一組預設定價維度。</span><span class="sxs-lookup"><span data-stu-id="89a35-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="89a35-113">您可以移至 **Project Operations** > **參數** 來檢視這些定價維度。</span><span class="sxs-lookup"><span data-stu-id="89a35-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="89a35-114">在參數記錄的 **以金額為準的定價維度** 索引標籤上，確認角色 **msdyn_resourcecategory** 和資源分配單位 **msdyn_organizationalunit** 的 **適用於銷售** 及 **適用於成本** 欄位已設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="89a35-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="89a35-115">啟用這些欄位後，您就可以設定每個角色與組織單位組合的價格和成本。</span><span class="sxs-lookup"><span data-stu-id="89a35-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![反白顯示「適用於銷售」的 Project Service 參數螢幕擷取畫面](media/PS-OOB-parameters.png)

<span data-ttu-id="89a35-117">如果您需要使用其他屬性來為資源定訂價格或估算成本，則可以建立自訂欄位、實體和維度。</span><span class="sxs-lookup"><span data-stu-id="89a35-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="89a35-118">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="89a35-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="89a35-119">必須按照所列的順序來完成程序。</span><span class="sxs-lookup"><span data-stu-id="89a35-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="89a35-120">建立自訂定價維度解決方案</span><span class="sxs-lookup"><span data-stu-id="89a35-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="89a35-121">建立自訂欄位和實體</span><span class="sxs-lookup"><span data-stu-id="89a35-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="89a35-122">將自訂欄位新增至價格設定與交易實體</span><span class="sxs-lookup"><span data-stu-id="89a35-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="89a35-123">將自訂欄位設定為定價維度</span><span class="sxs-lookup"><span data-stu-id="89a35-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="89a35-124">更新外掛程式屬性以包含新的定價維度</span><span class="sxs-lookup"><span data-stu-id="89a35-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="89a35-125">定訂人力資源時間價格</span><span class="sxs-lookup"><span data-stu-id="89a35-125">Pricing human resource time</span></span>
<span data-ttu-id="89a35-126">組織對人力資源時間的定價方式通常是直接影響組織獲利能力的重要策略考量。</span><span class="sxs-lookup"><span data-stu-id="89a35-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="89a35-127">當您的組織準備好要確定其設定人力資源時間帳單及成本費率所需的方式時，請與財務團隊和執業負責人合作。</span><span class="sxs-lookup"><span data-stu-id="89a35-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="89a35-128">其他定價考量包括是否要重複使用並非目前定價維度但套用做為組織定價維度的欄位或實體。</span><span class="sxs-lookup"><span data-stu-id="89a35-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="89a35-129">像 **交易類別** (**msdyn_transactioncategory**) 和 **可預約資源** (**bookableresource**) 等欄位即是候選維度的範例。</span><span class="sxs-lookup"><span data-stu-id="89a35-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="89a35-130">考慮定價維度要使用的是表格還是選項組。</span><span class="sxs-lookup"><span data-stu-id="89a35-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="89a35-131">如果您預料維度值的變動會超過 10 或 12，而您在這些值上需要其他屬性時，您可以建立實體，而不是選項組。</span><span class="sxs-lookup"><span data-stu-id="89a35-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="89a35-132">維護選項組 (例如新增或移除值) 時，需要系統管理員或開發人員，而將新的列新增至表格則可由大多數使用者來完成。</span><span class="sxs-lookup"><span data-stu-id="89a35-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="89a35-133">下列範例顯示根據角色以及資源所隸屬資源分配組織單位所設定的帳單費率。</span><span class="sxs-lookup"><span data-stu-id="89a35-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="89a35-134">成本費率通常是根據員工的薪資範圍以及他們所屬組織單位來設定。</span><span class="sxs-lookup"><span data-stu-id="89a35-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="89a35-135">在此範例中，帳單費率表和成本費率表看起來如下。</span><span class="sxs-lookup"><span data-stu-id="89a35-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="89a35-136">**範例帳單費率**</span><span class="sxs-lookup"><span data-stu-id="89a35-136">**Sample bill rates**</span></span>

| <span data-ttu-id="89a35-137">角色</span><span class="sxs-lookup"><span data-stu-id="89a35-137">Role</span></span>        | <span data-ttu-id="89a35-138">組織單位</span><span class="sxs-lookup"><span data-stu-id="89a35-138">Org Unit</span></span>    |<span data-ttu-id="89a35-139">單位</span><span class="sxs-lookup"><span data-stu-id="89a35-139">Unit</span></span>      |<span data-ttu-id="89a35-140">價格</span><span class="sxs-lookup"><span data-stu-id="89a35-140">Price</span></span>      |<span data-ttu-id="89a35-141">貨幣</span><span class="sxs-lookup"><span data-stu-id="89a35-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="89a35-142">開發人員</span><span class="sxs-lookup"><span data-stu-id="89a35-142">Developer</span></span>   | <span data-ttu-id="89a35-143">Contoso US</span><span class="sxs-lookup"><span data-stu-id="89a35-143">Contoso US</span></span>  |<span data-ttu-id="89a35-144">Hour</span><span class="sxs-lookup"><span data-stu-id="89a35-144">Hour</span></span> | <span data-ttu-id="89a35-145">200</span><span class="sxs-lookup"><span data-stu-id="89a35-145">200</span></span>|<span data-ttu-id="89a35-146">USD</span><span class="sxs-lookup"><span data-stu-id="89a35-146">USD</span></span>     |
| <span data-ttu-id="89a35-147">開發人員</span><span class="sxs-lookup"><span data-stu-id="89a35-147">Developer</span></span>   | <span data-ttu-id="89a35-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="89a35-148">Contoso India</span></span> |<span data-ttu-id="89a35-149">Hour</span><span class="sxs-lookup"><span data-stu-id="89a35-149">Hour</span></span>|   <span data-ttu-id="89a35-150">112</span><span class="sxs-lookup"><span data-stu-id="89a35-150">112</span></span>|<span data-ttu-id="89a35-151">USD</span><span class="sxs-lookup"><span data-stu-id="89a35-151">USD</span></span>     |


<span data-ttu-id="89a35-152">**範例成本費率**</span><span class="sxs-lookup"><span data-stu-id="89a35-152">**Sample cost rates**</span></span>

| <span data-ttu-id="89a35-153">薪資範圍</span><span class="sxs-lookup"><span data-stu-id="89a35-153">Salary Band</span></span>     | <span data-ttu-id="89a35-154">組織單位</span><span class="sxs-lookup"><span data-stu-id="89a35-154">Org Unit</span></span>    |<span data-ttu-id="89a35-155">單位</span><span class="sxs-lookup"><span data-stu-id="89a35-155">Unit</span></span>      |<span data-ttu-id="89a35-156">價格</span><span class="sxs-lookup"><span data-stu-id="89a35-156">Price</span></span>      |<span data-ttu-id="89a35-157">貨幣</span><span class="sxs-lookup"><span data-stu-id="89a35-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="89a35-158">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="89a35-158">My company_Band1</span></span> | <span data-ttu-id="89a35-159">Contoso US</span><span class="sxs-lookup"><span data-stu-id="89a35-159">Contoso US</span></span>  |<span data-ttu-id="89a35-160">Hour</span><span class="sxs-lookup"><span data-stu-id="89a35-160">Hour</span></span> | <span data-ttu-id="89a35-161">145</span><span class="sxs-lookup"><span data-stu-id="89a35-161">145</span></span>|<span data-ttu-id="89a35-162">USD</span><span class="sxs-lookup"><span data-stu-id="89a35-162">USD</span></span>     |
| <span data-ttu-id="89a35-163">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="89a35-163">My company_Band2</span></span> | <span data-ttu-id="89a35-164">Contoso India</span><span class="sxs-lookup"><span data-stu-id="89a35-164">Contoso India</span></span> |<span data-ttu-id="89a35-165">Hour</span><span class="sxs-lookup"><span data-stu-id="89a35-165">Hour</span></span>|   <span data-ttu-id="89a35-166">67</span><span class="sxs-lookup"><span data-stu-id="89a35-166">67</span></span>|<span data-ttu-id="89a35-167">USD</span><span class="sxs-lookup"><span data-stu-id="89a35-167">USD</span></span>     |
