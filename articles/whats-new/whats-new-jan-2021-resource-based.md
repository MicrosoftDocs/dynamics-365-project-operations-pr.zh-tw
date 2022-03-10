---
title: 2021 年 1 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 本主題提供有關資源/非庫存型案例適用的 Project Operations 2021 年 1 月版本所提供的品質更新資訊。
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9d54d5fed6e8ec1535ad798073ac8a1eec36e87d1dbba4cc4acd94d8bbdc5157
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008081"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 1 月 - 資源/非庫存型案例適用的 Project Operations 新增功能

_**適用於：** 資源/非庫存型案例適用的 Project Operations_


此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

  - Dataverse 環境的 Project Operations 版本 4.6.0.154
  - Dynamics 365 Finance 環境 10.0.16 版本的專案管理與會計

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| **部署和設定** | 2106818 | 修正造成與自訂頁面相關問題的 Web 資源重新命名。 |
| **帳單和定價** | 2091908 | 修正 Project Operations 與 Dynamics 365 Field Service 一起安裝時，**鎖定價格** 及 **使用目前定價** 選項在 **發票** 頁面上的顯示性。 |
| **帳單和定價** | 2103058 | 重新整理 **專案總計** 以處理工作上實際成本的 Null 值。 |
| **帳單和定價** | 2116100 | 改善與 **更正實際值上的項目** 功能搭配使用的錯誤訊息。 |
| **帳單和定價** | 2116129 | 改善 **專案** 頁面上費用估計值在 **估計值** 索引標籤中的顯示性。 |
| **帳單和定價** | 2119112 | 修正實際銷售和實際成本在使用不同匯率時的彙整。 |
| **帳單和定價** | 2134705 | 修正開啟 **發票** 頁面和 安裝 Field Service 時出現的錯誤無法讀取未定義的屬性 **getResourceString**。 |
| **商機管理** | 2022195 | **專案** 頁面上的工作型帳單包含表示有合約或報價明細連結至該工作的圖示。 |
| **商機管理** | 2029135 | 修正使用者嘗試在開立了預付款金額發票的已確認發票上開啟發票明細時發生的商務程序錯誤。 |
| **商機管理** | 2040713 | 修正從合約建立發票和安裝 Field Service 時發生的指令碼錯誤。 |
| **專案規劃和追蹤** | 2090202 | 將不再使用的商務規則標示為 **取代**。 |
| **時間和費用** | 2091249 | 加強控制，使使用者無法變更已送出或已核准時間項目上的工作。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| **專案管理與會計** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | 合約金額有多個資金來源的固定價格專案的 **賒帳** 頁面上不正確。 |
| **專案管理與會計** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | **Invoiceproposal.PSAnfRefProjId** 預留位置未顯示工作流程的專案識別碼，請 **檢閱專案發票提案**。 |
| **專案管理與會計** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | 過帳專案發票提案時，使用了錯誤的現金折扣日期。 |
| **專案管理與會計** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | 在 Project Operations 中移除和讀取資源指派會將 Finance 中的專案預測項目加倍。 |
| **專案管理與會計** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | 在 Project Operations 中，您無法在專案沒有合約服務內容的情況下，建立 Dataverse 中的專案估計值。 |
| **專案管理與會計** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | 將成本過帳至資產負債表時，專案費用交易上的財務維度未與費用報表的相關憑單及會計分配進行同步處理。 |
| **專案管理與會計** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | 固定價格專案已過帳專案交易的 **發票狀態** 篩選無法運作。 |
| **專案管理與會計** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | 沖回估計值抵銷無法在 **週期** 區段中發生作用。 |
| **專案管理與會計** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | 與 Dataverse 整合時，可以在 Project Operations 中刪除發票提案明細。 |
| **專案管理與會計** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | 避免在沒有 Dataverse 整合的情況下啟用多個合約服務內容。 |
| **專案管理與會計** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | 當賖帳發票請款等於損益時，[估計值] 頁面上的已開立發票收入會列為零。 |
| **專案管理與會計** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | 發票更正無法在整合環境中運作。 |
| **專案管理與會計** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | 過帳公司間專案發票請款中的 WIP 銷售值時，選擇了錯誤的科目。 |
| **專案管理與會計** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | 在 Project Operations 中，無法更新對 Dataverse 中估計工作的相依性。 |
| **專案管理與會計** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | 重複刪除 Finance 中的 Project Operations 整合帳目會導致資料遺失。 |
| **專案管理與會計** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | 過帳專案發票提案時，發生下列錯誤：「Transaction does not balance on reporting currency 將已扣減的預付金發票加入時，按照報表貨幣計算的交易未達借貸平衡」。 |
| **專案管理與會計** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | 在 Project Operations 中更新預設專案合約之後，扣除額上加入了錯誤的專案識別碼。 |
| **專案管理與會計** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | 啟用 Project Operations 時，無法完成估計值和收入認列。 |
| **專案管理與會計** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | 在 Project Operations 中，從合約移除專案，並不會重設合約上的預設專案。 |
| **專案管理與會計** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | 在 Project Operations 中，公司間發票的 **新增明細** 清單中出現錯誤的費用明細。 |
| **差旅和費用** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | 無法過帳費用明細，因為合約服務內容缺少時數設定。 |
| **差旅和費用** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | 當專案/類別驗證是強制性時，在費用報表中看不到與專案相關聯的費用類別。 |
| **差旅和費用** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | 費用報表依明細進行過帳時，未更新預付現金餘額。 |
| **差旅和費用** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | **更新付款資訊** 工作會在已使用兩個或更多付款交易進行結算的沖回結算之後失敗。 |
| **差旅和費用** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | 扣減每日津貼費用類別最後一天餐費的計算發生問題。 |
| **差旅和費用** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | 如果使用者第一次連線使用的是 es-MX 語言，則 **每個員工的費用類型** 報表不會顯示分項明列的費用。 |
| **差旅和費用** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | 費用報表發票的供應商付款使用了錯誤的彙總科目進行結算過帳。 |
| **差旅和費用** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | 當費用報表是在啟用 **允許根據抵銷付款帳戶對交易進行分組** 和 **過帳時更正會計日期** 的情況下進行過帳時，**會計分配** 表格中未將會計日期分組，這會影響銷售稅記錄。 |
| **差旅和費用** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | 清除 [在費用中使用] 核取方塊，然後再次選取時，會移除費用子類別對應。 |
| **差旅和費用** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | 如果專案識別碼是在標題層級上加入，則無法建立公司間費用報表。 |
| **差旅和費用** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | 當費用金額大於預付現金金額時，發生費用付款問題。 |
| **差旅和費用** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | 如果將使用者角色指派給特定組織，則公司間費用報表上的 **專案識別碼** 欄位會是空白。 |
| **差旅和費用** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | 加入新的費用明細時，費用類別遭鎖定。 |
| **差旅和費用** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | 分項明列已分割的費用報表明細會產生不完整的已過帳應付帳款\總帳憑單。 由於 **TRVEXPTRANS.SOURCEDOCUMENTLINE** 的資料重複，會計來源總管也會因此中斷。 |
| **差旅和費用** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | **TRVREQUISITIONLINE** 資料表上所加入的索引與客戶的資料有所重複，會在升級期間造成錯誤。 |
| **差旅和費用** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | 在 Project Operations 中，無法建立或核准 Dataverse 中包含公司間工作的時間項目。 |

## <a name="regulatory-updates"></a>法規更新

如需 Finance and Operations 應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。 您也可以使用問題搜尋工具登入 LCS 並查看計畫的法規更新。 問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。


[!INCLUDE[footer-include](../includes/footer-banner.md)]