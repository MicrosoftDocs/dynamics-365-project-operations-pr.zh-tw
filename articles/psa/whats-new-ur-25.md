---
title: Project Service Automation V3 更新版本 25 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 25 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183533"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="18a62-103">Project Service Automation V3 更新版本 25 的新功能或變更內容</span><span class="sxs-lookup"><span data-stu-id="18a62-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="18a62-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="18a62-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="18a62-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="18a62-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="18a62-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="18a62-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="18a62-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="18a62-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="18a62-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="18a62-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="18a62-109">本主題列出了 Project Service Automation V3 更新版本 25 的新增或變更功能和修正。此版本的組建編號為 V 3.10.43.76，一般可透過 2020 年 10 月的自我更新獲得。</span><span class="sxs-lookup"><span data-stu-id="18a62-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="18a62-110">更新版本 25</span><span class="sxs-lookup"><span data-stu-id="18a62-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="18a62-111">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="18a62-111">Bug fixes</span></span>

<span data-ttu-id="18a62-112">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="18a62-112">**Time and Expense**</span></span>

<span data-ttu-id="18a62-113">已修正下列問題：</span><span class="sxs-lookup"><span data-stu-id="18a62-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="18a62-114">時間項目圖表，根據擷取的間隔太長而顯示額外的資料。</span><span class="sxs-lookup"><span data-stu-id="18a62-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="18a62-115">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="18a62-115">**Resource Management**</span></span>

<span data-ttu-id="18a62-116">已修正下列問題：</span><span class="sxs-lookup"><span data-stu-id="18a62-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="18a62-117">新增了 Package Deployer 程式碼，以在更高版本的修補程式已存在時跳過 Universal Resource Scheduling 修補程式匯入。</span><span class="sxs-lookup"><span data-stu-id="18a62-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="18a62-118">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="18a62-118">**Project Management**</span></span>

<span data-ttu-id="18a62-119">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="18a62-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="18a62-120">校正了導致在專案追蹤網格中的計劃成本不正確的捨入和匯率差異。</span><span class="sxs-lookup"><span data-stu-id="18a62-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="18a62-121">支援在 **專案** 表單上顯示兩個或多個反應網格的能力。</span><span class="sxs-lookup"><span data-stu-id="18a62-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="18a62-122">提供驗證以解決在日曆結束日期之後指派工作因而導致資源指派失敗的能力。</span><span class="sxs-lookup"><span data-stu-id="18a62-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="18a62-123">改進了錯誤處理，以解決由以下各項所產生的 Null 參考例外狀況：</span><span class="sxs-lookup"><span data-stu-id="18a62-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="18a62-124">**PreValidateProjectTeamMemberCreate** 外掛程式</span><span class="sxs-lookup"><span data-stu-id="18a62-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="18a62-125">建立沒有關聯專案的專案工作時的 **PreValidateProjectTaskCreate**</span><span class="sxs-lookup"><span data-stu-id="18a62-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="18a62-126">**PreProjectTeamMemberCreate** 外掛程式</span><span class="sxs-lookup"><span data-stu-id="18a62-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="18a62-127">**PostProjectTeamMemberDelete** 外掛程式</span><span class="sxs-lookup"><span data-stu-id="18a62-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="18a62-128">**PreValidateProjectTaskDelete** 外掛程式</span><span class="sxs-lookup"><span data-stu-id="18a62-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="18a62-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="18a62-129">**Sales**</span></span>

<span data-ttu-id="18a62-130">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="18a62-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="18a62-131">改進了錯誤處理，以解決由 **複製專案：估計 HelperResource 管理** 所產生的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="18a62-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="18a62-132">**時間和資料帳務積存** 上的 **尚未準備好開立發票** 並未清除帳單狀態。</span><span class="sxs-lookup"><span data-stu-id="18a62-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="18a62-133">更正 **角色價格** 和 **目錄項目** 索引標籤上錯誤標籤的 **價格** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="18a62-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
