---
title: Project Service Automation 3.x 版 2020 年第 1 段發行浪潮中新推出或已變更的功能
description: 本主題提供 Project Service Automation 版本 3 2020 年第 1 段發行浪潮中新推出或已變更功能的相關資訊。
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
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
ms.openlocfilehash: 5110679038ae7ed1e21a3e7dc80a4657e0752b49
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150928"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Project Service Automation 版本 3 2020 年第 1 段發行浪潮中新推出或已變更的功能

[!include [banner](../includes/psa-now-project-operations.md)]

本主題著重說明移轉至最新發行的 Project Service Automation (PSA) 3.x 版 2020 年第 1 段發行浪潮時的重要升級考量。

## <a name="time-entry"></a>時間項目
時間項目體驗已擴充，以便在更多客戶案例中提供可用於擴充時間項目的功能。 這包括用於新增項目類型的功能，這些類型會根據顯示為 **時間來源** 的欄位結構描述名稱 **時間項目設定** 來促使產生特定行為。 已新增名為「時間、費用、狀態和核准」(TESA) 的新解決方案來支援此功能。

### <a name="upgrade-consideration"></a>升級考量
為了支援此功能，PSA 中的角色已更新為包含新權限。 這些權限會將讀取權限授與新的實體 **時間專案設定**。

除了現有角色之外，還應該將使用者角色 **時間項目使用者** 授與需要記錄時間功能的使用者。 此角色包含新的功能，可確保時間項目會繼續運作。

此外，如果您有任何自訂應用程式模組 (包括時間項目實體的所有表單)，則還必須從模組中移除 **TESA 時間項目快速建立表單**。

### <a name="currently-extended-time-entry-changes"></a>目前已擴充的時間項目變更
為了盡可能降低對目前時間項目使用者的影響，這個角色變更是繼續使用時間項目所需的唯一核心需求。 如果您已建立自訂檢視表或不同的時間項目體驗，就必須將 **時間項目設定** 欄位設定為正確的 PSA 值。


[!INCLUDE[footer-include](../includes/footer-banner.md)]