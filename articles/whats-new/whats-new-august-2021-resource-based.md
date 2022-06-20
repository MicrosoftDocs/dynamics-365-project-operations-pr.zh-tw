---
title: 2021 年 8 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本文提供有關資源/非庫存型案例適用 Project Operations 2021 年 8 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bd91f7f6b3a6f78161f8900aa06c810a58609b53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912276"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 8 月新增功能 - 資源/非庫存型案例適用的 Project Operations

*適用於：資源/非庫存型案例適用的 Project Operations*

這篇文章適用於下列 Dynamics 365 Project Operations 元件和版本：

   - Microsoft Dataverse 環境版本 4.13.0.152 中的 Project Operations。
   - Dynamics 365 Finance 環境 10.0.20 版中的專案管理與會計。

## <a name="features-included-in-this-release"></a>此版本包含的功能

此版本包含下列功能：

- **核准集**：核准集會將時間、費用或材料使用核准要求群組成較小的作業子集。 此群組功能允許由專案依特定順序處理核准，並允許重試和排序。 將要求群組在一起，可改善大量核准處理工作的可靠性和可追蹤性。 如需詳細資訊，請參閱[核准集](../approvals/approval-sets.md)。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

此版本中沒有 Project Operations 雙重寫入對應的更新。

如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](../environment/resource-dual-write-maps.md)。

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果未啟用最新版本的對應，特定功能可能無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中查看對應的使用中版本。 選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本，以啟用對應的新版本。 如果您已對現成可用的資料表對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應缺少表格欄的問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 帳單和定價 | 2295625 | 里程碑名稱必須是從發票排程複製到發票明細詳細資料。 |
| 帳單和定價 | 2316323 | 在資源型案例適用的 Project Operations 中，預估發票上的折扣應為不可編輯。 |
|   商機管理 | 2338619 | **商機** 和 **報價** 商務規則只能在頁面上進行叫用。 |
| 資源管理 | 2316523 | 從已附加角色的資源需求中使用 **傳送要求** 時，不應顯示錯誤。 |
| 資源管理 | 2326885 | 透過專案建立資源需求時，不應顯示錯誤。 |
| 時間和費用 | 2335584 | 時間項目中已取代的工作流程。 |
| 時間和費用 | 2336884 | **複製週次** 時間項目按鈕必須不只是對目前的使用者有作用。 |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 差旅和費用 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 從信用卡交易建立費用時，過帳了不正確的廠商交易及銷售稅交易金額。 |
| 差旅和費用 | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | 錯誤的結算是在建立付款帳目時所建立的明細。 |
| 差旅和費用 | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | 從信用卡交易建立費用時，過帳了不正確的銷售稅交易金額。 |
| 差旅和費用 | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | 刪除費用明細可能需要花費很長時間。 |
| 專案會計 | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | 在套用 KB 4619395 後進行估計值過帳時，系統不支援連續編號順序設定。 |
| 專案會計 | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | 廠商發票過帳可能會失敗，並出現錯誤訊息「依據 2021/5/17 帳目，憑單上的交易未達借貸平衡。 (會計貨幣: 0.00 - 報表貨幣: 0.01)」 |
