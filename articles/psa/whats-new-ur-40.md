---
title: Project Service Automation V3 更新版本 40 的新功能或變更內容
description: 本文列出 Microsoft Dynamics 365 Project Service Automation V3 更新版本 40 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912782"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Project Service Automation V3 更新版本 40 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出 Project Service Automation V3 更新版本 40 新增或變更的功能和修正。 此版本的組建編號為 V3.10.61.61，已於 2022 年 2 月透過自我更新正式推出。

## <a name="update-release-40"></a>更新版本 40

### <a name="features"></a>功能
從 Project Service Automation 至 Project Operations - 精簡版的第 1 階段升級，將於 2022 年 2 月向所有客戶發行。 若要查看所需資格，請參閱[從 Project Service Automation 升級至 Project Operations](upgrade-project-operations-non-stocked.md)。 如果您在 Power Platform 系統管理中心的執行個體沒有出現此應用程式，請連絡支援服務，並要求為您的環境啟用此正式發行前小眾測試版。 您的要求必須附上需要啟用此正式發行前小眾測試版的環境識別碼清單。

### <a name="bug-fixes"></a>Bug 修正

下列問題已獲修正。

**時間和費用**
- 時間項目遭拒絕或取消時，遺失附註項目。 

**銷售**

- 使用現成可用的外掛程式更新成本或銷售估計值時，系統錯誤地允許您傳送在使用者介面之外無效的 JSON 承載。
- 使用快速檢視來更新報價明細時，允許您啟用報價。
