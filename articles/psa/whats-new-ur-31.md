---
title: Project Service Automation V3 更新版本 31 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 31 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945525"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="a65f7-103">Project Service Automation V3 更新版本 31 的新功能或變更內容</span><span class="sxs-lookup"><span data-stu-id="a65f7-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a65f7-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="a65f7-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a65f7-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="a65f7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a65f7-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="a65f7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a65f7-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="a65f7-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a65f7-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="a65f7-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a65f7-109">本主題列出 Project Service Automation V3 更新版本 31 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="a65f7-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="a65f7-110">此版本的組建編號是 V3.10.52.77，已於 2021 年 5 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="a65f7-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="a65f7-111">更新版本 31</span><span class="sxs-lookup"><span data-stu-id="a65f7-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a65f7-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="a65f7-112">Bug fixes</span></span>

<span data-ttu-id="a65f7-113">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="a65f7-113">**Time and Expense**</span></span>

<span data-ttu-id="a65f7-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="a65f7-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="a65f7-115">**可預約資源** 頁面上的時間項目控制項命令按鈕造成混淆。</span><span class="sxs-lookup"><span data-stu-id="a65f7-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="a65f7-116">核准時間項目時，在 **Project.SetTrackingFields** 中產生了 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a65f7-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="a65f7-117">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="a65f7-117">**Resource Management**</span></span>

<span data-ttu-id="a65f7-118">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="a65f7-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a65f7-119">**建立團隊成員** 未正確顯示 **預設預約認可狀態** 的預約設定中繼資料設定。</span><span class="sxs-lookup"><span data-stu-id="a65f7-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="a65f7-120">從 PSA 1.X 升級至 3.X 時，升級程序會在 **UpgradeResourceRequirements** 處失敗。</span><span class="sxs-lookup"><span data-stu-id="a65f7-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="a65f7-121">**銷售**</span><span class="sxs-lookup"><span data-stu-id="a65f7-121">**Sales**</span></span>

<span data-ttu-id="a65f7-122">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="a65f7-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="a65f7-123">實際營收會將金額轉換為追蹤網格中的專案貨幣。</span><span class="sxs-lookup"><span data-stu-id="a65f7-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="a65f7-124">在組織基準貨幣與專案貨幣不同的案例中建立帳目明細、報價明細和合約服務內容時，貨幣預設值不明確。</span><span class="sxs-lookup"><span data-stu-id="a65f7-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="a65f7-125">**擱置中更正帳目驗證** 查詢未依專案進行篩選。</span><span class="sxs-lookup"><span data-stu-id="a65f7-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="a65f7-126">專案中的剩餘銷售計算不正確。</span><span class="sxs-lookup"><span data-stu-id="a65f7-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="a65f7-127">未使用價目表來建立以合約為根據的報價時，這些報價會失敗。</span><span class="sxs-lookup"><span data-stu-id="a65f7-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="a65f7-128">選取 **確認發票** 時，未顯示任何處理微調按鈕。</span><span class="sxs-lookup"><span data-stu-id="a65f7-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="a65f7-129">選取 **建立發票** 時，未顯示任何處理微調按鈕。</span><span class="sxs-lookup"><span data-stu-id="a65f7-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="a65f7-130">以未成交關閉報價不會取消預約。</span><span class="sxs-lookup"><span data-stu-id="a65f7-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







