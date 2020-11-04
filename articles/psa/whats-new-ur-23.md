---
title: Project Service Automation V3 更新版本 23 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 23 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072943"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="807a3-103">Project Service Automation 更新版本 23 V3</span><span class="sxs-lookup"><span data-stu-id="807a3-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="807a3-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="807a3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="807a3-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="807a3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="807a3-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="807a3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="807a3-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="807a3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="807a3-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="807a3-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="807a3-109">本主題列出 Project Service Automation V3 更新版本 23 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="807a3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="807a3-110">此版本的組建編號為 V 3.10.34.30，已於 2020 年 8 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="807a3-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="807a3-111">更新版本 23</span><span class="sxs-lookup"><span data-stu-id="807a3-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="807a3-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="807a3-112">Bug fixes</span></span>

<span data-ttu-id="807a3-113">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="807a3-113">**Time and Expense**</span></span>

<span data-ttu-id="807a3-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="807a3-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="807a3-115">處理 **專案團隊成員刪除** 中的邊緣案例，以提供有意義的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="807a3-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="807a3-116">指派匯入會產生空白移除畫面。</span><span class="sxs-lookup"><span data-stu-id="807a3-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="807a3-117">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="807a3-117">**Resource Management**</span></span>

<span data-ttu-id="807a3-118">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="807a3-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="807a3-119">時幅超過五天時， **資源使用率網格資源卡片** 會顯示不正確的資料。</span><span class="sxs-lookup"><span data-stu-id="807a3-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="807a3-120">客戶建立可預約資源時，外掛程式會間歇性發生無法自動將資源新增至 Microsoft Office 365 群組的情況。</span><span class="sxs-lookup"><span data-stu-id="807a3-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="807a3-121">**協調** 檢視表未正確顯示 **週** 或 **月** 檢視表中的手動分佈。</span><span class="sxs-lookup"><span data-stu-id="807a3-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="807a3-122">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="807a3-122">**Project Management**</span></span>

<span data-ttu-id="807a3-123">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="807a3-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="807a3-124">過多 **使用者設定的 RetrieveMultiple** 實體造成專案核准及其他作業的效能降低。</span><span class="sxs-lookup"><span data-stu-id="807a3-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="807a3-125">**工作規劃** 網格資源查詢受到限制，最多只能顯示五個來自專案團隊的團隊成員。</span><span class="sxs-lookup"><span data-stu-id="807a3-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="807a3-126">**工作規劃** 網格資源查詢不會篩選非使用中資源。</span><span class="sxs-lookup"><span data-stu-id="807a3-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="807a3-127">在專案規劃分工結構圖中，手動模式無法依預期正常運作。</span><span class="sxs-lookup"><span data-stu-id="807a3-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="807a3-128">**工作規劃** 網格會顯示 **非使用中交易類別** 。</span><span class="sxs-lookup"><span data-stu-id="807a3-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="807a3-129">工作有多個指派時， **資源指派** 網格捨入不正確。</span><span class="sxs-lookup"><span data-stu-id="807a3-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="807a3-130">單一工作的捨入值在計劃成本與實際成本之間不相同。</span><span class="sxs-lookup"><span data-stu-id="807a3-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="807a3-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="807a3-131">**Sales**</span></span>

<span data-ttu-id="807a3-132">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="807a3-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="807a3-133">按兩下 **擷取所有交易類別** 會建立多行。</span><span class="sxs-lookup"><span data-stu-id="807a3-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
