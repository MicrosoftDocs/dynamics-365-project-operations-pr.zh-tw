---
title: 計算產品型報價明細的成本
description: 本主題提供有關將成本價套用至產品型報價明細的資訊。
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003441"
---
# <a name="costing-product-based-quote-lines"></a>計算產品型報價明細的成本

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_


Dynamics 365 Project Operations 中的產品型報價明細也有 **成本價** 欄位。 此欄位會用來追蹤報價明細上的產品成本價，並用於進行下游續獲利率計算。

建立產品類別目錄產品的產品型報價明細時，產品型報價明細的成本預設會使用產品類別目錄中的 **標準成本** 欄位。 產品類別目錄中的標準成本欄位是以組織的基準貨幣來設定。 產品型報價明細上的預設單位成本會轉換為報價上的銷售貨幣。

## <a name="unit-cost-on-a-product-based-quote-line"></a>產品型報價明細的單位成本

產品型報價明細上設有單位成本的目的是為了讓每次銷售的產品各有不同的成本。 這不是常見的案例，但是產品的成本有時可能會由供應商視最終銷售的客戶而定打折扣。

例如：

Fabrikam Robotics 正在 A Datum Corporation 的裝配線上安裝機器人手臂。 Fabrikam 提供安裝服務，但機器人手臂是從 Trey Robotics 取得。 如果在 A Datum Corporation 安裝機器人手臂會為 Trey 的機器人手臂開拓新市場，Trey 可能會向 Fabrikam 提供這筆交易的特殊折扣。

在此情況下，Fabrikam 會為機器人手臂建立產品型報價明細，並為此報價輸入每單位成本的特價優惠。 這項成本與 Trey 機器人手臂的標準成本不同。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]