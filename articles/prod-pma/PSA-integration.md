---
title: Project Service Automation 概觀
description: 本主題提供關於 Dynamics 365 Project Service Automation 至 Dynamics 365 Finance 整合解決方案的資訊。
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642443"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="95548-103">Project Service Automation 概觀</span><span class="sxs-lookup"><span data-stu-id="95548-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="95548-104">Project Service Automation 至 Finance 整合解決方案會使用資料整合功能，透過 Common Data Service 跨 Dynamics 365 Finance 與 Dynamics 365 Project Service Automation 的執行個體來同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="95548-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="95548-105">可與資料整合功能搭配使用的整合範本會啟用從 Project Service Automation 到 Finance 的專案、專案合約、專案合約服務內容、專案合約服務內容里程碑、專案工作、費用交易類別、工時估計及費用估計流程。</span><span class="sxs-lookup"><span data-stu-id="95548-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="95548-106">如果您使用的是 7.3.0 版，則必須安裝 KB 4074835。</span><span class="sxs-lookup"><span data-stu-id="95548-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="95548-107">您可以接著整合固定價格專案。</span><span class="sxs-lookup"><span data-stu-id="95548-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="95548-108">如果您使用 7.3.0 版，而且要將費用交易從 Project Service Automation 那裡帶過來，則必須安裝 KB 4345320，才能將這些費用包含在專案發票中。</span><span class="sxs-lookup"><span data-stu-id="95548-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="95548-109">如果使用 8.0 版，您將可以使用專案工作整合、費用交易類別、工時估計、費用估計和功能鎖定。</span><span class="sxs-lookup"><span data-stu-id="95548-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="95548-110">如果使用的是 8.0.1 版或更新版本，就可以同步處理實際值。</span><span class="sxs-lookup"><span data-stu-id="95548-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="95548-111">整合 Project Service Automation 與 Finance 之前，您必須先設定 Project Service Automation 整合參數。</span><span class="sxs-lookup"><span data-stu-id="95548-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="95548-112">如需詳細資訊，請參閱 [Project Service Automation 整合參數](PSA-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="95548-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="95548-113">此整合解決方案可在下列案例中啟用直接同步處理：</span><span class="sxs-lookup"><span data-stu-id="95548-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="95548-114">在 Project Service Automation 中維護專案合約，並將其直接從 Project Service Automation 同步處理至 Finance。</span><span class="sxs-lookup"><span data-stu-id="95548-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="95548-115">在 Project Service Automation 中建立專案，並將其直接從 Project Service Automation 同步處理至 Finance。</span><span class="sxs-lookup"><span data-stu-id="95548-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="95548-116">在 Project Service Automation 中維護合約服務內容，並將其直接從 Project Service Automation 同步處理至 Finance。</span><span class="sxs-lookup"><span data-stu-id="95548-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="95548-117">在 Project Service Automation 中維護合約服務內容里程碑，並將其直接從 Project Service Automation 同步處理至 Finance。</span><span class="sxs-lookup"><span data-stu-id="95548-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="95548-118">在 Project Service Automation 中維護專案工作，並將其直接從 Project Service Automation 同步處理至 Finance。</span><span class="sxs-lookup"><span data-stu-id="95548-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="95548-119">在 Finance 中維護費用交易類別，並將其直接從 Finance 同步處理至 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="95548-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="95548-120">在 Project Service Automation 中建立專案工時估計，並將其直接從 Project Service Automation 同步處理至 Finance。</span><span class="sxs-lookup"><span data-stu-id="95548-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="95548-121">在 Project Service Automation 中建立專案費用估計，並將其直接從 Project Service Automation 同步處理至 Finance。</span><span class="sxs-lookup"><span data-stu-id="95548-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="95548-122">在 Project Service Automation 中建立專案時間、費用及服務費實際值，並在 Project Service Automation 整合日記帳中建立專案交易，讓這些可以在 Finance 中過帳。</span><span class="sxs-lookup"><span data-stu-id="95548-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="95548-123">資料同步</span><span class="sxs-lookup"><span data-stu-id="95548-123">Data synchronization</span></span>

<span data-ttu-id="95548-124">下圖這些顯示如何將資料同步處理為 Project Service Automation 與 Finance 之間整合的一部分。</span><span class="sxs-lookup"><span data-stu-id="95548-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="95548-125">目前並非所有的範本都有提供。</span><span class="sxs-lookup"><span data-stu-id="95548-125">Not all templates are currently available.</span></span> <span data-ttu-id="95548-126">範本完成時，就會發行。</span><span class="sxs-lookup"><span data-stu-id="95548-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="95548-127">[![Project Service Automation 與 Finance 整合](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="95548-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="95548-128">Finance 系統需求</span><span class="sxs-lookup"><span data-stu-id="95548-128">System requirements for Finance</span></span>

<span data-ttu-id="95548-129">若要使用 Project Service Automation 至 Finance 整合解決方案，您必須安裝 Enterprise Edition 7.3 (含平台更新 12) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="95548-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="95548-130">Project Service Automation 系統需求</span><span class="sxs-lookup"><span data-stu-id="95548-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="95548-131">若要使 Project Service Automation 至 Finance 整合解決方案，您必須安裝下列元件：</span><span class="sxs-lookup"><span data-stu-id="95548-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="95548-132">Dynamics 365 Project Service Automation 版本 9.0.0.0 或更新的版本</span><span class="sxs-lookup"><span data-stu-id="95548-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="95548-133">Dynamics 365 Sales 1.14.0.0 版 (v14) 或更新版本的潛在客戶轉現金解決方案</span><span class="sxs-lookup"><span data-stu-id="95548-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="95548-134">Dynamics 365 Project Service Automation 1.0.0.0 版或更新版本的 Project Service Automation 至 Finance 解決方案</span><span class="sxs-lookup"><span data-stu-id="95548-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="95548-135">在 Project Service Automation 執行個體中安裝 Project Service Automation 至 Finance 整合解決方案</span><span class="sxs-lookup"><span data-stu-id="95548-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="95548-136">從 [Microsoft 下載中心](https://www.microsoft.com/download/details.aspx?id=57016)下載 Project Service Automation 至 Finance 整合解決方案，並依照解決方案隨附的指示進行。</span><span class="sxs-lookup"><span data-stu-id="95548-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
