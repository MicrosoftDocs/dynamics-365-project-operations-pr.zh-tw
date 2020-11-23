---
title: 預約給專案
description: 本主題提供有關預約資源給專案的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c87b0c32ef081f601ed79c11687f008bb454dd45
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131063"
---
# <a name="book-to-a-project"></a><span data-ttu-id="6fa50-103">預約給專案</span><span class="sxs-lookup"><span data-stu-id="6fa50-103">Book to a project</span></span>

<span data-ttu-id="6fa50-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="6fa50-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6fa50-105">專案經理或資源管理員有時需要將資源配置給沒有一般團隊成員所定義之特定需求的專案。</span><span class="sxs-lookup"><span data-stu-id="6fa50-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="6fa50-106">這可以透過三種方式之一來達成。</span><span class="sxs-lookup"><span data-stu-id="6fa50-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="6fa50-107">從團隊成員網格預約</span><span class="sxs-lookup"><span data-stu-id="6fa50-107">Book from the team member grid</span></span>
- <span data-ttu-id="6fa50-108">從排程面板預約</span><span class="sxs-lookup"><span data-stu-id="6fa50-108">Book from the schedule board</span></span>
- <span data-ttu-id="6fa50-109">從 **專案** 表單預約</span><span class="sxs-lookup"><span data-stu-id="6fa50-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="6fa50-110">從團隊成員網格預約</span><span class="sxs-lookup"><span data-stu-id="6fa50-110">Book from the team member grid</span></span>

<span data-ttu-id="6fa50-111">如果您的組織是在混合資源配置模式下運作，則專案經理可以完成下列步驟，直接將資源預約給專案。</span><span class="sxs-lookup"><span data-stu-id="6fa50-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="6fa50-112">從專案中移至團隊成員網格，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="6fa50-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="6fa50-113">定義資源的職位名稱和角色。</span><span class="sxs-lookup"><span data-stu-id="6fa50-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="6fa50-114">從可用的查詢中選取可預約資源。</span><span class="sxs-lookup"><span data-stu-id="6fa50-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="6fa50-115">選取資源之後，定義下列欄位資訊以預約資源：</span><span class="sxs-lookup"><span data-stu-id="6fa50-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="6fa50-116">開始日期</span><span class="sxs-lookup"><span data-stu-id="6fa50-116">Start date</span></span>
    - <span data-ttu-id="6fa50-117">完成日期</span><span class="sxs-lookup"><span data-stu-id="6fa50-117">Finish date</span></span>
    - <span data-ttu-id="6fa50-118">配置方法</span><span class="sxs-lookup"><span data-stu-id="6fa50-118">Allocation method</span></span>
    - <span data-ttu-id="6fa50-119">時數 (如果適用)</span><span class="sxs-lookup"><span data-stu-id="6fa50-119">Hours, if applicable</span></span>
    - <span data-ttu-id="6fa50-120">專案核准者</span><span class="sxs-lookup"><span data-stu-id="6fa50-120">Project approver</span></span>

6. <span data-ttu-id="6fa50-121">選取 **儲存後關閉**</span><span class="sxs-lookup"><span data-stu-id="6fa50-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="6fa50-122">從排程面板預約</span><span class="sxs-lookup"><span data-stu-id="6fa50-122">Book from the schedule board</span></span>

<span data-ttu-id="6fa50-123">資源管理員需要直接將資源預約給專案時，他們可以使用排程面板和專案需求。</span><span class="sxs-lookup"><span data-stu-id="6fa50-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="6fa50-124">專案需求是隨時可供預約的資源需求。</span><span class="sxs-lookup"><span data-stu-id="6fa50-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="6fa50-125">若要直接從排程面板預約給專案，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="6fa50-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="6fa50-126">瀏覽至排程面板，然後在左側頁面上，篩選您考慮要用於需求的資源。</span><span class="sxs-lookup"><span data-stu-id="6fa50-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="6fa50-127">在下方窗格中，選取 **專案** 索引標籤，以檢視專案需求清單。</span><span class="sxs-lookup"><span data-stu-id="6fa50-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="6fa50-128">將需求拖曳到資源，並定義下列資訊：</span><span class="sxs-lookup"><span data-stu-id="6fa50-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="6fa50-129">開始日期</span><span class="sxs-lookup"><span data-stu-id="6fa50-129">Start date</span></span>
    - <span data-ttu-id="6fa50-130">完成日期</span><span class="sxs-lookup"><span data-stu-id="6fa50-130">Finish date</span></span>
    - <span data-ttu-id="6fa50-131">預約狀態</span><span class="sxs-lookup"><span data-stu-id="6fa50-131">Booking status</span></span>
    - <span data-ttu-id="6fa50-132">預約方式</span><span class="sxs-lookup"><span data-stu-id="6fa50-132">Booking method</span></span>
    - <span data-ttu-id="6fa50-133">持續時間</span><span class="sxs-lookup"><span data-stu-id="6fa50-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="6fa50-134">從專案表單中預約</span><span class="sxs-lookup"><span data-stu-id="6fa50-134">Book from the Project form</span></span>

<span data-ttu-id="6fa50-135">身為專案經理，您可能需要將資源預約給專案，但是只知道準則，而不知資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fa50-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="6fa50-136">請完成下列步驟，使用排程小幫手根據資源的任何可用屬性來尋找資源。</span><span class="sxs-lookup"><span data-stu-id="6fa50-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="6fa50-137">瀏覽至專案，並選取 **預約** 以開啟排程小幫手。</span><span class="sxs-lookup"><span data-stu-id="6fa50-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="6fa50-138">使用排程小幫手左側的篩選，縮小準則的範圍並選取 **搜尋**。</span><span class="sxs-lookup"><span data-stu-id="6fa50-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="6fa50-139">您可以根據結果中傳回的資源來預約資源。</span><span class="sxs-lookup"><span data-stu-id="6fa50-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="6fa50-140">此方法不會為資源建立任何預約。</span><span class="sxs-lookup"><span data-stu-id="6fa50-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="6fa50-141">反而是將資源新增至團隊。</span><span class="sxs-lookup"><span data-stu-id="6fa50-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="6fa50-142">將團隊成員新增至專案之後，專案經理就可以使用維護預約或延長預約，將必要的預約新增至資源。</span><span class="sxs-lookup"><span data-stu-id="6fa50-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
