---
title: 複製專案
description: 本主題提供有關在 Dynamics 365 Project Operations 中複製專案的資訊。
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072937"
---
# <a name="copy-a-project"></a><span data-ttu-id="114ae-103">複製專案</span><span class="sxs-lookup"><span data-stu-id="114ae-103">Copy a project</span></span>

<span data-ttu-id="114ae-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="114ae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="114ae-105">有了 Dynamics 365 Project Operations，您就可以選取 **專案** 表單上的 **複製專案** 快速建置新的專案。</span><span class="sxs-lookup"><span data-stu-id="114ae-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="114ae-106">若要複製專案，請開啟想要複製的專案，然後選取 **複製專案** 。</span><span class="sxs-lookup"><span data-stu-id="114ae-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="114ae-107">此動作會複製：</span><span class="sxs-lookup"><span data-stu-id="114ae-107">The action will copy:</span></span>

- <span data-ttu-id="114ae-108">專案屬性</span><span class="sxs-lookup"><span data-stu-id="114ae-108">Project properties</span></span>
- <span data-ttu-id="114ae-109">分工結構圖</span><span class="sxs-lookup"><span data-stu-id="114ae-109">The Work breakdown structure</span></span>
- <span data-ttu-id="114ae-110">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="114ae-110">Project team members</span></span>
- <span data-ttu-id="114ae-111">專案估計值</span><span class="sxs-lookup"><span data-stu-id="114ae-111">Project estimates</span></span>
- <span data-ttu-id="114ae-112">專案費用估計</span><span class="sxs-lookup"><span data-stu-id="114ae-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="114ae-113">專案屬性</span><span class="sxs-lookup"><span data-stu-id="114ae-113">Project properties</span></span>

<span data-ttu-id="114ae-114">複製專案時，會複製下列欄位中的值：</span><span class="sxs-lookup"><span data-stu-id="114ae-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="114ae-115">名字</span><span class="sxs-lookup"><span data-stu-id="114ae-115">Name</span></span>
- <span data-ttu-id="114ae-116">描述</span><span class="sxs-lookup"><span data-stu-id="114ae-116">Description</span></span>
- <span data-ttu-id="114ae-117">客戶</span><span class="sxs-lookup"><span data-stu-id="114ae-117">Customer</span></span>
- <span data-ttu-id="114ae-118">行事曆範本</span><span class="sxs-lookup"><span data-stu-id="114ae-118">Calendar Template</span></span>
- <span data-ttu-id="114ae-119">貨幣</span><span class="sxs-lookup"><span data-stu-id="114ae-119">Currency</span></span>
- <span data-ttu-id="114ae-120">合約單位</span><span class="sxs-lookup"><span data-stu-id="114ae-120">Contracting Unit</span></span>
- <span data-ttu-id="114ae-121">專案經理</span><span class="sxs-lookup"><span data-stu-id="114ae-121">Project Manager</span></span>
- <span data-ttu-id="114ae-122">Status</span><span class="sxs-lookup"><span data-stu-id="114ae-122">Status</span></span>
- <span data-ttu-id="114ae-123">整體專案狀態</span><span class="sxs-lookup"><span data-stu-id="114ae-123">Overall Project Status</span></span>
- <span data-ttu-id="114ae-124">註解</span><span class="sxs-lookup"><span data-stu-id="114ae-124">Comments</span></span>
- <span data-ttu-id="114ae-125">估計值</span><span class="sxs-lookup"><span data-stu-id="114ae-125">Estimates</span></span>
- <span data-ttu-id="114ae-126">估計開始日期</span><span class="sxs-lookup"><span data-stu-id="114ae-126">Estimated Start Date</span></span>
- <span data-ttu-id="114ae-127">完成日期</span><span class="sxs-lookup"><span data-stu-id="114ae-127">Finish Date</span></span>
- <span data-ttu-id="114ae-128">投入 (小時)</span><span class="sxs-lookup"><span data-stu-id="114ae-128">Effort (Hours)</span></span>
- <span data-ttu-id="114ae-129">估計人力成本</span><span class="sxs-lookup"><span data-stu-id="114ae-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="114ae-130">估計費用成本</span><span class="sxs-lookup"><span data-stu-id="114ae-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="114ae-131">分工結構圖</span><span class="sxs-lookup"><span data-stu-id="114ae-131">Work breakdown structure</span></span>

<span data-ttu-id="114ae-132">複製專案時，會複製整個資源載入的分工結構圖。</span><span class="sxs-lookup"><span data-stu-id="114ae-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="114ae-133">具名資源會以一般資源來取代。</span><span class="sxs-lookup"><span data-stu-id="114ae-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="114ae-134">如果具名資源的工作時數與一般資源的不同，則會重新計算排程，而且工作期間可能會變更。</span><span class="sxs-lookup"><span data-stu-id="114ae-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="114ae-135">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="114ae-135">Project team members</span></span>

<span data-ttu-id="114ae-136">從來源專案複製專案團隊時，會複製一般資源。</span><span class="sxs-lookup"><span data-stu-id="114ae-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="114ae-137">一般資源指派也會保持與原先在來源專案中的一樣。</span><span class="sxs-lookup"><span data-stu-id="114ae-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="114ae-138">具名資源將會轉換為一般團隊成員。</span><span class="sxs-lookup"><span data-stu-id="114ae-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="114ae-139">估計值</span><span class="sxs-lookup"><span data-stu-id="114ae-139">Estimates</span></span>

<span data-ttu-id="114ae-140">複製專案時，會從來源專案複製資源及費用估計明細。</span><span class="sxs-lookup"><span data-stu-id="114ae-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="114ae-141">如需有關如何以程式設計方式存取 [複製專案] 的詳細資訊，請參閱[使用 [複製專案] 開發專案範本](dev-copy-project.md)。</span><span class="sxs-lookup"><span data-stu-id="114ae-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>
