---
title: 庫存/生產型案例適用的 Project Operations 2021 年 10 月新增功能或變更
description: 本文提供有關庫存/生產型案例適用 Project Operations 2021 年 10 月發行版本中所提供之品質更新的資訊。
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029933"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>庫存/生產型案例適用的 Project Operations 2021 年 10 月新增功能或變更

_**適用於：** 庫存/生產型案例適用的 Project Operations_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dynamics 365 Finance 環境 10.0.22 版中的專案管理與會計
 
## <a name="quality-updates"></a>品質更新

| 功能區域 | 參考編號 | 品質更新 |
|--------------|------------------|----------------|
| 專案管理與會計 | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | 進行公司間客戶發票過帳時，無法正確沖回專案在製品 (WIP) 及應計收入金額。 |
| 專案管理與會計 | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | **如果有未結交易，則防止專案關閉** 功能無法運作。 |
| 專案管理與會計 | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | 啟用該功能時，任意文字發票上的帳單分類不會自動填入專案中的維度。 |
| 專案管理與會計 | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | 在非公司間案例中，進行專案發票過帳時，無法正確沖回 WIP 及應計收入金額。 |
| 專案管理與會計 | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | 將 Microsoft Excel 增益集與專案費用帳目搭配使用時，且 **抵銷科目類型** 欄位設定為 **專案** 時，借方值和貸方值會對調。 |
| 專案管理與會計 | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | 在包含庫存項目且於標示 **UseTax** 時有非扣除稅額的專案採購單上，專案交易中所過帳的金額有多報的情形。 |
| 專案管理與會計 | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | 系統會在專案損益表與專案 WIP 報表之間分割金額。 |
| 專案管理與會計 | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | 調整部分傳回的項目需求之後，現有庫存量不正確。 |
| 專案管理與會計 | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | 在 Microsoft Project 中編輯資源名稱時，這些名稱會在 Project Operations 中發生重複。 |
| 專案管理與會計 | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | 含有應付帳款公司間待處理廠商發票成本的公司間費用報表首先會過帳到 **專案 WIP 成本** 過帳類型。 但是在處理期間，估計相關成本會過帳到的是 **專案成本** 過帳類型，而不是預期的 **公司間成本** 過帳類型。 |
| 專案管理與會計 | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | 無法顯示專案費用交易中的廠商保留款結果。 |
| 專案管理與會計 | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | 時程表對所有的會計分配及總帳配置分錄，都必須將交易貨幣計價的交易金額捨入至指定的小數位數。 |
| 專案管理與會計 | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | 確認計畫訂單時，專案項目需求的數量會自動更新。 |
| 專案管理與會計 | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | 憑單號碼、交易類型廠商餘額和科目編號無法在採購單的預付款發票上進行沖回。 |
| 專案管理與會計 | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | 開啟廠商發票整合時，會中斷公司間廠商發票。 |
| 專案管理與會計 | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | 建立專案費用帳目時，成本金額會顯示在 **貸方** 欄位中。 |
| 專案管理與會計 | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | 專案發票的付款條件無法依預期發揮作用。 |
| 專案管理與會計 | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | 將編號序列設定為連續時，可能會重複使用時程表憑單。 |
| 專案管理與會計 | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | 法國：**手動留成金額** 邏輯與專案合約發票提案中的 **自動留成金額** 邏輯不相符。 |
| 專案管理與會計 | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | 釋放廠商付款留成時，憑單過帳的額外明細不正確。 |
| 專案管理與會計 | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | 變更 **建立發票提案** 頁面上的 **發票日期** 欄位時，可能發生下列錯誤：「物件參考未設定為物件的執行個體。」 |
| 專案管理與會計 | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | 嘗試從 **TSLine** 工作流程核准時程表，且有適用於星期六和星期日的時程表原則時，會發生錯誤。 |
| 專案管理與會計 | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | 計算發票提案的發票總額時，**發票提案交易摘要** 中不包含期初餘額專案項目類型。 |
| 專案管理與會計 | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | 如果專案生產訂單的耗用成本為 0 (零)，當您嘗試估計時，會發生下列錯誤：「嘗試除以零。」 |
| 專案管理與會計 | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Android 適用的專案時程表行動應用程式停止回應。 此問題與 **TimeEntryDataManager ArgumentNullException** 有關。 |
| 專案管理與會計 | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operations 整合帳目過帳時，會因為科目缺少維度而失敗。 然而，缺少維度的科目並不是您要過帳到的科目。 |
| 專案管理與會計 | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | 從 **過帳成本** 頁面的 **選取** 對話方塊中移除搜尋中的 **ToDate** 篩選時，無法將其清除。 |
| 專案管理與會計 | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **重設所有分配** 失敗，而且類型為 **只有時間** 的專案所建立的時程表會顯示錯誤。 |
| 專案管理與會計 | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | 將採購類別指派至項目時，無法編輯待處理廠商發票上的 **專案** 索引標籤。 |
| 專案管理與會計 | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | 如果您沒有登入 Project Operations Dataverse，就會找不到導覽窗格。 |
| 專案管理與會計 | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | 公司間專案調整交易會在目的地公司中出現問題。 |
| 專案管理與會計 | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | 如果採購單是由總帳中的 **採購單年終程序** 所處理，則專案的已認可成本會計算出錯誤的數量和成本價。 |
| 專案管理與會計 | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | 將具有品質訂單的專案生產訂單報表報告為已完成時，會發生下列錯誤：「沒有任何以庫存交易標示的虛擬交易。」 |
| 專案管理與會計 | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | 將專案相關應付帳款發票過帳時，會發生下列錯誤：「列舉文字專案 - 成本 - 項目不存在。」 |
| 專案管理與會計 | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | 手動計入收入時，間接成本會加倍。 |
| 專案管理與會計 | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | 應計收入和 WIP 過帳不會產生交易。 |
| 專案管理與會計 | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | 有收到的專案採購單時，標準成本項目啟用待定價格會失敗。 |
| 專案管理與會計 | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | 發票過帳的 WIP 沖回值與時間項目的原始已過帳 WIP 值不同。 |
| 專案管理與會計 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 在憑單中交易未達借貸平衡之已套用保留款的案例中，專案的已開發票收入有過帳問題。 |
| 專案管理與會計 | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | 在將發票提案過帳之後建立估計值，會阻止匯入 Project Operations 中的更正明細。 |
| 專案管理與會計 | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | 應該會無法修改已完整開立發票的里程碑記錄。 |
| 專案管理與會計 | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | 使用自動收費時，無法將時程表的公司間客戶發票過帳，而會顯示錯誤訊息。 |
| 專案管理與會計 | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | 無法正確更新子專案上的地址。 |
| 專案管理與會計 | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | 項目需求的成本價會以合併採購單的購買價來更新。 |
| 專案管理與會計 | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | 更新採購價並啟用 **啟動變更管理** 參數之後，過帳的成本不正確。 |
| 差旅和費用 | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | 在費用行動應用程式中搜尋類別時，您可以看到所有的使用者費用。 |
| 差旅和費用 | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | 從根據信用卡交易所建立之費用進行過帳的廠商交易及銷售稅交易金額不正確。 |
| 差旅和費用 | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | 重新整理費用報表頁面時，顯示不相關的警告訊息。 |
| 差旅和費用 | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | 刪除臨時核准者後，再透過工作流程重新提交時，會使用錯誤的臨時核准者。 |
| 差旅和費用 | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | 發生與里程碑設定相關的過帳錯誤。 |
| 差旅和費用 | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | 將未附加的交易重新加入至公司間費用的費用報表時，分配並不會更新法律實體。 |

### <a name="regulatory-updates"></a>法規更新

如需有關 財務和營運應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。 您也可以登入 Microsoft Dynamics Lifecycle Services (LCS)，並使用問題搜尋工具來檢視規劃的法規更新資訊。 問題搜尋可讓您依據國家或地區、功能類型以及發行版本來進行搜尋。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
