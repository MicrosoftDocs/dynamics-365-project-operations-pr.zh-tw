---
title: 專案定價
description: 本主題提供有關定價如何在 Dynamics 365 Project Service Automation 中運作的資訊。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b319f9be9fd72ac99ce6012b6baffde812e3077d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073193"
---
# <a name="project-pricing"></a><span data-ttu-id="5f9cb-103">專案定價</span><span class="sxs-lookup"><span data-stu-id="5f9cb-103">Project pricing</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5f9cb-104">Dynamics 365 Project Service Automation 可擴充 Dynamics 365 Sales 中的價目表實體。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-104">Dynamics 365 Project Service Automation extends the Price list entity in Dynamics 365 Sales.</span></span> 

## <a name="key-entities"></a><span data-ttu-id="5f9cb-105">主要實體</span><span class="sxs-lookup"><span data-stu-id="5f9cb-105">Key entities</span></span>

<span data-ttu-id="5f9cb-106">價目表包含四種不同實體所提供的資訊：</span><span class="sxs-lookup"><span data-stu-id="5f9cb-106">A price list includes information that is provided by four different entities:</span></span>

- <span data-ttu-id="5f9cb-107">**價目表** - 此實體儲存有關定價時間的內容、貨幣、日期有效性和時間單位的資訊。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-107">**Price List** - This entity stores information about context, currency, date effectivity, and time unit for pricing time.</span></span> <span data-ttu-id="5f9cb-108">內容會顯示價目表是表示成本費率還是銷售費率。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-108">Context shows whether the price list is expresses cost rates or sales rates.</span></span> 
- <span data-ttu-id="5f9cb-109">**貨幣** -此實體會在價目表上儲存價格的貨幣。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-109">**Currency** - This entity stores the currency of prices on the price list.</span></span> 
- <span data-ttu-id="5f9cb-110">**日期** - 系統會在嘗試輸入交易的預設價格時使用此實體。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-110">**Date** - This entity is used when the system tries to enter a default a price on a transaction.</span></span> <span data-ttu-id="5f9cb-111">PSA 定價會選取其有效日期包含交易日期的價目表。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-111">PSA pricing selects the price list that has date effectivity that includes the date of the transaction.</span></span> <span data-ttu-id="5f9cb-112">如果 PSA 定價發現有多個對交易日期有效的價目表附加至相關報價、合約或組織單位，則不會預設使用任何價格。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-112">If PSA pricing finds more than one price list that is effective for the transaction date is attached to the related quote, contract, or organizational unit, then no price is defaulted.</span></span> 
- <span data-ttu-id="5f9cb-113">**時間** - 此實體會儲存表示價格所指的時間單位，例如每天或每小時費率。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-113">**Time** - This entity stores the unit of time that prices are expressed for, such as daily or hourly rates.</span></span> 

<span data-ttu-id="5f9cb-114">價目表實體有三個儲存價格的相關表格：</span><span class="sxs-lookup"><span data-stu-id="5f9cb-114">The Price list entity has three related tables that store prices:</span></span>

  - <span data-ttu-id="5f9cb-115">**角色價格** - 此表格儲存角色與組織單位值的組合費率，並用於設定人力資源的角色型價格。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-115">**Role Price** - This table stores a rate for a combination of role and organizational unit values and is used to set up role-based prices for human resources.</span></span>
  - <span data-ttu-id="5f9cb-116">**交易類別價格** - 此表格依交易類別儲存價格，並用於設定費用類別價格。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-116">**Transaction Category Price** - This table stores prices by transaction category and is used to set up expense category prices.</span></span>
  - <span data-ttu-id="5f9cb-117">**價目表項目** - 此表格儲存目錄產品的價格。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-117">**Price List Items** - This table stores prices for catalog products.</span></span>

> ![使用價目表設定價格](media/basic-guide-12.png)
 
<span data-ttu-id="5f9cb-119">價目表是費率卡。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-119">The price list is a rate card.</span></span> <span data-ttu-id="5f9cb-120">費率卡是價目表實體與 [角色價格]、[交易類別價格] 及 [價目表項目] 表格中相關列的組合。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-120">A rate card is a combination of the Price List entity and related rows in the Role Price, Transaction Category Price, and Price List Items tables.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="5f9cb-121">資源角色</span><span class="sxs-lookup"><span data-stu-id="5f9cb-121">Resource roles</span></span>

<span data-ttu-id="5f9cb-122">*資源角色* 一詞是指人員必須具備才能執行專案中一組特定工作的一組技能、專長和認證。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-122">The term *resource role* refers to a set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span>

<span data-ttu-id="5f9cb-123">人力資源時間通常根據資源在特定專案上所填補的角色來報價。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-123">Human resources time is usually quoted based on the role that a resource fills on a specific project.</span></span> <span data-ttu-id="5f9cb-124">對於人工資源時間，PSA 支援根據資源角色估算成本和開單收費。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-124">For human resource time, PSA supports costing and billing that are based on resource role.</span></span> <span data-ttu-id="5f9cb-125">時間可按照 **時間** 單位群組中的任何單位來定價。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-125">Time can be priced in any unit in the **Time** unit group.</span></span>

<span data-ttu-id="5f9cb-126">安裝 PSA 時，會建立 **時間** 單位群組。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-126">The **Time** unit group is crated when PSA is installed.</span></span> <span data-ttu-id="5f9cb-127">其預設單位是 **小時** 。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-127">It has a default unit of **Hour**.</span></span> <span data-ttu-id="5f9cb-128">您無法刪除、重新命名或編輯 **時間** 單位群組的屬性或 **小時** 單位。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-128">You can't delete, rename, or edit the attributes fo teh **Time** unit group or the **Hour** unit.</span></span> <span data-ttu-id="5f9cb-129">不過，您可以將其他單位新增至 **時間** 單位群組。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-129">However, you can add other units to the **Time** unit group.</span></span> <span data-ttu-id="5f9cb-130">如果嘗試刪除 **時間** 單位群組或 **小時** 單位，您可能會在 PSA 業務規則中造成失敗。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-130">If you try to delete either the **Time** unit group or the **Hour** unit, you might cause failures in the PSA business logic.</span></span>

> ![依角色設定價格](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a><span data-ttu-id="5f9cb-132">交易類別與費用類別</span><span class="sxs-lookup"><span data-stu-id="5f9cb-132">Transaction categories and expense categories</span></span>

<span data-ttu-id="5f9cb-133">專案顧問的差旅及其他費用的開支通常可向客戶收費。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-133">Travel and other expenses that project consultants incur are usually billed to the customer.</span></span> <span data-ttu-id="5f9cb-134">PSA 支援使用價目表對費用類別進行定價。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-134">PSA supports pricing of expense categories by using price lists.</span></span> <span data-ttu-id="5f9cb-135">機票、旅館和租車是費用類別的範例。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-135">Airfare, hotel, and car rental are examples fo expense categories.</span></span> <span data-ttu-id="5f9cb-136">費用的每個價目表明細會指定特定費用類別的定價。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-136">Each price list line for expenses specifies pricing for a specific expense category.</span></span> <span data-ttu-id="5f9cb-137">對於費用類別的定價，PSA 支援下列三種定價方式：</span><span class="sxs-lookup"><span data-stu-id="5f9cb-137">For pricing of expense categories, PSA supports the following three pricing methods:</span></span>

- <span data-ttu-id="5f9cb-138">**依照成本** – 向客戶收取費用成本，不套用任何加成。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-138">**At cost** - The expense cost is billed to the customer, and no markup is applied.</span></span>
- <span data-ttu-id="5f9cb-139">**加成百分比** - 向客戶收取超過實際成本的百分比。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-139">**Markup percentage** - The percentage over the actual cost is billed to the customer.</span></span> 
- <span data-ttu-id="5f9cb-140">**單價** – 針對費用類別的每個單位來設定帳單價格。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-140">**Price per unit** - A billing price is set for each unit of the expense category.</span></span> <span data-ttu-id="5f9cb-141">向客戶收取的金額是根據顧問所報銷的費用單位數來計算。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-141">The amount that is billed ot the customer is calculated based on the number of expense units that the consultant reports.</span></span> <span data-ttu-id="5f9cb-142">里程會使用單價定價方式。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-142">Mileage uses the price-per-unit pricing method.</span></span> <span data-ttu-id="5f9cb-143">例如，里程費用類別可以設定為每天 30 美元 (USD) 或每英里 2 USD。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-143">For example, the mileage expense category can be configured for 30 US dollars (USD) per day or 2 USD per mile.</span></span> <span data-ttu-id="5f9cb-144">當顧問報銷專案上的里程時，要收取的帳單金額是根據顧問所報的英里數來計算。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-144">When a consultant reports mileage on a project, the amount to bill is calculated based on the number of miles that the consultant reported.</span></span>

> ![設定費用類別的定價](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a><span data-ttu-id="5f9cb-146">專案銷售定價和覆寫</span><span class="sxs-lookup"><span data-stu-id="5f9cb-146">Project sales pricing and overrides</span></span>

<span data-ttu-id="5f9cb-147">對於專案報價和合約，專案價目表的價格覆寫模式與產品價目表的不同。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-147">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="5f9cb-148">在產品類別目錄型報價明細上，您可以直接在報價明細上覆寫角色和類別的價格，因為每個報價明細都只指向一個目錄項目。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-148">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="5f9cb-149">不過，在專案型報價明細上，您無法直接在報價明細上覆寫角色和類別的價格。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-149">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="5f9cb-150">為了支援兩種不同的覆寫模式，PSA 引進了新的價目表關聯，即專案價目表。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-150">To support the two distinct override patterns, PSA has introduced a new price list association, the project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="5f9cb-151">建議您讓專案資源和目錄項目使用不同的價目表，因為覆寫定價時，兩者之間的行為有差異。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-151">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="5f9cb-152">下列每個實體都可以有一個或多個用於專案定價的相關聯銷售價目表：</span><span class="sxs-lookup"><span data-stu-id="5f9cb-152">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="5f9cb-153">客戶 (帳戶)</span><span class="sxs-lookup"><span data-stu-id="5f9cb-153">Customer (account)</span></span> 
- <span data-ttu-id="5f9cb-154">商機</span><span class="sxs-lookup"><span data-stu-id="5f9cb-154">Opportunity</span></span> 
- <span data-ttu-id="5f9cb-155">報價</span><span class="sxs-lookup"><span data-stu-id="5f9cb-155">Quote</span></span> 
- <span data-ttu-id="5f9cb-156">專案合約</span><span class="sxs-lookup"><span data-stu-id="5f9cb-156">Project Contract</span></span>

<span data-ttu-id="5f9cb-157">這些實體與價目表的關聯是透過專案價目表來表示。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-157">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="5f9cb-158">您可以將一個或多個價目表與客戶、商機、報價及專案合約銷售實體建立關聯。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-158">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="5f9cb-159">系統不會自動在客戶記錄上輸入預設專案價目表。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-159">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="5f9cb-160">不過，您可以手動將專案價目表附加至客戶記錄。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-160">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="5f9cb-161">然而，只有在與客戶之間存在自訂定價合約時，您才應該手動附加專案價目表。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-161">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="5f9cb-162">將專案價目表附加至銷售實體時，PSA 會驗證下列資訊：</span><span class="sxs-lookup"><span data-stu-id="5f9cb-162">When a project price list is attached to a sales entity, PSA validates the following information:</span></span>

- <span data-ttu-id="5f9cb-163">價目表的內容與 **銷售** 有關。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-163">The price list las a context of **Sales**.</span></span> 
- <span data-ttu-id="5f9cb-164">價目表貨幣與客戶貨幣相符。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-164">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="5f9cb-165">在專案合約上，PSA 使用下列優先權順序自動設定相關的專案價格清單：</span><span class="sxs-lookup"><span data-stu-id="5f9cb-165">On a project contract, PSA uses the following order of precedence to automatically set related project price lists:</span></span>

1. <span data-ttu-id="5f9cb-166">報價</span><span class="sxs-lookup"><span data-stu-id="5f9cb-166">Quote</span></span>
2. <span data-ttu-id="5f9cb-167">商機</span><span class="sxs-lookup"><span data-stu-id="5f9cb-167">Opportunity</span></span>
3. <span data-ttu-id="5f9cb-168">客戶</span><span class="sxs-lookup"><span data-stu-id="5f9cb-168">Customer</span></span> 
4. <span data-ttu-id="5f9cb-169">PSA 的全域設定</span><span class="sxs-lookup"><span data-stu-id="5f9cb-169">Global settings for PSA</span></span>

<span data-ttu-id="5f9cb-170">預設會輸入專案價目表時，PSA 會驗證貨幣是否與客戶貨幣相符，以及已輸入的預設價目表是否有 **銷售** 的內容。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-170">When a project price list is entered by default, PSA validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="5f9cb-171">您可以將或多個專案價目表與客戶、商機、報價及專案合約銷售實體建立關聯。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-171">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="5f9cb-172">此功能支援長期專案合約的日期特定預設價格，您可能需要多個價目表來處理因通貨膨脹而進行的價格更新。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-172">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="5f9cb-173">不過，如果與客戶、商機、報價或專案合約實體建立關聯的價目表有重疊的有效日期範圍，則預設價格可能不正確。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-173">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="5f9cb-174">因此，您必須確保有效日期範圍重疊的專案價目表未與這些實體相關聯。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-174">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>

### <a name="deal-specific-price-overrides"></a><span data-ttu-id="5f9cb-175">交易特定價格覆寫</span><span class="sxs-lookup"><span data-stu-id="5f9cb-175">Deal-specific price overrides</span></span>

<span data-ttu-id="5f9cb-176">在 PSA 中，您可以為在報價或專案合約上預設輸入的專案價目表建立交易特定覆寫。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-176">In PSA, you can create deal-specific overrides for selected prices on project price lists that are entered by default on a quote or project contract.</span></span>

<span data-ttu-id="5f9cb-177">專案合約預設一律要取得主要銷售價目表的複本，而不是與該價格直接連結。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-177">By default, a project contract always gets a copy of the master sales price list instead of a direct link to it.</span></span> <span data-ttu-id="5f9cb-178">此行為有助於保證即使主要價目表變更時，針對工作說明書 (SOW) 與客戶達成的價格協議也不會變更。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-178">This behavior helps guarantee that price agreements that are made iwth a customer for a statement of work (SOW) don't change if the master price list is changed.</span></span>

<span data-ttu-id="5f9cb-179">不過，在報價上，您可以使用主要價目表。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-179">However, on a quote, you can use a master price list.</span></span> <span data-ttu-id="5f9cb-180">或者，也可以複製主要價目表後再進行編輯，以建立只適用於該報價的自訂價目表。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-180">Alternatively, you can copy a master price list and edit it to create a custom price list that applies only to that quote.</span></span> <span data-ttu-id="5f9cb-181">若要建立專屬於報價的新價目表，請在 **報價** 頁面上選取 **建立自訂定價** 。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-181">To create a new price list that is specific to a quote, on the **Quote** page, select **Create custom pricing**.</span></span> <span data-ttu-id="5f9cb-182">您只能從報價存取交易特定的專案價目表。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-182">You can access the deal-specific project price list only from the quote.</span></span> 

<span data-ttu-id="5f9cb-183">當您建立自訂專案價目表時，只會複製價目表的專案元件。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-183">When you create a custom project price list, only the project components of the price list are copied.</span></span> <span data-ttu-id="5f9cb-184">換句話說，新價目表已建立為報價上所附加現有專案價目表的複本，而這個新的價目表只有相關的角色價格和交易類別價格</span><span class="sxs-lookup"><span data-stu-id="5f9cb-184">In other words, a new price list created as a copy of the existing project price list that is attached on the quote, and this new price list has only related role prices and transaction category prices.</span></span>

> ![檢視和設定專案合約的自訂定價](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a><span data-ttu-id="5f9cb-186">追蹤成本</span><span class="sxs-lookup"><span data-stu-id="5f9cb-186">Tracking costs</span></span>

<span data-ttu-id="5f9cb-187">PSA 會追蹤專案的人力資源時間使用成本。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-187">PSA tracks costs for the use of human resource time on projects.</span></span> <span data-ttu-id="5f9cb-188">還會追蹤專案期間產生的其他費用成本，例如差旅費。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-188">It also tracks costs for other expenses that are incurrred during hte project, such as travel expenses.</span></span>

<span data-ttu-id="5f9cb-189">與帳單費率一樣，人力資源也會使用價目表來設定。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-189">Like bill rates, cost rates for human resources are also set up using price lists.</span></span> <span data-ttu-id="5f9cb-190">以下是成本價目表和銷售價目表在行為上的主要區別：</span><span class="sxs-lookup"><span data-stu-id="5f9cb-190">Here are the main differences in the behavior of the cost price list and sales price list:</span></span>

- <span data-ttu-id="5f9cb-191">資源的成本費率在特定專案、合約或報價上無法被覆寫。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-191">The cost rate of a resource can’t be overridden on a specific project, contract, or quote.</span></span> <span data-ttu-id="5f9cb-192">不過，如果所做變更是交易性質所特有，則可以在每次交易時覆寫帳單比率。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-192">However, bill rates can be overridden on a per-deal basis if changes are made that are specific to the nature of the deal.</span></span> 

- <span data-ttu-id="5f9cb-193">以下順序會用來解析成本價目表：</span><span class="sxs-lookup"><span data-stu-id="5f9cb-193">The following order is used to resolve a cost price list:</span></span>

    1. <span data-ttu-id="5f9cb-194">附加至組織單位的成本價目表。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-194">The cost price list that is attached to the organizational unit.</span></span>
    2. <span data-ttu-id="5f9cb-195">附加至 Project Service 參數 的成本價目表。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-195">The cost price list that is attached to the project service parameters.</span></span> <span data-ttu-id="5f9cb-196">因為可以將使用許多不同貨幣的成本價目表附加至 Project Service 參數，PSA 會在專案、合約或報價的承包組織單位貨幣與成本價目表的貨幣之間進行貨幣比較。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-196">Because cost price lists in many different currencies can be attached to project service parameters, PSA does a currency match between the currency of the contracting organizational unit of the project, contract, or quote, and the currency of the cost price list.</span></span>
    3. <span data-ttu-id="5f9cb-197">如果是費用，則依照成本和成本加成定價方式不適用於成本價目表。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-197">For expenses, the at-cost and markup-over-cost pricing methods don’t apply to cost price lists.</span></span> <span data-ttu-id="5f9cb-198">即使這些定價方式是在成本價目表明細上用來設定交易類別成本，系統還是會予以忽略，而不會輸入預設成本價。</span><span class="sxs-lookup"><span data-stu-id="5f9cb-198">Even if these pricing methods are used on cost price list lines to set up transaction category costs, the system ignores them, and no default cost price is entered.</span></span>
