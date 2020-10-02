---
title: 檢閱提案的資源
description: 本主題提供有關如何提案建議專案資源的資訊。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897351"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="cb11f-103">檢閱提案的資源</span><span class="sxs-lookup"><span data-stu-id="cb11f-103">Review proposed resources</span></span>

<span data-ttu-id="cb11f-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="cb11f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cb11f-105">資源管理員可以使用資源要求，提案向專案經理建議資源。</span><span class="sxs-lookup"><span data-stu-id="cb11f-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="cb11f-106">從要求網格或要求本身中選取**尋找資源**。</span><span class="sxs-lookup"><span data-stu-id="cb11f-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="cb11f-107">在**排程小幫手**頁面上，選取資源，然後在**建立資源預約**窗格的**預約狀態**欄位中選取**預約**。</span><span class="sxs-lookup"><span data-stu-id="cb11f-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="cb11f-108">發生下列狀態更新：</span><span class="sxs-lookup"><span data-stu-id="cb11f-108">The following status updates occur:</span></span>

- <span data-ttu-id="cb11f-109">在**排程小幫手**頁面上，狀態指示器會更新，以指定該預約是提案所建議，而不是已確認預約。</span><span class="sxs-lookup"><span data-stu-id="cb11f-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="cb11f-110">在資源要求上，狀態已變更為**需要檢閱**。</span><span class="sxs-lookup"><span data-stu-id="cb11f-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="cb11f-111">在專案的**團隊**索引標籤上，一般團隊成員的**要求狀態**值會變更為**需要檢閱**。</span><span class="sxs-lookup"><span data-stu-id="cb11f-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="cb11f-112">專案經理可以接受或拒絕提案。</span><span class="sxs-lookup"><span data-stu-id="cb11f-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="cb11f-113">資源經理處理資源要求時，可以使用下列任一方法：</span><span class="sxs-lookup"><span data-stu-id="cb11f-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="cb11f-114">如果沒有單一資源可用來履行需要的時數，請提案建議多個資源以滿足需求。</span><span class="sxs-lookup"><span data-stu-id="cb11f-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="cb11f-115">提案的時數隨後會在多個可滿足所需時數的資源間進行分割。</span><span class="sxs-lookup"><span data-stu-id="cb11f-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="cb11f-116">在此案例中，時數不能重疊。</span><span class="sxs-lookup"><span data-stu-id="cb11f-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="cb11f-117">提案建議比所需資源還要少的資源。</span><span class="sxs-lookup"><span data-stu-id="cb11f-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="cb11f-118">在此案例中，提案的資源產能小於要求者所指定的需要時數。</span><span class="sxs-lookup"><span data-stu-id="cb11f-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="cb11f-119">因此，當要求者接受提案的資源時，就會建立未履行資源需求，以擷取剩餘的索求。</span><span class="sxs-lookup"><span data-stu-id="cb11f-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="cb11f-120">如果沒有單一資源可用來完成工作，請預約建議多個資源以滿足索求。</span><span class="sxs-lookup"><span data-stu-id="cb11f-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="cb11f-121">預約比所需資源還要少的資源。</span><span class="sxs-lookup"><span data-stu-id="cb11f-121">Book fewer resources than are required.</span></span> <span data-ttu-id="cb11f-122">在此案例中，預約的工時少於需要的時數。</span><span class="sxs-lookup"><span data-stu-id="cb11f-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="cb11f-123">系統會引導您提案建議的是資源而不是預約，這樣要求者才能驗證並追蹤剩餘的索求。</span><span class="sxs-lookup"><span data-stu-id="cb11f-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="cb11f-124">計費使用率</span><span class="sxs-lookup"><span data-stu-id="cb11f-124">Billable utilization</span></span>

<span data-ttu-id="cb11f-125">資源可以有目標計費使用率。</span><span class="sxs-lookup"><span data-stu-id="cb11f-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="cb11f-126">此目標使用率會定義為資源預設角色的屬性，或是透過個別可預約資源的記錄來設定。</span><span class="sxs-lookup"><span data-stu-id="cb11f-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="cb11f-127">使用率計算是根據資源使用核准的時間項目所報告的實際時數來進行。</span><span class="sxs-lookup"><span data-stu-id="cb11f-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="cb11f-128">下列公式用於計算使用率：</span><span class="sxs-lookup"><span data-stu-id="cb11f-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="cb11f-129">計費使用率 = 應收費實際時數 ÷ 資源產能</span><span class="sxs-lookup"><span data-stu-id="cb11f-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="cb11f-130">非計費使用率 = 帳單類型識別碼為 [不應收費]、[附贈] 或 [不適用] 的實際時間 ÷ 資源產能</span><span class="sxs-lookup"><span data-stu-id="cb11f-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="cb11f-131">內部 = 無銷售合約的實際時間 ÷ 資源產能</span><span class="sxs-lookup"><span data-stu-id="cb11f-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="cb11f-132">資源產能 = 資源工作時數 – 不在辦公室 – 非工作天數</span><span class="sxs-lookup"><span data-stu-id="cb11f-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="cb11f-133">您可以在**資源**窗格中找到**資源使用率**檢視表。</span><span class="sxs-lookup"><span data-stu-id="cb11f-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="cb11f-134">網格中的每個儲存格表示一個週期 (例如日、週或月) 中資源的計費使用率百分比。</span><span class="sxs-lookup"><span data-stu-id="cb11f-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="cb11f-135">下列公式用於設定儲存格的色彩：</span><span class="sxs-lookup"><span data-stu-id="cb11f-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="cb11f-136">**綠色：** 計費使用率 \>= 資源目標使用率</span><span class="sxs-lookup"><span data-stu-id="cb11f-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="cb11f-137">**黃色：** 目標使用率 – 20 \<= 計費使用率 \< 目標使用率</span><span class="sxs-lookup"><span data-stu-id="cb11f-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="cb11f-138">**紅色：** 計費使用率 \< 目標使用率 – 20。</span><span class="sxs-lookup"><span data-stu-id="cb11f-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="cb11f-139">因為**資源使用率**檢視表以排程面板為基礎，所以您可以使用排程面板的篩選功能來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="cb11f-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="cb11f-140">網格要求您必須對角色或個別資源設定目標使用率。</span><span class="sxs-lookup"><span data-stu-id="cb11f-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="cb11f-141">若要進行此設定，請移至**資源** \> **資源角色**。</span><span class="sxs-lookup"><span data-stu-id="cb11f-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="cb11f-142">此外，還必須將預設角色指派給每個可預約資源。</span><span class="sxs-lookup"><span data-stu-id="cb11f-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="cb11f-143">移至**資源** \> **資源**。</span><span class="sxs-lookup"><span data-stu-id="cb11f-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="cb11f-144">在 **Project Service** 索引標籤上，確認已定義資源角色，且該角色的**是預設值**欄位已設定為**是**。</span><span class="sxs-lookup"><span data-stu-id="cb11f-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="cb11f-145">您可以新增其他角色，其中**是預設值 = 否**。</span><span class="sxs-lookup"><span data-stu-id="cb11f-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="cb11f-146">**是預設值 = 是**的角色會用來對照該角色的目標來評估資源的使用率。</span><span class="sxs-lookup"><span data-stu-id="cb11f-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="cb11f-147">在 **Project Service** 索引標籤上，您也可以設定資源的個別目標使用率。</span><span class="sxs-lookup"><span data-stu-id="cb11f-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="cb11f-148">使用率計算接著會使用該目標使用率來評估資源的目標，而不是資源預設角色的目標。</span><span class="sxs-lookup"><span data-stu-id="cb11f-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="cb11f-149">只有當資源在網格所顯示週期內有獲核准的應收費時間時，才會顯示資源的使用率。</span><span class="sxs-lookup"><span data-stu-id="cb11f-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="cb11f-150">資源可用性</span><span class="sxs-lookup"><span data-stu-id="cb11f-150">Resource availability</span></span>

<span data-ttu-id="cb11f-151">資源管理員要能夠檢視資源可用性並更新預約，至關重要。</span><span class="sxs-lookup"><span data-stu-id="cb11f-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="cb11f-152">在某些情況下，沒有正式索求 (資源要求)，但是資源管理員必須回應來自電子郵件、通話或立即訊息等管道的計劃外索求。</span><span class="sxs-lookup"><span data-stu-id="cb11f-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="cb11f-153">資源管理員會使用排程面板來更新資源和預約。</span><span class="sxs-lookup"><span data-stu-id="cb11f-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="cb11f-154">資源工作時數會用來做為計算資源可用性的基準。</span><span class="sxs-lookup"><span data-stu-id="cb11f-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="cb11f-155">資源預約會耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="cb11f-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="cb11f-156">排程面板使用色彩與陰影來顯示預約、可用性和過量預約，以及預約的狀態。</span><span class="sxs-lookup"><span data-stu-id="cb11f-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="cb11f-157">排程面板中的設定可讓您顯示圖例。</span><span class="sxs-lookup"><span data-stu-id="cb11f-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="cb11f-158">如果排程面板上的個別可預約資源旁邊出現向右箭頭，則可以展開資源來顯示該資源所預約之工作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cb11f-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="cb11f-159">因為 Dynamics 365 Project Operations 使用 Universal Resource Scheduling 引擎，如果您也已安裝 Dynamics 365 Field Service，則可以檢視專案、工單以及任何其他您已將排程功能擴展至之實體的資源預約詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cb11f-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="cb11f-160">若要檢視更多關於個別資源的詳細資料，請在其上按滑鼠右鍵以開啟資源卡片。</span><span class="sxs-lookup"><span data-stu-id="cb11f-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

