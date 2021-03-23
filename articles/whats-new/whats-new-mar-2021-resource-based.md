---
title: 2021 年 3 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 本主題提供有關資源/非庫存型案例適用的 Project Operations 2021 年 3 月版本所提供的品質更新資訊。
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 95a9251707de3699322471535aa93070ba4fb2ae
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499983"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="db835-103">2021 年 3 月 - 資源/非庫存型案例適用的 Project Operations 新增功能</span><span class="sxs-lookup"><span data-stu-id="db835-103">What's new March 2021 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="db835-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="db835-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="db835-105">此主題適用於下列 Dynamics 365 Project Operations 元件和版本：</span><span class="sxs-lookup"><span data-stu-id="db835-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="db835-106">Dataverse 環境的 Project Operations 版本 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="db835-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 
- <span data-ttu-id="db835-107">Dynamics 365 Finance 環境 10.0.16 版中的專案管理與會計</span><span class="sxs-lookup"><span data-stu-id="db835-107">Project management and accounting on Dynamics 365 Finance environment version 10.0.16</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="db835-108">品質更新</span><span class="sxs-lookup"><span data-stu-id="db835-108">Quality updates</span></span>

### <a name="project-operations-on-dataverse"></a><span data-ttu-id="db835-109">Dataverse 上的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="db835-109">Project Operations on Dataverse</span></span>


| <span data-ttu-id="db835-110">**功能區域**</span><span class="sxs-lookup"><span data-stu-id="db835-110">**Feature area**</span></span> | <span data-ttu-id="db835-111">**參考編號**</span><span class="sxs-lookup"><span data-stu-id="db835-111">**Reference number**</span></span> | <span data-ttu-id="db835-112">**品質更新**</span><span class="sxs-lookup"><span data-stu-id="db835-112">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="db835-113">帳單和定價</span><span class="sxs-lookup"><span data-stu-id="db835-113">Billing and pricing</span></span> | <span data-ttu-id="db835-114">2133873</span><span class="sxs-lookup"><span data-stu-id="db835-114">2133873</span></span> | <span data-ttu-id="db835-115">修正 **銷售單價** 貨幣符號在 **費用估計值** 網格中的顯示。</span><span class="sxs-lookup"><span data-stu-id="db835-115">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="db835-116">帳單和定價</span><span class="sxs-lookup"><span data-stu-id="db835-116">Billing and pricing</span></span> | <span data-ttu-id="db835-117">2174616</span><span class="sxs-lookup"><span data-stu-id="db835-117">2174616</span></span> | <span data-ttu-id="db835-118">報價成交時，從報價複製而來的合約服務內容詳細資料會參考合約自訂價目表。</span><span class="sxs-lookup"><span data-stu-id="db835-118">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="db835-119">商機管理</span><span class="sxs-lookup"><span data-stu-id="db835-119">Opportunity Management</span></span> | <span data-ttu-id="db835-120">2167475</span><span class="sxs-lookup"><span data-stu-id="db835-120">2167475</span></span> | <span data-ttu-id="db835-121">修正源自未開單實際值項目之更正發票中的稅額。</span><span class="sxs-lookup"><span data-stu-id="db835-121">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="db835-122">商機管理</span><span class="sxs-lookup"><span data-stu-id="db835-122">Opportunity Management</span></span> | <span data-ttu-id="db835-123">2176285</span><span class="sxs-lookup"><span data-stu-id="db835-123">2176285</span></span> | <span data-ttu-id="db835-124">不可將銷售合約/報價明細詳細資料中的稅額複製到成本合約/報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="db835-124">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="db835-125">商機管理</span><span class="sxs-lookup"><span data-stu-id="db835-125">Opportunity Management</span></span> | <span data-ttu-id="db835-126">2188079</span><span class="sxs-lookup"><span data-stu-id="db835-126">2188079</span></span> | <span data-ttu-id="db835-127">不可建立非工作型合約的分割帳單規則。</span><span class="sxs-lookup"><span data-stu-id="db835-127">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="db835-128">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="db835-128">Planning and Tracking</span></span> | <span data-ttu-id="db835-129">2125274</span><span class="sxs-lookup"><span data-stu-id="db835-129">2125274</span></span> | <span data-ttu-id="db835-130">將 **專案開始日期對應** 的 **專案 雙重寫入對應** 屬性從 **msdyn\_taskearlieststart** 為 **msdyn\_actualstart**。</span><span class="sxs-lookup"><span data-stu-id="db835-130">**Project Dual Write Map** attribute for **Project Start Date Mapping** updated from **msdyn\_taskearlieststart** to **msdyn\_actualstart**.</span></span> |
| <span data-ttu-id="db835-131">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="db835-131">Planning and Tracking</span></span> | <span data-ttu-id="db835-132">2138853</span><span class="sxs-lookup"><span data-stu-id="db835-132">2138853</span></span> | <span data-ttu-id="db835-133">更新專案複製功能，確保已將參考工作的費用估計明細複製到目的地專案。</span><span class="sxs-lookup"><span data-stu-id="db835-133">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="db835-134">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="db835-134">Planning and Tracking</span></span> | <span data-ttu-id="db835-135">2154306</span><span class="sxs-lookup"><span data-stu-id="db835-135">2154306</span></span> | <span data-ttu-id="db835-136">修正與刪除資源型案例適用 Project Operations 中費用估計值有關的問題。</span><span class="sxs-lookup"><span data-stu-id="db835-136">Fixed issues with deleting expense estimates in Project Operations for resource-based scenarios.</span></span> |
| <span data-ttu-id="db835-137">規劃和追蹤</span><span class="sxs-lookup"><span data-stu-id="db835-137">Planning and Tracking</span></span> | <span data-ttu-id="db835-138">2173259</span><span class="sxs-lookup"><span data-stu-id="db835-138">2173259</span></span> | <span data-ttu-id="db835-139">更新專案複製功能，以確保此功能不會在特定案例中顯示 **複製 WBS** 錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="db835-139">Project copy function updated to ensure it doesn't display **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="db835-140">時間和費用</span><span class="sxs-lookup"><span data-stu-id="db835-140">Time and Expense</span></span> | <span data-ttu-id="db835-141">2148910</span><span class="sxs-lookup"><span data-stu-id="db835-141">2148910</span></span> | <span data-ttu-id="db835-142">修正 **編輯項目** 頁面在 **時間項目** 網格中的顯示問題。</span><span class="sxs-lookup"><span data-stu-id="db835-142">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="db835-143">時間和費用</span><span class="sxs-lookup"><span data-stu-id="db835-143">Time and Expense</span></span> | <span data-ttu-id="db835-144">2159798</span><span class="sxs-lookup"><span data-stu-id="db835-144">2159798</span></span> | <span data-ttu-id="db835-145">加強控制，以確保無法編輯已核准的費用項目。</span><span class="sxs-lookup"><span data-stu-id="db835-145">Tightened controls to ensure approved expense entries can't be edited.</span></span> |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a><span data-ttu-id="db835-146">Dynamics 365 Finance 中的專案管理與會計</span><span class="sxs-lookup"><span data-stu-id="db835-146">Project management and accounting on Dynamics 365 Finance</span></span>

<span data-ttu-id="db835-147">如需詳細資訊，請參閱 [2021 年 1 月 - 資源/非庫存型案例適用的 Project Operations 新增功能](whats-new-jan-2021-resource-based.md)。</span><span class="sxs-lookup"><span data-stu-id="db835-147">For more information, see [What's new January 2021 - Project Operations for resource/non-stocked based scenarios](whats-new-jan-2021-resource-based.md).</span></span>

## <a name="regulatory-updates"></a><span data-ttu-id="db835-148">法規更新</span><span class="sxs-lookup"><span data-stu-id="db835-148">Regulatory updates</span></span>

<span data-ttu-id="db835-149">如需 Finance and Operations 應用程式的法規更新資訊，請參閱[法規更新](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates)。</span><span class="sxs-lookup"><span data-stu-id="db835-149">For information about regulatory updates for Finance and Operations apps, see [Regulatory updates](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span></span> <span data-ttu-id="db835-150">另一個了解法規更新的方式就是，登入 LCS，並使用問題搜尋工具來檢視已規劃的法規更新。</span><span class="sxs-lookup"><span data-stu-id="db835-150">Another way to learn about regulatory updates is to sign in to LCS and view the planned regulatory updates using the issue search tool.</span></span> <span data-ttu-id="db835-151">問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="db835-151">Issue search lets you search by country, type of feature, and release.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]