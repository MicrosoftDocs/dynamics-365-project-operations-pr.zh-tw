---
title: 同步處理 Finance and Operations 與 Project Service Automation 之間的專案費用類別
description: 本主題說明用於同步處理 Microsoft Dynamics 365 Finance 與 Dynamics 365 Project Service Automation 之間的專案費用類別的範本和基礎工作。
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073135"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>同步處理 Finance and Operations 與 Project Service Automation 之間的專案費用類別

[!include[banner](../includes/banner.md)]

本主題說明用於同步處理 Dynamics 365 Finance 與 Dynamics 365 Project Service Automation 之間的專案費用類別的範本和基礎工作。

> [!NOTE]
> - 專案工作整合、費用交易類別、工時估計、費用估計和功能鎖定可在 8.0 版中使用。
> - 實際值整合可在 8.0.1 版或更新版本中使用。
> - 如果您使用的是 Enterprise Edition 7.3.0，則安裝 KB 4132657 和 KB 4132660 之後，您就可以使用範本來整合專案工作、費用交易類別、工時估計、費用估計與實際值，以及設定功能鎖定。 如果您必須重設會計分配，建議您還要安裝 KB 4131710。

## <a name="data-flow-for-project-service-automation-and-finance"></a>Project Service Automation 與 Finance 的資料流程

Project Service Automation 與 Finance 整合解決方案會使用資料整合功能，跨 Project Service Automation 與 Finance 的執行個體來同步處理。 可與資料整合功能搭配使用的整合會在 Finance 與 Project Service Automation 之間啟用有關專案費用交易類別的資料流程。

如果專案費用類別是在 Finance 中主控，則整合流程會先從 Finance 執行到 Project Service Automation。 專案費用類別的整合識別碼接著會透過從 Project Service Automation 到 Finance 的同步處理進行更新。

如果專案費用類別是在 Project Service Automation 中主控，則整合流程會先從 Project Service Automation 執行到 Finance。 專案類別必須已經先在 Finance 中進行設定，才能從 Project Service Automation 進行同步處理。 從 Finance 同步處理回到 Project Service Automation，然後再次從 Project Service Automation 同步處理到 Finance。 如此一來，就有助於保證類別已連結，且不會建立任何重複資料。

> [!NOTE]
> 專案費用類別通常是在 Finance 中主控。 不過，如果不是，或如果已經在 Project Service Automation 中建立費用類別，您就必須先使用「專案費用交易類別 (PSA 至 Fin 和 Ops)」範本來同步處理。 然後使用「專案費用交易類別 (Fin 和 Ops 至 PSA)」範本進行同步處理。 您應該再從 Project Service Automation 執行同步處理到 Finance 一次。
>
> 如果先從 Project Service Automation 進行同步處理，則必須在 Finance 中符合下列需求，才能執行同步處理：
>
> - 符合 Project Service Automation 中所設定專案類別的共用類別必須存在，且必須已針對 **專案** 及 **費用** 啟用。
> - 對於每個必須與之整合的 Finance 法律實體，必須有下列專案類別存在：
>
>     - **專案類別** 存在。 
>     - **在費用中使用** 已啟用。
>     - **在日記帳中啟動** 已啟用。
>     - **交易類型** 設定為 **費用** 。

下圖這些顯示如何在 Project Service Automation 與 Finance 之間同步處理資料。

[![Project Service Automation 與 Finance 整合的資料流程](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>從 Finance 至 Project Service Automation 的專案費用類別同步處理

### <a name="template-and-task"></a>範本與工作

若要存取範本，請在 Microsoft Power Apps 系統管理中心選取 **專案** ，然後選取右上角的 **新增專案** 以選取公用範本。

下列範本與基礎工作會用來將專案費用類別從 Finance 同步處理至 Project Service Automation：

- **資料整合中範本的名稱：** 專案費用交易類別 (Fin 和 Ops 至 PSA)
- **專案中工作的名稱：** 將類別同步至 PSA

### <a name="entity-set"></a>實體集

| 財務                           | Project Service Automation |
|-----------------------------------|----------------------------|
| 類別至的整合實體 | 交易類別     |

### <a name="entity-flow"></a>實體流程

專案費用類別是在 FinanceFinance 中進行管理，並同步處理至 Project Service Automation 做為交易類別。

### <a name="power-query"></a>Power Query

同步處理至 Project Service Automation 時，您必須使用 Microsoft Power Query for Excel 來設定交易類別的帳單類型。 「專案費用交易類別 (Fin 和 Ops 至 PSA)」範本會提供預設欄和對應。 如果您自行建立範本，就必須在 Power Query 中新增條件欄。 依照下列步驟執行。

1. 按一下箭頭以開啟「專案費用交易類別 (Fin 和 Ops 至 PSA)」範本中專案費用類別工作的對應。
2. 按一下 **進階查詢及篩選** 連結，以開啟 Power Query。
2. 選取 **新增條件欄** 。
3. 輸入新欄的名稱，例如 **BillingType** 。
4. 輸入下列條件： **如果 CATEGORYID 不等於 Null 則為 19235001，否則為 Null** 。
5. 按一下欄中的 **確定** 。
6. 請務必在對應頁面上對應這個新欄。

下圖顯示資料整合中的範本工作對應範例。 此對應顯示會從 Finance 同步處理至 Project Service Automation 的欄位資訊。

[![專案費用類別至 Project Service Automation 範本對應](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>從 Project Service Automation 至 Finance 的專案費用類別同步處理

### <a name="template-and-task"></a>範本與工作

下列範本與基礎工作會用來將專案費用類別從 Project Service Automation 同步處理至 Finance：

- **資料整合中範本的名稱：** 專案費用交易類別 (PSA 至 Fin 和 Ops)
- **專案中工作的名稱：** 將類別同步至 Fin Ops

### <a name="entity-set"></a>實體集

| Project Service Automation | 財務                           |
|----------------------------|-----------------------------------|
| 交易類別     | 類別至的整合實體 |

### <a name="entity-flow"></a>實體流程

專案費用類別是在 FinanceFinance 中進行管理，並同步處理至 Project Service Automation 做為交易類別。 同步處理回到 Finance 會將 Finance 中的專案類別更新為 Project Service Automation 中的整合識別碼。

### <a name="template-mapping-in-data-integration"></a>資料整合中的範本對應

下圖顯示資料整合中的範本工作對應範例。

> [!NOTE]
> 此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。

[![Project Service Automation 至 Finance 範本對應](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]