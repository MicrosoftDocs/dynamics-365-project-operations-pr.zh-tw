---
title: Project Service Automation V3 更新版本 32 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 32 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129656"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="e40dc-103">Project Service Automation V3 更新版本 32 的新功能或變更內容</span><span class="sxs-lookup"><span data-stu-id="e40dc-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e40dc-104">我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="e40dc-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="e40dc-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="e40dc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e40dc-106">與 Dynamics 365 9.x 相容。</span><span class="sxs-lookup"><span data-stu-id="e40dc-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e40dc-107">若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。</span><span class="sxs-lookup"><span data-stu-id="e40dc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="e40dc-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="e40dc-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e40dc-109">本主題列出 Project Service Automation V3 更新版本 32 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="e40dc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="e40dc-110">此版本的組建編號是 V3.10.53.108，已於 2021 年 6 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="e40dc-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="e40dc-111">更新版本 32</span><span class="sxs-lookup"><span data-stu-id="e40dc-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e40dc-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="e40dc-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="e40dc-113">一般</span><span class="sxs-lookup"><span data-stu-id="e40dc-113">General</span></span>

- <span data-ttu-id="e40dc-114">主要升級失敗時，只能封鎖主要應用程式進入點，以確保共用的實體仍然可供存取。</span><span class="sxs-lookup"><span data-stu-id="e40dc-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="e40dc-115">時間和費用</span><span class="sxs-lookup"><span data-stu-id="e40dc-115">Time and Expense</span></span>

<span data-ttu-id="e40dc-116">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="e40dc-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="e40dc-117">**TimeEntriesImportFromResourceAssignment** 不會保留資源指派分佈配量的開始時間和結束時間。</span><span class="sxs-lookup"><span data-stu-id="e40dc-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="e40dc-118">當您選取 **時間項目** 窗格中的 **開啟項目** 時，可能會禁止您選取其他表單。</span><span class="sxs-lookup"><span data-stu-id="e40dc-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="e40dc-119">將指派匯入至時間項目時，用戶端程式碼查詢可能會產生造成查詢失敗的冗長 URL。</span><span class="sxs-lookup"><span data-stu-id="e40dc-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="e40dc-120">在 **時間項目** 網格中，從儲存格刪除某個值之後，焦點不會留在網格中。</span><span class="sxs-lookup"><span data-stu-id="e40dc-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="e40dc-121">**拒絕** 按鈕已從新式核准的 **處理核准** 視圖中移除。</span><span class="sxs-lookup"><span data-stu-id="e40dc-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="e40dc-122">發生鎖死以及未能適當處理與 **時間項目** 實體相關的自訂，會影響時間項目大量核准的穩定性及效能。</span><span class="sxs-lookup"><span data-stu-id="e40dc-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="e40dc-123">專案規劃</span><span class="sxs-lookup"><span data-stu-id="e40dc-123">Project Planning</span></span>

- <span data-ttu-id="e40dc-124">更新其 **承包單位** 欄位有 Null 值的專案時，會產生 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e40dc-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="e40dc-125">**重新整理專案總計** 不正確地計算專案的剩餘成本與剩餘銷售。</span><span class="sxs-lookup"><span data-stu-id="e40dc-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="e40dc-126">冗長的定價計算會影響與資源指派分佈更新相關的效能。</span><span class="sxs-lookup"><span data-stu-id="e40dc-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="e40dc-127">資源管理</span><span class="sxs-lookup"><span data-stu-id="e40dc-127">Resource Management</span></span>

<span data-ttu-id="e40dc-128">已修正下列問題：</span><span class="sxs-lookup"><span data-stu-id="e40dc-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="e40dc-129">可預約資源的行事曆產能大於 1 時，Project Service Automation 會錯誤地將產能辨識為 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="e40dc-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="e40dc-130">因此，排程檢視表中會發生無限迴圈。</span><span class="sxs-lookup"><span data-stu-id="e40dc-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="e40dc-131">銷售</span><span class="sxs-lookup"><span data-stu-id="e40dc-131">Sales</span></span>

<span data-ttu-id="e40dc-132">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="e40dc-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="e40dc-133">建立具有自訂交易類型的帳目明細時，會發生下列 Null 參考例外狀況：*Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*。</span><span class="sxs-lookup"><span data-stu-id="e40dc-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="e40dc-134">不可將複製報價前已停用的角色和類別新增至新複製報價的應收費角色和類別。</span><span class="sxs-lookup"><span data-stu-id="e40dc-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="e40dc-135">文件日期和會計日期，與直接在草稿發票中建立的發票明細詳細資料所提供的開始日期不一致。</span><span class="sxs-lookup"><span data-stu-id="e40dc-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="e40dc-136">在與角色和類別已於複製報價前停用一事相關的案例中，會產生 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e40dc-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="e40dc-137">**專案** 頁面上的 **更新價格** 動作不會更新費用估計值和材料估計值。</span><span class="sxs-lookup"><span data-stu-id="e40dc-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
