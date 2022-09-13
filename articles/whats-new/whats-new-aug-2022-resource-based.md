---
title: 資源/非庫存型案例適用的 Project Operations 2022 年 8 月新增功能
description: 本文提供有關資源/非庫存型案例適用的 Microsoft Dynamics 365 Project Operations 2022 年 8 月發行版本中，所提供之品質更新的資訊。
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403846"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>資源/非庫存型案例適用的 Project Operations 2022 年 8 月新增功能

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.45.0.53 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.28 版中的專案管理與會計

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

此版本中沒有 Project Operations 雙重寫入對應的更新。 如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](../environment/resource-dual-write-maps.md)。

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
|   商機管理 | 2762089 | 當組織停用自動儲存時，將關閉合約視為遺失的錯誤處理。|
|專案規劃和追蹤 | 2767841 | 遙測會更新「專案實體建立」或「專案實體更新」案例。|
|帳單和定價 | 2771072 | 報價成交時的 Null 參考例外狀況處理。|
|帳單和定價 | 2844181 |取得相互關聯識別碼和封鎖發票建立作業時失敗。|
|帳單和定價 | 2852836 | 在 CE 中建立和核准的公司間費用缺少公司間實際值。|


### <a name="project-management-and-accounting-in-finance"></a>Finance 中的專案管理與會計

如需有關此更新中所包含 Bug 修正的詳細資訊，請登入 Microsoft Dynamics Lifecycle Services (LCS)，並檢視[知識庫文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438)。
