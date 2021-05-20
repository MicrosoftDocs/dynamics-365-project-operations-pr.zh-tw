---
title: Project Service Automation V3 更新版本 19 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 19 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949129"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation 更新版本 19 V3

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 PSA V3 更新版本 19 新推出或已變更的功能及修正。 此版本的組建編號是 V3.10.30.41，已於 2020 年 5 月透過自我更新正式推出。

## <a name="update-release-19"></a>更新版本 19

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

下列問題已獲修正： 

- 無法正確顯示從時間項目匯入衍生的錯誤。
- 時間項目網格不支援 **只有日期** 欄位行為。
- 專案資源無法建立專案的費用。

**專案管理**

下列問題已獲修正： 

-  下下層工作在完工估計值 (EAC) 計算過程中造成努力估計值不正確。

**Sales**

下列問題已獲修正： 

- **重新計算** 動作無法使用費用合約服務內容詳細資料或報價明細詳細資料。
- 費用估計值缺少 **更新價格**。
-  客戶無法從 **專案合約** 頁面選取自訂合約狀態原因。
- 從報價建立自訂價目表時，客戶感受到效能變差。
- 客戶發現 **報價明細詳細資料** 與 **合約服務內容詳細資料** 頁面上的 **單位** 預設值不一致。
- 將非收費交易類別項目新增至收費合約服務內容時，不會採用 **非收費** 帳單類型的交易類別。
- 客戶無法在先前建立的合約上使用新加入的角色和類別。
- 客戶感受到效能變差 PreValidateProjectTeamMemberUpdate.cs 中不必要的擷取
- 必須將 **資源類別** 清單中設定為非收費的角色當做專案合約服務內容的 **非收費項目** 新增至 **收費角色** 索引標籤。
- 建立專案時，客戶可能會感受到效能變差，因為 **GetBookableResourceIdFromUser** 擷取的是可預約資源所有的欄，而不只是主要識別碼。
- **TransactionType** 實體缺少預先驗證更新外掛程式，無法防止使用者輸入對交易類型不正確的 **單位** 和 **單位群組**。
- **移除** 步驟不適用於時間項目匯入。


[!INCLUDE[footer-include](../includes/footer-banner.md)]