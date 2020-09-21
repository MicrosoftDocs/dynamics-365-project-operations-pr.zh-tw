---
title: 排程專案的資源
description: 如何在 Project Service 中排程專案的資源
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749988"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="29133-103">排程專案的資源 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="29133-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="29133-104">您可以檢查資源可用性，以檢視資源預約的整體情況，或者您可以依技能、團隊、地點及其他選項篩選檢視。</span><span class="sxs-lookup"><span data-stu-id="29133-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="29133-105">排程面板會顯示資源清單及其可用性。</span><span class="sxs-lookup"><span data-stu-id="29133-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="29133-106">選取檢視模式，依**小時**、**日**、**週**或**月**顯示可用性。</span><span class="sxs-lookup"><span data-stu-id="29133-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="29133-107">在您使用排程面版之前，務必將它設定好。</span><span class="sxs-lookup"><span data-stu-id="29133-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="29133-108">如需詳細資訊，請參閱[設定排程面板 (Field Service 或 Project Service Automation)](../field-service/configure-schedule-board.md)。</span><span class="sxs-lookup"><span data-stu-id="29133-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](../field-service/configure-schedule-board.md).</span></span>
  
<span data-ttu-id="29133-109">如果您使用的是舊版，請參閱[檢視資源可用性](../project-service/view-resource-availability.md)以了解資源可用性。</span><span class="sxs-lookup"><span data-stu-id="29133-109">If you are using an older version, for resource availability, see [View resource availability](../project-service/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="29133-110">若要使用排程面板預約功能、地理編碼及位置服務，您需要開啟地圖。</span><span class="sxs-lookup"><span data-stu-id="29133-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="29133-111">在主要功能表上，選取**資源排程** > **管理**。</span><span class="sxs-lookup"><span data-stu-id="29133-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="29133-112">按一下**排程參數**。</span><span class="sxs-lookup"><span data-stu-id="29133-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="29133-113">開啟記錄，然後向下捲動至 **Resource Scheduling Optimization** 區段。</span><span class="sxs-lookup"><span data-stu-id="29133-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="29133-114">在**連線到地圖服務**欄位中，選擇 **是**。</span><span class="sxs-lookup"><span data-stu-id="29133-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="29133-115">接受條款並儲存記錄。</span><span class="sxs-lookup"><span data-stu-id="29133-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="29133-116">在主要功能表上，選取 **Project Service** > **排程面板**。</span><span class="sxs-lookup"><span data-stu-id="29133-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="29133-117">在這裡，有數種不同方式可手動排程預約需求。</span><span class="sxs-lookup"><span data-stu-id="29133-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="29133-118">選擇適合您使用的方法。</span><span class="sxs-lookup"><span data-stu-id="29133-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="29133-119">尋找可用資源</span><span class="sxs-lookup"><span data-stu-id="29133-119">Find available resources</span></span>

1.  <span data-ttu-id="29133-120">在**預約需求**清單中，以滑鼠右鍵按一下未排程的預約，然後選擇下列其中一項︰</span><span class="sxs-lookup"><span data-stu-id="29133-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="29133-121">選擇 **尋找可用性 - 目前資源**，從排程面板上的清單中尋找可用的資源。</span><span class="sxs-lookup"><span data-stu-id="29133-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="29133-122">選擇 **尋找可用性 - 所有資源**，從系統中的資源尋找可用的資源。</span><span class="sxs-lookup"><span data-stu-id="29133-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="29133-123">當您這樣做時，篩選會顯示選取的預約需求的選項。</span><span class="sxs-lookup"><span data-stu-id="29133-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="29133-124">看到可用的時段時，以滑鼠右鍵按一下排程面板上的該時段，並選擇**在這裡預約**。</span><span class="sxs-lookup"><span data-stu-id="29133-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="29133-125">或者，將預約需求拖曳到可用的時段。</span><span class="sxs-lookup"><span data-stu-id="29133-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="29133-126">使用每日檢視表預約資源，並尋找誰還能預約</span><span class="sxs-lookup"><span data-stu-id="29133-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="29133-127">在排程面板上，選取**檢視模式**，然後選取**天**。</span><span class="sxs-lookup"><span data-stu-id="29133-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="29133-128">這會顯示資源每天預約的時數以及哪些天有空的網格檢視表。</span><span class="sxs-lookup"><span data-stu-id="29133-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="29133-129">按一下您想要預約的資源的名稱，然後選取**預約**。</span><span class="sxs-lookup"><span data-stu-id="29133-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="29133-130">在**資源預約 (建立)** 對話方塊中，選擇要預約資源來處理的專案，以及預約方法及開始和結束時間。</span><span class="sxs-lookup"><span data-stu-id="29133-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="29133-131">完成時，選取**預約**。</span><span class="sxs-lookup"><span data-stu-id="29133-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="29133-132">檢視排程面板</span><span class="sxs-lookup"><span data-stu-id="29133-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="29133-133">從底部的清單中選取未排程的預約需求。</span><span class="sxs-lookup"><span data-stu-id="29133-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="29133-134">將預約需求拖曳至排程面板上可用的資源/時段。</span><span class="sxs-lookup"><span data-stu-id="29133-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="29133-135">完成時，選取**預約**。</span><span class="sxs-lookup"><span data-stu-id="29133-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="29133-136">其他資源</span><span class="sxs-lookup"><span data-stu-id="29133-136">Additional resources</span></span>  
 [<span data-ttu-id="29133-137">資源管理員指南</span><span class="sxs-lookup"><span data-stu-id="29133-137">Resource manager guide</span></span>](../project-service/resource-manager-guide.md)
