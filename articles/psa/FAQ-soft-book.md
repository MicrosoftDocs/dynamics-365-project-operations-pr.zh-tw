---
title: 以未確認方式預約資源
description: 本主題提供有關如何對專案團隊成員進行暫訂排程或未確認預約的資訊。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 36246dadb1c4ba0234ae1042ba9e78c96f9d2bd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992867"
---
# <a name="soft-book-a-resource"></a><span data-ttu-id="6e5c2-103">以未確認方式預約資源</span><span class="sxs-lookup"><span data-stu-id="6e5c2-103">Soft book a resource</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6e5c2-104">您可透過暫訂方式將資源排程或「未確認預約」到專案團隊上，以顯示您計劃要將資源指派給專案。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-104">You can tentatively schedule or "soft book" a resource onto a project team to show that you plan to assign the resource to the project.</span></span> <span data-ttu-id="6e5c2-105">未確認預約不會耗用資源的可用產能，而且您可以將未確認預約的團隊成員指派給專案工作。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-105">Soft bookings don’t consume a resource’s available capacity, and you can assign soft-booked team members to project tasks.</span></span> <span data-ttu-id="6e5c2-106">不過，正因為未確認預約不耗用資源的產能，您仍可透過「已確認預約」方式來為其他工作預約同一期間內的資源。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-106">However, because soft booking doesn’t consume a resource’s capacity, you can still "hard book" the resource for other tasks within the same period.</span></span> <span data-ttu-id="6e5c2-107">一般資源無法進行未確認預約，而未確認預約也不能履行一般資源的要求。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-107">Generic resources can’t be soft booked, nor can a soft booking fulfill a request for a generic resource.</span></span>

<span data-ttu-id="6e5c2-108">未確認預約的專案團隊成員會在 **專案** 頁面的 **團隊** 索引標籤上列出，而其未確認預約時數則顯示在 **具名資源成員** 檢視表的 **未確認預約時數** 欄中。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-108">Soft-booked project team members are listed on the **Team** tab of the **Project** page, with their soft-booked hours shown in the **Soft Booked Hours** column in the **Named Team Members** view.</span></span> <span data-ttu-id="6e5c2-109">排程面板也會列出未確認預約的團隊成員。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-109">Soft-booked team members are also listed on the Schedule board.</span></span> <span data-ttu-id="6e5c2-110">因為這些成員已未確認預約，排程面板不會顯示任何對這些資源產能的耗用量。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-110">Because they are soft booked, the Schedule board doesn't show any consumption of capacity for these resources.</span></span> <span data-ttu-id="6e5c2-111">未確認預約的時間不會出現在 **協調** 索引標籤上，也不會顯示在排程面板 **協調** 索引標籤的 **延長預約** 欄位中。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-111">Soft-booked time doesn’t show up on the **Reconciliation** tab, nor is it shown in the **Extend Bookings** field in the **Reconciliation** tab of the Schedule board.</span></span> 

<span data-ttu-id="6e5c2-112">有兩種方式可以將團隊成員未確認預約到專案：直接透過排程面板，或在 **團隊** 索引標籤上新增團隊成員。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-112">There are two ways to soft book a team member onto a project: directly from the Schedule board, or by adding the team member on the **Team** tab.</span></span> 

## <a name="soft-book-from-the-schedule-board"></a><span data-ttu-id="6e5c2-113">透過排程面板進行未確認預約</span><span class="sxs-lookup"><span data-stu-id="6e5c2-113">Soft book from the Schedule board</span></span>
<span data-ttu-id="6e5c2-114">完成下列步驟，以透過排程面板對資源進行未確認預約。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-114">Complete the following steps to soft book a resource from the Schedule board.</span></span> 

1. <span data-ttu-id="6e5c2-115">開啟排程面板，然後在 **預約需求** 面板中選取 **專案** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-115">Open the Schedule board, and then in the **Booking Requirements** panel, select the **Project** tab.</span></span>
2. <span data-ttu-id="6e5c2-116">尋找您要以未確認方式為其預約資源的專案。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-116">Find the project for which you want to soft book a resource.</span></span> <span data-ttu-id="6e5c2-117">如果清單中有大量專案，請選取 **專案** 欄標題，然後使用篩選來搜尋一個或多個專案。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-117">If there are a large number of projects in the list, select the **Project** column header, and then use the filter to search for one or more projects.</span></span>
3. <span data-ttu-id="6e5c2-118">選取專案，然後將其拖放到資源的時間網格。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-118">Select the project, and then drag-and-drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="6e5c2-119">在 **建立資源預約** 面板中，調整開始和結束日期、將 **預約狀態** 設定為 **未確認**，然後設定時數。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-119">In the **Create Resource Booking** panel, adjust the start and end date, set the **Booking Status** to **Soft**, and then set the hours.</span></span> 
6. <span data-ttu-id="6e5c2-120">按一下 **預約**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-120">Click **Book**.</span></span> <span data-ttu-id="6e5c2-121">資源立即在 **團隊** 索引標籤上顯示為專案的資源。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-121">The resource now shows on the **Team** tab as a resource for the project.</span></span> <span data-ttu-id="6e5c2-122">在 **具名團隊成員** 檢視表上，您會看到 **未確認預約時數** 欄中的未確認預約時數。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-122">On the **Named Team Member** view you’ll see the soft-booked hours in the **Soft Booked Hours** column.</span></span>

> [!NOTE]
> <span data-ttu-id="6e5c2-123">您現在可以將未確認預約的資源指派給 **排程** 索引標籤上的工作。在 **協調** 索引標籤上，資源將會顯示相對於工作指派的預約短缺，因為 **協調** 索引標籤僅考慮已確認預約的情況。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-123">You can now assign the soft booked to tasks on the **Schedule** tab. On the **Reconciliation** tab, the resource shows a booking deficit relative to the task assignment as the **Reconciliation** tab only considers hard-bookings.</span></span> <span data-ttu-id="6e5c2-124">您可以使用 **延長預約** 功能對資源進行已確認預約，針對資源指派消除已確認預約的短缺情況。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-124">You can use the **Extend Bookings** feature to hard-book the resource to eliminate the deficit of hard-bookings against the resources assignments.</span></span> <span data-ttu-id="6e5c2-125">您需要使用 **維護預約**，手動取消資源的未確認預約。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-125">You’ll have to manually cancel the soft booking for the resource by using **Maintain Bookings**.</span></span>

## <a name="soft-book-on-the-team-tab"></a><span data-ttu-id="6e5c2-126">團隊索引標籤上的未確認預約</span><span class="sxs-lookup"><span data-stu-id="6e5c2-126">Soft book on the Team tab</span></span>

<span data-ttu-id="6e5c2-127">您可以直接在 **團隊** 索引標籤上新增團隊成員，然後使用 **維護預約** 將其預約狀態從 **已確認** 變更為 **未確認**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-127">You can add team members directly on the **Team** tab, and then change their booking status from **Hard** to **Soft** with **Maintain Bookings**.</span></span> <span data-ttu-id="6e5c2-128">依此方式新增團隊成員時，除非您選取的配置方法為 **無**，否則這永遠都會產生已確認預約。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-128">When you add a team member this way, it will always result in a hard-booking unless you select the allocation method as **None**.</span></span>

<span data-ttu-id="6e5c2-129">若要使用此方法，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-129">To use this method, complete the following steps.</span></span>

1. <span data-ttu-id="6e5c2-130">在 **專案** 頁面的 **團隊** 索引標籤上，按一下 **新增**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-130">On the **Project** page, on the **Team** tab, click **New**.</span></span>
2. <span data-ttu-id="6e5c2-131">選取可預約資源、角色、開始和結束日期。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-131">Select the bookable resource, the role, and the from and to dates.</span></span>
3. <span data-ttu-id="6e5c2-132">選取 **無** 以外的配置方法。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-132">Select an allocation method other than **None**.</span></span>
4. <span data-ttu-id="6e5c2-133">選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-133">Select **Save**.</span></span> <span data-ttu-id="6e5c2-134">您將會在網格上看到資源，而其時數會顯示在 **已確認預約時數** 欄中。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-134">You’ll see the resource on the grid and their hours in the **Hard Booked Hours** column.</span></span>
5. <span data-ttu-id="6e5c2-135">選取 **維護預約** 以維持資源的預約。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-135">Maintain the resource’s bookings by selecting **Maintain Bookings**.</span></span>
6. <span data-ttu-id="6e5c2-136">排程面板開啟時，展開資源以顯示其預約。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-136">When the Schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="6e5c2-137">您會看到預約顯示為 **已確認**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-137">You will see the booking shown as **Hard**.</span></span>
7. <span data-ttu-id="6e5c2-138">以滑鼠右鍵按一下預約、然後在 **變更狀態** 下，選取 **未確認預約**\>**未確認**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-138">Right-click the booking, and under **Change Status**, select **Soft Book** \> **Soft**.</span></span> <span data-ttu-id="6e5c2-139">預約狀態現在為 **未確認**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-139">The booking status is now **Soft**.</span></span>
8. <span data-ttu-id="6e5c2-140">關閉排程面板後，當您查看 **具名團隊成員** 檢視表時，會看到資源的時數已從 **已確認預約時數** 欄移至 **團隊** 索引標籤網格的 **未確認預約時數**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-140">After you close the Schedule board, you’ll see that the hours for the resource have moved from the **Hard Booked Hours** column to the **Soft Booked Hours** on the **Team** tab grid, when looking at the **Named Team Members** view.</span></span>

> [!NOTE]
> <span data-ttu-id="6e5c2-141">使用 **維護預約** 將狀態從 **已確認** 變更為 **未確認** 時，如果您透過已確認方式將資源預約到團隊，然後再將工作指派給資源，則會保留該資源的工作指派。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-141">When you use **Maintain Bookings** to change the status from **Hard** to **Soft**, if you hard-book a resource onto the team and then assign tasks to the resource, the task assignments for the resource are retained.</span></span> <span data-ttu-id="6e5c2-142">不過，在 **協調** 索引標籤中，資源會有預約短缺的情況，因為協調預約與指派時，只會考慮已確認預約。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-142">However, on the **Reconciliation** tab, the resource will have a booking deficiency because only hard-bookings are considered when reconciling bookings versus assignments.</span></span> <span data-ttu-id="6e5c2-143">您可以使用 **協調** 索引標籤上的 **延長預約** 功能對資源進行已確認預約，針對資源指派消除已確認預約的短缺情況。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-143">You can use the **Extend Bookings** feature on the **Reconciliation** tab to hard-book the resource to eliminate the deficit of hard bookings against the resources assignments.</span></span> <span data-ttu-id="6e5c2-144">您需要使用 **維護預約** 來取消資源的未確認預約。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-144">You’ll have to cancel the soft booking for the resource by using **Maintain Bookings**.</span></span>

<span data-ttu-id="6e5c2-145">當您準備好將未確認預約團隊成員資源變更為已確認預約團隊成員時，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="6e5c2-145">When you’re ready to change a soft-booked team member resource to a hard-booked team member, do the following:</span></span>

1. <span data-ttu-id="6e5c2-146">在排程面板上，展開資源以顯示其預約。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-146">On the Schedule board, expand the resource to show their bookings.</span></span> <span data-ttu-id="6e5c2-147">您將看到預約顯示為 **未確認**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-147">You’ll see the booking shown as **Soft**.</span></span>
2. <span data-ttu-id="6e5c2-148">以滑鼠右鍵按一下預約、在 **變更狀態** 下選取 **已確認預約**\>**已確認**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-148">Right-click the booking, and under **Change Status**, select **Hard Book** \> **Hard**.</span></span> <span data-ttu-id="6e5c2-149">預約狀態現在為 **已確認**。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-149">The booking status is now **Hard**.</span></span>
3. <span data-ttu-id="6e5c2-150">關閉排程面板、回到專案並開啟 **團隊** 索引標籤之後，當您進入 **具名團隊成員** 檢視表時，會看到資源的時數已從 **未確認預約時數** 欄移到 **團隊** 索引標籤的 **已確認預約時數** 欄。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-150">After you close the Schedule board, return to the project, and open the **Team** tab, you’ll see that the hours for the resource have moved from the **Soft Booked Hours** column to the **Hard Booked Hours** column on the **Team** tab when in the **Named Team Members** view.</span></span> <span data-ttu-id="6e5c2-151">如果資源已指派給工作，這些資源在 **協調** 索引標籤上將不再顯示預約短缺，因為其預約現在是已確認預約。</span><span class="sxs-lookup"><span data-stu-id="6e5c2-151">If the resource was assigned to tasks, they’ll no longer show a booking deficit on the **Reconciliation** tab as their bookings are now hard.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]