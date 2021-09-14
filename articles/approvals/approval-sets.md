---
title: 核准集
description: 本主題說明如何使用核准集、要求以及這些作業的子集。
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323226"
---
# <a name="approval-sets"></a>核准集

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

核准集會將核准要求集合成較小型作業子集的群組。 此群組功能允許由專案依特定順序處理核准，並允許重試和排序。 將核准要求群組在一起，可改善大量核准處理工作的可靠性和可追蹤性。

核准集表示其相關記錄的整體處理狀態。 使用核准集處理核准記錄時，該記錄會從 **已提交** 移為 **已核准**，並且不再與核准集連結。 如果記錄在提交供核准時失敗，則記錄仍會保持在 **已提交** 狀態，而核准集會標示為失敗。 核准集會記錄失敗的錯誤訊息。

## <a name="processing-approvals-and-approval-sets"></a>處理核准和核准集
已排入佇列等待處理的核准會顯示在 **處理核准** 檢視表中。 系統會以非同步方式多次處理所有的項目，包括重試核准 (如果先前的嘗試失敗的話)。

**核准集存留期** 欄位會記錄將此集合標示為失敗前，剩餘的嘗試處理次數。

## <a name="failed-approvals-and-approval-sets"></a>失敗的核准和核准集
**失敗的核准** 檢視表會列出所有需要使用者操作的核准。 開啟相關聯的核准集記錄，找出失敗原因。
選取 **重試** 會增加核准集存留期計數、將核准集移回 **處理中** 狀態，並嘗試處理其餘的記錄。

## <a name="configure-approval-sets"></a>設定核准集

### <a name="enable-the-approval-sets-feature"></a>啟用核准集功能
啟用核准集功能之前，請先確認目前沒有任何核准在處理中。

- 移至 **專案參數** 頁面，並選取 **功能控制** > **啟用現代化核准**。

### <a name="turn-off-the-approval-sets-feature"></a>關閉核准集功能
關閉核准集功能之前，請先確認目前沒有任何核准在處理中。

- 移至 **專案參數** 頁面，並選取 **功能控制** > **停用現代化核准**。

### <a name="configuring-the-asynchronous-threshold"></a>設定非同步閾值 
如果建立了核准集，當所選取待核准的記錄數目超過指示的閾值時，處理作業就會移至背景。 使用 **非同步閾值** 欄位來設定何時應同步或非同步執行核准處理。 選取下列其中一個值：

  - 零：所有要求都必須以非同步方式來處理。 
  - 大於零的數字：只有在提交核准的數目超過此值時，才會以非同步方式處理核准。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
