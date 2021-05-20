---
title: 廠商發票整合
description: 本主題提供有關 Project Operations 中廠商發票整合的資訊。
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955718"
---
# <a name="vendor-invoice-integration"></a><span data-ttu-id="0a79f-103">廠商發票整合</span><span class="sxs-lookup"><span data-stu-id="0a79f-103">Vendor invoice integration</span></span>

<span data-ttu-id="0a79f-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0a79f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0a79f-105">移至 **應付帳款** > **發票** > **待處理廠商發票** 並使用待處理廠商發票單據，可以記錄 Dynamics 365 Project Operations 中的專案相關採購。</span><span class="sxs-lookup"><span data-stu-id="0a79f-105">Project-related procurement in Dynamics 365 Project Operations can be recorded by going to **Accounts Payable** > **Invoices** > **Pending vendor invoices** and using a pending vendor invoice document.</span></span> <span data-ttu-id="0a79f-106">如需詳細資訊，請參閱[使用待處理廠商發票購買非庫存材料](../procurement/pending-vendor-invoices.md)。</span><span class="sxs-lookup"><span data-stu-id="0a79f-106">For more information, see [Purchase non-stocked materials using a pending vendor invoice](../procurement/pending-vendor-invoices.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a79f-107">使用本主題中所述的功能之前，請先檢閱並套用必要的設定。</span><span class="sxs-lookup"><span data-stu-id="0a79f-107">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="0a79f-108">如需詳細資訊，請參閱[啟用非庫存材料和待處理廠商發票](../procurement/configure-materials-nonstocked.md)。</span><span class="sxs-lookup"><span data-stu-id="0a79f-108">For more information, see [Enable non-stocked materials and pending vendor invoices](../procurement/configure-materials-nonstocked.md).</span></span>

<span data-ttu-id="0a79f-109">在 Project Operations 中，會使用特殊過帳規則將專案相關廠商發票過帳：</span><span class="sxs-lookup"><span data-stu-id="0a79f-109">In Project Operations, project-related vendor invoices are posted using special posting rules:</span></span>

- <span data-ttu-id="0a79f-110">專案相關成本 (包括不可退回稅金) 不會立即過帳至總帳中的專案成本科目。</span><span class="sxs-lookup"><span data-stu-id="0a79f-110">Project-related cost (including non-recoverable tax) isn't immediately posted to the project cost account in the general ledger.</span></span> <span data-ttu-id="0a79f-111">反而是將成本過帳至 **採購整合科目**。</span><span class="sxs-lookup"><span data-stu-id="0a79f-111">Instead, the cost is posted to the **Procurement integration account**.</span></span> <span data-ttu-id="0a79f-112">此科目是在 **Dynamics 365 Customer Engagement 上的 Project Operations** 索引標籤的 **專案管理與會計** > **設定** > **專案管理與會計參數** 中進行設定。</span><span class="sxs-lookup"><span data-stu-id="0a79f-112">This account is configured in **Project management and accounting** > **Setup** > **Project management and accounting parameters** on the **Project Operations on Dynamics 365 Customer engagement** tab.</span></span>
- <span data-ttu-id="0a79f-113">雙重寫入會使用下列資料表對應，將廠商發票詳細資料同步處理 Microsoft Dataverse：</span><span class="sxs-lookup"><span data-stu-id="0a79f-113">Dual-write synchronizes vendor invoice details to Microsoft Dataverse using the following table maps:</span></span>

     - <span data-ttu-id="0a79f-114">**Project Operations 整合專案廠商發票匯出實體 (msdyn_projectvendorinvoices)**：此資料表對應會同步處理廠商發票標題資訊。</span><span class="sxs-lookup"><span data-stu-id="0a79f-114">**Project Operations integration project vendor invoice export entity (msdyn_projectvendorinvoices)**: This table map synchronizes vendor invoice header information.</span></span> <span data-ttu-id="0a79f-115">只有在廠商發票至少有一行明細包含專案識別碼時，才會同步處理至 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="0a79f-115">Only vendor invoices with at least one line that contains a project ID are synchronized to Dataverse.</span></span>
     - <span data-ttu-id="0a79f-116">**Project Operations 整合專案廠商發票明細匯出實體 (msdyn_projectvendorinvoicelines)**：此資料表對應會同步處理廠商發票明細資訊。</span><span class="sxs-lookup"><span data-stu-id="0a79f-116">**Project Operations integration project vendor invoice line export entity (msdyn_projectvendorinvoicelines)**: This table map synchronizes vendor invoice line information.</span></span> <span data-ttu-id="0a79f-117">只有包含專案識別碼的訂單才會同步處理至 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="0a79f-117">Only lines that contain a project ID are synchronized to Dataverse.</span></span>

     > [!NOTE]
     > <span data-ttu-id="0a79f-118">Dataverse 中的廠商發票詳細資料不可編輯。</span><span class="sxs-lookup"><span data-stu-id="0a79f-118">Vendor invoice details in Dataverse are not editable.</span></span>

<span data-ttu-id="0a79f-119">系統會在過帳廠商發票時，視實際情況在 Dynamics 365 Finance 中記錄稅金子分類帳、廠商子分類帳及其他財務過帳。</span><span class="sxs-lookup"><span data-stu-id="0a79f-119">Tax subledger, vendor subledger, and other financial postings are recorded as applicable in Dynamics 365 Finance when the vendor invoice is posted.</span></span>

![廠商發票整合](media/DW7VendorInvoice.png)

<span data-ttu-id="0a79f-121">將記錄寫入 Dataverse 中的 **廠商發票** 實體時，記錄的自動化核准程序會開始。</span><span class="sxs-lookup"><span data-stu-id="0a79f-121">When records are written to a **Vendor invoice** entity in Dataverse, an automated approval process of the records begins.</span></span> <span data-ttu-id="0a79f-122">如果需要，您可以移至 **進階設定** > **系統** > **系統作業**，在 Dataverse 中檢閱自動化核准程序狀態。</span><span class="sxs-lookup"><span data-stu-id="0a79f-122">If needed, the automated approval process status can be reviewed in Dataverse by going to **Advanced settings** > **System** > **System jobs**.</span></span> <span data-ttu-id="0a79f-123">核准完成後，系統會在 **實際值** 實體中建立材料交易分類記錄。</span><span class="sxs-lookup"><span data-stu-id="0a79f-123">After the approval is complete, the system creates material transaction class records in the **Actuals** entity.</span></span>

<span data-ttu-id="0a79f-124">接著會使用雙重寫入資料表對應 **Project Operations 整合實際值 (msdyn_actuals)** 來處理材料相關實際值。</span><span class="sxs-lookup"><span data-stu-id="0a79f-124">Material-related actuals are then processed using the dual-write table map, **Project Operations integration actuals (msdyn_actuals)**.</span></span> <span data-ttu-id="0a79f-125">如需詳細資訊，請參閱[專案估計值和實際值](resource-dual-write-estimates-actuals.md)。</span><span class="sxs-lookup"><span data-stu-id="0a79f-125">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span>

<span data-ttu-id="0a79f-126">定期程序 **從臨時表格匯入** 會建立廠商發票相關 Project Operations 整合帳目明細。</span><span class="sxs-lookup"><span data-stu-id="0a79f-126">The periodic process, **Import from staging** creates vendor invoice-related Project Operations integration journal lines.</span></span> <span data-ttu-id="0a79f-127">抵銷科目預設為採購整合科目。</span><span class="sxs-lookup"><span data-stu-id="0a79f-127">The offset account defaults to the procurement integration account.</span></span> <span data-ttu-id="0a79f-128">過帳整合帳目時，會結清廠商發票交易的帳戶餘額，並將明細金額轉入專案成本科目。</span><span class="sxs-lookup"><span data-stu-id="0a79f-128">When the integration journal is posted, the account balance is cleared for the vendor invoice transaction and the line amount is moved to the project cost account.</span></span> <span data-ttu-id="0a79f-129">系統還會建立專案子分類帳交易，供作下游開立發票和收入認列之用。</span><span class="sxs-lookup"><span data-stu-id="0a79f-129">Project subledger transactions are also created for downstream invoicing and revenue recognition purposes.</span></span>
