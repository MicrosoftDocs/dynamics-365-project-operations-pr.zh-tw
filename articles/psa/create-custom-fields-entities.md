---
title: 建立自訂欄位和實體
description: 本主題說明如何在 Power Apps 平台建立自己解決方案中的選項組與實體。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290517"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="ac7ca-103">建立自訂欄位和實體</span><span class="sxs-lookup"><span data-stu-id="ac7ca-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ac7ca-104">每當您想要在 Power Apps 平台建立自訂選項組或實體時，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="ac7ca-105">本主題中的程序應使用 Project Service Automation (PSA) 的 Web 介面來完成。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac7ca-106">建議您在不同的解決方案中進行所有自訂定價維度變更。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="ac7ca-107">這個重要的最佳做法提供您日後視需要更新或移除變更的彈性、有助於重複使用您的工作，以及讓您更便於將這些變更移植到另一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="ac7ca-108">進行所有必要變更之後，將此解決方案匯出為 **受管理的解決方案**，再將其匯入至其他執行個體，即可重複使用您的定價設定。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="ac7ca-109">在定價維度解決方案中建立自訂欄位及選項組</span><span class="sxs-lookup"><span data-stu-id="ac7ca-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="ac7ca-110">定價維度可以是選項組或實體。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="ac7ca-111">兩者預必須在定價解決方案中建立。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="ac7ca-112">此程序中的步驟說明如何建立以實體為準的維度和以選項組為準的維度。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="ac7ca-113">以實體為準的維度</span><span class="sxs-lookup"><span data-stu-id="ac7ca-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="ac7ca-114">在 PSA 中，按一下 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="ac7ca-115">在方案總管的左導覽窗格中，選取 **實體**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="ac7ca-116">按一下 **新增** 建立名為 **標準職稱** 的新實體。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="ac7ca-117">輸入其餘必要資訊，然後按一下 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![標準職稱實體定義](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="ac7ca-119">以選項組為準的維度</span><span class="sxs-lookup"><span data-stu-id="ac7ca-119">Option set-based dimensions</span></span> 
<span data-ttu-id="ac7ca-120">您可以建立兩個以選項組為準的維度。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="ac7ca-121">使用 **資源工作地點** 來追蹤 **住家** 地點工作和 **現場** 工作的價格，以及使用 **資源工作時數** 搭配 **正常工時** 和 **加班工時** 值，在工作完成時套用加成。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="ac7ca-122">在 PSA 中，按一下 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="ac7ca-123">在方案總管的左導覽窗格中，選取 **選項組**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="ac7ca-124">按一下 **新增** 建立新的選項組、輸入其餘必要資訊，然後按一下 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="ac7ca-125">以選項組為準的定價維度，名為「資源工作地點」</span><span class="sxs-lookup"><span data-stu-id="ac7ca-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="ac7ca-126">以選項組為準的定價維度，名為「資源工作時數」</span><span class="sxs-lookup"><span data-stu-id="ac7ca-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="ac7ca-127">建立以實體為準維度的資料</span><span class="sxs-lookup"><span data-stu-id="ac7ca-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="ac7ca-128">您可以手動建立以實體為準維度的資料，或是使用 Microsoft Excel 匯入或服務通話來建立此資料</span><span class="sxs-lookup"><span data-stu-id="ac7ca-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="ac7ca-129">使用此程序中的步驟，從以實體為準的維度 **標準職稱** 建立兩個標準職稱 **系統工程師** 和 **資深系統工程師**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="ac7ca-130">如果要建立的資料不大 (如下列範例所示)，您可以使用標準表單。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="ac7ca-131">在 PSA, 中，按一下 **進階尋找**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="ac7ca-132">選取 **標準職稱** 實體，然後按一下 **結果**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="ac7ca-133">將會顯示 **標準職稱** 實體中所有的列。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="ac7ca-134">按一下 **新增**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-134">Click **New**.</span></span> <span data-ttu-id="ac7ca-135">在 **名稱** 欄位中輸入「系統工程師」，然後按一下 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="ac7ca-136">關閉表單。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-136">Close the form.</span></span> 
4. <span data-ttu-id="ac7ca-137">重複步驟 1-3，為「資深系統工程師」建立另一個標準職稱。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="ac7ca-138">標準職稱實體的範例資料</span><span class="sxs-lookup"><span data-stu-id="ac7ca-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]