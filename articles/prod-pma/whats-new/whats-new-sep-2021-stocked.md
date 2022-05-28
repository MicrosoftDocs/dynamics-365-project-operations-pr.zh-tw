---
title: 庫存/生產型案例適用的 Project Operations 2021 年 9 月新增功能或變更
description: 本主題提供有關庫存/生產型案例適用 Project Operations 2021 年 9 月發行版本中所提供之品質更新的資訊。
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 24de8626199a3ed56bb6703b78d746ff7a43a089
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582010"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>庫存/生產型案例適用的 Project Operations 2021 年 9 月新增功能或變更

_**適用於：** 庫存/生產型案例適用的 Project Operations_

本主題適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dynamics 365 Finance 環境 10.0.21 版中的專案管理與會計
 
## <a name="quality-updates"></a>品質更新

| 功能區域 | 參考編號 | 品質更新 |
|---|---|---|
| 專案管理與會計 | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | 如果授與採購經理角色一個法律實體的存取權，此角色也會獲得所有法律實體中任何專案的存取權。 |
| 專案管理與會計 | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | 根據原始專案發票結算貸項通知單時，會出現加值稅 (VAT) 捨入問題。 |
| 專案管理與會計 | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | 使用備選專案預算進行預算驗證。 |
| 專案管理與會計 | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | **銷售價格小時** 價格群組不是根據專案報價的分工結構圖計算得出。 |
| 專案管理與會計 | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | 啟用 **啟用專案合約貨幣以計算估計值** 功能時，估計值消除失敗。 |
| 專案管理與會計 | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | 將使用稅金用於專案費用帳目的銷售稅群組時，會將根據數量的銷售稅因式分解新增至售價金額。 |
| 專案管理與會計 | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | 將廠商留成和預付款套用至採購單發票時，未正確計算上次付款的優惠稅額。 |
| 專案管理與會計 | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | 調整追蹤不適用於期初餘額日記帳。 |
| 專案管理與會計 | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **依期間的專案預算訂正撥款** 會分攤到所有預算期間。 提交撥款時，不會清除記錄。 |
| 專案管理與會計 | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | 過帳至總帳的在製品 (WIP)，其金額不正確。 |
| 專案管理與會計 | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | 專案時數帳目的核准無法運作。 |
| 專案管理與會計 | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | 取消融資金限制標示時，無法以間接成本來更新專案調整銷售價。 |
| 專案管理與會計 | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | 當發票已按銷售表抬頭開立，且現有明細的佐證採購單已最終確定時，無法建立項目需求。 |
| 專案管理與會計 | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | 對不同專案各使用一個里程碑的帳單規則，其留成金額不會使用里程碑所選的對應專案識別碼來進行過帳。 反而會以第一個專案來過帳。 |
| 專案管理與會計 | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | 選取發票提案上的 **財務維度集** 時，會發生下列錯誤：「無法將類型為 'Dynamics.AX.Application.FormIntControl' 的物件強制轉換為類型 'Dynamics.AX.Application.FormStringControl'。」 |
| 專案管理與會計 | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | **專案發票** 報表會跳過幾行明細。 |
| 專案管理與會計 | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | 計算投資專案的成本控制時，發生錯誤。 |
| 專案管理與會計 | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | **ProjTable::InitFromCustTable - canDeletePostalAddress** 方法會造成效能問題。 |
| 專案管理與會計 | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | 錯誤訊息應該會比「未預期的錯誤」更明確。 |
| 專案管理與會計 | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | 即使尚未產生發票明細，專案發票過帳批次工作仍會處理並過帳發票提案。 |
| 專案管理與會計 | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | 關閉公共事業授權設定金鑰時，會發生捨入問題。 根據具有多個資料金來源之合約的時程表時數所產生的成本價或銷售價會不正確。 |
| 專案管理與會計 | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | 當銷售價模型為 **貢獻比率** 時，已開發票專案採購單的專案銷售價會計算錯誤。 |
| 專案管理與會計 | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | 系統在計算員工的有效人力費率時，不考慮其間的使用中天數。 |
| 專案管理與會計 | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | 公司間時程表因為下列驗證錯誤而發生過帳錯誤：「法律實體沒有設定任何交易夥伴。」 |
| 專案管理與會計 | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | 已過帳的專案交易清單未擷取具有費用類別之採購單中的描述。 |
| 專案管理與會計 | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | 已過帳至專案的項目帳目有不正確的轉換。 |
| 專案管理與會計 | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | 即使已超過資金限制，您仍然可以確認採購單。 |
| 專案管理與會計 | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | 選取專案識別碼時，任意文字發票上的 **更正/取消發票** 區段會消失。 |
| 專案管理與會計 | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | 根據包含庫存項目的專案銷售訂單將專案發票提案過帳時，會發生效能問題。 |
| 專案管理與會計 | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | 專案採購發票因發生下列錯誤而無法進行過帳：「已不正確呼叫函式 AccDistProcessorProjectExtension.createForProjectRevenueLine。」 |
| 專案管理與會計 | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | 更新 [建立專案估計值] 批次工作以支援執行多個子工作。 |
| 專案管理與會計 | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | 當工作流程停滯於 **已取消** 狀態時，無法將時程表的狀態更新為 **草稿**。 |
| 專案管理與會計 | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | 如果有多個明細，則不會在貸項通知單發票提案中計算留成金額。 |
| 專案管理與會計 | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | 嘗試變更從採購單產生之發票的金額時，發生下列錯誤：「憑單上的交易未依據 XXXX/XX/XX 事項達到借貸平衡。 (會計貨幣：0.00 - 報表貨幣：0.01)。」 |
| 專案管理與會計 | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | 專案發票提案在批次模式下進行過帳時，因與 **GeneralJournalAccountEntry** 聯結而發生效能問題。 |
| 專案管理與會計 | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | 將時程表過帳時，發生效能問題。 |
| 專案管理與會計 | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | 展開所有工作之後，或是手動展開單一工作之後，分工結構圖的成本估計階層未正確對齊。 |
| 專案管理與會計 | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | 無法將專案報價 Excel 範本新增至 **在 Excel 中開啟** 功能表。 |
| 專案管理與會計 | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | 法律實體的免稅號碼未包含在列印的專案發票中。 |
| 專案管理與會計 | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | 根據貸項明細調整專案時，不會更新庫存單位錯誤中的任何財務資料。 |
| 專案管理與會計 | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | 套用 KB 461935 之後，如果您切換至編號序列，就無法將估計值過帳。 |
| 專案管理與會計 | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** 會導致 Android 適用的專案時程表行動應用程式停止回應。 |
| 專案管理與會計 | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | 發票過帳的 WIP 沖回值與原先從時間項目過帳的 WIP 值不同。 |
| 專案管理與會計 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 在已套用保留款的案例中，對專案的已開發票收入進行過帳時，憑單上的交易未達到借貸平衡。 |
| 專案管理與會計 | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | 啟用 **專案資源排程效能增強** 功能時，資源可用性和產能的小數值捨入不正確。 |
| 專案管理與會計 | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | 啟用 **使用多個批次工作建立專案估計值** 功能時，在具有多個子工作的批次中建立估計值的作業只適用於目前的期間。 |
| 差旅和費用 | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | 差旅申請原則遭忽略，而且在不發生錯誤的情況下核准工作流程。 |
| 差旅和費用 | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>行動費用應用程式未將下列資訊儲存在費用明細中：</p><ul><li>專案識別碼</li><li>費用是否為計費項目</li><li>活動編號</li></ul> |
| 差旅和費用 | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | 即使費用明細沒有附上任何收據，**附加的收據** 欄位仍會設定為 **是**。 |
| 差旅和費用 | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | 將費用類別變更為 **個人** 時，發生錯誤。 |
| 差旅和費用 | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | 將信用卡交易分割至個人費用之後，您無法附加收據和編輯上層費用。 |
| 差旅和費用 | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | 費用原則對含有專案識別碼的公司間交易無法正確發揮作用。 |
| 差旅和費用 | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | 已過帳的費用報表缺少過帳日期資訊。 |
| 差旅和費用 | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | 費用行動應用程式發生付款方式問題。 |
| 差旅和費用 | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | 一個工作人員建立的差旅申請可以在委派日期之前用於另一個工作人員的費用報表。 |
| 差旅和費用 | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | 建立費用時，無法在 **費用管理** 工作區的會計分配層級上正確更新財務維度值的變更。 |
| 差旅和費用 | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | 主要費用明細核准狀態未與分項列出的明細工作流程核准狀態同步。 |
| 差旅和費用 | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | 如果您將費用報表過帳，且退稅已啟用時，將會發生錯誤。 |
| 差旅和費用 | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | 代理人無法為離職員工刪除費用憑證。 |
| 差旅和費用 | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | 刪除費用明細所花費的時間超過預期，並會影響效能。 |
| 差旅和費用 | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** 因為只刪除 **SourceDocumentLine** 而產生孤立的 **TaxUncommitted** 記錄。 |
| 差旅和費用 | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** 不會接受 **trvExpTrans.ReferenceDataAreaId** 來建立新的編號序列。 |

## <a name="regulatory-updates"></a>法規更新

如需有關 財務和營運應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。 您也可以登入 Microsoft Dynamics Lifecycle Services (LCS)，並使用問題搜尋工具來檢視規劃的法規更新資訊。 問題搜尋可讓您依據國家或地區、功能類型以及發行版本來進行搜尋。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
