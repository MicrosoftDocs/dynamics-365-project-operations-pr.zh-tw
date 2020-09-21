---
title: 建立自訂欄位和實體
description: 本主題說明如何在 Power Apps 平台建立自己解決方案中的選項組與實體。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749980"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="7e86b-103">建立自訂欄位和實體</span><span class="sxs-lookup"><span data-stu-id="7e86b-103">Create custom fields and entities</span></span> 

<span data-ttu-id="7e86b-104">每當您想要在 Power Apps 平台建立自訂選項組或實體時，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="7e86b-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="7e86b-105">本主題中的程序應使用 Project Service Automation (PSA) 的 Web 介面來完成。</span><span class="sxs-lookup"><span data-stu-id="7e86b-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e86b-106">建議您在不同的解決方案中進行所有自訂定價維度變更。</span><span class="sxs-lookup"><span data-stu-id="7e86b-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="7e86b-107">這個重要的最佳做法提供您日後視需要更新或移除變更的彈性、有助於重複使用您的工作，以及讓您更便於將這些變更移植到另一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="7e86b-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="7e86b-108">進行所有必要變更之後，將此解決方案匯出為**受管理的解決方案**，再將其匯入至其他執行個體，即可重複使用您的定價設定。</span><span class="sxs-lookup"><span data-stu-id="7e86b-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="7e86b-109">建立自訂定價維度解決方案</span><span class="sxs-lookup"><span data-stu-id="7e86b-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="7e86b-110">在 PSA 中，按一下**設定** > **解決方案**，然後按一下**新增**建立新的解決方案。</span><span class="sxs-lookup"><span data-stu-id="7e86b-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="7e86b-111">將解決方案命名為 **\<您的組織名稱> 定價維度**、輸入其餘必要資訊，然後按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![建立自訂定價維度解決方案](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="7e86b-113">在定價維度解決方案中建立自訂欄位及選項組</span><span class="sxs-lookup"><span data-stu-id="7e86b-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="7e86b-114">定價維度可以是選項組或實體。</span><span class="sxs-lookup"><span data-stu-id="7e86b-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="7e86b-115">兩者預必須在定價解決方案中建立。</span><span class="sxs-lookup"><span data-stu-id="7e86b-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="7e86b-116">此程序中的步驟說明如何建立以實體為準的維度和以選項組為準的維度。</span><span class="sxs-lookup"><span data-stu-id="7e86b-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="7e86b-117">以實體為準的維度</span><span class="sxs-lookup"><span data-stu-id="7e86b-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="7e86b-118">在PSA 中，按一下**設定** > **解決方案**，然後按兩下 **\<您的組織名稱> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="7e86b-119">在方案總管的左導覽窗格中，選取**實體**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="7e86b-120">按一下**新增**建立名為**標準職稱**的新實體。</span><span class="sxs-lookup"><span data-stu-id="7e86b-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="7e86b-121">輸入其餘必要資訊，然後按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![標準職稱實體定義](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="7e86b-123">以選項組為準的維度</span><span class="sxs-lookup"><span data-stu-id="7e86b-123">Option set-based dimensions</span></span> 
<span data-ttu-id="7e86b-124">您可以建立兩個以選項組為準的維度。</span><span class="sxs-lookup"><span data-stu-id="7e86b-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="7e86b-125">使用**資源工作地點**來追蹤**住家**地點工作和**現場**工作的價格，以及使用**資源工作時數**搭配**正常工時**和**加班工時**值，在工作完成時套用加成。</span><span class="sxs-lookup"><span data-stu-id="7e86b-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="7e86b-126">在PSA 中，按一下**設定** > **解決方案**，然後按兩下 **\<您的組織名稱> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="7e86b-127">在方案總管的左導覽窗格中，選取**選項組**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="7e86b-128">按一下**新增**建立新的選項組、輸入其餘必要資訊，然後按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="7e86b-129">以選項組為準的定價維度，名為「資源工作地點」</span><span class="sxs-lookup"><span data-stu-id="7e86b-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="7e86b-130">以選項組為準的定價維度，名為「資源工作時數」</span><span class="sxs-lookup"><span data-stu-id="7e86b-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="7e86b-131">建立以實體為準維度的資料</span><span class="sxs-lookup"><span data-stu-id="7e86b-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="7e86b-132">您可以手動建立以實體為準維度的資料，或是使用 Microsoft Excel 匯入或服務通話來建立此資料</span><span class="sxs-lookup"><span data-stu-id="7e86b-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="7e86b-133">使用此程序中的步驟，從以實體為準的維度**標準職稱**建立兩個標準職稱**系統工程師**和**資深系統工程師**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="7e86b-134">如果要建立的資料不大 (如下列範例所示)，您可以使用標準表單。</span><span class="sxs-lookup"><span data-stu-id="7e86b-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="7e86b-135">在 PSA, 中，按一下**進階尋找**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="7e86b-136">選取**標準職稱**實體，然後按一下**結果**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="7e86b-137">將會顯示**標準職稱**實體中所有的列。</span><span class="sxs-lookup"><span data-stu-id="7e86b-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="7e86b-138">按一下 **新增**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-138">Click **New**.</span></span> <span data-ttu-id="7e86b-139">在**名稱**欄位中輸入「系統工程師」，然後按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="7e86b-140">關閉表單。</span><span class="sxs-lookup"><span data-stu-id="7e86b-140">Close the form.</span></span> 
4. <span data-ttu-id="7e86b-141">重複步驟 1-3，為「資深系統工程師」建立另一個標準職稱。</span><span class="sxs-lookup"><span data-stu-id="7e86b-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="7e86b-142">標準職稱實體的範例資料</span><span class="sxs-lookup"><span data-stu-id="7e86b-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="7e86b-143">將所有必要的 PSA 實體及相關元件新增至定價維度解決方案</span><span class="sxs-lookup"><span data-stu-id="7e86b-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="7e86b-144">您必須將下列 Project Service 實體新增至您的定價方案。</span><span class="sxs-lookup"><span data-stu-id="7e86b-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="7e86b-145">使用此程序中的步驟，在定價方案中進行一些重要的結構描述變更，讓實體得知新的定價維度。</span><span class="sxs-lookup"><span data-stu-id="7e86b-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="7e86b-146">在PSA 中，按一下**設定** > **解決方案**，然後按兩下 **\<您的組織名稱> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="7e86b-147">在方案總管的左導覽窗格中，選取**新增現有的** >  **實體**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="7e86b-148">在**解決方案元件**對話方塊中，選取下列實體：</span><span class="sxs-lookup"><span data-stu-id="7e86b-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="7e86b-149">實際</span><span class="sxs-lookup"><span data-stu-id="7e86b-149">Actual</span></span>
- <span data-ttu-id="7e86b-150">可預約資源</span><span class="sxs-lookup"><span data-stu-id="7e86b-150">Bookable Resource</span></span>
- <span data-ttu-id="7e86b-151">估計明細</span><span class="sxs-lookup"><span data-stu-id="7e86b-151">Estimate Line</span></span>
- <span data-ttu-id="7e86b-152">發票明細詳細資料</span><span class="sxs-lookup"><span data-stu-id="7e86b-152">Invoice Line Detail</span></span>
- <span data-ttu-id="7e86b-153">帳目明細</span><span class="sxs-lookup"><span data-stu-id="7e86b-153">Journal Line</span></span>
- <span data-ttu-id="7e86b-154">專案合約服務內容詳細資料</span><span class="sxs-lookup"><span data-stu-id="7e86b-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="7e86b-155">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="7e86b-155">Project Team Member</span></span>
- <span data-ttu-id="7e86b-156">報價明細詳細資料</span><span class="sxs-lookup"><span data-stu-id="7e86b-156">Quote Line Detail</span></span>
- <span data-ttu-id="7e86b-157">角色價格加成</span><span class="sxs-lookup"><span data-stu-id="7e86b-157">Role Price Markup</span></span>
- <span data-ttu-id="7e86b-158">角色價格</span><span class="sxs-lookup"><span data-stu-id="7e86b-158">Role Price</span></span> 
- <span data-ttu-id="7e86b-159">時間項目</span><span class="sxs-lookup"><span data-stu-id="7e86b-159">Time Entry</span></span> 

> ![將現有實體新增至定價維度解決方案](media/Existing-entities-to-PD-solution.png)

> ![選取解決方案元件](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="7e86b-162">請務必包含所選每個實體的所有表單和檢視表。</span><span class="sxs-lookup"><span data-stu-id="7e86b-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="7e86b-163">當系統提示您包含上述所選實體的任何相依實體時，按一下**否**。</span><span class="sxs-lookup"><span data-stu-id="7e86b-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![不要包括所有相關元件。](media/Do-not-include-required.png)


