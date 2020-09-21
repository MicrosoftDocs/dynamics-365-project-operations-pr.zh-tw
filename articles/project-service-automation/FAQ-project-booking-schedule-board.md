---
title: 從排程面板建立專案預約
description: 本主題提供有關如何從排程面板建立專案預約的資訊。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Dynamics 365 Project Service Automation 2.x and 3.x
ms.technology: ''
ms.assetid: bbc1bbe2-3482-4b84-9e89-f7e0e585ade8
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7b6c7e07ea6451e0654ccf1ba7be10e7b38e0d09
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749974"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="35c83-103">從排程面板建立專案預約</span><span class="sxs-lookup"><span data-stu-id="35c83-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="35c83-104">您可以直接將資源從**團隊**索引標籤預約到專案，做法是在專案的專案團隊索引標籤上預約，或是從一般團隊成員指派產生資源需求，然後透過專案團隊成員履行產生的需求。</span><span class="sxs-lookup"><span data-stu-id="35c83-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="35c83-105">您也可以直接從排程面板將資源預約到專案。</span><span class="sxs-lookup"><span data-stu-id="35c83-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="35c83-106">有三種方式來完成此動作：</span><span class="sxs-lookup"><span data-stu-id="35c83-106">There are three ways to do this:</span></span>

- <span data-ttu-id="35c83-107">**透過產生的資源需求預約：** 建立一般資源並於專案中指派工作之後，就可以產生資源需求。</span><span class="sxs-lookup"><span data-stu-id="35c83-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="35c83-108">**從主要需求預約：** 主要需求會顯示在**專案**索引標籤的排程面板上。</span><span class="sxs-lookup"><span data-stu-id="35c83-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="35c83-109">**透過新的資源需求預約**：您可以從頭開始建立資源需求，並將其與專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="35c83-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="35c83-110">在排程面板中，資源需求會出現在**開啟需求**索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="35c83-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="35c83-111">透過產生的資源需求預約</span><span class="sxs-lookup"><span data-stu-id="35c83-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="35c83-112">您可以建立一般資源，再將其指派給專案中的一個或多個工作。</span><span class="sxs-lookup"><span data-stu-id="35c83-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="35c83-113">然後就可以從一般選團隊成員產生資源需求。</span><span class="sxs-lookup"><span data-stu-id="35c83-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="35c83-114">在排程面板中，此資源會出現在**開啟需求**索引標籤上。如果您有許多開啟需求，可能就需要使用網格上的欄篩選。</span><span class="sxs-lookup"><span data-stu-id="35c83-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="35c83-115">![排程面板上的開啟需求索引標籤](media/FAQ-Project-Booking-Schedule-Board-1.png "預約及指派表格的螢幕擷取畫面")</span><span class="sxs-lookup"><span data-stu-id="35c83-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="35c83-116">選取需求。</span><span class="sxs-lookup"><span data-stu-id="35c83-116">Select the requirement.</span></span> <span data-ttu-id="35c83-117">**尋找可用性**索引標籤會顯示在所選列的上方。</span><span class="sxs-lookup"><span data-stu-id="35c83-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="35c83-118">選取索引標籤時，排程面板的 [排程小幫手] 模式會開啟，然後篩選符合資源需求的可用資源。</span><span class="sxs-lookup"><span data-stu-id="35c83-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="35c83-119">在那之後，即可預約資源。</span><span class="sxs-lookup"><span data-stu-id="35c83-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="35c83-120">您也可以將所選取的列從排程面板底部拖放到上方網格中的資源儲存格。</span><span class="sxs-lookup"><span data-stu-id="35c83-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="35c83-121">放下需求時，這會在右側開啟**建立資源預約**面板。</span><span class="sxs-lookup"><span data-stu-id="35c83-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="35c83-122">選取**預約**就會將資源預約到專案團隊。</span><span class="sxs-lookup"><span data-stu-id="35c83-122">Selecting **Book** books the resource onto the project team.</span></span>

![建立資源預約面板](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="35c83-124">從主要需求預約</span><span class="sxs-lookup"><span data-stu-id="35c83-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="35c83-125">在 Project Service 中建立專案會自動建立稱為「主要需求」的資源需求。</span><span class="sxs-lookup"><span data-stu-id="35c83-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="35c83-126">這是在不產生需求，或從頭開始建立需求的情況下，用來快速透過排程面板預約資源的空白需求。</span><span class="sxs-lookup"><span data-stu-id="35c83-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="35c83-127">因為需求是空的，您必須指定日期以及配置方法和時數 (如果適用)。</span><span class="sxs-lookup"><span data-stu-id="35c83-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="35c83-128">若要使用主要需求預約資源，請在排程面板上選取**專案**索引標籤。如果您有許多專案，您可能需要使用**專案**欄上的欄篩選。</span><span class="sxs-lookup"><span data-stu-id="35c83-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="35c83-129">![排程面板上的欄篩選](media/FAQ-Project-Booking-Schedule-Board-2.png "預約及指派表格的螢幕擷取畫面")</span><span class="sxs-lookup"><span data-stu-id="35c83-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="35c83-130">選取僅以專案名稱做為其名稱且期間為零 (0) 的需求。</span><span class="sxs-lookup"><span data-stu-id="35c83-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="35c83-131">選取列上顯示的**尋找可用性**索引標籤。</span><span class="sxs-lookup"><span data-stu-id="35c83-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="35c83-132">這會讓排程面板進入 [排程小幫手] 模式，並顯示可以預約到專案的可用資源。</span><span class="sxs-lookup"><span data-stu-id="35c83-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="35c83-133">因為**主要需求**是期間為零 (0) 的空白需求，當您選取和預約資源時，必須在**建立資源預約**面板上設定期間。</span><span class="sxs-lookup"><span data-stu-id="35c83-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="35c83-134">您也可以選取排程面板底部的**專案主要需求**，再將其拖放到要預約的資源。</span><span class="sxs-lookup"><span data-stu-id="35c83-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="35c83-135">因為**主要需求**是期間為零 (0) 的空白需求，當您選取和預約資源時，必須在**建立資源預約**面板上設定期間。</span><span class="sxs-lookup"><span data-stu-id="35c83-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="35c83-136">當您在排程面板上透過**主要需求**預約資源時，不做任何指派，也能將資源新增至專案團隊。</span><span class="sxs-lookup"><span data-stu-id="35c83-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="35c83-137">透過新的資源需求預約</span><span class="sxs-lookup"><span data-stu-id="35c83-137">Book from a new resource requirement</span></span>
<span data-ttu-id="35c83-138">完成下列步驟，以透過新的資源需求預約。</span><span class="sxs-lookup"><span data-stu-id="35c83-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="35c83-139">移至**資源需求**，然後選取**新增**以建立新的資源需求。</span><span class="sxs-lookup"><span data-stu-id="35c83-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="35c83-140">在**專案**索引標籤上，選取要將需求與專案建立關聯的專案。</span><span class="sxs-lookup"><span data-stu-id="35c83-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="35c83-141">在排程面板上，這個新需求會在排程面板上顯示為您可以履行的**開啟需求**。</span><span class="sxs-lookup"><span data-stu-id="35c83-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="35c83-142">預約資源以將該資源新增至專案團隊。</span><span class="sxs-lookup"><span data-stu-id="35c83-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="35c83-143">現在資源已預約，您必須以手動方式指派工作。</span><span class="sxs-lookup"><span data-stu-id="35c83-143">Now that the resource is booked, you must assign tasks manually.</span></span>

