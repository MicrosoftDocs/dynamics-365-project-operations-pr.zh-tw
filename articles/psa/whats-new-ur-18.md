---
title: Project Service Automation V3 更新版本 18 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 18 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: f7def50e77a83fd790b81b1b4fd36008ce293b0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006636"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation 更新版本 18 V3

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 18 新推出或已變更的功能及修正。 此版本的組建編號是 V3.10.8.12，已於 2020 年 4 月透過自我更新正式推出。

## <a name="update-release-18"></a>更新版本 18

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

- 已修正：**回收**、**要求** 和 **取消核准** 流程擲回例外狀況，並出現不明確的錯誤訊息。
- 已修正：費用的 **取消核准** 失敗時，未擲回相關的錯誤。
- 已修正：在 10 月份的日光節約時間 (DST) 切換之後，時間項目網格未正確處理澳大利亞的非工作日。
- 已修正：不正確的預設邏輯導致無法提交費用。
- 已修正：時間項目核准失敗時，核准仍保持在 **擱置** 狀態。
- 已修正：大量核准時發生 SQL 錯誤 (鎖死/逾時)。
- 已修正：核准時間項目時，使用者體驗因更新團隊成員而產生重大效能問題。

**專案管理**

- 已修正：時區通知已從 **協調** 檢視移到 **專案** 主要表單。
- 已修正：新的專案表單開啟時，行事曆範本未正確使用預設值。
- 已修正：使用以 Chromium 為基礎的瀏覽器時，使用者無法輕鬆地選取要刪除的前置工作。
- 已修正：建立或複製 **專案 (從空白範本)** 會擷取無關的指派。
- 已修正：在特定邊緣案例中，從工作網格建立新指派會導致建立重複的記錄。
- 已修正：在手動模式下，使用者無法將工作開始日期更新成晚於已儲存的目前日期。

**資源管理**

- 已修正：延長預約之後，**協調** 檢視表小計列計算的預約差異不正確。
- 已修正：可預約資源的行事曆與專案行事曆不相符時，**協調** 檢視表無法正確顯示資源指派。

**Sales**

- 已修正：重新核准時間項目 (**核准 > 取消 >** 再次核准) 時，會建立重複的不應收費實際值。


[!INCLUDE[footer-include](../includes/footer-banner.md)]