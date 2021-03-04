---
title: 將專案合約和專案直接從 Project Service Automation 同步處理至 Finance
description: 本主題說明用於將專案合約和專案直接從 Microsoft Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 1a470fd86ceccd7b6058da6972399a6d6be2a991
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764809"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a><span data-ttu-id="646af-103">將專案合約和專案直接從 Project Service Automation 同步處理至 Finance</span><span class="sxs-lookup"><span data-stu-id="646af-103">Synchronize project contracts and projects directly from Project Service Automation to Finance</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="646af-104">本主題說明用於將專案合約和專案直接從 Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。</span><span class="sxs-lookup"><span data-stu-id="646af-104">This topic describes the template and underlying tasks that are used to synchronize project contracts and projects directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE] 
> <span data-ttu-id="646af-105">如果您使用的是 Enterprise Edition 7.3.0，則必須安裝 KB 4074835。</span><span class="sxs-lookup"><span data-stu-id="646af-105">If you're using Enterprise edition 7.3.0, you must install KB 4074835.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="646af-106">Project Service Automation 至 Finance 的資料流程</span><span class="sxs-lookup"><span data-stu-id="646af-106">Data flow for Project Service Automation to Finance</span></span>

> [!NOTE]
> <span data-ttu-id="646af-107">使用 Project Service Automation to Finance 整合解決方案之前，您必須先熟悉 Dynamics 365 資料整合功能。</span><span class="sxs-lookup"><span data-stu-id="646af-107">Before you can use the Project Service Automation to Finance integration solution, you should be familiar with the Dynamics 365 Data integration feature.</span></span>

<span data-ttu-id="646af-108">Project Service Automation 至 Finance 整合解決方案會使用資料整合功能，跨 Project Service Automation 與 Finance 的執行個體來同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="646af-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="646af-109">可與資料整合功能搭配使用的整合範本會啟用有關從 Project Service Automation 到 Finance 的專案合約、專案、專案合約服務內容及專案合約服務內容里程碑的資料流程。</span><span class="sxs-lookup"><span data-stu-id="646af-109">The integration template that is available with the Data integration feature enables the flow of data about project contracts, projects, project contract lines, and project contract line milestones from Project Service Automation to Finance.</span></span>

<span data-ttu-id="646af-110">下圖這些顯示如何在 Project Service Automation 與 Finance 之間同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="646af-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="646af-111">[![Project Service Automation 與 Finance 整合的資料流程](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)</span><span class="sxs-lookup"><span data-stu-id="646af-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="646af-112">範本與工作</span><span class="sxs-lookup"><span data-stu-id="646af-112">Templates and tasks</span></span>

<span data-ttu-id="646af-113">若要存取可用範本，請在 Microsoft Power Apps 系統管理中心選取 **專案**，然後選取右上角的 **新增專案** 以選取公用範本。</span><span class="sxs-lookup"><span data-stu-id="646af-113">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="646af-114">下列範本與基礎工作會用來將專案合約和專案從 Project Service Automation 同步處理至 Finance：</span><span class="sxs-lookup"><span data-stu-id="646af-114">The following templates and underlying tasks are used to synchronize project contracts and projects from Project Service Automation to Finance:</span></span>

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a><span data-ttu-id="646af-115">與 Dynamics 365 Project Service Automation v2.x 整合</span><span class="sxs-lookup"><span data-stu-id="646af-115">Integrating with Dynamics 365 Project Service Automation v2.x</span></span>
- <span data-ttu-id="646af-116">**資料整合中的範本名稱：** 專案和合約 (Project Service Automation 至 Finance)</span><span class="sxs-lookup"><span data-stu-id="646af-116">**Name of the template in Data integration:** Projects and contracts (Project Service Automation to Finance)</span></span>
- <span data-ttu-id="646af-117">**專案中工作的名稱：**</span><span class="sxs-lookup"><span data-stu-id="646af-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="646af-118">專案合約 Project Service Automation 至 Finance</span><span class="sxs-lookup"><span data-stu-id="646af-118">Project contracts Project Service Automation to Finance</span></span>
    - <span data-ttu-id="646af-119">專案 Project Service Automation 至 Finance</span><span class="sxs-lookup"><span data-stu-id="646af-119">Projects Project Service Automation to Finance</span></span>
    - <span data-ttu-id="646af-120">專案合約服務內容 Project Service Automation 至 Finance</span><span class="sxs-lookup"><span data-stu-id="646af-120">Project contract lines Project Service Automation to Finance</span></span>
    - <span data-ttu-id="646af-121">專案合約服務內容里程碑 Project Service Automation 至 Finance</span><span class="sxs-lookup"><span data-stu-id="646af-121">Project contract line milestones Project Service Automation to Finance</span></span>
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a><span data-ttu-id="646af-122">與 Dynamics 365 Project Service Automation v3.x 整合</span><span class="sxs-lookup"><span data-stu-id="646af-122">Integrating with Dynamics 365 Project Service Automation v3.x</span></span>
<span data-ttu-id="646af-123">Project Service Automation 中發生中繼資料變更，這會影響專案合約服務內容里程碑範本，並需要使用 v2 版本的範本，才能將 Project Service Automation v3.x 與 Dynamics 365 整合。</span><span class="sxs-lookup"><span data-stu-id="646af-123">There is a schema change in Project Service Automation that impacts the Project contract line milestone template and use of the v2 version of the template is required to integrate Project Service Automation v3.x with Dynamics 365.</span></span>

- <span data-ttu-id="646af-124">**資料整合中的範本名稱：** 專案和合約 (Project Service Automation 3.x 至 Finance) - v2</span><span class="sxs-lookup"><span data-stu-id="646af-124">**Name of the template in Data integration:** Projects and Contracts (Project Service Automation 3.x to Finance) - v2</span></span>
- <span data-ttu-id="646af-125">**專案中工作的名稱：**</span><span class="sxs-lookup"><span data-stu-id="646af-125">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="646af-126">專案合約 Project Service Automation 至 Finance</span><span class="sxs-lookup"><span data-stu-id="646af-126">Project contracts Project Service Automation to Finance</span></span>
    - <span data-ttu-id="646af-127">專案 Project Service Automation 至 Finance</span><span class="sxs-lookup"><span data-stu-id="646af-127">Projects Project Service Automation to Finance</span></span>
    - <span data-ttu-id="646af-128">專案合約服務內容 Project Service Automation 至 Finance</span><span class="sxs-lookup"><span data-stu-id="646af-128">Project contract lines Project Service Automation to Finance</span></span>
    - <span data-ttu-id="646af-129">專案合約服務內容里程碑 Project Service Automation 至 Finance</span><span class="sxs-lookup"><span data-stu-id="646af-129">Project contract line milestones Project Service Automation to Finance</span></span>

<span data-ttu-id="646af-130">您必須先同步處理帳戶，才能進行專案合約和專案同步處理。</span><span class="sxs-lookup"><span data-stu-id="646af-130">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>

## <a name="entity-set"></a><span data-ttu-id="646af-131">實體集</span><span class="sxs-lookup"><span data-stu-id="646af-131">Entity set</span></span>

| <span data-ttu-id="646af-132">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="646af-132">Project Service Automation</span></span>       | <span data-ttu-id="646af-133">財務</span><span class="sxs-lookup"><span data-stu-id="646af-133">Finance</span></span>                                                |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="646af-134">訂單</span><span class="sxs-lookup"><span data-stu-id="646af-134">Orders</span></span>                           | <span data-ttu-id="646af-135">專案合約的整合實體</span><span class="sxs-lookup"><span data-stu-id="646af-135">Integration entity for project contract</span></span>                |
| <span data-ttu-id="646af-136">專案</span><span class="sxs-lookup"><span data-stu-id="646af-136">Projects</span></span>                         | <span data-ttu-id="646af-137">專案的整合實體</span><span class="sxs-lookup"><span data-stu-id="646af-137">Integration entity for project</span></span>                         |
| <span data-ttu-id="646af-138">訂單明細</span><span class="sxs-lookup"><span data-stu-id="646af-138">Order lines</span></span>                      | <span data-ttu-id="646af-139">專案合約服務內容的整合實體</span><span class="sxs-lookup"><span data-stu-id="646af-139">Integration entity for project contract line</span></span>           |
| <span data-ttu-id="646af-140">專案合約服務內容里程碑</span><span class="sxs-lookup"><span data-stu-id="646af-140">Project contract line milestones</span></span> | <span data-ttu-id="646af-141">專案合約服務內容里程碑的整合實體</span><span class="sxs-lookup"><span data-stu-id="646af-141">Integration entity for project contract line milestone</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="646af-142">實體流程</span><span class="sxs-lookup"><span data-stu-id="646af-142">Entity flow</span></span>

<span data-ttu-id="646af-143">專案合約是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案合約。</span><span class="sxs-lookup"><span data-stu-id="646af-143">Project contracts are managed in Project Service Automation, and they are synchronized to Finance as project contracts.</span></span> <span data-ttu-id="646af-144">在整合範本中，您可以為專案合約設定 Finance 中的整合來源。</span><span class="sxs-lookup"><span data-stu-id="646af-144">As part of the integration template, you can set the integration source in Finance for the project contract.</span></span>

<span data-ttu-id="646af-145">時間和材料專案以及固定價格專案是在 Project Service Automation 中進行管理，並當做物件同步處理至 Finance。</span><span class="sxs-lookup"><span data-stu-id="646af-145">Time and material and fixed-price projects are managed in Project Service Automation and synchronized to Finance as projects.</span></span> <span data-ttu-id="646af-146">在範本整合過程中，您可以在 Finance 中設定專案的整合來源。</span><span class="sxs-lookup"><span data-stu-id="646af-146">As part of the template integration, you can set the integration source for the project in Finance.</span></span> <span data-ttu-id="646af-147">目前僅支援時間和材料專案以及固定價格專案。</span><span class="sxs-lookup"><span data-stu-id="646af-147">Currently, only time and material and fixed-price projects are supported.</span></span>


<span data-ttu-id="646af-148">專案合約服務內容是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案合約帳單規則。</span><span class="sxs-lookup"><span data-stu-id="646af-148">Project contract lines are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rules.</span></span> <span data-ttu-id="646af-149">如果帳務方式與預設專案類型不同，則同步處理會更新合約服務內容專案與專案群組的專案類型。</span><span class="sxs-lookup"><span data-stu-id="646af-149">If the billing method differs from the default project type, the synchronization updates the project type for the contract line project and project group.</span></span>

<span data-ttu-id="646af-150">專案合約服務內容里程碑是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案合約帳單規則里程碑。</span><span class="sxs-lookup"><span data-stu-id="646af-150">Project contract line milestones are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rule milestones.</span></span>

## <a name="project-service-automation-to-finance-integration-solution"></a><span data-ttu-id="646af-151">Project Service Automation 至 Finance 整合解決方案</span><span class="sxs-lookup"><span data-stu-id="646af-151">Project Service Automation to Finance integration solution</span></span>

<span data-ttu-id="646af-152">**專案合約識別碼** 欄位可在 **專案合約** 頁面上找到。</span><span class="sxs-lookup"><span data-stu-id="646af-152">The **Project contract ID** field is available on the **Project contracts** page.</span></span> <span data-ttu-id="646af-153">此欄位已設定為用來支援整合的自然對唯一索引鍵。</span><span class="sxs-lookup"><span data-stu-id="646af-153">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="646af-154">建立新的專案合約時，如果還沒有 **專案合約識別碼** 值，就會使用數字序列自動產生此值。</span><span class="sxs-lookup"><span data-stu-id="646af-154">When a new project contract is created, if a **Project contract ID** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="646af-155">此值由後面跟著一個遞增數字序列的 **ORD** 以及再接著的六字元尾碼所組成。</span><span class="sxs-lookup"><span data-stu-id="646af-155">The value consists of **ORD** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="646af-156">以下是範例：**ORD-01022-Z4M9Q0**。</span><span class="sxs-lookup"><span data-stu-id="646af-156">Here is an example: **ORD-01022-Z4M9Q0**.</span></span>

<span data-ttu-id="646af-157">**專案編號** 欄位可在 **專案** 頁面上找到。</span><span class="sxs-lookup"><span data-stu-id="646af-157">The **Project Number** field is available on the **Projects** page.</span></span> <span data-ttu-id="646af-158">此欄位已設定為用來支援整合的自然對唯一索引鍵。</span><span class="sxs-lookup"><span data-stu-id="646af-158">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="646af-159">建立新的專案合約時，如果還沒有 **專案編號** 值，就會使用數字序列自動產生此值。</span><span class="sxs-lookup"><span data-stu-id="646af-159">When a new project is created, if a **Project Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="646af-160">此值由後面跟著一個遞增數字序列的 **PRJ** 以及再接著的六字元尾碼所組成。</span><span class="sxs-lookup"><span data-stu-id="646af-160">The value consists of **PRJ** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="646af-161">以下是範例：**PRJ-01049-CCNID0**。</span><span class="sxs-lookup"><span data-stu-id="646af-161">Here is an example: **PRJ-01049-CCNID0**.</span></span>

<span data-ttu-id="646af-162">套用 Project Service Automation 至 Finance 整合解決方案時，升級指令碼會在 Project Service Automation 中設定現有專案合約的 **專案合約識別碼** 以及現有專案的 **專案編號**。</span><span class="sxs-lookup"><span data-stu-id="646af-162">When the Project Service Automation to Finance integration solution is applied, an upgrade script sets the **Project contract ID** field for existing project contracts and the **Project Number** field for existing projects in Project Service Automation.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="646af-163">先決條件與對應設定</span><span class="sxs-lookup"><span data-stu-id="646af-163">Prerequisites and mapping setup</span></span>

- <span data-ttu-id="646af-164">您必須先同步處理帳戶，才能進行專案合約和專案同步處理。</span><span class="sxs-lookup"><span data-stu-id="646af-164">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>
- <span data-ttu-id="646af-165">在您的連接集中，新增 **msdyn\_organizationalunits** 至 **msdyn\_name \[名稱\]** 的整合索引鍵欄位對應。</span><span class="sxs-lookup"><span data-stu-id="646af-165">In your connection set, add an integration key field mapping for **msdyn\_organizationalunits** to **msdyn\_name \[Name\]**.</span></span> <span data-ttu-id="646af-166">您可能需要先將專案新增至連接集。</span><span class="sxs-lookup"><span data-stu-id="646af-166">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="646af-167">如需詳細資訊，請參閱[將資料整合至應用程式適用的 Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="646af-167">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="646af-168">在您的連接集中，新增 **msdyn\_projects** 至 **msdynce\_projectnumber \[專案編號\]** 的整合索引鍵欄位對應。</span><span class="sxs-lookup"><span data-stu-id="646af-168">In your connection set, add an integration key field mapping for **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span></span> <span data-ttu-id="646af-169">您可能需要先將專案新增至連接集。</span><span class="sxs-lookup"><span data-stu-id="646af-169">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="646af-170">如需詳細資訊，請參閱[將資料整合至應用程式適用的 Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="646af-170">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="646af-171">專案合約和專案的 **SourceDataID** 可以更新為不同的值，或從對應中移除。</span><span class="sxs-lookup"><span data-stu-id="646af-171">**SourceDataID** for project contracts and projects can be updated to a different value or removed from the mapping.</span></span> <span data-ttu-id="646af-172">預設範本值是 **Project Service Automation**。</span><span class="sxs-lookup"><span data-stu-id="646af-172">The default template value is **Project Service Automation**.</span></span>
- <span data-ttu-id="646af-173">**PaymentTerms** 對應必須更新，以便在 Finance 中反映有效的付款條件。</span><span class="sxs-lookup"><span data-stu-id="646af-173">The **PaymentTerms** mapping must be updated so that it reflects valid terms of payment in Finance.</span></span> <span data-ttu-id="646af-174">您也可以從專案工作移除對應。</span><span class="sxs-lookup"><span data-stu-id="646af-174">You can also remove the mapping from the project task.</span></span> <span data-ttu-id="646af-175">預設值對應具有示範資料的預設值。</span><span class="sxs-lookup"><span data-stu-id="646af-175">The default value map has default values for demo data.</span></span> <span data-ttu-id="646af-176">下表顯示 Project Service Automation 中的值。</span><span class="sxs-lookup"><span data-stu-id="646af-176">The following table shows the values in Project Service Automation.</span></span>

    | <span data-ttu-id="646af-177">值</span><span class="sxs-lookup"><span data-stu-id="646af-177">Value</span></span> | <span data-ttu-id="646af-178">描述</span><span class="sxs-lookup"><span data-stu-id="646af-178">Description</span></span>   |
    |-------|---------------|
    | <span data-ttu-id="646af-179">7</span><span class="sxs-lookup"><span data-stu-id="646af-179">1</span></span>     | <span data-ttu-id="646af-180">30 天內付款</span><span class="sxs-lookup"><span data-stu-id="646af-180">Net 30</span></span>        |
    | <span data-ttu-id="646af-181">2</span><span class="sxs-lookup"><span data-stu-id="646af-181">2</span></span>     | <span data-ttu-id="646af-182">10 天內付款折扣 2%，30 天內付款</span><span class="sxs-lookup"><span data-stu-id="646af-182">2% 10, Net 30</span></span> |
    | <span data-ttu-id="646af-183">3</span><span class="sxs-lookup"><span data-stu-id="646af-183">3</span></span>     | <span data-ttu-id="646af-184">45 天內付款</span><span class="sxs-lookup"><span data-stu-id="646af-184">Net 45</span></span>        |
    | <span data-ttu-id="646af-185">4</span><span class="sxs-lookup"><span data-stu-id="646af-185">4</span></span>     | <span data-ttu-id="646af-186">60 天內付款</span><span class="sxs-lookup"><span data-stu-id="646af-186">Net 60</span></span>        |

## <a name="power-query"></a><span data-ttu-id="646af-187">Power Query</span><span class="sxs-lookup"><span data-stu-id="646af-187">Power Query</span></span>

<span data-ttu-id="646af-188">如果符合下列條件，請使用 Microsoft Power Query for Excel 來篩選資料：</span><span class="sxs-lookup"><span data-stu-id="646af-188">Use Microsoft Power Query for Excel to filter data if the following conditions are met:</span></span>

- <span data-ttu-id="646af-189">您在 Dynamics 365 Sales 中有銷售訂單。</span><span class="sxs-lookup"><span data-stu-id="646af-189">You have sales orders in Dynamics 365 Sales.</span></span>
- <span data-ttu-id="646af-190">您在 Project Service Automation 中有多個組織單位，而且這些組織單位將會對應至 Finance 中的多個法律實體。</span><span class="sxs-lookup"><span data-stu-id="646af-190">You have multiple organizational units in Project Service Automation, and these organizational units will be mapped to multiple legal entities in Finance.</span></span>

<span data-ttu-id="646af-191">如果您必須使用 Power Query，請遵循下列準則：</span><span class="sxs-lookup"><span data-stu-id="646af-191">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="646af-192">「專案與合約 (PSA 至 Fin 和 Ops)」範本有一個只會包含類型為 **工作項目 (msdyn\_ordertype = 192350001)** 之銷售訂單的預設篩選。</span><span class="sxs-lookup"><span data-stu-id="646af-192">The Projects and contracts (PSA to Fin and Ops) template has a default filter that includes only sales orders of the **Work item (msdyn\_ordertype = 192350001)** type.</span></span> <span data-ttu-id="646af-193">此篩選有助於保證不會為 Finance 中的銷售訂單建立專案合約。</span><span class="sxs-lookup"><span data-stu-id="646af-193">This filter helps guarantee that project contracts aren't created for sales orders in Finance.</span></span> <span data-ttu-id="646af-194">如果您自行建立範本，就必須新增此篩選。</span><span class="sxs-lookup"><span data-stu-id="646af-194">If you create your own template, you must add this filter.</span></span>
- <span data-ttu-id="646af-195">建立只包含合約組織的 Power Query 篩選，這些組織應同步處理至整合關係組的法律實體。</span><span class="sxs-lookup"><span data-stu-id="646af-195">Create a Power Query filter that includes only the contract organizations that should be synchronized to the legal entity of the integration connection set.</span></span> <span data-ttu-id="646af-196">例如，您與合約組織單位 Contoso US 之間的專案合約，必須同步處理至 USSI 法律實體，但是您與合約組織單位 Contoso Global 之後專案合約則應同步處理至 USMF 法律實體。</span><span class="sxs-lookup"><span data-stu-id="646af-196">For example, project contracts that you have with the contract organizational unit of Contoso US should be synchronized to the USSI legal entity, but project contracts that you have with the contract organizational unit of Contoso Global should be synchronized to the USMF legal entity.</span></span> <span data-ttu-id="646af-197">如果您未將此篩選新增至工作對應，則會將所有專案合約都同步處理至針對連接集所定義的法律實體，而不考慮合約組織單位。</span><span class="sxs-lookup"><span data-stu-id="646af-197">If you don't add this filter to your task mapping, all project contracts will be synchronized to the legal entity that is defined for the connection set, regardless of the contract organizational unit.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="646af-198">資料整合中的範本對應</span><span class="sxs-lookup"><span data-stu-id="646af-198">Template mapping in Data integration</span></span>

> [!NOTE] 
> <span data-ttu-id="646af-199">**CustomerReference**、**AddressCity**、**AddressCountryRegionID**、**AddressDescription**、**AddressLine1**、**AddressLine2**、**AddressState** 和 **AddressZipCode** 欄位不會包含在專案合約的預設對應中。</span><span class="sxs-lookup"><span data-stu-id="646af-199">The **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, and **AddressZipCode** fields aren't included in the default mapping for project contracts.</span></span> <span data-ttu-id="646af-200">如果專案合約需要同步處理此資料，您可以新增對應。</span><span class="sxs-lookup"><span data-stu-id="646af-200">You can add the mappings if you require that this data be synchronized for project contracts.</span></span>
>
> <span data-ttu-id="646af-201">**描述**、**ParentID**、**ProjectGroup**、**ProjectManagerPersonnelNumber** 和 **ProjectType** 欄位不會包含在專案的預設對應中。</span><span class="sxs-lookup"><span data-stu-id="646af-201">The **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fields aren't included in the default mapping for projects.</span></span> <span data-ttu-id="646af-202">如果專案需要同步處理此資料，您可以新增對應。</span><span class="sxs-lookup"><span data-stu-id="646af-202">You can add the mappings if you require that this data be synchronized for projects.</span></span>

<span data-ttu-id="646af-203">下圖顯示資料整合中的範本工作對應範例。</span><span class="sxs-lookup"><span data-stu-id="646af-203">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="646af-204">此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="646af-204">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="646af-205">[![專案合約範本對應](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="646af-205">[![Project contract template mapping](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span></span>

<span data-ttu-id="646af-206">[![專案範本對應](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="646af-206">[![Project template mapping](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span></span>

<span data-ttu-id="646af-207">[![專案合約服務內容範本對應](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="646af-207">[![Project contract lines template mapping](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span></span>

<span data-ttu-id="646af-208">[![專案合約服務內容里程碑範本對應](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="646af-208">[![Project contract line milestone template mapping](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span></span>

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a><span data-ttu-id="646af-209">「專案與合約 (PSA 3.x 至 Dynamics) - v2」範本中的專案合約服務內容里程碑：</span><span class="sxs-lookup"><span data-stu-id="646af-209">Project contract line milestone mapping in the Projects and Contracts (PSA 3.x to Dynamics) - v2 template:</span></span>

<span data-ttu-id="646af-210">[![專案合約服務內容里程碑與版本 2 範本的對應](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span><span class="sxs-lookup"><span data-stu-id="646af-210">[![Project contract line milestone mapping with version two template](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span></span>
