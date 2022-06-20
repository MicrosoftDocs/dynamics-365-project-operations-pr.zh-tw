---
title: Project Service Automation V3 更新版本 42 的新功能或變更內容
description: 本文列出 Microsoft Dynamics 365 Project Service Automation V3 更新版本 42 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912705"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Project Service Automation V3 更新版本 42 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出 Project Service Automation V3 更新版本 42 新增或變更的功能和修正。 此版本的組建編號是 V3.10.73.61，已於 2022 年 4 月透過自我更新正式推出。

## <a name="update-release-42"></a>更新版本 42

### <a name="bug-fixes"></a>Bug 修正

下列問題已獲修正。

**時間和費用**

- 工時單遭拒絕時，會將拒絕工時單的使用者錯誤地識別為 **系統**。
- 匯入時間項目時，**資源類別** 值遺失。
- 未將專案核准者的權限明確設定為 **可以核准** 時，他們可以核准已提交的專案。

**銷售**

- 當實際值是記錄在非根層級工作上時，實際成本會不正確彙總。
