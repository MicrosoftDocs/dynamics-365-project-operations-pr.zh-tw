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
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127340"
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
