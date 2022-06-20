---
title: Project Service Automation V3 更新版本 21 的新功能或變更內容
description: 本文列出 Project Service Automation V3 更新版本 21 中提供的功能和修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 7d7c098a4572aa4f5730ffdbdab77b2897cdfeff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918808"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation 更新版本 21 V3

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出 Project Service Automation V3 更新版本 21 新增或變更的功能和修正。 此版本的組建編號為 V 3.10.32.50，已於 2020 年 6 月透過自我更新正式發行。

## <a name="update-release-21"></a>更新版本 21

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

下列問題已獲修正：

- 在儀表板中裝載 **時間項目網格控制項** 時，網格未使用儀表板網格容器的全幅寬度。
- 對於特定時區，**時間項目** 網格控制項無法顯示記錄。
- 下午 9:00 以後的時間項目出現在錯誤的日期上。
- 如果費用類別 **需要費用收據** 沒有值，使用者就無法提交費用。

**資源管理**

下列問題已獲修正：

- 非使用中預約會顯示 **協調** 檢視表中。
- 一般資源履行缺少驗證，無法確保存在有效的預約狀態。

**專案管理**

下列問題已獲修正：

- 即使專案處於非使用中狀態，**專案** 表單網格 (**資源指派**、**工作**、**協調** 檢視表、**費用估計值**) 仍會保持可編輯。
- 重複的客戶無法與連結至已確認專案合約的客戶合併。
- 新增未具備有效行事曆的資源時，系統不會傳回使用者易懂的錯誤訊息。
- 當專案連結至 **Microsoft Project 增益集** 時，工作網格會啟用 **新增工作** 按鈕。
- 當工作的類別已指派給其角色沒有定義成本價的資源時，投入量會不受控制地擴大。

**Sales**

我們已進行下列增強：

- **發票頻率** 和 **帳單開始日期** 已移到 **發票排程** 索引標籤。

下列問題已獲修正：

- **類別** 的 **總售價** 為零 (0)，即使 **角色** 的總售價不為零也一樣。
- 另一個自訂程序正在更新其他欄位時，客戶無法將 **發票狀態** 欄位值變更為 **已準備好開立發票**。
- 如果重複選取 **重新整理發票明細** 按鈕，此按鈕可以建立多個重複的明細。
- **更新價格** 按鈕在 **快速檢視** 表單的 **角色價格** 子格上不起作用。
- **銷售價目表解析** 邏輯處理時區不當，導致錯誤選擇價目表。
- 核准單一時間項目之後，專案的 **總實際成本** 可能會不計整數以外尾數的金額。
- 如果 **擷取的角色價格** 沒有 **主要單位** 及 **以主要單位計的價格** 欄位中的值，**價格解析** 邏輯無法提供使用者易懂的錯誤訊息。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
