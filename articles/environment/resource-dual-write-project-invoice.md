---
title: 專案發票整合
description: 本主題提供有關用於開立客戶發票之 Project Operations 雙重寫入整合的資訊。
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996556"
---
# <a name="project-invoice-integration"></a><span data-ttu-id="d345f-103">專案發票整合</span><span class="sxs-lookup"><span data-stu-id="d345f-103">Project invoice integration</span></span>

<span data-ttu-id="d345f-104">本主題提供有關用於開立客戶發票之 Project Operations 雙重寫入整合的資訊。</span><span class="sxs-lookup"><span data-stu-id="d345f-104">This topic provides information about Project Operations dual-write integration for customer invoicing.</span></span>

<span data-ttu-id="d345f-105">在 Project Operations 中，專案經理會管理專案帳務積存，並在 Microsoft Dataverse 中為客戶建立預估發票。</span><span class="sxs-lookup"><span data-stu-id="d345f-105">In Project Operations, the Project manager manages the project billing backlog and creates a proforma invoice for the customer in Microsoft Dataverse.</span></span> <span data-ttu-id="d345f-106">應收帳款記帳員或專案會計師會根據此預估發票，建立客戶面向發票。</span><span class="sxs-lookup"><span data-stu-id="d345f-106">Based on this proforma invoice, the Accounts receivable clerk or Project accountant creates a customer-facing invoice.</span></span> <span data-ttu-id="d345f-107">雙重寫入整合可確保將預估發票詳細資料同步處理至 Finance and Operations 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d345f-107">Dual-write integration ensures that the proforma invoice details are synchronized to Finance and Operations apps.</span></span> <span data-ttu-id="d345f-108">將客戶面向發票過帳之後，系統 會根據會計詳細資料更新 Dataverse 中的相關專案實際值。</span><span class="sxs-lookup"><span data-stu-id="d345f-108">After the customer-facing invoice is posted, the system updates the relevant project actuals in Dataverse with the accounting detail.</span></span> <span data-ttu-id="d345f-109">下圖提供此項整合的高階概念概觀。</span><span class="sxs-lookup"><span data-stu-id="d345f-109">The following graphic provides a high-level conceptual overview of this integration.</span></span>

   ![專案發票整合](./media/DW5Invoicing.png)

<span data-ttu-id="d345f-111">專案經理在 Dataverse 中確認預估發票之後，預估發票標題資訊會使用雙重寫入資料表對應 **專案發票提案 V2 (發票)** 同步處理至 Finance and Operations 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d345f-111">After the Project manager confirms the proforma invoice in Dataverse, the proforma invoice header information synchronizes to Finance and Operations apps using the dual-write table map, **Project invoice proposal V2 (invoices)**.</span></span> <span data-ttu-id="d345f-112">這是從 Dataverse 到 Finance and Operations 應用程式的單向整合。</span><span class="sxs-lookup"><span data-stu-id="d345f-112">This is a one-way integration from Dataverse to Finance and Operations apps.</span></span> <span data-ttu-id="d345f-113">不支援直接在 Finance and Operations 應用程式中建立或刪除專案發票提案。</span><span class="sxs-lookup"><span data-stu-id="d345f-113">Creating or deleting Project invoice proposals directly in Finance and Operations apps isn't supported.</span></span>

<span data-ttu-id="d345f-114">Dataverse 中的發票確認還會觸發商務規則，在 **實際值** 實體中建立帳務相關記錄。</span><span class="sxs-lookup"><span data-stu-id="d345f-114">Invoice confirmation in Dataverse also triggers the business logic to create billing-related records in the **Actuals** entity.</span></span> <span data-ttu-id="d345f-115">這些記錄是使用雙重寫入資料表對應 **Project Operations 整合實際值 (msdyn\_actuals)** 同步處理至 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="d345f-115">These records are synchronized to Finance and Operations using the dual-write table map, **Project Operations integration actuals (msdyn\_actuals).**</span></span> <span data-ttu-id="d345f-116">如需詳細資訊，請參閱[專案估計值和實際值](resource-dual-write-estimates-actuals.md)。</span><span class="sxs-lookup"><span data-stu-id="d345f-116">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span> 

<span data-ttu-id="d345f-117">專案發票提案明細是由定期程序 **從臨時表格匯入** 所建立。</span><span class="sxs-lookup"><span data-stu-id="d345f-117">Project invoice proposal lines are created by the periodic process, **Import form staging**.</span></span> <span data-ttu-id="d345f-118">此程序是根據 **實際值臨時表格** 資料表中的已開單銷售實際值詳細資料來執行。</span><span class="sxs-lookup"><span data-stu-id="d345f-118">This process is based on the billed sales actuals details in the **Actuals staging** table.</span></span> <span data-ttu-id="d345f-119">如需詳細資訊，請參閱[管理專案發票提案](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)。</span><span class="sxs-lookup"><span data-stu-id="d345f-119">For more information, see [Manage project invoice proposals](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals).</span></span> 
