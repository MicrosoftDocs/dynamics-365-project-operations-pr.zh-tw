---
title: Project Service Automation V3 更新版本 19 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 19 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 8a73a6acd4ce4c9559cdf4591ede735a613f4d52
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143596"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="eb0e4-103">Project Service Automation 更新版本 19 V3</span><span class="sxs-lookup"><span data-stu-id="eb0e4-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="eb0e4-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="eb0e4-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="eb0e4-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="eb0e4-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="eb0e4-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="eb0e4-109">本主題列出 PSA V3 更新版本 19 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="eb0e4-110">此版本的組建編號是 V3.10.30.41，已於 2020 年 5 月透過自我更新正式推出。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="eb0e4-111">更新版本 19</span><span class="sxs-lookup"><span data-stu-id="eb0e4-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="eb0e4-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="eb0e4-112">Bug fixes</span></span>

<span data-ttu-id="eb0e4-113">**時間和費用**</span><span class="sxs-lookup"><span data-stu-id="eb0e4-113">**Time and Expense**</span></span>

<span data-ttu-id="eb0e4-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="eb0e4-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="eb0e4-115">無法正確顯示從時間項目匯入衍生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="eb0e4-116">時間項目網格不支援 **只有日期** 欄位行為。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="eb0e4-117">專案資源無法建立專案的費用。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="eb0e4-118">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="eb0e4-118">**Project Management**</span></span>

<span data-ttu-id="eb0e4-119">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="eb0e4-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="eb0e4-120">下下層工作在完工估計值 (EAC) 計算過程中造成努力估計值不正確。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="eb0e4-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="eb0e4-121">**Sales**</span></span>

<span data-ttu-id="eb0e4-122">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="eb0e4-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="eb0e4-123">**重新計算** 動作無法使用費用合約服務內容詳細資料或報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="eb0e4-124">費用估計值缺少 **更新價格**。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="eb0e4-125">客戶無法從 **專案合約** 頁面選取自訂合約狀態原因。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="eb0e4-126">從報價建立自訂價目表時，客戶感受到效能變差。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="eb0e4-127">客戶發現 **報價明細詳細資料** 與 **合約服務內容詳細資料** 頁面上的 **單位** 預設值不一致。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="eb0e4-128">將非收費交易類別項目新增至收費合約服務內容時，不會採用 **非收費** 帳單類型的交易類別。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="eb0e4-129">客戶無法在先前建立的合約上使用新加入的角色和類別。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="eb0e4-130">客戶感受到效能變差 PreValidateProjectTeamMemberUpdate.cs 中不必要的擷取</span><span class="sxs-lookup"><span data-stu-id="eb0e4-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="eb0e4-131">必須將 **資源類別** 清單中設定為非收費的角色當做專案合約服務內容的 **非收費項目** 新增至 **收費角色** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="eb0e4-132">建立專案時，客戶可能會感受到效能變差，因為 **GetBookableResourceIdFromUser** 擷取的是可預約資源所有的欄，而不只是主要識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="eb0e4-133">**TransactionType** 實體缺少預先驗證更新外掛程式，無法防止使用者輸入對交易類型不正確的 **單位** 和 **單位群組**。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="eb0e4-134">**移除** 步驟不適用於時間項目匯入。</span><span class="sxs-lookup"><span data-stu-id="eb0e4-134">The **Remove** step does not work for time entry import.</span></span>
