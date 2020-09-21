---
title: 將自訂欄位設定為定價維度
description: 本主題提供有關設定自訂定價維度的資訊。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: d5f59779-a6ed-4854-ab82-2810dace288f
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 8f19254acfc7f03ed7ccca95ed7e2b94cc199d3b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749885"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="e59b9-103">將自訂欄位設定為定價維度</span><span class="sxs-lookup"><span data-stu-id="e59b9-103">Set up custom fields as pricing dimensions</span></span> 

<span data-ttu-id="e59b9-104">開始之前，本主題假設您已完成[建立自訂欄位和實體](create-custom-fields-entities.md)以及[將自訂欄位新增至價格設定與交易實體](field-references.md)主題中的程序。</span><span class="sxs-lookup"><span data-stu-id="e59b9-104">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md) and [Add custom fields to price setup and transactional entities](field-references.md).</span></span> <span data-ttu-id="e59b9-105">如果您尚未完成這些程序，請返回並加以完，然後再回到本主題。</span><span class="sxs-lookup"><span data-stu-id="e59b9-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="e59b9-106">本主題提供有關設定自訂定價維度的資訊。</span><span class="sxs-lookup"><span data-stu-id="e59b9-106">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="e59b9-107">在 Project Service Web 介面的**參數**頁面中，**以金額為準的定價維度**索引標籤會顯示定價維度實體中的記錄。</span><span class="sxs-lookup"><span data-stu-id="e59b9-107">In the Project Service web interface, on the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="e59b9-108">Project Service 安裝預設會在此索引標籤的網格中建立 2 個列：</span><span class="sxs-lookup"><span data-stu-id="e59b9-108">By default, Project Service installation creates 2 rows in the grid on this tab:</span></span>

- <span data-ttu-id="e59b9-109">**msdyn_resourcecategory** (角色)</span><span class="sxs-lookup"><span data-stu-id="e59b9-109">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="e59b9-110">**msdyn_OrganizationalUnit** (組織單位)</span><span class="sxs-lookup"><span data-stu-id="e59b9-110">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e59b9-111">請勿刪除這些列。</span><span class="sxs-lookup"><span data-stu-id="e59b9-111">Do not delete these rows.</span></span> <span data-ttu-id="e59b9-112">不過，如果您不需要這些列，則可以將**適用於成本**、**適用於銷售**和**適用於購買**都設定為**否**，將其設定為不適用於特定內容。</span><span class="sxs-lookup"><span data-stu-id="e59b9-112">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="e59b9-113">將這些屬性值設定為**否**，效果如同未將欄位設定為定價維度。</span><span class="sxs-lookup"><span data-stu-id="e59b9-113">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="e59b9-114">若要讓欄位變成定價維度，該欄位必須：</span><span class="sxs-lookup"><span data-stu-id="e59b9-114">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="e59b9-115">建立為**角色價格**和**角色價格加成**實體中的欄位。</span><span class="sxs-lookup"><span data-stu-id="e59b9-115">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="e59b9-116">如需執行此動作的詳細資訊，請參[將自訂欄位新增至價格設定與交易實體](field-references.md)。</span><span class="sxs-lookup"><span data-stu-id="e59b9-116">For more information on how to do this, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>
- <span data-ttu-id="e59b9-117">建立為**定價維度**表格中的一列。</span><span class="sxs-lookup"><span data-stu-id="e59b9-117">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="e59b9-118">例如，新增如下圖形所示的定價維度列。</span><span class="sxs-lookup"><span data-stu-id="e59b9-118">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

![以金額為準的定價維度列](media/Amt-based-PD.png)

<span data-ttu-id="e59b9-120">請注意，資源工作時數 (**msdyn_resourceworkhours**) 已新增為以加成為準的定價維度，並已新增至**以加成為準的定價維度**索引標籤上的網格。</span><span class="sxs-lookup"><span data-stu-id="e59b9-120">Notice that Resource Work hours (**msdyn_resourceworkhours**) has been added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

![以加成為準的定價維度列](media/Markup-based-PD.png)

> [!IMPORTANT]
> <span data-ttu-id="e59b9-122">任何對此表格中定價維度資料 (現有或新增) 的變更，只有在重新整理快取之後，才會傳播至 Project Service 定價商機規則。</span><span class="sxs-lookup"><span data-stu-id="e59b9-122">Any change to pricing dimension data in this table, existing or new, is propagated to the Project Service pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="e59b9-123">快取重新整理時間可能需要長達 10 分鐘。</span><span class="sxs-lookup"><span data-stu-id="e59b9-123">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="e59b9-124">請等待這段時間過後，再查看必須從定價維度資料變更產生之價格預設邏輯中的變更。</span><span class="sxs-lookup"><span data-stu-id="e59b9-124">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="e59b9-125">定價維度表格的屬性</span><span class="sxs-lookup"><span data-stu-id="e59b9-125">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="e59b9-126">以下各節提供有關**定價維度**表格中不同屬性的資訊。</span><span class="sxs-lookup"><span data-stu-id="e59b9-126">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="e59b9-127">定價維度名稱</span><span class="sxs-lookup"><span data-stu-id="e59b9-127">Pricing Dimension Name</span></span>
<span data-ttu-id="e59b9-128">此值應與新增至自訂定價維度之**角色價格**表格中的欄位結構描述名稱相同。</span><span class="sxs-lookup"><span data-stu-id="e59b9-128">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="e59b9-129">如需有關將欄位新增至**角色價格**表格的詳細資訊，請參閱[將自訂欄位新增至價格設定與交易實體](field-references.md)。</span><span class="sxs-lookup"><span data-stu-id="e59b9-129">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="e59b9-130">維度的類型</span><span class="sxs-lookup"><span data-stu-id="e59b9-130">Type of dimension</span></span>
<span data-ttu-id="e59b9-131">定維度有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="e59b9-131">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="e59b9-132">**以金額為準的維度**：輸入內容中的維度值會與**角色價格**明細上的維度值相符合，而且直接由**角色價格**表格預設價格/成本。</span><span class="sxs-lookup"><span data-stu-id="e59b9-132">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="e59b9-133">**以加成為準的維度**：這些是 Project Service 將採用下列 3 步驟程序取得價格/成本的維度。</span><span class="sxs-lookup"><span data-stu-id="e59b9-133">**Markup-based dimensions**: These are dimensions where Project Service will adopt the following 3-step process to get the price/cost</span></span>
 
    1. <span data-ttu-id="e59b9-134">Project Service 會將來自輸入內容的非以加成為準維度值與角色價格明細進行比對以取得基準費率。</span><span class="sxs-lookup"><span data-stu-id="e59b9-134">Project Service matches the non-markup-based dimension values from the input context to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="e59b9-135">Project Service 會將所有來自輸入內容的維度值與**角色價格加成**明細進行比對以取得加成百分比。</span><span class="sxs-lookup"><span data-stu-id="e59b9-135">Project Service matches all of the dimension values from the input context to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="e59b9-136">Project Service 會將第二個步驟產生的加成百分比套用至第一個步驟從**角色價格**表格取得的基準費率，以決定最終價格/成本。</span><span class="sxs-lookup"><span data-stu-id="e59b9-136">Project Service applies the markup percentage from the second step to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="e59b9-137">下表說明價格加成的計算。</span><span class="sxs-lookup"><span data-stu-id="e59b9-137">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="e59b9-138">角色</span><span class="sxs-lookup"><span data-stu-id="e59b9-138">Role</span></span>        | <span data-ttu-id="e59b9-139">組織單位</span><span class="sxs-lookup"><span data-stu-id="e59b9-139">Org Unit</span></span>    |<span data-ttu-id="e59b9-140">工作地點</span><span class="sxs-lookup"><span data-stu-id="e59b9-140">Work Location</span></span>      |<span data-ttu-id="e59b9-141">標準職稱</span><span class="sxs-lookup"><span data-stu-id="e59b9-141">Standard Title</span></span>      |<span data-ttu-id="e59b9-142">資源工作時數</span><span class="sxs-lookup"><span data-stu-id="e59b9-142">Resource Work Hours</span></span>      |  <span data-ttu-id="e59b9-143">加成</span><span class="sxs-lookup"><span data-stu-id="e59b9-143">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="e59b9-144">Contoso India</span><span class="sxs-lookup"><span data-stu-id="e59b9-144">Contoso India</span></span>|<span data-ttu-id="e59b9-145">現場</span><span class="sxs-lookup"><span data-stu-id="e59b9-145">Onsite</span></span>            |                    |<span data-ttu-id="e59b9-146">加班時間</span><span class="sxs-lookup"><span data-stu-id="e59b9-146">Overtime</span></span>                 |<span data-ttu-id="e59b9-147">15</span><span class="sxs-lookup"><span data-stu-id="e59b9-147">15</span></span>     |
|             | <span data-ttu-id="e59b9-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="e59b9-148">Contoso India</span></span>|<span data-ttu-id="e59b9-149">本機</span><span class="sxs-lookup"><span data-stu-id="e59b9-149">Local</span></span>             |                    |<span data-ttu-id="e59b9-150">加班時間</span><span class="sxs-lookup"><span data-stu-id="e59b9-150">Overtime</span></span>                 |<span data-ttu-id="e59b9-151">10</span><span class="sxs-lookup"><span data-stu-id="e59b9-151">10</span></span>     |
|             | <span data-ttu-id="e59b9-152">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e59b9-152">Contoso US</span></span>   |<span data-ttu-id="e59b9-153">本機</span><span class="sxs-lookup"><span data-stu-id="e59b9-153">Local</span></span>             |                    |<span data-ttu-id="e59b9-154">加班時間</span><span class="sxs-lookup"><span data-stu-id="e59b9-154">Overtime</span></span>                 |<span data-ttu-id="e59b9-155">20</span><span class="sxs-lookup"><span data-stu-id="e59b9-155">20</span></span>     |


<span data-ttu-id="e59b9-156">如果來自 Contoso India、基準費率為 100 USD 的資源在現場工作，而他們在時間項目上記入了 8 小時正常工時與 2 小時加班工時，此 Project Service pricing 定價引擎將會使用 base rate of 100 的基準費率乘上 8 小時以記錄 800 USD。</span><span class="sxs-lookup"><span data-stu-id="e59b9-156">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the Project Service pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="e59b9-157">至於 2 小時加班工時，則將 15% 的加成套用至基準費率 100 以取得 115 USD 的單價，並記錄 230 USD 的總成本。</span><span class="sxs-lookup"><span data-stu-id="e59b9-157">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="e59b9-158">適用於成本</span><span class="sxs-lookup"><span data-stu-id="e59b9-158">Applicable to Cost</span></span> 
<span data-ttu-id="e59b9-159">如果此選項設定為**是**，即表示擷取成本及加成費率時，應使用來自輸入內容的維度值，與**角色價格**和**角色價格加成**進行比對。</span><span class="sxs-lookup"><span data-stu-id="e59b9-159">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="e59b9-160">適用於銷售</span><span class="sxs-lookup"><span data-stu-id="e59b9-160">Applicable to Sales</span></span>
<span data-ttu-id="e59b9-161">如果此選項設定為**是**，即表示擷取帳單及加成費率時，應使用來自輸入內容的維度值，與**角色價格**和**角色價格加成**進行比對。</span><span class="sxs-lookup"><span data-stu-id="e59b9-161">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="e59b9-162">適用於購買</span><span class="sxs-lookup"><span data-stu-id="e59b9-162">Applicable to Purchase</span></span>
<span data-ttu-id="e59b9-163">如果此選項設定為**是**，即表示擷取購買價時，應使用來自輸入內容的維度值，與**角色價格**和**角色價格加成**進行比對。</span><span class="sxs-lookup"><span data-stu-id="e59b9-163">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="e59b9-164">Project Service 目前不支援轉承包案例，因此不使用此欄位。</span><span class="sxs-lookup"><span data-stu-id="e59b9-164">Currently Project Service does not support subcontracting scenarios, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="e59b9-165">優先順序</span><span class="sxs-lookup"><span data-stu-id="e59b9-165">Priority</span></span>
<span data-ttu-id="e59b9-166">設定維度優先順序可協助 Project Service 定價功能即使在輸入維度值與**角色價格**或**角色價格加成**表格中的值之間找不到完全相符的項目，也能產生價格。</span><span class="sxs-lookup"><span data-stu-id="e59b9-166">Setting the dimension priority helps Project Service pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="e59b9-167">在此案例中，Project Service 會依維度優先順序對其進行加權，並使用 null 值表示不相符的維度值。</span><span class="sxs-lookup"><span data-stu-id="e59b9-167">In this scenario, Project Service will use null values for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="e59b9-168">**成本優先順序**：依據成本價設定比對相符時，維度的成本優先順序值將指示該維度的權數。</span><span class="sxs-lookup"><span data-stu-id="e59b9-168">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="e59b9-169">**成本優先順序**值在所有**適用於成本**的維度中須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e59b9-169">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="e59b9-170">**銷售優先順序**：依據銷售價或帳單費率設定比對相符時，維度的銷售優先順序值將指示該維度的權數。</span><span class="sxs-lookup"><span data-stu-id="e59b9-170">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="e59b9-171">**銷售優先順序**值在所有**適用於銷售**的維度中須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e59b9-171">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>
