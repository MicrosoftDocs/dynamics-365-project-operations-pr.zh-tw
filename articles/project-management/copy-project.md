---
title: 複製專案
description: 本主題提供有關在 Dynamics 365 Project Operations 中複製專案的資訊。
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091244"
---
# <a name="copy-a-project"></a><span data-ttu-id="2b81a-103">複製專案</span><span class="sxs-lookup"><span data-stu-id="2b81a-103">Copy a project</span></span>

<span data-ttu-id="2b81a-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="2b81a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2b81a-105">在 Dynamics 365 Project Operations 中，您可以選取 **專案** 表單上的 **複製專案**，快速建置新專案。</span><span class="sxs-lookup"><span data-stu-id="2b81a-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="2b81a-106">若要複製專案，請開啟想要複製的專案，然後選取 **複製專案**。</span><span class="sxs-lookup"><span data-stu-id="2b81a-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="2b81a-107">此動作會複製下列項目：</span><span class="sxs-lookup"><span data-stu-id="2b81a-107">The action will copy the following:</span></span>

- <span data-ttu-id="2b81a-108">專案屬性</span><span class="sxs-lookup"><span data-stu-id="2b81a-108">Project properties</span></span> 
- <span data-ttu-id="2b81a-109">分工結構圖</span><span class="sxs-lookup"><span data-stu-id="2b81a-109">Work breakdown structure</span></span>
- <span data-ttu-id="2b81a-110">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="2b81a-110">Project team members</span></span>
- <span data-ttu-id="2b81a-111">專案估計值</span><span class="sxs-lookup"><span data-stu-id="2b81a-111">Project estimates</span></span>
- <span data-ttu-id="2b81a-112">專案費用估計</span><span class="sxs-lookup"><span data-stu-id="2b81a-112">Project expense estimates</span></span>
- <span data-ttu-id="2b81a-113">專案材料估計值</span><span class="sxs-lookup"><span data-stu-id="2b81a-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="2b81a-114">專案屬性</span><span class="sxs-lookup"><span data-stu-id="2b81a-114">Project properties</span></span>

<span data-ttu-id="2b81a-115">複製專案時，會複製下列欄位中的值：</span><span class="sxs-lookup"><span data-stu-id="2b81a-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="2b81a-116">名字</span><span class="sxs-lookup"><span data-stu-id="2b81a-116">Name</span></span>
- <span data-ttu-id="2b81a-117">描述</span><span class="sxs-lookup"><span data-stu-id="2b81a-117">Description</span></span>
- <span data-ttu-id="2b81a-118">客戶</span><span class="sxs-lookup"><span data-stu-id="2b81a-118">Customer</span></span>
- <span data-ttu-id="2b81a-119">行事曆範本</span><span class="sxs-lookup"><span data-stu-id="2b81a-119">Calendar Template</span></span>
- <span data-ttu-id="2b81a-120">貨幣</span><span class="sxs-lookup"><span data-stu-id="2b81a-120">Currency</span></span>
- <span data-ttu-id="2b81a-121">合約單位</span><span class="sxs-lookup"><span data-stu-id="2b81a-121">Contracting Unit</span></span>
- <span data-ttu-id="2b81a-122">專案經理</span><span class="sxs-lookup"><span data-stu-id="2b81a-122">Project Manager</span></span>
- <span data-ttu-id="2b81a-123">Status</span><span class="sxs-lookup"><span data-stu-id="2b81a-123">Status</span></span>
- <span data-ttu-id="2b81a-124">整體專案狀態</span><span class="sxs-lookup"><span data-stu-id="2b81a-124">Overall Project Status</span></span>
- <span data-ttu-id="2b81a-125">註解</span><span class="sxs-lookup"><span data-stu-id="2b81a-125">Comments</span></span>
- <span data-ttu-id="2b81a-126">估計值</span><span class="sxs-lookup"><span data-stu-id="2b81a-126">Estimates</span></span>
- <span data-ttu-id="2b81a-127">估計開始日期：這是從複本所建立專案的日期。</span><span class="sxs-lookup"><span data-stu-id="2b81a-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="2b81a-128">估計完成日期：此日期已根據從複本所建立之新專案的開始日期進行調整。</span><span class="sxs-lookup"><span data-stu-id="2b81a-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="2b81a-129">投入 (小時)</span><span class="sxs-lookup"><span data-stu-id="2b81a-129">Effort (Hours)</span></span>
- <span data-ttu-id="2b81a-130">估計人力成本</span><span class="sxs-lookup"><span data-stu-id="2b81a-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="2b81a-131">估計費用成本</span><span class="sxs-lookup"><span data-stu-id="2b81a-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="2b81a-132">估計材料成本</span><span class="sxs-lookup"><span data-stu-id="2b81a-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="2b81a-133">複製專案是長時間執行的作業。</span><span class="sxs-lookup"><span data-stu-id="2b81a-133">Copy project is a long running operation.</span></span> <span data-ttu-id="2b81a-134">也會複製專案記錄、其相關屬性以及許多相關實體。</span><span class="sxs-lookup"><span data-stu-id="2b81a-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="2b81a-135">由於作業執行時間很長，因此開始複製後，除非複製作業完成，否則會一直鎖定目標專案頁面，無法進行編輯。</span><span class="sxs-lookup"><span data-stu-id="2b81a-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="2b81a-136">分工結構圖</span><span class="sxs-lookup"><span data-stu-id="2b81a-136">Work breakdown structure</span></span>

<span data-ttu-id="2b81a-137">複製專案時，會複製整個資源載入的分工結構圖。</span><span class="sxs-lookup"><span data-stu-id="2b81a-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="2b81a-138">具名資源會以一般資源來取代。</span><span class="sxs-lookup"><span data-stu-id="2b81a-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="2b81a-139">如果具名資源的工作時數與一般資源的不同，則會重新計算排程，而且工作期間可能會變更。</span><span class="sxs-lookup"><span data-stu-id="2b81a-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="2b81a-140">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="2b81a-140">Project team members</span></span>

<span data-ttu-id="2b81a-141">從來源專案複製專案團隊時，會複製一般資源。</span><span class="sxs-lookup"><span data-stu-id="2b81a-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="2b81a-142">一般資源指派也會保持與原先在來源專案中的一樣。</span><span class="sxs-lookup"><span data-stu-id="2b81a-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="2b81a-143">具名資源將會轉換為一般團隊成員。</span><span class="sxs-lookup"><span data-stu-id="2b81a-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="2b81a-144">估計值</span><span class="sxs-lookup"><span data-stu-id="2b81a-144">Estimates</span></span>

<span data-ttu-id="2b81a-145">複製專案時，會從來源專案複製資源、費用及材料估計明細。</span><span class="sxs-lookup"><span data-stu-id="2b81a-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="2b81a-146">如需有關如何以程式設計方式存取 [複製專案] 的詳細資訊，請參閱[使用 [複製專案] 開發專案範本](dev-copy-project.md)。</span><span class="sxs-lookup"><span data-stu-id="2b81a-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
