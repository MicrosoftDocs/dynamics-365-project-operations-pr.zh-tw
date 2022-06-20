---
title: 2022 年 3 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 本文提供有關資源/非庫存型案例適用 Project Operations 2022 年 3 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910896"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 3 月 - 資源/非庫存型案例適用的 Project Operations 新增功能

*適用於：資源/非庫存型案例適用的 Project Operations*

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.30.0.99 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.25 版中的專案管理與會計

## <a name="features-included-in-this-release"></a>此版本包含的功能

全新重新設計的現代化費用工作區現已支援每日津貼。 使用每日津貼的公司可以啟用此功能，讓使用者以輕鬆的方式提交並報銷其出差津貼費用。 如需詳細資訊，請參閱[每日津貼費用](../expense/per-diem-expenses.md)。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

下列清單顯示 Project Operations 2022 年 3 月發行版本中已修改或新增的雙重寫入對應。

| **實體對應** | **更新的版本** | **註解** |
| --- | --- | --- |
| Project Operations 整合專案廠商發票明細匯出實體 msdyn\_projectvendorinvoicelines | 1.0.0.3 | 對應已更新，可與 Dataverse 中的廠商發票明細實體協調一致。 <br>不要啟用對應版本 1.0.0.4。 這準備要與下一個每月更新中的 Finance 環境版本 10.0.26 搭配使用。 |

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 時間和費用 | 2388011 | 進行大量核准時，向時間項目提交者顯示拒絕註解。 |
| 專案規劃和追蹤 | 2495294 | **工作詳細資料** 頁面上的專案詳細資料必須是不可編輯。 |
| 帳單和定價 | 2499605 | 從報價里程碑建立的合約里程碑錯誤地標示為唯讀。 |
| 專案規劃和追蹤 | 2506050 | 如果沒有要儲存的變更，則作業集會保持暫止一小時。 接著會錯誤地將此項作業集標示為 **失敗**，然而必須立即將其完成。 |
| 帳單和定價 | 2507401 | 因快取不正確而在專案中錯誤地輸入預設合約單位。 |
| 帳單和定價 | 2541660 | 雙重寫入中的 **銷售訂單建立驗證** 只能用於專案型訂單。 |
| 帳單和定價 | 2552745 | 稅金未在已設定分割帳單規則的客戶之間分攤。 |
| 帳單和定價 | 2558859 | 改善進行定價維度設定時的錯誤訊息。 |
| 帳單和定價 | 2558933 | 將 **msdyn\_project** 新增為定價維度時，**從專案估計值匯入** 失敗。 |
| 帳單和定價 | 2559101 | 專案參數刪除作業未封鎖，並造成問題。 |
|   商機管理 | 2570390 | 雙重寫入外掛程式強制報價、訂單及商機上的帳戶類型做為 **客戶**，即使該帳戶類型不正確。 |
| 帳單和定價 | 2586097 | 從專案合約服務內容移除專案時，未沖回分割的已開單成本實際值。 |
| 帳單和定價 | 2589619 | 目錄外材料上的稅金會傳播至未開單銷售實際值和發票。 |
|   商機管理 | 2594015 | 對於付款條件為 **Net60** 的客戶，無法以成交關閉報價。 |
| 專案規劃和追蹤 | 2595841 | 在 Project for the Web 中，使用者會在建立新的資源要求時收到有關遺失 **msdyn\_actualstart** 的錯誤訊息。 |
| 時間和費用 | 2602511 | 時間項目的 **拒絕者** 欄位會顯示的拒絕者是 **系統**，而不是具名使用者。 |
| 時間和費用 | 2602528 | 專案核准者可以在其未列為核准者的專案上核准時間。 |
| 帳單和定價 | 2608550 | 即使原始發票沒有發生變更，也可以確認更正發票。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 專案管理與會計 | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | **類別識別碼** 欄位的允許長度在 Finance 與 Project Operations 之間有不相符的情形。 |
| 專案管理與會計 | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | 將 **分期付款發票開具** 欄位設定為 **損益開**，並使用 **完成百分比** 原則時，無法消除固定價格專案。 |
| 專案管理與會計 | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | 在 Project Operations 整合帳目之費用明細的專案設定中，輸入了不正確的預設銷售稅群組。 |
| 專案管理與會計 | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | 您無法在 Project Operations 的整合部署中編輯專案發票提案標題維度。 |
| 專案管理與會計 | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | 公司間廠商發票不可與 Dataverse 進行整合。 |
| 專案管理與會計 | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | 客戶餘額貨幣與報表貨幣不相符。 |
| 專案管理與會計 | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | 您可以過帳專案發票，即使客戶的所有發票都在保留狀態。 |
| 專案管理與會計 | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | 在有 **標題** 及 **明細** 檢視表的專案發票提案中找不到 **刪除所有明細** 按鈕。 |
| 專案管理與會計 | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | 過帳廠商發票時，發生下列錯誤：「發票的會計日期必須是在相關採購單的同一個會計年度中。 請執行採購單年終程序，或是將日期變更至目前會計年度。」 |
| 差旅和費用 | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | 發佈差旅申請的已認可成本之後，未發佈專案的已認可成本。 |
| 差旅和費用 | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | 提交費用報表時，發生下列錯誤：「堆疊追蹤：公司不存在。」 |
| 差旅和費用 | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | 在專案上選取 **需要帳目活動** 參數時，未在費用報表中輸入預設 **專案識別碼**。 |
| 差旅和費用 | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | **過帳費用** 按鈕無法在資源/非庫存案例適用的 Project Operations 中正常運作。 |
| 差旅和費用 | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | 包含乘客的里程費用報表的 **每英里費率** 發生問題。 |
| 差旅和費用 | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | 在 **里程費率層級** 費用類別中使用兩種不同的車輛類型時，員工的費用里程費率合計不正確。 |
| 差旅和費用 | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | 對差旅申請明細中 **專案** 欄位的查詢未傳回正確的專案清單。 |
| 差旅和費用 | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **里程審查中** 會在費用報表上顯示警告。 |
| 差旅和費用 | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | 收據光學字元辨識 (OCR) 服務無法正常運作，因為費用 OCR 服務的 URL 有問題。 |
| 差旅和費用 | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | 如果啟用 **可以快速分項列舉定期費用** 功能，每次開啟 **分項列舉** 頁面時，費用報表中分項列舉明細的金額都會變更金額。 |
| 差旅和費用 | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | 當臨時名單有多個核准者時，您無法刪除費用報表。 |

## <a name="removed-and-deprecated-features"></a>已移除和已取代的功能

[Project Operations 中已移除或已取代的功能](removed-depreciated-features-project.md)文章題說明 Dynamics 365 Project Operations 已移除或已取代的功能。

- 已移除的功能在產品中不復存在。
- 取代的功能不在主動開發之列，可能會在未來的更新中遭移除。

將任何功能從產品移除之前 12 個月，取代公告會出現在 [Project Operations 中已移除或已取代的功能](removed-depreciated-features-project.md)文章中。

對於僅影響編譯時間但與沙箱和生產環境二進位相容,的中斷性變更來說，取代時間將少於12個月。 這些變更通常是必須對編譯器進行的功能更新。
