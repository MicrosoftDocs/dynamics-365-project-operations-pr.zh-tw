---
title: 將專案實際值從 Project Service Automation 直接同步處理至專案整合日記帳，以便在 Finance and Operations 中進行過帳
description: 本主題說明用於將專案實際值直接從 Microsoft Dynamics 365 Project Service Automation 同步處理至 Finance and Operations 的範本與基礎工作。
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073128"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a><span data-ttu-id="13791-103">將專案實際值從 Project Service Automation 直接同步處理至專案整合日記帳，以便在 Finance and Operations 中進行過帳</span><span class="sxs-lookup"><span data-stu-id="13791-103">Synchronize project actuals directly from Project Service Automation to the project integration journal for posting in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="13791-104">本主題說明用於將專案實際值直接從 Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。</span><span class="sxs-lookup"><span data-stu-id="13791-104">This topic describes the templates and underlying tasks that are used to synchronize project actuals directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

<span data-ttu-id="13791-105">範本會將交易從 Project Service Automation 同步處理至 Finance 中的暫存表格。</span><span class="sxs-lookup"><span data-stu-id="13791-105">The template synchronizes transactions from Project Service Automation into a staging table in Finance.</span></span> <span data-ttu-id="13791-106">完成同步處理後，您 **必須** 將資料從暫存表格匯入至整合日記帳中。</span><span class="sxs-lookup"><span data-stu-id="13791-106">After synchronization is completed, you **must** import the data from the staging table into the integration journal.</span></span>

> [!NOTE]
> - <span data-ttu-id="13791-107">專案實際值整合是在 8.0.1 版中開始提供。</span><span class="sxs-lookup"><span data-stu-id="13791-107">Project actuals integration is available starting in version 8.0.1.</span></span>
> - <span data-ttu-id="13791-108">如果您在安裝 KB 4132657 和 KB 4132660 之後使用 Enterprise Edition 7.3.0，則可以使用範本來整合專案工作、費用交易類別、工時估計、費用估計值和實際值，以及設定功能鎖定。</span><span class="sxs-lookup"><span data-stu-id="13791-108">If you're using Enterprise edition 7.3.0 after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="13791-109">如果您必須重設會計分配，建議您還要安裝 KB 4131710。</span><span class="sxs-lookup"><span data-stu-id="13791-109">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="13791-110">如果您使用 7.3.0 版，而且要將費用交易從 Project Service Automation 那裡帶過來，則必須安裝 KB 4345320，才能將這些費用包含在專案發票中。</span><span class="sxs-lookup"><span data-stu-id="13791-110">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="13791-111">如果您在 Project Service Automation 中輸入時間或費用交易的銷售稅額，則必須安裝 Project Service Automation 更新 7。</span><span class="sxs-lookup"><span data-stu-id="13791-111">If you're entering sales tax amounts on time or expense transactions in Project Service Automation, you must install Project Service Automation Update 7.</span></span> <span data-ttu-id="13791-112">否則，稅金實際值不會連結至相關的時間或費用實際值，而這些實際值不會同步處理至 Finance。</span><span class="sxs-lookup"><span data-stu-id="13791-112">Otherwise, the tax actuals won't be linked to the associated time or expense actuals, and they won't be synchronized to Finance.</span></span> <span data-ttu-id="13791-113">如需詳細資訊，請連絡支援人員。</span><span class="sxs-lookup"><span data-stu-id="13791-113">For more information, contact Support.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="13791-114">Project Service Automation 至 Finance 的資料流程</span><span class="sxs-lookup"><span data-stu-id="13791-114">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="13791-115">Project Service Automation 至 Finance 整合解決方案會使用資料整合功能，跨 Project Service Automation 與 Finance 的執行個體來同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="13791-115">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="13791-116">可與資料整合功能搭配使用的整合範本會啟用有關專案實際值從 Project Service Automation 到 Finance 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="13791-116">The integration templates that are available with the Data integration feature enable the flow of data about project actuals from Project Service Automation to Finance.</span></span>

<span data-ttu-id="13791-117">下圖這些顯示如何在 Project Service Automation 與 Finance 之間同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="13791-117">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="13791-118">[![Project Service Automation 與 Finance and Operations 整合的資料流程](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span><span class="sxs-lookup"><span data-stu-id="13791-118">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span></span>

## <a name="project-actuals-from-project-service-automation"></a><span data-ttu-id="13791-119">Project Service Automation 中的專案實際值</span><span class="sxs-lookup"><span data-stu-id="13791-119">Project actuals from Project Service Automation</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="13791-120">範本與工作</span><span class="sxs-lookup"><span data-stu-id="13791-120">Template and tasks</span></span>

<span data-ttu-id="13791-121">若要存取可用範本，請在 Microsoft Power Apps 系統管理中心選取 **專案** ，然後選取右上角的 **新增專案** 以選取公用範本。</span><span class="sxs-lookup"><span data-stu-id="13791-121">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="13791-122">下列範本與基礎工作會用來將專案實際值從 Project Service Automation 同步處理至 Finance：</span><span class="sxs-lookup"><span data-stu-id="13791-122">The following template and underlying tasks are used to synchronize project actuals from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="13791-123">**資料整合中範本的名稱：** 專案實際值 (PSA 至 Fin 和 Ops)</span><span class="sxs-lookup"><span data-stu-id="13791-123">**Name of the template in Data integration:** Project actuals (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="13791-124">**專案中工作的名稱：**</span><span class="sxs-lookup"><span data-stu-id="13791-124">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="13791-125">實際值</span><span class="sxs-lookup"><span data-stu-id="13791-125">Actuals</span></span>
    - <span data-ttu-id="13791-126">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="13791-126">TransactionConnections</span></span>

### <a name="entity-set"></a><span data-ttu-id="13791-127">實體集</span><span class="sxs-lookup"><span data-stu-id="13791-127">Entity set</span></span>

| <span data-ttu-id="13791-128">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="13791-128">Project Service Automation</span></span> | <span data-ttu-id="13791-129">財務</span><span class="sxs-lookup"><span data-stu-id="13791-129">Finance</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="13791-130">實際值</span><span class="sxs-lookup"><span data-stu-id="13791-130">Actuals</span></span>                    | <span data-ttu-id="13791-131">專案實際值的整合實體</span><span class="sxs-lookup"><span data-stu-id="13791-131">Integration entity for project actuals</span></span>                   |
| <span data-ttu-id="13791-132">交易人脈</span><span class="sxs-lookup"><span data-stu-id="13791-132">Transaction Connections</span></span>    | <span data-ttu-id="13791-133">專案交易關聯的整合實體</span><span class="sxs-lookup"><span data-stu-id="13791-133">Integration entity for project transaction relationships</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="13791-134">實體流程</span><span class="sxs-lookup"><span data-stu-id="13791-134">Entity flow</span></span>

<span data-ttu-id="13791-135">專案實際值是在 Project Service Automation 中進行管理，並同步處理至 Finance 中的專案整合日記帳。</span><span class="sxs-lookup"><span data-stu-id="13791-135">Project actuals are managed in Project Service Automation, and they are synchronized to the project integration journal in Finance.</span></span> <span data-ttu-id="13791-136">會計系統將會根據預設財務維度和過帳設定來套用。</span><span class="sxs-lookup"><span data-stu-id="13791-136">The accounting will be applied based on default financial dimensions and the posting setup.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="13791-137">先決條件</span><span class="sxs-lookup"><span data-stu-id="13791-137">Prerequisites</span></span>

<span data-ttu-id="13791-138">實際值同步處理發生之前，您必須先設定 Project Service Automation 整合參數，並同步處理專案、專案工作以及專案費用交易類別。</span><span class="sxs-lookup"><span data-stu-id="13791-138">Before synchronization of actuals can occur, you must configure the Project Service Automation integration parameters and synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="13791-139">Power Query</span><span class="sxs-lookup"><span data-stu-id="13791-139">Power Query</span></span>

<span data-ttu-id="13791-140">在專案實際值範本中，您必須使用 Microsoft Power Query for Excel 來完成這些工作：</span><span class="sxs-lookup"><span data-stu-id="13791-140">In the project actuals template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="13791-141">將 Project Service Automation 中的交易類型轉換為 Finance 中的正確交易類型。</span><span class="sxs-lookup"><span data-stu-id="13791-141">Transform the transaction type in Project Service Automation to the correct transaction type in Finance.</span></span> <span data-ttu-id="13791-142">此轉換已經在「專案實際值 (PSA 至 Fin 和 Ops)」範本中定義。</span><span class="sxs-lookup"><span data-stu-id="13791-142">This transformation is already defined in the Project actuals (PSA to Fin and Ops) template.</span></span>
- <span data-ttu-id="13791-143">將 Project Service Automation 中的帳單類型轉換為 Finance 中的正確帳單類型。</span><span class="sxs-lookup"><span data-stu-id="13791-143">Transform the billing type in Project Service Automation to the correct billing type in Finance.</span></span> <span data-ttu-id="13791-144">此轉換已經在「專案實際值 (PSA 至 Fin 和 Ops)」範本中定義。</span><span class="sxs-lookup"><span data-stu-id="13791-144">This transformation is already defined in the Project actuals (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="13791-145">然後，根據 **Project Service Automation 整合參數** 頁面上的設定，將帳單類型對應至明細屬性。</span><span class="sxs-lookup"><span data-stu-id="13791-145">The billing type is then mapped to the line property, based on the configuration on the **Project Service Automation integration parameters** page.</span></span>
- <span data-ttu-id="13791-146">篩選為必須與此範本同步處理的特定資源組織單位。</span><span class="sxs-lookup"><span data-stu-id="13791-146">Filter to specific resource organizational units that must be synchronized with this template.</span></span>
- <span data-ttu-id="13791-147">如果公司間時間或公司間費用實際值會同步處理至 Finance，您必須將合約組織單位轉換為 Finance 中的正確法律實體。</span><span class="sxs-lookup"><span data-stu-id="13791-147">If intercompany time or intercompany expense actuals will be synchronized to Finance, you must transform the contract organizational unit to the correct legal entity in Finance.</span></span> <span data-ttu-id="13791-148">在「專案實際值 (PSA 至 Fin 和 Ops)」範本中，根據示範資料定義條件欄。</span><span class="sxs-lookup"><span data-stu-id="13791-148">In the Project actuals (PSA to Fin and Ops) template, a conditional column is defined based on demo data.</span></span> <span data-ttu-id="13791-149">您必須將上次插入的條件欄更新為正確的法律實體。</span><span class="sxs-lookup"><span data-stu-id="13791-149">You must update the last inserted conditional column to the correct legal entities.</span></span> <span data-ttu-id="13791-150">否則，可能會發生整合錯誤，或者可能會將不正確的實際值交易匯入至 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="13791-150">Otherwise, either an integration error might occur, or incorrect actual transactions might be imported into Finance.</span></span>
- <span data-ttu-id="13791-151">如果公司間時間或公司間費用實際值不會同步處理至 Finance，就必須從範本中移除上次插入的條件欄。</span><span class="sxs-lookup"><span data-stu-id="13791-151">If intercompany time or intercompany expense actuals won't be synchronized to Finance, you must delete the last inserted conditional column from your template.</span></span> <span data-ttu-id="13791-152">否則，可能會發生整合錯誤，或者可能會將不正確的實際值交易匯入至 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="13791-152">Otherwise, either an integration error might occur, or incorrect actual transactions might be imported into Finance.</span></span>

#### <a name="contract-organizational-unit"></a><span data-ttu-id="13791-153">合約組織單位</span><span class="sxs-lookup"><span data-stu-id="13791-153">Contract organizational unit</span></span>
<span data-ttu-id="13791-154">若要更新範本中插入的條件欄，請按一下 **對應** 箭頭以開啟對應。</span><span class="sxs-lookup"><span data-stu-id="13791-154">To update the inserted conditional column in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="13791-155">選取 **進階查詢及篩選** 連結，以開啟 Power Query。</span><span class="sxs-lookup"><span data-stu-id="13791-155">Select the **Advanced Query and Filtering** link to open Power Query.</span></span>

- <span data-ttu-id="13791-156">如果您使用預設「專案實際值 (PSA 至 Fin 和 Ops)」範本，請在 Power Query 中，從 **已套用的步驟** 區段中選取上次 **插入的條件** 。</span><span class="sxs-lookup"><span data-stu-id="13791-156">If you're using the default Project actuals (PSA to Fin and Ops) template, in Power Query, select the last **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="13791-157">在 **函數** 項目中，將 **USSI** 取代為應與整合搭配使用的法律實體名稱。</span><span class="sxs-lookup"><span data-stu-id="13791-157">In the **Function** entry, replace **USSI** with the name of the legal entity that should be used with the integration.</span></span> <span data-ttu-id="13791-158">視需要將其他條件新增至 **函數** 項目，並將 **否則** 條件從 **USMF** 更新為正確的法律實體。</span><span class="sxs-lookup"><span data-stu-id="13791-158">Add additional conditions to the **Function** entry as you require, and update the **else** condition from **USMF** to the correct legal entity.</span></span>
- <span data-ttu-id="13791-159">如果要建立新範本，您必須新增該欄才能支援公司間的時間與費用。</span><span class="sxs-lookup"><span data-stu-id="13791-159">If you're creating a new template, you must add the column to support intercompany time and expenses.</span></span> <span data-ttu-id="13791-160">選取 **新增條件欄** ，並輸入該欄的名稱，例如 **LegalEntity** 。</span><span class="sxs-lookup"><span data-stu-id="13791-160">Select **Add Conditional Column** , and enter a name for the column, such as **LegalEntity**.</span></span> <span data-ttu-id="13791-161">輸入該欄的條件，如果 **msdyn\_contractorganizationalunitid.msdyn\_name** 是 \<organizational unit\>，則為 \<enter the legal entity\>；否則為 Null。</span><span class="sxs-lookup"><span data-stu-id="13791-161">Enter a condition for the column, where, if **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="13791-162">資料整合中的範本對應</span><span class="sxs-lookup"><span data-stu-id="13791-162">Template mapping in Data integration</span></span>

<span data-ttu-id="13791-163">下圖顯示資料整合中的範本工作對應範例。</span><span class="sxs-lookup"><span data-stu-id="13791-163">The following illustrations show an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="13791-164">此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="13791-164">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="13791-165">[![範本對應 - 實際值](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="13791-165">[![Template mapping - Actuals](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span></span>

<span data-ttu-id="13791-166">[![範本對應 - 交易人脈](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span><span class="sxs-lookup"><span data-stu-id="13791-166">[![Template mapping - Transaction connections](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span></span>

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a><span data-ttu-id="13791-167">從 Project Service Automation 整合之後從暫存表格匯入</span><span class="sxs-lookup"><span data-stu-id="13791-167">Import from staging table after integration from Project Service Automation</span></span>

<span data-ttu-id="13791-168">[從暫存表格匯入] 定期程序必須在實際值從 Project Service Automation 同步處理後執行。</span><span class="sxs-lookup"><span data-stu-id="13791-168">The Import from staging table periodic process must be run after the synchronization of actuals from Project Service Automation to Finance.</span></span> <span data-ttu-id="13791-169">此程序會將專案交易從暫存表格匯入至 Project Service Automation 整合日記帳，其中會套用會計功能，並且可以過帳匯入的交易。</span><span class="sxs-lookup"><span data-stu-id="13791-169">This process will import the project transactions from the staging table into the Project Service Automation integration journal, where the accounting is applied and the imported transactions can be posted.</span></span> <span data-ttu-id="13791-170">建議您在批次模式下執行此程序；您可以選擇性將此程序設定為以定期批次方式執行。</span><span class="sxs-lookup"><span data-stu-id="13791-170">We recommend that you run this process in batch mode; it can optionally be set up to run as a recurring batch.</span></span>

## <a name="update-actuals-from-finance"></a><span data-ttu-id="13791-171">從 Finance 更新實際值</span><span class="sxs-lookup"><span data-stu-id="13791-171">Update actuals from Finance</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="13791-172">範本與工作</span><span class="sxs-lookup"><span data-stu-id="13791-172">Template and tasks</span></span>

<span data-ttu-id="13791-173">以下範本及基礎工作會用於將已過帳專案交易的憑單編號和銷售稅金，從 Finance 同步處理至Project Service Automation：</span><span class="sxs-lookup"><span data-stu-id="13791-173">The following template and underlying tasks are used to synchronize the voucher number and sales taxes for posted project transactions from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="13791-174">**資料整合中範本的名稱：** 專案實際值更新 (Fin Ops 至 PSA)</span><span class="sxs-lookup"><span data-stu-id="13791-174">**Name of the template in Data integration:** Project actuals update (Fin Ops to PSA)</span></span>
- <span data-ttu-id="13791-175">**專案中工作的名稱：**</span><span class="sxs-lookup"><span data-stu-id="13791-175">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="13791-176">實際值</span><span class="sxs-lookup"><span data-stu-id="13791-176">Actuals</span></span> 
    - <span data-ttu-id="13791-177">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="13791-177">TransactionConnections</span></span>

### <a name="entity-set"></a><span data-ttu-id="13791-178">實體集</span><span class="sxs-lookup"><span data-stu-id="13791-178">Entity set</span></span>

| <span data-ttu-id="13791-179">財務</span><span class="sxs-lookup"><span data-stu-id="13791-179">Finance</span></span>                                                  | <span data-ttu-id="13791-180">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="13791-180">Project Service Automation</span></span> |
|----------------------------------------------------------|----------------------------|
| <span data-ttu-id="13791-181">專案實際值的整合實體</span><span class="sxs-lookup"><span data-stu-id="13791-181">Integration entity for project actuals</span></span>                   | <span data-ttu-id="13791-182">實際值</span><span class="sxs-lookup"><span data-stu-id="13791-182">Actuals</span></span>                    |
| <span data-ttu-id="13791-183">專案交易關聯的整合實體</span><span class="sxs-lookup"><span data-stu-id="13791-183">Integration entity for project transaction relationships</span></span> | <span data-ttu-id="13791-184">交易人脈</span><span class="sxs-lookup"><span data-stu-id="13791-184">Transaction Connections</span></span>    |

### <a name="entity-flow"></a><span data-ttu-id="13791-185">實體流程</span><span class="sxs-lookup"><span data-stu-id="13791-185">Entity flow</span></span>

<span data-ttu-id="13791-186">專案實際值是在 Project Service Automation 中進行管理，並同步處理至 Finance 中的專案整合日記帳。</span><span class="sxs-lookup"><span data-stu-id="13791-186">Project actuals are managed in Project Service Automation, and they are synchronized to the project integration journal in Finance.</span></span> <span data-ttu-id="13791-187">在 Finance 中過帳實際值之後，這些實際值會在 Project Service Automation 中更新為 Finance 中的憑單編號。</span><span class="sxs-lookup"><span data-stu-id="13791-187">After actuals are posted in Finance, they are updated in Project Service Automation with the voucher number from Finance.</span></span> <span data-ttu-id="13791-188">如果在 Finance 中新增了銷售稅金，則會在 Project Service Automation 中建立新的稅金實際值。</span><span class="sxs-lookup"><span data-stu-id="13791-188">If sales taxes were added in Finance, new tax actuals are created in Project Service Automation.</span></span>

### <a name="power-query"></a><span data-ttu-id="13791-189">Power Query</span><span class="sxs-lookup"><span data-stu-id="13791-189">Power Query</span></span>

<span data-ttu-id="13791-190">在專案實際值更新範本中，您必須使用 Power Query 來完成這些工作：</span><span class="sxs-lookup"><span data-stu-id="13791-190">In the project actuals update template, you must use Power Query to complete these tasks:</span></span>

- <span data-ttu-id="13791-191">將 Finance 中的交易類型轉換為 Project Service Automation 中的正確交易類型。</span><span class="sxs-lookup"><span data-stu-id="13791-191">Transform the transaction type in Finance to the correct transaction type in Project Service Automation.</span></span> <span data-ttu-id="13791-192">此轉換已經在「專案實際值更新 (Fin Ops 至 PSA)」範本中定義。</span><span class="sxs-lookup"><span data-stu-id="13791-192">This transformation is already defined in the Project actuals update (Fin Ops to PSA) template.</span></span>
- <span data-ttu-id="13791-193">將 Finance 中的帳單類型轉換為 Project Service Automation 中的正確帳單類型。</span><span class="sxs-lookup"><span data-stu-id="13791-193">Transform the billing type in Finance to the correct billing type in Project Service Automation.</span></span> <span data-ttu-id="13791-194">此轉換已經在「專案實際值更新 (Fin Ops 至 PSA)」範本中定義。</span><span class="sxs-lookup"><span data-stu-id="13791-194">This transformation is already defined in the Project actuals update (Fin Ops to PSA) template.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="13791-195">資料整合中的範本對應</span><span class="sxs-lookup"><span data-stu-id="13791-195">Template mapping in Data integration</span></span>

<span data-ttu-id="13791-196">下圖顯示資料整合中的範本工作對應範例。</span><span class="sxs-lookup"><span data-stu-id="13791-196">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="13791-197">此對應顯示會從 Finance 同步處理至 Project Service Automation 的欄位資訊。</span><span class="sxs-lookup"><span data-stu-id="13791-197">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="13791-198">[![範本對應 - 實際值更新](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="13791-198">[![Template mapping - Actuals update](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span></span>

<span data-ttu-id="13791-199">[![範本對應 - 交易更新](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span><span class="sxs-lookup"><span data-stu-id="13791-199">[![Template mapping - Transaction update](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span></span>
