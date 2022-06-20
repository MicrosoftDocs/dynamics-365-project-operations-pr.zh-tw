---
title: 2021 年 5 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本文提供有關資源/非庫存型案例適用 Project Operations 2021 年 5 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930400"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 5 月新增功能 - 資源/非庫存型案例適用的 Project Operations

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

這篇文章適用於下列 Dynamics 365 Project Operations 元件和版本：

- Project Operations on Dynamics 365 Dataverse 環境 4.10.0.186 版
- 財務和營運應用程式環境 10.0.18 版中的專案管理與會計

## <a name="features-included-in-this-release"></a>此版本包含的功能

此版本包含下列功能：

- [排程模式](../project-management/scheduling-modes.md)：專案經理可以規定管理專案時所應使用的是固定期間、固定工時還是固定單位排程模式。
- [使用里程費率層級來設定里程](../expense/set-up-mileage.md)：更新員工費用報表的里程費率層級。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

下表顯示 Project Operations 2021 年 5 月版本中已修改或新增的雙重寫入對應。

| 實體對應 | 更新的版本 | 註解 |
| --- | --- | --- |
| 專案資金來源 (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | 同步處理專案合約客戶付款條件。 |
| 專案發票提案 V2 (發票) | 1.0.0.3 | 同步處理預估發票付款條件。 |
| Project Operations 整合專案廠商發票明細匯出實體 (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | 品質更新 |
| 專案 V2 (msdyn\_projects) | 1.0.0.2 | 品質更新 |

更新 Project Operations Dataverse 解決方案以及財務和營運應用程式解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的資料表對應。 如果未啟用最新版本的對應，特定功能可能無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中查看對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的資料表對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果啟動對應時發生問題，請依照[對應上發生的遺失資料表欄問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)雙重寫入疑難排解指南一節中的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 帳單和定價 | 2227635 | **單位群組** 和 **單位** 欄位中的值預設會根據 **材料估計值** 網格中的產品來設定。 |
| 帳單和定價 | 2234127 | 將廠商發票過帳時，**工作識別碼** 欄位現在可正確併入至 Dataverse 專案實際值。 |
| 帳單和定價 | 2235564 | 儲存帳目明細可確保帳目明細項目中顯示的貨幣，在儲存後與該明細的預設貨幣相符。 |
| 帳單和定價 | 2246671 | 開立發票時將交易設為不應收費，會沖回原始未開單銷售記錄，並建立標示為不應收費的新未開單銷售記錄。 |
| 帳單和定價 | 2264042 | 如果有在環境中為無效的發票更正詳細資料，則不得封鎖有效的發票更正。 |
| 帳單和定價 | 2146367 | 專案發票標題雙重寫入對應已擴充為包含付款條件。 |
|   商機管理 | 2086888 | 將報價複製到新複製報價的應收費角色和類別之前，請勿新增已停用的角色和類別。 |
|   商機管理 | 2234376 | 唯讀欄位會在 **材料估計值** 窗格中反灰顯示。 |
|   商機管理 | 2238337 | 即使與專案價目表無關聯，也可以儲存以連絡人為根據的報價。 |
|   商機管理 | 2239810 | 以未成交關閉報價也會關閉相關聯的專案，並取消任何預約。 |
| 專案規劃和追蹤 | 2099559 | 新增在 **專案工作** 網格開啟前對系統健全狀況的額外驗證。 |
| 專案規劃和追蹤 | 2178987 | 修正選取 **專案** 頁面的 **下一個階段** 時發生的暫時性錯誤。 |
| 資源管理 | 2224817 | 用於延長預約的功能預設會使用正確的預約狀態。 |
| 時間項目 | 2202476 | **時間項目** 頁面現在會使用回應網格控制項，並修正諸如網格對齊錯誤之類的問題。 |
| 時間項目 | 2223377 | 時間項目會在 **可預約資源** 頁面的 **相關** 區段中隱藏，以避免與可用性產生混淆。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 專案管理與會計 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | 資源型案例適用的 Project Operations：因為整合錯誤，無法將報價轉換為已成交。 |
| 專案管理與會計 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations：因為檢查是否有重疊合約服務內容與交易類型，當您嘗試將合約服務內容與專案識別碼建立關聯時，發生錯誤。 |
| 專案管理與會計 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 會設定不同客戶的資金來源發票地址。 |
| 差旅和費用 | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | 可能會發生與里程設定相關的過帳錯誤。 |
| 差旅和費用 | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | 外幣費用交易的 **分攤至個人** 功能無法運作。 |
| 差旅和費用 | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | 不論是否代理人為資源，[費用類別] 下拉式清單值顯示給他們的都是不正確的類別。 |
| 差旅和費用 | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | 您無法儲存公司間費用報表，因為發生 **資源/類別驗證** 錯誤。 |
| 差旅和費用 | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | 費用報表過帳中的錯誤里程費率計算有分割明細。 |
| 差旅和費用 | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | 含銷售稅且付款方式上的抵銷科目類型為 **工作者** 時，您無法將公司間費用報表過帳。 |
| 差旅和費用 | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | 復原 **TrvRequisitionLine** 資料實體與唯一索引相關聯。 |
| 差旅和費用 | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | 費用報表支援建立和更新原始憑證明細。 |
| 差旅和費用 | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 如果銷售稅已過帳至目的地法律實體，則會在公司間案例中顯示不正確的子分類帳日記帳。 |
| 差旅和費用 | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations：從 Dataverse 移除費用估計值時，並未將其從 Finance 中刪除。 |
| 差旅和費用 | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 當費用類別屬於非專案類別時，在 **費用** 頁面上選取的財務維度並未複製到費用報表。 |
