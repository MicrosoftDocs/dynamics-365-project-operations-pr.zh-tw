---
title: Project Service Automation V3 更新版本 23 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 23 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131108"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation 更新版本 23 V3

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 23 新推出或已變更的功能及修正。 此版本的組建編號為 V 3.10.34.30，已於 2020 年 8 月透過自我更新正式推出。

## <a name="update-release-23"></a>更新版本 23

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

下列問題已獲修正：
- 處理 **專案團隊成員刪除** 中的邊緣案例，以提供有意義的例外狀況。
- 指派匯入會產生空白移除畫面。

**資源管理**

下列問題已獲修正：

- 時幅超過五天時，**資源使用率網格資源卡片** 會顯示不正確的資料。
- 客戶建立可預約資源時，外掛程式會間歇性發生無法自動將資源新增至 Microsoft Office 365 群組的情況。
- **協調** 檢視表未正確顯示 **週** 或 **月** 檢視表中的手動分佈。

**專案管理**

下列問題已獲修正：

- 過多 **使用者設定的 RetrieveMultiple** 實體造成專案核准及其他作業的效能降低。
- **工作規劃** 網格資源查詢受到限制，最多只能顯示五個來自專案團隊的團隊成員。 
- **工作規劃** 網格資源查詢不會篩選非使用中資源。
- 在專案規劃分工結構圖中，手動模式無法依預期正常運作。
- **工作規劃** 網格會顯示 **非使用中交易類別**。
- 工作有多個指派時，**資源指派** 網格捨入不正確。
- 單一工作的捨入值在計劃成本與實際成本之間不相同。

**Sales**

下列問題已獲修正：

- 按兩下 **擷取所有交易類別** 會建立多行。
