---
title: 2021 年 9 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本文提供有關資源/非庫存型案例適用 Project Operations 2021 年 9 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923362"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 9 月新增功能 - 資源/非庫存型案例適用的 Project Operations

*適用於：資源/非庫存型案例適用的 Project Operations*

這篇文章適用於下列 Dynamics 365 Project Operations 元件和版本：

   - Microsoft Dataverse 環境版本 4.14.0.99 中的 Project Operations。
   - Dynamics 365 Finance 環境 10.0.20 版中的專案管理與會計。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

此版本中沒有 Project Operations 雙重寫入對應的更新。 如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](../environment/resource-dual-write-maps.md)。

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果未啟用最新版本的對應，特定功能可能無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中查看對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的資料表對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 時間和費用 | 1811407 | 調整核准費用項目所需的專案核准者資訊安全角色。 |
| 時間和費用 | 1811438 | 調整取消時間項目核准所需的專案核准者資訊安全角色。 |
| 時間和費用 | 2370126 | 更新 **時間項目** 實體中的 **專案工作** 及 **角色** 圖示。 |
| 時間和費用 | 2379879 | 更正使用行動電話用 Dynamics 365 時的時間項目中的 **複製週次** 功能。 |
| 帳單和定價 | 2371906 | 預估發票總計金額在資源型部署適用的 Project Operations 中不能是可調整的。 |
| 帳單和定價 | 2385802 | 修正重新整理專案總計時出現負數實際時數的錯誤。 |
| 帳單和定價 | 2389675 | 改善預估發票確認行為。 長時間執行的工作實體必須考量寫入會計確認結果所需的活動。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 差旅和費用 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 從根據信用卡交易所建立之費用過帳的廠商及銷售稅交易金額不正確。 |
| 差旅和費用 | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | 產生付款帳目時，會建立錯誤的結算明細。 |
| 差旅和費用 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 從根據信用卡交易所建立之費用過帳的銷售稅交易金額不正確。 |
| 差旅和費用 | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | 刪除費用明細可能需要花費很長時間。 |
| 專案會計 | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | 套用 KB 4619395 之後，不支援將編號序列變更為 **連續**，並且會在過帳估計值時，發生下列錯誤：「系統不支援設定「連續」的編號序列 Proj_X。」 |
| 專案會計 | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | 廠商發票過帳可能會失敗，並顯示下列錯誤訊息：「憑單上的交易未依據 2021/5/17 事項達到借貸平衡。 (會計貨幣：0.00 - 報表貨幣：0.01)。」 |
