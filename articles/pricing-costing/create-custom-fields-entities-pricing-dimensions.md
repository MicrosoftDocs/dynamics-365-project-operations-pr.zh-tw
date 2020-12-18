---
title: 將自訂欄位及實體建立為定價維度
description: 本主題提供有關如何建立自訂選項組或實體的資訊。
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642803"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="3048d-103">將自訂欄位及實體建立為定價維度</span><span class="sxs-lookup"><span data-stu-id="3048d-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="3048d-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="3048d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3048d-105">當您想要建立自訂選項組或實體以用作定價維度時，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="3048d-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="3048d-106">如需詳細資訊，請參閱[定價維度概觀](pricing-dimensions-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="3048d-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="3048d-107">建議您在不同的解決方案中進行所有自訂定價維度變更。</span><span class="sxs-lookup"><span data-stu-id="3048d-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="3048d-108">這個重要的最佳做法提供您日後視需要更新或移除變更的彈性。</span><span class="sxs-lookup"><span data-stu-id="3048d-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="3048d-109">有助於重複使用您的工作，以及讓您更便於將這些變更移植到另一個執行個體。進行所有必要變更之後，將此解決方案匯出為 **受管理的解決方案**，再將其匯入至其他執行個體，即可重複使用您的定價設定。</span><span class="sxs-lookup"><span data-stu-id="3048d-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="3048d-110">在定價維度解決方案中建立自訂欄位及選項組</span><span class="sxs-lookup"><span data-stu-id="3048d-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="3048d-111">定價維度可以是選項組或實體。</span><span class="sxs-lookup"><span data-stu-id="3048d-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="3048d-112">兩者預必須在定價解決方案中建立。</span><span class="sxs-lookup"><span data-stu-id="3048d-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="3048d-113">此程序中的步驟說明如何建立以實體為準的維度和以選項組為準的維度。</span><span class="sxs-lookup"><span data-stu-id="3048d-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="3048d-114">以實體為準的維度</span><span class="sxs-lookup"><span data-stu-id="3048d-114">Entity-based dimensions</span></span>
<span data-ttu-id="3048d-115">若要建立以實體為準的維度，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="3048d-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="3048d-116">移至 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="3048d-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="3048d-117">在方案總管的左導覽窗格中，選取 **實體**。</span><span class="sxs-lookup"><span data-stu-id="3048d-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="3048d-118">選取 **新增** 以建立名為 **標準職稱** 的新實體。</span><span class="sxs-lookup"><span data-stu-id="3048d-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="3048d-119">輸入其餘必要資訊，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="3048d-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![標準職稱實體定義](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="3048d-121">以選項組為準的維度</span><span class="sxs-lookup"><span data-stu-id="3048d-121">Option set-based dimensions</span></span> 
<span data-ttu-id="3048d-122">您可以建立兩個以選項組為準的維度。</span><span class="sxs-lookup"><span data-stu-id="3048d-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="3048d-123">使用 **資源工作地點** 來追蹤 **住家** 地點工作和 **現場** 工作的價格。</span><span class="sxs-lookup"><span data-stu-id="3048d-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="3048d-124">使用 **資源工作時數** 搭配 **正常工時** 和 **加班工時** 值，在工作完成時套用加成。</span><span class="sxs-lookup"><span data-stu-id="3048d-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="3048d-125">下圖提供 **資源工作地點** 維度的檢視表。</span><span class="sxs-lookup"><span data-stu-id="3048d-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![以選項組為準的定價維度，名為「資源工作地點」](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="3048d-127">下圖提供 **資源工作時數** 維度的檢視表。</span><span class="sxs-lookup"><span data-stu-id="3048d-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![以選項組為準的定價維度，名為「資源工作時數」](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="3048d-129">移至 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="3048d-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="3048d-130">在方案總管的左導覽窗格中，選取 **選項組**。</span><span class="sxs-lookup"><span data-stu-id="3048d-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="3048d-131">選取 **新增** 建立新的選項組、輸入其餘必要資訊，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="3048d-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="3048d-132">建立以實體為準維度的資料</span><span class="sxs-lookup"><span data-stu-id="3048d-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="3048d-133">您可以手動建立以實體為準維度的資料，或是使用 Microsoft Excel 匯入或服務通話來建立此資料</span><span class="sxs-lookup"><span data-stu-id="3048d-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="3048d-134">使用此程序中的步驟，從以實體為準的維度 **標準職稱** 建立兩個標準職稱 **系統工程師** 和 **資深系統工程師**。</span><span class="sxs-lookup"><span data-stu-id="3048d-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="3048d-135">如果要建立的資料不大 (如下列範例所示)，您可以使用標準表單。</span><span class="sxs-lookup"><span data-stu-id="3048d-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="3048d-136">選取 **進階尋找**。</span><span class="sxs-lookup"><span data-stu-id="3048d-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="3048d-137">選取 **標準職稱** 實體，然後選取 **結果**。</span><span class="sxs-lookup"><span data-stu-id="3048d-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="3048d-138">將會顯示 **標準職稱** 實體中所有的列。</span><span class="sxs-lookup"><span data-stu-id="3048d-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="3048d-139">選取 **新增**，並在 **名稱** 欄位中輸入「系統工程師」，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="3048d-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="3048d-140">關閉頁面。</span><span class="sxs-lookup"><span data-stu-id="3048d-140">Close the page.</span></span> 
5. <span data-ttu-id="3048d-141">重複步驟 1-3，為「資深系統工程師」建立另一個標準職稱。</span><span class="sxs-lookup"><span data-stu-id="3048d-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![標準職稱實體的範例資料](media/ST-data.png)
