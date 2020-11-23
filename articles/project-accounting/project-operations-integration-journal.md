---
title: Project Operations 中的整合帳目
description: 此主題提供在 Project Operations 中使用整合帳目的資訊。
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ffe3373184c8cd776bf3705fd674bedf221d9b77
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133296"
---
# <a name="integration-journal-in-project-operations"></a>Project Operations 中的整合帳目

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

時間和費用項目會建立 **實際** 交易，表示針對專案完成的工作運作檢視表。 Dynamics 365 Project Operations 為會計師提供審查交易，並視需要調整會計屬性的工具。 在審查和調整完成後，交易會過帳至專案分類帳和總帳。 會計可以使用 **Project Operations 整合** 帳目執行這些活動（**Dynamics 365 Finance** > **專案管理與會計** > **帳目** > **Project Operations 整合** 帳目）。

![整合帳目流程](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>在 Project Operations 整合帳目中建立記錄

Project Operations 整合帳目中的記錄是使用週期程序（**從臨時表格匯入**）建立。 您可以前往 **Dynamics 365 Finance** > **專案管理和會計** > **週期** > **Project Operations 整合** > **從臨時表格匯入** 以執行此程序。 您可以視需要以互動方式執行程序，或將程序設定成在背景執行。

當週期程序執行時，會找出尚未新增至 Project Operations 整合帳目的任何實際值。 即會建立每個實際交易的帳目明細。
系統會根據 **Project Operations 整合帳目上的週期單位** 欄位（**財務** > **專案管理和會計** > **設定** > **專案管理與會計參數**、**Dynamics 365 Customer Engagement 上的 Project Operations** 索引標籤）中所選取的值，將帳目明細分組為不同的帳目。 這個欄位的可能值包括：

  - _*天**：實際值是依交易日期進行分組。 每一天都會建立不同的帳目。
  - **月**：實際值是依日曆月分組。 每個月都會建立不同的帳目。
  - **年**：實際值是依日曆年分組。 每一年都會建立不同的帳目。
  - **全部**：所有實際交易均包含在相同的整合帳目中。 如果當週期程序執行時無法使用該帳目，例如，帳目是在過帳交易程序中，就會建立新的帳目。

會根據專案實際值建立帳目明細。 以下清單包括一些較為明顯的預設和轉換規則：

  - 每個專案實際交易在 Project Operations 整合帳目中都有一行。 時間和資料帳單類型的成本與未開單銷售交易會顯示在不同的行上。
  - **日期** 欄位表示交易的日期。 **會計日期** 欄位表示將交易記錄到總帳的日期。 如果會計日期是在 [已關閉的財務期間](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end)，且在 **專案管理與會計參數** 頁面的 **財務** 索引標籤上設定了參數 **自動設定會計日期以開放總帳期間**，則系統會將交易的會計日期調整為下一個開放式總帳期間的第一個日期。
  - **傳票** 欄位會顯示每個實際交易的傳票號碼。 傳票號碼序列是在 **專案管理與會計參數** 頁面的 **數字序列** 索引標籤上定義。 每個明細都會指派一個新的號碼。 在過帳傳票後，您可以透過在 **傳票交易** 頁面上選取 **相關傳票**，來查看成本與未開單銷售交易的關聯方式。
  - **類別** 欄位代表專案交易，並根據相關專案實際值的交易類別來進行預設值。
    - 如果在專案實際值中設定了 **交易類別**，而在給定的法律實體中有相關 **專案類別**，則類別預設為此專案類別。
    - 如果專案實際值中未設定 **交易類別**，則系統會使用 **專案管理與會計參數** 頁面上 **Dynamics 365 Customer Engagement 上的 Project Operations** 索引標籤的 **專案類別預設值** 欄位中的值。
  - **資源** 欄位表示與此交易相關的專案資源。 資源可做為向客戶提供專案發票提案中的參考。
  - **匯率** 欄位的預設值是 Dynamics 365 Finance 中設定的 **貨幣匯率**。 如果遺失匯率設定，則 **從臨時匯入** 週期程序不會將記錄新增至日記，並會將錯誤訊息新增至作業執行記錄。
  - **明細屬性** 欄位代表專案實際值中的帳單類型。 在 **專案管理與會計參數** 頁面的 **Dynamics 365 Customer Engagement 上的 Project Operations** 索引標籤上，定義明細屬性與帳單類型對應。

在 Project Operations 整合帳目明細中，只能更新下列會計屬性：

- **帳單銷售稅金群組** 和 **帳單項目銷售稅金群組**
- **財務維度**（使用 **分配金額** 動作）

您可以刪除整合帳目明細，但是在您從 **從臨時匯入** 週期程序重新匯入之後，將會再次將任何未過帳的明細插入至帳目中。

當您過帳整合帳目時，會建立專案分類帳和總帳交易。 這些用於下游客戶開立發票、營收確認和財務報表。
