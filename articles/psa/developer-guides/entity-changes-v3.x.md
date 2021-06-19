---
title: 實體、控制項和使用者介面變更 (Project Service Automation 3.x)
description: 本主題說明 Microsoft Dynamics Project Service Automation 3.x 中的解決方案變更。
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e3d6f515cec51cb30f83ff22a14ecb125dc81214
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007941"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>實體、控制項和使用者介面變更 (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Microsoft Dynamics Project Service Automation (PSA) 3.x 發行後，實體、控制項、檢視表和使用者介面已發生許多變更。 本主題提供有關這些重要變更的資訊。

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>銷售文件、銷售文件明細、銷售文件明細詳細資料實體的上下層關聯
在版本 3.0 之前發行的 Dynamics 365 Project Service Automation (PSA) 版本中，銷售文件、銷售文件明細、銷售文件明細詳細資料實體之間的部分關聯是透過保存相關實體 GUID 之字串表示法的字串欄位來實作。 這是因為平台的限制，要求解決方案伺服器端及用戶端上必須有大量自訂程式碼，才能讓這些關聯運作起來仿如一般 Dynamics CRM 實體關聯，以及讓字串欄位作用起來像查詢欄位那樣。

PSA 3.0 已更新為運用銷售文件與銷售文件明細實體之間的新實體關聯。

由於現在可以使用查詢欄位來指示實體參照，保留舊版中相關實體 GUID 字串值的欄位已不再需要，因此已被取代。 處理舊版字串欄位所定義之關聯的自訂用戶端及伺服器端程式碼也已被取代。

### <a name="entity-schema-changes"></a>實體結構描述變更
下表提供已取代字串欄位的一對一清單，以及實體的新查詢欄位。 

 實體 |   取代的欄位 (字串) | 新的欄位 (查詢)
--- | --- | ---
invoicedetail (發票明細) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (實際值) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (專案合約服務內容發票清單) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (專案合約服務內容里程碑) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (事實) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (發票明細詳細資料) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (帳目明細) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (專案合約服務內容資源類別) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (專案合約服務內容詳細資料) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (專案合約服務內容交易類別) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (專案合約服務內容交易分類) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (報價明細發票清單) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (報價明細資源類別) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (報價明細里程碑) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (報價明細詳細資料) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (報價明細交易類別) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (報價明細交易分類) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (訂單明細) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>取代的自訂檢視表與控制項
下列自訂檢視表和控制項以及其相關成品，已被取代。

- 可收費率檢視表。
- 在報價明細的 **專案資訊** 頁面上用於顯示報價明細詳細資料的自訂網格控制項。
- 在銷售訂單明細的 **專案資訊** 頁面上用於顯示專案合約服務內容詳細資料的自訂網格控制項。

> [!NOTE]
> 如需已被取代資源的完整清單，請參閱 [Project Service Automation v3.x 中已被取代的 Web 資源](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>整合用戶端介面應用程式模組
隨著整合用戶端介面 (UCI) 應用程式模組的推出，PSA 網站地圖項目已從系統中移除。  
由於與商機、報價、訂單、發票表單切換相關的功能因 UCI 應用程式模組僅包含 PSA 版本的表單而不再需要，該功能已被取代。  

下列 Web 資源已被取代：

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> 如需已被取代資源的完整清單，請參閱 [Project Service Automation v3.x 中已被取代的 Web 資源](../developer-guides/web-resources-deprecated-v3.x.md)。




[!INCLUDE[footer-include](../../includes/footer-banner.md)]