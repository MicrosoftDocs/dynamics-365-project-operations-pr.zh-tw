---
title: 專案設定
description: 本主題提供有關專案管理設定的資訊。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073159"
---
# <a name="project-settings"></a><span data-ttu-id="4c601-103">專案設定</span><span class="sxs-lookup"><span data-stu-id="4c601-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4c601-104">使用下列設定來存取專案規劃功能。</span><span class="sxs-lookup"><span data-stu-id="4c601-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="4c601-105">工作範本</span><span class="sxs-lookup"><span data-stu-id="4c601-105">Work template</span></span>

<span data-ttu-id="4c601-106">為了建立專案排程，您會建立專案行事曆範本，以定義每天的工作時數以及所有公休日。</span><span class="sxs-lookup"><span data-stu-id="4c601-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="4c601-107">若要建立專案行事曆範本，您可以將工作範本與專案的 **行事曆範本** 欄位建立關聯。</span><span class="sxs-lookup"><span data-stu-id="4c601-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="4c601-108">依照下列步驟建立建立工作範本。</span><span class="sxs-lookup"><span data-stu-id="4c601-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="4c601-109">在 PSA 的左導覽窗格中，按一下 **資源** 。</span><span class="sxs-lookup"><span data-stu-id="4c601-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="4c601-110">在 **資源** 清單頁面上，開啟使用者記錄，然後選取 **顯示工作時數** 。</span><span class="sxs-lookup"><span data-stu-id="4c601-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="4c601-111">請確定您已允許瀏覽器頁面出現快顯。</span><span class="sxs-lookup"><span data-stu-id="4c601-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="4c601-112">這可讓您看到資源設定的工作時數。</span><span class="sxs-lookup"><span data-stu-id="4c601-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="4c601-113">在 **每月檢視表** 索引標籤中，按一下 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="4c601-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="4c601-114">有三個選項的清單會出現：</span><span class="sxs-lookup"><span data-stu-id="4c601-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="4c601-115">新增每週排程</span><span class="sxs-lookup"><span data-stu-id="4c601-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="4c601-116">一日工作行事曆</span><span class="sxs-lookup"><span data-stu-id="4c601-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="4c601-117">休假</span><span class="sxs-lookup"><span data-stu-id="4c601-117">Time Off</span></span>

> ![設定選項](media/project-13.png)

4. <span data-ttu-id="4c601-119">選取 **新增每週排程** ，然後設定此資源排程的選項。</span><span class="sxs-lookup"><span data-stu-id="4c601-119">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="4c601-120">您可以設定週期性每週排程、每天時數參數、公休日等等。</span><span class="sxs-lookup"><span data-stu-id="4c601-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="4c601-121">設定日期範圍、選取 **儲存** ，然後按一下 **關閉** 。</span><span class="sxs-lookup"><span data-stu-id="4c601-121">Set the date range, select **Save** , and then click **Close**.</span></span> 
6. <span data-ttu-id="4c601-122">返回 **資源** 清單頁面，並選取您設定其工作時數的資源。</span><span class="sxs-lookup"><span data-stu-id="4c601-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="4c601-123">選取 **設定行事曆為** 以設定工作範本。</span><span class="sxs-lookup"><span data-stu-id="4c601-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="4c601-124">在 **工作範本** 對話方塊中輸入工作範本的名稱，然後選取 **套用** 。</span><span class="sxs-lookup"><span data-stu-id="4c601-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="4c601-125">您現在可以將工作範本與專案行事曆範本建立關聯。</span><span class="sxs-lookup"><span data-stu-id="4c601-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="4c601-126">資源角色</span><span class="sxs-lookup"><span data-stu-id="4c601-126">Resource roles</span></span>

<span data-ttu-id="4c601-127">*資源角色* 一詞是指人員必須具備才能執行專案中一組特定工作的一組技能、專長和認證。</span><span class="sxs-lookup"><span data-stu-id="4c601-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="4c601-128">PSA 可讓您根據資源的關聯角色來為資源的時間估算成本並開單收費。</span><span class="sxs-lookup"><span data-stu-id="4c601-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="4c601-129">每個組織都必須使用 **Project Service** 功能表的左側導覽來設定這些角色。</span><span class="sxs-lookup"><span data-stu-id="4c601-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="4c601-130">每個組織都必須在 **使用中資源類別** 頁面上設定這些角色。</span><span class="sxs-lookup"><span data-stu-id="4c601-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="4c601-131">若要開啟此頁面，請選取左導覽窗格中的 **資源角色** 。</span><span class="sxs-lookup"><span data-stu-id="4c601-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="4c601-132">價目表</span><span class="sxs-lookup"><span data-stu-id="4c601-132">Price lists</span></span>

<span data-ttu-id="4c601-133">價目表可讓您針對組織中的資源角色、費用類別、產品及其他元素設定成本和售價。</span><span class="sxs-lookup"><span data-stu-id="4c601-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="4c601-134">設定必須為專案交付之工作的財務估計值之前，您應該建立支援成本和銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="4c601-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="4c601-135">在參數區段中，您也應該設定套用至所有於組織建立之專案的預設成本和銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="4c601-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="4c601-136">在 **使用中專案參數** 頁面上，確定您已設定預設成本和銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="4c601-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
