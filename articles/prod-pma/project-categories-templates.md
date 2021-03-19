---
title: 同步處理 Finance and Operations 與 Project Service Automation 之間的專案費用類別
description: 本主題說明用於同步處理 Microsoft Dynamics 365 Finance 與 Dynamics 365 Project Service Automation 之間的專案費用類別的範本和基礎工作。
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289629"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="babe5-103">同步處理 Finance and Operations 與 Project Service Automation 之間的專案費用類別</span><span class="sxs-lookup"><span data-stu-id="babe5-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="babe5-104">本主題說明用於同步處理 Dynamics 365 Finance 與 Dynamics 365 Project Service Automation 之間的專案費用類別的範本和基礎工作。</span><span class="sxs-lookup"><span data-stu-id="babe5-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="babe5-105">專案工作整合、費用交易類別、工時估計、費用估計和功能鎖定可在 8.0 版中使用。</span><span class="sxs-lookup"><span data-stu-id="babe5-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="babe5-106">實際值整合可在 8.0.1 版或更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="babe5-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="babe5-107">如果您使用的是 Enterprise Edition 7.3.0，則安裝 KB 4132657 和 KB 4132660 之後，您就可以使用範本來整合專案工作、費用交易類別、工時估計、費用估計與實際值，以及設定功能鎖定。</span><span class="sxs-lookup"><span data-stu-id="babe5-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="babe5-108">如果您必須重設會計分配，建議您還要安裝 KB 4131710。</span><span class="sxs-lookup"><span data-stu-id="babe5-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="babe5-109">Project Service Automation 與 Finance 的資料流程</span><span class="sxs-lookup"><span data-stu-id="babe5-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="babe5-110">Project Service Automation 與 Finance 整合解決方案會使用資料整合功能，跨 Project Service Automation 與 Finance 的執行個體來同步處理。</span><span class="sxs-lookup"><span data-stu-id="babe5-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="babe5-111">可與資料整合功能搭配使用的整合會在 Finance 與 Project Service Automation 之間啟用有關專案費用交易類別的資料流程。</span><span class="sxs-lookup"><span data-stu-id="babe5-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="babe5-112">如果專案費用類別是在 Finance 中主控，則整合流程會先從 Finance 執行到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="babe5-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="babe5-113">專案費用類別的整合識別碼接著會透過從 Project Service Automation 到 Finance 的同步處理進行更新。</span><span class="sxs-lookup"><span data-stu-id="babe5-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="babe5-114">如果專案費用類別是在 Project Service Automation 中主控，則整合流程會先從 Project Service Automation 執行到 Finance。</span><span class="sxs-lookup"><span data-stu-id="babe5-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="babe5-115">專案類別必須已經先在 Finance 中進行設定，才能從 Project Service Automation 進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="babe5-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="babe5-116">從 Finance 同步處理回到 Project Service Automation，然後再次從 Project Service Automation 同步處理到 Finance。</span><span class="sxs-lookup"><span data-stu-id="babe5-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="babe5-117">如此一來，就有助於保證類別已連結，且不會建立任何重複資料。</span><span class="sxs-lookup"><span data-stu-id="babe5-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="babe5-118">專案費用類別通常是在 Finance 中主控。</span><span class="sxs-lookup"><span data-stu-id="babe5-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="babe5-119">不過，如果不是，或如果已經在 Project Service Automation 中建立費用類別，您就必須先使用「專案費用交易類別 (PSA 至 Fin 和 Ops)」範本來同步處理。</span><span class="sxs-lookup"><span data-stu-id="babe5-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="babe5-120">然後使用「專案費用交易類別 (Fin 和 Ops 至 PSA)」範本進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="babe5-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="babe5-121">您應該再從 Project Service Automation 執行同步處理到 Finance 一次。</span><span class="sxs-lookup"><span data-stu-id="babe5-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="babe5-122">如果先從 Project Service Automation 進行同步處理，則必須在 Finance 中符合下列需求，才能執行同步處理：</span><span class="sxs-lookup"><span data-stu-id="babe5-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="babe5-123">符合 Project Service Automation 中所設定專案類別的共用類別必須存在，且必須已針對 **專案** 及 **費用** 啟用。</span><span class="sxs-lookup"><span data-stu-id="babe5-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="babe5-124">對於每個必須與之整合的 Finance 法律實體，必須有下列專案類別存在：</span><span class="sxs-lookup"><span data-stu-id="babe5-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="babe5-125">**專案類別** 存在。</span><span class="sxs-lookup"><span data-stu-id="babe5-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="babe5-126">**在費用中使用** 已啟用。</span><span class="sxs-lookup"><span data-stu-id="babe5-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="babe5-127">**在日記帳中啟動** 已啟用。</span><span class="sxs-lookup"><span data-stu-id="babe5-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="babe5-128">**交易類型** 設定為 **費用**。</span><span class="sxs-lookup"><span data-stu-id="babe5-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="babe5-129">下圖這些顯示如何在 Project Service Automation 與 Finance 之間同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="babe5-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="babe5-130">[![Project Service Automation 與 Finance 整合的資料流程](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="babe5-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="babe5-131">從 Finance 至 Project Service Automation 的專案費用類別同步處理</span><span class="sxs-lookup"><span data-stu-id="babe5-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="babe5-132">範本與工作</span><span class="sxs-lookup"><span data-stu-id="babe5-132">Template and task</span></span>

<span data-ttu-id="babe5-133">若要存取範本，請在 Microsoft Power Apps 系統管理中心選取 **專案**，然後選取右上角的 **新增專案** 以選取公用範本。</span><span class="sxs-lookup"><span data-stu-id="babe5-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="babe5-134">下列範本與基礎工作會用來將專案費用類別從 Finance 同步處理至 Project Service Automation：</span><span class="sxs-lookup"><span data-stu-id="babe5-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="babe5-135">**資料整合中範本的名稱：** 專案費用交易類別 (Fin 和 Ops 至 PSA)</span><span class="sxs-lookup"><span data-stu-id="babe5-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="babe5-136">**專案中工作的名稱：** 將類別同步至 PSA</span><span class="sxs-lookup"><span data-stu-id="babe5-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="babe5-137">實體集</span><span class="sxs-lookup"><span data-stu-id="babe5-137">Entity set</span></span>

| <span data-ttu-id="babe5-138">財務</span><span class="sxs-lookup"><span data-stu-id="babe5-138">Finance</span></span>                           | <span data-ttu-id="babe5-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="babe5-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="babe5-140">類別至的整合實體</span><span class="sxs-lookup"><span data-stu-id="babe5-140">Integration entity for categories</span></span> | <span data-ttu-id="babe5-141">交易類別</span><span class="sxs-lookup"><span data-stu-id="babe5-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="babe5-142">實體流程</span><span class="sxs-lookup"><span data-stu-id="babe5-142">Entity flow</span></span>

<span data-ttu-id="babe5-143">專案費用類別是在 FinanceFinance 中進行管理，並同步處理至 Project Service Automation 做為交易類別。</span><span class="sxs-lookup"><span data-stu-id="babe5-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="babe5-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="babe5-144">Power Query</span></span>

<span data-ttu-id="babe5-145">同步處理至 Project Service Automation 時，您必須使用 Microsoft Power Query for Excel 來設定交易類別的帳單類型。</span><span class="sxs-lookup"><span data-stu-id="babe5-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="babe5-146">「專案費用交易類別 (Fin 和 Ops 至 PSA)」範本會提供預設欄和對應。</span><span class="sxs-lookup"><span data-stu-id="babe5-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="babe5-147">如果您自行建立範本，就必須在 Power Query 中新增條件欄。</span><span class="sxs-lookup"><span data-stu-id="babe5-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="babe5-148">依照下列步驟執行。</span><span class="sxs-lookup"><span data-stu-id="babe5-148">Follow these steps.</span></span>

1. <span data-ttu-id="babe5-149">按一下箭頭以開啟「專案費用交易類別 (Fin 和 Ops 至 PSA)」範本中專案費用類別工作的對應。</span><span class="sxs-lookup"><span data-stu-id="babe5-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="babe5-150">按一下 **進階查詢及篩選** 連結，以開啟 Power Query。</span><span class="sxs-lookup"><span data-stu-id="babe5-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="babe5-151">選取 **新增條件欄**。</span><span class="sxs-lookup"><span data-stu-id="babe5-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="babe5-152">輸入新欄的名稱，例如 **BillingType**。</span><span class="sxs-lookup"><span data-stu-id="babe5-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="babe5-153">輸入下列條件：**如果 CATEGORYID 不等於 Null 則為 19235001，否則為 Null**。</span><span class="sxs-lookup"><span data-stu-id="babe5-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="babe5-154">按一下欄中的 **確定**。</span><span class="sxs-lookup"><span data-stu-id="babe5-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="babe5-155">請務必在對應頁面上對應這個新欄。</span><span class="sxs-lookup"><span data-stu-id="babe5-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="babe5-156">下圖顯示資料整合中的範本工作對應範例。</span><span class="sxs-lookup"><span data-stu-id="babe5-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="babe5-157">此對應顯示會從 Finance 同步處理至 Project Service Automation 的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="babe5-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="babe5-158">[![專案費用類別至 Project Service Automation 範本對應](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="babe5-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="babe5-159">從 Project Service Automation 至 Finance 的專案費用類別同步處理</span><span class="sxs-lookup"><span data-stu-id="babe5-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="babe5-160">範本與工作</span><span class="sxs-lookup"><span data-stu-id="babe5-160">Template and task</span></span>

<span data-ttu-id="babe5-161">下列範本與基礎工作會用來將專案費用類別從 Project Service Automation 同步處理至 Finance：</span><span class="sxs-lookup"><span data-stu-id="babe5-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="babe5-162">**資料整合中範本的名稱：** 專案費用交易類別 (PSA 至 Fin 和 Ops)</span><span class="sxs-lookup"><span data-stu-id="babe5-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="babe5-163">**專案中工作的名稱：** 將類別同步至 Fin Ops</span><span class="sxs-lookup"><span data-stu-id="babe5-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="babe5-164">實體集</span><span class="sxs-lookup"><span data-stu-id="babe5-164">Entity set</span></span>

| <span data-ttu-id="babe5-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="babe5-165">Project Service Automation</span></span> | <span data-ttu-id="babe5-166">財務</span><span class="sxs-lookup"><span data-stu-id="babe5-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="babe5-167">交易類別</span><span class="sxs-lookup"><span data-stu-id="babe5-167">Transaction categories</span></span>     | <span data-ttu-id="babe5-168">類別至的整合實體</span><span class="sxs-lookup"><span data-stu-id="babe5-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="babe5-169">實體流程</span><span class="sxs-lookup"><span data-stu-id="babe5-169">Entity flow</span></span>

<span data-ttu-id="babe5-170">專案費用類別是在 FinanceFinance 中進行管理，並同步處理至 Project Service Automation 做為交易類別。</span><span class="sxs-lookup"><span data-stu-id="babe5-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="babe5-171">同步處理回到 Finance 會將 Finance 中的專案類別更新為 Project Service Automation 中的整合識別碼。</span><span class="sxs-lookup"><span data-stu-id="babe5-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="babe5-172">資料整合中的範本對應</span><span class="sxs-lookup"><span data-stu-id="babe5-172">Template mapping in Data integration</span></span>

<span data-ttu-id="babe5-173">下圖顯示資料整合中的範本工作對應範例。</span><span class="sxs-lookup"><span data-stu-id="babe5-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="babe5-174">此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="babe5-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="babe5-175">[![Project Service Automation 至 Finance 範本對應](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="babe5-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]