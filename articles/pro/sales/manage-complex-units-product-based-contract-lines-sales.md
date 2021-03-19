---
title: 管理產品型合約服務內容的複雜單位 - 精簡
description: 本主題提供有關支援訂閱型產品銷售的資訊。
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273323"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="0b086-103">管理產品型合約服務內容的複雜單位 - 精簡</span><span class="sxs-lookup"><span data-stu-id="0b086-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="0b086-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="0b086-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0b086-105">Dynamics 365 Project Operations 使用數量因素來支援訂閱型產品的銷售。</span><span class="sxs-lookup"><span data-stu-id="0b086-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="0b086-106">對於訂閱型產品，合約或專案合約服務內容上的數量會以使用者月數來表示。</span><span class="sxs-lookup"><span data-stu-id="0b086-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="0b086-107">訂閱軟體的價格在目錄中儲存為每個月每個使用者的價格。</span><span class="sxs-lookup"><span data-stu-id="0b086-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="0b086-108">在銷售處理期間，合約服務內容的價格通常是由 IT 銷售專員所議定且給予折扣優惠的每個使用者、每個月的價格。</span><span class="sxs-lookup"><span data-stu-id="0b086-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="0b086-109">每筆交易都有不同的使用者數目和不同的訂閱月數。</span><span class="sxs-lookup"><span data-stu-id="0b086-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="0b086-110">用來計算合約服務內容金額的數量，是使用者人數與訂閱月數的乘積。</span><span class="sxs-lookup"><span data-stu-id="0b086-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="0b086-111">為了支援此類型的銷售，Project Operations 支援 *數量因數* 的概念。</span><span class="sxs-lookup"><span data-stu-id="0b086-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="0b086-112">數量因數依賴產品屬性。</span><span class="sxs-lookup"><span data-stu-id="0b086-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="0b086-113">設定產品的特定屬性時，您可以將這其中一部分屬性或所有屬性標示為數量因數。</span><span class="sxs-lookup"><span data-stu-id="0b086-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="0b086-114">Project Operations 會驗證是否只有含有數值資料類型的數值屬性或產品屬性，才會標記為數量因數。</span><span class="sxs-lookup"><span data-stu-id="0b086-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="0b086-115">將已設定數量因數的產品新增至合約服務內容時，**數量** 欄位會變成唯讀。</span><span class="sxs-lookup"><span data-stu-id="0b086-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="0b086-116">輸入數量因數的產品屬性值之後，Project Operations 會計算合約服務內容的數量。</span><span class="sxs-lookup"><span data-stu-id="0b086-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="0b086-117">例如，Dynamics 365 Sales 可能有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="0b086-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="0b086-118">**使用者數**：使用者的數目。</span><span class="sxs-lookup"><span data-stu-id="0b086-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="0b086-119">**月數**：訂閱的月期數。</span><span class="sxs-lookup"><span data-stu-id="0b086-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="0b086-120">**產品 SKU**：產品的庫存單位 (SKU)。</span><span class="sxs-lookup"><span data-stu-id="0b086-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="0b086-121">您可以編輯產品明細的屬性，將 **使用者數** 和 **月數** 屬性標示為數量因數。</span><span class="sxs-lookup"><span data-stu-id="0b086-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="0b086-122">若要從產品屬性建立數量因數，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="0b086-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="0b086-123">在 **Project Operations** 中，選取 **銷售 - 產品**。</span><span class="sxs-lookup"><span data-stu-id="0b086-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="0b086-124">開啟需要設定數量因數的產品。</span><span class="sxs-lookup"><span data-stu-id="0b086-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="0b086-125">確定已設定該產品的屬性。</span><span class="sxs-lookup"><span data-stu-id="0b086-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="0b086-126">在 **專案資訊** 頁面上，選取 **數量因數** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="0b086-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="0b086-127">在子格中，選取 **+ 新增欄位計算**。</span><span class="sxs-lookup"><span data-stu-id="0b086-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="0b086-128">輸入 **數量因數** 的名稱，並選取對應至欄位計算的屬性值。</span><span class="sxs-lookup"><span data-stu-id="0b086-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="0b086-129">儲存後關閉表單。</span><span class="sxs-lookup"><span data-stu-id="0b086-129">Save and close the form.</span></span>
7. <span data-ttu-id="0b086-130">針對所有共同構成產品型合約服務內容數量的屬性，重複步驟 2-6。</span><span class="sxs-lookup"><span data-stu-id="0b086-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="0b086-131">設定了數量因數後，當使用者建立此產品的合約服務內容時，就會鎖定合約服務內容的數量。</span><span class="sxs-lookup"><span data-stu-id="0b086-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="0b086-132">此數量接著會計算成該合約服務內容的屬性值乘積。</span><span class="sxs-lookup"><span data-stu-id="0b086-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]