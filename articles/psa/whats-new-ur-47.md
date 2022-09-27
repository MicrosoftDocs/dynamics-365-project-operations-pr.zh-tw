---
title: Project Service Automation V3 更新版本 47 的新功能或變更內容
description: 本文列出 Microsoft Dynamics 365 Project Service Automation V3 更新版本 47 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477226"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Project Service Automation V3 更新版本 47 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出 Project Service Automation V3 更新版本 45 新增或變更的功能和修正。 此版本的組建編號為 V3.10.78.8，已於 2022 年 7 月透過自我更新正式推出。

## <a name="update-release-47"></a>更新版本 47

### <a name="bug-fixes"></a>Bug 修正

下列問題已獲修正。

**資源管理**
- 更新了驗證以確保使用者在嘗試建立沒有 **可預訂資源** 的專案團隊成員時不會觸發 Null 參考異常。
