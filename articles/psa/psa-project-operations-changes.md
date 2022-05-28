---
title: 從 Project Service Automation 到 Project Operations 的功能變更
description: 本主題提供從 Project Service Automation 到 Dynamics 365 Project Operations 的功能變更概觀。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7e41b381d6da267f58174305f33fc229c66cd7b7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595396"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>從 Project Service Automation 到 Project Operations 的功能變更

從 Dynamics 365 Project Service Automation 至 Dynamics 365 Project Operations 精簡版的升級分三個階段提供。 本主題提供有關完成升級時預期可看到的主要變更的資訊。

| 升級傳遞 | 階段 1 <br>(2022 年 1 月) | 階段 2 <br>(2022 年 4 月浪潮) | 階段 3  |
|------------------|------------------------|---------------------------|---------------------------|
| 對專案的分工結構圖 (WBS) 沒有相依性。 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| 在 Project Operations 目前支援的限制中包括 WBS。 | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
|  在 Project Operations 目前所支援之限制 (包括對 Project Desktop Client 的支援) 以外的 WBS。 | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>專案管理

使用者體驗中最重大的變更將會在專案規劃範圍中。 Project Operations 採用新的新式體驗，以運用 [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) 提供的排程功能來管理分工結構圖 (WBS) 。

## <a name="differences-in-the-scheduling-experience"></a>排程體驗的差異

下表摘要 Project Service Automation 與 Project Operations 之間的排程差異。

|  正在排程     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| 專案範本 - 可以在建立專案時定義和套用專案範本  |  &nbsp;    | :heavy_check_mark: |
| 專案分工結構圖 (WBS) 與桌面用戶端整合   |    &nbsp;  | :heavy_check_mark: |
| 限制式 - 開始時間不早於、完成時間不晚於  | :heavy_check_mark: |   &nbsp;  |
| 里程碑 - 期間為零的工作   | :heavy_check_mark:  |  &nbsp;  |
| 資源導向工作會考慮已指派資源的可用性   | :heavy_check_mark: |  &nbsp;    |
| 分時期編輯 - 每天編輯方案和工作   |   &nbsp;  | :heavy_check_mark: |
| 自動/手動排程 - 使用專案排程引擎自動或手動排程工作 |  &nbsp; | :heavy_check_mark:  |
| 直接在使用者介面中編輯大型專案：不限制可編輯的方案的大小  | 500 個工作限制  | :heavy_check_mark:       |
| 完成百分比 - 標示記工作進度   | :heavy_check_mark:  |  &nbsp;  |
| [專案排程模式](../project-management/scheduling-modes.md) - 將專案定義為固定單位、固定投入或固定期間 | :heavy_check_mark: | &nbsp; |
| 時間表 - 建置和自訂時間表檢視表，以具體呈現排程詳細資料，並與利害關係人溝通。 | :heavy_check_mark:  | &nbsp; |
| 投入導向工作 - 排程引擎支援將工作排定為投入導向  | :heavy_check_mark:  | &nbsp; |
| **工作資訊** 對話方塊 - 使用對話方塊儲存工作詳細資料 | :heavy_check_mark:  |  &nbsp;  |
| 拖放功能 - 多重選取工作並修改其在 WBS 上位置 | :heavy_check_mark: | &nbsp;  |
| 彈性持續檢視表 - 定義更細微的工作屬性檢視表   | :heavy_check_mark:  | &nbsp; |
| 排序和篩選 WBS  | :heavy_check_mark:  | &nbsp; |
| 非瀑布式專案交付的 Boards 檢視表  | :heavy_check_mark:   | &nbsp; |
| 時間表檢視 - 用於視覺化和編輯 WBS 的互動式甘特圖   | :heavy_check_mark:  | &nbsp; |
| 鍵盤快速鍵 - 使用鍵盤快速鍵進行一般操作，例如縮排或插入  | :heavy_check_mark:  |  &nbsp; |
| 多層級復原 - 執行假設狀況分析，藉由反轉和重新套用整組操作，充分了解變更產生的影響 | :heavy_check_mark: | &nbsp; |
| 剪下/複製/貼上 - 在應用程式間複製並貼上排程詳細資料，以在排程開發上進行共同作業  | :heavy_check_mark: | &nbsp; |
| 工作檢查清單 - 將最多達 20 個的檢查清單項目新增至工作   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>專案規劃

與 Project Service Automation 中的 **專案** 頁面相比，Project Operations 中的 **專案** 頁面有大量差異。

在第 1 階段升級過程中，下列動作已從 **專案** 頁面中移除：

  - **在 MS Project 中開啟**
  - **建立範本**
  - **與 MS Project 取消連結**

Project Operations 中的 **專案** 頁面包含下列新的索引標籤。

- **材料估計值**
- **工作帳單設定**

**狀態** 索引標籤已移除，且 **狀態** 欄位現在位於使用專案的排程模式的 **摘要** 索引標籤上。

   ![[專案] 頁面的更新。](media/projectform.png)

**排程** 索引標籤已重新命名為 **工作** 索引標籤，並使用 Project for the Web 提供新的專案規劃體驗。

   ![新的專案工作索引標籤。](media/tasktab.png)

## <a name="scheduling-modes"></a>排程模式

Project Operations 已引進新功能[排程模式](../project-management/scheduling-modes.md)。 所有現有的 Project Service Automation 專案都會在 Project Operations 中預設為 **固定期間**。 不過，可以移至 **設定** > **參數** > **參數** > **排程模式** 來管理新專案的預設值。

   ![排程模式的專案參數設定。](media/projectparameter.png)

## <a name="project-planning-limits"></a>專案規劃限制

Project Operations 需要使用 Project for the Web 來進行所有專案排程作業。 Project for the Web 使用下表中的限制來管理分工結構圖。

| **欄位**                                          | **限制**             |
|----------------------------------------------------|-----------------------|
| 專案的工作總數上限                  | 500                   |
| 專案的總期間上限               | 3650 天 (10 年)  |
| 專案的資源總數上限              | 300                   |
| 專案的連結總數 (僅限後續任務) 上限 | 600                   |
| 專案的自訂欄位總數上限          | 10                    |
| 最大階層層級                            | 10 層             |
| 連結數上限 (後續任務 + 前置任務)            | 20                    |
| 分葉工作的最大期間                      | 1250 天             |
| 摘要工作的最大期間                 | 3650 天 (10 年)  |
| 指派給工作的資源數上限               | 20 個資源          |
| 工作的支援日期範圍                    | 2000/1/1 - 2149/12/31 |
| 檢查清單項目                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>專案規劃擴充性與開發

升級至 Project Operations 之後，您必須使用專案排程 API 對下列實體執行建立、更新和刪除作業：

|   實體名稱           |   實體邏輯名稱       |
|-------------------------|-----------------------------|
| 專案                 | msdyn_project               |
| 專案工作            | msdyn_projecttask           |
| 專案工作相依性 | msdyn_projecttaskdependency |
| 資源指派     | msdyn_resourceassignment    |
| 專案貯體          | msdyn_projectbucket         |
| 專案團隊成員     | msdyn_projectteam           |

如果您目前有涉及這些實體的自訂，請參閱[使用專案排程 API 對排程實體執行作業](../project-management/schedule-api-preview.md)。

## <a name="data-model-changes"></a>資料模型變更

在升級階段 1 中，資料模型有所變更。 這些變更主要是對現有實體的欄位變更。 在階段 1 中，實體 **msydn_project** 和 **msdyn_projectteam** 是對自訂的重構。 

> [!IMPORTANT]
> 當未來升級階段完成時，此區段還會以其他的實體來更新。

下列欄位已取代為新的欄位。

|   Entity          |   舊的邏輯名稱   |   新的邏輯名稱    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

已新增下列欄位。

|   Entity          |   邏輯名稱                               |   名稱 |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | 顯示專案的實際費用銷售彙總值。 僅用於 Project Service Automation。 |
| msdyn_project     | msdyn_actualmaterialcost                     | 顯示專案的實際材料成本彙總值。 僅用於 Project Service Automation。 |
| msdyn_project     | msdyn_actualmaterialsales                    | 顯示專案的實際材料銷售彙總值。 僅用於 Project Service Automation。 |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | 與此專案相關聯的合約服務內容。 |
| msdyn_project     | msdyn_copyprojectcorrelationid               | 這是用於與相互關聯識別碼相關之 **專案複製** 的內部系統欄位。 僅用於 Project Service Automation。 |
| msdyn_project     | msdyn_copyprojectsessionid                   | 這是用於與工作階段識別碼相關之 **專案複製** 的內部系統欄位。 僅用於 Project Service Automation。 |
| msdyn_project     | msdyn_globalrevisiontoken                    | 專案排程服務的上次同步 xRM 全域修訂代用文字。 |
| msdyn_project     | msdyn_msprojectdocument                      | 屬於專案的 Microsoft Project 文件。 |
| msdyn_project     | msdyn_plannedmaterialcost                    | 專案的計劃材料成本彙總值。 僅用於 Project Service Automation。 |
| msdyn_project     | msdyn_plannedmaterialsales                   | 專案的計劃材料銷售彙總值。 僅用於 Project Service Automation。 |
| msdyn_project     | msdyn_program                                | 與此專案相關的方案。 |
| msdyn_project     | msdyn_quotelineproject                       | 與此專案相關聯的報價明細。 |
| msdyn_project     | msdyn_replaylogheader                        | 重新執行記錄的標題。 |
| msdyn_project     | msdyn_schedulemode                           | 用於專案上所有工作的預設排程模式。  |
| msdyn_project     | msdyn_taskearlieststart                      | 專案中任何工作的最早開始日期。  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | 從其中複製此專案團隊成員的來源專案團隊成員。 |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | 指示是否要為新建立的一般團隊成員建立資源需求。  |
| msdyn_projectteam | msdyn_deletestatus                           | 團隊成員的刪除狀態，用來追蹤是否有傳送至專案排程服務的刪除要求，以及此服務是否已在預期的時間範圍內成功傳送回覆。 |
| msdyn_projectteam | msdyn_effortcompleted                        | 追蹤團隊成員已對其工作指派完成的投入。 |
| msdyn_projectteam | msdyn_effortremaining                        | 追蹤團隊成員對其工作指派尚未完成的投入。 |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | 從團隊成員傳送刪除要求至專案排程服務開始，直到 Microsoft Dataverse 中實際刪除此團隊成員為止的等待期間。|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | 用於記錄何將團隊成員刪除要求傳送至專案排程服務的時間戳記。 |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | 顯示從其中複製此專案團隊成員的來源專案團隊成員。  |

## <a name="project-templates"></a>專案範本

Project Operations 不提供對專案範本的支援。 不過，您可以使用[專案複製 API](../project-management/dev-copy-project.md) 來複製大部分核心功能。

## <a name="desktop-add-in-support"></a>桌面增益集支援

升級的前兩個階段沒有提供對 Microsoft Project 桌面增益集的支援。 在階段 3 中，專案數大於 Project for the Web 目前支援的限制的客戶，將可以使用桌面增益集。

## <a name="editing-resource-assignment-contours"></a>編輯資源指派分佈

第 2 階段的升級推出時，將可使用編輯資源指派分佈的功能。

## <a name="billing-and-pricing"></a>帳單和定價

Project Operations 中已新增下列新功能。 這些功能實際上是附加的，不會影響 Project Service Automation 資料模型。

- [記錄專案和專案工作的材料使用方式](../material/material-usage-log.md)
- [轉包合約管理](../pro/subcontracting/managing-subcontracts-overview.md)
- [預付金或定額保留後隨用即扣型合約](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [合約不得超過狀態和驗證](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [工作型帳單](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>已取代元件

下表記載所有在升級後移到已取代元件解決方案的被取代欄位。 如需詳細資訊以及解決方案的連結，請參閱 [Dynamics 365 Project Service Automation 3x 至 Project Operations 4x 的已取代元件](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution)。

### <a name="invoicedetail"></a>invoicedetail

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| 欄位​​                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

