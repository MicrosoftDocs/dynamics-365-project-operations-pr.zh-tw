---
title: 協調預約和指派
description: 本主題提供有關實際值的資訊。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 73cbc89ae4350cbd568f1bb978825ff53da07afb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008886"
---
# <a name="reconcile-bookings-and-assignments"></a><span data-ttu-id="3b4dd-103">協調預約和指派</span><span class="sxs-lookup"><span data-stu-id="3b4dd-103">Reconcile bookings and assignments</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3b4dd-104">專案團隊成員的專案預約與專案工作指派聯繫鬆散。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-104">A project team member's project bookings and project task assignments are loosely coupled.</span></span> <span data-ttu-id="3b4dd-105">因此，資源可以有未對應於預約的工作指派，以及未對應於工作指派的預約。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-105">Therefore, a resource can have task assignments that don't correspond to bookings and bookings that don't correspond to task assignments.</span></span> <span data-ttu-id="3b4dd-106">專案預約與指派最好是一致，讓資源有已認可產能來執行其工作指派。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-106">Ideally, project bookings and assignments are aligned, so that resources have committed capacity to perform their task assignments.</span></span> <span data-ttu-id="3b4dd-107">不過，實際狀況是預約可以根據可用性來進行，而工作計時也可以隨著專案在生命週期中持續進行時變更。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-107">However, the reality is that bookings can occur based on availability, and task timings can change as the project continues through its lifecycle.</span></span> <span data-ttu-id="3b4dd-108">因此鬆散聯繫可以提供彈性。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-108">Therefore, the loose coupling allows for flexibility.</span></span>

<span data-ttu-id="3b4dd-109">由於專案預約與工作指派聯繫鬆散，因此 **協調** 索引標籤會包含在專案實體中。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-109">Because of the loose coupling of project bookings and task assignments, a **Reconciliation** tab is included on the Project entity.</span></span> <span data-ttu-id="3b4dd-110">此索引標籤可讓專案經理協調團隊成員的預約及其對專案團隊的指派。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-110">This tab helps project managers reconcile team members' bookings and their assignments for their project team.</span></span>

<span data-ttu-id="3b4dd-111">**協調** 索引標籤會針對每個具名團隊成員顯示下至個別工作指派的預約及指派。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-111">For each named team member, the **Reconciliation** tab shows bookings and assignments down to the individual task assignment.</span></span> <span data-ttu-id="3b4dd-112">它會在儲存格中顯示可表示從月數下至天數期間的時數。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-112">It shows hours in cells that can represent periods from months down to days.</span></span>

<span data-ttu-id="3b4dd-113">在 **時幅** 欄位中，您可以選取 **月**、**週** 或 **日**。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-113">In the **Timescale** field, you can select **Month**, **Week**, or **Day**.</span></span> <span data-ttu-id="3b4dd-114">預設會選取 **週**。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-114">By default, **Week** is selected.</span></span> <span data-ttu-id="3b4dd-115">不過，您可以選取 **設定** 按鈕來變更預設值。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-115">However, you can change the default value by selecting the **Settings** button.</span></span> <span data-ttu-id="3b4dd-116">**協調** 索引標籤開啟時，會顯示目前的日期，但您可以使用行事曆控制項向前或向後移動時間。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-116">When the **Reconciliation** tab is opened, it shows the current date, but you can use the calendar control to move forward or backward in time.</span></span> <span data-ttu-id="3b4dd-117">專案的開始日期在未來時，索引標籤會顯示其開啟時的日期。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-117">When a project has a start date that is in the future, the tab shows that date when it's opened.</span></span> <span data-ttu-id="3b4dd-118">行事曆控制項也有選項可讓您移至專案的開始和結束日期。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-118">The calendar control also has options that let you move to the project start and end dates.</span></span>

<span data-ttu-id="3b4dd-119">您可以對每個資源使用展開器控制項來顯示資源的預約詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-119">You can use the expander controls on each resource to show the details of that resource's bookings.</span></span> <span data-ttu-id="3b4dd-120">您也可以將每個資源的指派展開至個別工作的層級。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-120">You can also expand each resource's assignments to the level of the individual task.</span></span>

<span data-ttu-id="3b4dd-121">**協調** 索引標籤的底端會顯示專案的整體淨總數，而索引標籤也包含總計欄。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-121">The bottom of the **Reconciliation** tab shows an overall net total for the project, and the tab also includes a total column.</span></span> <span data-ttu-id="3b4dd-122">對於每項資源，此索引標籤會計算專案上團隊成員預約與團隊成員工作指派彙總之間的差異。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-122">For each resource, the tab takes the difference between a team member's bookings on the project and rollup of that team member's task assignments.</span></span> <span data-ttu-id="3b4dd-123">此差異最好是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-123">Ideally, the difference should be 0 (zero).</span></span> <span data-ttu-id="3b4dd-124">換句話說，資源預約與工作指派之間應該要沒有差異。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-124">In other words, there should be no difference between the resource's bookings and its task assignments.</span></span> <span data-ttu-id="3b4dd-125">任何差異都會用色彩和陰影表示，以調出兩種條件：</span><span class="sxs-lookup"><span data-stu-id="3b4dd-125">Any differences are indicated by color and shading to call out two conditions:</span></span>

- <span data-ttu-id="3b4dd-126">**預約不足** – 當資源的指派數超過預約數時，就會發生預約短缺。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-126">**Booking shortage** – Booking shortages occur when a resource has more assignments than bookings.</span></span> <span data-ttu-id="3b4dd-127">由於尚未保留此產能，專案經理可能需要延長資源的預約以彌補短缺來更正此情況。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-127">Because this capacity hasn't been reserved, a project manager can correct this condition by extending the resource's bookings to cover the shortage.</span></span>
- <span data-ttu-id="3b4dd-128">**超額預約** – 當資源已預約給專案，但尚未指派給工作時，會發生超額預約。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-128">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="3b4dd-129">例如，如果已在工作指派發生之前預約資源，則可以接受此條件。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-129">This condition might be acceptable if, for example, the resource has been booked before task assignment occurs.</span></span> <span data-ttu-id="3b4dd-130">不過，在其他情況下，可能並未規劃要指派資源。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-130">However, in other cases, the resource might not be planned to be assigned.</span></span> <span data-ttu-id="3b4dd-131">在這些情況下，專案經理應考慮取消資源的預約，讓該產能可以用於其他專案。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-131">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

> [!NOTE]
> <span data-ttu-id="3b4dd-132">這些條件的圖例可能會隱藏，以便為網格留出更多空間。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-132">The legend for these conditions might be hidden to leave more room for the grid.</span></span> <span data-ttu-id="3b4dd-133">在這種情況下，您可以選取 **設定** 按鈕讓圖例顯示出來。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-133">In this case, you can make the legend visible by selecting the **Settings** button.</span></span>

<span data-ttu-id="3b4dd-134">在某些情況下，將 **時幅** 欄位設定為高於 **天** 的層級時，可能會計算出差額為 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-134">In some cases, when the **Timescale** field is set to a level that is higher than **Day**, differences might be calculated as 0 (zero).</span></span> <span data-ttu-id="3b4dd-135">例如，在 **月** 層級上，資源的淨差可能會是 0 (零)，表示該預約等於指派。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-135">For example, at the **Month** level, the net difference for a resource might be 0 (zero) to indicate that bookings equal assignments.</span></span> <span data-ttu-id="3b4dd-136">不過，如果以 **週** 層級來檢視，您可能會在當月第一週看到 0 (零) 小時的指派以及 40 小時的預約，並在當月第二週看到 40 小時的指派以及 0 (零) 小時的預約。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-136">However, if you look at the **Week** level, you might see that there are assignments of 0 (zero) hours and bookings of 40 hours in the first week of the month, and assignments of 40 hours and bookings of 0 (zero) hours in the second week of the month.</span></span> <span data-ttu-id="3b4dd-137">雖然月的預約與指派都相等，但以週來看，便會不同。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-137">Although the total bookings and assignments for the month are equal, they differ by week.</span></span>

<span data-ttu-id="3b4dd-138">檢視較高時間層級時，**協調** 索引標籤會顯示儲存格指示器，通知您較低時間層級上有差異。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-138">When you view higher time levels, the **Reconciliation** tab shows a cell indicator to notify you that there are differences at lower time levels.</span></span> <span data-ttu-id="3b4dd-139">例如，在下圖中，名為「黃文珍」的資源有儲存格指示器出現於 2018 年 10 月的月份儲存格。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-139">For example, in the following illustration, a cell indicator appears in the cell for the month of October 2018 for the resource that is named Katelyn Merritt.</span></span> <span data-ttu-id="3b4dd-140">因此，您可以看到，即使資源的預約與指派在 **月** 層級進行彙總時相等，但在較低層級上卻不相符。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-140">Therefore, you can see that, even though the resource's bookings and assignments are equal when they are aggregated at the **Month** level, they don't match at lower levels.</span></span>

![在每月層級上不相符的預約與指派](media/reconcile-assignments-01.JPG)

<span data-ttu-id="3b4dd-142">按兩下儲存格以放大到下一個較低層級，並檢視差異。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-142">Double-click a cell to zoom in to the next lower level and view the difference.</span></span> <span data-ttu-id="3b4dd-143">例如，如果按兩下黃文珍的 2018 年 10 月差異，就會向下切入到 **週** 層級。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-143">For example, if you double-click the October 2018 difference for Katelyn Merritt, you drill down to the **Week** level.</span></span> <span data-ttu-id="3b4dd-144">接著可以看到資源的預約時間為 16 小時，但在 10 月前兩週中沒有任何指派，而在 10 月第三週有 16 小時指派但沒有任何預約。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-144">You can then see that the resource has bookings of 16 hours but no assignments in the first two weeks of October, and 16 hours of assignments but no bookings in the third week of October.</span></span>

![在每週層級上不相符的預約與指派](media/reconcile-assignments-02.JPG)

<span data-ttu-id="3b4dd-146">您可以在儲存格上按一下滑鼠右鍵，縮小到下一個較高層級。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-146">You can right-click a cell to zoom out the next higher level.</span></span> <span data-ttu-id="3b4dd-147">您也可以選取 **設定** 按鈕來關閉儲存格指示器。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-147">You can also turn off the cell indicator by selecting the **Settings** button.</span></span> 

<span data-ttu-id="3b4dd-148">您也可以使用網格上方的 **上一個** 和 **下一個** 按鈕，移動瀏覽專案中的任何差異。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-148">You can also use the **Previous** and **Next** buttons above the grid to move through any differences in your project.</span></span> <span data-ttu-id="3b4dd-149">若要使用這些按鈕，您必須先選取資源。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-149">To use these buttons, you must first select a resource.</span></span> <span data-ttu-id="3b4dd-150">選取 **下一個** 移至該資源預約與指派之間的下一個差異。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-150">Select **Next** to go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="3b4dd-151">選取 **上一個** 以移至上一個差異。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-151">Select **Previous** to go to the previous difference.</span></span>

<span data-ttu-id="3b4dd-152">在資源有工作指派但沒有預約的狀況下，您可以選取預訂短缺，然後選取 **延長預約**。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-152">In situations where you have task assignments for a resource but no bookings, you can select the booking shortage and then select **Extend Booking**.</span></span> <span data-ttu-id="3b4dd-153">您可以接著查看所需的預約以解決資源的短缺。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-153">You can then see the booking that is required in order to address the resource's shortage.</span></span> <span data-ttu-id="3b4dd-154">您也可以檢視資源在目前專案和其他專案上的預約。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-154">You can also view the resource's bookings on the current project and other projects.</span></span> <span data-ttu-id="3b4dd-155">選取 **確定**，為資源建立預約，但不考慮目前的可用性。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-155">Select **OK** to create the booking for the resource without regard to current availability.</span></span> <span data-ttu-id="3b4dd-156">專案經理或資源管理員可以接著使用排程面板，管理資源因其預約延長而變成過量預約超過其產能的狀況。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-156">The project manager or resource manager can then use Schedule Board to manage situations where a resource has become overbooked beyond capacity because its bookings were extended.</span></span>

## <a name="managing-with-time-zones"></a><span data-ttu-id="3b4dd-157">使用時區進行管理</span><span class="sxs-lookup"><span data-stu-id="3b4dd-157">Managing with time zones</span></span>
<span data-ttu-id="3b4dd-158">為了確保在使用延長預約時產生準確且可預測的結果，必須符合兩個重要的先決條件：</span><span class="sxs-lookup"><span data-stu-id="3b4dd-158">To ensure accurate and predictable results when using Extend Booking, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="3b4dd-159">使用者必須設定其裝置的時區，使其符合系統的個人化設定中所定義的時區。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-159">The user must configure their device's time zone to match the time zone defined in your system's Personalization Settings.</span></span>
 
  ![Windows 10 的時區設定](media/reconcile-assignments-03.png)

  ![個人化設定中的時區設定](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="3b4dd-162">可預約資源至少必須有一分鐘的工作時間，與用於定義所要求之展延的分佈重疊。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-162">The Bookable Resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="3b4dd-163">例如，下列範例顯示上班時間落在上午 9:00 到下午 7:00 之間的評論資源。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-163">For instance, the following example shows review resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![資源分佈的比較](media/reconcile-assignments-05.png)

<span data-ttu-id="3b4dd-165">下表顯示：</span><span class="sxs-lookup"><span data-stu-id="3b4dd-165">The following table shows:</span></span>

- <span data-ttu-id="3b4dd-166">專案行事曆範本。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-166">A project calendar template.</span></span>
- <span data-ttu-id="3b4dd-167">資源 A：此資源有相同的行事曆，並且與專案位於同一個時區。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-167">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="3b4dd-168">此預約的開始時間會是上午 9:00。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-168">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="3b4dd-169">資源 B：此資源與專案位於不同的時區，因此開始時間是從他們時區的上午 7:00 起算。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-169">Resources B: This resource is located in a different time zone than the project and therefore starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="3b4dd-170">不過，這些預約會從上午 9:00 開始，因為這是指派分佈的最早開始時間。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-170">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="3b4dd-171">資源 C 和 D：這些資源同樣位於不同的時區，不僅彼此互異，也與專案有所不同，他們的預訂開始時間不早於各自的可用開始時間。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-171">Resources C and D: The resources are also located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="3b4dd-172">實體</span><span class="sxs-lookup"><span data-stu-id="3b4dd-172">Entity</span></span>  |<span data-ttu-id="3b4dd-173">行事曆</span><span class="sxs-lookup"><span data-stu-id="3b4dd-173">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="3b4dd-174">專案行事曆範本</span><span class="sxs-lookup"><span data-stu-id="3b4dd-174">Project calendar template</span></span>   | ![專案行事曆](media/reconcile-assignments-06.png) |
|<span data-ttu-id="3b4dd-176">資源 A</span><span class="sxs-lookup"><span data-stu-id="3b4dd-176">Resource A</span></span>  | ![資源 A 行事曆](media/reconcile-assignments-06.png) |
|<span data-ttu-id="3b4dd-178">資源 B</span><span class="sxs-lookup"><span data-stu-id="3b4dd-178">Resource B</span></span>  |  ![資源 B 行事曆](media/reconcile-assignments-07.png) |
|<span data-ttu-id="3b4dd-180">資源 C</span><span class="sxs-lookup"><span data-stu-id="3b4dd-180">Resource C</span></span>  |  ![資源 C 行事曆](media/reconcile-assignments-08.png) |
|<span data-ttu-id="3b4dd-182">資源 D</span><span class="sxs-lookup"><span data-stu-id="3b4dd-182">Resource D</span></span>  | ![資源 D 行事曆](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="3b4dd-184">當您瀏覽至協調檢視表時，將會顯示資源指派和相關的預約不足。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-184">When you navigate to the reconciliation view, the resource assignments and the associated booking shortages will be displayed.</span></span>
 <span data-ttu-id="3b4dd-185">![延長前的協調檢視表](media/reconcile-assignments-10.png)</span><span class="sxs-lookup"><span data-stu-id="3b4dd-185">![Reconciliation view before extension](media/reconcile-assignments-10.png)</span></span>

<span data-ttu-id="3b4dd-186">對每個資源執行 [延長預約] 功能之後，就會成功延長每個資源的預約。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-186">After the Extend Booking functionality has been executed on each resource, bookings are successfully extended for each resource.</span></span> <span data-ttu-id="3b4dd-187">這是因為每個資源的工作時數都會與短缺分佈重疊。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-187">This is because each resource’s working hours overlapped with the contours of the shortage.</span></span>
 <span data-ttu-id="3b4dd-188">![展長後的協調檢視表](media/reconcile-assignments-11.png)</span><span class="sxs-lookup"><span data-stu-id="3b4dd-188">![Reconciliation view after booking extension](media/reconcile-assignments-11.png)</span></span> 

<span data-ttu-id="3b4dd-189">不過，如果更仔細查看預約的詳細資料，就會了解預約開始時間中的差異。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-189">However, a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="3b4dd-190">這些預約的開始時間不會早於指派分佈的開始時間，也不會早於資源的可用開始時間。</span><span class="sxs-lookup"><span data-stu-id="3b4dd-190">The bookings will start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>
 <span data-ttu-id="3b4dd-191">![資源在排程面板中的新預約](media/reconcile-assignments-12.png)</span><span class="sxs-lookup"><span data-stu-id="3b4dd-191">![New bookings of the resources in the schedule board](media/reconcile-assignments-12.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]