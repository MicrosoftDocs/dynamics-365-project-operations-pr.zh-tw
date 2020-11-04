---
title: Project Service Automation V3 更新版本 24 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 24 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072948"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="87f47-103">Project Service Automation 更新版本 24 V3</span><span class="sxs-lookup"><span data-stu-id="87f47-103">Project Service Automation Update Release 24, V3</span></span>

<span data-ttu-id="87f47-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="87f47-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="87f47-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="87f47-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="87f47-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="87f47-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="87f47-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="87f47-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="87f47-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="87f47-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="87f47-109">本主題列出 Project Service Automation V3 更新版本 24 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="87f47-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="87f47-110">此版本的組建編號為 V 3.10.42.43，已於 2020 年 10 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="87f47-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="87f47-111">更新版本 24</span><span class="sxs-lookup"><span data-stu-id="87f47-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="87f47-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="87f47-112">Bug fixes</span></span>

<span data-ttu-id="87f47-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="87f47-113">**Sales**</span></span>

<span data-ttu-id="87f47-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="87f47-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="87f47-115">設定產品的預設價目表時發生問題。</span><span class="sxs-lookup"><span data-stu-id="87f47-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="87f47-116">報價成交效能因內嵌價目表及角色價格記錄複本而變慢。</span><span class="sxs-lookup"><span data-stu-id="87f47-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="87f47-117">**專案合約/銷售中心** > **產品條項/訂單明細數量** 會自動捨入至最接近的整數。</span><span class="sxs-lookup"><span data-stu-id="87f47-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="87f47-118">讀取價目表時，提高權限至系統權限。</span><span class="sxs-lookup"><span data-stu-id="87f47-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="87f47-119">將客戶地址欄位 **address1_freighttermscode** 及 **address1_shippingmethodcode** 複製到報價/訂單。</span><span class="sxs-lookup"><span data-stu-id="87f47-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="87f47-120">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="87f47-120">**Time and Expense**</span></span>

<span data-ttu-id="87f47-121">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="87f47-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="87f47-122">**時間項目網格** 不支援 **只有日期** 時間行為。</span><span class="sxs-lookup"><span data-stu-id="87f47-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="87f47-123">**時間項目** 未自動重新整理。</span><span class="sxs-lookup"><span data-stu-id="87f47-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="87f47-124">需要手動重新整理。</span><span class="sxs-lookup"><span data-stu-id="87f47-124">A manual refresh is required.</span></span>
- <span data-ttu-id="87f47-125">資源指派中有休息時數 (0 小時) 時，無法從指派匯入時間項目。</span><span class="sxs-lookup"><span data-stu-id="87f47-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="87f47-126">建立時間項目時，將開始時間設定成與 **msdyn_date** 相同。</span><span class="sxs-lookup"><span data-stu-id="87f47-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="87f47-127">重新啟用對時間項目的大量編輯。</span><span class="sxs-lookup"><span data-stu-id="87f47-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="87f47-128">**資源管理**</span><span class="sxs-lookup"><span data-stu-id="87f47-128">**Resource Management**</span></span>

<span data-ttu-id="87f47-129">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="87f47-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="87f47-130">嘗試更新無需求異日間預約的狀態會擲回 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="87f47-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="87f47-131">載入 **協調檢視表** 時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="87f47-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="87f47-132">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="87f47-132">**Project Management**</span></span>

<span data-ttu-id="87f47-133">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="87f47-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="87f47-134">在 **專案排程** 中，從 **手動** 變更為 **自動** 時，自動儲存將不會完成。</span><span class="sxs-lookup"><span data-stu-id="87f47-134">In the **Project Schedule** , when changing from **Manual** to **Auto** , auto save is not completing.</span></span>
- <span data-ttu-id="87f47-135">費用成本不應在 **專案追蹤網格** 上針對差異進行計算。</span><span class="sxs-lookup"><span data-stu-id="87f47-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="87f47-136">**估計值標籤** 欄在載入期間相對於變更 **分時期** 類型時的行為不一致。</span><span class="sxs-lookup"><span data-stu-id="87f47-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="87f47-137">專案的實際成本可能不會反映 **實際值** 的總計。</span><span class="sxs-lookup"><span data-stu-id="87f47-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="87f47-138">**摘要** 索引標籤上的 **估計完成日期** 與 **WBS 排程** 不相符。</span><span class="sxs-lookup"><span data-stu-id="87f47-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="87f47-139">凸排上的 **更新實際時數** 無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="87f47-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="87f47-140">在根 **業務單位** 外部的專案經理無法建立專案。</span><span class="sxs-lookup"><span data-stu-id="87f47-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="87f47-141">對 **費用估計值** 的工作或類別所做的變更無法保存。</span><span class="sxs-lookup"><span data-stu-id="87f47-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="87f47-142">**合約複本** 會複製發票排程和執行狀態。</span><span class="sxs-lookup"><span data-stu-id="87f47-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="87f47-143">**重新整理實際值** 按鈕未正確計算摘要工作。</span><span class="sxs-lookup"><span data-stu-id="87f47-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="87f47-144">Microsoft Project 增益集：如果任何團隊成員有空白資源分配單位，則修正 Null 參考錯誤。</span><span class="sxs-lookup"><span data-stu-id="87f47-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

