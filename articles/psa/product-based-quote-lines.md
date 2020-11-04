---
title: 產品型報價明細
description: 此主題提供有關產品型報價明細的資訊。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: 55a5b5041a494892e6d96bf24e1bc132a26521dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073176"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="65d05-103">產品型報價明細</span><span class="sxs-lookup"><span data-stu-id="65d05-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="65d05-104">您可以在 Dynamics 365 Project Service Automation 中建立產品型報價明細。</span><span class="sxs-lookup"><span data-stu-id="65d05-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="65d05-105">產品型報價明細可以是「目錄外項目」明細，也可以是產品類別目錄中的項目。</span><span class="sxs-lookup"><span data-stu-id="65d05-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="65d05-106">產品類別目錄</span><span class="sxs-lookup"><span data-stu-id="65d05-106">Product catalog</span></span>

<span data-ttu-id="65d05-107">Dynamics 365 產品類別目錄中的產品有預設單位與單位群組。</span><span class="sxs-lookup"><span data-stu-id="65d05-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="65d05-108">如果有數種產品共用同一組屬性，您可以建立同樣有這些屬性的產品系列。</span><span class="sxs-lookup"><span data-stu-id="65d05-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="65d05-109">一個產品系列中所有的產品都會繼承同一組屬性。</span><span class="sxs-lookup"><span data-stu-id="65d05-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="65d05-110">例如，公司銷售各種軟體的訂閱授權。</span><span class="sxs-lookup"><span data-stu-id="65d05-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="65d05-111">所有訂閱軟體都有下列兩個屬性：</span><span class="sxs-lookup"><span data-stu-id="65d05-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="65d05-112">使用者數目</span><span class="sxs-lookup"><span data-stu-id="65d05-112">Number of users</span></span> 
- <span data-ttu-id="65d05-113">訂閱期間 (以月為單位)</span><span class="sxs-lookup"><span data-stu-id="65d05-113">Subscription duration (in months)</span></span>

<span data-ttu-id="65d05-114">維護這種目錄類型的好方法是建立名為 **訂閱軟體** ，且有 **使用者數目** 和 **訂閱期間** 做為屬性的產品系列。</span><span class="sxs-lookup"><span data-stu-id="65d05-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software** , and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="65d05-115">然後，您可以將個別產品 (例如 **Dynamics 365 Sales** 或 **Dynamics 365 Field Service** ) 新增至 **訂閱軟體** 產品系列。</span><span class="sxs-lookup"><span data-stu-id="65d05-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="65d05-116">將產品類別目錄專案新增至專案報價</span><span class="sxs-lookup"><span data-stu-id="65d05-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="65d05-117">專案報價與專案合約頁面有兩種類型的明細區段：專案型和產品型明細。</span><span class="sxs-lookup"><span data-stu-id="65d05-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="65d05-118">對於產品型明細，使用 Dynamics 365 將項目從產品類別目錄新增至報價。</span><span class="sxs-lookup"><span data-stu-id="65d05-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="65d05-119">報價明細或專案合約服務內容的下拉式清單，包含附加至報價或專案合約之產品價目表中的所有產品和單位。</span><span class="sxs-lookup"><span data-stu-id="65d05-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="65d05-120">您也可以新增不屬於報價之產品價目表的產品。</span><span class="sxs-lookup"><span data-stu-id="65d05-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="65d05-121">此外，您還可以從其他價目表選取產品，或者直接從產品類別目錄選取產品。</span><span class="sxs-lookup"><span data-stu-id="65d05-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="65d05-122">直接從產品類別目錄選取產品時，會使用該產品的預設價目表來取得產品的銷售價格。</span><span class="sxs-lookup"><span data-stu-id="65d05-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="65d05-123">如果未設定預設價目表，價格會設定為 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="65d05-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="65d05-124">如果報價明細是根據產品類別目錄所建立，您可以直接在報價明細上覆寫銷售價格。</span><span class="sxs-lookup"><span data-stu-id="65d05-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="65d05-125">請注意，Dynamics 365 中的報價明細有 **定價** 欄位。</span><span class="sxs-lookup"><span data-stu-id="65d05-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="65d05-126">有兩個值可用：</span><span class="sxs-lookup"><span data-stu-id="65d05-126">Two values are available:</span></span>

- <span data-ttu-id="65d05-127">自訂定價</span><span class="sxs-lookup"><span data-stu-id="65d05-127">Override pricing</span></span>  
- <span data-ttu-id="65d05-128">使用預設</span><span class="sxs-lookup"><span data-stu-id="65d05-128">Use default</span></span>

<span data-ttu-id="65d05-129">如果將此欄位設定為 **自訂定價** ，Dynamics 365 就不會設定預設價格。</span><span class="sxs-lookup"><span data-stu-id="65d05-129">If you set this field to **Override pricing** , Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="65d05-130">您必須在報價明細上輸入產品的價格。</span><span class="sxs-lookup"><span data-stu-id="65d05-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="65d05-131">如果將此欄位設定為 **使用預設** ，則 Dynamics 365 會使用預設銷售價格，並鎖定欄位以防編輯。</span><span class="sxs-lookup"><span data-stu-id="65d05-131">If you set this field to **Use default** , Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="65d05-132">安裝 PSA 之後，會在報價的產品型明細上輸入預設銷售價格。</span><span class="sxs-lookup"><span data-stu-id="65d05-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="65d05-133">**定價** 欄位會接著設定為 **自訂定價** ，因此您可以編輯報價明細上的預設價格。</span><span class="sxs-lookup"><span data-stu-id="65d05-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![設定自訂定價](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="65d05-135">產品的數量因數</span><span class="sxs-lookup"><span data-stu-id="65d05-135">Quantity factors for products</span></span>

<span data-ttu-id="65d05-136">PSA 使用數量因素來支援以訂閱型產品的銷售。</span><span class="sxs-lookup"><span data-stu-id="65d05-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="65d05-137">對於訂閱型產品，報價或專案合約服務內容上的數量會以使用者的月數來表示。</span><span class="sxs-lookup"><span data-stu-id="65d05-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="65d05-138">訂閱軟體的價格通常在目錄中儲存為每個月每個使用者的價格。</span><span class="sxs-lookup"><span data-stu-id="65d05-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="65d05-139">但是，您可以改用其他時間描述。</span><span class="sxs-lookup"><span data-stu-id="65d05-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="65d05-140">在銷售處理期間，報價明細的價格通常是由 IT 銷售專員議定並打折扣的每個使用者、每個月的價格。</span><span class="sxs-lookup"><span data-stu-id="65d05-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="65d05-141">每筆交易都有不同的使用者數目和不同的訂閱月數。</span><span class="sxs-lookup"><span data-stu-id="65d05-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="65d05-142">用來計算報價明細金額的數量，是使用者人數與訂閱月數的乘積。</span><span class="sxs-lookup"><span data-stu-id="65d05-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="65d05-143">為了支援此類型的銷售，PSA 引進了數量因數的概念。</span><span class="sxs-lookup"><span data-stu-id="65d05-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="65d05-144">數量因數依賴 Dynamics 365 中的產品屬性。</span><span class="sxs-lookup"><span data-stu-id="65d05-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="65d05-145">當您設定產品的特定屬性時，PSA 可讓您將這些屬性子集或所有屬性標示為數量因數。</span><span class="sxs-lookup"><span data-stu-id="65d05-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="65d05-146">PSA 會驗證只有含有數值資料類型的數值屬性或產品屬性，才會標記為數量因數。</span><span class="sxs-lookup"><span data-stu-id="65d05-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="65d05-147">將設定數量因數的產品新增至報價明細時，報價明細上的 **數量** 欄位會變成唯讀欄位。</span><span class="sxs-lookup"><span data-stu-id="65d05-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="65d05-148">輸入數量因數的產品屬性值之後，PSA 會計算報價明細的數量。</span><span class="sxs-lookup"><span data-stu-id="65d05-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="65d05-149">例如，Dynamics 365 可能有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="65d05-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="65d05-150">**使用者數** - 使用者的數目</span><span class="sxs-lookup"><span data-stu-id="65d05-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="65d05-151">**月數** - 訂閱的月期數</span><span class="sxs-lookup"><span data-stu-id="65d05-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="65d05-152">**產品 SKU**</span><span class="sxs-lookup"><span data-stu-id="65d05-152">**Product SKU**</span></span> 

<span data-ttu-id="65d05-153">您可以編輯產品明細的屬性，將 **使用者數** 和 **月數** 屬性標示為數量因數。</span><span class="sxs-lookup"><span data-stu-id="65d05-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![將 [使用者數] 和 [月數] 標示為品質因數](media/basic-guide-11.png)
 
