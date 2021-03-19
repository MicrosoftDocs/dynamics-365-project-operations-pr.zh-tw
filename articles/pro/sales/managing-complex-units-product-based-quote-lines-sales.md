---
title: 管理產品型報價明細的複雜單位，例如按使用者、按月為單位 - 精簡
description: 本主題提供有關管理產品型報價明細複雜單位的資訊。
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4a075ae5a7329f241cc31afceab0e085c771f72
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272873"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="27f15-103">管理產品型報價明細的複雜單位，例如按使用者、按月為單位 - 精簡</span><span class="sxs-lookup"><span data-stu-id="27f15-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="27f15-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="27f15-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="27f15-105">Dynamics 365 Project Operations 使用數量因素來支援訂閱型產品的銷售。</span><span class="sxs-lookup"><span data-stu-id="27f15-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="27f15-106">對於訂閱型產品，報價或專案合約服務內容上的數量會以使用者的月數來表示。</span><span class="sxs-lookup"><span data-stu-id="27f15-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="27f15-107">訂閱軟體的價格通常在目錄中儲存為每個月每個使用者的價格。</span><span class="sxs-lookup"><span data-stu-id="27f15-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="27f15-108">在銷售處理期間，報價明細的價格通常是由 IT 銷售專員議定並打折扣的每個使用者、每個月的價格。</span><span class="sxs-lookup"><span data-stu-id="27f15-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="27f15-109">每筆交易都有不同的使用者數目和不同的訂閱月數。</span><span class="sxs-lookup"><span data-stu-id="27f15-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="27f15-110">用來計算報價明細的數量，是使用者人數與訂閱月數的乘積。</span><span class="sxs-lookup"><span data-stu-id="27f15-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="27f15-111">為了支援此類型的銷售，Project Operations 引進了數量因數的概念。</span><span class="sxs-lookup"><span data-stu-id="27f15-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="27f15-112">數量因數依賴 Dynamics 365 中的產品屬性。</span><span class="sxs-lookup"><span data-stu-id="27f15-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="27f15-113">設定產品的特定屬性時，Project Operations 可讓您將這些屬性子集或所有屬性標記為數量因數。</span><span class="sxs-lookup"><span data-stu-id="27f15-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="27f15-114">Project Operations 會驗證是否只有含有數值資料類型的數值屬性或產品屬性，才會標記為數量因數。</span><span class="sxs-lookup"><span data-stu-id="27f15-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="27f15-115">當您將含有數量因數的產品新增至報價明細時，**數量** 欄位會變成唯讀。</span><span class="sxs-lookup"><span data-stu-id="27f15-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="27f15-116">輸入數量因數的產品屬性值之後，Project Operations 會計算報價明細的數量。</span><span class="sxs-lookup"><span data-stu-id="27f15-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="27f15-117">例如，Dynamics 365 Sales 可能有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="27f15-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="27f15-118">**使用者數**：使用者的數目</span><span class="sxs-lookup"><span data-stu-id="27f15-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="27f15-119">**月數**：訂閱的月期數</span><span class="sxs-lookup"><span data-stu-id="27f15-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="27f15-120">**產品 SKU**</span><span class="sxs-lookup"><span data-stu-id="27f15-120">**Product SKU**</span></span>

<span data-ttu-id="27f15-121">您可以編輯產品明細的屬性，將 **使用者數** 和 **月數** 屬性標記為數量因數。</span><span class="sxs-lookup"><span data-stu-id="27f15-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="27f15-122">若要從產品屬性建立數量因數，請依照下列步驟進行：</span><span class="sxs-lookup"><span data-stu-id="27f15-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="27f15-123">在 Project Operations 左導覽窗格上，移至 **銷售** > **產品**。</span><span class="sxs-lookup"><span data-stu-id="27f15-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="27f15-124">開啟需要設定數量因數的產品。</span><span class="sxs-lookup"><span data-stu-id="27f15-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="27f15-125">確定已設定產品的屬性。</span><span class="sxs-lookup"><span data-stu-id="27f15-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="27f15-126">在產品的 **專案資訊** 頁面上，選取 **數量因數** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="27f15-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="27f15-127">在子格中，選取 **+ 新增欄位計算**。</span><span class="sxs-lookup"><span data-stu-id="27f15-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="27f15-128">輸入數量因數的名稱，並選取對應至欄位計算的屬性值。</span><span class="sxs-lookup"><span data-stu-id="27f15-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="27f15-129">儲存後關閉表單。</span><span class="sxs-lookup"><span data-stu-id="27f15-129">Save and close the form.</span></span> <span data-ttu-id="27f15-130">針對所有要用於計算產品型報價明細數量的屬性，重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="27f15-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="27f15-131">建立產品的產品型報價明細時，會鎖定報價明細的數量。</span><span class="sxs-lookup"><span data-stu-id="27f15-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="27f15-132">計算所得數量會是您針對該報價明細所輸入各個屬性值的乘積。</span><span class="sxs-lookup"><span data-stu-id="27f15-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]