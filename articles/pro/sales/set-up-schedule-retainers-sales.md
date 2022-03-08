---
title: 設定保留款排程
description: 此主題提供如何在 Project Operations 中設定保留款排程的資訊。
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a1cfd83837a91a8d1b3db6df688da6e216a90ada4735e5909a7e8cb26b87247d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994356"
---
# <a name="set-up-a-retainer-schedule"></a>設定保留款排程

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

在 Dynamics 365 Project Operations 的 **專案合約** 頁面上設定保留款排程。

1. 在 **專案合約** 頁面的 **預付款和保留款** 索引標籤中，選取 **設定保留款排程**。
2. 在開啟的對話方塊頁面上，會顯示下表列出的欄位。 下表給出了所輸入的值如何影響將建立的保留款排程的想法。

| 欄位 | 描述 | 下游影響 |
| --- | --- | --- |
| 專案合約客戶 | 要為合約上的哪個客戶開立此保留款或預付金的發票。 | 如果合約上有多個客戶，而您想要為其中每一個客戶開立特定保留款或預付款金額的發票時，請為每個客戶手動建立一個發票。 |
| 保留款排程開始 | 輸入保留款排程的開始日期。 | 此日期可能不是建立第一個保留款或預付金的日期。 建立第一個保留款或預付金的日期也會受到發票頻率的影響。 |
| 保留款排程結束 | 輸入保留款排程的結束日期。 | 此日期可能不是建立最後一個保留款或預付金的日期。 建立最後一個保留款或預付金的日期也會受到發票頻率的影響。 |
| 要建立的保留款數目 | 當您輸入要建立的保留款數目時，系統會使用開始日期和頻率來建立此欄位中的數目。 | 手動更新此欄位時，系統會忽略 **保留款排程結束** 欄位中的值，而是建立特定數目的保留款或預付款。 |
| 發票頻率 | 應用程式建立保留款和預付款的頻率。 | 此值會直接影響保留款和預付款的數目，以及建立的日期。 |
| 總金額 | 總計金額是指分割成要建立的各個保留款或預付款的金額。 | 此欄位沒有任何下游影響。 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]