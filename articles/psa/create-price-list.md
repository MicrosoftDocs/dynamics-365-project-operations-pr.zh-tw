---
title: 建立價目表
description: 如何建立 Project Service 中的價目表
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290304"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="1029f-103">建立價目表 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1029f-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1029f-104">價目表提供範本，可讓客戶經理用來建立報價和專案，以及建立專案的成本。</span><span class="sxs-lookup"><span data-stu-id="1029f-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="1029f-105">價目表提供角色和費用的明細項目清單，以及您對每一項的收費價格。</span><span class="sxs-lookup"><span data-stu-id="1029f-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="1029f-106">您可以建立多份價目表，針對不同的產品銷售區域或不同的銷售管道維護不同的價格結構。</span><span class="sxs-lookup"><span data-stu-id="1029f-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="1029f-107">最好為您打算向客戶收費所採用的每一種貨幣建立至少一份價目表。</span><span class="sxs-lookup"><span data-stu-id="1029f-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="1029f-108">若要建立所要交付工作的財務估計值，請確定每個專案都有支援成本和銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="1029f-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="1029f-109">設定預設成本和銷售價目表，套用至組織中建立的所有專案。</span><span class="sxs-lookup"><span data-stu-id="1029f-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="1029f-110">價目表是依據角色和費用類別，因此在您建立價目表之前，請確定您已經設定要在建立價目表時使用的角色和成本類別。</span><span class="sxs-lookup"><span data-stu-id="1029f-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="1029f-111">移至 **Project Service > 價目表**。</span><span class="sxs-lookup"><span data-stu-id="1029f-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="1029f-112">按一下 **新增**。</span><span class="sxs-lookup"><span data-stu-id="1029f-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="1029f-113">在 **內容** 中，選取此價目表用於 **成本**、**購買** 或 **銷售**。</span><span class="sxs-lookup"><span data-stu-id="1029f-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="1029f-114">在 **名稱** 中，輸入價目表的名稱。</span><span class="sxs-lookup"><span data-stu-id="1029f-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="1029f-115">在 **貨幣** 中，選取您要用於計費或成本的貨幣。</span><span class="sxs-lookup"><span data-stu-id="1029f-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="1029f-116">在 **時間單位** 中，指定價格適用的期間，例如天或小時。</span><span class="sxs-lookup"><span data-stu-id="1029f-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="1029f-117">視需要填入 **開始日期**、**結束日期** 及 **描述**。</span><span class="sxs-lookup"><span data-stu-id="1029f-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="1029f-118">按一下 **儲存** 建立記錄，如此就能繼續編輯。</span><span class="sxs-lookup"><span data-stu-id="1029f-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="1029f-119">若要在價目表中新增角色價格，按一下 **角色價格** 底下的 **+**。</span><span class="sxs-lookup"><span data-stu-id="1029f-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="1029f-120">在 **角色價格** 窗格中填入詳細資料，然後按一下 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="1029f-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="1029f-121">視需要繼續新增角色價格。</span><span class="sxs-lookup"><span data-stu-id="1029f-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="1029f-122">完成時，按一下畫面右下角的 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="1029f-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="1029f-123">若要在價目表中新增費用類別價格，按一下 **類別價格** 底下的 **+**。</span><span class="sxs-lookup"><span data-stu-id="1029f-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="1029f-124">在 **交易類別價格** 窗格中填入詳細資料，然後按一下 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="1029f-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="1029f-125">視需要繼續新增類別價格。</span><span class="sxs-lookup"><span data-stu-id="1029f-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="1029f-126">完成時，按一下畫面右下角的 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="1029f-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="1029f-127">若要在價目表中新增價目表項目，按一下 **價目表項目** 底下的 **+**。</span><span class="sxs-lookup"><span data-stu-id="1029f-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="1029f-128">在 **價目表項目** 窗格中填入詳細資料，然後按一下 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="1029f-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="1029f-129">視需要繼續新增價目表項目。</span><span class="sxs-lookup"><span data-stu-id="1029f-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="1029f-130">完成時，按一下畫面右下角的 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="1029f-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="1029f-131">若要在價目表中新增領域關聯，按一下 **領域關聯** 底下的 **+**。</span><span class="sxs-lookup"><span data-stu-id="1029f-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="1029f-132">在 **新增關係** 視窗中填入詳細資料，然後按一下 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="1029f-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="1029f-133">視需要繼續新增領域關聯。</span><span class="sxs-lookup"><span data-stu-id="1029f-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="1029f-134">完成時，按一下畫面右下角的 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="1029f-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1029f-135">請參閱</span><span class="sxs-lookup"><span data-stu-id="1029f-135">See Also</span></span>  
 [<span data-ttu-id="1029f-136">設定 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1029f-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]