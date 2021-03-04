---
title: 產品類別目錄定價
description: 此主題提供有關產品類別目錄定價如何在 Dynamics 365 Project Service Automation (PSA) 中運作的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 3fb9b51d58cbe3b0db6dad902461b90ac04cc42f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151198"
---
# <a name="product-catalog-pricing"></a><span data-ttu-id="6fb67-103">產品類別目錄定價</span><span class="sxs-lookup"><span data-stu-id="6fb67-103">Product catalog pricing</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="6fb67-104">價目表和價目表項目實體支援產品類別目錄定價。</span><span class="sxs-lookup"><span data-stu-id="6fb67-104">Price lists and price list item entities support product catalog pricing.</span></span> <span data-ttu-id="6fb67-105">最重要的是，此功能用於專案報價和專案合約上的目錄型明細。</span><span class="sxs-lookup"><span data-stu-id="6fb67-105">For the most part, this functionality is used for catalog-based lines on project quotes and project contracts.</span></span>

<span data-ttu-id="6fb67-106">對於專案型明細，合約代表成交後贏得的交易。</span><span class="sxs-lookup"><span data-stu-id="6fb67-106">For project-based lines, a contract represents the deal after it was won.</span></span> <span data-ttu-id="6fb67-107">協商程序通常在成交之前進行，因此附加至報價的定價一律會原樣複製到新的價目表，並附加至合約。</span><span class="sxs-lookup"><span data-stu-id="6fb67-107">Because the process of negotiation usually precedes the win, the pricing that is attached to the quote is always copied as-is to a new price list and attached to the contract.</span></span> <span data-ttu-id="6fb67-108">這份新的價目表無法在合約範圍之外變更。</span><span class="sxs-lookup"><span data-stu-id="6fb67-108">This new price list can't be changed outside the scope of the contract.</span></span> <span data-ttu-id="6fb67-109">這項限制可協助保護議定的費率卡，避免任何在主要價目表中發生的價格變更。</span><span class="sxs-lookup"><span data-stu-id="6fb67-109">This limitation helps protect the rate card that was negotiated from any price changes that occur in the master price list.</span></span>

<span data-ttu-id="6fb67-110">必須設定產品，讓這些產品在產品類別目錄中有預設成本和價目表。</span><span class="sxs-lookup"><span data-stu-id="6fb67-110">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="6fb67-111">您必須使用定價、標準成本和目前成本來設定預設成本與定價。</span><span class="sxs-lookup"><span data-stu-id="6fb67-111">You must use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="6fb67-112">只有當系統在報價或專案合約的產品價目表中找不到該產品的價目表明細時，才會在報價明細或專案合約服務內容上使用預設定價。</span><span class="sxs-lookup"><span data-stu-id="6fb67-112">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="6fb67-113">您可以在報價之間變更產品類別目錄明細的成本價。</span><span class="sxs-lookup"><span data-stu-id="6fb67-113">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="6fb67-114">這項功能很重要，因為如果您沒有準確追蹤成本，就無法判斷專案業務開發的營運利潤。</span><span class="sxs-lookup"><span data-stu-id="6fb67-114">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="6fb67-115">預設會使用產品的標準成本做為成本價。</span><span class="sxs-lookup"><span data-stu-id="6fb67-115">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="6fb67-116">不過，如果該報價有不同的成本價，則可以在報價明細上更新預設成本價。</span><span class="sxs-lookup"><span data-stu-id="6fb67-116">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="6fb67-117">價目表項目</span><span class="sxs-lookup"><span data-stu-id="6fb67-117">Price list items</span></span>

<span data-ttu-id="6fb67-118">您可以將產品類別目錄中的產品新增至不同的價目表。</span><span class="sxs-lookup"><span data-stu-id="6fb67-118">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="6fb67-119">產品的價目表明細一律參照特定單位。</span><span class="sxs-lookup"><span data-stu-id="6fb67-119">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="6fb67-120">價目表項目中的產品定價可以設定為貨幣金額。</span><span class="sxs-lookup"><span data-stu-id="6fb67-120">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="6fb67-121">或者，也可以設定為定價、目前成本或標準成本的函數。</span><span class="sxs-lookup"><span data-stu-id="6fb67-121">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="6fb67-122">當價格設定為定價、標準成本或目前成本的函數時，PSA 支援各種不同的舍入選項。</span><span class="sxs-lookup"><span data-stu-id="6fb67-122">PSA supports various rounding options when prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="6fb67-123">除了利用多個定價方式和舍入選項之外，您還可以將折扣清單與價目表項目建立關聯。</span><span class="sxs-lookup"><span data-stu-id="6fb67-123">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

> ![將類別目錄中的產品新增至不同的價目表](media/basic-guide-16.png)

<span data-ttu-id="6fb67-125">選取 **專案報價** 頁面上的 **建立自訂定價** 以建立報價的新自訂價目表時，PSA 會製作價目表的複本，而新價目表標頭上的 **實體** 欄位會設定為 **銷售實體**。</span><span class="sxs-lookup"><span data-stu-id="6fb67-125">When you create a new custom price list for a quote by selecting **Create Custom Pricing** on the **Project Quote** page, PSA makes a copy of the price list, and the **Entity** field on the header of the new price list is set to **Sales Entity**.</span></span> <span data-ttu-id="6fb67-126">新價目表的名稱會附加在報價名稱和時間戳記的後面。</span><span class="sxs-lookup"><span data-stu-id="6fb67-126">The name of the new price list is appended with the name of the quote and a timestamp.</span></span> <span data-ttu-id="6fb67-127">您也可以在自訂工作流程中使用新價目表名稱和報價名稱，以觸發對使用自訂定價之報價的其他檢閱和核准。</span><span class="sxs-lookup"><span data-stu-id="6fb67-127">You also can use the name of the new price list and the name of the quote in custom workflows to trigger additional review and approvals for quotes that use custom pricing.</span></span>

 
## <a name="default-product-price-list"></a><span data-ttu-id="6fb67-128">預設產品價目表</span><span class="sxs-lookup"><span data-stu-id="6fb67-128">Default product price list</span></span>
<span data-ttu-id="6fb67-129">每個客戶記錄都有一個 **預設價目表** 欄位，您可以在其中指定符合客戶貨幣的價目表。</span><span class="sxs-lookup"><span data-stu-id="6fb67-129">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="6fb67-130">在 PSA 中，不會自動在此欄位中輸入預設值。</span><span class="sxs-lookup"><span data-stu-id="6fb67-130">In PSA, a default value isn't automatically entered in this field.</span></span> <span data-ttu-id="6fb67-131">當有特定客戶的自訂定價合約存在時，您可以使用此欄位，將價目表與該客戶產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6fb67-131">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="6fb67-132">商機、報價和專案合約實體會使用下列順序來輸入預設產品價格清單。</span><span class="sxs-lookup"><span data-stu-id="6fb67-132">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="6fb67-133">專案價目表也使用相同的順序。</span><span class="sxs-lookup"><span data-stu-id="6fb67-133">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="6fb67-134">報價</span><span class="sxs-lookup"><span data-stu-id="6fb67-134">Quote</span></span>
2.  <span data-ttu-id="6fb67-135">商機</span><span class="sxs-lookup"><span data-stu-id="6fb67-135">Opportunity</span></span>
3.  <span data-ttu-id="6fb67-136">客戶</span><span class="sxs-lookup"><span data-stu-id="6fb67-136">Customer</span></span>
4.  <span data-ttu-id="6fb67-137">PSA 的全域設定</span><span class="sxs-lookup"><span data-stu-id="6fb67-137">Global settings for PSA</span></span>

<span data-ttu-id="6fb67-138">根據預設，報價明細上的 **產品** 欄位會列出報價的產品價目表中所有的使用中產品。</span><span class="sxs-lookup"><span data-stu-id="6fb67-138">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="6fb67-139">如果產品已停用，或此產品為草稿產品，則即使位在價目表中，也不會將其列出。</span><span class="sxs-lookup"><span data-stu-id="6fb67-139">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="6fb67-140">產品類別目錄明細會新增為專案合約所建立之第一張發票上的發票明細。</span><span class="sxs-lookup"><span data-stu-id="6fb67-140">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="6fb67-141">在草稿發票上，您可以刪除這些發票明細。</span><span class="sxs-lookup"><span data-stu-id="6fb67-141">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="6fb67-142">在此情況下，這些明細將會出現在後續發票上，直到已開立發票，或發票已傳送給客戶為止。</span><span class="sxs-lookup"><span data-stu-id="6fb67-142">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="6fb67-143">在 PSA 中，您無法為產品發票明細的部分數量開立發票。</span><span class="sxs-lookup"><span data-stu-id="6fb67-143">In PSA, you can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="6fb67-144">當專案合約中的產品明細已開票時，就會建立實際值。</span><span class="sxs-lookup"><span data-stu-id="6fb67-144">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="6fb67-145">但是，這些實際值並不會連結至相關的專案實體。</span><span class="sxs-lookup"><span data-stu-id="6fb67-145">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="6fb67-146">換言之，產品型專案合約服務內容與任何專案型使用方式無關</span><span class="sxs-lookup"><span data-stu-id="6fb67-146">In other words, product-based project contract lines are independent of any project-based use.</span></span> <span data-ttu-id="6fb67-147">PSA 不會追蹤專案的材料耗用量。</span><span class="sxs-lookup"><span data-stu-id="6fb67-147">PSA doesn't track material consumption on projects.</span></span>
