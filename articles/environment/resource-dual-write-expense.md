---
title: 費用管理整合
description: 本主題提供有關 Project Operations 中使用雙重寫入進行費用報表整合的資訊。
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7fff69f062bf09fe7ceca61d951b535d2e010bfd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999976"
---
# <a name="expense-management-integration"></a><span data-ttu-id="c415b-103">費用管理整合</span><span class="sxs-lookup"><span data-stu-id="c415b-103">Expense management integration</span></span>

<span data-ttu-id="c415b-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="c415b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c415b-105">本主題提供有關 Project Operations [全額費用部署](../expense/expense-overview.md)中使用雙重寫入進行費用報表整合的資訊。</span><span class="sxs-lookup"><span data-stu-id="c415b-105">This topic provides information about expense reports integration in Project Operations [full expense deployment](../expense/expense-overview.md) using dual-write.</span></span>

## <a name="expense-categories"></a><span data-ttu-id="c415b-106">費用類別</span><span class="sxs-lookup"><span data-stu-id="c415b-106">Expense categories</span></span>

<span data-ttu-id="c415b-107">在全額費用部署中，費用類別是在 Finance and Operations 應用程式中所建立和維護。</span><span class="sxs-lookup"><span data-stu-id="c415b-107">In a full expense deployment, expense categories are created and maintained in Finance and Operations apps.</span></span> <span data-ttu-id="c415b-108">若要建立新的費用類別，完成下列步驟：</span><span class="sxs-lookup"><span data-stu-id="c415b-108">To create a new expense category, complete the following steps:</span></span>

1. <span data-ttu-id="c415b-109">在 Microsoft Dataverse 中，建立 **交易** 類別。</span><span class="sxs-lookup"><span data-stu-id="c415b-109">In Microsoft Dataverse, create a **Transaction** category.</span></span> <span data-ttu-id="c415b-110">雙重寫入整合會將此交易類別同步處理至 Finance and Operations 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c415b-110">Dual-write integration will synchronize this transaction category to Finance and Operations apps.</span></span> <span data-ttu-id="c415b-111">如需詳細資訊，請參閱[設定專案類別](/dynamics365/project-operations/project-accounting/configure-project-categories)和 [Project Operations 設定和設定資料整合](resource-dual-write-setup-integration.md)。</span><span class="sxs-lookup"><span data-stu-id="c415b-111">For more information, see [Configure project categories](/dynamics365/project-operations/project-accounting/configure-project-categories) and [Project Operations setup and configuration data integration](resource-dual-write-setup-integration.md).</span></span> <span data-ttu-id="c415b-112">由於此整合，系統在 Finance and Operations 應用程式中建立四個共用類別記錄。</span><span class="sxs-lookup"><span data-stu-id="c415b-112">As a result of this integration, the system creates four shared category records in Finance and Operations apps.</span></span>
2. <span data-ttu-id="c415b-113">在 Finance 中，移至 **費用管理** > **設定** > **共用類別**，然後選取具有 **費用** 交易分類的共用類別。</span><span class="sxs-lookup"><span data-stu-id="c415b-113">In Finance, go to **Expense management** > **Setup** > **Shared categories** and select a shared category with an **Expense** transaction class.</span></span> <span data-ttu-id="c415b-114">將 **可在費用中使用** 參數設定為 **True**，並定義要使用的費用類型。</span><span class="sxs-lookup"><span data-stu-id="c415b-114">Set the **Can be used in Expense** parameter to **True** and define the expense type to use.</span></span>
3. <span data-ttu-id="c415b-115">移至 **費用管理** > **設定** > **費用類別** 並選擇 **新增**，以使用此共用類別記錄建立新的費用類別。</span><span class="sxs-lookup"><span data-stu-id="c415b-115">Using this shared category record, create a new expense category by going to **Expense management** > **Setup** > **Expense categories** and selecting **New**.</span></span> <span data-ttu-id="c415b-116">儲存記錄時，雙重寫入會使用資料表對應 **Project Operations 整合專案費用類別匯出實體 (msdyn\_expensecategories)**，將此記錄同步處理至 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="c415b-116">When the record is saved, dual-write uses the table map, **Project Operations integration project expense categories export entity (msdyn\_expensecategories)** to synchronize this record to Dataverse.</span></span>

  ![費用類別整合](./media/DW6ExpenseCategories.png)

<span data-ttu-id="c415b-118">Finance and Operations 應用程式中的費用類別各有不同的適用公司或法律實體。</span><span class="sxs-lookup"><span data-stu-id="c415b-118">Expense categories in Finance and Operations apps are company- or legal entity-specific.</span></span> <span data-ttu-id="c415b-119">在 Dataverse 中有個別對應的法律實體特定記錄。</span><span class="sxs-lookup"><span data-stu-id="c415b-119">There are separate, corresponding legal entity-specific records in Dataverse.</span></span> <span data-ttu-id="c415b-120">當專案經理估計費用時，他們無法選取針對由與擁有他們所從事專案之公司不同的公司所建立的費用類別。</span><span class="sxs-lookup"><span data-stu-id="c415b-120">When a project manager estimates expenses, they can’t select expense categories that were created for a project that is owned by a different company than the company that owns the project they are working on.</span></span> 

## <a name="expense-reports"></a><span data-ttu-id="c415b-121">費用報表</span><span class="sxs-lookup"><span data-stu-id="c415b-121">Expense reports</span></span>

<span data-ttu-id="c415b-122">費用報表是在 Finance and Operations 應用程式中所建立和核准。</span><span class="sxs-lookup"><span data-stu-id="c415b-122">Expense reports are created and approved in Finance and Operations apps.</span></span> <span data-ttu-id="c415b-123">如需詳細資訊，請參閱[在 Dynamics 365 Project Operations 中建立和處理費用報價](/learn/modules/create-process-expense-reports/)。</span><span class="sxs-lookup"><span data-stu-id="c415b-123">For more information, see [Create and process expense reports in Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/).</span></span> <span data-ttu-id="c415b-124">專案經理核准費用報表之後，此報價會過帳至總帳。</span><span class="sxs-lookup"><span data-stu-id="c415b-124">After the expense report is approved by the Project manager, it's posted to the general ledger.</span></span> <span data-ttu-id="c415b-125">在 Project Operations 中，會使用特殊過帳規則將專案相關費用報表明細過帳：</span><span class="sxs-lookup"><span data-stu-id="c415b-125">In Project Operations, project-related expense report lines are posted using special posting rules:</span></span>

  - <span data-ttu-id="c415b-126">專案相關成本 (包括不可退回稅金) 不會立即過帳至總帳中的專案成本科目，而是過帳至費用整合科目。</span><span class="sxs-lookup"><span data-stu-id="c415b-126">Project-related cost (including non-recoverable tax) is not immediately posted to project cost account in general ledger, but instead is posted to expense integration account.</span></span> <span data-ttu-id="c415b-127">此科目是在 **Dynamics 365 Customer Engagement 上的 Project Operations** 索引標籤的 **專案管理與會計** > **設定** > **專案管理與會計參數** 中進行設定。</span><span class="sxs-lookup"><span data-stu-id="c415b-127">This account is configured in **Project management and accounting** > **Setup** > **Project management and accounting parameters**, **Project Operations on Dynamics 365 Customer engagement** tab.</span></span>
  - <span data-ttu-id="c415b-128">雙重寫入會使用 **Project Operations 整合專案費用報表實體 (msdyn\_expenses)** 資料表對應來同步處理至 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="c415b-128">Dual-write synchronizes to Dataverse using **Project Operations integration project expenses export entity (msdyn\_expenses)** table map.</span></span>
  - <span data-ttu-id="c415b-129">系統會視費用報表過帳時的實際情況來記錄稅金子分類帳、廠商子分類帳及其他財務過帳。</span><span class="sxs-lookup"><span data-stu-id="c415b-129">Tax subledger, vendor subledger, and other financial postings are recorded as applicable at the time of expense report posting.</span></span>

  ![費用報表整合](./media/DW6ExpenseReports.png)

<span data-ttu-id="c415b-131">在 Dataverse 中將記錄寫入 **費用** 實體時，系統會觸發記錄的自動化核准程序。</span><span class="sxs-lookup"><span data-stu-id="c415b-131">When a record is written to the **Expense** entity in Dataverse, the system triggers the automated approval process of the record.</span></span> <span data-ttu-id="c415b-132">如果需要，您可以移至 **進階設定** > **系統** > **系統作業**，在 Dataverse 中檢閱自動化核准程序狀態。</span><span class="sxs-lookup"><span data-stu-id="c415b-132">If needed, the automated approval process status can be reviewed in Dataverse by going to **Advanced settings** > **System** > **System jobs**.</span></span> <span data-ttu-id="c415b-133">核准完成後，**實際值** 實體中會建立費用交易分類記錄。</span><span class="sxs-lookup"><span data-stu-id="c415b-133">After approval is complete, expense transaction class records are created in the **Actuals** entity.</span></span>

<span data-ttu-id="c415b-134">接著會使用雙重寫入資料表對應 **Project Operations 整合實際值 (msdyn\_actuals)** 來處理費用相關實際值。</span><span class="sxs-lookup"><span data-stu-id="c415b-134">Expense related actuals are then processed using the dual-write table map **Project Operations integration actuals (msdyn\_actuals)**.</span></span> <span data-ttu-id="c415b-135">如需詳細資訊，請參閱[專案估計值和實際值](resource-dual-write-estimates-actuals.md)。</span><span class="sxs-lookup"><span data-stu-id="c415b-135">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span>

<span data-ttu-id="c415b-136">定期程序 **從臨時表格匯入** 會在 Project Operations 整合帳目中建立費用報表相關帳目明細。</span><span class="sxs-lookup"><span data-stu-id="c415b-136">The periodic process, **Import from staging** creates Expense report-related journal lines in the Project Operations Integration journal.</span></span> <span data-ttu-id="c415b-137">抵銷科目預設為費用整合科目。</span><span class="sxs-lookup"><span data-stu-id="c415b-137">The offset account defaults to the expense integration account.</span></span> <span data-ttu-id="c415b-138">過帳整合帳目會結清費用交易的帳戶餘額，並將費用金額轉入專案成本科目。</span><span class="sxs-lookup"><span data-stu-id="c415b-138">The Posting integration journal clears the account balance for the expense transaction and moves the expense amount to the project cost account.</span></span> <span data-ttu-id="c415b-139">系統還會建立專案子分類帳交易，供作下游開立發票和收入認列之用。</span><span class="sxs-lookup"><span data-stu-id="c415b-139">The system also creates project subledger transactions for downstream invoicing and revenue recognition purposes.</span></span>