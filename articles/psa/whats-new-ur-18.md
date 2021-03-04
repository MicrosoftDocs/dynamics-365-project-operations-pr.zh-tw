---
title: Project Service Automation V3 更新版本 18 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 18 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147193"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="af80e-103">Project Service Automation 更新版本 18 V3</span><span class="sxs-lookup"><span data-stu-id="af80e-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="af80e-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="af80e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="af80e-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="af80e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="af80e-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="af80e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="af80e-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="af80e-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="af80e-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="af80e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="af80e-109">本主題列出 Project Service Automation V3 更新版本 18 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="af80e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="af80e-110">此版本的組建編號是 V3.10.8.12，已於 2020 年 4 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="af80e-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="af80e-111">更新版本 18</span><span class="sxs-lookup"><span data-stu-id="af80e-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="af80e-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="af80e-112">Bug fixes</span></span>

<span data-ttu-id="af80e-113">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="af80e-113">**Time and Expense**</span></span>

- <span data-ttu-id="af80e-114">已修正：**回收**、**要求** 和 **取消核准** 流程擲回例外狀況，並出現不明確的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="af80e-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="af80e-115">已修正：費用的 **取消核准** 失敗時，未擲回相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="af80e-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="af80e-116">已修正：在 10 月份的日光節約時間 (DST) 切換之後，時間項目網格未正確處理澳大利亞的非工作日。</span><span class="sxs-lookup"><span data-stu-id="af80e-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="af80e-117">已修正：不正確的預設邏輯導致無法提交費用。</span><span class="sxs-lookup"><span data-stu-id="af80e-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="af80e-118">已修正：時間項目核准失敗時，核准仍保持在 **擱置** 狀態。</span><span class="sxs-lookup"><span data-stu-id="af80e-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="af80e-119">已修正：大量核准時發生 SQL 錯誤 (鎖死/逾時)。</span><span class="sxs-lookup"><span data-stu-id="af80e-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="af80e-120">已修正：核准時間項目時，使用者體驗因更新團隊成員而產生重大效能問題。</span><span class="sxs-lookup"><span data-stu-id="af80e-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="af80e-121">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="af80e-121">**Project Management**</span></span>

- <span data-ttu-id="af80e-122">已修正：時區通知已從 **協調** 檢視移到 **專案** 主要表單。</span><span class="sxs-lookup"><span data-stu-id="af80e-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="af80e-123">已修正：新的專案表單開啟時，行事曆範本未正確使用預設值。</span><span class="sxs-lookup"><span data-stu-id="af80e-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="af80e-124">已修正：使用以 Chromium 為基礎的瀏覽器時，使用者無法輕鬆地選取要刪除的前置工作。</span><span class="sxs-lookup"><span data-stu-id="af80e-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="af80e-125">已修正：建立或複製 **專案 (從空白範本)** 會擷取無關的指派。</span><span class="sxs-lookup"><span data-stu-id="af80e-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="af80e-126">已修正：在特定邊緣案例中，從工作網格建立新指派會導致建立重複的記錄。</span><span class="sxs-lookup"><span data-stu-id="af80e-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="af80e-127">已修正：在手動模式下，使用者無法將工作開始日期更新成晚於已儲存的目前日期。</span><span class="sxs-lookup"><span data-stu-id="af80e-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="af80e-128">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="af80e-128">**Resource Management**</span></span>

- <span data-ttu-id="af80e-129">已修正：延長預約之後，**協調** 檢視表小計列計算的預約差異不正確。</span><span class="sxs-lookup"><span data-stu-id="af80e-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="af80e-130">已修正：可預約資源的行事曆與專案行事曆不相符時，**協調** 檢視表無法正確顯示資源指派。</span><span class="sxs-lookup"><span data-stu-id="af80e-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="af80e-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="af80e-131">**Sales**</span></span>

- <span data-ttu-id="af80e-132">已修正：重新核准時間項目 (**核准 > 取消 >** 再次核准) 時，會建立重複的不應收費實際值。</span><span class="sxs-lookup"><span data-stu-id="af80e-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
