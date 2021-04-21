---
title: 產品價目表
description: 本主題提供有關專案報價及合約所用類別目錄定價中的價目表的資訊。
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877480"
---
# <a name="product-price-lists"></a><span data-ttu-id="6d642-103">產品價目表</span><span class="sxs-lookup"><span data-stu-id="6d642-103">Product price lists</span></span>

<span data-ttu-id="6d642-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="6d642-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="6d642-105">在 Project Operations 中，**產品價目表** 和相關價目表項目實體支援為產品型報價明細及合約服務內容中產品定價的功能。</span><span class="sxs-lookup"><span data-stu-id="6d642-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="6d642-106">對於專案中使用的產品，會使用專案價目表的價目表項目記錄。</span><span class="sxs-lookup"><span data-stu-id="6d642-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="6d642-107">必須設定產品，讓這些產品在產品類別目錄中有預設成本和價目表。</span><span class="sxs-lookup"><span data-stu-id="6d642-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="6d642-108">使用定價、標準成本和目前成本來設定預設成本與定價。</span><span class="sxs-lookup"><span data-stu-id="6d642-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="6d642-109">只有當系統在報價或專案合約的產品價目表中找不到該產品的價目表明細時，才會在報價明細或專案合約服務內容上使用預設定價。</span><span class="sxs-lookup"><span data-stu-id="6d642-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="6d642-110">您可以在報價之間變更產品類別目錄明細的成本價。</span><span class="sxs-lookup"><span data-stu-id="6d642-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="6d642-111">這項功能很重要，因為如果您沒有準確追蹤成本，就無法判斷專案業務開發的營運利潤。</span><span class="sxs-lookup"><span data-stu-id="6d642-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="6d642-112">預設會使用產品的標準成本做為成本價。</span><span class="sxs-lookup"><span data-stu-id="6d642-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="6d642-113">不過，如果該報價有不同的成本價，則可以在報價明細上更新預設成本價。</span><span class="sxs-lookup"><span data-stu-id="6d642-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="6d642-114">價目表項目</span><span class="sxs-lookup"><span data-stu-id="6d642-114">Price list items</span></span>

<span data-ttu-id="6d642-115">您可以將產品類別目錄中的產品新增至不同的價目表。</span><span class="sxs-lookup"><span data-stu-id="6d642-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="6d642-116">產品的價目表明細一律參照特定單位。</span><span class="sxs-lookup"><span data-stu-id="6d642-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="6d642-117">價目表項目中的產品定價可以設定為貨幣金額。</span><span class="sxs-lookup"><span data-stu-id="6d642-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="6d642-118">或者，也可以設定為定價、目前成本或標準成本的函數。</span><span class="sxs-lookup"><span data-stu-id="6d642-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="6d642-119">當產品價格設定為定價、標準成本或目前成本的函數時，定價功能支援各種不同的舍入選項。</span><span class="sxs-lookup"><span data-stu-id="6d642-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="6d642-120">除了利用多個定價方式和舍入選項之外，您還可以將折扣清單與價目表項目建立關聯。</span><span class="sxs-lookup"><span data-stu-id="6d642-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="6d642-121">預設產品價目表</span><span class="sxs-lookup"><span data-stu-id="6d642-121">Default product price list</span></span>
<span data-ttu-id="6d642-122">每個客戶記錄都有一個 **預設價目表** 欄位，您可以在其中指定符合客戶貨幣的價目表。</span><span class="sxs-lookup"><span data-stu-id="6d642-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="6d642-123">此欄位不會自動輸入預設值。</span><span class="sxs-lookup"><span data-stu-id="6d642-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="6d642-124">當有特定客戶的自訂定價合約存在時，您可以使用此欄位，將價目表與該客戶產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6d642-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="6d642-125">商機、報價和專案合約實體會使用下列順序來輸入預設產品價格清單。</span><span class="sxs-lookup"><span data-stu-id="6d642-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="6d642-126">專案價目表也使用相同的順序。</span><span class="sxs-lookup"><span data-stu-id="6d642-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="6d642-127">報價</span><span class="sxs-lookup"><span data-stu-id="6d642-127">Quote</span></span>
2.  <span data-ttu-id="6d642-128">商機​​</span><span class="sxs-lookup"><span data-stu-id="6d642-128">Opportunity</span></span>
3.  <span data-ttu-id="6d642-129">客戶</span><span class="sxs-lookup"><span data-stu-id="6d642-129">Customer</span></span>
4.  <span data-ttu-id="6d642-130">全域設定</span><span class="sxs-lookup"><span data-stu-id="6d642-130">Global settings</span></span> 

<span data-ttu-id="6d642-131">根據預設，報價明細上的 **產品** 欄位會列出報價的產品價目表中所有的使用中產品。</span><span class="sxs-lookup"><span data-stu-id="6d642-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="6d642-132">如果產品已停用，或此產品為草稿產品，則即使位在價目表中，也不會將其列出。</span><span class="sxs-lookup"><span data-stu-id="6d642-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="6d642-133">產品類別目錄明細會新增為專案合約所建立之第一張發票上的發票明細。</span><span class="sxs-lookup"><span data-stu-id="6d642-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="6d642-134">在草稿發票上，您可以刪除這些發票明細。</span><span class="sxs-lookup"><span data-stu-id="6d642-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="6d642-135">在此情況下，這些明細將會出現在後續發票上，直到已開立發票，或發票已傳送給客戶為止。</span><span class="sxs-lookup"><span data-stu-id="6d642-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="6d642-136">您無法為產品發票明細的部分數量開立發票。</span><span class="sxs-lookup"><span data-stu-id="6d642-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="6d642-137">當專案合約中的產品明細已開票時，就會建立實際值。</span><span class="sxs-lookup"><span data-stu-id="6d642-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="6d642-138">但是，這些實際值並不會連結至相關的專案實體。</span><span class="sxs-lookup"><span data-stu-id="6d642-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="6d642-139">換言之，產品型專案合約服務內容與任何專案型使用方式無關</span><span class="sxs-lookup"><span data-stu-id="6d642-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
