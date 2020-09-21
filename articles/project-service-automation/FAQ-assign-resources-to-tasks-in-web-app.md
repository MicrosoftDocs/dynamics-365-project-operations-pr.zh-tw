---
title: 如何在 Web 應用程式中將可預約資源指派給工作
description: 有關如何指派可預約資源的概觀。
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750011"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="53ed1-103">如何在 Web 應用程式 (Project Service 應用程式 2.x 版) 中將可預約資源指派給工作？</span><span class="sxs-lookup"><span data-stu-id="53ed1-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="53ed1-104">有兩種方法可以在 Project Service 中指派資源給工作。</span><span class="sxs-lookup"><span data-stu-id="53ed1-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="53ed1-105">您可以預約資源做為團隊成員，再將該資源指派給工作。</span><span class="sxs-lookup"><span data-stu-id="53ed1-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="53ed1-106">或者，也可以在工作上透過角色指派建立一般團隊成員、產生團隊，然後使用具名資源履行支援需求。</span><span class="sxs-lookup"><span data-stu-id="53ed1-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="53ed1-107">請注意，如果您想要將可預約資源指派給工作，則可預約資源團隊成員必須足夠的可用預約。</span><span class="sxs-lookup"><span data-stu-id="53ed1-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="53ed1-108">預約的狀態必須是 [認可類型為已確認預約] 和 [狀態已認可]。</span><span class="sxs-lookup"><span data-stu-id="53ed1-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="53ed1-109">如果資源沒有足夠的預約，Project Service 就會移除指派，並顯示下列錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="53ed1-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="53ed1-110">*無法指派資源給工作 - 下列資源對專案沒有充足的預約時數*</span><span class="sxs-lookup"><span data-stu-id="53ed1-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="53ed1-111">預約資源做為團隊成員，再將該資源指派給工作</span><span class="sxs-lookup"><span data-stu-id="53ed1-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="53ed1-112">您可以使用此方法，將資源新增至專案團隊，然後將工作指派給專案排程中的資源。</span><span class="sxs-lookup"><span data-stu-id="53ed1-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="53ed1-113">以下說明如何執行此動作：</span><span class="sxs-lookup"><span data-stu-id="53ed1-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="53ed1-114">在團隊成員網格中，選取**新增**以將新的團隊成員加入。</span><span class="sxs-lookup"><span data-stu-id="53ed1-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="53ed1-115">在 [團隊成員快速建立] 畫面中，選取可預約資源名稱並設定角色。</span><span class="sxs-lookup"><span data-stu-id="53ed1-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="53ed1-116">選取**開始**和**結束**日期。</span><span class="sxs-lookup"><span data-stu-id="53ed1-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="53ed1-117">![新增團隊成員的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-1.png "新增團隊成員的螢幕擷取畫面")</span><span class="sxs-lookup"><span data-stu-id="53ed1-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="53ed1-118">選取下列其中一個配置方法以進行資源預約：</span><span class="sxs-lookup"><span data-stu-id="53ed1-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="53ed1-119">**完整產能**會預約資源在指定之開始和結束日期的完整產能。</span><span class="sxs-lookup"><span data-stu-id="53ed1-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="53ed1-120">**產能百分比**會預約資源在指定之開始和結束日期一定百分比資源的產能。</span><span class="sxs-lookup"><span data-stu-id="53ed1-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="53ed1-121">**依時數平均分配**會預約指定時數的資源，並在指定之開始和結束日期內平均分配每日的時數。</span><span class="sxs-lookup"><span data-stu-id="53ed1-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="53ed1-122">**依時數前重後輕**會預約指定時數的資源，並在指定之開始和結束日期內以前重後輕的方式分配每日的時數。</span><span class="sxs-lookup"><span data-stu-id="53ed1-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="53ed1-123">不要選取**無**，因為這會將資源新增至團隊，但不會建立任何吸收資源產能的預約。</span><span class="sxs-lookup"><span data-stu-id="53ed1-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="53ed1-124">選取**儲存**。</span><span class="sxs-lookup"><span data-stu-id="53ed1-124">Select **Save**.</span></span>

    <span data-ttu-id="53ed1-125">請注意，預約的時數必須足以涵蓋獲指派此資源之工作的努力時數和日期範圍。</span><span class="sxs-lookup"><span data-stu-id="53ed1-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="53ed1-126">如果其間有不一致的情況，就無法將資源指派給工作。</span><span class="sxs-lookup"><span data-stu-id="53ed1-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="53ed1-127">在工作的分工結構圖 (WBS) 上，按一下資源儲存格下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="53ed1-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="53ed1-128">接下來：</span><span class="sxs-lookup"><span data-stu-id="53ed1-128">Then:</span></span> 

    1. <span data-ttu-id="53ed1-129">選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="53ed1-129">Select **Add**.</span></span>
    2. <span data-ttu-id="53ed1-130">選取**資源**下方的下拉式清單，並選取您先前新增的團隊成員。</span><span class="sxs-lookup"><span data-stu-id="53ed1-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="53ed1-131">選取**確定**。</span><span class="sxs-lookup"><span data-stu-id="53ed1-131">Select **OK**.</span></span> <span data-ttu-id="53ed1-132">團隊成員現在已指派給工作。</span><span class="sxs-lookup"><span data-stu-id="53ed1-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="53ed1-133">![透過 WBS 新增資源的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-2.png "透過 WBS 新增資源的螢幕擷取畫面")</span><span class="sxs-lookup"><span data-stu-id="53ed1-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="53ed1-134">在團隊成員網格中，您會在 [指派的時數] 底下看到資源指派時數的彙總。</span><span class="sxs-lookup"><span data-stu-id="53ed1-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="53ed1-135">這會小於或等於資源的預約時數。</span><span class="sxs-lookup"><span data-stu-id="53ed1-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="53ed1-136">![資源指派時數的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-3.png "資源指派時數的螢幕擷取畫面")</span><span class="sxs-lookup"><span data-stu-id="53ed1-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="53ed1-137">如果您嘗試指派給資源的工作是在資源預約的結束日期之後開始，則該資源不會出現在下拉式清單中。</span><span class="sxs-lookup"><span data-stu-id="53ed1-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="53ed1-138">請注意，如果資源還剩餘一些未指派的產能，您可以將資源指派給較其預約時數更多的時數。</span><span class="sxs-lookup"><span data-stu-id="53ed1-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="53ed1-139">在這種情況下，只會部分指派資源，最多以其預約數為限。</span><span class="sxs-lookup"><span data-stu-id="53ed1-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="53ed1-140">您可將 [無配置人員的時數] 欄新增至分工結構圖，以查看這些剩餘未指派的工作時數。</span><span class="sxs-lookup"><span data-stu-id="53ed1-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="53ed1-141">如果資源已指派給其預約時數 (其預約時數等於其指派時數)，您將會在嘗試將這些時數指派給更多工作時看到下列錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="53ed1-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="53ed1-142">*無法指派資源給工作 - 下列資源對專案沒有充足的預約時數。*</span><span class="sxs-lookup"><span data-stu-id="53ed1-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="53ed1-143">此外，還會在沒有任何預約的情況下新增您建立專案時所新增至團隊的預設專案經理團隊成員，而此成員也無法指派給任何工作。</span><span class="sxs-lookup"><span data-stu-id="53ed1-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="53ed1-144">這些成員不會顯示在工作的資源下拉式清單中。</span><span class="sxs-lookup"><span data-stu-id="53ed1-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="53ed1-145">如果您想要指派此資源，就必須將這些資源從團隊移除，然後使用 [無] 以外的配置方法重新加入團隊中。</span><span class="sxs-lookup"><span data-stu-id="53ed1-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="53ed1-146">建立專案時將這些資源新增至團隊的原因是，為了讓專案預設會有至少一個專案核准者。</span><span class="sxs-lookup"><span data-stu-id="53ed1-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="53ed1-147">透過在工作上指派角色建立一般團隊成員</span><span class="sxs-lookup"><span data-stu-id="53ed1-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="53ed1-148">此方法可確保資源有足夠的預約提供給工作。</span><span class="sxs-lookup"><span data-stu-id="53ed1-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="53ed1-149">首先，您可在指派角色給工作後產生團隊，以建立描述您最終要在工作上使用之具名資源特性的預留位置或一般資源。</span><span class="sxs-lookup"><span data-stu-id="53ed1-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="53ed1-150">以下說明如何執行此動作：</span><span class="sxs-lookup"><span data-stu-id="53ed1-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="53ed1-151">在分工結構圖中，選取一項工作。</span><span class="sxs-lookup"><span data-stu-id="53ed1-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="53ed1-152">選取資源儲存格中的**指派的角色**下拉式清單圖示。</span><span class="sxs-lookup"><span data-stu-id="53ed1-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="53ed1-153">選取**角色**下拉式清單，並為一般資源選取角色。</span><span class="sxs-lookup"><span data-stu-id="53ed1-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="53ed1-154">選取**確定**。</span><span class="sxs-lookup"><span data-stu-id="53ed1-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="53ed1-155">![使用 WBS 新增資源的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-4.png "使用 WBS 新增資源的螢幕擷取畫面")</span><span class="sxs-lookup"><span data-stu-id="53ed1-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="53ed1-156">當您完成指派角色給 WBS 中的工作後，選取**產生專案團隊**。</span><span class="sxs-lookup"><span data-stu-id="53ed1-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="53ed1-157">Project Service 會彙總工作指派，以根據角色、資源分配組織單位和專案行事曆，建立最小數目的一般團隊成員。</span><span class="sxs-lookup"><span data-stu-id="53ed1-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="53ed1-158">![產生專案團隊的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-5.png "產生專案團隊的螢幕擷取畫面")</span><span class="sxs-lookup"><span data-stu-id="53ed1-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="53ed1-159">在 [團隊成員] 網格中，您會看到包含角色及位置名稱且類型為 [一般資源] 的資源。</span><span class="sxs-lookup"><span data-stu-id="53ed1-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="53ed1-160">如果一個角色需要兩項資源才能完成工作，[產生團隊] 功能就會建立兩個團隊成員，並使用位置名稱來區別這些成員。</span><span class="sxs-lookup"><span data-stu-id="53ed1-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="53ed1-161">![新增兩項一般資源的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-6.png "新增兩項一般資源的螢幕擷取畫面")</span><span class="sxs-lookup"><span data-stu-id="53ed1-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="53ed1-162">您可選取 [資源需求] 下方的連結，以開啟一般團隊成員的支援資源需求。</span><span class="sxs-lookup"><span data-stu-id="53ed1-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="53ed1-163">![開啟支援資源需求的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-7.png "開啟支援資源需求的螢幕擷取畫面")</span><span class="sxs-lookup"><span data-stu-id="53ed1-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="53ed1-164">選取一般資源的**預約**，然後您就可以使用排程面板來尋找並預訂實際資源。</span><span class="sxs-lookup"><span data-stu-id="53ed1-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="53ed1-165">您也可以選取**送出要求**，送出要求資源管理員履行的需求。</span><span class="sxs-lookup"><span data-stu-id="53ed1-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="53ed1-166">使用具名資源履行一般資源時，一般資源將會從團隊中移除，而且一般資源的工作指派會指派給履行一般資源之資源需求的具名資源。</span><span class="sxs-lookup"><span data-stu-id="53ed1-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

