---
title: Project Service Automation V3 更新版本 20 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 20 V3 中提供的功能和修正
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 5562b1de1d655328cfbb22e46c7fed53525507b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006501"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="4e516-103">Project Service Automation 更新版本 20 V3</span><span class="sxs-lookup"><span data-stu-id="4e516-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4e516-104">我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="4e516-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4e516-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="4e516-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4e516-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="4e516-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4e516-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="4e516-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4e516-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="4e516-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4e516-109">本主題列出 Project Service Automation V3 更新版本 20 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="4e516-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="4e516-110">此版本的組建編號為 V 3.10.31.37，已於 2020 年 6 月透過自我更新正式發行。</span><span class="sxs-lookup"><span data-stu-id="4e516-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="4e516-111">更新版本 20</span><span class="sxs-lookup"><span data-stu-id="4e516-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4e516-112">Bug 修正</span><span class="sxs-lookup"><span data-stu-id="4e516-112">Bug fixes</span></span>

<span data-ttu-id="4e516-113">**專案管理**</span><span class="sxs-lookup"><span data-stu-id="4e516-113">**Project Management**</span></span>

<span data-ttu-id="4e516-114">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="4e516-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="4e516-115">使用需要時數的配置方法匯入專案團隊成員會在指定的時數為零時產生不明確的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4e516-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="4e516-116">在專案工作的 **描述** 欄位中輸入數目已達上限的字元時，使用者收到不正確的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4e516-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="4e516-117">當使用者的語言設定設為日文時，**Microsoft Dynamics 365 Project Service Automation 增益集下載** 頁面會重新導向至英文下載頁面。</span><span class="sxs-lookup"><span data-stu-id="4e516-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="4e516-118">發生伺服器錯誤時，**專案** 表單 **排程** 索引標籤上的同步處理標籤有時會保留。</span><span class="sxs-lookup"><span data-stu-id="4e516-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="4e516-119">工作遭修改時，多餘的工作更新將會傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="4e516-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="4e516-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4e516-120">**Sales**</span></span>

<span data-ttu-id="4e516-121">下列問題已獲修正：</span><span class="sxs-lookup"><span data-stu-id="4e516-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="4e516-122">在 **合約** 表單上，按兩下 **建立發票** 會為單一實際值記錄建立兩份發票。</span><span class="sxs-lookup"><span data-stu-id="4e516-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="4e516-123">在 Internet Explorer 11 中，使用者無法建立費用分錄。</span><span class="sxs-lookup"><span data-stu-id="4e516-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="4e516-124">成本沖回與未開單銷售實際值沖回未連結。</span><span class="sxs-lookup"><span data-stu-id="4e516-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="4e516-125">**專案** 表單上的 **重新整理實際值** 按鈕不會重新整理 **工作實際時數**。</span><span class="sxs-lookup"><span data-stu-id="4e516-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="4e516-126">將 **msdyn_isgenericresourceprojectscoped** 屬性設定為 **否** 時，**PreValidateProjectTeamMemberCreate** 外掛程式可能會建立重複的一般可預約資源。</span><span class="sxs-lookup"><span data-stu-id="4e516-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="4e516-127">**重新計算** 會清除產品型報價明細詳細資料和合約服務內容詳細資料的應收費成本。</span><span class="sxs-lookup"><span data-stu-id="4e516-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="4e516-128">在特定案例中，**PostEstimateLineUpdate** 外掛程式會顯示 Null 參考例外狀況錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e516-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="4e516-129">**獲利率分析圖表** 的時間階段期間與報價固定價格報價明細詳細資料中的成本期間不相符。</span><span class="sxs-lookup"><span data-stu-id="4e516-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="4e516-130">在 **合約服務內容詳細資料** 和 **報價明細詳細資料** 表單上的費用類別未正確設定單位與單位群組的預設值。</span><span class="sxs-lookup"><span data-stu-id="4e516-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="4e516-131">**組織單位成本價** 清單允許日期時效性有重疊。</span><span class="sxs-lookup"><span data-stu-id="4e516-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="4e516-132">當訂單類型不是工作型時，不允許使用者變更 **組織單位**，因為這會導致 Null 參考例外狀況錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e516-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="4e516-133">嘗試從 **報價明細詳細資料** 表單瀏覽返回 **報價** 索引標籤時，表單會重新整理並顯示 **摘要** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="4e516-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]