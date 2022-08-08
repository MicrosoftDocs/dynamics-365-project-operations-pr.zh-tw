---
title: 庫存/生產型案例適用的 Project Operations 2021 年 7 月新功能或變更
description: 本文提供有關庫存/生產型案例適用 Project Operations 2021 年 7 月發行版本中所提供之品質更新的資訊。
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: c04d0465f5f7dd43ba50d4c0d2937b45fed6df86
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028830"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>庫存/生產型案例適用的 Project Operations 2021 年 7 月新功能或變更

_**適用於：** 庫存/生產型案例適用的 Project Operations_

這篇文章適用於下列 Dynamics 365 Project Operations 元件和版本：

- Dynamics 365 Finance 環境 10.0.20 版中的專案管理與會計
 
### <a name="quality-updates"></a>品質更新
                                                                                                                                                                                  
| 功能區域                      | 參考編號| 品質更新                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 專案管理與會計 | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | 一旦因提出採購申請而發佈採購單，就會立即清除採購申請中的成本承諾記錄。                                                                           |
| 專案管理與會計 | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | 對採購申請進行兩次預算驗證。 這種重複情形意味著，無法關閉申請，且未建立對應的採購單。                                                                                                                        |
| 專案管理與會計 | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | **據以收費的百分比** 帳單規則因此捨入問題而無法完成。                                                                              |
| 專案管理與會計 | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | 當您調整交易記錄，而百分比有小數點時，無法正確調整成本與銷價。                                      |
| 專案管理與會計 | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | 會計來源總管會針對多個有不同活動的工時單明細，顯示單一工時單明細的時數。                                      |
| 專案管理與會計 | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | 已儲存的檢視表與工時單明細詳細資料個人化會造成系統在嘗試開啟工時單時，永遠開啟清單中第一個工時單的詳細資料。  |
| 專案管理與會計 | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | 匯入後，專案根節點消失，且分工結構圖記錄遭刪除。                                                                                             |
| 專案管理與會計 | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | 從項目需求接收並簽發項目時，系統會更新錯誤的預算消耗量餘額。 |
| 專案管理與會計 | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | 專案保留款採購單在 **總計** 窗格或 **待處理發票** 網格中沒有正確顯示總計。                                                                  |
| 專案管理與會計 | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | 結轉庫存時，專案項目成本調整會過帳至資產負債科目，而不是損益科目。                                                            |
| 專案管理與會計 | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | 專案已過帳交易憑單和估計憑單使用美元做為會計貨幣，但金額顯示的卻是加拿大幣等值金額。              |
| 專案管理與會計 | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | 項目需求與採購單的承諾成本在處理部分產品及部分開票的採購單發票程序中是錯誤的。       |
| 專案管理與會計 | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | 專案調整不正確地根據間接成本更新銷售金額。                                                                                    |
| 專案管理與會計 | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | **工時單** 表格缺少與 **工作人員/資源** 檢視表的已定義關聯。                                                                                   |
| 專案管理與會計 | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | 從公司間工時單的下拉式功能表中選取 **活動編號** 欄位時，無法填入該欄位。                                                                 |
| 專案管理與會計 | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | 您無法將個人化 **用途** 或 **活動描述** 欄位新增至下列頁面：**專案已過帳交易**、**發票提案建立** 或 **發票提案**。  |
| 專案管理與會計 | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | 使用資料管理 (**ProjSalesItemRequirementEntity**) 建立專案需求時，系統提供錯誤的交貨日期控制項。                                              |
| 專案管理與會計 | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | 在 Finance 中選取專案合約識別碼時，Project Operations 整合環境開啟用於建立新記錄的頁面，而不是開啟現有的專案合約。                                                                                                                 |
| 專案管理與會計 | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  標籤「@SYS4083080」(「找不到與輸入的值對應的唯一工作人員記錄」) 未翻譯為丹麥文。                                |
| 專案管理與會計 | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | 無法編輯發票提案中的 **項目銷售稅群組** 欄位。                                                                               |
| 專案管理與會計 | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | 承諾成本多報了非扣除稅額。                                                                                                    |
| 專案管理與會計 | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | 使用多個專案和不同財務維度進行公司間工時單過帳時，會在總分類帳中產生非預期值。                             |
| 專案管理與會計 | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | 發票提案明細因定期程序 **從臨時表格匯入** 的多個執行個體同時執行而發生重複。                                      |
| 專案管理與會計 | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | 貸項通知發票提案過帳發生錯誤，因此憑單上的交易不平衡。    |
| 專案管理與會計 | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | 發佈暫停的待處理發票後，專案承諾成本變得不正確。                                                                             |
| 專案管理與會計 | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | 當稅金使用的貨幣與公司貨幣不同時，您無法建立專案銷售訂單的貸項通知。                                      |
| 專案管理與會計 | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | 刪除合約也會刪除與客戶相關聯的地址。                                                                                     |
| 專案管理與會計 | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | 無法過帳負值時間交易更正所產生的發票提案。                                                                    |
| 差旅和費用                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | 稅金在費用報表中是以不同的方式來計算。                                                                                                                  |
| 差旅和費用                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | 版本更新 **DB72_Expense.updateTrvExpTransProjTransId()** 不允許 **trvExpTrans.ReferenceDataAreaId** 建立新的號碼序列。                    |
| 差旅和費用                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | 金額欄位未與必要欄位一起顯示。                                                                                                             |
| 差旅和費用                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | 使用重新設計過的費用使用者介面改善將費用附加至費用報表的效能。                                                            |
| 差旅和費用                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | 您可以刪除已過帳的費用報表。                                                                                           |
| 差旅和費用                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | 費用原則訊息多次顯示。                                                                                                       |
| 差旅和費用                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | **付款方式** 欄位已包含在 **新增費用** 窗格中。                                                                                                      |
| 差旅和費用                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | 如果找不到工作流程，則 **重設費用單據狀態** 工具應該會將費用報表狀態重設為 **草稿**。 

### <a name="regulatory-updates"></a>法規更新
如需有關 財務和營運應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。 您也可以使用問題搜尋工具登入 Lifecycle Services (LCS)，並檢視規劃的法規更新。 問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
