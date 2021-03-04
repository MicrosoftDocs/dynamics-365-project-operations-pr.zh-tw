---
title: Project Service Automation V3 更新版本 15 的新功能或變更內容
description: 本主題提供 Project Service Automation V3 更新版本 15 中新功能的相關資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 0ec6746c0d3a1a03ee56440c73d044df844046f8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143953"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation 更新版本 15 V3

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興宣布 Dynamics 365 Project Service Automation (PSA) 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，然後移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主題列出 PSA V3 更新版本 15 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.5.28，已於 2020 年 1 月透過自我更新正式推出。

## <a name="update-release-15"></a>更新版本 15 

### <a name="enhancements"></a>增強功能

- 專案管理

### <a name="bug-fixes"></a>錯誤修正

- 時間和費用

  - 已修正：在協調檢視表中新增載入時錯誤處理功能。
  - 已修正：專案資源中心：重新命名 **金額** 以減少模稜兩可的情況。
  - 已修正：調整 **複製時間項目欄** 檢視表以包含類型。
  - 已修正：使用小數點編輯網格檢視表中的時間項目期間會導致部分數字發生不明的錯誤。

- 專案管理

  - 已修正：**在追蹤檢視表中使用** 的下拉式功能表現在會根據選項的寬度展開。
  - 已修正：管理 +13 時區的專案時，工作計算可能會顯示不正確的結果。
  - 已修正：使用 24 小時制行事曆時，**團隊成員結束時間** 已更正。
  - 已修正：已在 **msdyn_project** 主要表單中重新啟用 **BPF**。
  - 已修正：指派計算不再忽略一天。
  - 已修正：已在使用者與專案之間的時區不同時，將新的通知橫幅加入至專案表單。

- Sales

  - 已修正：費用估計值類別查詢可以用來篩選重復資料。
  - 已修正：**PluginDomain.ExecuteInTryCatchBlock(..)** 中的程式碼不再隱藏例外狀況的來源。
  - 已修正：當有 1000 個以上的專案時，不再於 **報價明細** 表單中的 **專案查詢** 中收到錯誤訊息。
  - 已修正：人力估計值及費用估計值的 **估計值** 網格現在會顯示正確的貨幣符號。
  - 已修正：組織將 PSA 從更新版本 14 更新為更新版本 15 之後，**排程** 索引標籤不再於 **專案** 表單上顯示為空白。


[!INCLUDE[footer-include](../includes/footer-banner.md)]