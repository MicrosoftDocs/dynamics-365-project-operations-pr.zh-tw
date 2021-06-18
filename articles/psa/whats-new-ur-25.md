---
title: Project Service Automation V3 更新版本 25 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 25 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 92dd74378457cf877e8ec26eb85a7883dda97d51
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000201"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Project Service Automation V3 更新版本 25 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出了 Project Service Automation V3 更新版本 25 的新增或變更功能和修正。此版本的組建編號為 V 3.10.43.76，一般可透過 2020 年 10 月的自我更新獲得。

## <a name="update-release-25"></a>更新版本 25

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

已修正下列問題：

- 時間項目圖表，根據擷取的間隔太長而顯示額外的資料。

**資源管理**

已修正下列問題：

- 新增了 Package Deployer 程式碼，以在更高版本的修補程式已存在時跳過 Universal Resource Scheduling 修補程式匯入。

**專案管理**

下列問題已獲修正：

- 校正了導致在專案追蹤網格中的計劃成本不正確的捨入和匯率差異。
- 支援在 **專案** 表單上顯示兩個或多個反應網格的能力。
- 提供驗證以解決在日曆結束日期之後指派工作因而導致資源指派失敗的能力。
- 改進了錯誤處理，以解決由以下各項所產生的 Null 參考例外狀況：

    - **PreValidateProjectTeamMemberCreate** 外掛程式
    - 建立沒有關聯專案的專案工作時的 **PreValidateProjectTaskCreate**
    - **PreProjectTeamMemberCreate** 外掛程式
    - **PostProjectTeamMemberDelete** 外掛程式
    - **PreValidateProjectTaskDelete** 外掛程式

**Sales**

下列問題已獲修正：

- 改進了錯誤處理，以解決由 **複製專案：估計 HelperResource 管理** 所產生的 Null 參考例外狀況。
- **時間和資料帳務積存** 上的 **尚未準備好開立發票** 並未清除帳單狀態。
- 更正 **角色價格** 和 **目錄項目** 索引標籤上錯誤標籤的 **價格** 按鈕。


[!INCLUDE[footer-include](../includes/footer-banner.md)]