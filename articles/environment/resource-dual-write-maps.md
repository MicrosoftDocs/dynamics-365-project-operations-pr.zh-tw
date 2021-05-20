---
title: Project Operations 雙重寫入對應版本
description: 本主題提供 Dynamics 365 Project Operations 所需的雙重寫入對應清單。
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938956"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations 雙重寫入對應版本

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

使用資源/非庫存案例適用的 Dynamics 365 Project Operations 時，必須有一組雙重寫入對應，才能在環境中執行。 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>必要的對應：雙重寫入協調流程解決方案

下列對應是 Project Operations 解決方案的必要先決條件。 請務必在環境中執行下表中所列的對應，以及任何相關的資料表對應。

| 資料表對應 | 初始同步 |
| --- | --- |
| 分類帳 (msdyn_ledgers) | 需要對資料表對應和所有先決條件進行初始同步。 初始同步的主機是 Finance and Operations 應用程式。 |
| 法律實體 (cdm_companies) | 非必要。 使用雙重寫入連結環境時，系統會自動填入此實體。 |
| 客戶 V3 (帳戶) | 佈建時不需要。 |
| 廠商 V2 (msdyn_vendors) | 佈建時不需要。 |

1. 從對應清單中選取與所有先決條件的總帳 **(msdyn\_ledgers)** 對應，然後選取 **初始同步** 核取方塊。 在 **初始同步主機** 欄位中，為總帳對應以及所有必要的對應選取 **Finance and Operations**。 選取 **執行**。

![總帳對應同步處理](media/DW6.png)

1. 對上表列出的其餘所有資料表對應，執行相同的步驟。 執行這些對應時，不要選取 **初始同步** 核取方塊。

## <a name="project-operations-dual-write-maps"></a>Project Operations 雙重寫入對應

下列對應是 Project Operations 解決方案的必要對應。

| **實體對應** | **最新版本** | **初始同步** |
| --- | --- | --- |
| 專案交易關聯的整合實體 (msdyn\_transactionconnections) | 1.0.0.0 | 佈建時不需要。 |
| 專案合約標題 (銷售訂單) | 1.0.0.1 | 佈建時不需要。 |
| 專案合約服務內容 (salesorderdetails) | 1.0.0.0 | 佈建時不需要。 |
| 專案資金來源 (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | 佈建時不需要。 |
| Project Operations 材料估計值整合資料表 (msdyn\_estimatelines) | 1.0.0.0 | 佈建時不需要。 |
| 專案發票提案 V2 (發票) | 1.0.0.2 | 佈建時不需要。 |
| Project Operations 整合實際值 (msdyn_actuals) | 1.0.0.14 | 佈建時不需要。 |
| Project Operations 整合合約服務內容里程碑 (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | 佈建時不需要。 |
| 費用估計值的 Project Operations 整合實體 (msdyn_estimateslines) | 1.0.0.2 | 佈建時不需要。 |
| 時數估計值的 Project Operations 整合實體 (msdyn_resourceassignments) | 1.0.0.5 | 佈建時不需要。 |
| Project Operations 整合專案費用類別匯出實體 (msdyn_expensecategories) | 1.0.0.2 | 佈建時不需要。 |
| Project Operations 整合專案費用匯出實體 (msdyn_expenses) | 1.0.0.2 | 佈建時不需要。 |
| Project Operations 整合專案廠商發票匯出實體 (msdyn_projectvendorinvoices) | 1.0.0.0 | 佈建時不需要。 |
| Project Operations 整合專案廠商發票明細匯出實體 (msdyn_projectvendorinvoicelines) | 1.0.0.0 | 佈建時不需要。 |
| 所有公司的專案資源角色 (bookableresourcecategories) | 1.0.0.1 | 資料表對應必須進行初始同步，才能同步處理佈建時在 Dynamics 365 Dataverse 環境中填入的專案經理和團隊成員資源角色。 Dataverse 是初始同步處理的主要來源。 |
| 專案工作 (msdyn_projecttasks) | 1.0.0.4 | 佈建時不需要。 |
| 專案交易類別 (msdyn_transactioncategories) | 1.0.0.0 | 佈建時不需要。 |
| 專案 V2 (msdyn_projects) | 1.0.0.1 | 佈建時不需要。 |

完成下列步驟以執行列出的對應。

1. 啟用專案資源角色的 **所有公司 (bookableresourcecategories)** 資料表對應，因為此對應需要初始同步。在 **初始同步主機** 欄位中選取 **Common Data Service**。 

 ![資源角色資料表對應同步](media/6ResourceInitialSync.jpg)

 等到對應的狀態變成 **執行中** 之後，再移至下一個步驟。

2. 選取其餘所有的必要對應。 您可以右上角的搜尋中使用關鍵字 **專案**，在雙重寫入對應清單中篩選這些對應。 您可以多重選取所有對應，然後執行。 如需詳細資訊，請參閱[管理多個資料表對應](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps)。 請務必另行啟用並執行相關的實體對應。

### <a name="project-operations-dual-write-map-versions"></a>Project Operations 雙重寫入對應版本

在您的環境中一定要執行最新的對應版本。 如有下列任一情形，特定功能可能無法正確運作：

- 未啟用某個對應。
- 未啟用最新版本的對應。 
- 未啟用相關的資料表格對應。

您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 您可以選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本來啟用新的對應版本。 如果您已對現成可用的資料表對應進行自訂，就需要重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。
