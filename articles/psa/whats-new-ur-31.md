---
title: Project Service Automation V3 更新版本 31 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 31 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 2e5fce003c25f9c5911e5a01fb4ec3e19c06c078e00b054472699a522b9cd070
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002141"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Project Service Automation V3 更新版本 31 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 31 新推出或已變更的功能及修正。 此版本的組建編號是 V3.10.52.77，已於 2021 年 5 月透過自我更新正式推出。

## <a name="update-release-31"></a>更新版本 31

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

下列問題已獲修正：

- **可預約資源** 頁面上的時間項目控制項命令按鈕造成混淆。
- 核准時間項目時，在 **Project.SetTrackingFields** 中產生了 Null 參考例外狀況。

**資源管理**

下列問題已獲修正：

- **建立團隊成員** 未正確顯示 **預設預約認可狀態** 的預約設定中繼資料設定。
- 從 PSA 1.X 升級至 3.X 時，升級程序會在 **UpgradeResourceRequirements** 處失敗。


**銷售**

下列問題已獲修正：

- 實際營收會將金額轉換為追蹤網格中的專案貨幣。
- 在組織基準貨幣與專案貨幣不同的案例中建立帳目明細、報價明細和合約服務內容時，貨幣預設值不明確。
- **擱置中更正帳目驗證** 查詢未依專案進行篩選。
- 專案中的剩餘銷售計算不正確。
- 未使用價目表來建立以合約為根據的報價時，這些報價會失敗。
- 選取 **確認發票** 時，未顯示任何處理微調按鈕。
- 選取 **建立發票** 時，未顯示任何處理微調按鈕。
- 以未成交關閉報價不會取消預約。







