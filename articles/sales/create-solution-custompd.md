---
title: 建立自訂定價維度解決方案
description: 本主題提供如何為自訂定價維度建立解決方案的資訊。
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278408"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="3b57b-103">建立自訂定價維度解決方案</span><span class="sxs-lookup"><span data-stu-id="3b57b-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="3b57b-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="3b57b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="3b57b-105">所有自訂定價維度變更都必須是在另一個的解決方案中。</span><span class="sxs-lookup"><span data-stu-id="3b57b-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="3b57b-106">這個重要的最佳做法提供您日後視需要更新或移除變更的彈性、有助於重複使用您的工作，以及讓您更便於將變更移植到另一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="3b57b-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="3b57b-107">進行所有必要變更之後，將此解決方案匯出為 **受管理的** 解決方案，再將其匯入至其他執行個體即可重複使用。</span><span class="sxs-lookup"><span data-stu-id="3b57b-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="3b57b-108">建立自訂定價維度解決方案</span><span class="sxs-lookup"><span data-stu-id="3b57b-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="3b57b-109">選取 **設定** > **解決方案**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="3b57b-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="3b57b-110">將解決方案命名為 *<your organization name> 定價維度*。</span><span class="sxs-lookup"><span data-stu-id="3b57b-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="3b57b-111">輸入其餘必要資訊，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="3b57b-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![建立自訂定價維度解決方案](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="3b57b-113">將所有必要的實體及相關元件新增至定價維度解決方案</span><span class="sxs-lookup"><span data-stu-id="3b57b-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="3b57b-114">將下列 Project Service 實體新增至定價解決方案中，以在定價解決方案中進行重要的架構變更。</span><span class="sxs-lookup"><span data-stu-id="3b57b-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="3b57b-115">在您完成此程序之後，實體將會識別新的定價維度。</span><span class="sxs-lookup"><span data-stu-id="3b57b-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="3b57b-116">選取 **設定** > **解決方案**，然後按兩下 **<*您的組織名稱*> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="3b57b-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="3b57b-117">在方案總管的左導覽窗格中，選取 **新增現有的** >  **實體**。</span><span class="sxs-lookup"><span data-stu-id="3b57b-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="3b57b-118">在 **解決方案元件** 對話方塊中，選取下列實體：</span><span class="sxs-lookup"><span data-stu-id="3b57b-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="3b57b-119">**實際**</span><span class="sxs-lookup"><span data-stu-id="3b57b-119">**Actual**</span></span>
   - <span data-ttu-id="3b57b-120">**可預約資源**</span><span class="sxs-lookup"><span data-stu-id="3b57b-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="3b57b-121">**估計明細**</span><span class="sxs-lookup"><span data-stu-id="3b57b-121">**Estimate Line**</span></span>
   - <span data-ttu-id="3b57b-122">**專案工作**</span><span class="sxs-lookup"><span data-stu-id="3b57b-122">**Project Task**</span></span>
   - <span data-ttu-id="3b57b-123">**發票明細詳細資料**</span><span class="sxs-lookup"><span data-stu-id="3b57b-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="3b57b-124">**帳目明細**</span><span class="sxs-lookup"><span data-stu-id="3b57b-124">**Journal Line**</span></span>
   - <span data-ttu-id="3b57b-125">**專案合約服務內容詳細資料**</span><span class="sxs-lookup"><span data-stu-id="3b57b-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="3b57b-126">**專案團隊成員**</span><span class="sxs-lookup"><span data-stu-id="3b57b-126">**Project Team Member**</span></span>
   - <span data-ttu-id="3b57b-127">**報價明細詳細資料**</span><span class="sxs-lookup"><span data-stu-id="3b57b-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="3b57b-128">**角色價格加成**</span><span class="sxs-lookup"><span data-stu-id="3b57b-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="3b57b-129">**角色價格**</span><span class="sxs-lookup"><span data-stu-id="3b57b-129">**Role Price**</span></span>
   - <span data-ttu-id="3b57b-130">**時間項目**</span><span class="sxs-lookup"><span data-stu-id="3b57b-130">**Time Entry**</span></span>
 
   ![新增現有實體自訂定價維度解決方案](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="3b57b-132">針對每個實體，複查要新增的元件，以及每個實體的最終實體資產清單。</span><span class="sxs-lookup"><span data-stu-id="3b57b-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="3b57b-133">包含所選每個實體的所有表單和檢視表。</span><span class="sxs-lookup"><span data-stu-id="3b57b-133">Include all forms and views for each of the selected entities.</span></span>

  ![已新增實體](./media/solution-component-selection.png)


5.  <span data-ttu-id="3b57b-135">當系統提示您包括所選取實體的任何相依實體時，請選取 **不，請勿包括必要元件**。</span><span class="sxs-lookup"><span data-stu-id="3b57b-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![包括相依實體](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]