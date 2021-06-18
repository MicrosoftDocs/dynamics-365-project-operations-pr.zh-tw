---
title: Project Service Automation V3 更新版本 24 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 24 V3 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000246"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation 更新版本 24 V3

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 24 新推出或已變更的功能及修正。 此版本的組建編號為 V 3.10.42.43，已於 2020 年 10 月透過自我更新正式推出。

## <a name="update-release-24"></a>更新版本 24

### <a name="bug-fixes"></a>Bug 修正

**Sales**

下列問題已獲修正：

- 設定產品的預設價目表時發生問題。
- 報價成交效能因內嵌價目表及角色價格記錄複本而變慢。
- **專案合約/銷售中心** > **產品條項/訂單明細數量** 會自動捨入至最接近的整數。
- 讀取價目表時，提高權限至系統權限。
- 將客戶地址欄位 **address1_freighttermscode** 及 **address1_shippingmethodcode** 複製到報價/訂單。 


**時間和費用**

下列問題已獲修正：

- **時間項目網格** 不支援 **只有日期** 時間行為。
- **時間項目** 未自動重新整理。 需要手動重新整理。
- 資源指派中有休息時數 (0 小時) 時，無法從指派匯入時間項目。
- 建立時間項目時，將開始時間設定成與 **msdyn_date** 相同。
- 重新啟用對時間項目的大量編輯。

**資源管理**

下列問題已獲修正：

- 嘗試更新無需求異日間預約的狀態會擲回 Null 參考例外狀況。
- 載入 **協調檢視表** 時發生錯誤。


**專案管理**

下列問題已獲修正：

- 在 **專案排程** 中，從 **手動** 變更為 **自動** 時，自動儲存將不會完成。
- 費用成本不應在 **專案追蹤網格** 上針對差異進行計算。
- **估計值標籤** 欄在載入期間相對於變更 **分時期** 類型時的行為不一致。
- 專案的實際成本可能不會反映 **實際值** 的總計。
- **摘要** 索引標籤上的 **估計完成日期** 與 **WBS 排程** 不相符。
- 凸排上的 **更新實際時數** 無法正常運作。
- 在根 **業務單位** 外部的專案經理無法建立專案。
- 對 **費用估計值** 的工作或類別所做的變更無法保存。
- **合約複本** 會複製發票排程和執行狀態。
- **重新整理實際值** 按鈕未正確計算摘要工作。
- Microsoft Project 增益集：如果任何團隊成員有空白資源分配單位，則修正 Null 參考錯誤。



[!INCLUDE[footer-include](../includes/footer-banner.md)]