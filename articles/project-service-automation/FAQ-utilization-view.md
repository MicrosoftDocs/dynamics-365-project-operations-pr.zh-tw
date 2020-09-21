---
title: 檢視資源的應收費使用率
description: 本主題提供有關資源使用率檢視表的資訊。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749863"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="90ec5-103">檢視資源的應收費使用率</span><span class="sxs-lookup"><span data-stu-id="90ec5-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="90ec5-104">**Project Service 資源使用率**頁面上的**使用率檢視表**會顯示每個可預約資源的應收費使用率。</span><span class="sxs-lookup"><span data-stu-id="90ec5-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="90ec5-105">檢視表是以排程面板為基礎所建立，因此您會發現許多相同的功能。</span><span class="sxs-lookup"><span data-stu-id="90ec5-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![使用率檢視表的螢幕擷取畫面](media/FAQ-utilization-1.png)
 

<span data-ttu-id="90ec5-107">應收費使用率計算依下列方式運作：</span><span class="sxs-lookup"><span data-stu-id="90ec5-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="90ec5-108">應收費使用率 = (應收費實際時數) / (資源產能)</span><span class="sxs-lookup"><span data-stu-id="90ec5-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="90ec5-109">儲存格表示所選期間 (日、週或月) 的已計算應收費使用率。</span><span class="sxs-lookup"><span data-stu-id="90ec5-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="90ec5-110">每個儲存格中的色彩顯示資源相較於其目標應收費使用率的應收費使用率。</span><span class="sxs-lookup"><span data-stu-id="90ec5-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="90ec5-111">您可以在資源的預設角色或個別資源本身設定目標使用率。</span><span class="sxs-lookup"><span data-stu-id="90ec5-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="90ec5-112">計算會先查看個別資源以取得目標，然後參考資源的預設角色。</span><span class="sxs-lookup"><span data-stu-id="90ec5-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="90ec5-113">對資源設定目標</span><span class="sxs-lookup"><span data-stu-id="90ec5-113">Set target on a resource</span></span>

1. <span data-ttu-id="90ec5-114">移至**資源** \> **資源**。</span><span class="sxs-lookup"><span data-stu-id="90ec5-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="90ec5-115">選取要開啟記錄的資源。</span><span class="sxs-lookup"><span data-stu-id="90ec5-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="90ec5-116">在 **Project Service** 索引標籤上，您可以設定資源的目標使用率。</span><span class="sxs-lookup"><span data-stu-id="90ec5-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![使用 [Project Service] 索引標籤設定目標使用率的螢幕擷取畫面](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="90ec5-118">設定角色的目標使用率</span><span class="sxs-lookup"><span data-stu-id="90ec5-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="90ec5-119">移至**資源**\>**資源角色**。</span><span class="sxs-lookup"><span data-stu-id="90ec5-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="90ec5-120">選取角色並開啟記錄。</span><span class="sxs-lookup"><span data-stu-id="90ec5-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="90ec5-121">設定角色的目標使用率。</span><span class="sxs-lookup"><span data-stu-id="90ec5-121">Set the target utilization for the role.</span></span>

> ![使用 [資源角色] 設定目標使用率的螢幕擷取畫面](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="90ec5-123">計算資源的應收費使用率</span><span class="sxs-lookup"><span data-stu-id="90ec5-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="90ec5-124">若要計算資源的應收費使用率，您必須完成一些先決條件。</span><span class="sxs-lookup"><span data-stu-id="90ec5-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="90ec5-125">設定個別資源的預設角色</span><span class="sxs-lookup"><span data-stu-id="90ec5-125">Set default role for individual resource</span></span>

<span data-ttu-id="90ec5-126">首先，必須對個別資源或資源角色設定目標使用率。</span><span class="sxs-lookup"><span data-stu-id="90ec5-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="90ec5-127">如果您使用資源角色設定目標，則每項個別資源都必須有預設角色。</span><span class="sxs-lookup"><span data-stu-id="90ec5-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="90ec5-128">若要進行此設定，請移至**資源**\>**資源**。</span><span class="sxs-lookup"><span data-stu-id="90ec5-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="90ec5-129">選取資源、開啟記錄，然後選取 **Project Service** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="90ec5-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="90ec5-130">在**資源角色**網格中，確定資源有一個角色，且**是預設值**已設定為**是**。</span><span class="sxs-lookup"><span data-stu-id="90ec5-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="90ec5-131">變更資源角色的帳單類型</span><span class="sxs-lookup"><span data-stu-id="90ec5-131">Change billing type for resource role</span></span>

<span data-ttu-id="90ec5-132">必須設定資源角色，才會有**應收費**的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="90ec5-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="90ec5-133">移至**資源**\>**資源角色**。</span><span class="sxs-lookup"><span data-stu-id="90ec5-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="90ec5-134">開啟要更新的記錄，然後將帳單類型設定為**應收費**。</span><span class="sxs-lookup"><span data-stu-id="90ec5-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="90ec5-135">設定資源角色的工作時數</span><span class="sxs-lookup"><span data-stu-id="90ec5-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="90ec5-136">資源必須有工作時數，才能計算產能。</span><span class="sxs-lookup"><span data-stu-id="90ec5-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="90ec5-137">移至**資源** \> **資源**。</span><span class="sxs-lookup"><span data-stu-id="90ec5-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="90ec5-138">選取要開啟記錄的資源，然後選取**顯示工作時數**。</span><span class="sxs-lookup"><span data-stu-id="90ec5-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="90ec5-139">您可套用**資源清單**檢視表的**工作時數範本**，以大量更新資源清單。</span><span class="sxs-lookup"><span data-stu-id="90ec5-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="90ec5-140">應收費實際時數疑難排解</span><span class="sxs-lookup"><span data-stu-id="90ec5-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="90ec5-141">應收費實際時數的來源是**實際值**實體。</span><span class="sxs-lookup"><span data-stu-id="90ec5-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="90ec5-142">帳單類型為**應收費**的實際值會納入計算，因此您必須有實際值為應收費的專案。</span><span class="sxs-lookup"><span data-stu-id="90ec5-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="90ec5-143">如果您沒有看到應收費使用率，以下是一些您可以檢查的項目：</span><span class="sxs-lookup"><span data-stu-id="90ec5-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="90ec5-144">資源有針對產能所定義的工作時數。</span><span class="sxs-lookup"><span data-stu-id="90ec5-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="90ec5-145">資源有個別定義的使用率目標，或是有指派給它的預設角色。</span><span class="sxs-lookup"><span data-stu-id="90ec5-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="90ec5-146">角色有其定義的使用率目標。</span><span class="sxs-lookup"><span data-stu-id="90ec5-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="90ec5-147">實際值在您預期要進行使用率計算的期間有**應收費**的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="90ec5-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="90ec5-148">如果您看到帳單類型為 [應收費] 以外類型的實際值，請檢查下列項目：</span><span class="sxs-lookup"><span data-stu-id="90ec5-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="90ec5-149">實際值上使用的角色有 [應收費] 以外的預設計費類型。</span><span class="sxs-lookup"><span data-stu-id="90ec5-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="90ec5-150">支援專案的專案合約服務內容上的角色已設定為不應收費。</span><span class="sxs-lookup"><span data-stu-id="90ec5-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="90ec5-151">專案沒有相關聯的合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="90ec5-151">The project does not have an associated contract line.</span></span>

