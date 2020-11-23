---
title: 資源協調概觀
description: 本主題提供有關確保專案的資源預約與指派一致的資訊。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125708"
---
# <a name="resource-reconciliation-overview"></a><span data-ttu-id="d21d5-103">資源協調概觀</span><span class="sxs-lookup"><span data-stu-id="d21d5-103">Resource reconciliation overview</span></span>

<span data-ttu-id="d21d5-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="d21d5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d21d5-105">在團隊成員中，預約與指派的聯繫鬆散。</span><span class="sxs-lookup"><span data-stu-id="d21d5-105">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="d21d5-106">換言之，資源可以有指派但沒有預約，或者可以有預約但沒有指派。</span><span class="sxs-lookup"><span data-stu-id="d21d5-106">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="d21d5-107">預約與指派最好要一致，讓資源有已認可產能來執行工作指派。</span><span class="sxs-lookup"><span data-stu-id="d21d5-107">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="d21d5-108">不過，預約可能會根據可用性，而工作計時可能會隨著專案持續而改變。</span><span class="sxs-lookup"><span data-stu-id="d21d5-108">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="d21d5-109">因此，鬆散聯繫的預約和指派提供了彈性。</span><span class="sxs-lookup"><span data-stu-id="d21d5-109">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="d21d5-110">**專案** 表單上的 **協調** 索引標籤，可讓專案經理協調團隊成員的預約及其對專案團隊的指派。</span><span class="sxs-lookup"><span data-stu-id="d21d5-110">The **Reconciliation** tab on the **Project** form lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

<span data-ttu-id="d21d5-111">**協調** 索引標籤還會顯示下至每個團隊成員個別工作指派層級的預約及指派。</span><span class="sxs-lookup"><span data-stu-id="d21d5-111">The **Reconciliation** tab also shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="d21d5-112">時數會顯示在儲存格中，表示從月數下至天數時段期間。</span><span class="sxs-lookup"><span data-stu-id="d21d5-112">Hours are displayed in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="d21d5-113">此索引標籤也會顯示專案的整體淨總數以及 **總計** 欄。</span><span class="sxs-lookup"><span data-stu-id="d21d5-113">The tab also shows an overall net total for the project, together with a **Total** column.</span></span>

<span data-ttu-id="d21d5-114">對於每項資源中，此索引標籤會計算團隊成員預約與團隊成員工作指派彙總之間的差異。</span><span class="sxs-lookup"><span data-stu-id="d21d5-114">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="d21d5-115">此差異最好是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="d21d5-115">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="d21d5-116">換句話說，預約與指派之間應該要沒有差異。</span><span class="sxs-lookup"><span data-stu-id="d21d5-116">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="d21d5-117">差異會著色並有明暗層次，以吸引對兩種狀況的注意：</span><span class="sxs-lookup"><span data-stu-id="d21d5-117">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="d21d5-118">**預約不足** – 當資源的指派數超過預約數時，就會發生預約短缺。</span><span class="sxs-lookup"><span data-stu-id="d21d5-118">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="d21d5-119">因為尚未保留此產能，專案經理可能需要延長資源的預約以彌補短缺來更正此情況。</span><span class="sxs-lookup"><span data-stu-id="d21d5-119">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="d21d5-120">**超額預約** – 當資源已預約給專案，但尚未指派給工作時，會發生超額預約。</span><span class="sxs-lookup"><span data-stu-id="d21d5-120">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="d21d5-121">在資源已在進行工作指派之前預約給專案的情況下，此狀況可能會是可接受的。</span><span class="sxs-lookup"><span data-stu-id="d21d5-121">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="d21d5-122">不過，在其他情況下，資源並未規劃要指派給工作。</span><span class="sxs-lookup"><span data-stu-id="d21d5-122">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="d21d5-123">在這些情況下，專案經理應考慮取消資源的預約，讓該產能可以用於其他專案。</span><span class="sxs-lookup"><span data-stu-id="d21d5-123">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="d21d5-124">在某些情況下中，當您以高於日的層級來檢視時間 (例如，月層級) 時，您可能會看到資源的淨差異為零 (換句話說，預約 = 指派)。</span><span class="sxs-lookup"><span data-stu-id="d21d5-124">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="d21d5-125">不過，如果您以週層級檢視時間，您可能會在第一週看到零小時的指派以及 40 小時的預約，但在第二週看到 40 小時的指派以及零小時的預約。</span><span class="sxs-lookup"><span data-stu-id="d21d5-125">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="d21d5-126">總而言之，預約和指派已協調，但它們在一週與下一週中不相同。</span><span class="sxs-lookup"><span data-stu-id="d21d5-126">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="d21d5-127">以較高層級檢視時間時，**調解** 索引標籤中的儲存格會有指示器，通知您較低層級上有差異。</span><span class="sxs-lookup"><span data-stu-id="d21d5-127">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="d21d5-128">在儲存格中按兩下，可以放大來檢視差異。</span><span class="sxs-lookup"><span data-stu-id="d21d5-128">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="d21d5-129">您可以接著按一下滑鼠右鍵來縮小。您可以選取資源，然後使用網格工具列的 **下一個差異** 控制項，移至該資源的預約與指派之間的下一個差異。</span><span class="sxs-lookup"><span data-stu-id="d21d5-129">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="d21d5-130">然後可以使用 **上一個差異** 控制項返回。</span><span class="sxs-lookup"><span data-stu-id="d21d5-130">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="d21d5-131">您也可以在 **設定** 底下關閉差異指示器和導覽行為。</span><span class="sxs-lookup"><span data-stu-id="d21d5-131">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>


<span data-ttu-id="d21d5-132">如果您資源有工作指派但沒有預約，請在 **專案** 頁面的 **協調** 索引標籤上，選取 [預訂不足]，然後選取 **延長預約**。</span><span class="sxs-lookup"><span data-stu-id="d21d5-132">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="d21d5-133">**延長預約** 對話方塊隨即出現，並顯示解決資源不足狀況所需的預約。</span><span class="sxs-lookup"><span data-stu-id="d21d5-133">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="d21d5-134">其中也會顯示資源在所有專案或其他可排程實體中的現有預約。</span><span class="sxs-lookup"><span data-stu-id="d21d5-134">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="d21d5-135">如果您選取 **確定** 建立資源的預約，不論該資源的可用性如何，都可能會造成過量預約。</span><span class="sxs-lookup"><span data-stu-id="d21d5-135">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

<span data-ttu-id="d21d5-136">專案經理或資源管理員可以接著使用排程面板，管理任何過量預約資源超過其產能的狀況。</span><span class="sxs-lookup"><span data-stu-id="d21d5-136">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>

