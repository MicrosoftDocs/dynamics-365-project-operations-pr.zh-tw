---
title: 產品價目表
description: 本主題提供有關專案報價及合約所用類別目錄定價中的價目表的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3570aeb78804e9b267caa55a27e02d6c8df9a5c6
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898161"
---
# <a name="product-price-lists"></a><span data-ttu-id="6df7a-103">產品價目表</span><span class="sxs-lookup"><span data-stu-id="6df7a-103">Product price lists</span></span>

<span data-ttu-id="6df7a-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="6df7a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6df7a-105">價目表和價目表項目實體支援產品類別目錄定價。</span><span class="sxs-lookup"><span data-stu-id="6df7a-105">Price lists and price list item entities support product catalog pricing.</span></span> <span data-ttu-id="6df7a-106">最重要的是，此功能用於專案報價和專案合約上的目錄型明細。</span><span class="sxs-lookup"><span data-stu-id="6df7a-106">For the most part, this functionality is used for catalog-based lines on project quotes and project contracts.</span></span>

<span data-ttu-id="6df7a-107">對於專案型明細，合約代表成交後贏得的交易。</span><span class="sxs-lookup"><span data-stu-id="6df7a-107">For project-based lines, a contract represents the deal after it was won.</span></span> <span data-ttu-id="6df7a-108">協商程序通常在成交之前進行，因此附加至報價的定價一律會原樣複製到新的價目表，並附加至合約。</span><span class="sxs-lookup"><span data-stu-id="6df7a-108">Because the process of negotiation usually precedes the win, the pricing that is attached to the quote is always copied as-is to a new price list and attached to the contract.</span></span> <span data-ttu-id="6df7a-109">這份新的價目表無法在合約範圍之外變更。</span><span class="sxs-lookup"><span data-stu-id="6df7a-109">This new price list can't be changed outside the scope of the contract.</span></span> <span data-ttu-id="6df7a-110">這項限制可協助保護議定的費率卡，避免任何在主要價目表中發生的價格變更。</span><span class="sxs-lookup"><span data-stu-id="6df7a-110">This limitation helps protect the rate card that was negotiated from any price changes that occur in the master price list.</span></span>

<span data-ttu-id="6df7a-111">必須設定產品，讓這些產品在產品類別目錄中有預設成本和價目表。</span><span class="sxs-lookup"><span data-stu-id="6df7a-111">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="6df7a-112">使用定價、標準成本和目前成本來設定預設成本與定價。</span><span class="sxs-lookup"><span data-stu-id="6df7a-112">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="6df7a-113">只有當系統在報價或專案合約的產品價目表中找不到該產品的價目表明細時，才會在報價明細或專案合約服務內容上使用預設定價。</span><span class="sxs-lookup"><span data-stu-id="6df7a-113">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="6df7a-114">您可以在報價之間變更產品類別目錄明細的成本價。</span><span class="sxs-lookup"><span data-stu-id="6df7a-114">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="6df7a-115">這項功能很重要，因為如果您沒有準確追蹤成本，就無法判斷專案業務開發的營運利潤。</span><span class="sxs-lookup"><span data-stu-id="6df7a-115">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="6df7a-116">預設會使用產品的標準成本做為成本價。</span><span class="sxs-lookup"><span data-stu-id="6df7a-116">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="6df7a-117">不過，如果該報價有不同的成本價，則可以在報價明細上更新預設成本價。</span><span class="sxs-lookup"><span data-stu-id="6df7a-117">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="6df7a-118">價目表項目</span><span class="sxs-lookup"><span data-stu-id="6df7a-118">Price list items</span></span>

<span data-ttu-id="6df7a-119">您可以將產品類別目錄中的產品新增至不同的價目表。</span><span class="sxs-lookup"><span data-stu-id="6df7a-119">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="6df7a-120">產品的價目表明細一律參照特定單位。</span><span class="sxs-lookup"><span data-stu-id="6df7a-120">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="6df7a-121">價目表項目中的產品定價可以設定為貨幣金額。</span><span class="sxs-lookup"><span data-stu-id="6df7a-121">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="6df7a-122">或者，也可以設定為定價、目前成本或標準成本的函數。</span><span class="sxs-lookup"><span data-stu-id="6df7a-122">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="6df7a-123">當價格設定為定價、標準成本或目前成本的函數時，PSA 支援各種不同的舍入選項。</span><span class="sxs-lookup"><span data-stu-id="6df7a-123">PSA supports various rounding options when prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="6df7a-124">除了利用多個定價方式和舍入選項之外，您還可以將折扣清單與價目表項目建立關聯。</span><span class="sxs-lookup"><span data-stu-id="6df7a-124">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

<span data-ttu-id="6df7a-125">選取**專案報價**頁面上的**建立自訂定價**以建立報價的新自訂價目表時，系統會建立價目表的複本，並將新價目表標題中的**實體**欄位設定為**銷售實體**。</span><span class="sxs-lookup"><span data-stu-id="6df7a-125">When you create a new custom price list for a quote by selecting **Create Custom Pricing** on the **Project Quote** page, a copy of the price list is made, and the **Entity** field on the header of the new price list is set to **Sales Entity**.</span></span> <span data-ttu-id="6df7a-126">新價目表的名稱會附加在報價名稱和時間戳記的後面。</span><span class="sxs-lookup"><span data-stu-id="6df7a-126">The name of the new price list is appended with the name of the quote and a timestamp.</span></span> <span data-ttu-id="6df7a-127">您也可以在自訂工作流程中使用新價目表名稱和報價名稱，以觸發對使用自訂定價之報價的其他檢閱和核准。</span><span class="sxs-lookup"><span data-stu-id="6df7a-127">You also can use the name of the new price list and the name of the quote in custom workflows to trigger additional review and approvals for quotes that use custom pricing.</span></span>

 
## <a name="default-product-price-list"></a><span data-ttu-id="6df7a-128">預設產品價目表</span><span class="sxs-lookup"><span data-stu-id="6df7a-128">Default product price list</span></span>
<span data-ttu-id="6df7a-129">每個客戶記錄都有一個**預設價目表**欄位，您可以在其中指定符合客戶貨幣的價目表。</span><span class="sxs-lookup"><span data-stu-id="6df7a-129">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="6df7a-130">此欄位不會自動輸入預設值。</span><span class="sxs-lookup"><span data-stu-id="6df7a-130">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="6df7a-131">當有特定客戶的自訂定價合約存在時，您可以使用此欄位，將價目表與該客戶產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6df7a-131">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="6df7a-132">商機、報價和專案合約實體會使用下列順序來輸入預設產品價格清單。</span><span class="sxs-lookup"><span data-stu-id="6df7a-132">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="6df7a-133">專案價目表也使用相同的順序。</span><span class="sxs-lookup"><span data-stu-id="6df7a-133">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="6df7a-134">報價</span><span class="sxs-lookup"><span data-stu-id="6df7a-134">Quote</span></span>
2.  <span data-ttu-id="6df7a-135">商機​​</span><span class="sxs-lookup"><span data-stu-id="6df7a-135">Opportunity</span></span>
3.  <span data-ttu-id="6df7a-136">客戶</span><span class="sxs-lookup"><span data-stu-id="6df7a-136">Customer</span></span>
4.  <span data-ttu-id="6df7a-137">全域設定</span><span class="sxs-lookup"><span data-stu-id="6df7a-137">Global settings</span></span> 

<span data-ttu-id="6df7a-138">根據預設，報價明細上的**產品**欄位會列出報價的產品價目表中所有的使用中產品。</span><span class="sxs-lookup"><span data-stu-id="6df7a-138">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="6df7a-139">如果產品已停用，或此產品為草稿產品，則即使位在價目表中，也不會將其列出。</span><span class="sxs-lookup"><span data-stu-id="6df7a-139">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="6df7a-140">產品類別目錄明細會新增為專案合約所建立之第一張發票上的發票明細。</span><span class="sxs-lookup"><span data-stu-id="6df7a-140">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="6df7a-141">在草稿發票上，您可以刪除這些發票明細。</span><span class="sxs-lookup"><span data-stu-id="6df7a-141">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="6df7a-142">在此情況下，這些明細將會出現在後續發票上，直到已開立發票，或發票已傳送給客戶為止。</span><span class="sxs-lookup"><span data-stu-id="6df7a-142">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="6df7a-143">您無法為產品發票明細的部分數量開立發票。</span><span class="sxs-lookup"><span data-stu-id="6df7a-143">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="6df7a-144">當專案合約中的產品明細已開票時，就會建立實際值。</span><span class="sxs-lookup"><span data-stu-id="6df7a-144">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="6df7a-145">但是，這些實際值並不會連結至相關的專案實體。</span><span class="sxs-lookup"><span data-stu-id="6df7a-145">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="6df7a-146">換言之，產品型專案合約服務內容與任何專案型使用方式無關</span><span class="sxs-lookup"><span data-stu-id="6df7a-146">In other words, product-based project contract lines are independent of any project-based use.</span></span> <span data-ttu-id="6df7a-147">不會追蹤專案的材料耗用量。</span><span class="sxs-lookup"><span data-stu-id="6df7a-147">Material consumption on projects isn't tracked.</span></span>
