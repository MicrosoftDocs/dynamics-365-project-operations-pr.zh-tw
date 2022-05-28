---
title: Project Service Automation V3 更新版本 20 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 20 V3 中提供的功能和修正
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 4b1a8b5b65f0dfeeff74db363c918206c64e81f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588818"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation 更新版本 20 V3

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 20 新推出或已變更的功能及修正。 此版本的組建編號為 V 3.10.31.37，已於 2020 年 6 月透過自我更新正式發行。

## <a name="update-release-20"></a>更新版本 20

### <a name="bug-fixes"></a>Bug 修正

**專案管理**

下列問題已獲修正：

- 使用需要時數的配置方法匯入專案團隊成員會在指定的時數為零時產生不明確的錯誤訊息。
- 在專案工作的 **描述** 欄位中輸入數目已達上限的字元時，使用者收到不正確的錯誤訊息。
- 當使用者的語言設定設為日文時，**Microsoft Dynamics 365 Project Service Automation 增益集下載** 頁面會重新導向至英文下載頁面。
- 發生伺服器錯誤時，**專案** 表單 **排程** 索引標籤上的同步處理標籤有時會保留。
- 工作遭修改時，多餘的工作更新將會傳送至伺服器。

**Sales**

下列問題已獲修正：

- 在 **合約** 表單上，按兩下 **建立發票** 會為單一實際值記錄建立兩份發票。
- 在 Internet Explorer 11 中，使用者無法建立費用分錄。
- 成本沖回與未開單銷售實際值沖回未連結。
- **專案** 表單上的 **重新整理實際值** 按鈕不會重新整理 **工作實際時數**。
- 將 **msdyn_isgenericresourceprojectscoped** 屬性設定為 **否** 時，**PreValidateProjectTeamMemberCreate** 外掛程式可能會建立重複的一般可預約資源。
- **重新計算** 會清除產品型報價明細詳細資料和合約服務內容詳細資料的應收費成本。
- 在特定案例中，**PostEstimateLineUpdate** 外掛程式會顯示 Null 參考例外狀況錯誤。
- **獲利率分析圖表** 的時間階段期間與報價固定價格報價明細詳細資料中的成本期間不相符。
- 在 **合約服務內容詳細資料** 和 **報價明細詳細資料** 表單上的費用類別未正確設定單位與單位群組的預設值。
- **組織單位成本價** 清單允許日期時效性有重疊。
- 當訂單類型不是工作型時，不允許使用者變更 **組織單位**，因為這會導致 Null 參考例外狀況錯誤。
- 嘗試從 **報價明細詳細資料** 表單瀏覽返回 **報價** 索引標籤時，表單會重新整理並顯示 **摘要** 索引標籤。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
