---
title: Project Service Automation V3 更新版本 28 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 28 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b3afeaf131c8bab25e1ed3a9eb3b41cb3059f711
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586794"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Project Service Automation V3 更新版本 28 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 28 新增或變更的功能和修正；此版本的組建編號為 V3.10.46.32，已於 2021 年 1 月透過自我更新正式推出。

## <a name="update-release-28"></a>更新版本 28

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

下列問題已獲修正：

- 使用者可以使用 **大量編輯** 來更新已核准且已提交的時間項目。

**專案管理**

下列問題已獲修正：

- 在將工作 GUID 解譯為數字的情況下，無法使用 **分工結構圖** 頁面上功能區中的 **編輯工作**，開啟工作以進行編輯。

**Sales**

下列問題已獲修正：

- Null 參考例外狀況是叫用 **GetEstimatesForProject** 外掛程式時所產生。
- 里程碑網格上的 **標示為已準備好開立發票** 除了更新 **InvoiceStatus** 屬性以外，對其他屬性只會進行部分更新。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
