---
title: 廠商發票整合
description: 本主題提供有關 Project Operations 中廠商發票整合的資訊。
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d4f1b0ad94b71dc4adc5b2b3423340c5fdb171eb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002245"
---
# <a name="vendor-invoice-integration"></a>廠商發票整合

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

移至 **應付帳款** > **發票** > **待處理廠商發票** 並使用待處理廠商發票單據，可以記錄 Dynamics 365 Project Operations 中的專案相關採購。 如需詳細資訊，請參閱[使用待處理廠商發票購買非庫存材料](../procurement/pending-vendor-invoices.md)。

> [!IMPORTANT]
> 使用本主題中所述的功能之前，請先檢閱並套用必要的設定。 如需詳細資訊，請參閱[啟用非庫存材料和待處理廠商發票](../procurement/configure-materials-nonstocked.md)。

在 Project Operations 中，會使用特殊過帳規則將專案相關廠商發票過帳：

- 專案相關成本 (包括不可退回稅金) 不會立即過帳至總帳中的專案成本科目。 反而是將成本過帳至 **採購整合科目**。 此科目是在 **Dynamics 365 Customer Engagement 上的 Project Operations** 索引標籤的 **專案管理與會計** > **設定** > **專案管理與會計參數** 中進行設定。
- 雙重寫入會使用下列資料表對應，將廠商發票詳細資料同步處理 Microsoft Dataverse：

     - **Project Operations 整合專案廠商發票匯出實體 (msdyn_projectvendorinvoices)**：此資料表對應會同步處理廠商發票標題資訊。 只有在廠商發票至少有一行明細包含專案識別碼時，才會同步處理至 Dataverse。
     - **Project Operations 整合專案廠商發票明細匯出實體 (msdyn_projectvendorinvoicelines)**：此資料表對應會同步處理廠商發票明細資訊。 只有包含專案識別碼的訂單才會同步處理至 Dataverse。

     > [!NOTE]
     > Dataverse 中的廠商發票詳細資料不可編輯。

系統會在過帳廠商發票時，視實際情況在 Dynamics 365 Finance 中記錄稅金子分類帳、廠商子分類帳及其他財務過帳。

![廠商發票整合](media/DW7VendorInvoice.png)

將記錄寫入 Dataverse 中的 **廠商發票** 實體時，記錄的自動化核准程序會開始。 如果需要，您可以移至 **進階設定** > **系統** > **系統作業**，在 Dataverse 中檢閱自動化核准程序狀態。 核准完成後，系統會在 **實際值** 實體中建立材料交易分類記錄。

接著會使用雙重寫入資料表對應 **Project Operations 整合實際值 (msdyn_actuals)** 來處理材料相關實際值。 如需詳細資訊，請參閱[專案估計值和實際值](resource-dual-write-estimates-actuals.md)。

定期程序 **從臨時表格匯入** 會建立廠商發票相關 Project Operations 整合帳目明細。 抵銷科目預設為採購整合科目。 過帳整合帳目時，會結清廠商發票交易的帳戶餘額，並將明細金額轉入專案成本科目。 系統還會建立專案子分類帳交易，供作下游開立發票和收入認列之用。
