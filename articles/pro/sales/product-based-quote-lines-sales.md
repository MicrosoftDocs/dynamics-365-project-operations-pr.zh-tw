---
title: 產品型報價明細概觀 - 精簡
description: 本主題提供有關使用產品型報價明細的資訊。
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178178"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="6505a-103">產品型報價明細概觀 - 精簡</span><span class="sxs-lookup"><span data-stu-id="6505a-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="6505a-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="6505a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6505a-105">您可以在 Dynamics 365 Project Operations 中建立產品型報價明細。</span><span class="sxs-lookup"><span data-stu-id="6505a-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="6505a-106">產品型報價明細可以手動新增，也可以是產品類別目錄中的項目。</span><span class="sxs-lookup"><span data-stu-id="6505a-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="6505a-107">產品類別目錄</span><span class="sxs-lookup"><span data-stu-id="6505a-107">Product catalog</span></span>

<span data-ttu-id="6505a-108">產品類別目錄中的每個產品都有預設單位與單位群組。</span><span class="sxs-lookup"><span data-stu-id="6505a-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="6505a-109">如果有數種產品共用同一組屬性，您可以建立共用這些屬性的產品系列。</span><span class="sxs-lookup"><span data-stu-id="6505a-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="6505a-110">例如，公司銷售各種不同軟體的訂閱授權。</span><span class="sxs-lookup"><span data-stu-id="6505a-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="6505a-111">所有訂閱軟體都有下列兩個屬性：</span><span class="sxs-lookup"><span data-stu-id="6505a-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="6505a-112">使用者數目</span><span class="sxs-lookup"><span data-stu-id="6505a-112">Number of users</span></span>
- <span data-ttu-id="6505a-113">訂閱期間 (以月為單位)</span><span class="sxs-lookup"><span data-stu-id="6505a-113">A subscription duration measured in months</span></span>

<span data-ttu-id="6505a-114">若要維護這種目錄類型，請建立名為 **訂閱軟體** 的產品系列，並新增使用者數目和訂閱期間做為屬性。</span><span class="sxs-lookup"><span data-stu-id="6505a-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="6505a-115">接下來，您可以將個別產品新增至 **訂閱軟體** 產品系列。</span><span class="sxs-lookup"><span data-stu-id="6505a-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="6505a-116">將產品類別目錄專案新增至專案報價</span><span class="sxs-lookup"><span data-stu-id="6505a-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="6505a-117">**專案報價** 與 **專案合約** 頁面有專案型和產品型明細的區段。</span><span class="sxs-lookup"><span data-stu-id="6505a-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="6505a-118">對於產品型明細，報價明細或專案合約服務內容的下拉式清單產品價目表中的所有產品和單位。</span><span class="sxs-lookup"><span data-stu-id="6505a-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="6505a-119">您也可以新增不屬於產品價目表的產品。</span><span class="sxs-lookup"><span data-stu-id="6505a-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="6505a-120">此外，您還可以從其他價目表或者直接從產品類別目錄選取產品。</span><span class="sxs-lookup"><span data-stu-id="6505a-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="6505a-121">直接從產品類別目錄選取產品時，會使用該產品的預設價目表來取得產品的銷售價格。</span><span class="sxs-lookup"><span data-stu-id="6505a-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="6505a-122">如果未設定預設價目表，價格會設定為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="6505a-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="6505a-123">當報價明細是根據產品類別目錄所建立，您可以直接在報價明細上覆寫銷售價格。</span><span class="sxs-lookup"><span data-stu-id="6505a-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="6505a-124">**定價** 欄位中的報價明細有兩個可用值：</span><span class="sxs-lookup"><span data-stu-id="6505a-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="6505a-125">**覆寫定價**</span><span class="sxs-lookup"><span data-stu-id="6505a-125">**Override Pricing**</span></span>
- <span data-ttu-id="6505a-126">**預設價格**</span><span class="sxs-lookup"><span data-stu-id="6505a-126">**Use Default**</span></span>

<span data-ttu-id="6505a-127">如果您選取 **覆寫定價**，將不會設定預設價格。</span><span class="sxs-lookup"><span data-stu-id="6505a-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="6505a-128">反之，您必須在報價明細上輸入產品的價格。</span><span class="sxs-lookup"><span data-stu-id="6505a-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="6505a-129">如果您選取 **使用預設值**，則會使用預設售價，而且欄位會鎖定無法編輯。</span><span class="sxs-lookup"><span data-stu-id="6505a-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="6505a-130">在報價的產品型明細上輸入預設售價。</span><span class="sxs-lookup"><span data-stu-id="6505a-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="6505a-131">**定價** 欄位會接著設定為 **覆寫定價**，因此您可以編輯報價明細上的預設價格。</span><span class="sxs-lookup"><span data-stu-id="6505a-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="6505a-132">這是 Dynamics 365 Sales 中，針對產品型明細行為的 Project Operations 特有覆寫功能。</span><span class="sxs-lookup"><span data-stu-id="6505a-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
