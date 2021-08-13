---
title: 費用管理整合
description: 本主題提供有關 Project Operations 中使用雙重寫入進行費用報表整合的資訊。
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 06471532d2e41bb80ebf92f0a8b93c324b3f6d3e845cea8033d85d291ea237eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986571"
---
# <a name="expense-management-integration"></a>費用管理整合

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本主題提供有關 Project Operations [全額費用部署](../expense/expense-overview.md)中使用雙重寫入進行費用報表整合的資訊。

## <a name="expense-categories"></a>費用類別

在全額費用部署中，費用類別是在 Finance and Operations 應用程式中所建立和維護。 若要建立新的費用類別，完成下列步驟：

1. 在 Microsoft Dataverse 中，建立 **交易** 類別。 雙重寫入整合會將此交易類別同步處理至 Finance and Operations 應用程式。 如需詳細資訊，請參閱[設定專案類別](/dynamics365/project-operations/project-accounting/configure-project-categories)和 [Project Operations 設定和設定資料整合](resource-dual-write-setup-integration.md)。 由於此整合，系統在 Finance and Operations 應用程式中建立四個共用類別記錄。
2. 在 Finance 中，移至 **費用管理** > **設定** > **共用類別**，然後選取具有 **費用** 交易分類的共用類別。 將 **可在費用中使用** 參數設定為 **True**，並定義要使用的費用類型。
3. 移至 **費用管理** > **設定** > **費用類別** 並選擇 **新增**，以使用此共用類別記錄建立新的費用類別。 儲存記錄時，雙重寫入會使用資料表對應 **Project Operations 整合專案費用類別匯出實體 (msdyn\_expensecategories)**，將此記錄同步處理至 Dataverse。

  ![費用類別整合。](./media/DW6ExpenseCategories.png)

Finance and Operations 應用程式中的費用類別各有不同的適用公司或法律實體。 在 Dataverse 中有個別對應的法律實體特定記錄。 當專案經理估計費用時，他們無法選取針對由與擁有他們所從事專案之公司不同的公司所建立的費用類別。 

## <a name="expense-reports"></a>費用報表

費用報表是在 Finance and Operations 應用程式中所建立和核准。 如需詳細資訊，請參閱[在 Dynamics 365 Project Operations 中建立和處理費用報價](/learn/modules/create-process-expense-reports/)。 專案經理核准費用報表之後，此報價會過帳至總帳。 在 Project Operations 中，會使用特殊過帳規則將專案相關費用報表明細過帳：

  - 專案相關成本 (包括不可退回稅金) 不會立即過帳至總帳中的專案成本科目，而是過帳至費用整合科目。 此科目是在 **Dynamics 365 Customer Engagement 上的 Project Operations** 索引標籤的 **專案管理與會計** > **設定** > **專案管理與會計參數** 中進行設定。
  - 雙重寫入會使用 **Project Operations 整合專案費用報表實體 (msdyn\_expenses)** 資料表對應來同步處理至 Dataverse。
  - 系統會視費用報表過帳時的實際情況來記錄稅金子分類帳、廠商子分類帳及其他財務過帳。

  ![費用報表整合。](./media/DW6ExpenseReports.png)

在 Dataverse 中將記錄寫入 **費用** 實體時，系統會觸發記錄的自動化核准程序。 如果需要，您可以移至 **進階設定** > **系統** > **系統作業**，在 Dataverse 中檢閱自動化核准程序狀態。 核准完成後，**實際值** 實體中會建立費用交易分類記錄。

接著會使用雙重寫入資料表對應 **Project Operations 整合實際值 (msdyn\_actuals)** 來處理費用相關實際值。 如需詳細資訊，請參閱[專案估計值和實際值](resource-dual-write-estimates-actuals.md)。

定期程序 **從臨時表格匯入** 會在 Project Operations 整合帳目中建立費用報表相關帳目明細。 抵銷科目預設為費用整合科目。 過帳整合帳目會結清費用交易的帳戶餘額，並將費用金額轉入專案成本科目。 系統還會建立專案子分類帳交易，供作下游開立發票和收入認列之用。
