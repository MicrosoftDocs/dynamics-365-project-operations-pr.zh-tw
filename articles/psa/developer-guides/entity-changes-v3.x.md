---
title: 實體、控制項和使用者介面變更 (Project Service Automation 3.x)
description: 本主題說明 Microsoft Dynamics Project Service Automation 3.x 中的解決方案變更。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: fa80f459260f30360e78a1e7bcc00706dbc0b5a4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284888"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a><span data-ttu-id="236a4-103">實體、控制項和使用者介面變更 (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="236a4-103">Entity, control, and user interface changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]


<span data-ttu-id="236a4-104">Microsoft Dynamics Project Service Automation (PSA) 3.x 發行後，實體、控制項、檢視表和使用者介面已發生許多變更。</span><span class="sxs-lookup"><span data-stu-id="236a4-104">With the release of Microsoft Dynamics Project Service Automation (PSA) 3.x, many changes have been made to the entities, controls, views, and user interface.</span></span> <span data-ttu-id="236a4-105">本主題提供有關這些重要變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="236a4-105">This topic provides information about these important changes.</span></span>

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a><span data-ttu-id="236a4-106">銷售文件、銷售文件明細、銷售文件明細詳細資料實體的上下層關聯</span><span class="sxs-lookup"><span data-stu-id="236a4-106">Parent-child relationships for sales document, sales document line, sales document line detail entities</span></span>
<span data-ttu-id="236a4-107">在版本 3.0 之前發行的 Dynamics 365 Project Service Automation (PSA) 版本中，銷售文件、銷售文件明細、銷售文件明細詳細資料實體之間的部分關聯是透過保存相關實體 GUID 之字串表示法的字串欄位來實作。</span><span class="sxs-lookup"><span data-stu-id="236a4-107">In versions of Dynamics 365 Project Service Automation (PSA) released prior to version 3.0, some of the relationships between sales documents, sales document lines, and sales document line detail entities were implemented through string fields that would hold a string representation of GUID of the related entity.</span></span> <span data-ttu-id="236a4-108">這是因為平台的限制，要求解決方案伺服器端及用戶端上必須有大量自訂程式碼，才能讓這些關聯運作起來仿如一般 Dynamics CRM 實體關聯，以及讓字串欄位作用起來像查詢欄位那樣。</span><span class="sxs-lookup"><span data-stu-id="236a4-108">This was due to platform limitations that required significant custom code on the server and client sides of the solution to make those relationships work similar to typical Dynamics CRM entity relationships and to make string fields act like lookup fields.</span></span>

<span data-ttu-id="236a4-109">PSA 3.0 已更新為運用銷售文件與銷售文件明細實體之間的新實體關聯。</span><span class="sxs-lookup"><span data-stu-id="236a4-109">PSA 3.0 has been updated to leverage the new entity relationships between sales document and sales document line entities.</span></span>

<span data-ttu-id="236a4-110">由於現在可以使用查詢欄位來指示實體參照，保留舊版中相關實體 GUID 字串值的欄位已不再需要，因此已被取代。</span><span class="sxs-lookup"><span data-stu-id="236a4-110">Because lookup fields can now be used to indicate references to entities, the fields that held the string value of the GUID of the related entity in previous versions are no longer needed and therefore have been deprecated.</span></span> <span data-ttu-id="236a4-111">處理舊版字串欄位所定義之關聯的自訂用戶端及伺服器端程式碼也已被取代。</span><span class="sxs-lookup"><span data-stu-id="236a4-111">The custom client and server side code that handles the relationships defined by legacy string fields has also been deprecated.</span></span>

### <a name="entity-schema-changes"></a><span data-ttu-id="236a4-112">實體結構描述變更</span><span class="sxs-lookup"><span data-stu-id="236a4-112">Entity schema changes</span></span>
<span data-ttu-id="236a4-113">下表提供已取代字串欄位的一對一清單，以及實體的新查詢欄位。</span><span class="sxs-lookup"><span data-stu-id="236a4-113">The following table provides a one-to-one list of the deprecated string fields and the new lookup fields for the entities.</span></span> 

 <span data-ttu-id="236a4-114">實體</span><span class="sxs-lookup"><span data-stu-id="236a4-114">Entity</span></span> |   <span data-ttu-id="236a4-115">取代的欄位 (字串)</span><span class="sxs-lookup"><span data-stu-id="236a4-115">Deprecated field (String)</span></span> | <span data-ttu-id="236a4-116">新的欄位 (查詢)</span><span class="sxs-lookup"><span data-stu-id="236a4-116">New field (Lookup)</span></span>
--- | --- | ---
<span data-ttu-id="236a4-117">invoicedetail (發票明細)</span><span class="sxs-lookup"><span data-stu-id="236a4-117">invoicedetail (Invoice Line)</span></span> |  <span data-ttu-id="236a4-118">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="236a4-118">msdyn_contractline</span></span> |    <span data-ttu-id="236a4-119">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-119">msdyn_contractlineid</span></span>
<span data-ttu-id="236a4-120">msdyn_actual (實際值)</span><span class="sxs-lookup"><span data-stu-id="236a4-120">msdyn_actual (Actual)</span></span> | <span data-ttu-id="236a4-121">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="236a4-121">msdyn_salescontractline</span></span> |   <span data-ttu-id="236a4-122">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-122">msdyn_salescontractlineid</span></span>
<span data-ttu-id="236a4-123">msdyn_contractlineinvoiceschedule (專案合約服務內容發票清單)</span><span class="sxs-lookup"><span data-stu-id="236a4-123">msdyn_contractlineinvoiceschedule (Project Contract Line Invoice Schedule)</span></span> |    <span data-ttu-id="236a4-124">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="236a4-124">msdyn_contractline</span></span> |    <span data-ttu-id="236a4-125">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-125">msdyn_contractlineid</span></span>
<span data-ttu-id="236a4-126">msdyn_contractlinescheduleofvalue (專案合約服務內容里程碑)</span><span class="sxs-lookup"><span data-stu-id="236a4-126">msdyn_contractlinescheduleofvalue (Project Contract Line Milestone)</span></span> |   <span data-ttu-id="236a4-127">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="236a4-127">msdyn_contractline</span></span> |    <span data-ttu-id="236a4-128">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-128">msdyn_contractlineid</span></span>
<span data-ttu-id="236a4-129">msdyn_fact (事實)</span><span class="sxs-lookup"><span data-stu-id="236a4-129">msdyn_fact (Fact)</span></span> | <span data-ttu-id="236a4-130">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="236a4-130">msdyn_salescontractline</span></span> |   <span data-ttu-id="236a4-131">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-131">msdyn_salescontractlineid</span></span>
<span data-ttu-id="236a4-132">msdyn_invoicelinetransaction (發票明細詳細資料)</span><span class="sxs-lookup"><span data-stu-id="236a4-132">msdyn_invoicelinetransaction (Invoice Line Detail)</span></span> | <span data-ttu-id="236a4-133">msdyn_invoiceline</span><span class="sxs-lookup"><span data-stu-id="236a4-133">msdyn_invoiceline</span></span> <br> <span data-ttu-id="236a4-134">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="236a4-134">msdyn_salescontractline</span></span> | <span data-ttu-id="236a4-135">msdyn_invoicelineid</span><span class="sxs-lookup"><span data-stu-id="236a4-135">msdyn_invoicelineid</span></span> <br> <span data-ttu-id="236a4-136">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-136">msdyn_salescontractlineid</span></span>
<span data-ttu-id="236a4-137">msdyn_journalline (帳目明細)</span><span class="sxs-lookup"><span data-stu-id="236a4-137">msdyn_journalline (Journal Line)</span></span> |  <span data-ttu-id="236a4-138">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="236a4-138">msdyn_salescontractline</span></span> |   <span data-ttu-id="236a4-139">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-139">msdyn_salescontractlineid</span></span>
<span data-ttu-id="236a4-140">msdyn_orderlineresourcecategory (專案合約服務內容資源類別)</span><span class="sxs-lookup"><span data-stu-id="236a4-140">msdyn_orderlineresourcecategory (Project Contract Line Resource Category)</span></span> | <span data-ttu-id="236a4-141">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="236a4-141">msdyn_salescontractline</span></span> |   <span data-ttu-id="236a4-142">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-142">msdyn_contractlineid</span></span>
<span data-ttu-id="236a4-143">msdyn_orderlinetransaction (專案合約服務內容詳細資料)</span><span class="sxs-lookup"><span data-stu-id="236a4-143">msdyn_orderlinetransaction (Project Contract Line Detail)</span></span> | <span data-ttu-id="236a4-144">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="236a4-144">msdyn_salescontractline</span></span> |   <span data-ttu-id="236a4-145">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-145">msdyn_salescontractlineid</span></span>
<span data-ttu-id="236a4-146">msdyn_orderlinetransactioncategory (專案合約服務內容交易類別)</span><span class="sxs-lookup"><span data-stu-id="236a4-146">msdyn_orderlinetransactioncategory (Project Contract Line Transaction Category)</span></span> |   <span data-ttu-id="236a4-147">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="236a4-147">msdyn_contractline</span></span> |    <span data-ttu-id="236a4-148">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-148">msdyn_contractlineid</span></span>
<span data-ttu-id="236a4-149">msdyn_orderlinetransactionclassification (專案合約服務內容交易分類)</span><span class="sxs-lookup"><span data-stu-id="236a4-149">msdyn_orderlinetransactionclassification (Project Contract Line Transaction Classification)</span></span> |   <span data-ttu-id="236a4-150">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="236a4-150">msdyn_contractline</span></span> |    <span data-ttu-id="236a4-151">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="236a4-151">msdyn_contractlineid</span></span>
<span data-ttu-id="236a4-152">msdyn_quotelineinvoiceschedule (報價明細發票清單)</span><span class="sxs-lookup"><span data-stu-id="236a4-152">msdyn_quotelineinvoiceschedule (Quote Line Invoice Schedule)</span></span> |  <span data-ttu-id="236a4-153">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="236a4-153">msdyn_quoteline</span></span> |   <span data-ttu-id="236a4-154">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="236a4-154">msdyn_quotelineid</span></span>
<span data-ttu-id="236a4-155">msdyn_quotelineresourcecategory (報價明細資源類別)</span><span class="sxs-lookup"><span data-stu-id="236a4-155">msdyn_quotelineresourcecategory (Quote Line Resource Category)</span></span> |    <span data-ttu-id="236a4-156">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="236a4-156">msdyn_quoteline</span></span> |   <span data-ttu-id="236a4-157">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="236a4-157">msdyn_quotelineid</span></span>
<span data-ttu-id="236a4-158">msdyn_quotelinescheduleofvalue (報價明細里程碑)</span><span class="sxs-lookup"><span data-stu-id="236a4-158">msdyn_quotelinescheduleofvalue (Quote Line Milestone)</span></span> | <span data-ttu-id="236a4-159">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="236a4-159">msdyn_quoteline</span></span> |   <span data-ttu-id="236a4-160">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="236a4-160">msdyn_quotelineid</span></span>
<span data-ttu-id="236a4-161">msdyn_quotelinetransaction (報價明細詳細資料)</span><span class="sxs-lookup"><span data-stu-id="236a4-161">msdyn_quotelinetransaction (Quote Line Detail)</span></span> |    <span data-ttu-id="236a4-162">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="236a4-162">msdyn_quoteline</span></span> |   <span data-ttu-id="236a4-163">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="236a4-163">msdyn_quotelineid</span></span>
<span data-ttu-id="236a4-164">msdyn_quotelinetransactioncategory (報價明細交易類別)</span><span class="sxs-lookup"><span data-stu-id="236a4-164">msdyn_quotelinetransactioncategory (Quote Line Transaction Category)</span></span> |  <span data-ttu-id="236a4-165">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="236a4-165">msdyn_quoteline</span></span> |   <span data-ttu-id="236a4-166">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="236a4-166">msdyn_quotelineid</span></span>
<span data-ttu-id="236a4-167">msdyn_quotelinetransactionclassification (報價明細交易分類)</span><span class="sxs-lookup"><span data-stu-id="236a4-167">msdyn_quotelinetransactionclassification (Quote Line Transaction Classification)</span></span> |  <span data-ttu-id="236a4-168">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="236a4-168">msdyn_quoteline</span></span> |   <span data-ttu-id="236a4-169">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="236a4-169">msdyn_quotelineid</span></span>
<span data-ttu-id="236a4-170">SalesOrderDetail (訂單明細)</span><span class="sxs-lookup"><span data-stu-id="236a4-170">SalesOrderDetail (Order Line)</span></span> | <span data-ttu-id="236a4-171">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="236a4-171">msdyn_quotelineid</span></span> | <span data-ttu-id="236a4-172">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="236a4-172">msdyn_quoteline</span></span> 

### <a name="deprecated-custom-views-and-controls"></a><span data-ttu-id="236a4-173">取代的自訂檢視表與控制項</span><span class="sxs-lookup"><span data-stu-id="236a4-173">Deprecated custom views and controls</span></span>
<span data-ttu-id="236a4-174">下列自訂檢視表和控制項以及其相關成品，已被取代。</span><span class="sxs-lookup"><span data-stu-id="236a4-174">The following custom views and controls, and their related artifacts, have been deprecated.</span></span>

- <span data-ttu-id="236a4-175">可收費率檢視表。</span><span class="sxs-lookup"><span data-stu-id="236a4-175">Chargeability view.</span></span>
- <span data-ttu-id="236a4-176">在報價明細的 **專案資訊** 頁面上用於顯示報價明細詳細資料的自訂網格控制項。</span><span class="sxs-lookup"><span data-stu-id="236a4-176">Custom grid controls for showing quote line details on the **Project Information** page for the quote line.</span></span>
- <span data-ttu-id="236a4-177">在銷售訂單明細的 **專案資訊** 頁面上用於顯示專案合約服務內容詳細資料的自訂網格控制項。</span><span class="sxs-lookup"><span data-stu-id="236a4-177">Custom grid controls for showing project contract line details on the **Project Information** page for the sales order line.</span></span>

> [!NOTE]
> <span data-ttu-id="236a4-178">如需已被取代資源的完整清單，請參閱 [Project Service Automation v3.x 中已被取代的 Web 資源](../developer-guides/web-resources-deprecated-v3.x.md)</span><span class="sxs-lookup"><span data-stu-id="236a4-178">For the full list of deprecated resources, see [Deprecated Web resources in Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)</span></span>

## <a name="unified-client-interface-app-module"></a><span data-ttu-id="236a4-179">整合用戶端介面應用程式模組</span><span class="sxs-lookup"><span data-stu-id="236a4-179">Unified Client Interface App Module</span></span>
<span data-ttu-id="236a4-180">隨著整合用戶端介面 (UCI) 應用程式模組的推出，PSA 網站地圖項目已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="236a4-180">With the introduction of Unified Client Interface (UCI) App Modules, the PSA site map entries have been removed from the system.</span></span>  
<span data-ttu-id="236a4-181">由於與商機、報價、訂單、發票表單切換相關的功能因 UCI 應用程式模組僅包含 PSA 版本的表單而不再需要，該功能已被取代。</span><span class="sxs-lookup"><span data-stu-id="236a4-181">Functionality related to form switching for Opportunity, Quote, Order, Invoice has been deprecated as it is no longer required because the UCI App Module includes only PSA versions of the forms.</span></span>  

<span data-ttu-id="236a4-182">下列 Web 資源已被取代：</span><span class="sxs-lookup"><span data-stu-id="236a4-182">The following web resources have been deprecated:</span></span>

- <span data-ttu-id="236a4-183">msdyn_\SalesDocument\SalesDocumentFormLoader.js</span><span class="sxs-lookup"><span data-stu-id="236a4-183">msdyn_\SalesDocument\SalesDocumentFormLoader.js</span></span>
- <span data-ttu-id="236a4-184">msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js</span><span class="sxs-lookup"><span data-stu-id="236a4-184">msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js</span></span>

> [!NOTE]
> <span data-ttu-id="236a4-185">如需已被取代資源的完整清單，請參閱 [Project Service Automation v3.x 中已被取代的 Web 資源](../developer-guides/web-resources-deprecated-v3.x.md)。</span><span class="sxs-lookup"><span data-stu-id="236a4-185">For the full list of deprecated resources, see [Deprecated Web resources in Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]