---
title: 檢閱提案的資源
description: 本主題提供有關如何提案建議專案資源的資訊。
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279263"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="6044e-103">檢閱提案的資源</span><span class="sxs-lookup"><span data-stu-id="6044e-103">Review proposed resources</span></span>

<span data-ttu-id="6044e-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="6044e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6044e-105">資源管理員可以使用資源要求，提案向專案經理建議資源。</span><span class="sxs-lookup"><span data-stu-id="6044e-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="6044e-106">從要求網格或要求本身中選取 **尋找資源**。</span><span class="sxs-lookup"><span data-stu-id="6044e-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="6044e-107">在 **排程小幫手** 頁面上，選取資源，然後在 **建立資源預約** 窗格的 **預約狀態** 欄位中選取 **預約**。</span><span class="sxs-lookup"><span data-stu-id="6044e-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="6044e-108">發生下列狀態更新：</span><span class="sxs-lookup"><span data-stu-id="6044e-108">The following status updates occur:</span></span>

- <span data-ttu-id="6044e-109">在 **排程小幫手** 頁面上，狀態指示器會更新，以指定該預約是提案所建議，而不是已確認預約。</span><span class="sxs-lookup"><span data-stu-id="6044e-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="6044e-110">在資源要求上，狀態已變更為 **需要檢閱**。</span><span class="sxs-lookup"><span data-stu-id="6044e-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="6044e-111">在專案的 **團隊** 索引標籤上，一般團隊成員的 **要求狀態** 值會變更為 **需要檢閱**。</span><span class="sxs-lookup"><span data-stu-id="6044e-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="6044e-112">專案經理可以接受或拒絕提案。</span><span class="sxs-lookup"><span data-stu-id="6044e-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="6044e-113">資源經理處理資源要求時，可以使用下列任一方法：</span><span class="sxs-lookup"><span data-stu-id="6044e-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="6044e-114">如果沒有單一資源可用來履行需要的時數，請提案建議多個資源以滿足需求。</span><span class="sxs-lookup"><span data-stu-id="6044e-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="6044e-115">提案的時數隨後會在多個可滿足所需時數的資源間進行分割。</span><span class="sxs-lookup"><span data-stu-id="6044e-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="6044e-116">在此案例中，時數不能重疊。</span><span class="sxs-lookup"><span data-stu-id="6044e-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="6044e-117">提案建議比所需資源還要少的資源。</span><span class="sxs-lookup"><span data-stu-id="6044e-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="6044e-118">在此案例中，提案的資源產能小於要求者所指定的需要時數。</span><span class="sxs-lookup"><span data-stu-id="6044e-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="6044e-119">因此，當要求者接受提案的資源時，就會建立未履行資源需求，以擷取剩餘的索求。</span><span class="sxs-lookup"><span data-stu-id="6044e-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="6044e-120">如果沒有單一資源可用來完成工作，請預約建議多個資源以滿足索求。</span><span class="sxs-lookup"><span data-stu-id="6044e-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="6044e-121">預約比所需資源還要少的資源。</span><span class="sxs-lookup"><span data-stu-id="6044e-121">Book fewer resources than are required.</span></span> <span data-ttu-id="6044e-122">在此案例中，預約的工時少於需要的時數。</span><span class="sxs-lookup"><span data-stu-id="6044e-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="6044e-123">系統會引導您提案建議的是資源而不是預約，這樣要求者才能驗證並追蹤剩餘的索求。</span><span class="sxs-lookup"><span data-stu-id="6044e-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="6044e-124">資源可用性</span><span class="sxs-lookup"><span data-stu-id="6044e-124">Resource availability</span></span>

<span data-ttu-id="6044e-125">資源管理員要能夠檢視資源可用性並更新預約，至關重要。</span><span class="sxs-lookup"><span data-stu-id="6044e-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="6044e-126">在某些情況下，沒有正式索求 (資源要求)，但是資源管理員必須回應來自電子郵件、通話或立即訊息等管道的計劃外索求。</span><span class="sxs-lookup"><span data-stu-id="6044e-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="6044e-127">資源管理員會使用排程面板來更新資源和預約。</span><span class="sxs-lookup"><span data-stu-id="6044e-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="6044e-128">資源工作時數會用來做為計算資源可用性的基準。</span><span class="sxs-lookup"><span data-stu-id="6044e-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="6044e-129">資源預約會耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="6044e-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="6044e-130">排程面板使用色彩與陰影來顯示預約、可用性和過量預約，以及預約的狀態。</span><span class="sxs-lookup"><span data-stu-id="6044e-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="6044e-131">排程面板中的設定可讓您顯示圖例。</span><span class="sxs-lookup"><span data-stu-id="6044e-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="6044e-132">如果排程面板上的個別可預約資源旁邊出現向右箭頭，則可以展開資源來顯示該資源所預約之工作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6044e-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="6044e-133">因為 Dynamics 365 Project Operations 使用 Universal Resource Scheduling 引擎，如果您也已安裝 Dynamics 365 Field Service，則可以檢視專案、工單以及任何其他您已給予排程之實體的資源預約詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6044e-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="6044e-134">若要檢視更多關於個別資源的詳細資料，請在其上按滑鼠右鍵以開啟資源卡片。</span><span class="sxs-lookup"><span data-stu-id="6044e-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]