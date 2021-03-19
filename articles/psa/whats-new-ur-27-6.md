---
title: Project Service Automation 更新版本 27.6 Hotfix V3 中的新功能或變更
description: 本主題列出 Project Service Automation 更新版本 27.6 Hotfix V3 提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/17/2021
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
ms.openlocfilehash: f6576c6c5660ff6e8e53286ae226c8278a33f2be
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "5481230"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-276-v3"></a><span data-ttu-id="e1a3b-103">Project Service Automation V3 更新版本 27.6 的新功能或變更內容</span><span class="sxs-lookup"><span data-stu-id="e1a3b-103">What's new or changed in Project Service Automation Update Release 27.6, V3</span></span>

<span data-ttu-id="e1a3b-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="e1a3b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e1a3b-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="e1a3b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e1a3b-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="e1a3b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e1a3b-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="e1a3b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e1a3b-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="e1a3b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e1a3b-109">本主題列出 Project Service Automation V3 更新版本 27.6 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="e1a3b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 27.6.</span></span> <span data-ttu-id="e1a3b-110">此版本的組建編號為 V3.10.45.120，已於 2021 年 1 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="e1a3b-110">This version has a build number of V3.10.45.120 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-276"></a><span data-ttu-id="e1a3b-111">更新版本 27.6</span><span class="sxs-lookup"><span data-stu-id="e1a3b-111">Update Release 27.6</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e1a3b-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="e1a3b-112">Bug fixes</span></span>


<span data-ttu-id="e1a3b-113">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="e1a3b-113">**Resource Management**</span></span>

<span data-ttu-id="e1a3b-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="e1a3b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e1a3b-115">尋找資源可用性時，會針對每個尚未套用行事曆規則的資源呼叫 **ExpandCalendar**。</span><span class="sxs-lookup"><span data-stu-id="e1a3b-115">When finding resource availability, **ExpandCalendar** is called for each resource that has no calendar rules applied.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
