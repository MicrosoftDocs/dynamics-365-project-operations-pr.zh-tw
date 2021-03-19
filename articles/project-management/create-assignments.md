---
title: 建立資源指派
description: 本主題提供有關建立一般及具名資源指派的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a6f4f12a962cb570e8b83d8ee7a01fc0cc2c6155
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287093"
---
# <a name="create-resource-assignments"></a><span data-ttu-id="7886c-103">建立資源指派</span><span class="sxs-lookup"><span data-stu-id="7886c-103">Create resource assignments</span></span>

<span data-ttu-id="7886c-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="7886c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7886c-105">資源指派是專案團隊成員與分葉節點工作的直接關聯。</span><span class="sxs-lookup"><span data-stu-id="7886c-105">A resource assignment is the direct association of a project team member to a leaf node task.</span></span> <span data-ttu-id="7886c-106">本主題提供有關不同指派資源方式的資訊。</span><span class="sxs-lookup"><span data-stu-id="7886c-106">This topic provides information about the different ways to assign resources.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="7886c-107">透過工作指派建立一般團隊成員</span><span class="sxs-lookup"><span data-stu-id="7886c-107">Create a generic team member through task assignment</span></span>


<span data-ttu-id="7886c-108">透過工作指派建立一般團隊成員時，您會建立預留位置或一般資源。</span><span class="sxs-lookup"><span data-stu-id="7886c-108">When you create a generic team member through task assignment, you create a placeholder or generic resource.</span></span> <span data-ttu-id="7886c-109">此一般資源描述您最終要在工作上使用之具名資源的特性。</span><span class="sxs-lookup"><span data-stu-id="7886c-109">This generic resource describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="7886c-110">您接著會產生用來搜尋並預約具名資源的需求 (或使用需求送出要求)。</span><span class="sxs-lookup"><span data-stu-id="7886c-110">You then generate a requirement, or submit a request using the requirement, that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="7886c-111">在工作的排程網格中，選取 **資源** 儲存格中的資源圖示。</span><span class="sxs-lookup"><span data-stu-id="7886c-111">On the Schedule grid for a task, select the Resource icon in the **Resource** cell.</span></span>
2. <span data-ttu-id="7886c-112">輸入要做為預留位置資源名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="7886c-112">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="7886c-113">例如，「方案經理」。</span><span class="sxs-lookup"><span data-stu-id="7886c-113">For example, Program Manager.</span></span>
3. <span data-ttu-id="7886c-114">選取 **建立**，並在右側的 **快速建立專案團隊成員** 欄位中，設定一般資源的角色。</span><span class="sxs-lookup"><span data-stu-id="7886c-114">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>
4. <span data-ttu-id="7886c-115">在工作的 **資源選取器** 上選取資源，視需要將工作指派給此預留位置資源。</span><span class="sxs-lookup"><span data-stu-id="7886c-115">Assign tasks as needed to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="7886c-116">**團隊成員** 下方列出的資源。</span><span class="sxs-lookup"><span data-stu-id="7886c-116">The resources listed under **Team Members**.</span></span>
5. <span data-ttu-id="7886c-117">完成指派一般資源時，選取 **團隊** 索引標籤上的一般資源，然後選取 **產生需求** 以建立一般資源的資源需求。</span><span class="sxs-lookup"><span data-stu-id="7886c-117">When you’re finished assigning the generic resource, on the **Team** tab, select the generic resource, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>
6. <span data-ttu-id="7886c-118">選取一般資源的 **預約**，然後使用排程面板來尋找並預約實際資源。</span><span class="sxs-lookup"><span data-stu-id="7886c-118">Select **Book** for the generic resource and then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="7886c-119">您也可以送出要求資源管理員履行的需求。</span><span class="sxs-lookup"><span data-stu-id="7886c-119">You can also submit the requirement for fulfillment by a resource manager.</span></span>
7. <span data-ttu-id="7886c-120">使用具名資源完全履行一般資源 (部分資源需求履行不會產生資源指派) 時，一般資源會從團隊中移除。</span><span class="sxs-lookup"><span data-stu-id="7886c-120">When the generic resource is fully fulfilled (partial resource requirement fulfillment will not result in a resource assignment) with a named resource, the generic resource is removed from the team.</span></span> <span data-ttu-id="7886c-121">一般資源的工作指派會指派給履行一般資源之資源需求的具名資源。</span><span class="sxs-lookup"><span data-stu-id="7886c-121">The task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="7886c-122">從所有可預約資源清單中指派具名預約</span><span class="sxs-lookup"><span data-stu-id="7886c-122">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="7886c-123">您可以使用 **資源選擇器** 中的搜尋方塊，搜尋所有使用中可預約資源，並將這些資源指派給任何分葉節點工作。</span><span class="sxs-lookup"><span data-stu-id="7886c-123">You can use the search box in the **Resource Picker** to search all active bookable resources and assign them to any leaf node task.</span></span> <span data-ttu-id="7886c-124">以此方式指派的資源會新增至沒有任何預約的團隊。</span><span class="sxs-lookup"><span data-stu-id="7886c-124">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="7886c-125">這類似於新增團隊成員後，再選取 **無** 做為配置方法。</span><span class="sxs-lookup"><span data-stu-id="7886c-125">This is similar to adding a team member and selecting **None** as the allocation method.</span></span> <span data-ttu-id="7886c-126">資源會在 **團隊**、**資源指派** 和 **協調** 索引標籤中顯示為只有指派且預約短缺的資源。</span><span class="sxs-lookup"><span data-stu-id="7886c-126">The resource is displayed on the **Team**, **Resource Assignment**, and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="7886c-127">如果您想要使用其可用產能，請加以預約。</span><span class="sxs-lookup"><span data-stu-id="7886c-127">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="7886c-128">從工作網格、面板或時間表，瀏覽至 **指派至** 儲存格。</span><span class="sxs-lookup"><span data-stu-id="7886c-128">From the task grid, board, or timeline, navigate to the **Assigned To** cell.</span></span>
2. <span data-ttu-id="7886c-129">在搜尋方塊中，開始輸入名稱。</span><span class="sxs-lookup"><span data-stu-id="7886c-129">In the search box, start typing a name.</span></span> <span data-ttu-id="7886c-130">該名稱的搜尋結果會顯示在 **資源選取器** 的 **其他資源** 下方。</span><span class="sxs-lookup"><span data-stu-id="7886c-130">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>
3. <span data-ttu-id="7886c-131">選取您要指派給工作的資源，或選取 **其他團隊資源** 底下的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7886c-131">Select the resource that you want to assign to the task or select the name of the resource under **Other Team Resources**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]