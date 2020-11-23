---
title: 瀏覽使用者介面
description: 本主題提供有關 Dynamics 365 Project Operations 中專案管理的資訊。
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: deedfe0c6601fd09e09460034c9a0db936b6566e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127508"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="face1-103">瀏覽使用者介面</span><span class="sxs-lookup"><span data-stu-id="face1-103">Navigating the user interface</span></span>

<span data-ttu-id="face1-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="face1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="face1-105">概觀</span><span class="sxs-lookup"><span data-stu-id="face1-105">Overview</span></span>

<span data-ttu-id="face1-106">主要專案表單分成數個索引標籤。</span><span class="sxs-lookup"><span data-stu-id="face1-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="face1-107">每個索引標籤都代表專案中不同層級的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="face1-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="face1-108">**摘要**：提供專案描述，並彙總規劃和實際的專案績效。</span><span class="sxs-lookup"><span data-stu-id="face1-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![[摘要] 索引標籤和欄位](media/navigation7.png)

- <span data-ttu-id="face1-110">**工作**：提供關於網格檢視、面板檢視和甘特圖所表示之分工結構圖的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="face1-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![[工作] 索引標籤和欄位](media/navigation8.png)

- <span data-ttu-id="face1-112">**團隊**：提供專案參與者的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="face1-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="face1-113">每個團隊成員獲指派的投入量也會在此檢視表中摘要列出。</span><span class="sxs-lookup"><span data-stu-id="face1-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![[團隊] 索引標籤和欄位](media/navigation9.png)

- <span data-ttu-id="face1-115">**資源指派**：提供每個資源在專案中投入量的分時期檢視表。</span><span class="sxs-lookup"><span data-stu-id="face1-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![[資源指派] 索引標籤和欄位](media/navigation10.png)

- <span data-ttu-id="face1-117">**資源協調**：提供每個具名資源及其預約在指派之間差異的分時期檢視表。</span><span class="sxs-lookup"><span data-stu-id="face1-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![[資源協調] 索引標籤和欄位](media/navigation11.png)

- <span data-ttu-id="face1-119">**估計值**：提供專案成本及銷售估計值的分時期檢視表。</span><span class="sxs-lookup"><span data-stu-id="face1-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![[估計值] 索引標籤和欄位](media/navigation12.png)

- <span data-ttu-id="face1-121">**追蹤**：提供在投入量、成本及銷售分工結構圖中顯示工作進度的檢視表。</span><span class="sxs-lookup"><span data-stu-id="face1-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![[追蹤] 索引標籤和欄位](media/navigation13.png)

- <span data-ttu-id="face1-123">**銷售**：提供與專案相關聯之報價及合約的深層連結。</span><span class="sxs-lookup"><span data-stu-id="face1-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="face1-124">**費用估計值**：提供根據組織費用類別定義專案費用的網格。</span><span class="sxs-lookup"><span data-stu-id="face1-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![[費用估計值] 索引標籤和欄位](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="face1-126">網格控制項</span><span class="sxs-lookup"><span data-stu-id="face1-126">Grid controls</span></span>

<span data-ttu-id="face1-127">以下是在位於各種專案規劃索引標籤的一般控制項的簡要概觀。</span><span class="sxs-lookup"><span data-stu-id="face1-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="face1-128">重新整理​</span><span class="sxs-lookup"><span data-stu-id="face1-128">Refresh</span></span>

<span data-ttu-id="face1-129">**重新整理**：如果載入網格後發生任何變更，則從伺服器擷取最新資料。</span><span class="sxs-lookup"><span data-stu-id="face1-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![[重新整理] 按鈕](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="face1-131">群組依據</span><span class="sxs-lookup"><span data-stu-id="face1-131">Group by</span></span>

<span data-ttu-id="face1-132">**群組依據**：更新網格中的列群組，以根據使用者的需求反映資源、角色或類別。</span><span class="sxs-lookup"><span data-stu-id="face1-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![[群組依據] 按鈕](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="face1-134">上一個/下一個</span><span class="sxs-lookup"><span data-stu-id="face1-134">Previous/Next</span></span>

<span data-ttu-id="face1-135">**上一個**/**下一個**：更新分時期網格中可見的時段。</span><span class="sxs-lookup"><span data-stu-id="face1-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![[上一個] 及 [下一個] 按鈕](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="face1-137">時幅</span><span class="sxs-lookup"><span data-stu-id="face1-137">Timescale</span></span>

<span data-ttu-id="face1-138">**時幅**：變更分時期資料在日、週、月和年之間的彙總。</span><span class="sxs-lookup"><span data-stu-id="face1-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![[時幅] 按鈕](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="face1-140">Expand</span><span class="sxs-lookup"><span data-stu-id="face1-140">Expand</span></span>

<span data-ttu-id="face1-141">**展開**：將可見網格呈現為全螢幕畫面，並提供更多可查看其他角色的功能。</span><span class="sxs-lookup"><span data-stu-id="face1-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![[展開] 按鈕](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="face1-143">分時期依據</span><span class="sxs-lookup"><span data-stu-id="face1-143">Time-phase by</span></span>

<span data-ttu-id="face1-144">**分時期依據**：更新網格中的列群組，以反映銷售估計值的成本估計。</span><span class="sxs-lookup"><span data-stu-id="face1-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="face1-145">此控制項也適用於估計指令碼和追蹤網格。</span><span class="sxs-lookup"><span data-stu-id="face1-145">This control also applies to the estimate script and the tracking grid.</span></span>

![[分時期依據] 按鈕](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="face1-147">新增欄</span><span class="sxs-lookup"><span data-stu-id="face1-147">Add column</span></span>

<span data-ttu-id="face1-148">**新增欄**：允許使用者定義網格中可見的欄。</span><span class="sxs-lookup"><span data-stu-id="face1-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="face1-149">只有內建的欄才可以新增至 **專案規劃** 表單中的網格。</span><span class="sxs-lookup"><span data-stu-id="face1-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![[新增欄] 按鈕](media/navigation5.png)
