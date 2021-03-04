---
title: Project Service Automation V3 更新版本 17 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 17 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143691"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation 更新版本 17 V3

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。  此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主題列出 PSA V3 更新版本 17 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.6.34，已於 2020 年 3 月透過自我更新正式推出。


## <a name="update-release-17"></a>更新版本 17

### <a name="bug-fixes"></a>錯誤修正

**一般**

- 已修正：更新 Project Service Automation 以實行團隊成員授權 (專案資源中心將會包含團隊成員服務方案中繼資料 3.x)
 
**時間和費用**

- 已修正：無法將費用估計值從非零價格變更為零 (0)。 變更會遭忽略。

**專案管理**

- 已修正：已新增對團隊成員職位名稱的 null 值檢查。
- 已修正：**msdyn_resourceassignment** 實體上的 **msdyn_userresourceid** 欄位已被取代。
- 已修正：從 2.x 到 3.x 的升級現在會在工作指派上處理空白努力分佈。

**Sales**

- 已修正：**Invoice.PreValidateInvoiceUpdate** 現在會正確處理重新指派記錄負責人。
- 已修正：交易類別為 **時間** 時，**UnitGroup** 對所有實體 (包括 **QuoteLineDetails**、**JournalLine**、**InvoiceLineDetail** 和 **ContractLineDetails**) 都是不可編輯的。 不過，**單位** 只有對 **JournalLine** 和 **InvoiceLineDetails** 才是不可編輯。


