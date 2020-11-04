---
title: 將專案估計值直接從 Project Service Automation 同步處理至 Finance and Operations
description: 本主題說明用於將專案工時估計與專案位於估計直接從 Microsoft Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073124"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>將專案估計值直接從 Project Service Automation 同步處理至 Finance and Operations

[!include[banner](../includes/banner.md)]

本主題說明用於將專案工時估計與專案費用估計直接從 Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。

> [!NOTE]
> - 專案工作整合、費用交易類別、工時估計、費用估計和功能鎖定可在 8.0 版中使用。
> - 實際值整合可在 8.0.1 版或更新版本中使用。

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation 至 Finance 的資料流程

Project Service Automation 至 Finance 整合解決方案會使用資料整合功能，跨 Project Service Automation 與 Finance 的執行個體來同步處理資料。 可與資料整合功能搭配使用的整合範本會啟用有關專案工時估計與專案費用估計從 Project Service Automation 到 Finance 的資料流程。

下圖這些顯示如何在 Project Service Automation 與 Finance 之間同步處理資料。

[![Project Service Automation 與 Finance 整合的資料流程](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>專案工時估計

### <a name="template-and-tasks"></a>範本與工作

若要存取可用範本，請在 Microsoft Power Apps 系統管理中心選取 **專案** ，然後選取右上角的 **新增專案** 以選取公用範本。

下列範本與基礎工作會用來將專案工時估計從 Project Service Automation 同步處理至 Finance：

- **資料整合中範本的名稱：** 專案工時估計 (PSA 至 Fin 和 Ops)
- **專案中工作的名稱：**

    - 交易關聯
    - 費用估計值

### <a name="entity-set"></a>實體集

| Project Service Automation | 財務                                       |
|----------------------------|-----------------------------------------------|
| 專案工作              | 專案工時估計的整合實體 |

### <a name="entity-flow"></a>實體流程

專案工時估計是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案工時預測。

### <a name="prerequisites"></a>先決條件

進行專案工時估計之前，您必須同步處理專案、專案工作和專案費用交易類別。

### <a name="power-query"></a>Power Query

在專案工時估計範本中，您必須使用 Microsoft Power Query for Excel 來完成這些工作：

- 設定整合建立新工時預測時，將使用的預設預測模型識別碼。
- 在會讓工時預測中整合失敗的工作中，篩除任何資源特定記錄。
- 篩除任何空白交易類別列。 未能完成此工作可能會造成不正確的工時預測。

#### <a name="set-the-default-forecast-model-id"></a>設定預設預測模型識別碼

若要更新範本中的預設預測模型識別碼，請按一下 **對應** 箭頭以開啟對應。 然後選取 **進階查詢及篩選** 連結。

- 如果您使用預設「專案工時估計 (PSA 至 Fin 和 Ops)」範本，請選取 **已套用的步驟** 清單中的 **插入的條件** 。 在 **函數** 項目中，將 **O\_forecast** 取代為應與整合搭配使用的預測模型識別碼。 預設範本具有示範資料中的預測模型識別碼。
- 如果您要建立新範本，就必須新增此欄。 在 Power Query 中，選取 **新增條件欄** ，並輸入新欄的名稱，例如 **ModelID** 。 輸入該欄的條件，如果專案工作不是 Null，則為 \<enter the forecast model ID\>；否則為 Null。

#### <a name="filter-out-resource-specific-records"></a>篩除資源特定記錄

「專案工時估計 (PSA 至 Fin 和 Ops)」範本有一個會移除任何資源特定記錄的預設篩選。 如果您自行建立範本，就必須新增此篩選。 選取 **進階查詢及篩選** 連結以篩選 **msdyn\_islinetask** 欄，這樣就只會包含 **否** 記錄。

#### <a name="filter-out-empty-transaction-category-rows"></a>篩除空白交易類別列

您必須新增篩選，以移除任何具有空白交易類別的列。 不論您是使用預設範本還是自行建立範本，此工作都是必要工作。 此篩選會從 Project Service Automation 中移除任何可能會在 Finance 中造成工時預測不正確的摘要列。 選取 **進階查詢及篩選** 連結，以篩除 **msdyn\_transactioncategory\_value** 欄中的 Null 記錄。

### <a name="template-mapping-in-data-integration"></a>資料整合中的範本對應

下圖顯示資料整合中的範本工作對應範例。 此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。

[![資料整合中的範本工作對應](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>專案費用估計

### <a name="template-and-tasks"></a>範本與工作

下列範本與基礎工作會用來將專案費用估計從 Project Service Automation 同步處理至 Finance：

- **資料整合中範本的名稱：** 專案費用估計 (PSA 至 Fin 和 Ops)
- **專案中工作的名稱：**

    - 交易關聯 
    - 費用估計值

### <a name="entity-set"></a>實體集

| Project Service Automation | 財務                                                  |
|----------------------------|----------------------------------------------------------|
| 交易人脈    | 專案交易關聯的整合實體 |
| 估計明細             | 專案費用估計的整合實體         |

### <a name="entity-flow"></a>實體流程

專案費用估計是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案費用預測。

### <a name="prerequisites"></a>先決條件

進行專案費用估計之前，您必須同步處理專案、專案工作和專案費用交易類別。

### <a name="power-query"></a>Power Query

在專案費用估計範本中，您必須使用 Power Query 來完成下列工作：

- 篩選成僅包含費用估計明細記錄。
- 設定整合建立新工時預測時，將使用的預設預測模型識別碼。
- 轉換帳單類型。
- 轉換交易類型。

#### <a name="filter-to-include-only-expense-estimate-lines"></a>篩選成僅包含費用估計明細

「專案費用估計 (PSA 至 Fin 和 Ops)」範本有一個只會將費用明細包含在整合中預設篩選。 如果您自行建立範本，就必須新增此篩選。 選取 **交易關聯** 工作，然後按一下 **對應** 箭頭以開啟對應。 選取 **進階查詢及篩選** 連結。 篩選 **msdyn\_transactiontype1** 欄，使其僅包含 **msdyn\_estimateline** 。

#### <a name="set-the-default-forecast-model-id"></a>設定預設預測模型識別碼

若要更新範本中的預設預測模型識別碼，請選取 **費用估計** 工作，然後按一下 **對應** 箭頭以開啟對應。 選取 **進階查詢及篩選** 連結。

- 如果您使用預設「專案費用估計 (PSA 至 Fin 和 Ops)」範本，請在 Power Query 中，從 **已套用的步驟** 區段中選取第一個 **插入的條件** 。 在 **函數** 項目中，將 **O\_forecast** 取代為應與整合搭配使用的預測模型識別碼。 預設範本具有示範資料中的預測模型識別碼。
- 如果您要建立新範本，就必須新增此欄。 在 Power Query 中，選取 **新增條件欄** ，並輸入新欄的名稱，例如 **ModelID** 。 輸入該欄的條件，如果估計明細識別碼不是 Null，則為 \<enter the forecast model ID\>；否則為 Null。

#### <a name="transform-the-billing-types"></a>轉換帳單類型

「專案費用估計 (PSA 至 Fin 和 Ops)」範本包含一個用來轉換整合期間從 Project Service Automation 所收到帳單類型的條件欄。 如果您自行建立範本，就必須新增此條件欄。 選取 **進階查詢及篩選** 連結，然後選取 **新增條件欄** 。 輸入新欄的名稱，例如 **BillingType** 。 接著輸入下列條件︰

如果 **msdyn\_billingtype** = 192350000，則為 **NonChargeable**  
否則如果 **msdyn\_billingtype** = 192350001，則為 **Chargeable**  
否則如果 **msdyn\_billingtype** = 192350002，則為 **免費贈送**  
否則為 **NotAvailable**

#### <a name="transform-the-transaction-types"></a>轉換交易類型

「專案費用估計 (PSA 至 Fin 和 Ops)」範本包含一個用來轉換整合期間從 Project Service Automation 所收到交易類型的條件欄。 如果您自行建立範本，就必須新增此條件欄。 選取 **進階查詢及篩選** 連結，然後選取 **新增條件欄** 。 輸入新欄的名稱，例如 **TransactionType** 。 接著輸入下列條件︰

如果 **msdyn\_transactiontypecode** = 192350000，則為 **成本**  
否則如果 **msdyn\_transactiontypecode** = 192350005，則為 **銷售**  
否則為 **Null**

### <a name="template-mapping-in-data-integration"></a>資料整合中的範本對應

下圖顯示資料整合中的範本工作對應範例。 此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。

[![費用評估交易的範本對應](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![費用估計值的範本對應](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
