---
title: 確認專案廠商發票
description: 本文說明如何在 Microsoft Dynamics 365 Project Operations 中確認專案廠商發票，並敘述確認專案廠商發票的財務影響。
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475415"
---
# <a name="confirm-project-vendor-invoices"></a>確認專案廠商發票

**適用於：** 資源/非庫存型案例適用的 Project Operations

**需要專案經理手動確認** 參數已啟用時，Microsoft Dataverse 中所建立的廠商發票會有 **草稿** 狀態。 以這種方式建立的廠商發票必須經過審查和手動確認。 **需要專案經理手動確認** 參數已停用時，會自動確認 Dataverse 中所建立的廠商發票。 不需要進一步的動作。 

在 Dynamics 365 Project Operations 中驗證過廠商發票上所有的明細之後，選取 **確認** 以確認廠商發票。

在廠商發票上選取 **確認** 時，會發生下列行為：

1. 廠商發票的狀態會更新為 **已確認**。
1. 確認的廠商發票及其相關的記錄會變成唯讀，無法加以編輯或刪除。
1. 如果有任何成本實際值在比對程序中參考廠商發票明細，則會沖回所有與參考廠商發票明細相關聯的成本實際值。
1. 系統會使用廠商發票明細上的資訊建立新的成本實際值。
1. 您無法再建立更正帳目、處理時間項目回收，也無法取消核准已沖回的原始時間、費用或材料實際值。
1. 在 Dynamics 365 Finance 中，**專案成本** 值是使用專案整合帳目來更新，而且採購整合科目會在專案整合帳目過帳後 *沖回*。

> [!NOTE]
> 如果廠商發票的任何明細有 **完成** 以外的驗證狀態，則無法確認此廠商發票。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
