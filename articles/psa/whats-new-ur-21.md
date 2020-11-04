---
title: Project Service Automation V3 更新版本 21 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 21 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072947"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="eab11-103">Project Service Automation 更新版本 21 V3</span><span class="sxs-lookup"><span data-stu-id="eab11-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="eab11-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="eab11-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="eab11-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="eab11-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="eab11-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="eab11-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="eab11-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="eab11-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="eab11-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="eab11-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="eab11-109">本主題列出 Project Service Automation V3 更新版本 21 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="eab11-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="eab11-110">此版本的組建編號為 V 3.10.32.50，已於 2020 年 6 月透過自我更新正式發行。</span><span class="sxs-lookup"><span data-stu-id="eab11-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="eab11-111">更新版本 21</span><span class="sxs-lookup"><span data-stu-id="eab11-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="eab11-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="eab11-112">Bug fixes</span></span>

<span data-ttu-id="eab11-113">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="eab11-113">**Time and Expense**</span></span>

<span data-ttu-id="eab11-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="eab11-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="eab11-115">在儀表板中裝載 **時間項目網格控制項** 時，網格未使用儀表板網格容器的全幅寬度。</span><span class="sxs-lookup"><span data-stu-id="eab11-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="eab11-116">對於特定時區， **時間項目** 網格控制項無法顯示記錄。</span><span class="sxs-lookup"><span data-stu-id="eab11-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="eab11-117">下午 9:00 以後的時間項目出現在錯誤的日期上。</span><span class="sxs-lookup"><span data-stu-id="eab11-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="eab11-118">如果費用類別 **需要費用收據** 沒有值，使用者就無法提交費用。</span><span class="sxs-lookup"><span data-stu-id="eab11-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="eab11-119">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="eab11-119">**Resource Management**</span></span>

<span data-ttu-id="eab11-120">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="eab11-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="eab11-121">非使用中預約會顯示 **協調** 檢視表中。</span><span class="sxs-lookup"><span data-stu-id="eab11-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="eab11-122">一般資源履行缺少驗證，無法確保存在有效的預約狀態。</span><span class="sxs-lookup"><span data-stu-id="eab11-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="eab11-123">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="eab11-123">**Project Management**</span></span>

<span data-ttu-id="eab11-124">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="eab11-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="eab11-125">即使專案處於非使用中狀態， **專案** 表單網格 ( **資源指派** 、 **工作** 、 **協調** 檢視表、 **費用估計值** ) 仍會保持可編輯。</span><span class="sxs-lookup"><span data-stu-id="eab11-125">The **Project** form grids ( **Resource Assignment** , **Task** , **Reconciliation** view, **Expense Estimates** ) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="eab11-126">重複的客戶無法與連結至已確認專案合約的客戶合併。</span><span class="sxs-lookup"><span data-stu-id="eab11-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="eab11-127">新增未具備有效行事曆的資源時，系統不會傳回使用者易懂的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="eab11-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="eab11-128">當專案連結至 **Microsoft Project 增益集** 時，工作網格會啟用 **新增工作** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="eab11-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="eab11-129">當工作的類別已指派給其角色沒有定義成本價的資源時，投入量會不受控制地擴大。</span><span class="sxs-lookup"><span data-stu-id="eab11-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="eab11-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="eab11-130">**Sales**</span></span>

<span data-ttu-id="eab11-131">我們已進行下列增強：</span><span class="sxs-lookup"><span data-stu-id="eab11-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="eab11-132">**發票頻率** 和 **帳單開始日期** 已移到 **發票排程** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="eab11-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="eab11-133">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="eab11-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="eab11-134">**類別** 的 **總售價** 為零 (0)，即使 **角色** 的總售價不為零也一樣。</span><span class="sxs-lookup"><span data-stu-id="eab11-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="eab11-135">另一個自訂程序正在更新其他欄位時，客戶無法將 **發票狀態** 欄位值變更為 **已準備好開立發票** 。</span><span class="sxs-lookup"><span data-stu-id="eab11-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="eab11-136">如果重複選取 **重新整理發票明細** 按鈕，此按鈕可以建立多個重複的明細。</span><span class="sxs-lookup"><span data-stu-id="eab11-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="eab11-137">**更新價格** 按鈕對 **快速檢視** 表單中的 **角色價格** 子格沒有作用。</span><span class="sxs-lookup"><span data-stu-id="eab11-137">The **Update Prices** button doesn't work on the **Role Prices** sub-grid in the **Quick View** form.</span></span>
- <span data-ttu-id="eab11-138">**銷售價目表解析** 邏輯處理時區不當，導致錯誤選擇價目表。</span><span class="sxs-lookup"><span data-stu-id="eab11-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="eab11-139">核准單一時間項目之後，專案的 **總實際成本** 可能會不計整數以外尾數的金額。</span><span class="sxs-lookup"><span data-stu-id="eab11-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="eab11-140">如果 **擷取的角色價格** 沒有 **主要單位** 及 **以主要單位計的價格** 欄位中的值， **價格解析** 邏輯無法提供使用者易懂的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="eab11-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
