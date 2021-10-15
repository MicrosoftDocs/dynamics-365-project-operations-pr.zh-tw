---
title: Project Service Automation 中的核准集
description: 本主題提供有關核准集、要求以及這些作業子集的資訊。
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9a7a9efbd8615f4923c6795a16c9cf98a40362b6
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323541"
---
# <a name="approval-sets-in-project-service-automation"></a>Project Service Automation 中的核准集

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

核准集會將核准要求集合成較小型作業子集的群組。 這種群組方式可讓各項核准按照專案依序處理，並允許重試和排序。 群組功能可改善對大量核准記錄的核准處理可靠性和可追蹤性。

核准集表示其相關記錄的整體處理狀態。 使用核准集來處理核准記錄時，該記錄會從 **已提交** 移至 **已核准** 狀態，並解除與核准集的連結。 如果記錄在提交供核准時失敗，則記錄仍會保持在 **已提交** 狀態，而核准集會標示為失敗。 核准集會記錄失敗的錯誤訊息。

## <a name="processing-approvals-and-approval-sets"></a>處理核准和核准集
已排入佇列等待處理的核准會顯示在 **處理核准** 檢視表中。 系統會嘗試以非同步方式處理所有專案，包括會在前一次嘗試失敗時重試核准。

**核准集存留期** 欄位會記錄將此集合標示為失敗前，剩餘的嘗試處理次數。

## <a name="failed-approvals-and-approval-sets"></a>失敗的核准和核准集
**失敗的核准** 檢視表會列出所有需要使用者介入的核准。 開啟相關聯的核准集記錄，找出失敗原因。
選取 **重試** 會增加核准集存留期計數、將核准集移回 **處理中** 狀態，並嘗試處理其餘的記錄。

## <a name="configure-approval-sets"></a>設定核准集

###  <a name="enable-the-approval-sets-feature"></a>啟用核准集功能
啟用核准集功能之前，請先確認目前沒有任何核准在處理中。

- 移至 **專案參數** 頁面，並選取 **功能控制** > **啟用現代化核准**。

### <a name="turn-off-the-approval-sets-feature"></a>關閉核准集功能
關閉核准集功能之前，請先確認目前沒有任何核准在處理中。

- 移至 **專案參數** 頁面，並選取 **功能控制** > **停用現代化核准**。

### <a name="configuring-the-asynchronous-threshold"></a>設定非同步閾值 
如果建立了核准集，當所選取待核准的記錄數目超過指示的閾值時，處理作業就會移至背景。 使用 **非同步閾值** 欄位來設定何時應同步或非同步執行核准處理。
有效值為：

  - 零：所有要求都必須以非同步方式來處理。 
  - 大於零的數字：只有在提交核准的數目超過此值時，才會以非同步方式處理核准。

[!INCLUDE[footer-include](../includes/footer-banner.md)]