---
title: 2020 年 11 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 此主題提供有關資源/非庫存型案例適用的 Project Operations 2020 年 11 月版本所提供的品質更新資訊。
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f6b14a1cbe7f3d41c86aedaf863434214f911eaa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995611"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>2020 年 11 月 - 資源/非庫存型案例適用的 Project Operations 新增功能

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

- CDS 環境的 Project Operations 版本 4.4.0.70
- Dynamics 365 Finance 環境 10.0.14 版本的專案管理與會計

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>更新至資源/非庫存型案例適用的 Project Operations

### <a name="project-operations-on-cds"></a>CDS 上的 Project Operations

| 功能區域                 | 參考編號 | 品質更新                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   商機管理       | 2036993          | 當報價明細類型為 **所有工作** 時，會在贏得報價上更新估計明細和資源指派合約服務內容。                                                 |
| 帳單和定價          | 2070392          | 每次選取 **重新整理發票交易** 時，發票上的專案合約服務內容都會增加。                                                                         |
| 專案規劃             | 2043336          | 無法刪除專案團隊成員記錄。                                                                                                                                  |
| 專案規劃             | 2046013          | 載入期間和變更分時期類型時，估計標籤欄的行為不一致。                                                                                   |
| 專案規劃             | 2046647          | 從專案團隊成員產生資源需求時，開始和結束時間會停用一小時。                                                                      |
| 專案規劃             | 2053879          | （根據即將推出的 CDS 首展）PublishUnassignedAssignments 會在發生錯誤「傳遞給 ConditionOperator.In 的值是空的」時中斷儲存工作的嘗試。                       |
| 專案規劃             | 2055501          | 將 **專案開始日期** 保留空白會造成排程失敗。                                                                                                      |
| 專案規劃             | 2066817          | 無法使用 **工作** 索引標籤上的人員選擇器建立一般資源。                                                                                                   |
| 專案規劃             | 2067034          | **工作的詳細資料** 頁面上無法使用 **檢視詳細資料** 按鈕。                                                                                                       |
| 資源管理          | 2046667          | 即使已履行所有資源，也不會刪除一般團隊成員。                                                                                                    |
| 時間和快速費用項目 | 2047499          | [時間項目] 頁面上的 **新增** 按鈕會開啟 **新電子郵件簽章** 頁面。                                                                                               |
| 時間和快速費用項目 | 2059859          | 建立費用項目時，出現意外的快顯對話方塊。                                                                                                                         |
| その他                        | 2044181          | （解除安裝採購單）嘗試解除安裝 msdyn_ProjectServiceCore_Patch 和 msdyn 專案服務核心解決方案時，會發生錯誤「無法使用記錄」。  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| 功能區域        | 參考編號 | 品質更新                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 收入認列 | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | 當合約使用外幣和完成方法的工作進度百分比時，專案估計完成百分比是錯誤的。                     |
| 收入認列 | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | 無法使用 **實際成本** 完成方法來張貼估計。                                                                                                    |
| 收入認列 | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | 當公司貨幣與交易貨幣不同時，由於傳票不平衡錯誤導致消除失敗。                                              |
| 費用管理  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | 如果是非管理員使用者，則費用明細欄的查詢值（例如 **專案識別碼** 和 **費用類別**）無法正確顯示在資料連接器架構中。 |
| 費用管理  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | 費用類別未顯示明細屬性預設值。                                                                                                         |
| 費用管理  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | 費用整合必須包含來自費用報表的明細屬性。                                                                                             |
| 發票請款           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | 無法過帳專案發票提案，因為錯誤訊息指出 FD 的組合未經過驗證。                                                    |
| 發票請款           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | 無法從 **發票** 詳細資料頁面查看交易。                                                                                                              |
| 發票請款           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | 可以刪除發票提案明細。                                                                                                                                  |
| 專案會計  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | 在 **專案** 清單頁面上看不到 **預測** 功能表項目。                                                                                                   |
| 專案會計  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | 無法開啟 **專案陳述**   > **交易和預測**。                                                                                                       |
| 專案會計  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | 未針對已開立發票的專案交易啟用 **調整會計**。                                                                                                  |
| 專案會計  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | 過帳 **整合** 帳目時，**ProjCDSActualsImport** 資料表上不會包括會計詳細資料。                                                  |
| 專案會計  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | 當您移除然後重新新增資源指派時，專案預測項目會加倍。                                                                            |
| 專案會計  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | 選取 [專案識別碼] 連結時，不會開啟 CDS 深層連結 URL。                                                                                                         |
| 專案會計  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | 無法更新 CDS 中工作的開始日期。                                                                                                                           |
| 專案會計  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | 啟用功能後，不進行 CDS 整合就無法有多個合約服務內容。                                                                                   |

### <a name="regulatory-updates"></a>法規更新
如需 Finance and Operations 應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。 您也可以使用問題搜尋工具登入 LCS 並查看計畫的法規更新。 問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。


[!INCLUDE[footer-include](../includes/footer-banner.md)]