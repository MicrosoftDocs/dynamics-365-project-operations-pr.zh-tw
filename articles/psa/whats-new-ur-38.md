---
title: Project Service Automation V3 更新版本 38 的新功能或變更內容
description: 本主題列出 Microsoft Dynamics 365 Project Service Automation 更新版本 38 V3 中可用的功能與修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598708"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Project Service Automation V3 更新版本 38 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation 更新版本 38 V3 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.59.117，已於 2021 年 12 月透過自我更新正式推出。

## <a name="update-release-38"></a>更新版本 38

### <a name="bug-fixes"></a>Bug 修正

下列問題已獲修正。

**時間和費用**

- 當核准集記錄的長度超過 100,000 筆記錄時，就會發生例外狀況。
- 使用者無法從 **時間項目** 主要頁面存取 **時間項目** 網格。
- 沒有任何項目適合匯入時，**時間項目匯入** 對話方塊不會顯示任何文字。
- 使用者可以建立 **目標狀態** 欄位設定為 **未知** 的核准集。

**專案管理**

- 當日光節約時間開始時，分佈無法正確顯示在 UTC(+09:30) 和 UTC(+10:00) 的資源指派中。
- 分工結構圖的 **其他資料行** 欄位會在某些地區設定下隱藏。
- **專案工作** 網格中行事曆控制項的日期選擇器未正確地當地語系化為中文。

**銷售**

- 當具有不同合約單位和貨幣的可預約資源提交時間項目時，**合約績效** 與 **專案實際成本** 值不相符。
- 將發票匯入為受管理的解決方案時，自動確認發票的自訂工作流程會失敗。 顯示的訊息如下：「Microsoft.Xrm.Sdk.InvalidPluginExecutionException 訊息：發票狀態無效。」
- 選取 **根** 做為摘要選項，且專案具有混合交易類別的估計值 (例如，時間、費用與材料估計值的組合) 時，系統會將各個交易類別彙總為單一費用明細。
- 在費用明細是於合約服務內容與專案建立關聯之前所新增的案例中，**更新價格** 欄位中未輸入正確的定價做為預設值。
- **專案** 及 **工作** 實體不允許負數的銷售金額。
