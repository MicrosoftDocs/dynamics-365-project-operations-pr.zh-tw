---
title: 資源估計值
description: 本主題提供有關如何在 Project Operations 中計算資源估計值的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286508"
---
# <a name="resource-estimates"></a>資源估計值

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

資源估計值來自分工結構圖中定義的分時期投入量以及適用的定價維度。 計算方式通常是 **每個角色的每小時費率 x 時數**。 每個資源的分時期投入量都會儲存在資源指派記錄中。 定價會儲存在預先定義的價目表中。 單位轉換是根據適用的價目表來套用。

![資源估計值](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>預設成本價與成本貨幣

成本價預設會使用組織單位。

## <a name="default-bill-rate-and-sales-currency"></a>預設帳單費率與銷售貨幣

每筆交易會套用售價一次。 銷售價目表的階層預設如下：

1. 組織
2. 客戶
3. 報價/合約


[!INCLUDE[footer-include](../includes/footer-banner.md)]