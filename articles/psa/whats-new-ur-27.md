---
title: Project Service Automation V3 更新版本 27 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 27 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146653"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Project Service Automation V3 更新版本 27 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 27 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.45.98，已於 2021 年 1 月透過自我更新正式推出。

## <a name="update-release-27"></a>更新版本 27

### <a name="bug-fixes"></a>Bug 修正

**一般**

下列問題已獲修正：

- Project Service Automation 中外掛程式所產生的記錄檔尚未設定為自動刪除。
- 因為 Project Service Automation 解決方案包含舊版 Null NavBarArea 和標題元素，自動升級失敗。

**時間和費用**

下列問題已獲修正：

- **時間項目** 網格顯示不正確的 **時區不轉換** 日期行為資料。
- **時間項目** 網格建立不正確的 **時區不轉換** 日期行為時間。
- 工作查詢未受限於 **編輯時間項目** 頁面上所選取的專案。
- 非專案時間項目的時間核准因系統正在尋找專案核准者而遭封鎖。
- [更新實際值上的項目] 顯示不正確的錯誤訊息。
- 當工作的實際成本包含 Null 值，且專案總計進行重新整理時，發生下列錯誤：「字典中沒有指定的索引鍵」。
- 在特定情況中，**專案估計值** 索引標籤上的 **群組依據** 篩選未顯示費用估計值。
- 時間項目的 **日光節約時間** 間隔不正確。

**專案管理**

下列問題已獲修正：

- 快取改進功能，增強與載入 **專案** 頁面相關的效能。
- 廢棄造成無法完成專案工作的商務規則。
- Microsoft Project 增益集分佈未遵循增益集的行事曆，並產生不正確的資源需求。
- 從範本建立專案時不正確設定指派日期，造成無法產生資源需求。
- 使用者無法使用鍵盤存取 **類別**、**描述**、**狀態** 選項。
- 專案的實際銷售值未包含服務費和材料銷售值。
- 實際銷售與實際成本的彙整錯誤地使用不同的匯率來進行。
- **預設工作時數範本** 中的描述會使人誤解。
- 縮排工作時，除非重新整理使用者介面，否則不會移除其中的 **類別**。
- 缺少驗證，無法確保禁止移動專案超過其結束日期。

**Sales**

下列問題已獲修正：

- 專案報價明細產生 Null 參考例外狀況，因為尚未選取專案時可看到 **從專案估計匯入**。
- 以 **成交** 關閉報價時，發生下列錯誤：「物件參考未設定為物件的執行個體」。
- 從合約服務內容解除專案連結時，實際值沖銷期間未設定調整狀態。
- Dynamics 365 Field Service 和 Project Service Automation 都已安裝時，**鎖定價格** 和 **使用目前定價** 選項未同時顯示在 **發票** 頁面上。
- 就日文語言而論，在其他行事曆頁面上的翻譯有不一致的地方。
- **啟用** 和 **停用** 已從 Project Service Automation 的 **價目表關聯** 實體中移除。
