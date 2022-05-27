---
title: Project Service Automation V3 更新版本 35 的新功能或變更內容
description: 本主題列出 Microsoft Dynamics 365 Project Service Automation 更新版本 35 V3 中可用的功能與修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: e210777f1e4d149b700721ac7fb9bd129b1166fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574018"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Project Service Automation V3 更新版本 35 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation 更新版本 35 V3 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.56.110，已於 2021 年 9 月透過自我更新正式推出。

## <a name="update-release-35"></a>更新版本 35

### <a name="bug-fixes"></a>Bug 修正

下列問題已獲修正。

**時間和費用**

- 專案核准者以 **專案核准者** 角色核准費用項目時，收到讀取權限錯誤。
- 專案核准者以 **專案核准者** 角色取消已核准的時間項目時，他們會在 **msdyn_projectapproval** 上收到寫入權限錯誤。
- 在 [行動電話用 Dynamics 365- 專案資源中心] 應用程式模組的時間項目中選取 **複製週次**，發生下列錯誤：「...\OfficeProductivity_RibbonRules.js.map: HTTP 錯誤: 狀態碼 404，net::ERR_HTTP_RESPONSE_CODE_FAILURE。」
- **重試** 原則會自動核准先前被拒的項目。
- **核准集** 子格會顯示不適用的功能區動作。
- **時間項目** 實體中 **專案工作** 及 **資源角色** 的圖示遺失。
- 匯入資源指派時，所匯入時間項目的期間對透過手動模式工作所建立的指派來說不正確。
- **時間項目進階尋找記錄** 頁面中缺少 **刪除**。
- **時間項目資訊** 頁面中缺少 **儲存**。 此問題會造成無法在頁面關閉時儲存變更。

**專案規劃**

- **資源指派** 和 **資源協調** 網格無法依字母順序排序分組的屬性。
- 如果日期行為已自訂為 **只有日期**，則無法建立工作。

**資源管理**

- 如果 Dynamics 365 Field Service 和 Project Service Automation 都已安裝，則會在 **資源需求相關檢視表** 與主要頁面建立關聯時發生重疊問題。
- 按兩下 **團隊成員快速建立** 對話方塊中的 **儲存** 可防止建立資源需求。

**銷售**

- 如果您刪除與狀態為 **已成交** 之報價相關聯的工作，則會擲回例外狀況。
