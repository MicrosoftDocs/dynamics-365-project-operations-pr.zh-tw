---
title: 2022 年 7 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本文提供有關資源/非庫存型案例適用 Microsoft Dynamics 365 Project Operations 2022 年 7 月發行版本中所提供之品質更新的資訊。
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183878"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 7 月新增功能 - 資源/非庫存型案例適用的 Project Operations

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.44.0.22 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.28 版中的專案管理與會計

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

此版本中沒有 Project Operations 雙重寫入對應的更新。 如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](../environment/resource-dual-write-maps.md)。

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 部署和設定 | 2761472 | 已處理 Project Operations 安裝錯誤。 |
| 帳單和定價 | 2746940 | 轉包合約服務內容名稱的最大長度應為 100 個字元。 |
| 帳單和定價 | 2739162 | 客戶必須可以在實際值網格檢視表中看到功能區按鈕。 |
| 專案規劃和追蹤 | 2730318 | 更新對專案主題中不支援字元的驗證。 |
| 帳單和定價 | 2705361 | 里程碑已開單銷售實際值必須包含在專案追蹤欄位中。 |
| 帳單和定價 | 2675880 | 避免將專案連結至不屬於工作型的合約服務內容。 |
| 帳單和定價 | 2664396 | 如果在沒有報價的情況下儲存報價價目表，則必須有錯誤指出報價不可為空白。 |
| 帳單和定價 | 2184019 | 對於沒有支援合約或報價的專案，不應顯示 **工作型帳單** 索引標籤。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance 中的專案管理與會計

如需有關此更新中所包含 Bug 修正的詳細資訊，請登入 Microsoft Dynamics Lifecycle Services (LCS)，並檢視[知識庫文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438)。

## <a name="features-turned-on-by-default-in-upcoming-release"></a>即將推出的版本中預設啟用的功能

下表列出 10.0.29 版中預設開啟的功能。 大多數已自動開啟的功能都可以在[功能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)中關閉。 將來，某些已自動開啟的功能可能會從功能管理中移除，並成為必要功能。 這項變更可確保客戶使用最新功能，讓增強功能可以根據在其新增至系統時的最新功能進行建置。 除非判斷功能是必要的，否則永遠不會在不到一年的時間內自動啟用這些功能。

| 功能名稱 | 啟用日期 | 新增的功能 | 功能狀態 | 模組 |
| --- | --- | --- |--- |--- |
| 根據資金規則配置中的變更，啟用工時交易調整 | 2022 年 9 月 16 日 | 2020 年 10 月 7 日 | 預設開啟 | 專案管理與會計 |
| 專案採購單預付款發票沖回功能 | 2022 年 9 月 16 日 | 2021 年 10 月 6 日 | 預設開啟 | 專案管理與會計 |
| 使用資源型/非庫存案例適用的 Project Operations 時，刪除發票提案明細 | 2022 年 9 月 16 日 | 2021 年 10 月 6 日 | 預設開啟 | 專案管理與會計 |
| 調整已過帳專案交易的會計核算 | 2022 年 9 月 16 日 | 2020 年 5 月 10 日 | 預設開啟 | 專案管理與會計 |
| 啟用專案的預設會計設定 | 2022 年 9 月 16 日 | 2020 年 2 月 19 日 | 預設開啟 | 專案管理與會計 |
| 為專案啟用多個合約服務內容 | 2022 年 9 月 16 日 | 2020 年 6 月 29 日 | 預設開啟 | 專案管理與會計 |
| 如果目前核准狀態不允許編輯，則將專案工時帳目設定為唯讀 | 2022 年 9 月 16 日 | 2021 年 10 月 6 日 | 預設開啟 | 專案管理與會計 |
| 更新採購明細並開啟採購單變更管理參數時，允許從採購單明細中同步銷售明細 | 2022 年 9 月 16 日 | 2020 年 10 月 7 日 | 預設開啟 | 專案管理與會計 |
| 啟用 Dynamics 365 Customer Engagement 上的 Project Operations | 2022 年 9 月 16 日 | 2020 年 6 月 29 日 | 預設開啟 | 專案管理與會計 |
| 專案交易沖回更正功能 | 2022 年 9 月 16 日 | 2020 年 7 月 13 日 | 預設開啟 | 專案管理與會計 |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>在即將推出的發行版本中變成必要功能的功能

下表列出從 10.0.29 版開始強制使用的功能。

| 功能名稱 | 啟用日期 | 新增的功能 | 功能狀態 | 模組 |
| --- | --- | --- | --- | --- |
| 在未將匯率四捨五入的情況下，計算資金來源的已認可值 | 2022 年 9 月 16 日 | 2020 年 6 月 14 日 | 必要 | 專案管理與會計 |
| 使用與原始交易相同的分類帳科目啟用專案調整過帳 | 2022 年 9 月 16 日 | 2020 年 6 月 14 日 | 必要 | 專案管理與會計 |
| 專案合約認可金額詳細資料 | 2022 年 9 月 16 日 | 2019 年 8 月 31 日 | 必要 | 專案管理與會計 |
| 在建立專案發票提案期間啟用依資源排序 | 2022 年 9 月 16 日 | 2019 年 8 月 31 日 | 必要 | 專案管理與會計 |
