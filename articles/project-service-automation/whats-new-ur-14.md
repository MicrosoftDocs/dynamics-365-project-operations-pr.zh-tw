---
title: Project Service Automation V3 更新版本 14 的新功能
description: 本主題提供 Project Service Automation V3 更新版本 14 中新功能的相關資訊。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749913"
---
# <a name="project-service-automation-v3-update-release-14"></a>Project Service Automation V3 更新版本 14 的新功能
我們很高興宣布 Dynamics 365 Project Service Automation (PSA) 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，然後移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主題列出 PSA V3 更新版本 14 新推出或已變更的功能及修正。 這個版本的組建編號為 V3.10.4.21，依照下列排程提供：

- **正式運作 (自我更新)：** 2020 年 1 月
- **自動更新：** 2020 年 2 月

## <a name="update-release-14"></a>更新版本 14

### <a name="enhancements"></a>增強功能

- Sales

     - 當報價更新為**以成交關閉**時，會將**報價明細詳細資料**中的自訂欄位值複製到**專案合約服務內容詳細資料**。
     - 確認的專案可以是**以未成交關閉**。

- 資源管理

     - 延長預約時，系統會顯示確認對話方塊提示使用者，以摘要列出預約結果並提供 [維護預約] 的連結。


### <a name="bug-fixes"></a>錯誤修正

- 時間和費用

     - 已修正：改善使用者沒有選取任何要更正的項目時的使用者體驗。

- 資源管理

     - 已修正：預約資源多次會溢過可預約資源的名稱。

- Sales

     - 已修正：在使用者另外輸入了專案費用估計值的成本價之前，不會計算總銷售價格。
     - 已修正：如果相關聯的專案合約未處於**草稿**狀態時，以**成交**驗證報價會失敗。

