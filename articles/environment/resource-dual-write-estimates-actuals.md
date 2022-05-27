---
title: 專案估計值和實際值整合
description: 本主題提供有關 Project Operations 雙重寫入專案估計值與實際值整合的資訊。
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5aaa59020427438fa6ebab3789fbb70c5b86e272
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577180"
---
# <a name="project-estimates-and-actuals-integration"></a>專案估計值和實際值整合

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本主題提供有關 Project Operations 雙重寫入專案估計值與實際值整合的資訊。

## <a name="project-estimates"></a>專案估計值

專案人力、費用和材料估計值是在 Microsoft Dataverse 中所建立和維護，並同步處理至財務和營運應用程式以作會計用途。 不支援透過財務和營運應用程式建立、更新和刪除作業。

建立估計值需要專案的有效會計設定。 與合約服務內容相關的專案在專案成本和營收設定檔規則中必須已定義有效的專案成本和營收設定檔。 如需詳細資訊，請參閱[設定計費專案會計](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules)。

## <a name="labor-estimates"></a>人力估計值

人力估計值是由同樣將一般或具名資源指派給專案工作的專案經理或資源管理員所建立。 您可以在 Dataverse 中 **專案詳細資料** 頁面的 **資源指派** 索引標籤上檢閱資源指派記錄。 Dataverse 的資源指派記錄會使用 **Project Operations 整合實體，在財務和營運應用程式中建立工時估計值的工時預測記錄 (msdyn\_resourceassignments)**。

   ![人力估計值整合。](./Media/DW4LaborEstimates.png)

雙重寫入會將資源指派記錄同步處理至臨時表格 (**ProjCDSEstimateHoursImport**)，然後使用商務規則來建立和更新時數預測記錄 (**ProjForecastEmpl**)。

專案會計師會審查財務和營運應用程式中所建立的趨勢預測工時記錄，方法是移至 **專案管理與會計** > **所有專案** > **方案** > **工時預測**。

## <a name="expense-estimates"></a>費用估計值

費用估計值是由專案經理在 Dataverse 中 **專案詳細資料** 頁面的 **費用估計值** 索引標籤上所建立。 費用估計值記錄會儲存在 Dataverse 的 **估計明細** 實體中。 這些估計記錄有 **費用** 交易類別，並使用 **費用估計值 (msdyn\_estimatelines) 的 Project Operations 整合實體** 同步處理至財務和營運應用程式中的費用預測記錄。

   ![費用估計值整合。](./Media/DW4ExpenseEstimates.png)

雙重寫入會將費用估計記錄同步處理至臨時表格 (**ProjCDSEstimateExpenseImport**)，然後使用商務規則來建立和更新費用預測記錄 (**ProjForecastCost**)。 估計明細會分別儲存銷售估計和成本估計記錄。 財務和營運應用程式中的商務規則會使用暫存資料表中的這項詳細資料填入單一費用預測記錄。

專案會計師可以審查財務和營運應用程式中的費用預測記錄，方法是移至 **專案管理與會計** > **所有專案** > **方案** > **費用預測**。

## <a name="material-estimates"></a>材料估計值

費用估計值是由專案經理在 Dataverse 中 **專案詳細資料** 頁面的 **材料估計值** 索引標籤上所建立。 材料估計值記錄會儲存在 Dataverse 的 **估計明細** 實體中。 這些估計記錄有 **材料** 交易類別，並使用 **材料估計值 (msdyn\_estimatelines) 的專案整合資料表** 同步處理至財務和營運應用程式中的項目預測記錄。

   ![材料估計值整合。](./Media/DW4MaterialEstimates.png)

雙重寫入會將材料估計記錄同步處理至臨時表格 **ProjForecastSalesImpor**，然後使用商務規則來建立和更新項目預測記錄 (**ForecastSales**)。 估計明細會分別儲存銷售估計和成本估計記錄。 財務和營運應用程式中的商務規則會使用暫存資料表中的這項詳細資料填入單一項目預測記錄。

專案會計師可以審查財務和營運應用程式中的項目預測記錄，方法是移至 **專案管理與會計** > **所有專案** > **方案** > **項目預測**。

## <a name="project-actuals"></a>專案實際值

專案實際值是在 Dataverse 中根據時間、費用、材料和帳務活動所建立。 這些交易的所有營運屬性 (包括數量、成本價、銷售價和專案) 都是在此 Dataverse 實體中擷取。 如需詳細資訊，請參[實際值](../actuals/actuals-overview.md)。 實際記錄是使用下游會計的雙重寫入資料表對應 **Project Operations 整合實際值 (msdyn\_actuals)** 來同步處理至財務和營運應用程式。

   ![實際值整合。](./Media/DW4Actuals.png)

**Project Operations 整合實際值** 資料表對應會在 **略過同步處理 (僅供內部使用)** 屬性設定為 **False** 的情況下，同步處理 Dataverse 中 **實際值** 實體的所有資料。 建立記錄時，Dataverse 會自動設定此屬性值。 此屬性設定為 **True** 的範例如下：

  - 公司間交易的專案成本實際值。 如需詳細資訊，請參閱[建立公司間交易](../project-accounting/create-intercompany-transactions.md)。 因為過帳公司間廠商發票時，系統會在財務和營運應用程式中重新建立專案成本實際值，所以會略過這些記錄。
  - 確認預估發票時建立負數的未開單銷售記錄。 因為財務和營運應用程式中的專案明細分類帳未在開立發票時沖回未開單銷售記錄，但是會將狀態變更為已完整開立發票，所以略過這些記錄。

雙重寫入資料表對應會將實際值記錄同步處理至臨時表格 **ProjCDSActualsImport**。 這些記錄會在建立 Project Operations 整合帳目明細和專案發票提案明細時，由定期程序 **從臨時表格匯入** 進行處理。 如需詳細資訊，請參閱 [Project Operations 中的整合帳目](../project-accounting/project-operations-integration-journal.md)。

Dataverse 還會擷取 **交易關係** 實體中專案實際交易之間的連結。 如需詳細資訊，請參閱[將實際值連結至原始記錄](../actuals/linkingactuals.md)。 實際交易之間的連結也會使用雙重寫入資料表對應 **專案交易關聯性整合實體 (msdyn\_transactionconnections)** 同步處理至財務和營運應用程式。 建立 Project Operations 整合帳目明細和專案發票提案明細時，定期程序 **從臨時表格匯入** 會使用這些記錄。

過帳 Project Operations 整合帳目和專案發票提案會觸發各自在臨時表格 **ProjCDSActualsImport** 中的記錄。 系統會擷取並記錄實際值交易的下列會計屬性：

- 會計貨幣金額
- 匯率
- 憑單號碼
- 銷售稅金額

**Project Operations 整合實際值** 資料表對應會使用此資訊更新各自在 Dataverse 中的實際值記錄。
