---
title: Project Service Automation V3 更新版本 13 的新功能
description: 本主題提供 Project Service Automation V3 更新版本 13 中新功能的相關資訊。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749914"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation V3 更新版本 13 的新功能
我們很高興宣布 Dynamics 365 Project Service Automation (PSA) 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，然後移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation V3 更新版本 13 新推出或已變更的功能及修正。 這個版本的組建編號為 V3.10.3.18，依照下列排程提供：

- **正式運作 (自我更新)：** 2019 年 11 月
- **自動更新：** 2019 年 12 月


## <a name="update-release-13"></a>更新版本 13 

### <a name="bug-fixes"></a>錯誤修正

- 時間和費用

     - 已修正：依費用目的進行搜尋時，**費用核准l**頁面上的搜尋功能無法運作。

- 資源管理

     - 已修正：協調中的數字已更新為靠右對齊。
     - 已修正：無法透過**排程**索引標籤將具名資源指派給工作。

- 專案管理

     - 已修正：在 **TransactionType** 缺少 **Unit** 及 **DefaultGroup** 設定資訊的情況下指派團隊成員時，發生 Null 參考例外狀況。

- Sales

     - 已修正：建立角色價格記錄時，重複的交易類型記錄傳回錯誤。
     - 已修正：**新商機**、**報價**、**訂單明細**和**新增產品**的額外按鈕出現在商機、報價、訂單產品及專案型明細子格的命令中。


