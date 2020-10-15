---
title: 部署類型
description: 本主題提供資訊以協助您判斷適合您公司的正確 Project Operations 部署類型。
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948778"
---
# <a name="deployment-types"></a><span data-ttu-id="e7d01-103">部署類型</span><span class="sxs-lookup"><span data-stu-id="e7d01-103">Deployment types</span></span>

<span data-ttu-id="e7d01-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="e7d01-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7d01-105">購買授權之後，請從這裡開始使用[引導式安裝流程](https://aka.ms/provisionprojectoperations)來判斷 Dynamics 365 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="e7d01-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="e7d01-106">完成引導式安裝流程之後，系統會將您導向至正確的管理入口網站，以完成您的安裝。</span><span class="sxs-lookup"><span data-stu-id="e7d01-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="e7d01-107">請參閱下方部署詳細資料，以完成安裝。</span><span class="sxs-lookup"><span data-stu-id="e7d01-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="e7d01-108">使用 Dynamics 365 Project Service Automation 的 Dynamics 現有客戶</span><span class="sxs-lookup"><span data-stu-id="e7d01-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="e7d01-109">Project Operations 包含隨附於 Project Service Automation 的功能。</span><span class="sxs-lookup"><span data-stu-id="e7d01-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="e7d01-110">日後將會為這些客戶發行升級路徑。</span><span class="sxs-lookup"><span data-stu-id="e7d01-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="e7d01-111">使用專案管理與會計的 Dynamics 365 Finance 現有客戶</span><span class="sxs-lookup"><span data-stu-id="e7d01-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="e7d01-112">使用專案管理與會計功能的現有 Finance 客戶可以依照原本方式繼續使用。</span><span class="sxs-lookup"><span data-stu-id="e7d01-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="e7d01-113">請參閱[庫存/生產訂單案例適用的 Project Operations](#pma)。</span><span class="sxs-lookup"><span data-stu-id="e7d01-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="e7d01-114">Project Operations 支援多個部署選項，以符合您的需求。</span><span class="sxs-lookup"><span data-stu-id="e7d01-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="e7d01-115">不論您是新的或現有 Dynamics 365 客戶，Project Operations 都能支援您的需求。</span><span class="sxs-lookup"><span data-stu-id="e7d01-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="e7d01-116">我們的[部署問卷 ](https://aka.ms/provisionprojectoperations)會協助您判斷適當的部署。</span><span class="sxs-lookup"><span data-stu-id="e7d01-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="e7d01-117">結果將引導您前往下列其中一個部署類型：</span><span class="sxs-lookup"><span data-stu-id="e7d01-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="e7d01-118">精簡部署 - 交易至開立預估發票</span><span class="sxs-lookup"><span data-stu-id="e7d01-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="e7d01-119">資源/非庫存案例適用的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="e7d01-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="e7d01-120">庫存/生產訂單案例適用的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="e7d01-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="e7d01-121">Project Operations 透過法律實體層級設定在同一個環境中支援庫存/生產訂單案例以及非庫存/資源型案例。</span><span class="sxs-lookup"><span data-stu-id="e7d01-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="e7d01-122">例如，Contoso 可以利用其美國製造設施 (法律實體 = Contoso Manufacturing United States) 中的庫存/生產訂單功能，以及其在英國的 Contoso 機器人手臂維修設施 (法律實體 = Contoso Robotics United Kingdom) 中的非庫存/資源型功能。</span><span class="sxs-lookup"><span data-stu-id="e7d01-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="e7d01-123"><a name="lite"><a/>精簡部署 - 交易至開立預估發票</span><span class="sxs-lookup"><span data-stu-id="e7d01-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="e7d01-124">精簡部署包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="e7d01-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="e7d01-125">使用 Microsoft Project 網頁版進行專案規劃</span><span class="sxs-lookup"><span data-stu-id="e7d01-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="e7d01-126">多維度定價</span><span class="sxs-lookup"><span data-stu-id="e7d01-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="e7d01-127">統一資源管理</span><span class="sxs-lookup"><span data-stu-id="e7d01-127">Unified Resource Management</span></span>
- <span data-ttu-id="e7d01-128">時間追蹤</span><span class="sxs-lookup"><span data-stu-id="e7d01-128">Time Tracking</span></span>
- <span data-ttu-id="e7d01-129">基本費用</span><span class="sxs-lookup"><span data-stu-id="e7d01-129">Basic Expense</span></span>
- <span data-ttu-id="e7d01-130">發票提案</span><span class="sxs-lookup"><span data-stu-id="e7d01-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="e7d01-131">部署步驟：</span><span class="sxs-lookup"><span data-stu-id="e7d01-131">Deployment steps:</span></span>
<span data-ttu-id="e7d01-132">使用[部署問卷](https://aka.ms/provisionprojectoperations)來判斷 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="e7d01-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="e7d01-133">若要進行此部署，請參閱[註冊預覽版訂閱](lite-preview-subscription-sign-up.md)和[佈建新環境](lite-deployment.md)。</span><span class="sxs-lookup"><span data-stu-id="e7d01-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="e7d01-134"><a name="integrated"><a/>資源/非庫存案例適用的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="e7d01-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="e7d01-135">資源/非庫存案例適用的 Project Operations 包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="e7d01-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="e7d01-136">使用 Microsoft Project 網頁版進行專案規劃</span><span class="sxs-lookup"><span data-stu-id="e7d01-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="e7d01-137">多維度定價</span><span class="sxs-lookup"><span data-stu-id="e7d01-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="e7d01-138">統一資源管理</span><span class="sxs-lookup"><span data-stu-id="e7d01-138">Unified Resource Management</span></span>
- <span data-ttu-id="e7d01-139">時間追蹤</span><span class="sxs-lookup"><span data-stu-id="e7d01-139">Time Tracking</span></span>
- <span data-ttu-id="e7d01-140">基本費用</span><span class="sxs-lookup"><span data-stu-id="e7d01-140">Basic Expense</span></span>
- <span data-ttu-id="e7d01-141">全額費用</span><span class="sxs-lookup"><span data-stu-id="e7d01-141">Full Expense</span></span>
- <span data-ttu-id="e7d01-142">收據 OCR</span><span class="sxs-lookup"><span data-stu-id="e7d01-142">Receipt OCR</span></span>
- <span data-ttu-id="e7d01-143">完整發票</span><span class="sxs-lookup"><span data-stu-id="e7d01-143">Full Invoicing</span></span>
- <span data-ttu-id="e7d01-144">收入認列</span><span class="sxs-lookup"><span data-stu-id="e7d01-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="e7d01-145">部署步驟：</span><span class="sxs-lookup"><span data-stu-id="e7d01-145">Deployment steps:</span></span>
<span data-ttu-id="e7d01-146">使用[部署問卷](https://aka.ms/provisionprojectoperations)來判斷 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="e7d01-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="e7d01-147">若要進行此部署，請參閱[註冊預覽版訂閱](resource-sign-up-preview-subscription.md)和[佈建新環境](resource-provision-new-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="e7d01-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="e7d01-148">庫存/生產訂單案例適用的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="e7d01-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="e7d01-149">使用 WBS 進行專案規劃</span><span class="sxs-lookup"><span data-stu-id="e7d01-149">Project planning using WBS</span></span>
- <span data-ttu-id="e7d01-150">資源管理</span><span class="sxs-lookup"><span data-stu-id="e7d01-150">Resource Management</span></span>
- <span data-ttu-id="e7d01-151">時間追蹤</span><span class="sxs-lookup"><span data-stu-id="e7d01-151">Time Tracking</span></span>
- <span data-ttu-id="e7d01-152">全額費用</span><span class="sxs-lookup"><span data-stu-id="e7d01-152">Full Expense</span></span>
- <span data-ttu-id="e7d01-153">收據 OCR</span><span class="sxs-lookup"><span data-stu-id="e7d01-153">Receipt OCR</span></span>
- <span data-ttu-id="e7d01-154">完整發票</span><span class="sxs-lookup"><span data-stu-id="e7d01-154">Full Invoicing</span></span>
- <span data-ttu-id="e7d01-155">收入認列</span><span class="sxs-lookup"><span data-stu-id="e7d01-155">Revenue Recognition</span></span>
- <span data-ttu-id="e7d01-156">生產訂單</span><span class="sxs-lookup"><span data-stu-id="e7d01-156">Production Orders</span></span>
- <span data-ttu-id="e7d01-157">材料支援</span><span class="sxs-lookup"><span data-stu-id="e7d01-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="e7d01-158">部署步驟：</span><span class="sxs-lookup"><span data-stu-id="e7d01-158">Deployment steps:</span></span>
<span data-ttu-id="e7d01-159">使用[部署問卷](https://aka.ms/provisionprojectoperations)來判斷 Project Operations 的最佳部署模型。</span><span class="sxs-lookup"><span data-stu-id="e7d01-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="e7d01-160">若要進行此部署，請參閱[註冊預覽版訂閱](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json)和[佈建新環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="e7d01-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



