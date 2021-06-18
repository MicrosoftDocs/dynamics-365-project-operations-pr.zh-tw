---
title: 維護團隊成員
description: 本主題提供有關將具名可預約資源預約給專案團隊以及將這些資源指派至工作的資訊。
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 00312c5a701768e0042e7e0236477c192690ded3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998626"
---
# <a name="maintain-team-members"></a><span data-ttu-id="fd8ae-103">維護團隊成員</span><span class="sxs-lookup"><span data-stu-id="fd8ae-103">Maintain team members</span></span>

<span data-ttu-id="fd8ae-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="fd8ae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fd8ae-105">您可以直接預約具名資源給團隊，以將此資源新增至團隊。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="fd8ae-106">在 Dynamics 365 Project Operations 中，移至 **專案**，然後選取並開啟您要預約到的專案。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="fd8ae-107">在 **專案** 頁面的 **團隊** 索引標籤上，選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="fd8ae-108">在 **快速建立專案團隊成員** 對話方塊中，選取可預約資源。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="fd8ae-109">**角色** 欄位將會有資源的預設角色填入 (如果已指派此角色)。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="fd8ae-110">您可以變更角色。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-110">You can change the role.</span></span> 
4. <span data-ttu-id="fd8ae-111">選取需要資源的開始及結束日期，並選取資源產能的配置方法。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="fd8ae-112">如果您要讓團隊成員成為專案核准者，請在 **專案核准者** 欄位中選取 **是**。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="fd8ae-113">團隊成員可以核准為此專案提交的時間和費用項目。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="fd8ae-114">選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-114">Select **Save**.</span></span>

<span data-ttu-id="fd8ae-115">您現在可以將預約的資源指派給專案中的工作。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="fd8ae-116">在 **專案** 頁面的 **排程** 索引標籤上，將工作指派給新的資源。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="fd8ae-117">從工作網格中 **資源** 欄位啟動的資源選擇器將會顯示您可以選取的團隊成員。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="fd8ae-118">在 Project Operations 中，資源預約和工作指派並非緊密聯繫。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="fd8ae-119">使用排程中的資源選擇器時，您可以將超過團隊成員預約對專案所能支援之時數的工作指派給該團隊成員。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="fd8ae-120">團隊成員預約與指派之間的差異會顯示在 **團隊** 和 **資源調節** 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="fd8ae-121">您也可以在更詳細的層級上協調資源預約與指派之間的差異。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="fd8ae-122">使用 **排程** 索引標籤上的資源選擇器來搜尋和選取尚不屬於專案團隊的可預約資源。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="fd8ae-123">這些資源會在資源選擇器中顯示為 **其他資源**。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="fd8ae-124">當您進行選擇時，資源會新增至專案團隊並指派給工作，但不會產生任何預約。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="fd8ae-125">您可以使用 **協調** 索引標籤的延長預約功能或是 **排程面板**，將資源的產能預約給專案。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="fd8ae-126">在專案上預約您的團隊成員之後，您可以使用 **維護預約** 或直接使用 **排程面板** 來管理其預約。</span><span class="sxs-lookup"><span data-stu-id="fd8ae-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]