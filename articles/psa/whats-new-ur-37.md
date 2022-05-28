---
title: Project Service Automation V3 更新版本 37 的新功能或變更內容
description: 本主題列出 Microsoft Dynamics 365 Project Service Automation 更新版本 37 V3 中可用的功能與修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: e8696d84aaca019c2e12d852e669df71146484b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593464"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Project Service Automation V3 更新版本 37 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation 更新版本 37 V3 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.58.120，已於 2021 年 11 月透過自我更新正式推出。

## <a name="update-release-37"></a>更新版本 37

### <a name="bug-fixes"></a>錯誤修正

下列問題已獲修正。

**時間和費用**
- 使用者無法以清除儲存格的方式刪除時間項目。
- **我失敗的核准** 檢視表僅包含狀態為 **已送出** 的專案核准。

**專案管理**
- 如果專案團隊成員的職位名稱為空白，則在 Microsoft 桌面增益集中開啟專案時，使用者會收到 Null 參考例外狀況錯誤。
- **專案工作** 頁面上沒有 **儲存** 按鈕，因此使用者無法儲存對工作記錄的變更。
- 使用者無法刪除其工作與狀態為 **已成交** 之報價有關聯的專案。

**銷售**
- **專案** 頁面上的 **貨幣** 欄位會更新，以符合所套用範本的貨幣。
- 有多種貨幣的工作，其成本計算會不正確。
