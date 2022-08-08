---
title: 庫存/生產型案例適用 Project Operations 2021 年 4 月的新功能或變更
description: 本文提供有關庫存/生產型案例適用 Project Operations 2021 年 4 月發行版本中所提供之品質更新的資訊。
author: andchoi
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 74cace069e0b5a982e6ea1df0607ff72f1911a0f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028144"
---
# <a name="whats-new-or-changed-in-project-operations-april-2021-for-stockedproduction-based-scenarios"></a>庫存/生產型案例適用 Project Operations 2021 年 4 月的新功能或變更

_**適用於：** 庫存/生產型案例適用的 Project Operations_

這篇文章適用於下列 Dynamics 365 Project Operations 元件和版本：

- Dynamics 365 Finance 環境 10.0.18 版中的專案管理與會計
 
### <a name="quality-updates"></a>品質更新
                                                                                                                                                                                  
| 功能區域                      | 參考編號| 品質更新                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 專案管理與會計 | [534393](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534393) | **專案排序** 網格中發生錯誤。                                                                                                                                                      |
| 專案管理與會計 | [542850](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542850) | 更正專案採購單的單價和數量之後，認可的金額有些誇大。                                                                                    |
| 專案管理與會計 | [543645](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543645) | 宣告 **ProjParameters** 變數，但從未在使用此變數前指派記錄緩衝區。                                                                                     |
| 專案管理與會計 | [543674](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543674) | 執行 **填入所有公司的專案資源** 批次作業時，刪除 **ResRollup** 資料表。                                                                          |
| 專案管理與會計 | [544417](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544417) | 使用 **採購單明細 V2** 實體更新採購單的 **專案銷售價** 欄位時，發生問題。                                                                           |
| 專案管理與會計 | [547652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547652) | 視身分證號碼而定，無法建立子專案。   發生下列錯誤：「不正確地呼叫了函式 Global::int642int。」                                         |
| 專案管理與會計 | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | 開立採購單的發票，且這張發票包含採購類別及項目時，客戶收到錯誤的科目。                                                                      |
| 專案管理與會計 | [509920](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509920) | 將包含間接成本的專案交易從可計費調整為不應計費後，又重新調整為可計費時，無法正確結算 WIP。                                       |
| 專案管理與會計 | [511274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=511274) | 在銷售訂單中使用保留期和總折扣時，發票金額不正確。                                                                                          |
| 專案管理與會計 | [511315](https://fix.lcs.dynamics.com/Issue/Details/?bugId=511315) | 即使選取不同的交易類型時，也不會變更明細詳細資料上的地址名稱。                                                                           |
| 專案管理與會計 | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | 在使用部分產品收據和部分發票的採購單發票程序中，項目需求和採購單的已認可成本不正確。                       |
| 專案管理與會計 | [524226](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524226) | 專案的財務維度變更時，採購單標題未反映變更。                                                                                                  |
| 專案管理與會計 | [524979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524979) | 產生的 **固定價格專案** 報表為空白。                                                                                                         |
| 專案管理與會計 | [529445](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529445) | 審查 **背靠背式付款** 頁面上的廠商發票時，發票未選擇專案識別碼參考。                                                                          |
| 專案管理與會計 | [529982](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529982) | 工時表分錄對一個法律實體在 **人資經理** 角色中存取權受限的使用者來說不正確，因為類別設定的預設值不正確。                                         |
| 專案管理與會計 | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | 未在調整中考慮原始專案日期，這會在 **使用調整日期做為新的專案日期** 欄位設定為 **否** 時造成錯誤。                                             |
| 專案管理與會計 | [530788](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530788) | 使用批次計算專案估計值時，結果不正確。                                                                                                         |
| 專案管理與會計 | [530834](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530834) | 專案合約上的已花費金額與專案上的記帳金額不一致。                                                                             |
| 專案管理與會計 | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | 專案會計師與專案經理角色無法建立含核准群組設定的時數帳目。                                                                                 |
| 專案管理與會計 | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | 無法過帳 Microsoft Excel 匯入的費用帳目。                                                                                                                                       |
| 專案管理與會計 | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | 允許公司間案例中的廠商交易沖回，包括廠商發票和費用報表。                                                                     |
| 專案管理與會計 | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | 專案調整不正確地根據間接成本更新銷售金額。                                                                                                    |
| 專案管理與會計 | [534869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534869) | 建立固定價格專案發票的貸項通知，且其使用的是交貨單位帳單規則時，解除的單位數無法用於重新開單。 |
| 專案管理與會計 | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | 具有不同貨幣的專案合約未在項目帳目或發票提案上正確計算會計貨幣。                                                   |
| 專案管理與會計 | [537158](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537158) | 變更採購單明細上的專案，以轉移項目需求。                                                                                                                          |
| 專案管理與會計 | [540603](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540603) | 從預測匯入專案預算會產生不正確的金額。                                                                                                                    |
| 專案管理與會計 | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5406222) | 將交易從可計費調整為不計費時，不會建立任何總帳分錄。                                                                                            |
| 專案管理與會計 | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | 開啟功能金鑰 **啟用專案廠商發票保留條款的成本金額計算功能** 時，不會以背靠背條款來建立專案交易。                  |
| 專案管理與會計 | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | **建立發票提案** 頁面有多個問題。                                                                                                                             |
| 專案管理與會計 | [543390](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543390) | **所有專案** 頁面未以新的語言代碼顯示清單。                                                                                                            |
| 專案管理與會計 | [543803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543803) | 修訂預算超過兩次時，專案預算餘額中未核准的預算金額不正確。                                                                |
| 專案管理與會計 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | **採購合約** 頁面無法顯示在與 Project Operations 整合的 Finance 法律實體中。                                                                               |
| 專案管理與會計 | [545456](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545456) | 正確的憑單日期未上傳至專案時數帳目明細。                                                                                                            |
| 專案管理與會計 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | 在資源型案例適用的 Project Operations 中，因為整合錯誤，您無法將報價轉換為已成交。                                                                      |
| 專案管理與會計 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | 在 Project Operations 中，因為檢查是否有重疊合約服務內容與交易類型，您會在嘗試建立合約服務內容與專案識別碼之間的關聯時收到錯誤訊息。                        |
| 專案管理與會計 | [546949](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546949) | 當 **ProjValEmplProjSetup** 資料表中有 14,000 筆以上的記錄時，**資源/專案驗證群組** 頁面會發生效能問題。                                                                     |
| 專案管理與會計 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 可以設定不同客戶的資金來源發票地址。                                                                                   |
| 專案管理與會計 | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | 發行版本 10.0.15 之後，資源的標準查詢無法使用。                                                                                          |
| 專案管理與會計 | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | 採購單發票憑單上的總帳科目及過帳類型與服務項目不相符。 專案群組設定為 **餘額**，且總帳科目不正確。                   |
| 專案管理與會計 | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | 待處理廠商發票未顯示活動編號，即使 **封鎖上層活動選取** 設定為 **否**，也無法顯示。                                            |
| 專案管理與會計 | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | 使用導覽路徑 **專案** > **預算** > **修訂** > **新增** > **匯入** 時，系統會為所有專案建立專案預算修訂。                                                            |
| 專案管理與會計 | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) | 根據不同交易及會計貨幣調整交易時，出現錯誤的過帳及總帳分錄。                                                                        |
| 專案管理與會計 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | 在建立交易的過帳發票時，未包含任何維度。                                                                                                   |
| 專案管理與會計 | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | 建立未與任何造成效能問題之採購單連結的待處理廠商發票時，呼叫 **PurchTotals.purchNewTotalAmount()** 方法。                    |
| 差旅和費用                | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | 發生與里程設定相關的過帳錯誤。                                                                                                                                          |
| 差旅和費用                | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | 外幣費用交易的 **分攤至個人** 功能無法運作。                                                                                                         |
| 差旅和費用                | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | 無論是否將 **代理人** 設定為資源，[費用類別] 下拉式功能表都會顯示不正確的類別。                                         |
| 差旅和費用                | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | 您無法儲存公司間費用報表，因為發生資源/類別驗證錯誤。                                                                                             |
| 差旅和費用                | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | 費用報表過帳中的錯誤里程費率計算有分割明細。                                                                                                        |
| 差旅和費用                | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | 包含銷售稅，且付款方式上的抵銷科目類型為 **工作者** 時，您無法將公司間費用報表過帳。                                                   |
| 差旅和費用                | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | 復原對 **TrvRequisitionLine** 資料實體的變更以及關聯至該實體的唯一索引。                                                                                            |
| 差旅和費用                | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | 新增在費用報表中特定點上的記錄功能，以支援建立和更新來源單據明細。                                                                                           |
| 差旅和費用                | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 如果銷售稅已過帳至目的地法律實體，則會在公司間案例中提供錯誤的子分類帳日記帳。                                              |
| 差旅和費用                | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | 在 Project Operations 中，從 Dataverse 移除費用估計值時，並未將其從 Finance 中刪除。                                                                                         |
| 差旅和費用                | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 當費用類別屬於非專案類別時，在 **費用** 頁面上選取的財務維度未複製到費用報表。                                          |

### <a name="regulatory-updates"></a>法規更新
如需有關 財務和營運應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。 您也可以使用問題搜尋工具登入 LCS 並查看計畫的法規更新。 問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
