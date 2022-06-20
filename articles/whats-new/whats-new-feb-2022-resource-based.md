---
title: 2022 年 2 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 本文提供有關資源/非庫存型案例適用 Project Operations 2022 年 2 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932976"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 2 月 - 資源/非庫存型案例適用的 Project Operations 新增功能

*適用於：資源/非庫存型案例適用的 Project Operations*

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.28.0.120 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.24 版中的專案管理與會計

## <a name="features-included-in-this-release"></a>此版本包含的功能

- 從此發行版本開始，您可以將最多可達 300 個的團隊成員新增至單一專案。 在此之前，團隊成員的數目限制為 150 個。 如需詳細資訊，請參閱[專案限制](../project-management/create-wbs.md#project-limitations)。

## <a name="project-operations-dual-write-map-updates"></a>Project Operations 雙重寫入對應更新

下列清單顯示 Project Operations 2022 年 2 月發行版本中已修改或新增的雙重寫入對應。

| 實體對應 | 更新的版本 | 意見 |
| --- | --- | --- |
| Project Operations 整合專案費用匯出實體 (msdyn\_expenses) | 1.0.0.3 | 擴充對 Dataverse 的專案活動同步處理。 |

如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](../environment/resource-dual-write-maps.md)。

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 帳單和定價 | 2415109 | **作業付款條件** 欄位中的預設值必須是專案合約客戶記錄和預估發票記錄。 |
| 帳單和定價 | 2497369 | 材料更正必須遵循 **更正** 參數中的日期值。 |
| 帳單和定價 | 2498697 | 改善 **時間項目回收** 的安全性設定。 |
| 帳單和定價 | 2513824 | 對於資源型案例，交易類別識別碼在 Project Operations 中不得超過 28 個字元。 |
| 帳單和定價 | 2517455 | 不可允許多次同時對同一份發票觸發 **重新整理發票明細交易** 動作。 |
| 帳單和定價 | 2517465 | **停用發票明細詳細資料** 動作已因不受支援而遭封鎖。 |
| 帳單和定價 | 2556660 | 修正對已附加至專案參數記錄之價目表進行的日期有效性檢查。 |
|   商機管理 | 2369202 | 更正商務規則，此規則確認是否可將有效性日期重疊的價目表附加至同一份專案合約。 |
|   商機管理 | 2385965 | 更正 **專案合約** 頁面的 **客戶** 索引標籤在您選取 **儲存後關閉** 時的行為。 |
| 時間和費用 | 2538503 | 過帳費用報表之後，**專案實際值** 實體中必須有專案工作可用。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 專案管理與會計 | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | 進行廠商貸項通知單匯入時，發生錯誤。 錯誤訊息表示「保留款金額不能大於剩餘的淨金額」。 |
| 專案管理與會計 | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | 如果發票提案包含未開單銷售實際值的任何零金額費用交易，則無法進行開立發票作業。 |
| 專案管理與會計 | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | 更新採購價並啟用 **啟用變更管理** 之後，過帳的成本不正確。|
| 專案管理與會計 | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | 固定價格專案的過帳估計在估計憑單中使用不正確貨幣和金額，即使 **啟用專案合約貨幣以計算估計值** 功能已啟用，也會這樣。 |
| 專案管理與會計 | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** 不可在不攔截組態金鑰未啟用實體之例外狀況的情況下進行要啟用變更追蹤的呼叫。 |
| 專案管理與會計 | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | 在過帳多個進階帳目而發生錯誤時，修正批次工作。 |
| 差旅和費用 | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | 因為發行與費用報表中預付現金相關的結算問題，稅金金額未包括在預付現金中。 |
| 差旅和費用 | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | 銷售稅資訊未包含在 **費用 - 已過帳交易** 報表中。 |
| 差旅和費用 | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | **需要收據** 費用原則違規錯誤地在費用報表上顯示警告。 |
| 差旅和費用 | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | 當交易是里程費用的結果時，專案交易未在總銷售金額中包含非應退銷售稅。 |
| 差旅和費用 | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | 當分項列出的明細含稅時，您無法變更分項列記明細日期，而且發生原始憑證狀態錯誤。 |

## <a name="removed-and-deprecated-features"></a>已移除和已取代的功能

[Project Operations 中已移除或已取代的功能](removed-depreciated-features-project.md)文章題說明 Dynamics 365 Project Operations 已移除或已取代的功能。

- 已移除的功能在產品中不復存在。
- 取代的功能不在主動開發之列，可能會在未來的更新中遭移除。

將任何功能從產品移除之前 12 個月，取代公告會出現在 [Project Operations 中已移除或已取代的功能](removed-depreciated-features-project.md)文章中。

對於僅影響編譯時間但與沙箱和生產環境二進位相容,的中斷性變更來說，取代時間將少於12個月。 這些變更通常是必須對編譯器進行的功能更新。
