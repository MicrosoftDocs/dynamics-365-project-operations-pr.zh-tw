---
title: Project Service Automation V3 更新版本 33 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 33 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334512"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="cd1f0-103">Project Service Automation V3 更新版本 33 的新功能或變更內容</span><span class="sxs-lookup"><span data-stu-id="cd1f0-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cd1f0-104">我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="cd1f0-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cd1f0-106">與 Dynamics 365 9.x 相容。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cd1f0-107">若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="cd1f0-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cd1f0-109">本主題列出 Project Service Automation V3 更新版本 33 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="cd1f0-110">此版本的組建編號為 V3.10.54.98，已於 2021 年 7 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="cd1f0-111">更新版本 33</span><span class="sxs-lookup"><span data-stu-id="cd1f0-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cd1f0-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="cd1f0-112">Bug fixes</span></span>

<span data-ttu-id="cd1f0-113">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="cd1f0-113">**Time and Expense**</span></span>

<span data-ttu-id="cd1f0-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="cd1f0-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd1f0-115">兩個鎖定的欄位 **msdyn_description** 和 **msdyn_externaldescription** 可在提交後進行編輯。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="cd1f0-116">如果建立與專案無關的費用，就會出現錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="cd1f0-117">建立時間項目時，該資源角色預設為非使用中角色。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="cd1f0-118">不會刪除與已回收及已刪除費用相關聯的帳目明細。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="cd1f0-119">在 **時間項目快速建立表單** 上，更新 **專案工作清單** 檢視表，以將預設顯示的日期變更為工作的開始日期。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="cd1f0-120">從可預約資源的 **相關** 索引標籤建立時間項目時，已登入的使用者 (而不是上層可預約資源) 會不確定地建立時間項目。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="cd1f0-121">新的欄位會新增至 **大量核准 MDD** 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="cd1f0-122">**專案規劃**</span><span class="sxs-lookup"><span data-stu-id="cd1f0-122">**Project planning**</span></span>

<span data-ttu-id="cd1f0-123">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="cd1f0-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="cd1f0-124">使用複雜行事曆套用專案工時數範本時，會讓專案建立效能變慢。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="cd1f0-125">開始日期大於結束日期時，錯誤會顯示在複製專案範本上，因為每個欄位的時間元件有差異。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="cd1f0-126">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="cd1f0-126">**Resource management**</span></span>

<span data-ttu-id="cd1f0-127">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="cd1f0-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="cd1f0-128">資源使用率查詢中使用了不正確的參數，而 XML 在 **資源使用率** 網格中導致不正確的篩選結果。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="cd1f0-129">**延長預約確認** 會顯示不正確的預約結束日期。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="cd1f0-130">**銷售**</span><span class="sxs-lookup"><span data-stu-id="cd1f0-130">**Sales**</span></span>

<span data-ttu-id="cd1f0-131">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="cd1f0-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="cd1f0-132">如果類別價格是以遺失的值建立，就會出現錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="cd1f0-133">如果合約服務內容里程碑是在不使用訂單明細的情況下所建立，就會出現錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="cd1f0-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
