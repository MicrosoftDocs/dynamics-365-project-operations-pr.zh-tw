---
title: 將專案工作直接從 Project Service Automation 同步處理至 Finance and Operations
description: 本主題說明用於將專案工作直接從 Microsoft Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749979"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="14af0-103">將專案工作直接從 Project Service Automation 同步處理至 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14af0-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="14af0-104">本主題說明用於將專案工作直接從 Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。</span><span class="sxs-lookup"><span data-stu-id="14af0-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="14af0-105">專案工作整合、費用交易類別、工時估計、費用估計和功能鎖定可在 8.0 版中使用。</span><span class="sxs-lookup"><span data-stu-id="14af0-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="14af0-106">如果您使用的是 Enterprise Edition 7.3.0，則安裝 KB 4132657 和 KB 4132660 之後，您就可以使用範本來整合專案工作、費用交易類別、工時估計、費用估計與實際值，以及設定功能鎖定。</span><span class="sxs-lookup"><span data-stu-id="14af0-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="14af0-107">如果必須重設會計分配，建議您還要再安裝 KB 4131710。</span><span class="sxs-lookup"><span data-stu-id="14af0-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="14af0-108">實際值整合可在 8.0.1 版或更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="14af0-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="14af0-109">Project Service Automation 至 Finance 的資料流程</span><span class="sxs-lookup"><span data-stu-id="14af0-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="14af0-110">Project Service Automation 至 Finance 整合解決方案會使用資料整合功能，跨 Project Service Automation 與 Finance 的執行個體來同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="14af0-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="14af0-111">可與資料整合功能搭配使用的整合範本會啟用有關專案工作從 Project Service Automation 到 Finance 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="14af0-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="14af0-112">下圖這些顯示如何在 Project Service Automation 與 Finance 之間同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="14af0-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="14af0-113">[![Project Service Automation 與 Finance 整合的資料流程](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="14af0-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="14af0-114">範本與工作</span><span class="sxs-lookup"><span data-stu-id="14af0-114">Template and task</span></span>

<span data-ttu-id="14af0-115">若要存取範本，請在 Microsoft Power Apps 系統管理中心選取**專案**，然後選取右上角的**新增專案**以選取公用範本。</span><span class="sxs-lookup"><span data-stu-id="14af0-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="14af0-116">下列範本與基礎工作會用來將專案工作從 Project Service Automation 同步處理至 Finance。</span><span class="sxs-lookup"><span data-stu-id="14af0-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="14af0-117">**資料整合中範本的名稱：** 專案工作 (PSA 至 Fin 和 Ops)</span><span class="sxs-lookup"><span data-stu-id="14af0-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="14af0-118">**專案中工作的名稱：** 專案工作</span><span class="sxs-lookup"><span data-stu-id="14af0-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="14af0-119">您必須先同步處理專案合約和專案，才能進行專案工作同步處理。</span><span class="sxs-lookup"><span data-stu-id="14af0-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="14af0-120">實體集</span><span class="sxs-lookup"><span data-stu-id="14af0-120">Entity set</span></span>

| <span data-ttu-id="14af0-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="14af0-121">Project Service Automation</span></span> | <span data-ttu-id="14af0-122">Finance</span><span class="sxs-lookup"><span data-stu-id="14af0-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="14af0-123">專案工作</span><span class="sxs-lookup"><span data-stu-id="14af0-123">Project Tasks</span></span>              | <span data-ttu-id="14af0-124">專案工作的整合實體</span><span class="sxs-lookup"><span data-stu-id="14af0-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="14af0-125">實體流程</span><span class="sxs-lookup"><span data-stu-id="14af0-125">Entity flow</span></span>

<span data-ttu-id="14af0-126">專案工作是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案活動。</span><span class="sxs-lookup"><span data-stu-id="14af0-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="14af0-127">先決條件與對應設定</span><span class="sxs-lookup"><span data-stu-id="14af0-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="14af0-128">您必須先同步處理專案合約和專案，才能進行專案工作同步處理。</span><span class="sxs-lookup"><span data-stu-id="14af0-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="14af0-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="14af0-129">Power Query</span></span>

<span data-ttu-id="14af0-130">如果符合此條件，您必須使用 Microsoft Power Query for Excel 來篩選資料：</span><span class="sxs-lookup"><span data-stu-id="14af0-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="14af0-131">您在專案工作中具有資源特定記錄。</span><span class="sxs-lookup"><span data-stu-id="14af0-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="14af0-132">如果您必須使用 Power Query，請遵循以下準則：</span><span class="sxs-lookup"><span data-stu-id="14af0-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="14af0-133">「專案工作 (PSA 至 Fin 和 Ops)」範本具有預設篩選，此篩選將 **IsLineTask** 的篩選設定為 **False**，從專案工作中排除資源特定記錄 。</span><span class="sxs-lookup"><span data-stu-id="14af0-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="14af0-134">如果您自行建立範本，就必須新增此篩選。</span><span class="sxs-lookup"><span data-stu-id="14af0-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="14af0-135">資料整合中的範本對應</span><span class="sxs-lookup"><span data-stu-id="14af0-135">Template mapping in Data integration</span></span>

<span data-ttu-id="14af0-136">下圖顯示資料整合中的範本工作對應範例。</span><span class="sxs-lookup"><span data-stu-id="14af0-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="14af0-137">此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="14af0-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="14af0-138">[![範本對應](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="14af0-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
