---
title: Project Service Automation V3 更新版本 22 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 22 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072944"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="676b5-103">Project Service Automation 更新版本 22 V3</span><span class="sxs-lookup"><span data-stu-id="676b5-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="676b5-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="676b5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="676b5-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="676b5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="676b5-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="676b5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="676b5-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="676b5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="676b5-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="676b5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="676b5-109">本主題列出 Project Service Automation V3 更新版本 22 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="676b5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="676b5-110">此版本的組建編號為 V 3.10.33.48，已於 2020 年 6 月透過自我更新正式發行。</span><span class="sxs-lookup"><span data-stu-id="676b5-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="676b5-111">更新版本 22</span><span class="sxs-lookup"><span data-stu-id="676b5-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="676b5-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="676b5-112">Bug fixes</span></span>



<span data-ttu-id="676b5-113">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="676b5-113">**Time and Expense**</span></span>

<span data-ttu-id="676b5-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="676b5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="676b5-115">**時間項目** 未在匯入後自動新增至時間項目排程中。</span><span class="sxs-lookup"><span data-stu-id="676b5-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="676b5-116">**時間項目** 網格日期選擇器無法辨識使用者的地區設定。</span><span class="sxs-lookup"><span data-stu-id="676b5-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="676b5-117">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="676b5-117">**Resource Management**</span></span>

<span data-ttu-id="676b5-118">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="676b5-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="676b5-119">在手動模式下，無法在產生 **資源需求** 時辨識 **資源指派** 分佈的變更。</span><span class="sxs-lookup"><span data-stu-id="676b5-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="676b5-120">**資源要求** 不支援自訂要求狀態。</span><span class="sxs-lookup"><span data-stu-id="676b5-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="676b5-121">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="676b5-121">**Project Management**</span></span>

<span data-ttu-id="676b5-122">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="676b5-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="676b5-123">對 EstimateGridControl 使用按兩下動作時，無法正確剖析荷蘭文格式數字。</span><span class="sxs-lookup"><span data-stu-id="676b5-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="676b5-124">使用 Microsoft Project 桌面用戶端增益集變更指派時，已指派的時數無法正確更新。</span><span class="sxs-lookup"><span data-stu-id="676b5-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="676b5-125">當合約貨幣與客戶貨幣不同，且組織是設定為顯示貨幣代碼而不是貨幣符號時，[專案追蹤] 和 [估計值] 網格顯示不正確的銷售貨幣代碼。</span><span class="sxs-lookup"><span data-stu-id="676b5-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="676b5-126">如果工作時數排程為每天 24 小時，則團隊成員的完成日期將會新增一天。</span><span class="sxs-lookup"><span data-stu-id="676b5-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="676b5-127">在專案排程中，將交易類別新增至工作時，不會觸發自動儲存。</span><span class="sxs-lookup"><span data-stu-id="676b5-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="676b5-128">將團隊成員新增至專案範本時，顯示下列錯誤：「資源需求無法與專案範本建立關聯」。</span><span class="sxs-lookup"><span data-stu-id="676b5-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="676b5-129">功能區規則指令碼「msdyn.Approval.CanApproveOrReject」顯示逾時錯誤。</span><span class="sxs-lookup"><span data-stu-id="676b5-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="676b5-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="676b5-130">**Sales**</span></span>

<span data-ttu-id="676b5-131">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="676b5-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="676b5-132">在 [新增報價專案價目表] 表單/實體的 [價目表] 查詢中選取 [成本價目表] 時，未顯示驗證錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="676b5-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="676b5-133">如果附加至報價的 BPF 處於最終階段，以成交關閉報價時，不會瀏覽時至建立的合約。</span><span class="sxs-lookup"><span data-stu-id="676b5-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="676b5-134">回收時間項目時，沖回 **未開單銷售** 會連結至原始成本。</span><span class="sxs-lookup"><span data-stu-id="676b5-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="676b5-135">選取 **確認** 按鈕之後，除非重新整理發票，否則發票狀態不會變更為 **已確認** 。</span><span class="sxs-lookup"><span data-stu-id="676b5-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
