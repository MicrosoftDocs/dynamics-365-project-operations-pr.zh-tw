---
title: Project Service Automation V3 更新版本 29 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 29 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010461"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Project Service Automation V3 更新版本 29 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 29 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.47.7，已 2021 年 2 月透過自我更新正式推出。

## <a name="update-release-29"></a>更新版本 29

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

下列問題已獲修正：

- 使用者在時間項目網格中看不到非工作日上記錄的工作時數。
- 可以在網格上編輯已核准的費用項目。

**專案管理**

下列問題已獲修正：

- 找不到用於確保資源指派投入時數不可為負數的驗證邏輯。
- 自訂動作 **AssignResourcesForTask** 會更新所有欄位，而不是只更新已變更的欄位。
- 在使用已於 **CreateProject** 事件註冊之外掛程式或工作流程的環境中複製專案時，如果 **CopyWBSToProject** 失敗，則不會更新 **msdyn_bulkgenerationstatus** 屬性。
- 展開專案行事曆時，工作日不會依遞增順序排序，造成部分專案工作更新失敗。
- 變更現有專案的專案經理時會觸發組織單位的設定預設值邏輯。

**銷售**

下列問題已獲修正：

- 沒有任何合約服務內容存在時，**合約** 頁面上的 **合約績效** 索引標籤會在初始化期間以無訊息方式失敗。