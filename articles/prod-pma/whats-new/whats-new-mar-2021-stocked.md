---
title: 庫存/生產型案例適用 Project Operations 2021 年 3 月的新功能或變更
description: 本主題提供有關 2021 年 3 月所發行庫存/生產型案例適用 Project Operations 中提供之品質更新的資訊。
author: andchoi
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: d1a4658c8eec23f6816b58de42d785d769050b07
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997006"
---
# <a name="whats-new-or-changed-in-project-operations-march-2021-for-stockedproduction-based-scenarios"></a>庫存/生產型案例適用 Project Operations 2021 年 3 月的新功能或變更

_**適用於：** 庫存/生產型案例適用的 Project Operations_

此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

- Dynamics 365 Finance 環境 10.0.17 版本的專案管理與會計

## <a name="features-included-in-this-release"></a>此版本包含的功能
此版本包含下列功能：

  - [專案發票提案績效](../project-invoice-proposal-performance.md)
 
### <a name="quality-updates"></a>品質更新

| 功能區域                        | 參考編號 | 品質更新                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 專案管理與會計 | [420064](https://fix.lcs.dynamics.com/Issue/Details/?bugId=420064) | 重新計算庫存之後，未更新負數的已過帳專案交易。                                                                                                                      |
| 專案管理與會計 | [438692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=438692) | 如果沒有任何為資金來源配置的交易或發票，則應該可以刪除資金來源。                                                                                                           |
| 專案管理與會計 | [439470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=439470) | 實際估計交易未顯示前期的費用和項目交易。                                                                                                       |
| 專案管理與會計 | [452710](https://fix.lcs.dynamics.com/Issue/Details/?bugId=452710) | 專案項目需求裝箱單的總帳描述值不正確。                                                                                                              |
| 專案管理與會計 | [455602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=455602) | 對專案的帳目進行過帳時，財務維度並不會從憑單中的員工與項目挑選。                                                                               |
| 專案管理與會計 | [472988](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472988) | 更新專案發票總計中的明細淨金額時，銷售金額會填入已過帳交易中已調整的金額。                                                                               |
| 專案管理與會計 | [477969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477969) | 審查 **背靠背式廠商發票** 頁面上的廠商發票明細時，發票未選取專案識別碼參考。                                                                                                   |
| 專案管理與會計 | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | 合約金額在有多個資金來源的固定價格專案的 **記帳** 頁面上不正確。                                                                                                  |
| 專案管理與會計 | [481443](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481443) | 即使在將抵銷項過帳之後，固定價格專案的應計收入也未調整。                                                                                                                                |
| 專案管理與會計 | [483209](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483209) | 透過發票提案開立專案銷售訂單發票時，未更新貸項通知單狀態。                                                                                                  |
| 專案管理與會計 | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | 當採購單已開發票且發票包含採購類別及項目時，客戶會收到錯誤的帳戶資訊。                                                                                              |
| 專案管理與會計 | [484817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484817) | 透過定期批次作業所產生的專案發票提案具有金額為零的重複交易。                                                                                                  |
| 專案管理與會計 | [486817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486817) | 執行專案損益報表時，移除錯誤限制檢查。                                                                                                                                  |
| 專案管理與會計 | [488076](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488076) | Expenses that are posted through intercompany recharge don't show the profit and loss entry 使用 **時間與材料專案代碼** 的 **過帳成本** 功能時，透過公司間轉記進行過帳的費用未顯示損益分錄。                                                         |
| 專案管理與會計 | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | 固定價格專案的已過帳專案交易中的 **發票狀態** 篩選無法運作。                                                                                                   |
| 專案管理與會計 | [488783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488783) | 工時表分錄因為代理人記錄重複而重複。                                                                                                                                           |
| 專案管理與會計 | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | 沖回估計抵銷項無法在 **週期** 中正常運作。                                                                                                                                                 |
| 專案管理與會計 | [498010](https://fix.lcs.dynamics.com/Issue/Details/?bugId=498010) | 新增其他範圍時，無法從 **專案管理與會計** 模組的 **調整交易** 選項中選取適當的資料。 **其他** 篩選會被忽略。                      |
| 專案管理與會計 | [508494](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508494) | 錄製工作之後，您無法重設生產訂單的狀態。                                                                                                              |
| 專案管理與會計 | [509716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509716) | 專案中具有自動預留及可承諾能力 (CTP) 的項目無法保留。                                                                                                                      |
| 專案管理與會計 | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | **會計調整** 功能在已選取 **不允許手動輸入** 的總帳科目上產生問題。                                                                     |
| 專案管理與會計 | [510079](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510079) | 抵銷估計值時，專案報表上的 **應計收入 - 銷售值** 欄位不應顯示任何值。                                                                                 |
| 專案管理與會計 | [510607](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510607) | 使用角色定價之專案調整中的成本價和銷售價不正確。                                                                                                                        |
| 專案管理與會計 | [10728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=10728) | 在 Project Operations 中，進行部分保留款更正之後，保留款更正發票無法運作。                                                                                                                   |
| 專案管理與會計 | [510743](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510743) | 只有在您取消公司間採購單時，才應啟用 **移除連結** 選項。                                                                                                                                          |
| 專案管理與會計 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | 公司間專案發票請款中的 WIP 銷售值過帳選擇了非預期的科目。                                                                                                                  |
| 專案管理與會計 | [514432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514432) | 當發票提案包含針對貸項通知單所選取的明細時，未重新計算帳單規則中的服務費。                                                                                            |
| 專案管理與會計 | [515820](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515820) | 尚未對費用交易執行專案發票提案時，聯邦獎勵支出時間表查詢 (Schedule of Expenditures of Federal Awards Inquiry) 顯示收據金額。                                               |
| 專案管理與會計 | [516301](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516301) | WIP 成本在服務項目有 **餘額** 專案群組的專案報表中不正確。                                                                                               |
| 專案管理與會計 | [516553](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516553) | 無法對與專案相關的任意文字發票進行更正。                                                                                                                                                  |
| 專案管理與會計 | [517074](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517074) | 將專案交易調整為零銷售價時，會建立新的含發票狀態為 **不應收費** 的已調整交易。                                                               |
| 專案管理與會計 | [517414](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517414) | 如果同時調整多個明細，進行專案調整過帳時會發生問題。                                                                                                                               |
| 專案管理與會計 | [518001](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518001) | 如果將裝箱單過帳後，產品成本價和項目需求數量變更，則會以不正確的成本金額過帳調整。                                                                   |
| 專案管理與會計 | [518092](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518092) | 直接交貨採購單的財務維度不正確，且已由銷售訂單財務維度所取代。                                                              |
| 專案管理與會計 | [518605](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518605) | 預測數量為零時，負值數量專案帳目明細不會更新預測。                                                                                        |
| 專案管理與會計 | [518657](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518657) | 嘗試使用 Microsoft Excel 匯入項目需求，造成收據日期錯誤。                                                                                                                                                    |
| 專案管理與會計 | [519200](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519200) | 將發票過帳時，未更新廠商發票交易的專案項目交易參考。                                                                                               |
| 專案管理與會計 | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | 將專案發票提案過帳時，可能會發生下列錯誤：「新增扣減的預付款發票時，交易在報表貨幣上未達借貸平衡」。                                                                    |
| 專案管理與會計 | [520268](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520268) | 如果您使用專案版面配置，則不會在 **廠商付款保留** 報表中填入專案識別碼和專案名稱。                                                                                              |
| 專案管理與會計 | [520872](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | 透過資料實體建立專案時，總帳過帳排序優先順序不正確。                                                                                                                      |
| 專案管理與會計 | [521150](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521150) | 在根據採購單 (含廠商保留款) 所產生的已過帳專案交易上，成本金額不正確。 這會導致在固定價格專案的專案報表和成本控制中產生不正確的值。 |
| 專案管理與會計 | [521374](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521374) | 更新標題時，專案銷售報價不正確地更新單價。                                                                                                                    |
| 專案管理與會計 | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | 在 Project Operations 中使用保留款時，在開立預付款發票後變更預設專案，稍後會在接踵而來的扣款上發生問題。                                                                        |
| 專案管理與會計 | [521857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521857) | 更新廠商發票及專案銷售價發票日期的功能已變更。                                                                                                                                  |
| 專案管理與會計 | [522897](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | 當您調整具有不同匯率的公司間交易時，會發生問題。                                                                                                                |
| 專案管理與會計 | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | 在使用部分產品收據和部分發票的採購單發票程序中，項目需求和採購單的已認可成本不正確。                                                |
| 專案管理與會計 | [523960](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523960) | 使用匯率沖回估計值時，出現不正確的值。                                                                                                                                             |
| 專案管理與會計 | [524242](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524242) | 工作層級的分工結構圖範本會自動清除時數投入量。                                                                                                                         |
| 專案管理與會計 | [524911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524911) | 將報價的狀態更新為 **未成交** 時，所有您已開始且狀態為 **已建立** 或 **已傳送** 的報價也會更新為 **未 成交**。                 |
| 專案管理與會計 | [525182](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525182) | 如果交貨日期是在未來，則發票提案中看不到銷售發票。                                                                                                                  |
| 專案管理與會計 | [526180](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526180) | **專案項目帳目明細** 實體的商務規則已有所變更。                                                                                                                                          |
| 專案管理與會計 | [526522](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526522) | 公司間客戶發票的應計收入不符合工時表及外幣重估。                                                                                 |
| 專案管理與會計 | [526650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526650) | 從專案採購申請或專案建立專案採購單明細的交貨提醒之後，錯誤地計算已認可成本。                    |
| 專案管理與會計 | [526812](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526812) | 調整專案時，可能發生下列錯誤：「庫存單位中未更新財務資料」。                                                                                                             |
| 專案管理與會計 | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | 在 Project Operations 中，從合約移除專案時，如有需要，應重設合約的預設專案。                                                                                       |
| 專案管理與會計 | [527945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527945) | 套用使用稅時，專案中費用的銷售價不正確。                                                                                                                                         |
| 專案管理與會計 | [528020](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528020) | 使用其他發票更新專案採購單明細時，在專案項目需求上過帳錯誤的數量。                                                                                                 |
| 專案管理與會計 | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | 在 Project Operations 中，公司間發票的 **新增明細** 清單中顯示錯誤的費用明細。                                                                                                |
| 專案管理與會計 | [529887](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529887) | 使用發票登記簿和發票核准將交易過帳時，**專案過帳交易** 頁面上的 **廠商帳戶** 欄位是空白。                                                                  |
| 專案管理與會計 | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | 未在調整中考慮原始專案日期，這會在 **使用調整日期做為新的專案日期** 設定為 **否** 時造成錯誤。                                                                     |
| 專案管理與會計 | [530241](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530241) | 交易貨幣與公司貨幣不同時，與專案相關的一般帳目與費用帳目的銷售價計算不正確。                                     |
| 專案管理與會計 | [530658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530658) | 銷售交易未顯示在專案採購單的部分發票憑單上。                                                                                                                          |
| 專案管理與會計 | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | 專案會計師與專案經理角色無法建立含核准群組設定的工時帳目。                                                                                                         |
| 專案管理與會計 | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | 無法將使用 Microsoft Excel 匯入的費用報表過帳。                                                                                                                                                              |
| 專案管理與會計 | [532106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532106) | 無法建立工時表原則，因為 **訊息** 欄位不是使用中。                                                                                                                               |
| 專案管理與會計 | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | 存在公司間案例允許廠商交易沖銷的問題。 這會套用至廠商發票和費用報表。                                                                                 |
| 專案管理與會計 | [532692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532692) | 無法重設已核准工時表上的分配。                                                                                                                                                     |
| 專案管理與會計 | [532843](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532843) | 使用工時與項目帳目的匯率沖回估計值時，出現不正確的值。                                                                                                                  |
| 專案管理與會計 | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | 專案調整不正確地以間接成本來更新銷售金額。                                                                                                                              |
| 專案管理與會計 | [534597](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534597) | 將工時帳目過帳時，出現下列錯誤訊息：「未指定維度值」。                                                                                                                                  |
| 專案管理與會計 | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | 具有不同貨幣的專案合約未在憑單上正確計算會計貨幣。                                                                                              |
| 專案管理與會計 | [535652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535652) | 公司間工時表 WIP 過帳使用了錯誤的銷售 WIP 科目。                                                                                                                                     |
| 專案管理與會計 | [536536](https://fix.lcs.dynamics.com/Issue/Details/?bugId=536536) | 套用折扣並更新倉庫時，專案報價的價格計算錯誤。                                                                                                       |
| 專案管理與會計 | [537905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537905) | 在專案交易中使用項目成本調整後執行重新計算時，出現下列錯誤訊息：「重新計算因錯誤而暫停」。                                                               |
| 專案管理與會計 | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540622) | 累算收入時，若將交易從可計費調整為不計費，則不會建立任何總帳分錄。                                                                                              |
| 專案管理與會計 | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | 開啟專案廠商發票保留功能 **啟用成本金額計算** 時，未以背靠背條款來建立 **ProjTrans**。                                             |
| 專案管理與會計 | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | **建立發票提案** 頁面存在多個問題。                                                                                                                                                     |
| 專案管理與會計 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | 在 Project Operations 中，**採購合約** 頁面無法顯示在與 Project Operations 整合的 Finance 法律實體中。                                                                                             |
| 專案管理與會計 | [544132](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544132) | 進階帳目無法使用已關帳期間內的會計日期進行過帳，即使在 **自動將會計日期設定為下一個開帳期間** 選項已開啟時，也不能。                                                |
| 專案管理與會計 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | 因為 Dataverse 整合錯誤，您無法在 Project Operations 中將報價轉換為已成交。                                                                                                                                       |
| 專案管理與會計 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | 在 Project Operations 中，因為檢查是否有重疊合約服務內容與交易類型，當您嘗試將合約服務內容與專案識別碼建立關聯時，出現錯誤訊息。                                                |
| 專案管理與會計 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 可以設定不同客戶的資金來源發票地址。                                                                                                             |
| 專案管理與會計 | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | 在 10.0.15 更新之後，頁面上資源的標準查詢無法使用。                                                                                                                    |
| 專案管理與會計 | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | 將專案群組設定為 **餘額** 時，總帳憑單上的總帳科目和過帳類型不正確，且非庫存服務項目的採購單憑單上的過帳類型不正確。                                 |
| 專案管理與會計 | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | 待處理廠商發票未顯示活動編號，即使 **封鎖上層活動選取** 設定為 [否]，也無法顯示。                                                                    |
| 專案管理與會計 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | 在 Project Operations 中，當您建立交易的過帳發票時，未選取任何維度。                                                                                                                   |
| 專案管理與會計 | [442814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=442814) | 在 [專案管理與會計] 中，公司間工時表未正確反映轉撥價格的優先順序。                                                                            |
| 專案管理與會計 | [533530](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533530) | 舊版分工結構圖 (WBS) 類別方法  **ProjWBSUpdateController::updateOutlineNumbersAndPublishInPreOrder** 已被取代。                                                                                                   |

### <a name="regulatory-updates"></a>法規更新
如需 Finance and Operations 應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates.md)。 您也可以使用問題搜尋工具登入 LCS 並查看計畫的法規更新。 問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
