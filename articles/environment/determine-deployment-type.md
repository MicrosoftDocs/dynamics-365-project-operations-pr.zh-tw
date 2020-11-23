---
title: 判斷您的部署類型
description: 本主題提供資訊以協助您判斷適合您公司的正確 Project Operations 部署類型。
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401208"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="5e590-103">判斷您的部署類型</span><span class="sxs-lookup"><span data-stu-id="5e590-103">Determine your deployment type</span></span>

<span data-ttu-id="5e590-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="5e590-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e590-105">購買授權之後，請從這裡開始使用[引導式安裝流程](https://aka.ms/provisionprojectoperations)來判斷 Dynamics 365 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="5e590-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="5e590-106">完成引導式安裝流程之後，系統會將您導向至正確的管理入口網站，以完成您的安裝。</span><span class="sxs-lookup"><span data-stu-id="5e590-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="5e590-107">請參閱部署詳細資料，以完成安裝。</span><span class="sxs-lookup"><span data-stu-id="5e590-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="5e590-108">使用 Dynamics 365 Project Service Automation 的 Dynamics 現有客戶</span><span class="sxs-lookup"><span data-stu-id="5e590-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="5e590-109">Project Operations 包含隨附於 Project Service Automation 的功能。</span><span class="sxs-lookup"><span data-stu-id="5e590-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="5e590-110">將會在 2021 年第 1 段發行浪潮中，為這些客戶發行升級路徑。</span><span class="sxs-lookup"><span data-stu-id="5e590-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="5e590-111">使用專案管理與會計的 Dynamics 365 Finance 現有客戶</span><span class="sxs-lookup"><span data-stu-id="5e590-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="5e590-112">使用 [專案管理與會計] 功能的現有 Finance 客戶仍可繼續依照原本方式使用該功能。</span><span class="sxs-lookup"><span data-stu-id="5e590-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="5e590-113">請參閱[庫存/生產訂單案例適用的 Project Operations](#pma)。</span><span class="sxs-lookup"><span data-stu-id="5e590-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="5e590-114">部署類型</span><span class="sxs-lookup"><span data-stu-id="5e590-114">Deployment types</span></span>
<span data-ttu-id="5e590-115">Project Operations 支援多個部署選項，以符合您的需求。</span><span class="sxs-lookup"><span data-stu-id="5e590-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="5e590-116">不論您是新的或現有 Dynamics 365 客戶，Project Operations 都能支援您的需求。</span><span class="sxs-lookup"><span data-stu-id="5e590-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="5e590-117">我們的[部署問卷 ](https://aka.ms/provisionprojectoperations)會協助您判斷適當的部署。</span><span class="sxs-lookup"><span data-stu-id="5e590-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="5e590-118">結果將引導您前往下列其中一個部署類型：</span><span class="sxs-lookup"><span data-stu-id="5e590-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="5e590-119">精簡部署 - 交易至開立預估發票</span><span class="sxs-lookup"><span data-stu-id="5e590-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="5e590-120">資源/非庫存案例適用的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="5e590-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="5e590-121">庫存/生產訂單案例適用的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="5e590-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="5e590-122">Project Operations 透過法律實體層級設定在同一個環境中支援庫存/生產訂單案例以及非庫存/資源型案例。</span><span class="sxs-lookup"><span data-stu-id="5e590-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="5e590-123">例如，Contoso 可以利用其美國製造設施 (法律實體 = Contoso Manufacturing United States) 中的庫存/生產訂單功能。</span><span class="sxs-lookup"><span data-stu-id="5e590-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="5e590-124">Contoso 可以利用其在英國的 Contoso 機器人手臂維修設施 (法律實體 = Contoso Robotics United Kingdom) 中的非庫存/資源型功能。</span><span class="sxs-lookup"><span data-stu-id="5e590-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="5e590-125">精簡部署 - 交易至開立預估發票</span><span class="sxs-lookup"><span data-stu-id="5e590-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="5e590-126">精簡部署包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="5e590-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="5e590-127">延伸 Dynamics 365 Sales 應用程式體驗的專案銷售處理</span><span class="sxs-lookup"><span data-stu-id="5e590-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="5e590-128">使用 Microsoft Project 網頁版進行專案規劃</span><span class="sxs-lookup"><span data-stu-id="5e590-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="5e590-129">多維度定價</span><span class="sxs-lookup"><span data-stu-id="5e590-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="5e590-130">統一資源管理</span><span class="sxs-lookup"><span data-stu-id="5e590-130">Unified resource management</span></span>
- <span data-ttu-id="5e590-131">時間追蹤</span><span class="sxs-lookup"><span data-stu-id="5e590-131">Time tracking</span></span>
- <span data-ttu-id="5e590-132">基本費用</span><span class="sxs-lookup"><span data-stu-id="5e590-132">Basic expense</span></span>
- <span data-ttu-id="5e590-133">開立預估發票和客戶面向發票</span><span class="sxs-lookup"><span data-stu-id="5e590-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="5e590-134">部署步驟</span><span class="sxs-lookup"><span data-stu-id="5e590-134">Deployment steps</span></span>
<span data-ttu-id="5e590-135">使用[部署問卷](https://aka.ms/provisionprojectoperations)來判斷 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="5e590-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="5e590-136">若要進行此部署，請參閱[註冊預覽版訂閱](lite-preview-subscription-sign-up.md)和[佈建新環境](lite-deployment.md)。</span><span class="sxs-lookup"><span data-stu-id="5e590-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="5e590-137">資源/非庫存案例適用的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="5e590-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="5e590-138">資源/非庫存案例適用的 Project Operations 包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="5e590-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="5e590-139">擴充 Dynamics 365 Sales 應用程式的專案銷售處理</span><span class="sxs-lookup"><span data-stu-id="5e590-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="5e590-140">使用 Microsoft Project 網頁版進行專案規劃</span><span class="sxs-lookup"><span data-stu-id="5e590-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="5e590-141">多維度定價</span><span class="sxs-lookup"><span data-stu-id="5e590-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="5e590-142">統一資源管理</span><span class="sxs-lookup"><span data-stu-id="5e590-142">Unified resource management</span></span>
- <span data-ttu-id="5e590-143">時間追蹤</span><span class="sxs-lookup"><span data-stu-id="5e590-143">Time tracking</span></span>
- <span data-ttu-id="5e590-144">基本費用</span><span class="sxs-lookup"><span data-stu-id="5e590-144">Basic expense</span></span>
- <span data-ttu-id="5e590-145">全額費用</span><span class="sxs-lookup"><span data-stu-id="5e590-145">Full expense</span></span>
- <span data-ttu-id="5e590-146">收據 OCR</span><span class="sxs-lookup"><span data-stu-id="5e590-146">Receipt OCR</span></span>
- <span data-ttu-id="5e590-147">開立預估發票和客戶面向發票</span><span class="sxs-lookup"><span data-stu-id="5e590-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="5e590-148">專案的營收認列</span><span class="sxs-lookup"><span data-stu-id="5e590-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="5e590-149">部署步驟</span><span class="sxs-lookup"><span data-stu-id="5e590-149">Deployment steps</span></span>
<span data-ttu-id="5e590-150">使用[部署問卷](https://aka.ms/provisionprojectoperations)來判斷 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="5e590-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="5e590-151">若要進行此部署，請參閱[註冊預覽版訂閱](resource-sign-up-preview-subscription.md)和[佈建新環境](resource-provision-new-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="5e590-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="5e590-152">庫存/生產訂單案例適用的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="5e590-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="5e590-153">使用 WBS 進行專案規劃</span><span class="sxs-lookup"><span data-stu-id="5e590-153">Project planning using WBS</span></span>
- <span data-ttu-id="5e590-154">資源管理</span><span class="sxs-lookup"><span data-stu-id="5e590-154">Resource Management</span></span>
- <span data-ttu-id="5e590-155">時間追蹤</span><span class="sxs-lookup"><span data-stu-id="5e590-155">Time Tracking</span></span>
- <span data-ttu-id="5e590-156">全額費用</span><span class="sxs-lookup"><span data-stu-id="5e590-156">Full Expense</span></span>
- <span data-ttu-id="5e590-157">收據 OCR</span><span class="sxs-lookup"><span data-stu-id="5e590-157">Receipt OCR</span></span>
- <span data-ttu-id="5e590-158">完整發票</span><span class="sxs-lookup"><span data-stu-id="5e590-158">Full Invoicing</span></span>
- <span data-ttu-id="5e590-159">收入認列</span><span class="sxs-lookup"><span data-stu-id="5e590-159">Revenue Recognition</span></span>
- <span data-ttu-id="5e590-160">生產訂單</span><span class="sxs-lookup"><span data-stu-id="5e590-160">Production Orders</span></span>
- <span data-ttu-id="5e590-161">材料支援</span><span class="sxs-lookup"><span data-stu-id="5e590-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="5e590-162">部署步驟</span><span class="sxs-lookup"><span data-stu-id="5e590-162">Deployment steps</span></span>
<span data-ttu-id="5e590-163">使用[部署問卷](https://aka.ms/provisionprojectoperations)來判斷 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="5e590-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="5e590-164">若要進行此部署，請參閱[註冊預覽版訂閱](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json)和[佈建新環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="5e590-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

