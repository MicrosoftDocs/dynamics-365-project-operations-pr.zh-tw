---
title: 如何在應用程式版本 2.x 中進行資源的「未確認預約」？
description: 本文說明如何使用 Project Service 對專案團隊成員進行未確認預約。
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9e5d1c91f8ea98117583996552c2f2834be9c537
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073019"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="411ad-103">如何在 Web 應用程式 (Project Service 應用程式 2.x 版) 中進行資源的「未確認預約」？</span><span class="sxs-lookup"><span data-stu-id="411ad-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="411ad-104">您可透過暫訂方式將資源排程或「未確認預約」到專案團隊上，以顯示您計劃要將資源指派給專案。</span><span class="sxs-lookup"><span data-stu-id="411ad-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="411ad-105">未確認預約不會耗用資源的可用產能。</span><span class="sxs-lookup"><span data-stu-id="411ad-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="411ad-106">無法將未確認預約的團隊成員指派給專案工作。</span><span class="sxs-lookup"><span data-stu-id="411ad-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="411ad-107">只能將狀態為 [已確認預約] 且認可類型為 [已認可] 的資源指派給工作 (假設這些資源有足夠的已確認預約時數用來完成指派工作)。</span><span class="sxs-lookup"><span data-stu-id="411ad-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="411ad-108">未確認預約的專案團隊成員會在 [團隊成員] 網格中與 [未確認預約] 欄顯示的未確認預約時數一起出現。</span><span class="sxs-lookup"><span data-stu-id="411ad-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="411ad-109">這些成員也會在排程面板上出現。</span><span class="sxs-lookup"><span data-stu-id="411ad-109">They also show up on the schedule board.</span></span> <span data-ttu-id="411ad-110">再說，他們也沒有任何耗用產能的跡象，因為未確認預約不會耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="411ad-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="411ad-111">Project Service 2.x 版有三種方法可以透過未確認預約將團隊成員預約到專案。</span><span class="sxs-lookup"><span data-stu-id="411ad-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="411ad-112">您可以透過排程面板、使用 [維護預約] 功能，或藉由建立一般資源來進行未確認預約。</span><span class="sxs-lookup"><span data-stu-id="411ad-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="411ad-113">以下說明這些方法。</span><span class="sxs-lookup"><span data-stu-id="411ad-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="411ad-114">使用排程面板進行未確認預約</span><span class="sxs-lookup"><span data-stu-id="411ad-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="411ad-115">若要使用排程面板進行未確認預約，請遵循此程序：</span><span class="sxs-lookup"><span data-stu-id="411ad-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="411ad-116">開啟排程面板。</span><span class="sxs-lookup"><span data-stu-id="411ad-116">Open the schedule board.</span></span>
2. <span data-ttu-id="411ad-117">在排程面板下方的 [預約需求] 面板中選取 [專案] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="411ad-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="411ad-118">尋找您要以未確認預約方式將資源預約到的目標專案。</span><span class="sxs-lookup"><span data-stu-id="411ad-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="411ad-119">如果您有許多專案，請按一下 [專案] 欄標題，然後使用篩選來尋找您的專案。</span><span class="sxs-lookup"><span data-stu-id="411ad-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="411ad-120">按一下專案，然後將其拖放到資源的時間網格。</span><span class="sxs-lookup"><span data-stu-id="411ad-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="411ad-121">這會在右側開啟 [建立資源預約] 面板。</span><span class="sxs-lookup"><span data-stu-id="411ad-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="411ad-122">調整開始和結束日期、選取 [未確認] 做為 [預約狀態]，然後設定時數。</span><span class="sxs-lookup"><span data-stu-id="411ad-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="411ad-123">按一下 [預約]。</span><span class="sxs-lookup"><span data-stu-id="411ad-123">Click Book.</span></span>
7. <span data-ttu-id="411ad-124">回到專案上，資源會立即顯示為 [未確認預約] 欄中有未確認預約時數的團隊成員。</span><span class="sxs-lookup"><span data-stu-id="411ad-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="411ad-125">請注意，您無法將他們指派給分工結構圖 (WBS) 上的工作，因為資源必須在團隊上是已確認預約才能進行指派。</span><span class="sxs-lookup"><span data-stu-id="411ad-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="411ad-126">使用的維護預約功能進行未確認預約</span><span class="sxs-lookup"><span data-stu-id="411ad-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="411ad-127">若要使用 [維護預約] 進行未確認預約，請遵循此程序：</span><span class="sxs-lookup"><span data-stu-id="411ad-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="411ad-128">在團隊成員網格中按一下 [新增]。</span><span class="sxs-lookup"><span data-stu-id="411ad-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="411ad-129">選取可預約資源、角色、開始/結束日期。</span><span class="sxs-lookup"><span data-stu-id="411ad-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="411ad-130">選取 [無] 以外的配置方法：</span><span class="sxs-lookup"><span data-stu-id="411ad-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="411ad-131">完整產能</span><span class="sxs-lookup"><span data-stu-id="411ad-131">Full Capacity</span></span>
- <span data-ttu-id="411ad-132">產能百分比</span><span class="sxs-lookup"><span data-stu-id="411ad-132">Percentage Capacity</span></span>
- <span data-ttu-id="411ad-133">依時數平均分配</span><span class="sxs-lookup"><span data-stu-id="411ad-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="411ad-134">依時數前重後輕</span><span class="sxs-lookup"><span data-stu-id="411ad-134">By Hours Front Load</span></span>
4. <span data-ttu-id="411ad-135">按一下 [儲存]。</span><span class="sxs-lookup"><span data-stu-id="411ad-135">Click Save.</span></span> <span data-ttu-id="411ad-136">您將會在團隊網格及其時數上看到資源顯示為 [已確認]。</span><span class="sxs-lookup"><span data-stu-id="411ad-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="411ad-137">按一下 [維護預約] 以維持資源的預約。</span><span class="sxs-lookup"><span data-stu-id="411ad-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="411ad-138">當排程面板開啟時，展開資源以顯示其預約。</span><span class="sxs-lookup"><span data-stu-id="411ad-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="411ad-139">您將會看到預約顯示為 [已確認]。</span><span class="sxs-lookup"><span data-stu-id="411ad-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="411ad-140">以滑鼠右鍵按一下預約、在 [變更狀態] 下選取 [未確認預約]，然後選取 [未確認]。</span><span class="sxs-lookup"><span data-stu-id="411ad-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="411ad-141">預約狀態現在為 [未確認]。</span><span class="sxs-lookup"><span data-stu-id="411ad-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="411ad-142">關閉排程面板之後，就會在團隊成員網格中看到資源的時數已從 [已確認] 變更為 [未確認]。</span><span class="sxs-lookup"><span data-stu-id="411ad-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="411ad-143">請注意，如果您透過已確認預約方式將資源預約到團隊，然後再指派給 WBS 中的工作，當您使用維護預約將 [已確認] 的狀態變更 [未確認] 時，這就會將指派從該資源的工作中移除，因為只能將預約已確認的資源指派給工作。</span><span class="sxs-lookup"><span data-stu-id="411ad-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="411ad-144">藉由建立一般資源進行未確認預約</span><span class="sxs-lookup"><span data-stu-id="411ad-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="411ad-145">您可以建立未確認預約，做法為產生一般資源團隊成員、透過排程面板或 [資源要求] 履行資源需求，然後在預約期間變更類型。</span><span class="sxs-lookup"><span data-stu-id="411ad-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="411ad-146">若要這樣做，請使用下列程序：</span><span class="sxs-lookup"><span data-stu-id="411ad-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="411ad-147">在專案 WBS 上，將角色指派給您要針對產生一般團隊成員的工作。</span><span class="sxs-lookup"><span data-stu-id="411ad-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="411ad-148">按一下 [產生專案團隊]。</span><span class="sxs-lookup"><span data-stu-id="411ad-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="411ad-149">在專案團隊成員網格中，選取一般資源並按一下 [預約]。</span><span class="sxs-lookup"><span data-stu-id="411ad-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="411ad-150">在排程面板上，選取您要預約的資源。</span><span class="sxs-lookup"><span data-stu-id="411ad-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="411ad-151">在排程面板的 [建立資源預約] 面板上，將 [預約狀態] 變更為 [未確認]。</span><span class="sxs-lookup"><span data-stu-id="411ad-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="411ad-152">按一下 [預約] 或 [結束]。</span><span class="sxs-lookup"><span data-stu-id="411ad-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="411ad-153">關閉排程面板之後，您將會看到所選的資源已連同未確認預約時數以及指派的時數一併新增至團隊。</span><span class="sxs-lookup"><span data-stu-id="411ad-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="411ad-154">您也會看到一般資源仍保留在團隊上，做為指出工作已指派給未確認預約團隊成員的指示器。</span><span class="sxs-lookup"><span data-stu-id="411ad-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="411ad-155">當您準備好將未確認預約團隊成員資源變更為已確認預約團隊成員，以便將他們指派給工作時，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="411ad-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="411ad-156">選取該資源，並按一下 [維護預約]。</span><span class="sxs-lookup"><span data-stu-id="411ad-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="411ad-157">當排程面板開啟時，展開資源以顯示其預約。</span><span class="sxs-lookup"><span data-stu-id="411ad-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="411ad-158">您將看到預約標示為 [未確認]。</span><span class="sxs-lookup"><span data-stu-id="411ad-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="411ad-159">以滑鼠右鍵按一下預約、在 [變更狀態] 下選取 [已確認預約]，然後選取 [已確認]。</span><span class="sxs-lookup"><span data-stu-id="411ad-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="411ad-160">預約狀態現在為 [已確認]。</span><span class="sxs-lookup"><span data-stu-id="411ad-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="411ad-161">關閉排程面板之後，就會在團隊成員網格中看到資源的時數已從 [未確認] 變更為 [已確認]。</span><span class="sxs-lookup"><span data-stu-id="411ad-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="411ad-162">您現在可以將資源指派給工作 (假如已確認預約的時數與指派的工作努力時數配合得上)。</span><span class="sxs-lookup"><span data-stu-id="411ad-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="411ad-163">請注意，如果您已依照上述第 3 項中的一般資源履行步驟進行，當您將未確認預約的可預約資源變更為 [已確認] 時，將 會將一般團隊成員從團隊中移除。</span><span class="sxs-lookup"><span data-stu-id="411ad-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>
