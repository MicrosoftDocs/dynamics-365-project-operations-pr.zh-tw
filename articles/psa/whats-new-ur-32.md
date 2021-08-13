---
title: Project Service Automation V3 更新版本 32 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 32 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994851"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Project Service Automation V3 更新版本 32 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 32 新推出或已變更的功能及修正。 此版本的組建編號是 V3.10.53.108，已於 2021 年 6 月透過自我更新正式推出。

## <a name="update-release-32"></a>更新版本 32

### <a name="bug-fixes"></a>Bug 修正

#### <a name="general"></a>一般

- 主要升級失敗時，只能封鎖主要應用程式進入點，以確保共用的實體仍然可供存取。

#### <a name="time-and-expense"></a>時間和費用

下列問題已獲修正：

- **TimeEntriesImportFromResourceAssignment** 不會保留資源指派分佈配量的開始時間和結束時間。
- 當您選取 **時間項目** 窗格中的 **開啟項目** 時，可能會禁止您選取其他表單。
- 將指派匯入至時間項目時，用戶端程式碼查詢可能會產生造成查詢失敗的冗長 URL。
- 在 **時間項目** 網格中，從儲存格刪除某個值之後，焦點不會留在網格中。
- **拒絕** 按鈕已從新式核准的 **處理核准** 視圖中移除。
- 發生鎖死以及未能適當處理與 **時間項目** 實體相關的自訂，會影響時間項目大量核准的穩定性及效能。

#### <a name="project-planning"></a>專案規劃

- 更新其 **承包單位** 欄位有 Null 值的專案時，會產生 Null 參考例外狀況。
- **重新整理專案總計** 不正確地計算專案的剩餘成本與剩餘銷售。
- 冗長的定價計算會影響與資源指派分佈更新相關的效能。

#### <a name="resource-management"></a>資源管理

已修正下列問題：

- 可預約資源的行事曆產能大於 1 時，Project Service Automation 會錯誤地將產能辨識為 0 (零)。 因此，排程檢視表中會發生無限迴圈。

#### <a name="sales"></a>銷售

下列問題已獲修正：

- 建立具有自訂交易類型的帳目明細時，會發生下列 Null 參考例外狀況：*Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*。
- 不可將複製報價前已停用的角色和類別新增至新複製報價的應收費角色和類別。
- 文件日期和會計日期，與直接在草稿發票中建立的發票明細詳細資料所提供的開始日期不一致。
- 在與角色和類別已於複製報價前停用一事相關的案例中，會產生 Null 參考例外狀況。
- **專案** 頁面上的 **更新價格** 動作不會更新費用估計值和材料估計值。
