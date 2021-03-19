---
title: Project Service Automation V3 更新版本 12 的新功能或變更內容
description: 本主題提供 Project Service Automation V3 更新版本 12 中新功能的相關資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f1b2fdc37fa2c2e31537b89b7027d2833e905578
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281063"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="43006-103">Project Service Automation 更新版本 12 V3</span><span class="sxs-lookup"><span data-stu-id="43006-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="43006-104">我們很高興宣布 Dynamics 365 Project Service Automation (PSA) 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="43006-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="43006-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="43006-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="43006-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="43006-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="43006-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，然後移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="43006-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="43006-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="43006-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="43006-109">本主題列出 Project Service Automation V3 更新版本 12 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="43006-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="43006-110">此版本的組建編號為 V3.10.2.34，已於 2019 年 10 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="43006-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="43006-111">更新版本 12</span><span class="sxs-lookup"><span data-stu-id="43006-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="43006-112">錯誤修正</span><span class="sxs-lookup"><span data-stu-id="43006-112">Bug fixes</span></span>

- <span data-ttu-id="43006-113">時間和費用</span><span class="sxs-lookup"><span data-stu-id="43006-113">Time and Expense</span></span>

    - <span data-ttu-id="43006-114">已修正：時間項目錯誤訊息已更新為相關性更高的內容。</span><span class="sxs-lookup"><span data-stu-id="43006-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="43006-115">已修正：時間項目網格和排程會視需要正確顯示垂直捲軸。</span><span class="sxs-lookup"><span data-stu-id="43006-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="43006-116">已修正：可以核准已送出的費用及時間項目。</span><span class="sxs-lookup"><span data-stu-id="43006-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="43006-117">已修正：[取消核准] 確認對話方塊訊息已更正為可在狀態由 **已核准** 變更成 **已送出** 時反映核准狀態。</span><span class="sxs-lookup"><span data-stu-id="43006-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="43006-118">已修正：核准了費用記錄之後，現在會鎖定此記錄上的 **價格**、**單位** 和 **品質** 欄位。</span><span class="sxs-lookup"><span data-stu-id="43006-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="43006-119">專案管理</span><span class="sxs-lookup"><span data-stu-id="43006-119">Project Management</span></span>

    - <span data-ttu-id="43006-120">已修正：**團隊成員** 主要表單上的 **新增** 動作已移除。</span><span class="sxs-lookup"><span data-stu-id="43006-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="43006-121">已修正：資源指派已更新，可解決不正確的捨入錯誤，此錯誤會導致工作結束日期變動。</span><span class="sxs-lookup"><span data-stu-id="43006-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="43006-122">已修正：在工作網格中，會向使用者顯露相關的伺服器端錯誤。</span><span class="sxs-lookup"><span data-stu-id="43006-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="43006-123">已修正：團隊成員在工作人員選擇器中顯示的是其姓名而不是職位名稱。</span><span class="sxs-lookup"><span data-stu-id="43006-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="43006-124">資源管理</span><span class="sxs-lookup"><span data-stu-id="43006-124">Resource Management</span></span>

    - <span data-ttu-id="43006-125">已修正：從範本所建立之專案的資源需求詳細資料現在會使用專案行事曆。</span><span class="sxs-lookup"><span data-stu-id="43006-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="43006-126">已修正：技能和專長現已從角色主要資料預設為針對該角色建立的資源需求。</span><span class="sxs-lookup"><span data-stu-id="43006-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="43006-127">Sales</span><span class="sxs-lookup"><span data-stu-id="43006-127">Sales</span></span>

    - <span data-ttu-id="43006-128">已修正：在 **合約主要** 表單上發現了重複的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="43006-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="43006-129">已修正：邏輯已更新，使得 **報價分析** 索引標籤可見，以便顯示索引標籤的中繼資料設定。</span><span class="sxs-lookup"><span data-stu-id="43006-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="43006-130">已修正：實際記錄上的會計日期現在是來自時間/費用項目日期，而不是核准日期。</span><span class="sxs-lookup"><span data-stu-id="43006-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]