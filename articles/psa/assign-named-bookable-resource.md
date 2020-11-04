---
title: 將具名可預約資源預約給專案團隊並指派工作
description: 本主題提供有關如何將具名資源預約給專案團隊以及將這些資源指派至工作的資訊。
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: defc92e701ae6baf9d54f41dca123a09ef834c35
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073115"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="709d3-103">將具名可預約資源預約給專案團隊並指派工作</span><span class="sxs-lookup"><span data-stu-id="709d3-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="709d3-104">您可以直接預約具名資源給團隊，以將此資源新增至團隊。</span><span class="sxs-lookup"><span data-stu-id="709d3-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="709d3-105">若要這麼做，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="709d3-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="709d3-106">在 Project Service Automation 中，移至 **專案** ，然後選取並開啟您要預約到的專案。</span><span class="sxs-lookup"><span data-stu-id="709d3-106">In  Project Service Automation, go to **Projects** , and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="709d3-107">在 **專案** 頁面的 **團隊** 索引標籤上，按一下 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="709d3-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![從團隊索引標籤新增團隊成員](media/RM-how-to-1.png)

3. <span data-ttu-id="709d3-109">在 **快速建立專案團隊成員** 對話方塊中，選取可預約資源。</span><span class="sxs-lookup"><span data-stu-id="709d3-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="709d3-110">**角色** 欄位將會有資源的預設角色填入 (如果已指派此角色)。</span><span class="sxs-lookup"><span data-stu-id="709d3-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="709d3-111">您可以視需要變更角色。</span><span class="sxs-lookup"><span data-stu-id="709d3-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="709d3-112">選取需要資源的開始及結束日期，並選取資源產能的配置方法。</span><span class="sxs-lookup"><span data-stu-id="709d3-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="709d3-113">如果您要讓團隊成員成為專案核准者，請在 **專案核准者** 欄位中選取 **是** 。</span><span class="sxs-lookup"><span data-stu-id="709d3-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="709d3-114">這表示團隊成員可以核准為此專案送出的時間和費用項目。</span><span class="sxs-lookup"><span data-stu-id="709d3-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="709d3-115">按一下 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="709d3-115">Click **Save**.</span></span>

![在快速建立表單上新增團隊成員](media/RM-how-to-2.png)


<span data-ttu-id="709d3-117">您現在可以將預約的資源指派給專案中的工作。</span><span class="sxs-lookup"><span data-stu-id="709d3-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="709d3-118">在 **專案** 頁面上，按一下 **排程** 索引標籤以將工作指派給新資源。</span><span class="sxs-lookup"><span data-stu-id="709d3-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="709d3-119">從工作網格中 **資源** 欄位啟動的資源選擇器將會顯示您可以選取的團隊成員。</span><span class="sxs-lookup"><span data-stu-id="709d3-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![將團隊成員指派給排程索引標籤上的工作](media/RM-how-to-3.png)

<span data-ttu-id="709d3-121">在 Project Service Automation (PSA) 版本 3 中，資源預約和工作指派並非緊密聯繫。</span><span class="sxs-lookup"><span data-stu-id="709d3-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="709d3-122">這表示使用排程中的資源選擇器時，您可以將超過團隊成員預約對專案所能支援之時數的工作指派給該團隊成員。</span><span class="sxs-lookup"><span data-stu-id="709d3-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="709d3-123">您可以在 **團隊** 索引標籤或 **資源協調** 索引標籤上查看團隊成員預約與指派之間的差異。您也可以在更詳細的層級上協調資源預約與指派之間的差異。</span><span class="sxs-lookup"><span data-stu-id="709d3-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![[資源協調] 索引標籤](media/RM-how-to-4.png)

<span data-ttu-id="709d3-125">您也可以使用 **排程** 索引標籤上的資源選擇器來搜尋和選取尚不屬於專案團隊的可預約資源。</span><span class="sxs-lookup"><span data-stu-id="709d3-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="709d3-126">這些資源會在資源選擇器中顯示為 **其他資源** 。</span><span class="sxs-lookup"><span data-stu-id="709d3-126">These are shown in the resource picker as **Other Resources**.</span></span>

![將非團隊成員資源指派給工作](media/RM-how-to-5.png)

<span data-ttu-id="709d3-128">這樣做時，資源會新增至專案團隊並指派給工作，但不會產生任何預約。</span><span class="sxs-lookup"><span data-stu-id="709d3-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![有指派但無預約的團隊成員](media/RM-how-to-6.png)

<span data-ttu-id="709d3-130">您可以使用 **協調** 索引標籤的延長預約功能或是 **排程面板** ，將資源的產能預約給專案。</span><span class="sxs-lookup"><span data-stu-id="709d3-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![在資源協調索引標籤上，為團隊成員延長預約](media/RM-how-to-7.png)

<span data-ttu-id="709d3-132">在專案上預約您的團隊成員之後，您可以使用維護預約或直接使用排程面板來管理其預約。</span><span class="sxs-lookup"><span data-stu-id="709d3-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
