---
title: 停用價目表
description: 本主題說明如何停用或移除未使用或舊的價目表。
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001326"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="6a939-103">停用價目表</span><span class="sxs-lookup"><span data-stu-id="6a939-103">Deactivate price lists</span></span> 

<span data-ttu-id="6a939-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="6a939-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6a939-105">若要從 Dynamics 365 Project Operations 移除舊的或未使用的價目表，必須完成兩個步驟。</span><span class="sxs-lookup"><span data-stu-id="6a939-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="6a939-106">從特定頁面移除或刪除價目表。</span><span class="sxs-lookup"><span data-stu-id="6a939-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="6a939-107">從 **價目表** 頁面的使用中價目表停用或刪除價目表。</span><span class="sxs-lookup"><span data-stu-id="6a939-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="6a939-108">您必須完成這兩個步驟才能完全移除價目表。</span><span class="sxs-lookup"><span data-stu-id="6a939-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="6a939-109">只執行步驟 2 (即直接從 [使用中價目表] 檢視表移除或停用價目表) 是不夠的。</span><span class="sxs-lookup"><span data-stu-id="6a939-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="6a939-110">您還必須從步驟 1 提到的所有位置中刪除此價目表的關聯。</span><span class="sxs-lookup"><span data-stu-id="6a939-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="6a939-111">從特定頁面刪除價目表</span><span class="sxs-lookup"><span data-stu-id="6a939-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="6a939-112">若要從 Project Operations 中刪除價目表，請移至下列頁面：</span><span class="sxs-lookup"><span data-stu-id="6a939-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="6a939-113">**專案參數** 頁面 > **價目表** 索引標籤</span><span class="sxs-lookup"><span data-stu-id="6a939-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="6a939-114">**組織單位** 頁面 > **價目表** 網格</span><span class="sxs-lookup"><span data-stu-id="6a939-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="6a939-115">**客戶** 頁面 > **專案價目表** 網格</span><span class="sxs-lookup"><span data-stu-id="6a939-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="6a939-116">**專案報價** 頁面 > **專案價目表** 網格：這會套用至所有使用中專案報價。</span><span class="sxs-lookup"><span data-stu-id="6a939-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="6a939-117">**專案連絡人** 頁面 > **專案價目表** 網格：這會套用至所有使用中專案連絡人。</span><span class="sxs-lookup"><span data-stu-id="6a939-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="6a939-118">您必須在每個頁面中選取您要刪除的價目表，然後選取 **刪除**。</span><span class="sxs-lookup"><span data-stu-id="6a939-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="6a939-119">從價目表頁面刪除或停用價目表</span><span class="sxs-lookup"><span data-stu-id="6a939-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="6a939-120">若要從使用中價目表中刪除價目表，請移至 **銷售** > **客戶** > **價目表**。</span><span class="sxs-lookup"><span data-stu-id="6a939-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="6a939-121">選取您要刪除的價目表，然後選取 **刪除**。</span><span class="sxs-lookup"><span data-stu-id="6a939-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="6a939-122">如果任何現有交易參考了價目表，就無法將其刪除。</span><span class="sxs-lookup"><span data-stu-id="6a939-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="6a939-123">如果發生這種情況，您可以停用價目表，使其不再出現於任何檢視表。</span><span class="sxs-lookup"><span data-stu-id="6a939-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="6a939-124">若要停用價目表，請再次選取價目表，然後選取 **停用**。</span><span class="sxs-lookup"><span data-stu-id="6a939-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
