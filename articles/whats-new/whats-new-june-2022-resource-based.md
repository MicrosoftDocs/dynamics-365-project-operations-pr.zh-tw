---
title: 2022 年 6 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本文提供有關資源/非庫存型案例適用 Microsoft Dynamics 365 Project Operations 2022 年 6 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959397"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 6 月新增功能 - 資源/非庫存型案例適用的 Project Operations

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.43.0.77 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.27 版中的專案管理與會計

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

下表顯示 Project Operations 2022 年 6 月發行版本中已修改或新增的雙重寫入對應。

| 實體對應 | 更新的版本 | 意見 |
| --- | --- | --- |
| Project Operations 整合專案廠商發票匯出實體 (msdyn_projectvendorinvoices) | 1.0.0.1 | 取代舊版欄位，並對應至要進行廠商發票狀態追蹤的新欄位。 |

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 轉承包 | 2708885 | 修正使用者建立未填入可預約資源之可預約資源預約標題記錄時出現的錯誤訊息。 |
| 專案規劃和追蹤 | 2629441 | 更正工作流程觸發邏輯，以協助避免在更新專案工作時出現無限迴圈。 |
| 時間和費用 | 2641209 | 從指派/預約匯入的時間項目必須保留可預約資源參考。 |
| 專案規劃和追蹤 | 2651148 | 必須保護專案文件標頭。|
| 專案規劃和追蹤 | 2653145 | 新增驗證，以確保無法建立名稱中包含無效字元的專案記錄。 |
| 時間和費用 | 2654710 | 更正 **核准** 頁面上的篩選功能。 |
| 帳單和定價 | 2667805 | 新增驗證，以協助避免在沒有支援的未開單銷售實際值時建立已開單銷售實際值。 |
| 帳單和定價 | 2668378 | 新增驗證，以協助避免在未填入邏輯名稱和欄位名稱時新增自訂定價維度。 |
| 轉承包 | 2677485 | 更新廠商發票明細雙重寫入對應的目標版本。 |
| 時間和費用 | 2700428 | 改善核准邏輯，以確保即使其中一個核准集停滯在系統作業中，也可以處理專案的其他核准集。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance 中的專案管理與會計

如需有關此更新中所包含 Bug 修正的詳細資訊，請登入 Microsoft Dynamics Lifecycle Services (LCS)，並檢視[知識庫文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271)。
