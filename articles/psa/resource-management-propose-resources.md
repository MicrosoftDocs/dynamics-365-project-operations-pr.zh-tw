---
title: 提案建議專案資源
description: 本主題提供有關如何提案建議專案資源的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 0a3eaa9929770c91523831d92744d5084aa28cb8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147508"
---
# <a name="propose-project-resources"></a><span data-ttu-id="517f6-103">提案建議專案資源</span><span class="sxs-lookup"><span data-stu-id="517f6-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="517f6-104">資源管理員可以使用資源要求，提案向專案經理建議資源。</span><span class="sxs-lookup"><span data-stu-id="517f6-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="517f6-105">從要求網格或要求本身中選取 **尋找資源**。</span><span class="sxs-lookup"><span data-stu-id="517f6-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="517f6-106">在 **排程小幫手** 頁面上，選取資源，然後在 **建立資源預約** 窗格的 **預約狀態** 欄位中選取 **預約**。</span><span class="sxs-lookup"><span data-stu-id="517f6-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![提案的資源已選取](media/Resource-Management-image62.png)

<span data-ttu-id="517f6-108">發生下列狀態更新：</span><span class="sxs-lookup"><span data-stu-id="517f6-108">The following status updates occur:</span></span>

- <span data-ttu-id="517f6-109">在 **排程小幫手** 頁面上，狀態指示器會更新，以指定該預約是提案所建議，而不是已確認預約。</span><span class="sxs-lookup"><span data-stu-id="517f6-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![排程小幫手頁面上提案的預約的狀態指示器](media/Resource-Management-image63.png)

- <span data-ttu-id="517f6-111">在資源要求上，狀態已變更為 **需要檢閱**。</span><span class="sxs-lookup"><span data-stu-id="517f6-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![資源要求狀態已變更為 [需要檢閱]。](media/Resource-Management-image64.png)

- <span data-ttu-id="517f6-113">在專案的 **團隊** 索引標籤上，一般團隊成員的 **要求狀態** 值會變更為 **需要檢閱**。</span><span class="sxs-lookup"><span data-stu-id="517f6-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![一般團隊成員的要求狀態在 [團隊] 索引標籤上已變更為 [需要檢閱]。](media/Resource-Management-image48.png)

<span data-ttu-id="517f6-115">專案經理可以接受或拒絕提案。</span><span class="sxs-lookup"><span data-stu-id="517f6-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="517f6-116">資源經理處理資源要求時，可以使用下列任一方法：</span><span class="sxs-lookup"><span data-stu-id="517f6-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="517f6-117">如果沒有單一資源可用來履行需要的時數，請提案建議多個資源以滿足需求。</span><span class="sxs-lookup"><span data-stu-id="517f6-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="517f6-118">提案的時數隨後會在多個可滿足所需時數的資源間進行分割。</span><span class="sxs-lookup"><span data-stu-id="517f6-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="517f6-119">在此案例中，時數不能重疊。</span><span class="sxs-lookup"><span data-stu-id="517f6-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="517f6-120">提案建議比所需資源還要少的資源。</span><span class="sxs-lookup"><span data-stu-id="517f6-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="517f6-121">在此案例中，提案的資源產能小於要求者所指定的需要時數。</span><span class="sxs-lookup"><span data-stu-id="517f6-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="517f6-122">因此，當要求者接受提案的資源時，就會建立未履行資源需求，以擷取剩餘的索求。</span><span class="sxs-lookup"><span data-stu-id="517f6-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="517f6-123">如果沒有單一資源可用來完成工作，請預約建議多個資源以滿足索求。</span><span class="sxs-lookup"><span data-stu-id="517f6-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="517f6-124">預約比所需資源還要少的資源。</span><span class="sxs-lookup"><span data-stu-id="517f6-124">Book fewer resources than are required.</span></span> <span data-ttu-id="517f6-125">在此案例中，預約的工時少於需要的時數。</span><span class="sxs-lookup"><span data-stu-id="517f6-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="517f6-126">系統會引導您提案建議的是資源而不是預約，這樣要求者才能驗證並追蹤剩餘的索求。</span><span class="sxs-lookup"><span data-stu-id="517f6-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="517f6-127">計費使用率</span><span class="sxs-lookup"><span data-stu-id="517f6-127">Billable utilization</span></span>

<span data-ttu-id="517f6-128">資源可以有目標計費使用率。</span><span class="sxs-lookup"><span data-stu-id="517f6-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="517f6-129">此目標使用率會定義為資源預設角色的屬性，或是透過個別可預約資源的記錄來設定。</span><span class="sxs-lookup"><span data-stu-id="517f6-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="517f6-130">使用率計算是根據資源使用核准的時間項目所報告的實際時數來進行。</span><span class="sxs-lookup"><span data-stu-id="517f6-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="517f6-131">下列公式用於計算使用率：</span><span class="sxs-lookup"><span data-stu-id="517f6-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="517f6-132">計費使用率 = 應收費實際時數 ÷ 資源產能</span><span class="sxs-lookup"><span data-stu-id="517f6-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="517f6-133">非計費使用率 = 帳單類型識別碼為 [不應收費]、[附贈] 或 [不適用] 的實際時間 ÷ 資源產能</span><span class="sxs-lookup"><span data-stu-id="517f6-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="517f6-134">內部 = 無銷售合約的實際時間 ÷ 資源產能</span><span class="sxs-lookup"><span data-stu-id="517f6-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="517f6-135">資源產能 = 資源工作時數 – 不在辦公室 – 非工作天數</span><span class="sxs-lookup"><span data-stu-id="517f6-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="517f6-136">您可以在 **資源** 窗格中找到 **資源使用率** 檢視表。</span><span class="sxs-lookup"><span data-stu-id="517f6-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![資源使用率檢視表](media/Resource-Management-image65.png)

<span data-ttu-id="517f6-138">網格中的每個儲存格表示一個週期 (例如日、週或月) 中資源的計費使用率百分比。</span><span class="sxs-lookup"><span data-stu-id="517f6-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="517f6-139">下列公式用於設定儲存格的色彩：</span><span class="sxs-lookup"><span data-stu-id="517f6-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="517f6-140">**綠色：** 計費使用率 \>= 資源目標使用率</span><span class="sxs-lookup"><span data-stu-id="517f6-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="517f6-141">**黃色：** 目標使用率 – 20 \<= 計費使用率 \< 目標使用率</span><span class="sxs-lookup"><span data-stu-id="517f6-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="517f6-142">**紅色：** 計費使用率 \< 目標使用率 – 20。</span><span class="sxs-lookup"><span data-stu-id="517f6-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="517f6-143">因為 **資源使用率** 檢視表以排程面板為基礎，所以您可以使用排程面板的篩選功能來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="517f6-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="517f6-144">網格要求您必須對角色或個別資源設定目標使用率。</span><span class="sxs-lookup"><span data-stu-id="517f6-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="517f6-145">若要進行此設定，請移至 **資源** \> **資源角色**。</span><span class="sxs-lookup"><span data-stu-id="517f6-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="517f6-146">此外，還必須將預設角色指派給每個可預約資源。</span><span class="sxs-lookup"><span data-stu-id="517f6-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="517f6-147">移至 **資源** \> **資源**。</span><span class="sxs-lookup"><span data-stu-id="517f6-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="517f6-148">在 **Project Service** 索引標籤上，確認已定義資源角色，且該角色的 **是預設值** 欄位已設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="517f6-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="517f6-149">您可以新增其他角色，其中 **是預設值 = 否**。</span><span class="sxs-lookup"><span data-stu-id="517f6-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="517f6-150">**是預設值 = 是** 的角色會用來對照該角色的目標來評估資源的使用率。</span><span class="sxs-lookup"><span data-stu-id="517f6-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![預設角色已設定](media/Resource-Management-image67.png)

<span data-ttu-id="517f6-152">在 **Project Service** 索引標籤上，您也可以設定資源的個別目標使用率。</span><span class="sxs-lookup"><span data-stu-id="517f6-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="517f6-153">使用率計算接著會使用該目標使用率來評估資源的目標，而不是資源預設角色的目標。</span><span class="sxs-lookup"><span data-stu-id="517f6-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="517f6-154">只有當資源在網格所顯示週期內有獲核准的應收費時間時，才會顯示資源的使用率。</span><span class="sxs-lookup"><span data-stu-id="517f6-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="517f6-155">資源可用性</span><span class="sxs-lookup"><span data-stu-id="517f6-155">Resource availability</span></span>

<span data-ttu-id="517f6-156">資源管理員要能夠檢視資源可用性並更新預約，至關重要。</span><span class="sxs-lookup"><span data-stu-id="517f6-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="517f6-157">在某些情況下，沒有正式索求 (資源要求)，但是資源管理員必須回應來自電子郵件、通話或立即訊息等管道的計劃外索求。</span><span class="sxs-lookup"><span data-stu-id="517f6-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="517f6-158">資源管理員會使用排程面板來更新資源和預約。</span><span class="sxs-lookup"><span data-stu-id="517f6-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="517f6-159">資源工作時數會用來做為計算資源可用性的基準。</span><span class="sxs-lookup"><span data-stu-id="517f6-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="517f6-160">資源預約會耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="517f6-160">Resource bookings consume the capacity of the resources.</span></span>

![排程面板](media/Resource-Management-image68.png)

<span data-ttu-id="517f6-162">排程面板使用色彩與陰影來顯示預約、可用性和過量預約，以及預約的狀態。</span><span class="sxs-lookup"><span data-stu-id="517f6-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="517f6-163">排程面板中的設定可讓您顯示圖例。</span><span class="sxs-lookup"><span data-stu-id="517f6-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="517f6-164">如果排程面板上的個別可預約資源旁邊出現向右箭頭，則可以展開資源來顯示該資源所預約之工作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="517f6-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![排程面板上已展開的可預約資源](media/Resource-Management-image69.png)

<span data-ttu-id="517f6-166">因為 Dynamics 365 Project Service Automation 使用 Universal Resource Scheduling 引擎，如果您也已安裝 Dynamics 365 Field Service，則可以檢視專案、工單以及任何其他您已給予排程之實體的資源預約詳細資料。</span><span class="sxs-lookup"><span data-stu-id="517f6-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![專案和工單的資源預約詳細資料](media/Resource-Management-image70.png)

<span data-ttu-id="517f6-168">若要檢視更多關於個別資源的詳細資料，請在其上按滑鼠右鍵以開啟資源卡片。</span><span class="sxs-lookup"><span data-stu-id="517f6-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![資源卡片](media/Resource-Management-image71.png)
