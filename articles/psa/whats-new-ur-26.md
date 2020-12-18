---
title: Project Service Automation V3 更新版本 26 的新功能或變更內容
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643253"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="bc5c6-102">Project Service Automation 更新版本 26 V3</span><span class="sxs-lookup"><span data-stu-id="bc5c6-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="bc5c6-103">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bc5c6-104">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bc5c6-105">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bc5c6-106">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bc5c6-107">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bc5c6-108">本主題列出 Project Service Automation 更新版本 26 V3 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="bc5c6-109">此版本的組建編號為 V3.10.44.59，一般可透過 2020 年 12 月的自我更新獲得。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="bc5c6-110">更新版本 26</span><span class="sxs-lookup"><span data-stu-id="bc5c6-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="bc5c6-111">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="bc5c6-111">Bug fixes</span></span>

<span data-ttu-id="bc5c6-112">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-112">**Time and Expense**</span></span>

<span data-ttu-id="bc5c6-113">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="bc5c6-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="bc5c6-114">使用者可以變更已核准/已送出之時間項目上的工作。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="bc5c6-115">儲存時間項目時發生「物件參照未設定」錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="bc5c6-116">從資源指派匯入的時間項目會建立具有不正確日期時間值的時間項目。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="bc5c6-117">當 Project Service Automation 與 Field Service 應用程式皆已安裝時，**新增** 按鈕在命令列上為 Field Service 應用程式中的時間項目顯示兩次。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="bc5c6-118">**允許單位** 與 **單位群組** 儲存格更新現在可在 **費用估計值** 窗格中運作。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="bc5c6-119">**更新時間項目編輯** 表單包括 **時間表**。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="bc5c6-120">非專案時間項目的時間核准會在搜尋專案核准者角色時封鎖系統。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="bc5c6-121">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-121">**Resource Management**</span></span>

<span data-ttu-id="bc5c6-122">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="bc5c6-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="bc5c6-123">新增在 **PostProjectCreate** 外掛程式中的驗證，以在建立之前檢查主要需求。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="bc5c6-124">如果已從表單移除欄位，則 **專案團隊成員** 快速建立表單將會擲回 null 參照例外狀況。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="bc5c6-125">產生超過 1 年的 12 小時需求將會失敗。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="bc5c6-126">在建立資源需求期間，改善了錯誤訊息 null 參照例外狀況。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="bc5c6-127">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-127">**Project Management**</span></span>

<span data-ttu-id="bc5c6-128">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="bc5c6-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="bc5c6-129">改善驗證以解決 **PreProjectUpdate** 外掛程式中所產生的 null 參照例外狀況。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="bc5c6-130">Microsoft Project 桌面增益集所發行的專案會刪除未指派的指派。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="bc5c6-131">新增驗證以因應 **PreValidateProjectTaskUpdate** 外掛程式中的 null 參照例外狀況而導致工作專案參照無效。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="bc5c6-132">團隊成員網格不會在團隊成員記錄中顯示不同的指派。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="bc5c6-133">由於 **PreProjectTaskDelete** 外掛程式中的 null 參照例外狀況而新增了新的驗證和錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="bc5c6-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-134">**Sales**</span></span>

<span data-ttu-id="bc5c6-135">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="bc5c6-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="bc5c6-136">當選取報價或合約中的專案型條項時，只有在選取與現有產品相關的專案型條項時，才會顯示 **建議** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="bc5c6-137">從 **Create_ProjectContract** 權限分割 **Create_Product** 權限。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="bc5c6-138">刪除發票明細會造成 **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** 上的 null 參照失敗。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
