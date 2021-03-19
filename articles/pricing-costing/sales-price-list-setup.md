---
title: 設定銷售價目表
description: 本主題提供有關專案定價銷售價目表的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 05b1c13540e902975eee7379276cf394d9fc5743
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275438"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="9d9aa-103">設定銷售價目表</span><span class="sxs-lookup"><span data-stu-id="9d9aa-103">Set up a sales price list</span></span>

<span data-ttu-id="9d9aa-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="9d9aa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9d9aa-105">對於專案報價和合約，專案價目表的價格覆寫模式與產品價目表的不同。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="9d9aa-106">在產品類別目錄型報價明細上，您可以直接在報價明細上覆寫角色和類別的價格，因為每個報價明細都只指向一個目錄項目。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="9d9aa-107">不過，在專案型報價明細上，您無法直接在報價明細上覆寫角色和類別的價格。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="9d9aa-108">您可以使用專案價目表來處理兩種不同的覆寫模式。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="9d9aa-109">建議您讓專案資源和目錄項目使用不同的價目表，因為覆寫定價時，兩者之間的行為有差異。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="9d9aa-110">下列每個實體都可以有一個或多個用於專案定價的相關聯銷售價目表：</span><span class="sxs-lookup"><span data-stu-id="9d9aa-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="9d9aa-111">客戶 (帳戶)</span><span class="sxs-lookup"><span data-stu-id="9d9aa-111">Customer (account)</span></span> 
- <span data-ttu-id="9d9aa-112">商機</span><span class="sxs-lookup"><span data-stu-id="9d9aa-112">Opportunity</span></span> 
- <span data-ttu-id="9d9aa-113">報價</span><span class="sxs-lookup"><span data-stu-id="9d9aa-113">Quote</span></span> 
- <span data-ttu-id="9d9aa-114">專案合約</span><span class="sxs-lookup"><span data-stu-id="9d9aa-114">Project Contract</span></span>

<span data-ttu-id="9d9aa-115">這些實體與價目表的關聯是透過專案價目表來表示。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="9d9aa-116">您可以將一個或多個價目表與客戶、商機、報價及專案合約銷售實體建立關聯。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="9d9aa-117">系統不會自動在客戶記錄上輸入預設專案價目表。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="9d9aa-118">不過，您可以手動將專案價目表附加至客戶記錄。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="9d9aa-119">然而，只有在與客戶之間存在自訂定價合約時，您才應該手動附加專案價目表。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="9d9aa-120">將專案價目表附加至銷售實體時，系統會驗證下列資訊：</span><span class="sxs-lookup"><span data-stu-id="9d9aa-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="9d9aa-121">價目表的內容與 **銷售** 有關。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="9d9aa-122">價目表貨幣與客戶貨幣相符。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="9d9aa-123">在專案合約上，使用下列優先順序自動設定相關的專案價目表：</span><span class="sxs-lookup"><span data-stu-id="9d9aa-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="9d9aa-124">報價</span><span class="sxs-lookup"><span data-stu-id="9d9aa-124">Quote</span></span>
2. <span data-ttu-id="9d9aa-125">商機​​</span><span class="sxs-lookup"><span data-stu-id="9d9aa-125">Opportunity</span></span>
3. <span data-ttu-id="9d9aa-126">客戶</span><span class="sxs-lookup"><span data-stu-id="9d9aa-126">Customer</span></span> 
4. <span data-ttu-id="9d9aa-127">全域設定</span><span class="sxs-lookup"><span data-stu-id="9d9aa-127">Global settings</span></span> 

<span data-ttu-id="9d9aa-128">預設會輸入專案價目表時，系統會驗證貨幣是否與客戶貨幣相符，以及所輸入預設價目表的內容是否與 **銷售** 有關。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="9d9aa-129">您可以將或多個專案價目表與客戶、商機、報價及專案合約銷售實體建立關聯。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="9d9aa-130">此功能支援長期專案合約的日期特定預設價格，您可能需要多個價目表來處理因通貨膨脹而進行的價格更新。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="9d9aa-131">不過，如果與客戶、商機、報價或專案合約實體建立關聯的價目表有重疊的有效日期範圍，則預設價格可能不正確。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="9d9aa-132">因此，您必須確保有效日期範圍重疊的專案價目表未與這些實體相關聯。</span><span class="sxs-lookup"><span data-stu-id="9d9aa-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]