---
title: Project Service Automation V3 更新版本 37.5 的新功能或變更內容
description: 本主題列出 Microsoft Dynamics 365 Project Service Automation 更新版本 37.5 V3 中可用的功能與修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/15/2021
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
ms.openlocfilehash: f4bb9a33f72cd98b74a4576bcc2a3760b42b3486
ms.sourcegitcommit: 6a852ca1e3aacb55d7357cd474d2f07b39381f03
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/16/2021
ms.locfileid: "7816149"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-375-v3"></a>Project Service Automation V3 更新版本 37.5 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation 更新版本 37.5 V3 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.58.130，已於 2021 年 11 月透過自我更新正式推出。

## <a name="update-release-375"></a>更新版本 37.5

### <a name="bug-fixes"></a>Bug 修正

下列問題已獲修正。

**資源管理**
- 當您更新現有的預約，且 **增加時數方法** 和 **減少時數方法** 選取的是 **按比例** 時，將會建立重複的預約。
