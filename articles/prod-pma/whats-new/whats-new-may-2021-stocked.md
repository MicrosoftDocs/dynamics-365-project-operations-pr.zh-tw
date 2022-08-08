---
title: 庫存/生產型案例適用的 Project Operations 2021 年 5 月新功能或變更
description: 本文提供有關庫存/生產型案例適用 Project Operations 2021 年 5 月發行版本中所提供之品質更新的資訊。
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: eff34a4e9fc1fc6429f1fa7a3e4b0d5b664222f9
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029382"
---
# <a name="whats-new-or-changed-in-project-operations-may-2021-for-stockedproduction-based-scenarios"></a>庫存/生產型案例適用的 Project Operations 2021 年 5 月新功能或變更

**適用於：** 庫存/生產型案例適用的 Project Operations

這篇文章適用於下列 Dynamics 365 Project Operations 元件和版本：

- Dynamics 365 Finance 環境 10.0.19 版中的專案管理與會計
 
### <a name="quality-updates"></a>品質更新
                                                                                                                                                                                  
| 功能區域                      | 參考編號| 品質更新                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 專案管理與會計 | [529751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529751) | 關閉專案項目帳目明細的實體驗證時，匯入失敗。                                                                                                                                                   |
| 專案管理與會計 | [550565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550565) | 與 **GeneralJournalEntry** 查詢相關的 WIP 帳戶報表發生效能問題。                                                                                                                                  |
| 專案管理與會計 | [539044](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539044) | WIP 專案缺少財務維度。                                                                                                                                                                                                    |
| 專案管理與會計 | [540903](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540903) | 發票提案過帳失敗，因為將錯誤的 **ProjBudgetAllocationLineIdSales** 指派給 **ProjBudgetReductionHistory**。                                                                                                                           |
| 專案管理與會計 | [547090](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547090) | 匯入 XML 檔案之後，一般帳目顯示不正確的憑單號碼。                                                                                                                                                              |
| 專案管理與會計 | [552160](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552160) | 分工結構圖範本發生錯誤。                                                                                                                                                                                          |
| 專案管理與會計 | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | 與 Project Operations 整合時，法律實體中的專案管理設定下無法顯示 **表單附註** 和 **表單設定**。                                                                                                             |
| 專案管理與會計 | [553313](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553313) | 取消公司間銷售訂單失敗，發生下列錯誤：「無法編輯採購單明細 (PurchLine) 中的記錄。 由於其他使用者程序刪除該記錄，或變更記錄中的一個或多個欄位，因此發生更新衝突。」 |
| 專案管理與會計 | [553775](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553775) | 專案交易調整為專案成本建立錯誤的財務維度。                                                                                                                                                          |
| 專案管理與會計 | [556751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=556751) | 處理已連接至專案的採購單時，廠商發票會有其他提示。                                                                                                                                                 |
| 專案管理與會計 | [557925](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557925) | 無法核准工時單明細，而且發生下列錯誤：「工作流程的啟用條件無效。 請向系統管理員報告此問題。」                                                                          |
| 專案管理與會計 | [559266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559266) | 如果收到錯誤「無法變更專案合約，因為有相關聯專案 XXXXXX 的交易存在」，您仍然可以變更專案層級上的合約。                                                                           |
| 專案管理與會計 | [560432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560432) | 如果收到錯誤「無法開立此數量的發票，因為狀態為 [已扣除] 的庫存交易不足」，則無法在執行庫存重新計算後過帳採購單發票。                             |
| 專案管理與會計 | [562013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=562013) | 資源要求工作流程已啟用時，如果嘗試使用專案資源可用性控制項來開啟頁面，就會發生效能問題。                                                                                                               |
| 專案管理與會計 | [488320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488320) | 新增帳單規則以將另一個專案指定給專案合約之後，發票狀態會變更為 **不應收費**。                                                                                                                                |
| 專案管理與會計 | [515219](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515219) | 當您從專案採購單移除預付款發票，且 **針對專案過帳預付款成本** 參數已啟用時，會發生錯誤。                                                                                                        |
| 專案管理與會計 | [526439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526439) | 當您過帳專案採購單發票時，錯誤會因為遺失自動項目標記而發生。                                                                                                                            |
| 專案管理與會計 | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | 過帳類型等於專案發票憑單的銷售稅時，加值稅的預設描述為空白。                                                                                                                                           |
| 專案管理與會計 | [530352](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530352) | 如果您刪除相關的已取消項目需求銷售訂單，則專案採購單會顯示錯誤。                                                                                                                                 |
| 專案管理與會計 | [530651](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530651) | 當您標示和取消標示專案項目需求採購單時，參考會遺失。                                                                                                                                                               |
| 專案管理與會計 | [533023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533023) | 列印專案項目需求的挑選清單時，發生縮減數量預設值的問題。                                                                                                                                                 |
| 專案管理與會計 | [535493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535493) | 如果發生超量交貨，計算出的銷售格就不正確。                                                                                                                                                                                 |
| 專案管理與會計 | [541329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541329) | 在發票提案沒有發票數量的情況下解除保留時，會過帳錯誤的保留數。                                                                                                                                                |
| 專案管理與會計 | [541997](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541997) | 產生工時單週期時，第一個週期會顯示為第 53 週。                                                                                                                                                                         |
| 專案管理與會計 | [542043](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542043) | Dynamics 365 Project Service Automation 整合參數中的預設專案類型必須是 [時間和材料] 和 [固定價格]。                                                                                                         |
| 專案管理與會計 | [543096](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543096) | 使用帳單規則刪除發票提案會產生過帳動作。                                                                                                                                                                              |
| 專案管理與會計 | [543463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543463) | 抵銷程序中使用完工百分比法的最終估計值無法抵銷，因為系統未認列營收。                                                                                                                                      |
| 專案管理與會計 | [543938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543938) | 將專案估計值過帳時，不會建立過帳估計記錄。                                                                                                                                                                            |
| 專案管理與會計 | [546885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546885) | 開立公司間發票期間，找不到待處理廠商發票上的主要科目。                                                                                                                                                               |
| 專案管理與會計 | [547885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547885) | 如果合約包含項目需求，就無法新增第二個資金來源。                                                                                                                                                         |
| 專案管理與會計 | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | 當您使用 **專案** > **預算** > **修訂** > **新增** > **匯入** 時，系統會針對所有專案建立專案預算的修訂。                                                                                                                         |
| 專案管理與會計 | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) |  如果您使用不同的交易與會計貨幣來調整交易，則過帳和總帳分錄會不正確。                                                                                                                                       |
| 專案管理與會計 | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | 承諾成本多報了非扣除稅額。                                                                                                                                                                                   |
| 專案管理與會計 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | 建立交易的過帳發票時，不會挑選任何維度。                                                                                                                                                                  |
| 專案管理與會計 | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | 當您建立未與採購單連結的待處理廠商發票時，會呼叫 **PurchTotals.purchNewTotalAmount()** 方法，這會產生效能問題。                                                                                   |
| 專案管理與會計 | [563694](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563694) | **已消耗預算** 和 **剩餘預算** 欄在專案預算餘額上顯示不正確的金額。                                                                                                                                                |
| 專案管理與會計 | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | 工作型帳單與 Project Operations 搭配用於 Dataverse 時，交易會過帳兩次。                                                                                                                                         |
| 專案管理與會計 | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | 使用 Project Operations 時，收入認列的完成百分比不正確。                                                                                                                                                  |
| 專案管理與會計 | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | 在 Project Operations 整合案例中使用待處理廠商發票時，收入應計值增加一倍。                                                                                                                                          |
| 專案管理與會計 | [569736](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569736) | 過帳專案工時單會建立重複的交易。                                                                                                                                                                        |
| 專案管理與會計 | [569819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569819) | 根據工單過帳項目耗用帳目時，發生錯誤。                                                                                                                                  |
| 專案管理與會計 | [571197](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571197) | 無法完成專案生產訂單，因為發生下列錯誤：「物件參考未設定為物件的執行個體。」                                                                                                                           |
| 專案管理與會計 | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | 如果收入設定檔規則設定為 **群組設定**，則無法過帳整合帳目。                                                                                                                                                           |
| 專案管理與會計 | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | 明細有多個度量單位的專案採購單無法進行採購發票過帳。                                                                                                                                             |
| 專案管理與會計 | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | 無法使用 **專案 V2** 資料實體來更新專案的預設財務維度。                                                                                                                                                          |
| 專案管理與會計 | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | 當稅金使用的貨幣與公司貨幣不同時，無法建立專案銷售訂單的貸項通知。                                                                                                                     |
| 專案管理與會計 | [574104](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574104) | 建立有 100 條以上帳單規則的發票提案時，發生問題。                                                                                                                                                                  |
| 專案管理與會計 | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | 建立專案估計值的批次程序需要的時間過長，無法完成。                                                                                                                                                                      |
| 專案管理與會計 | [577785](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577785) | 執行 **在所有公司中填入專案資源** 功能時，發生下列錯誤：「物件名稱 ResRollupCalendar 無效。」                                                                                                                                   |
| 專案管理與會計 | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | 刪除合約時，也會刪除與客戶相關聯的地址。                                                                                                                                                                    |
| 差旅和費用                  | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | 未正確評估費用報表核准工作流程條件。                                                                                                                                                                           |
| 差旅和費用                  | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | 費用報表原則沒有正確評估專案識別碼。                                                                                                                                                                                   |
| 差旅和費用                  | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | 對公司間費用交易的 **分割至個人** 動作沒有正常運作。                                                                                                                                                                |
| 差旅和費用                  | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | 刪除差旅申請時，有時會刪除費用報表明細的事由說明。 這會在費用報表與差旅申請的記錄識別碼相同時發生。                                                            |
| 差旅和費用                  | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | 當費用報表原則要求 **專案識別碼** 欄位時，費用行動應用程式發生問題。                                                                                                                                                |
| 差旅和費用                  | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | 嘗試編輯與專案相關聯的公司間費用時，出現下列錯誤訊息：「物件參考未設定為物件的執行個體。」                                                                           |
| 差旅和費用                  | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | 過帳費用報表後，銀行子分類帳中列出錯誤的貨幣和金額。                                                                                                                                                                |
| 差旅和費用                  | [555462](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5355462) | 關閉具有承諾成本的差旅申請後，未發佈專案的承諾成本。                                                                                                                                              |
| 差旅和費用                  | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | 對 [刪除信用卡交易] 功能進行改善。                                                                                                                                                                                           |
| 差旅和費用                  | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | 在法律實體中指定不同的報表貨幣時，未一致計算費用報表中所含的銷售稅。                                                                                                         |
| 差旅和費用                  | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | 將新的現金差旅費用加入時，效能受到影響。                                                                                                                                                                                         |
| 差旅和費用                  | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | 未在費用報表中觸發費用原則規則。                                                                                                                                                                                            |
| 差旅和費用                  | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | 使用資料管理架構上傳新的共用類別時，會移除所有共用類別的所有子類別。                                                                                                                         |
| 差旅和費用                  | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | 建立費用明細並選取類別時，發生下列錯誤：「銷售稅群組 DOM 與項目銷售稅群組 STD 的組合無效。」                                                                  |
| 差旅和費用                  | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | 費用行動應用程式發生同步處理問題。 

### <a name="regulatory-updates"></a>法規更新
如需有關 財務和營運應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。 您也可以使用問題搜尋工具登入 Lifecycle Services (LCS)，並檢視規劃的法規更新。 問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
