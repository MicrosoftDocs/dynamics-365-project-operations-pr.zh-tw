---
title: Project Service Automation V3 更新版本 30 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 30 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852835"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Project Service Automation V3 更新版本 30 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 30 新推出或已變更的功能及修正。 此版本的組建編號是 V3.10.51.61，已於 2021 年 4 月透過自我更新正式推出。

## <a name="update-release-30"></a>更新版本 30

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

下列問題已獲修正：

- 在 **快速建立** 頁面上建立並儲存時間項目時，如果 **角色** 欄位已移除，就會發生錯誤。
- 時間項目篩選套用錯誤的篩選運算子。
- 選取時間項目控制項上的 **複製週次** 時，未自動顯示複製的工時表。

**資源管理**

下列問題已獲修正：

- 延長預約時，指派給已確認預約的預約狀態不正確。 延長預約會採用預約設定中繼資料中定義為 **已認可** 的預約狀態。
- 未指定有效的預約狀態時，錯誤訊息未正確當地語系化。

**專案管理**

下列問題已獲修正：

- 專案不可以是使用一種貨幣所建立，卻又包含使用其他貨幣的相關工作。

**銷售**

下列問題已獲修正：

- 複製價目表時，未更新價格。
- 當成本明細具有來源的值時，以成交關閉報價會失敗。
- 在 **專案工作** 實體上，**估計成本** 已重新命名為 **規劃成本 (基準貨幣)**。
- 建立或刪除發票時，產生 Null 參考例外狀況。
