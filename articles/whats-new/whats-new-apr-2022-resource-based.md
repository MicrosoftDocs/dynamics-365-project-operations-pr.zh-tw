---
title: 2022 年 4 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本文提供有關資源/非庫存型案例適用 Microsoft Dynamics 365 Project Operations 2022 年 4 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ea1c96d64309990962f431b1c72ae47bf445bfa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912368"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 4 月新增功能 - 資源/非庫存型案例適用的 Project Operations

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.41.0.45 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.26 版中的專案管理與會計

## <a name="features-included-in-this-release"></a>此版本包含的功能

採購類別可用於專案採購訂單和待處理廠商發票中。 如需詳細資訊，請參閱[將採購類別與專案採購單及待處理廠商發票搭配使用](configure-procurement-categories.md)。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

下表顯示 Project Operations 的 2022 年 3 月發行版本中已修改或新增的雙重寫入對應。

| 實體對應 | 更新的版本 | 意見 |
| -------------- | ------------------- | ------------|
| Project Operations 整合專案廠商發票明細匯出實體 msdyn\_projectvendorinvoicelines | 1.0.0.4 | 此對應支援將採購類別與採購單及待處理廠商發票搭配使用。 |

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| ------------ | ---------------- | -------------- |
| 時間和費用 | 2573900 | 根據預設，必須啟用 **新式核准** 功能。 |
| 帳單和定價 | 2603313 | 修正造成您無法新增含有產品之報價和合約服務內容的重複記錄錯誤。 |
| 部署和設定 | 2611368 | 客戶必須使用現代化應用程式設計師，才能將多達五個的自訂實體新增至解決方案。 |
| 時間和費用 | 2628285 | 修正會在進行時間項目匯入時影響設定正確資源類別能力的問題。 |
|   商機管理| 2628815 | 更新報價明細詳細資料描述的字元限制以符合工作主題的字元限制，好讓主題長度超過 100 個字元的工作匯入成功。 |
| 時間和費用| 2629547 | 專案核准的 **提交者** 欄位必須指向提交記錄的使用者。 |
| 時間和費用| 2629865 | 工作在複製專案時的 **複製類別** 欄位。 |
| 時間和費用| 2636463 | 修正新式核准表單中對核准的篩選條件。 |
| 專案規劃和追蹤 | 2648300 | 修正造成無法變更專案負責人的問題。 |
| 帳單和定價 | 2563000 | 未開單銷售 (其中不能有與合約貨幣不同的貨幣) 的帳目明細。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

如需有關此更新中所包含 Bug 修正的詳細資訊，請登入 Microsoft Dynamics Lifecycle Services (LCS)，並檢視[知識庫文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864)。
