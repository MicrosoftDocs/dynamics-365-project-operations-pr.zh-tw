---
title: 2021 年 2 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 本主題提供有關資源/非庫存型案例適用的 Project Operations 2021 年 2 月版本所提供的品質更新資訊。
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8270214d47f712cdb0942991b0ffb5baff64cbfb
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948004"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="8822f-103">2021 年 2 月 - 資源/非庫存型案例適用的 Project Operations 新增功能</span><span class="sxs-lookup"><span data-stu-id="8822f-103">What's new February 2021 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="8822f-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="8822f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8822f-105">此主題適用於下列 Dynamics 365 Project Operations 元件和版本：</span><span class="sxs-lookup"><span data-stu-id="8822f-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="8822f-106">Dataverse 環境 4.7.0.95 上的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="8822f-106">Project Operations on Dataverse environment 4.7.0.95</span></span>
- <span data-ttu-id="8822f-107">Dynamics 365 Finance 環境 10.0.16 版本的專案管理與會計</span><span class="sxs-lookup"><span data-stu-id="8822f-107">Project management and accounting in Dynamics 365 Finance environment version 10.0.16</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="8822f-108">品質更新</span><span class="sxs-lookup"><span data-stu-id="8822f-108">Quality updates</span></span>

### <a name="project-operations-on-dataverse"></a><span data-ttu-id="8822f-109">Dataverse 上的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="8822f-109">Project Operations on Dataverse</span></span>

| <span data-ttu-id="8822f-110">**功能區域**</span><span class="sxs-lookup"><span data-stu-id="8822f-110">**Feature Area**</span></span> | <span data-ttu-id="8822f-111">**參考編號**</span><span class="sxs-lookup"><span data-stu-id="8822f-111">**Reference number**</span></span> | <span data-ttu-id="8822f-112">**品質更新**</span><span class="sxs-lookup"><span data-stu-id="8822f-112">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8822f-113">**帳單和定價**</span><span class="sxs-lookup"><span data-stu-id="8822f-113">**Billing and Pricing**</span></span> | <span data-ttu-id="8822f-114">2053736</span><span class="sxs-lookup"><span data-stu-id="8822f-114">2053736</span></span> | <span data-ttu-id="8822f-115">現在可移至 **發票** > **相關資訊** 存取發票明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8822f-115">Invoice line details are now accessible by going to **Invoice** > **Related information**.</span></span> |
| <span data-ttu-id="8822f-116">**帳單和定價**</span><span class="sxs-lookup"><span data-stu-id="8822f-116">**Billing and Pricing**</span></span> | <span data-ttu-id="8822f-117">2122613</span><span class="sxs-lookup"><span data-stu-id="8822f-117">2122613</span></span> | <span data-ttu-id="8822f-118">**啟用** 和 **停用** 動作已從 **價目表** 關聯實體中移除。</span><span class="sxs-lookup"><span data-stu-id="8822f-118">The **Activate** and **Deactivate** actions were removed from the **Price List** association entities.</span></span> |
| <span data-ttu-id="8822f-119">**帳單和定價**</span><span class="sxs-lookup"><span data-stu-id="8822f-119">**Billing and Pricing**</span></span> | <span data-ttu-id="8822f-120">2128606</span><span class="sxs-lookup"><span data-stu-id="8822f-120">2128606</span></span> | <span data-ttu-id="8822f-121">解決 **GetEstimatesForProject** 外掛程式中有關 **ullReferenceException** 的問題。</span><span class="sxs-lookup"><span data-stu-id="8822f-121">Resolved the issue with **ullReferenceException** in the **GetEstimatesForProject** plug-in.</span></span> |
| <span data-ttu-id="8822f-122">**部署和設定**</span><span class="sxs-lookup"><span data-stu-id="8822f-122">**Deployment and configuration**</span></span> | <span data-ttu-id="8822f-123">2139346</span><span class="sxs-lookup"><span data-stu-id="8822f-123">2139346</span></span> | <span data-ttu-id="8822f-124">解決匯入未受管理的 **Dynamics365ProjectOperationsDualWrite** 解決方案的問題。</span><span class="sxs-lookup"><span data-stu-id="8822f-124">Resolved the issue with importing unmanaged **Dynamics365ProjectOperationsDualWrite** solution.</span></span> |
| <span data-ttu-id="8822f-125">**部署和設定**</span><span class="sxs-lookup"><span data-stu-id="8822f-125">**Deployment and configuration**</span></span> | <span data-ttu-id="8822f-126">2140569</span><span class="sxs-lookup"><span data-stu-id="8822f-126">2140569</span></span> | <span data-ttu-id="8822f-127">不可將 Project 解決方案安裝在 Dataverse Teams 環境中。</span><span class="sxs-lookup"><span data-stu-id="8822f-127">Project solution must not be installed in the Dataverse Teams environments.</span></span> |
| <span data-ttu-id="8822f-128">**部署和設定**</span><span class="sxs-lookup"><span data-stu-id="8822f-128">**Deployment and configuration**</span></span> | <span data-ttu-id="8822f-129">2086991</span><span class="sxs-lookup"><span data-stu-id="8822f-129">2086991</span></span> | <span data-ttu-id="8822f-130">限制自訂 Web 資源的當地語系化。</span><span class="sxs-lookup"><span data-stu-id="8822f-130">Restricted customizing localization of web resources.</span></span> |
| <span data-ttu-id="8822f-131">**商機管理**</span><span class="sxs-lookup"><span data-stu-id="8822f-131">**Opportunity Management**</span></span> | <span data-ttu-id="8822f-132">2136794</span><span class="sxs-lookup"><span data-stu-id="8822f-132">2136794</span></span> | <span data-ttu-id="8822f-133">在 **確認發票** 或 **將發票標示為已付** 程序失敗時顯示正確的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="8822f-133">Display the correct error message when the **Confirm invoice** or **Mark invoice as paid** processes fail.</span></span> |
| <span data-ttu-id="8822f-134">**商機管理**</span><span class="sxs-lookup"><span data-stu-id="8822f-134">**Opportunity Management**</span></span> | <span data-ttu-id="8822f-135">2139330</span><span class="sxs-lookup"><span data-stu-id="8822f-135">2139330</span></span> | <span data-ttu-id="8822f-136">變更專案的專案經理時，不可將擁有公司重設回預設值。</span><span class="sxs-lookup"><span data-stu-id="8822f-136">Changing the Project manager on a project must not reset the owning company back to the default value.</span></span> |
| <span data-ttu-id="8822f-137">**商機管理**</span><span class="sxs-lookup"><span data-stu-id="8822f-137">**Opportunity Management**</span></span> | <span data-ttu-id="8822f-138">2146376</span><span class="sxs-lookup"><span data-stu-id="8822f-138">2146376</span></span> | <span data-ttu-id="8822f-139">不應收費實際值中已更正的稅金金額是從發票確認所建立。</span><span class="sxs-lookup"><span data-stu-id="8822f-139">Corrected tax amount in a non-chargeable actual is created from invoice confirmation.</span></span> |
| <span data-ttu-id="8822f-140">**專案規劃和追蹤**</span><span class="sxs-lookup"><span data-stu-id="8822f-140">**Project Planning and Tracking**</span></span> | <span data-ttu-id="8822f-141">2099879</span><span class="sxs-lookup"><span data-stu-id="8822f-141">2099879</span></span> | <span data-ttu-id="8822f-142">Dataverse 環境部署必須使用靜態識別碼建立預設交易類別，不可每個環境隨機產生一個類別。</span><span class="sxs-lookup"><span data-stu-id="8822f-142">The Dataverse environment deployment must create a default transaction category with a static ID and not randomly generate one per environment.</span></span> |
| <span data-ttu-id="8822f-143">**專案規劃和追蹤**</span><span class="sxs-lookup"><span data-stu-id="8822f-143">**Project Planning and Tracking**</span></span> | <span data-ttu-id="8822f-144">2128577</span><span class="sxs-lookup"><span data-stu-id="8822f-144">2128577</span></span> | <span data-ttu-id="8822f-145">修正 Project Service 使用者權限，以更新資源指派上的交易類別。</span><span class="sxs-lookup"><span data-stu-id="8822f-145">Fixed the Project service user privileges to update the transaction category on a resource assignment.</span></span> |
| <span data-ttu-id="8822f-146">**專案規劃和追蹤**</span><span class="sxs-lookup"><span data-stu-id="8822f-146">**Project Planning and Tracking**</span></span> | <span data-ttu-id="8822f-147">2164035</span><span class="sxs-lookup"><span data-stu-id="8822f-147">2164035</span></span> | <span data-ttu-id="8822f-148">修正 **複製專案** 功能的問題。</span><span class="sxs-lookup"><span data-stu-id="8822f-148">Fixed issues with the **Copy Project** function.</span></span> |
| <span data-ttu-id="8822f-149">**時間項目**</span><span class="sxs-lookup"><span data-stu-id="8822f-149">**Time entry**</span></span> | <span data-ttu-id="8822f-150">2129161</span><span class="sxs-lookup"><span data-stu-id="8822f-150">2129161</span></span> | <span data-ttu-id="8822f-151">套用更嚴格的限制，以確保使用者無法變更和更新已提交或核准的時間項目。</span><span class="sxs-lookup"><span data-stu-id="8822f-151">Tighter restrictions are applied to ensure users can't change and update a time entry that has been submitted or approved.</span></span> |
| <span data-ttu-id="8822f-152">**時間項目**</span><span class="sxs-lookup"><span data-stu-id="8822f-152">**Time entry**</span></span> | <span data-ttu-id="8822f-153">2103572</span><span class="sxs-lookup"><span data-stu-id="8822f-153">2103572</span></span> | <span data-ttu-id="8822f-154">非專案時間項目的時間核准不得尋找專案核准者角色。</span><span class="sxs-lookup"><span data-stu-id="8822f-154">Time approval for non-project time entries must not be looking for project approver role.</span></span> |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a><span data-ttu-id="8822f-155">Dynamics 365 Finance 中的專案管理與會計</span><span class="sxs-lookup"><span data-stu-id="8822f-155">Project management and accounting in Dynamics 365 Finance</span></span> 

<span data-ttu-id="8822f-156">如需 Dynamics 365 Finance 中 [專案管理與會計] 的詳細資訊，請參閱 [2021 年 1 月 - 資源/非庫存型案例適用的 Project Operations 新增功能](whats-new-jan-2021-resource-based.md)。</span><span class="sxs-lookup"><span data-stu-id="8822f-156">For more information about Project management and accounting in Dynamics 365 Finance, see [What's new January 2021 - Project Operations for resource/non-stocked based scenarios](whats-new-jan-2021-resource-based.md).</span></span>


## <a name="regulatory-updates"></a><span data-ttu-id="8822f-157">法規更新</span><span class="sxs-lookup"><span data-stu-id="8822f-157">Regulatory updates</span></span>

<span data-ttu-id="8822f-158">如需 Finance and Operations 應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。</span><span class="sxs-lookup"><span data-stu-id="8822f-158">For information about regulatory updates for Finance and Operations apps, see [Regulatory updates](/dynamics365/finance/localizations/regulatory-updates).</span></span> <span data-ttu-id="8822f-159">另一個了解法規更新的方式就是，登入 Lifecycle Services (LCS)，並使用問題搜尋工具來檢視已規劃的法規更新。</span><span class="sxs-lookup"><span data-stu-id="8822f-159">Another way to learn about regulatory updates is to sign in to Lifecycle Services (LCS) and view the planned regulatory updates using the issue search tool.</span></span> <span data-ttu-id="8822f-160">問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="8822f-160">Issue search lets you search by country, type of feature, and release.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]