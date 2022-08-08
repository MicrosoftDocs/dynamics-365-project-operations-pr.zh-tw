---
title: 2021 年 4 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本文提供有關資源/非庫存型案例適用 Project Operations 2021 年 4 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 490b7aa38bfdfbcdce21a21e582296e4ce15aeeb
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029244"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 4 月新增功能 - 資源/非庫存型案例適用的 Project Operations

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

這篇文章適用於下列 Dynamics 365 Project Operations 元件和版本：

- Dataverse 環境的 Project Operations 版本 4.9.0.221
- Dynamics 365 Finance 環境 10.0.17 版中的專案管理與會計

## <a name="features-included-in-this-release"></a>此版本包含的功能

此版本包含下列功能：

- 專案的非庫存材料。 主要功能包括：
  - 對專案銷售週期期間的非庫存材料進行估計和定價。 如需詳細資訊，請參閱[設定產品類別目錄產品的成本及銷售費率 - 精簡](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md)。
  - 追蹤專案交付期間的非庫存材料使用。 如需詳細資訊，請參閱[記錄專案和專案工作的材料使用方式](../material/material-usage-log.md)。
  - 開立已使用非庫存材料成本的發票。 如需詳細資訊，請參閱[管理帳務積存](../proforma-invoicing/manage-billing-backlog.md)。
  - 如需有關如何設定此功能的詳細資訊，請參閱[設定非庫存材料和待處理廠商發票](../procurement/configure-materials-nonstocked.md)
- 工作型帳務：新增將專案工作與專案合約服務內容建立關聯的功能，藉此使他們接受與合約服務內容中所規定相同的帳務方法、發票頻率和客戶。 此關聯可確保根據專案工作上的這項設定準確開立發票、會計、收入估計以及工作認列。
- Dynamics 365 Dataverse 中的新 API 允許對 **排程實體** 執行建立、更新和刪除作業。 如需詳細資訊，請參閱 [使用排程 API 對排程實體執行作業](../project-management/schedule-api-preview.md)。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

下表顯示 Project Operations 2021 年 4 月版本中已修改或新增的雙重寫入對應。

| **實體對應** | **更新的版本** | **註解** |
| --- | --- | --- |
| Project Operations 整合實際值 (msdyn\_actuals) | 1.0.0.14 | 修改對應以同步處理材料專案實際值。 |
| 費用估計值的 Project Operations 整合實體 (msdyn\_estimateslines) | 1.0.0.2 | 新增專案合約服務內容同步至財務和營運應用程式，以提供工作型帳單支援。 |
| 時數估計值的 Project Operations 整合實體 (msdyn\_resourceassignments) | 1.0.0.5 | 新增專案合約服務內容同步至財務和營運應用程式，以提供工作型帳單支援。 |
| Project Operations 材料估計值整合資料表 (msdyn\_estimatelines) | 1.0.0.0 | 新增資料表對應，以便將 Dataverse 中的材料估計值同步處理至財務和營運應用程式。 |
| Project Operations 整合專案廠商發票匯出實體 (msdyn\_projectvendorinvoices) | 1.0.0.0 | 新增資料表對應，以便將財務和營運應用程式中的廠商發票標題同步處理至 Dataverse。 |
| Project Operations 整合專案廠商發票明細匯出實體 (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | 新增資料表對應，以便將財務和營運應用程式中的廠商發票明細同步處理至 Dataverse。 |

更新 Project Operations Dataverse 解決方案以及財務和營運解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的資料表對應。 如果未啟用最新版本的對應，特定功能可能無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中查看對應的使用中版本。 您可以選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本來啟用新的對應版本。 如果您已對現成可用的資料表對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果啟動對應時發生問題，請依照[對應上發生的遺失資料表欄問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)雙重寫入疑難排解指南一節中的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-in-dynamics-365-dataverse"></a>Dynamics 365 Dataverse 中的 Project Operations

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 帳單和定價 | 2124532 | 當原始發票上有保留款金額或已套用的保留款金額時，預估發票上會顯示 **更正發票** 按鈕。 只有在環境有 Finance 10.0.19 版或更新版本時，才會顯示此按鈕。 |
| 帳單和定價 | 2224568 | 新增邏輯，以啟用涉及叫用發票確認外掛程式的自訂。 |
| 帳單和定價 | 2101098 | 改善預估發票預設欄位的邏輯：**帳單地址**、**帳單姓名** 和 **付款條件** 現在會根據對應的專案合約客戶記錄設定預設值。 |
| 帳單和定價 | 2021413 | 更新 **工作** 實體的 **實際成本** 與 **銷售** 欄位，以包含工作上未開單及已開單費用中的銷售值。 |
| 帳單和定價 | 2182110 | 複製專案合約時，目的地專案合約中會重新產生合約服務內容，以確保其唯一性。 |
| 商機管理 | 2186741 | 新增驗證，以確保無法更新現有報價明細詳細資料上的 **來源** 欄位和 **交易類型**。 |
| 商機管理 | 2191353 | 不可在時間和材料合約服務內容上建立里程碑。 |
| 商機管理 | 2216956 | 修正 **更新價格** 的問題。 |
| 規劃和追蹤 | 2182979 | 專案複製功能已改善，可確保費用估計明細是從原始專案複製而來。 |
| 規劃和追蹤 | 2184144 | 專案複製功能已改善，可確保資源職位名稱是從原始專案複製而來。 |
| 規劃和追蹤 | 2184799 | 專案複製：加強控制，以確保正在進行複製時無法變更估計開始日期。 |
| 規劃和追蹤 | 2185134 | 專案複製：目的地專案估計開始日期已設定為今天的日期。 |
| 規劃和追蹤 | 2196373 | 專案複製：確保專案經理和團隊成員記錄在專案團隊中不會重複。 |
| 規劃和追蹤 | 2211833 | 專案複製：資源指派會從源專案工作複製到目的地專案。 |
| 規劃和追蹤 | 2186541 | 修正 **估計值** 網格依資源分組時發生的問題。 |
| 規劃和追蹤 | 2166906 | 工作中的交易類別必須是複製到 **資源指派** 實體。 |
| 資源管理 | 2125362 | 修正使用根據工作時數配置方法建立一般團隊成員的問題。 |
| 時間和費用 | 2113603 | 修正從 **時間項目** 頁面中移除屬性的自訂相關問題。 系統現在會先檢查頁面上是否有該屬性，再使用指令碼來存取屬性。 |
| 時間和費用 | 2204377 | 在輸入時間期間選取 **複製週次** 時，必須自動顯示已複製的工時表。 |
| 時間和費用 | 2209059 | Dynamics 365 Field Service 時間項目的 **狀態** 欄位可以進行編輯。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 專案管理與會計 | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | 沖回估計值抵銷無法在 **週期** 區段中發生作用。  |
| 專案管理與會計 | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | **會計調整** 功能在已選取 **不允許手動輸入** 的總帳科目上產生問題。 |
| 專案管理與會計 | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | 新增商務規則以處理包含保留款金額或已套用保留款金額的更正發票。 |
| 專案管理與會計 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | 公司間專案發票請款中的 WIP 銷售值過帳選擇了非預期的科目。 |
| 專案管理與會計 | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | 在 Project Operations 中使用保留款時，如果在開立預付款發票後變更預設專案，就會在接踵而來的扣款上發生問題。 |
| 專案管理與會計 | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | 在 Project Operations 中，從合約移除專案時，如有需要，應重設合約的預設專案。 |
| 專案管理與會計 | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | 在 Project Operations 中，公司間發票的 **新增明細** 清單中顯示錯誤的費用明細。 |
| 專案管理與會計 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | 在 Project Operations 中，**採購合約** 頁面無法顯示在與 Project Operations 整合的 Finance 法律實體中。 |
| 專案管理與會計 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | 因為 Dataverse 整合錯誤，您無法在 Project Operations 中將報價轉換為已成交。 |
| 專案管理與會計 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 可以設定不同客戶的資金來源發票地址。  |
| 專案管理與會計 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | 在 Project Operations 中，當您建立交易的過帳發票時，未選取任何維度。 |
| 差旅和費用 | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | 如果費用報表獲核准且已按明細逐一過帳，則不會更新其預付現金餘額。 |
| 差旅和費用 | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | 無法正確計算分項列記公司間費用報表的稅金。 |
| 差旅和費用 | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | 與專案相關的其他欄位會顯示在重新建構的 **公司間費用報表** 頁面上。 |
| 差旅和費用 | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | 費用報表的頁首收據上出現不正確的錯誤訊息。 |
| 差旅和費用 | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | 如果銷售稅已過帳至目的地法律實體，則費用報表會在公司間案例中不正確地進行過帳。 |
| 差旅和費用 | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | 報表送出日期未列印在核准的費用報表上。 |
| 差旅和費用 | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | 費用獲核准後，未填入 **核准日期** 和 **拒絕日期** 欄位。 |
| 差旅和費用 | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | 為一個工作人員建立的差旅申請可以用於另一個工作人員的費用報表。 |
| 差旅和費用 | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | 新增新的費用明細時，費用類別遭鎖定。 |
| 差旅和費用 | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | 分項列記已分割費用報表明細會造成應付帳款\總帳憑單過帳不完全，並且中斷會計原始憑證總管，因為 **TRVEXPTRANS.SOURCEDOCUMENTLINE** 已重複。 |
| 差旅和費用 | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | 差旅申請原則未依預期正常運作。 |
| 差旅和費用 | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | 廠商帳戶名稱未顯示在費用報表的已過帳專案交易上。 |
| 差旅和費用 | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | 在 Project Operations 中，您無法核准包含公司間專案工作的時間。 |
| 差旅和費用 | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | 預付現金退回類別未在過帳時更新預付現金餘額。 |
| 差旅和費用 | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | 銷售價在使用匯入信用卡交易所建立且與專案相關聯的外幣計價費用報表上計算錯誤。 |
| 差旅和費用 | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | 復原 **TrvRequisitionLine** 資料實體以及相關聯的唯一索引。 |
| 差旅和費用 | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | 新增檢測至 **SOURCEDOCUMENTLINE** 生成集。 |
| 差旅和費用 | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 如果銷售稅已過帳至目的地法律實體，則會在公司間案例中顯示錯誤的子分類帳日記帳。 |
| 差旅和費用 | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | 在 Project Operations 中，從 Dataverse 移除費用估計值時，並不會將其從 Finance 中刪除。 |
| 差旅和費用 | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 當費用類別屬於非專案類別時，在 **費用** 頁面上選取的財務維度未複製到費用報表。 |
