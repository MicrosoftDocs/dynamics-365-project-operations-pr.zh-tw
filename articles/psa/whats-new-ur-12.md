---
title: Project Service Automation V3 更新版本 12 的新功能或變更內容
description: 本主題提供 Project Service Automation V3 更新版本 12 中新功能的相關資訊。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 2712cc671e9868bc4b3b143a2067da4381102eda
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577410"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation 更新版本 12 V3

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興宣布 Dynamics 365 Project Service Automation (PSA) 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，然後移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 12 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.2.34，已於 2019 年 10 月透過自我更新正式推出。

## <a name="update-release-12"></a>更新版本 12

### <a name="bug-fixes"></a>錯誤修正

- 時間和費用

    - 已修正：時間項目錯誤訊息已更新為相關性更高的內容。
    - 已修正：時間項目網格和排程會視需要正確顯示垂直捲軸。
    - 已修正：可以核准已送出的費用及時間項目。
    - 已修正：[取消核准] 確認對話方塊訊息已更正為可在狀態由 **已核准** 變更成 **已送出** 時反映核准狀態。
    - 已修正：核准了費用記錄之後，現在會鎖定此記錄上的 **價格**、**單位** 和 **品質** 欄位。

- 專案管理

    - 已修正：**團隊成員** 主要表單上的 **新增** 動作已移除。
    - 已修正：資源指派已更新，可解決不正確的捨入錯誤，此錯誤會導致工作結束日期變動。
    - 已修正：在工作網格中，會向使用者顯露相關的伺服器端錯誤。
    - 已修正：團隊成員在工作人員選擇器中顯示的是其姓名而不是職位名稱。

- 資源管理

    - 已修正：從範本所建立之專案的資源需求詳細資料現在會使用專案行事曆。
    - 已修正：技能和專長現已從角色主要資料預設為針對該角色建立的資源需求。

- Sales

    - 已修正：在 **合約主要** 表單上發現了重複的物件識別碼。
    - 已修正：邏輯已更新，使得 **報價分析** 索引標籤可見，以便顯示索引標籤的中繼資料設定。
    - 已修正：實際記錄上的會計日期現在是來自時間/費用項目日期，而不是核准日期。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
