---
title: 2022 年 9 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本文提供有關 Microsoft Dynamics 365 Project Operations 2022 年 9 月發行版本中資源/非庫存型案例的品質更新資訊。
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634795"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 9 月新增功能 - 資源/非庫存型案例適用的 Project Operations

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.46.0.60 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.29 版中的專案管理與會計

## <a name="features-included-in-this-release"></a>此版本包含的功能

| 功能區域 | 功能名稱 | 更多資訊 |
| --- | --- | --- |
| 商機管理 | **報價的修訂與啟用**<br>Project Operations 會提供銷售處理的完整支援。 可啟動專案報價來代表一個狀態，在此狀態中報價是唯讀且正被檢閱中。 可以修訂已啟動的報價，以建立具有遞增修訂版本編號的新報價。 啟用的專案報價或報價修訂可以成交或未成交狀態來關閉。 | [啟動和修訂專案報價](/dynamics365/project-operations/sales/activation-and-revision) |
| 帳單和定價 | **時區互通的價格預設**<br>Project Operations 在所有專案實際值上引進了時區互通日期的概念。 新的欄位 (**交易日期**) 現在可在帳目明細和實際值上使用，並將用來儲存交易發生的日期，但是不會將該日期轉換為國際標準時間。 此日期將用於下游處理，例如價格預設和發票建立。 | <p>[決定專案估計值及實際值的成本費率](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[判斷專案估計值及實際值的銷售價](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| 帳單和定價 | **Project Operations 中的日期有效價格覆寫**<br>有效期限內價格覆寫提供覆寫或變更價目表中特定價格的方法。 | [有效期限內價格覆寫](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| 轉承包 | **轉包合約和供應商發票對帳**<br>此功能讓客戶可建立轉包合約以購買資源時間、費用類別和用於專案工作的原料。 它也可讓客戶在財務和營運應用程式中記錄可用的供應商發票，供專案經理在 Dataverse 中驗證。 | <p>[轉包合約管理](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[建立廠商發票](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| 時間和費用 | **全域核准者**<br>此功能啟用獨立軟體廠商 (ISV) 和集中核准，無論專案中的專案或團隊成員狀態為何。 | [安全性與核准](/dynamics365/project-operations/approvals/approvals-security) |
| 費用管理 | **可用供應商貨幣的種類張貼欠款費用的能力**<br>此功能在現金支付方式中，讓費用報告能以供應商的貨幣種類張貼。 | [可用供應商的貨幣種類張貼費用欠款的能力](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| 專案採購 | **支付廠商付款時付款**<br>此功能啟用「付款時付款」(PWP) 功能，可和 Project Operations 非庫存環境一起使用。 它可依據保留條款封鎖/保留付給供應商的款項，直到從客戶那裡收到付款。 | [支付廠商付款時付款](/dynamics365/project-operations/procurement/pay-when-paid) |
| 專案採購 | **專案採購申請**<br>此功能可讓使用者在法律實體中建立專案相關的採購訂單，而此法律實體已啟用 Dynamics 365 Customer Engagement 整合上的 Project Operations。 專案採購單可用來讓採購部門角色記錄專案的非庫存原料採購。 專案採購單將不會同步到 Dataverse。 不過，您可以使用虛擬實體在 Dataverse 中顯示專案採購單內容的專案經理資訊。 與專案相關的供應商發票成本與 Dataverse 中的專案實際值實體整合。 使用 Project Operations 整合日誌可將專案成本紀錄在專案分類帳中。 | |
|專案規劃和追蹤|**使用專案排程 API 以對排程實體執行作業** </br> </br>資源指派分佈編輯 API 可讓開發人員在任何支援的日期範圍內，透過程式設計方式指定工作受託人的投入量，以進行更精細的時間分段投入規劃。|[使用專案排程 API 以對排程實體執行作業](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

下表顯示 Project Operations 2022 年 9 月發行版本中已修改或新增的雙重寫入對應。

| 實體對應 | 更新的版本 | 意見 |
| -------------- | ------------------- | ------------|
| Project Operations 整合實際值 (msdyn_actuals) | 1.0.0.15 | 此對應支援適用於資源型案例，使用 Project Operations 處理的轉包合約實際值。 |
| Project Operations 整合專案廠商發票匯出實體 (msdyn_projectvendorinvoices) | 1.0.0.2 | 此對應支援適用於資源型案例，使用 Project Operations 處理的轉包合約實際值。 |
| Project Operations 整合專案廠商發票明細匯出實體 (msdyn_projectvendorinvoicelines) | 1.0.0.5 | 此對應支援適用於資源型案例，使用 Project Operations 處理的轉包合約實際值。 |

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 帳單和定價 | 2754422 | 當專案在 Dataverse 中複製時，原料和費用估算不會流向 Finance。 |
| 時間和費用 | 2787409 | 非有效的核准者可以核准非專案時間項目。 |
| 商機管理 | 2788907 | 在包含標誌之訂單內容的唯一性驗證上，更新錯誤訊息。 |
| 時間和費用 | 2842253 | 用於時間審核的空例外狀況處理。 |
| 帳單和定價 | 2844181 | 無法取得關聯性識別碼，阻礙了發票建立。 |
| 帳單和定價 | 2876628 | QLD，CLD -估計價目表解決方案應使用價目表的舊版日期範圍欄位。 |
| 轉承包 | 2893222 | 如果未指定轉包合約服務內容的角色，則應該可以為任何角色在團隊成員上選取該內容。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance 中的專案管理與會計

如需此更新中有關 Bug 修正的詳細資訊，請登入 Microsoft Dynamics Lifecycle Services，查看[知識庫文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559)。

## <a name="features-turned-on-by-default-in-upcoming-release"></a>即將推出的版本中預設啟用的功能

下表列出 10.0.30 版中預設開啟的功能。 大多數已自動開啟的功能都可以在[功能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)中關閉。 將來，某些已自動開啟的功能可能會從功能管理中移除，並成為必要功能。 這項變更可確保客戶使用最新功能，讓增強功能可以根據在其新增至系統時的最新功能進行建置。 除非判斷功能是必要的，否則永遠不會在不到一年的時間內自動啟用這些功能。

| 功能名稱 | 啟用日期 | 新增的功能 | 功能狀態 | 模組 |
| --- | --- | --- |--- |--- |
| 當使用者需要在同步與非同步作業之間切換時，可啟用非同步作業 | 2022 年 10 月 21 日 | 2021 年 4 月 9 日 | 預設開啟 | 費用管理 |
| 所需的收據費用原則評估 | 2022 年 10 月 21 日 | 2021 年 12 月 20 日 | 預設開啟 | 費用管理 |
| 由委派工作人員建立的費用報表清單檢視表 | 2022 年 10 月 21 日 | 2020 年 2 月 19 日 | 預設開啟 | 費用管理 |
| 依據會計年度計算的總里程 | 2022 年 10 月 21 日 | 2022 年 5 月 10 日 | 預設開啟 | 費用管理 |
