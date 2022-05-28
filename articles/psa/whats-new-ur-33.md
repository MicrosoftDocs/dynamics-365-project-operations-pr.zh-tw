---
title: Project Service Automation V3 更新版本 33 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 33 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601468"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Project Service Automation V3 更新版本 33 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 33 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.54.98，已於 2021 年 7 月透過自我更新正式推出。

## <a name="update-release-33"></a>更新版本 33

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

下列問題已獲修正：

- 兩個鎖定的欄位 **msdyn_description** 和 **msdyn_externaldescription** 可在提交後進行編輯。
- 如果建立與專案無關的費用，就會出現錯誤訊息。
- 建立時間項目時，該資源角色預設為非使用中角色。
- 不會刪除與已回收及已刪除費用相關聯的帳目明細。
- 在 **時間項目快速建立表單** 上，更新 **專案工作清單** 檢視表，以將預設顯示的日期變更為工作的開始日期。
- 從可預約資源的 **相關** 索引標籤建立時間項目時，已登入的使用者 (而不是上層可預約資源) 會不確定地建立時間項目。
- 新的欄位會新增至 **大量核准 MDD** 對話方塊。

**專案規劃**

下列問題已獲修正：
- 使用複雜行事曆套用專案工時數範本時，會讓專案建立效能變慢。
- 開始日期大於結束日期時，錯誤會顯示在複製專案範本上，因為每個欄位的時間元件有差異。

**資源管理**

下列問題已獲修正：
- 資源使用率查詢中使用了不正確的參數，而 XML 在 **資源使用率** 網格中導致不正確的篩選結果。
- **延長預約確認** 會顯示不正確的預約結束日期。

**銷售**

下列問題已獲修正：
- 如果類別價格是以遺失的值建立，就會出現錯誤訊息。
- 如果合約服務內容里程碑是在不使用訂單明細的情況下所建立，就會出現錯誤訊息。
