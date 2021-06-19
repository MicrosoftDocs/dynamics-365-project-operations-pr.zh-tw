---
title: Project Service Automation V3 更新版本 22 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 22 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 5694aa27afe7618cfca6b27444393634a9686600
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006546"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation 更新版本 22 V3

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 22 新推出或已變更的功能及修正。 此版本的組建編號為 V 3.10.33.48，已於 2020 年 6 月透過自我更新正式發行。

## <a name="update-release-22"></a>更新版本 22

### <a name="bug-fixes"></a>Bug 修正



**時間和費用**

下列問題已獲修正：

- **時間項目** 未在匯入後自動新增至時間項目排程中。
- **時間項目** 網格日期選擇器無法辨識使用者的地區設定。

**資源管理**

下列問題已獲修正：

- 在手動模式下，無法在產生 **資源需求** 時辨識 **資源指派** 分佈的變更。
- **資源要求** 不支援自訂要求狀態。

**專案管理**

下列問題已獲修正：

- 對 EstimateGridControl 使用按兩下動作時，無法正確剖析荷蘭文格式數字。
- 使用 Microsoft Project 桌面用戶端增益集變更指派時，已指派的時數無法正確更新。
- 當合約貨幣與客戶貨幣不同，且組織是設定為顯示貨幣代碼而不是貨幣符號時，[專案追蹤] 和 [估計值] 網格顯示不正確的銷售貨幣代碼。
- 如果工作時數排程為每天 24 小時，則團隊成員的完成日期將會新增一天。
- 在專案排程中，將交易類別新增至工作時，不會觸發自動儲存。
- 將團隊成員新增至專案範本時，顯示下列錯誤：「資源需求無法與專案範本建立關聯」。 
- 功能區規則指令碼「msdyn.Approval.CanApproveOrReject」顯示逾時錯誤。

**Sales**

下列問題已獲修正：

- 在 [新增報價專案價目表] 表單/實體的 [價目表] 查詢中選取 [成本價目表] 時，未顯示驗證錯誤訊息。
- 如果附加至報價的 BPF 處於最終階段，以成交關閉報價時，不會瀏覽時至建立的合約。
- 回收時間項目時，沖回 **未開單銷售** 會連結至原始成本。
- 選取 **確認** 按鈕之後，除非重新整理發票，否則發票狀態不會變更為 **已確認**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]