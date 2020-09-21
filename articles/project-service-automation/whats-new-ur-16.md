---
title: Project Service Automation V3 更新版本 16 的新功能
description: 本主題列出 Project Service Automation 更新版本 16 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749911"
---
# <a name="project-service-automation-v3-update-release-16"></a><span data-ttu-id="ff36d-103">Project Service Automation V3 更新版本 16 的新功能</span><span class="sxs-lookup"><span data-stu-id="ff36d-103">Project Service Automation V3, Update Release 16</span></span>
<span data-ttu-id="ff36d-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="ff36d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ff36d-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="ff36d-105">This release includes some important improvements to quality, performance, and usability.</span></span>

<span data-ttu-id="ff36d-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="ff36d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ff36d-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="ff36d-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="ff36d-108">如需詳細資訊，請參閱[安裝、更新偏好的解決方案](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page)。</span><span class="sxs-lookup"><span data-stu-id="ff36d-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span> <span data-ttu-id="ff36d-109">本主題列出 PSA V3 更新版本 16 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="ff36d-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="ff36d-110">此版本的組建編號為 V3.10.6.34，已於 2020 年 1 月透過自我更新正式推出</span><span class="sxs-lookup"><span data-stu-id="ff36d-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020</span></span>

## <a name="update-release-16"></a><span data-ttu-id="ff36d-111">更新版本 16</span><span class="sxs-lookup"><span data-stu-id="ff36d-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ff36d-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="ff36d-112">Bug fixes</span></span>

-   <span data-ttu-id="ff36d-113">時間和費用</span><span class="sxs-lookup"><span data-stu-id="ff36d-113">Time and Expense</span></span>

    -   <span data-ttu-id="ff36d-114">已修正：嘗試提交已刪除時間及和費用分錄以取得核准的使用者，現在會收到相關的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="ff36d-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="ff36d-115">專案管理</span><span class="sxs-lookup"><span data-stu-id="ff36d-115">Project Management</span></span>

    -   <span data-ttu-id="ff36d-116">已修正：範本中團隊成員定義的資源分配單位與套用至新專案的範本有關。</span><span class="sxs-lookup"><span data-stu-id="ff36d-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="ff36d-117">已修正：改善對記錄擁有權重新指派的處理。</span><span class="sxs-lookup"><span data-stu-id="ff36d-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="ff36d-118">已修正：在所有複製作業完成前，不允許複製處於複製過程中的專案。</span><span class="sxs-lookup"><span data-stu-id="ff36d-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="ff36d-119">資源管理</span><span class="sxs-lookup"><span data-stu-id="ff36d-119">Resource Management</span></span>

    -   <span data-ttu-id="ff36d-120">已修正：延長預約現在會正確處理短期的期間，不再建立零時數的延長預約。</span><span class="sxs-lookup"><span data-stu-id="ff36d-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="ff36d-121">已修正：協調檢視表現在會在專案時區為 +5:30 GMT 且使用者時區不同時呈現。</span><span class="sxs-lookup"><span data-stu-id="ff36d-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="ff36d-122">Sales</span><span class="sxs-lookup"><span data-stu-id="ff36d-122">Sales</span></span>

    -   <span data-ttu-id="ff36d-123">已修正：移除對應至合約服務內容的專案並對應新專案時，新專案的實際記錄無法根據合約服務內容所定義的帳務及定價規則進行重新評估。</span><span class="sxs-lookup"><span data-stu-id="ff36d-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="ff36d-124">此問題已在此版本中修正。</span><span class="sxs-lookup"><span data-stu-id="ff36d-124">This has been fixed in this release.</span></span> <span data-ttu-id="ff36d-125">新對應專案的定價和實際記錄會根據合約服務內容的定價及帳務規則正確進行沖回和重建。</span><span class="sxs-lookup"><span data-stu-id="ff36d-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="ff36d-126">未對應專案的實際記錄也會因此進行重新評估和重建。</span><span class="sxs-lookup"><span data-stu-id="ff36d-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="ff36d-127">已修正：已將額外驗證新增至估計明細的**金額**欄位，以確保 null 值不會繼續存在。</span><span class="sxs-lookup"><span data-stu-id="ff36d-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="ff36d-128">已修正：專案的實際值已更新時，已將重新整理按鈕新增至專案主要表單，以允許使用者重新同步實際值。</span><span class="sxs-lookup"><span data-stu-id="ff36d-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="ff36d-129">已修正：使用者從 2.X 升級至 3.X 時，允許專案名稱含 NULL 值的專案。</span><span class="sxs-lookup"><span data-stu-id="ff36d-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

