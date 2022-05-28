---
title: 確認專案廠商發票
description: 本主題說明如何在 Microsoft Dynamics 365 Project Operations 中確認專案廠商發票，以及確認專案廠商發票的財務影響。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595718"
---
# <a name="confirm-a-project-vendor-invoice"></a>確認專案廠商發票

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

在 Microsoft Dynamics 365 Project Operations 中驗證過廠商發票上所有的明細之後，您可以使用確認動作來確認廠商發票。

在廠商發票上選取 **確認** 時，會發生下列行為：

1. 廠商發票的狀態會更新為 **已確認**。
2. 確認的廠商發票及其相關的記錄會變成唯讀，無法加以編輯或刪除。
3. 如果有任何成本實際值在比對程序中參考廠商發票明細，則會沖回所有與參考廠商發票明細相關聯的成本實際值。
4. 系統會使用廠商發票明細上的資訊建立新的成本實際值。
5. 確認廠商發票之後，您無法再建立更正帳目、處理時間項目回收，也無法取消核准已沖回的原始時間、費用或材料實際值。

> [!NOTE]
> 如果廠商發票的任何明細有 **完成** 以外的驗證狀態，則無法確認此廠商發票。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
