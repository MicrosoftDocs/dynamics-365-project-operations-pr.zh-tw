---
title: 將自訂欄位設定為定價維度
description: 本主題提供有關如何使用自訂欄位進行定價維度設定的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 087950c9639a95868a20d71286dfad4437555108
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072991"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="85821-103">將自訂欄位設定為定價維度</span><span class="sxs-lookup"><span data-stu-id="85821-103">Set up custom fields as pricing dimensions</span></span>

<span data-ttu-id="85821-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="85821-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="85821-105">開始之前，本主題假設您已完成[建立自訂欄位和實體](create-custom-fields-entities-pricing-dimensions.md)以及[將必要的自訂欄位新增至價格設定與交易實體](add-custom-fields-price-setup-transactional-entities.md)主題中的程序。</span><span class="sxs-lookup"><span data-stu-id="85821-105">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities-pricing-dimensions.md) and [Add required custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span> <span data-ttu-id="85821-106">如果您尚未完成這些程序，請返回並加以完，然後再回到本主題。</span><span class="sxs-lookup"><span data-stu-id="85821-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="85821-107">本主題提供有關設定自訂定價維度的資訊。</span><span class="sxs-lookup"><span data-stu-id="85821-107">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="85821-108">在 **參數** 頁面上， **以金額為準的定價維度** 索引標籤會顯示定價維度實體中的記錄。</span><span class="sxs-lookup"><span data-stu-id="85821-108">On the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="85821-109">此索引標籤中的網格預設會有兩列：</span><span class="sxs-lookup"><span data-stu-id="85821-109">By default, there are two rows in the grid on this tab:</span></span>

- <span data-ttu-id="85821-110">**msdyn_resourcecategory** (角色)</span><span class="sxs-lookup"><span data-stu-id="85821-110">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="85821-111">**msdyn_OrganizationalUnit** (組織單位)</span><span class="sxs-lookup"><span data-stu-id="85821-111">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85821-112">請勿刪除這些列。</span><span class="sxs-lookup"><span data-stu-id="85821-112">Do not delete these rows.</span></span> <span data-ttu-id="85821-113">不過，如果您不需要這些列，則可以將 **適用於成本** 、 **適用於銷售** 和 **適用於購買** 都設定為 **否** ，將其設定為不適用於特定內容。</span><span class="sxs-lookup"><span data-stu-id="85821-113">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost** , **Applicable to Sales** , and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="85821-114">將這些屬性值設定為 **否** ，效果如同未將欄位設定為定價維度。</span><span class="sxs-lookup"><span data-stu-id="85821-114">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="85821-115">若要讓欄位變成定價維度，該欄位必須：</span><span class="sxs-lookup"><span data-stu-id="85821-115">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="85821-116">建立為 **角色價格** 和 **角色價格加成** 實體中的欄位。</span><span class="sxs-lookup"><span data-stu-id="85821-116">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="85821-117">如需執行此動作的詳細資訊，請參[將自訂欄位新增至價格設定與交易實體](add-custom-fields-price-setup-transactional-entities.md)。</span><span class="sxs-lookup"><span data-stu-id="85821-117">For more information on how to do this, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>
- <span data-ttu-id="85821-118">建立為 **定價維度** 表格中的一列。</span><span class="sxs-lookup"><span data-stu-id="85821-118">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="85821-119">例如，新增如下圖形所示的定價維度列。</span><span class="sxs-lookup"><span data-stu-id="85821-119">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

<span data-ttu-id="85821-120">資源工作時數 ( **msdyn_resourceworkhours** ) 已新增為以加成為準的定價維度，並已新增至 **以加成為準的定價維度** 索引標籤上的網格。</span><span class="sxs-lookup"><span data-stu-id="85821-120">Resource Work hours ( **msdyn_resourceworkhours** ) is added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85821-121">任何對此表格中定價維度資料 (現有或新增) 的變更，只有在重新整理快取之後，才會傳播至定價商務規則。</span><span class="sxs-lookup"><span data-stu-id="85821-121">Any change to pricing dimension data in this table, existing or new, is propagated to the pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="85821-122">快取重新整理時間可能需要長達 10 分鐘。</span><span class="sxs-lookup"><span data-stu-id="85821-122">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="85821-123">請等待這段時間過後，再查看必須從定價維度資料變更產生之價格預設邏輯中的變更。</span><span class="sxs-lookup"><span data-stu-id="85821-123">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="85821-124">定價維度表格的屬性</span><span class="sxs-lookup"><span data-stu-id="85821-124">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="85821-125">以下各節提供有關 **定價維度** 表格中不同屬性的資訊。</span><span class="sxs-lookup"><span data-stu-id="85821-125">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="85821-126">定價維度名稱</span><span class="sxs-lookup"><span data-stu-id="85821-126">Pricing Dimension Name</span></span>
<span data-ttu-id="85821-127">此值應與新增至自訂定價維度之 **角色價格** 表格中的欄位結構描述名稱相同。</span><span class="sxs-lookup"><span data-stu-id="85821-127">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="85821-128">如需有關將欄位新增至 **角色價格** 表格的詳細資訊，請參閱[將自訂欄位新增至價格設定與交易實體](add-custom-fields-price-setup-transactional-entities.md)。</span><span class="sxs-lookup"><span data-stu-id="85821-128">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="85821-129">維度的類型</span><span class="sxs-lookup"><span data-stu-id="85821-129">Type of dimension</span></span>
<span data-ttu-id="85821-130">定維度有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="85821-130">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="85821-131">**以金額為準的維度** ：輸入內容中的維度值會與 **角色價格** 明細上的維度值相符合，而且直接由 **角色價格** 表格預設價格/成本。</span><span class="sxs-lookup"><span data-stu-id="85821-131">**Amount-based dimensions** : The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="85821-132">**以加成為準的維度** ：這些維度是使用下列三步驟程序取得價格/成本的維度。</span><span class="sxs-lookup"><span data-stu-id="85821-132">**Markup-based dimensions** : These are dimensions where the following three-step process to get the price/cost is used:</span></span>
 
    1. <span data-ttu-id="85821-133">來自輸入內容的非以加成為準的維度值會與角色價格明細進行比對以取得基準費率。</span><span class="sxs-lookup"><span data-stu-id="85821-133">The non-markup-based dimension values from the input context are matched to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="85821-134">來自輸入內容的維度值會與 **角色價格加成** 明細進行比對以取得加成百分比。</span><span class="sxs-lookup"><span data-stu-id="85821-134">The dimension values from the input context are matched to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="85821-135">第二個步驟產生的加成百分比會套用至第一個步驟從 **角色價格** 表格所取得的基準費率，以決定最終價格/成本。</span><span class="sxs-lookup"><span data-stu-id="85821-135">The markup percentage from the second step is applied to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="85821-136">下表說明價格加成的計算。</span><span class="sxs-lookup"><span data-stu-id="85821-136">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="85821-137">角色</span><span class="sxs-lookup"><span data-stu-id="85821-137">Role</span></span>        | <span data-ttu-id="85821-138">組織單位</span><span class="sxs-lookup"><span data-stu-id="85821-138">Org Unit</span></span>    |<span data-ttu-id="85821-139">工作地點</span><span class="sxs-lookup"><span data-stu-id="85821-139">Work Location</span></span>      |<span data-ttu-id="85821-140">標準職稱</span><span class="sxs-lookup"><span data-stu-id="85821-140">Standard Title</span></span>      |<span data-ttu-id="85821-141">資源工作時數</span><span class="sxs-lookup"><span data-stu-id="85821-141">Resource Work Hours</span></span>      |  <span data-ttu-id="85821-142">加成</span><span class="sxs-lookup"><span data-stu-id="85821-142">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="85821-143">Contoso India</span><span class="sxs-lookup"><span data-stu-id="85821-143">Contoso India</span></span>|<span data-ttu-id="85821-144">現場</span><span class="sxs-lookup"><span data-stu-id="85821-144">Onsite</span></span>            |                    |<span data-ttu-id="85821-145">加班時間</span><span class="sxs-lookup"><span data-stu-id="85821-145">Overtime</span></span>                 |<span data-ttu-id="85821-146">15</span><span class="sxs-lookup"><span data-stu-id="85821-146">15</span></span>     |
|             | <span data-ttu-id="85821-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="85821-147">Contoso India</span></span>|<span data-ttu-id="85821-148">本機</span><span class="sxs-lookup"><span data-stu-id="85821-148">Local</span></span>             |                    |<span data-ttu-id="85821-149">加班時間</span><span class="sxs-lookup"><span data-stu-id="85821-149">Overtime</span></span>                 |<span data-ttu-id="85821-150">10</span><span class="sxs-lookup"><span data-stu-id="85821-150">10</span></span>     |
|             | <span data-ttu-id="85821-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="85821-151">Contoso US</span></span>   |<span data-ttu-id="85821-152">本機</span><span class="sxs-lookup"><span data-stu-id="85821-152">Local</span></span>             |                    |<span data-ttu-id="85821-153">加班時間</span><span class="sxs-lookup"><span data-stu-id="85821-153">Overtime</span></span>                 |<span data-ttu-id="85821-154">20</span><span class="sxs-lookup"><span data-stu-id="85821-154">20</span></span>     |


<span data-ttu-id="85821-155">如果來自 Contoso India、基準費率為 100 美元的資源在現場工作，而他們在時間項目上記入了 8 小時正常工時與 2 小時加班工時，此定價引擎將會使用 8 小時的基準費率 100，將 800 美元列入記錄。</span><span class="sxs-lookup"><span data-stu-id="85821-155">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="85821-156">至於 2 小時加班工時，則將 15% 的加成套用至基準費率 100 以取得 115 美元的單價，並記錄 230 美元的總成本。</span><span class="sxs-lookup"><span data-stu-id="85821-156">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="85821-157">適用於成本</span><span class="sxs-lookup"><span data-stu-id="85821-157">Applicable to Cost</span></span> 
<span data-ttu-id="85821-158">如果此選項設定為 **是** ，即表示擷取成本及加成費率時，應使用來自輸入內容的維度值，與 **角色價格** 和 **角色價格加成** 進行比對。</span><span class="sxs-lookup"><span data-stu-id="85821-158">If this is set to **Yes** , it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="85821-159">適用於銷售</span><span class="sxs-lookup"><span data-stu-id="85821-159">Applicable to Sales</span></span>
<span data-ttu-id="85821-160">如果此選項設定為 **是** ，即表示擷取帳單及加成費率時，應使用來自輸入內容的維度值，與 **角色價格** 和 **角色價格加成** 進行比對。</span><span class="sxs-lookup"><span data-stu-id="85821-160">If this is set to **Yes** , it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="85821-161">適用於購買</span><span class="sxs-lookup"><span data-stu-id="85821-161">Applicable to Purchase</span></span>
<span data-ttu-id="85821-162">如果此選項設定為 **是** ，即表示擷取購買價時，應使用來自輸入內容的維度值，與 **角色價格** 和 **角色價格加成** 進行比對。</span><span class="sxs-lookup"><span data-stu-id="85821-162">If this is set to **Yes** , it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="85821-163">不支援轉承包案例，因此不使用此欄位。</span><span class="sxs-lookup"><span data-stu-id="85821-163">Subcontracting scenarios are not supported, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="85821-164">優先順序</span><span class="sxs-lookup"><span data-stu-id="85821-164">Priority</span></span>
<span data-ttu-id="85821-165">設定維度優先順序有助於定價，即使在輸入維度值與 **角色價格** 或 **角色價格加成** 表格中的值之間找不到完全相符的項目時，也能產生價格。</span><span class="sxs-lookup"><span data-stu-id="85821-165">Setting the dimension priority helps pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="85821-166">此案例依照維度優先順序對這些維度進行加權，並使用 Null 值表示不相符的維度值。</span><span class="sxs-lookup"><span data-stu-id="85821-166">In this scenario, null values are used for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="85821-167">**成本優先順序** ：依據成本價設定比對相符時，維度的成本優先順序值將指示該維度的權數。</span><span class="sxs-lookup"><span data-stu-id="85821-167">**Cost Priority** : The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="85821-168">**成本優先順序** 值在所有 **適用於成本** 的維度中須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="85821-168">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="85821-169">**銷售優先順序** ：依據銷售價或帳單費率設定比對相符時，維度的銷售優先順序值將指示該維度的權數。</span><span class="sxs-lookup"><span data-stu-id="85821-169">**Sales Priority** : The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="85821-170">**銷售優先順序** 值在所有 **適用於銷售** 的維度中須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="85821-170">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>
