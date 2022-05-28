---
title: 2021 年 6 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本主題提供有關資源/非庫存型案例適用之 Project Operations 2021 年 6 月發行版本所提供品質更新的資訊。
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 21a446fdb9526c1a2b110c5368516dafb64b5e01
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600778"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 6 月新增功能 - 資源/非庫存型案例適用的 Project Operations

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

- Dynamics 365 Dataverse 環境版本 4.11.0.156 或 4.11.0.164 上的 Project Operations。
- 財務和營運應用程式環境 10.0.19 版中的專案管理與會計。

## <a name="features-included-in-this-release"></a>此版本包含的功能

此版本包含下列功能：

- 可刪除[調整案例的專案發票提案明細](../invoicing/correct-project-invoice-proposals.md)的功能。
- 分項列出的費用明細會反映[顛覆想像的費用報表 - 新功能](../expense/expense-reports-reimagined.md#new-features)費用報表中的子類別名稱。
- 建立新的費用時，新的費用窗格中會有付款方式。
- 專案排程 API 正式發行。 這項新功能可讓客戶以程式設計方式對專案工作、資源指派、工作相依性及專案團隊成員記錄執行建立、更新和刪除作業。 如需詳細資訊，請參閱[使用專案排程 API 對排程實體執行作業](../project-management/schedule-api-preview.md)。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

此版本中沒有 Project Operations 雙重寫入對應的更新。 

如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](../environment/resource-dual-write-maps.md)。

更新 Project Operations Dataverse 解決方案以及財務和營運應用程式解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的資料表對應。 如果未啟用最新版本的對應，特定功能可能無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中查看對應的使用中版本。 選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本，以啟用對應的新版本。 如果您已對現成可用的資料表對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始對應時發生問題，請依照《雙重寫入疑難排解指南》的[對應缺少表格欄的問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節中指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 帳單和定價 | 2281417 | 修正有關透過發票排程自動建立發票之動作失敗的問題。 |
| 帳單和定價 | 2287835 | 改善發票確認效能。 |
| 商機管理 | 2222555 | 使用 **從專案估計匯入** 時，必須將材料估計可收費率選正確複製到報價明細詳細資料。 |
| 商機管理 | 2223427 | **GenerateRetainersFromRetainerScheduleOptions** 動作現在允許自訂。 |
| 商機管理 | 2277528 | 修正對包含多個客戶的專案合約服務內容的帳單里程碑值計算。 |
| 專案規劃和追蹤 | 2226110 | 修正 **專案團隊** 網格中 **產生需求** 功能的間歇性問題。 |
| 專案規劃和追蹤 | 2208109 | 使用者無法建立使用一種貨幣但其相關工作卻使用另一種貨幣的專案。 |
| 專案規劃和追蹤 | 2258228 | 允許使用排程 API 修改 **排程** 實體的欄位清單已更新。 |
| 專案規劃和追蹤 | 2293989 | 必須將正確的語言和地區設定傳遞至 **專案工作** 網格。 |
| 資源管理 | 2220493 | 修正 **工作** 網格在快速將資源要求標示為完成時的使用者體驗。 |
| 資源管理 | 2330496 | 修正 **排程面板** 載入問題。 (品質更新可在版本 4.11.0.164 中取得) |
| 時間和費用 | 2194431 | **時間項目** 網格必須遵循 **系統設定** 中所設定的當週開始日。 |
| 時間和費用 | 2277311 | 刪除 **時間項目** 網格中儲存格的值之後，游標仍然留在網格中。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 專案管理與會計 | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | 在與 Project Operations 整合的法律實體中，其 **專案管理設定** 下方看不到 **表單附註** 和 **表單設定**。 |
| 專案管理與會計 | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | 發票憑單的 **過帳類型** = **專案銷售稅** 時，加值稅的預設描述為空白。 |
| 專案管理與會計 | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | 工作型帳單與 Project Operations 整合搭配用於 Dataverse 時，過帳了雙重交易。 |
| 專案管理與會計 | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | 使用 Project Operations 時，收入認列中的完成百分比不正確。 |
| 專案管理與會計 | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | 在 Project Operations 整合案例的待處理廠商發票中，收入應計值增加一倍。 |
| 專案管理與會計 | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | 當收入設定檔規則設定為 **群組** 設定時，無法過帳整合帳目。 |
| 專案管理與會計 | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | 明細包含多個度量單位的專案採購單無法進行採購發票過帳。 |
| 專案管理與會計 | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | 無法使用專案 **V2** 資料實體來更新專案的預設財務維度。 |
| 專案管理與會計 | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | 用於建立專案估計值的批次程序需要的時間過長，無法完成。 |
| 專案管理與會計 | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | 刪除合約也會刪除與客戶相關聯的地址。 |
| 差旅和費用 | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | 未正確評估費用報表核准工作流程條件。 |
| 差旅和費用 | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | 費用報表原則沒有正確評估專案識別碼。 |
| 差旅和費用 | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | **對公司間費用交易分割至個人** 動作沒有正常運作。 |
| 差旅和費用 | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | 刪除特定差旅申請時，意外刪除費用報表明細的事由說明。 這會在費用報表與差旅申請的記錄識別碼相同時發生。 |
| 差旅和費用 | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | 當費用報表原則要求 **專案識別碼** 欄位時，費用行動應用程式發生問題。 |
| 差旅和費用 | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | 無法編輯與專案相關聯的公司間費用。 反而會顯示下列錯誤訊息：「物件參考未設定為物件的執行個體。」 |
| 差旅和費用 | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | 將費用報表過帳後，銀行子分類帳中列出錯誤的貨幣和金額。 |
| 差旅和費用 | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | 對 *刪除信用卡交易* 功能進行改善。  |
| 差旅和費用 | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | 在法律實體中指定不同的報表貨幣時，未一致計算費用報表中所含的銷售稅。 |
| 差旅和費用 | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | 將新的現金差旅費用加入時，效能受到影響。 |
| 差旅和費用 | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | 費用報表上未觸發費用原則規則。 |
| 差旅和費用 | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | 使用資料管理架構上傳新的共用類別時，會移除所有共用類別的所有子類別。 |
| 差旅和費用 | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | 當您建立費用明細，再接著選取類別時，顯示下列錯誤訊息：「銷售稅群組 DOM 與項目銷售稅群組 STD 的組合無效。」 |
| 差旅和費用 | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | 費用行動應用程式發生同步處理問題。 |
