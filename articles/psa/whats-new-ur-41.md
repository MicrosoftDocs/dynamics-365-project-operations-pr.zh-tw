---
title: Project Service Automation V3 更新版本 41 的新功能或變更內容
description: 本主題列出 Microsoft Dynamics 365 Project Service Automation 更新版本 41 V3 中可用的功能與修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580906"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Project Service Automation V3 更新版本 41 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation 更新版本 41 V3 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.62.162，已於 2022 年 3 月透過自我更新正式推出。

## <a name="update-release-41"></a>更新版本 41

### <a name="bug-fixes"></a>Bug 修正

下列問題已獲修正。

**專案管理**
- 嘗試從以根據桌面增益集所建立之專案為基礎的範本建立專案時，會顯示下列錯誤：「資源指派的 [計劃的工作] 欄位驗證: 每個資源指派時間配量的結束日期不可早於其開始日期」。

**時間和費用**
- 嘗試刪除時間項目時，會顯示下列錯誤訊息：「ISV 程式碼中發生未預期的錯誤」。

**銷售**
- 建立固定價格里程碑的發票時，資料不會填入 **描述** 及 **外部描述** 欄位。 
