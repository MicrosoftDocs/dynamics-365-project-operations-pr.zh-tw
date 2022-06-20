---
title: 2021 年 11 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 本文提供有關資源/非庫存型案例適用 Project Operations 2021 年 11 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932884"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 11 月 - 資源/非庫存型案例適用的 Project Operations 新增功能

*適用於：資源/非庫存型案例適用的 Project Operations*

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.26.0.145、4.26.0.148、4.26.0.150、4.26.0.155 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.22 版中的專案管理與會計

## <a name="features-included-in-this-release"></a>此版本包含的功能

此版本包含下列功能：

- 專案排程應用程式開發介面 (API) 現在支援建立和刪除專案貯體的功能。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

此版本中沒有 Project Operations 雙重寫入對應的更新。 如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](/dynamics365/project-operations/environment/resource-dual-write-maps)。

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-in-dataverse"></a>Dataverse 中的Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 帳單和定價 | 2240080 | **付款條件** 欄位不得預估發票上重複。 |
| 帳單和定價 | 2358236 | 發票更正必須允許進行價格為零之明細的修正。 |
| 資源管理 | 2410072 | 允許設定以專案經理身分指派至工作的資源。 |
| 帳單和定價 | 2430234 | 修正成本績效計算問題。 |
| 時間和費用 | 2436978 | 允許以 hh:mm 格式輸入時間。 |
| 帳單和定價 | 2448623 | 允許價目表在與組織單位建立關聯之後進行更新。 |
| 時間和費用 | 2460396 | 允許透過清除儲存格的方式刪除時間項目。 |
| 帳單和定價 | 2467386 | 即使在工作已與已成交報價產生關聯時，仍允許有工作要刪除的專案。 |
| 時間和費用 | 2461744 | **我失敗的核准** 檢視表僅包含狀態為 **已提交** 的專案核准。 |
| 時間和費用 | 2464082 | 當目標狀態符合時，移除從專案核准到核准集的連結。 |
| 時間和費用 | 2468108 | 排程工作不可為核准集設定 **處理中** 狀態。 |
| 時間和費用 | 2471503 | 刪除存留超過七天的核准集。 |
| 帳單和定價 | 2480687 | 建立報價明細里程碑時，不能移除報價明細參考。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance 中的專案管理與會計

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 專案管理與會計 | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | 專案費用交易中的保留廠商金額未顯示在交易清單中。 |
| 專案管理與會計 | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | 開啟廠商發票整合時，會中斷公司間廠商發票。 |
| 專案管理與會計 | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | 專案發票的付款條件無法依預期發揮作用。 |
| 專案管理與會計 | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | 釋放廠商付款留成時，憑單過帳會有不正確的額外明細。 |
| 專案管理與會計 | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operations 整合帳目過帳時，會因為未過帳到的科目缺少維度而失敗。 |
| 專案管理與會計 | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | 將採購類別指派至項目時，無法編輯待處理廠商發票上的 **專案** 索引標籤。 |
| 專案管理與會計 | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | 如果您沒有登入 Project Operations Dataverse，就會找不到導覽窗格。 |
| 專案管理與會計 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 在套用保留款的案例中，將專案發票的收入過帳時，會因為憑單上的交易未達借貸平衡而發生問題。 |
| 專案管理與會計 | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | 在過帳發票提案後建立估計，會封鎖更正明細，使其無法匯入。 |
| 專案管理與會計 | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | 應該會無法修改已完整開立發票的里程碑記錄。 |
| 差旅和費用 | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | 在費用行動應用程式中搜尋類別時，所有的費用報表都會顯示。 |
| 差旅和費用 | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | 從根據信用卡交易所建立之費用進行過帳的廠商交易及銷售稅交易金額不正確。 |
| 差旅和費用 | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | 重新整理 **費用報表** 頁面時，出現不相關的警告。 |
| 差旅和費用 | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | 刪除臨時核准者後，再透過工作流程重新提交費用報表時，會使用錯誤的臨時核准者。 |
| 差旅和費用 | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | 發生與里程碑設定相關的過帳錯誤。 |
