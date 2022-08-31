---
title: 取消專案廠商發票
description: 本文說明如何在 Microsoft Dynamics 365 Project Operations 中取消專案廠商發票，以及取消專案廠商發票的財務影響。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261080"
---
# <a name="cancel-a-project-vendor-invoice"></a>取消專案廠商發票

_**適用於：** 精簡部署 - 交易至開立預估發票_

確認廠商發票之後，無法對其進行編輯或刪除。 如果已確認的廠商發票發生錯誤，您可以使用取消動作來沖回廠商發票的影響，並建立新的廠商發票。

在廠商發票上選取 **取消** 時，會發生下列行為：

1. 廠商發票的狀態會更新為 **已取消**。
2. 取消的廠商發票及其相關的記錄會變成唯讀，無法加以編輯或刪除。
3. 任何在廠商發票確認過程中根據廠商發票明細建立的成本實際值都會進行沖回。
4. 如果比對過程中有任何成本實際值已連結至廠商發票明細，則原始廠商發票確認已將這些值沖回。 廠商發票取消期間會重新建立這些成本實際值。 來源會指向時間、費用或材料使用項目。
5. 取消廠商發票之後，您可以再一次建立更正帳目、處理時間項目回收以及取消原始時間、費用或材料實際值的核准。

> [!NOTE]
> 只能取消已確認的專案廠商發票。 無法取消其他狀態的廠商發票。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
