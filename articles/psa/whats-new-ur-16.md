---
title: Project Service Automation V3 更新版本 16 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 16 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f277d23e3fb0517f072e51f6f80f855479ab8189
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072955"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation 更新版本 16 V3

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。  此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新偏好的解決方案](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page)。
本主題列出 PSA V3 更新版本 16 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.6.34，已於 2020 年 1 月透過自我更新正式推出。


## <a name="update-release-16"></a>更新版本 16

### <a name="bug-fixes"></a>錯誤修正

-   時間和費用

    -   已修正：嘗試提交已刪除時間及和費用分錄以取得核准的使用者，現在會收到相關的錯誤訊息。

-   專案管理

    -   已修正：範本中團隊成員定義的資源分配單位與套用至新專案的範本有關。

    -   已修正：改善對記錄擁有權重新指派的處理。

    -   已修正：在所有複製作業完成前，不允許複製處於複製過程中的專案。

-   資源管理

    -   已修正：延長預約現在會正確處理短期的期間，不再建立零時數的延長預約。

    -   已修正：協調檢視表現在會在專案時區為 +5:30 GMT 且使用者時區不同時呈現。

-   Sales

    -   已修正：移除對應至合約服務內容的專案並對應新專案時，新專案的實際記錄無法根據合約服務內容所定義的帳務及定價規則進行重新評估。 此問題已在此版本中修正。 新對應專案的定價和實際記錄會根據合約服務內容的定價及帳務規則正確進行沖回和重建。 未對應專案的實際記錄也會因此進行重新評估和重建。

    -   已修正：已將額外驗證新增至估計明細的 **金額** 欄位，以確保 null 值不會繼續存在。

    -   已修正：專案的實際值已更新時，已將重新整理按鈕新增至專案主要表單，以允許使用者重新同步實際值。

    -   已修正：使用者從 2.X 升級至 3.X 時，允許專案名稱含 NULL 值的專案。

