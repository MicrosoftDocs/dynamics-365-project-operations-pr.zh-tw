---
title: 管理時區
description: 建立專案時，其時區取決於所套用工作時數範本中定義的時區。
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961830"
---
# <a name="manage-time-zones"></a><span data-ttu-id="db7d6-103">管理時區</span><span class="sxs-lookup"><span data-stu-id="db7d6-103">Manage time zones</span></span>

<span data-ttu-id="db7d6-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="db7d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="db7d6-105">專案</span><span class="sxs-lookup"><span data-stu-id="db7d6-105">Projects</span></span>

<span data-ttu-id="db7d6-106">建立專案時，時區取決於所套用工作時數範本中定義的時區。</span><span class="sxs-lookup"><span data-stu-id="db7d6-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="db7d6-107">在**專案**上，日期一律相對於每個索引標籤 (**工作**索引標籤除外) 中已登入的使用者。當您檢視分工結構圖時，日期永遠以專案的時區來顯示。</span><span class="sxs-lookup"><span data-stu-id="db7d6-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="db7d6-108">工作</span><span class="sxs-lookup"><span data-stu-id="db7d6-108">Tasks</span></span>

<span data-ttu-id="db7d6-109">建立工作時，開始時間、結束時間和小時/天都是由專案的工作時數所控制。</span><span class="sxs-lookup"><span data-stu-id="db7d6-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="db7d6-110">例如，如果工作是使用時區為 -8 PST 的專案所建立，而且其工作時間為星期一到星期五上午 9:00 至下午 5:00，則任何未使用指派所建立的工作都會遵循專案行事曆的開始時間和結束時間。</span><span class="sxs-lookup"><span data-stu-id="db7d6-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="db7d6-111">使用時區來管理資源</span><span class="sxs-lookup"><span data-stu-id="db7d6-111">Manage resources with time zones</span></span>

<span data-ttu-id="db7d6-112">若要在使用**延伸預約**時獲得準確且可預測的結果，必須符合兩個重要先決條件：</span><span class="sxs-lookup"><span data-stu-id="db7d6-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="db7d6-113">使用者必須設定其裝置的時區，使其符合系統**個人化設定**中所定義的時區。</span><span class="sxs-lookup"><span data-stu-id="db7d6-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Windows 10 的時區設定](media/reconcile-assignments-03.png)

  ![個人化設定中的時區設定](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="db7d6-116">可預約資源至少必須有一分鐘的工作時間，與用於定義所要求之展延的分佈重疊。</span><span class="sxs-lookup"><span data-stu-id="db7d6-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="db7d6-117">例如，工作時間介於上午 9:00 至下午 7:00 之間的下列資源。</span><span class="sxs-lookup"><span data-stu-id="db7d6-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![資源分佈的比較](media/reconcile-assignments-05.png)

<span data-ttu-id="db7d6-119">下表顯示：</span><span class="sxs-lookup"><span data-stu-id="db7d6-119">The following table shows:</span></span>

- <span data-ttu-id="db7d6-120">專案行事曆範本</span><span class="sxs-lookup"><span data-stu-id="db7d6-120">A project calendar template</span></span>
- <span data-ttu-id="db7d6-121">資源 A：此資源有相同的行事曆，並且與專案位於同一個時區。</span><span class="sxs-lookup"><span data-stu-id="db7d6-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="db7d6-122">此預約的開始時間會是上午 9:00。</span><span class="sxs-lookup"><span data-stu-id="db7d6-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="db7d6-123">資源 B：此資源與專案位於不同的時區，兩者在其各自時區中的開始時間皆為上午 7:00。</span><span class="sxs-lookup"><span data-stu-id="db7d6-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="db7d6-124">不過，這些預約會從上午 9:00 開始，因為這是指派分佈的最早開始時間。</span><span class="sxs-lookup"><span data-stu-id="db7d6-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="db7d6-125">資源 C 和 D：這些資源位於不同的時區，兩者不僅彼此互異，也與專案不相同，而其預約開始時間不早於各自的可用開始時間。</span><span class="sxs-lookup"><span data-stu-id="db7d6-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="db7d6-126">實體</span><span class="sxs-lookup"><span data-stu-id="db7d6-126">Entity</span></span>  |<span data-ttu-id="db7d6-127">行事曆</span><span class="sxs-lookup"><span data-stu-id="db7d6-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="db7d6-128">專案行事曆範本</span><span class="sxs-lookup"><span data-stu-id="db7d6-128">Project calendar template</span></span>   | ![專案行事曆](media/reconcile-assignments-06.png) |
|<span data-ttu-id="db7d6-130">資源 A</span><span class="sxs-lookup"><span data-stu-id="db7d6-130">Resource A</span></span>  | ![資源 A 行事曆](media/reconcile-assignments-06.png) |
|<span data-ttu-id="db7d6-132">資源 B</span><span class="sxs-lookup"><span data-stu-id="db7d6-132">Resource B</span></span>  |  ![資源 B 行事曆](media/reconcile-assignments-07.png) |
|<span data-ttu-id="db7d6-134">資源 C</span><span class="sxs-lookup"><span data-stu-id="db7d6-134">Resource C</span></span>  |  ![資源 C 行事曆](media/reconcile-assignments-08.png) |
|<span data-ttu-id="db7d6-136">資源 D</span><span class="sxs-lookup"><span data-stu-id="db7d6-136">Resource D</span></span>  | ![資源 D 行事曆](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="db7d6-138">當您瀏覽至**協調**檢視表時，會顯示資源指派以及相關聯的預約短缺。</span><span class="sxs-lookup"><span data-stu-id="db7d6-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![延長前的協調檢視表](media/reconcile-assignments-10.png)

<span data-ttu-id="db7d6-140">每個資源都使用了延長預約功能之後，每個資源都會成功延長預約，因為每個資源的時數都與短缺的分佈重疊。</span><span class="sxs-lookup"><span data-stu-id="db7d6-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![展長後的協調檢視表](media/reconcile-assignments-11.png) 

<span data-ttu-id="db7d6-142">請注意，仔細查看預約的詳細資料，就會顯示預約開始時間中的差異。</span><span class="sxs-lookup"><span data-stu-id="db7d6-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="db7d6-143">預約不會比指派分佈的開始時間更早開始，也不會早於資源的可用開始時間。</span><span class="sxs-lookup"><span data-stu-id="db7d6-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![資源在排程面板中的新預約](media/reconcile-assignments-12.png)
