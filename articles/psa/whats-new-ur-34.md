---
title: Project Service Automation V3 更新版本 34 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 34 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 1c8ef43b953ad282a1f5fed6eeeb1e1a991e715100b66938be03b5b5f3da575e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009746"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Project Service Automation V3 更新版本 34 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 34 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.55.38，已於 2021 年 7 月透過自我更新正式推出。

## <a name="update-release-34"></a>更新版本 34

### <a name="bug-fixes"></a>Bug 修正
下列問題已獲修正。

**一般**

- 發行者導向更新未啟用新的現代化核准工作流程。
- **核准集** 主要頁面上缺少 **目標狀態** 及 **動作類型** 屬性。

**時間和費用**

- 無法使用現代化核准流程來核准回收要求。
- 複製與已登入使用者無關的項目時，複製一週的時間項目沒有作用。

**專案規劃**

- 從 Microsoft Project 桌面增益集匯入時，資源指派指派分佈損毀。

**資源管理**

- 從 Microsoft Project 桌面用戶端增益集發佈專案時，現有需求的結束日期會變更。
- 在 [延長預約確認] 對話方塊中，小數點有效位數超過兩個小數位數。

**銷售**

- 將包含現有產品的產品型明細新增至專案合約時，顯示 **字典中找不到索引鍵** 例外狀況。
- 將訂單類型從潛在客戶對應至商機時，無法授與潛在客戶資格。
