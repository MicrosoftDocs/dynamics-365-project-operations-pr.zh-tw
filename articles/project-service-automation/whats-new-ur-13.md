---
title: Project Service Automation V3 更新版本 13 的新功能
description: 本主題提供 Project Service Automation V3 更新版本 13 中新功能的相關資訊。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749914"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="c3026-103">Project Service Automation V3 更新版本 13 的新功能</span><span class="sxs-lookup"><span data-stu-id="c3026-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="c3026-104">我們很高興宣布 Dynamics 365 Project Service Automation (PSA) 應用程式的最新更新。</span><span class="sxs-lookup"><span data-stu-id="c3026-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="c3026-105">此版本包含一些對品質、效能和可用性的重要改進。</span><span class="sxs-lookup"><span data-stu-id="c3026-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c3026-106">此版本與 Dynamics 365 9. x 相容。</span><span class="sxs-lookup"><span data-stu-id="c3026-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c3026-107">若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，然後移至解決方案頁面以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="c3026-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="c3026-108">如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="c3026-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c3026-109">本主題列出 Project Service Automation V3 更新版本 13 新推出或已變更的功能及修正。</span><span class="sxs-lookup"><span data-stu-id="c3026-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="c3026-110">這個版本的組建編號為 V3.10.3.18，依照下列排程提供：</span><span class="sxs-lookup"><span data-stu-id="c3026-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="c3026-111">**正式運作 (自我更新)：** 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="c3026-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="c3026-112">**自動更新：** 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="c3026-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="c3026-113">更新版本 13</span><span class="sxs-lookup"><span data-stu-id="c3026-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="c3026-114">錯誤修正</span><span class="sxs-lookup"><span data-stu-id="c3026-114">Bug fixes</span></span>

- <span data-ttu-id="c3026-115">時間和費用</span><span class="sxs-lookup"><span data-stu-id="c3026-115">Time and Expense</span></span>

     - <span data-ttu-id="c3026-116">已修正：依費用目的進行搜尋時，**費用核准l**頁面上的搜尋功能無法運作。</span><span class="sxs-lookup"><span data-stu-id="c3026-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="c3026-117">資源管理</span><span class="sxs-lookup"><span data-stu-id="c3026-117">Resource Management</span></span>

     - <span data-ttu-id="c3026-118">已修正：協調中的數字已更新為靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="c3026-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="c3026-119">已修正：無法透過**排程**索引標籤將具名資源指派給工作。</span><span class="sxs-lookup"><span data-stu-id="c3026-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="c3026-120">專案管理</span><span class="sxs-lookup"><span data-stu-id="c3026-120">Project Management</span></span>

     - <span data-ttu-id="c3026-121">已修正：在 **TransactionType** 缺少 **Unit** 及 **DefaultGroup** 設定資訊的情況下指派團隊成員時，發生 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c3026-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="c3026-122">Sales</span><span class="sxs-lookup"><span data-stu-id="c3026-122">Sales</span></span>

     - <span data-ttu-id="c3026-123">已修正：建立角色價格記錄時，重複的交易類型記錄傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c3026-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="c3026-124">已修正：**新商機**、**報價**、**訂單明細**和**新增產品**的額外按鈕出現在商機、報價、訂單產品及專案型明細子格的命令中。</span><span class="sxs-lookup"><span data-stu-id="c3026-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


