---
title: Project Service Automation V3 更新版本 45 的新功能或變更內容
description: 本文列出 Microsoft Dynamics 365 Project Service Automation V3 更新版本 45 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169149"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Project Service Automation V3 更新版本 45 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出 Project Service Automation V3 更新版本 45 新增或變更的功能和修正。 此版本的組建編號為 V3.10.76.168，已於 2022 年 7 月透過自我更新正式推出。

## <a name="update-release-45"></a>更新版本 45

### <a name="bug-fixes"></a>Bug 修正

下列問題已獲修正。

**銷售**

- 使用者嘗試建立不含任何未開單銷售的發票之後，如果他們也在檢視該頁面的相同執行個體，但沒有進行重新整理，則無法成功建立發票。

**時間和費用**

- 啟用新式核准已啟用且收回的專案核准已獲准時，記錄階段會不正確地更新為 **回收要求已核准**。
- 新式核准已啟用且雲端流程處於非使用中狀態時，核准程序不會成功，而且不會通知提交或核准使用者。
