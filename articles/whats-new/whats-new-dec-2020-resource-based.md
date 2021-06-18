---
title: 2020 年 12 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 此主題提供有關資源/非庫存型案例適用的 Project Operations 2020 年 12 月版本所提供的品質更新資訊。
author: sigitac
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e6ff32fff4cce0e848ad6edae827a62e6f33a5aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995791"
---
# <a name="whats-new-december-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>2020 年 12 月 - 資源/非庫存型案例適用的 Project Operations 新增功能

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

- Dataverse 環境的 Project Operations 版本 4.5.0.134
- Dynamics 365 Finance 環境 10.0.15 版本的專案管理與會計

如需有關如何更新至此版本的詳細資訊，請參閱[更新 Finance 環境中的 Project Operations](ur5-nonstocked-installation.md)。

## <a name="features-included-in-this-release"></a>此版本包含的功能
此版本包含下列功能：

  - [公司間開立開票](../project-accounting/intercompany-invoicing-overview.md) 
  - [客戶預付款和保留款](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>更新至資源/非庫存型案例適用的 Project Operations

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能區域                    | 參考編號 | 品質更新                                                                                                                                               |
|---------------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 帳單和定價             | 1986009          | 在專案與合約服務內容連結或取消連結之前進行確認時，手動建立的帳目明細的效能不一致                     |
| 帳單和定價             | 2028174          | 發票明細詳細資料的更新應遵循更正帳目邏輯                                                                                  |
| 帳單和定價             | 2028315          | 可編輯的巢狀網格行為修正                                                                                                                        |
| 帳單和定價             | 2031070          | 調整更正發票明細詳細資料必須符合更正帳目邏輯                                                                              |
| 帳單和定價             | 2034186          | 必須能夠在合約服務內容上更新專案                                                                                                        |
| 帳單和定價             | 2034206          | 從合約服務內容解除專案連結時，實際值沖銷期間必須設定調整狀態                                                        |
| 帳單和定價             | 2040871          | 允許在費用估計值網格上更新單位與單位群組儲存格                                                                                       |
| 帳單和定價             | 2053754          | 從發票編輯建立的實際值未標示為調整狀態和帳單狀態                                                                |
| 帳單和定價             | 2057874          | 更正在發票明細詳細資料編輯期間建立的交易關係                                                                                     |
| 帳單和定價             | 2057875          | 更正在發票明細詳細資料編輯期間建立的交易來源                                                                                        |
| 帳單和定價           | 2057944          | 對於尚未準備好從發票更正中開立發票的實際值，不得超過狀態設定為已認可                                             |
| 帳單和定價           | 2066169          | 更新使用雙重寫入整合時，負值未開單銷售記錄的會計日期                                                            |
| 帳單和定價           | 2067622          | 產生里程碑時應顯示處理圖示                                                                                                |
| 帳單和定價           | 2067624          | 產生里程碑時，應將合約金額標示為業務建議                                                                      |
| 帳單和定價           | 2086880          | 針對專案型報價明細隱藏功能區上的 **建議** 按鈕                                                                                                |
| 帳單和定價           | 2098140          | 顯示整合環境的 **更正發票** 按鈕                                                                                             |
| 部署和設定  | 2101152          | 使用 Power Platform 系統管理中心的 Project Operations 範本建立的新環境，必須執行所有的安裝後作業               |
| 商機管理        | 2086601          | 已停用的角色和類別不應該複製至報價明細和合約服務內容上的應收費角色和應收費類別清單 |
| 專案規劃和追蹤 | 1949065          | 資料顯示性在 200% 縮放時可正確運作                                                                                                                   |
| 專案規劃和追蹤 | 2046317          | 能夠在 Project Operations 中重新命名專案實體                                                                                   |
| 專案規劃和追蹤 | 2057171          | 更新 **專案** 頁面上的 **專案開始日期** 欄位為空白時的錯誤訊息                                                           |
| 專案規劃和追蹤 | 2057197          | 不支援使用工作參照的估計明細複製                                                                                                     |
| 專案規劃和追蹤 | 2060687          | 時區警告現在在特定期間後消失                                                                                                      |
| 資源管理           | 1832887          | 預設資源類別識別碼必須是靜態的，才能確保 Dataverse 和 Finance 環境的可重複資料載入                                                 |
| 時間和費用              | 2081793          | **費用類別名稱** 必須對應至 Finance and Operations 應用程式中的 **費用類別描述** 欄位                                                  |
| 時間和費用              | 2034882          | 安裝 Dynamics 365 Field Service 時，**新增** 按鈕會在命令列中為時間項目顯示兩次                                          |
| 時間和費用              | 2056028          | 更新 **時間編輯** 頁面以包括時間表                                                                                                              |
| 時間和費用              | 1983747          | 時間項目圖表顯示額外的資料                                                                                                                   |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| 功能區域                        | 參考編號 | 品質更新                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 專案管理與會計 | [441680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441680)           | 已封鎖項目需求退回的調整                                                                                                                                                                                                        |
| 專案管理與會計 | [446498](https://fix.lcs.dynamics.com/Issue/Details/?bugId=446498)           | 表單附註未出現在格式化專案發票上                                                                                                                                                                                                          |
| 專案管理與會計 | [453407](https://fix.lcs.dynamics.com/Issue/Details/?bugId=453407)           | 專案發票的 MEXICO CFDI 33 不允許從發票提案更新付款方法                                                                                                                                                           |
| 專案管理與會計 | [458149](https://fix.lcs.dynamics.com/Issue/Details/?bugId=458149)           | 在 **整合** 帳目中未考慮自動將會計日期設定為未結期間的參數                                                                                                                                                             |
| 專案管理與會計 | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | 在 **專案清單** 頁面上看不到預測功能表項目                                                                                                                                                                                                      |
| 專案管理與會計 | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | 無法開啟 **專案陳述** > **交易和預測**                                                                                                                                                                                                      |
| 專案管理與會計 | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | 移除和讀取資源指派會將 Finance 中的專案預測項目加倍                                                                                                                                                                   |
| 專案管理與會計 | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468)           | 若專案上未擁有合約服務內容，就無法 Dataverse 中建立專案估計值                                                                                                                                                                 |
| 專案管理與會計 | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | 當公司貨幣與交易貨幣不同時，由於傳票不平衡錯誤導致消除失敗                                                                                                                                            |
| 專案管理與會計 | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382)           | 固定價格專案的已過帳專案交易中的發票狀態篩選無法運作                                                                                                                                                            |
| 專案管理與會計 | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | 無法更新 Dataverse 中工作的開始日期                                                                                                                                                                                                                    |
| 專案管理與會計 | [507172](https://fix.lcs.dynamics.com/Issue/Details/?bugId=507172)           | 能夠在 Project Operations 整合案例中刪除發票提案明細                                                                                                                                                                                    |
| 專案管理與會計 | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989)           | 能夠在 Project Operations 整合案例中刪除發票提案明細                                                                                                                                                                                    |
| 專案管理與會計 | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | 避免在沒有 Dataverse 整合的情況下啟用多個合約服務內容                                                                                                                                                                                        |
| 專案管理與會計 | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527)           | 賒帳開立發票 = 損益時，估計畫面已開立發票營收為零 (0)                                                                                                                                                                          |
| 專案管理與會計 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364)           | WIP - 公司間專案開立發票中的銷售值過帳選擇了意外帳戶                                                                                                                                                                           |
| 專案管理與會計 | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799)           | 無法在已啟用 Project Operations 的情況中執行估計值/收入認列                                                                                                                                                                         |
| 差旅和費用                | [378738](https://fix.lcs.dynamics.com/Issue/Details/?bugId=378738)           | 代理人輸入的費用傳回給費用使用者，而不是代理人                                                                                                                                                                                           |
| 差旅和費用                | [409489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=409489)           | 提交工作流程的費用報表工作流程委派使用者未識別為工作流程建立者                                                                                                                                                             |
| 差旅和費用                | [464658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=464658)           | 法律實體中的預設維度不能處理公司間費用報表                                                                                                                                                                    |
| 差旅和費用                | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892)           | 每日津貼費用類別的最後一天進餐量計算的問題                                                                                                                                                                                    |
| 差旅和費用                | [473646](https://fix.lcs.dynamics.com/Issue/Details/?bugId=473646)           | 從連結至差旅申請的視費用報表中刪除費用明細項目後，**差旅申請** 頁面的 **調整金額** 欄位未更新                                                                                                       |
| 差旅和費用                | [474396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=474396)           | 在提交至工作流程後，費用報表才驗證原則                                                                                                                                                                                           |
| 差旅和費用                | [475777](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475777)            | 項目委派的差旅費用收據無法正確顯示                                                                                                                                                                                            |
| 差旅和費用                | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714)            | 當使用者語言設定為 es-MX 時，每個員工的費用類型不會顯示逐項費用                                                                                                                         |
| 差旅和費用                | [477831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477831)            | 費用報表允許輸入費用類別的錯誤子類別                                                                                                                                                                                       |
| 差旅和費用                | [478630](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478630)            | 當費用報表金額超過預付現金金額時，預付現金與費用報表協調不會如預期的方式運作                                                                                                           |
| 差旅和費用                | [486680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486680)            | 與 ProjProjectLookup 相關查詢的效能問題。 因為查詢花費很長的執行時間，所以客戶被封鎖。                                                                                                                     |
| 差旅和費用                | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531)            | **允許根據抵銷付款帳戶對交易進行分組** 和 **過帳時更正會計日期** 開啟時過帳的費用報表，顯示會計日期未在 **會計分配** 表格中分組，這會影響銷售稅記錄 |
| 差旅和費用                | [491759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491759)            | 如果在費用報表行上使用了 **沖銷加值稅**，則匯入含外幣的信用卡交易記錄時，會建立不正確的供應商交易                                                                                                                     |
| 差旅和費用                | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175)            | 如果專案識別碼是新增於標題等級，則無法建立公司間費用報表                                                                                                                                                                 |
| 差旅和費用                | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491)            | 當費用金額大於預付金額時的費用付款問題                                                                                                                                                                          |
| 差旅和費用                | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556)            | 如果將使用者角色指派給特定組織，則公司間費用報表下的專案識別碼資訊會是空的                                                                                                                                           |
| 差旅和費用                | [513845](https://fix.lcs.dynamics.com/Issue/Details/?bugId=513845)            | 已完成費用報表自動過帳工作流程，但是發票未過帳                                                                                                                                                                                          |

### <a name="regulatory-updates"></a>法規更新
如需 Finance and Operations 應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。 您也可以使用問題搜尋工具登入 LCS 並查看計畫的法規更新。 問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。


[!INCLUDE[footer-include](../includes/footer-banner.md)]