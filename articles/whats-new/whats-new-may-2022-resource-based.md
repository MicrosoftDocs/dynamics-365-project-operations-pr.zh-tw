---
title: 2022 年 5 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本文提供有關資源/非庫存型案例適用 Microsoft Dynamics 365 Project Operations 2022 年 5 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921384"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 5 月新增功能 - 資源/非庫存型案例適用的 Project Operations

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.42.0.70 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.26 版中的專案管理與會計

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

此版本中沒有 Project Operations 雙重寫入對應的更新。 如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](../environment/resource-dual-write-maps.md)。

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新
### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 資源管理 | 2634019 | 改善一般團隊成員新增為資源時的商務驗證錯誤訊息。 |
| 專案規劃和追蹤 | 2648515 | 限制排程實體中 **ownerid**、**state** 和 **status** 的更新。 |
| 帳單和定價 | 2653167 | **估計值** 網格小數點分隔符號必須遵循 **個人選項** 中的格式設定。 |
| 帳單和定價| 2662251 | 在材料估計中建立記錄時，會在 **更正的單位** 和 **單位群組** 欄位中使用預設值。 |
| 帳單和定價| 2571408 | 建立草稿發票時，未開單銷售實際值會有預估發票識別碼的戳記。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

如需有關此更新中所包含 Bug 修正的詳細資訊，請登入 Microsoft Dynamics Lifecycle Services (LCS)，並檢視[知識庫文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864)。
