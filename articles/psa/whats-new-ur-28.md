---
title: Project Service Automation V3 更新版本 28 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 28 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010506"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="3b3ca-103">Project Service Automation V3 更新版本 28 的新功能或變更內容</span><span class="sxs-lookup"><span data-stu-id="3b3ca-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3b3ca-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="3b3ca-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3b3ca-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="3b3ca-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3b3ca-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="3b3ca-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3b3ca-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="3b3ca-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3b3ca-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="3b3ca-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3b3ca-109">本主題列出 Project Service Automation V3 更新版本 28 新增或變更的功能和修正；此版本的組建編號為 V3.10.46.32，已於 2021 年 1 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="3b3ca-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="3b3ca-110">更新版本 28</span><span class="sxs-lookup"><span data-stu-id="3b3ca-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3b3ca-111">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="3b3ca-111">Bug fixes</span></span>

<span data-ttu-id="3b3ca-112">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="3b3ca-112">**Time and Expense**</span></span>

<span data-ttu-id="3b3ca-113">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="3b3ca-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="3b3ca-114">使用者可以使用 **大量編輯** 來更新已核准且已提交的時間項目。</span><span class="sxs-lookup"><span data-stu-id="3b3ca-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="3b3ca-115">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="3b3ca-115">**Project Management**</span></span>

<span data-ttu-id="3b3ca-116">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="3b3ca-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="3b3ca-117">在將工作 GUID 解譯為數字的情況下，無法使用 **分工結構圖** 頁面上功能區中的 **編輯工作**，開啟工作以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="3b3ca-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="3b3ca-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3b3ca-118">**Sales**</span></span>

<span data-ttu-id="3b3ca-119">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="3b3ca-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="3b3ca-120">Null 參考例外狀況是叫用 **GetEstimatesForProject** 外掛程式時所產生。</span><span class="sxs-lookup"><span data-stu-id="3b3ca-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="3b3ca-121">里程碑網格上的 **標示為已準備好開立發票** 除了更新 **InvoiceStatus** 屬性以外，對其他屬性只會進行部分更新。</span><span class="sxs-lookup"><span data-stu-id="3b3ca-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]