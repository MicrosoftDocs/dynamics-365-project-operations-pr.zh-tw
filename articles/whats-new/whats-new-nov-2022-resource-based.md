---
title: 2022 年 11 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 本文提供有關 Microsoft Dynamics 365 Project Operations 2022 年 11 月發行版本中資源/非庫存型案例的品質更新資訊。
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831073"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 11 月 - 資源/非庫存型案例適用的 Project Operations 新增功能

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.58.0.119 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.30 版中的專案管理與會計

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

此版本中沒有 Project Operations 雙重寫入對應的更新。 如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](../environment/resource-dual-write-maps.md)。

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 帳單和定價 | 2781818 | 設定材料使用記錄的預設價格時發生的找不到索引鍵錯誤。 |
| 帳單和定價 | 2922373 | 無法將報價明細連結至已關閉為未成交報價的專案。 |
| 帳單和定價 | 2943206 | [專案實體必須可選用] 中的 **合約明細** 欄位。 |
| 帳單和定價 | 2953182 | 改善更正發票的錯誤訊息。|
| 帳單和定價 | 2959500 | 無法將報價明細連結至已與未成交報價相關聯的專案工作。|
| 帳單和定價 | 2959560 | 在特定地區設定中以成交關閉報價時收到的「此客戶已經在專案合約中」訊息。 |
| 帳單和定價 | 3031727 | 資源指派因必要欄位「msdyn_Company」遺失錯誤而失敗。 |
| 帳單和定價 | 3036905 | 擁有公司永遠不會對 ProjectTeamMember 進行初始化。 |
| 商機管理 | 2763519 | EnsureProjectContractAllowsUpdates 中的 Null 參考錯誤。 |
| 商機管理 | 2783798 | 匯入報價明細的專案估計值時，費用和材料估計值缺少工作描述。|
| 商機管理 | 2988635 | 改善刪除報價中客戶時的錯誤訊息描述。 |
| 商機管理 | 3001191 | 無法從帳務方式指定為 Null 的商機建立報價。 |
| 升級 | 3012324 | 專案轉換在專案中因其名稱中有 Tab 等控制字元而失敗。 || 專案規劃和追蹤 | 2790384 | 擱置中 OperationSet 逾時太短。 |
| 專案規劃和追蹤 | 3044275 | 缺少下列訊息的當地語系化：missingProjectSchedulerErrorMessage。 |
| 專案規劃和追蹤 | 3044277 | 排程取消設定時，專案協調網格未載入。|
| 資源管理 | 2943153 | 要為期間顯示兩位小數位數的 [更新追蹤] 索引標籤。|
| 轉承包 | 2932774 | 「廠商發票明細唯讀」不正確地擲回錯誤。 |
| 轉承包 | 2939556 | 如果廠商發票標題狀態未處於使用中狀態，則刪除明細時不應將該狀態設定為為 [草稿]。 |
| 時間和費用 | 2939998 | 了解 ProjOps 中的新 TESA 版本。 |


### <a name="project-management-and-accounting-in-finance"></a>Finance 中的專案管理與會計

如需此更新中有關 Bug 修正的詳細資訊，請登入 Microsoft Dynamics Lifecycle Services，查看[知識庫文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468)。
