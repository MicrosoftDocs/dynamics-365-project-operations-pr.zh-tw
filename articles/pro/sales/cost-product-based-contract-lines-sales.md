---
title: 計算產品型合約服務內容的成本 - 精簡
description: 本主題提供有關建立產品型合約服務內容的資訊
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003531"
---
# <a name="cost-product-based-contract-lines---lite"></a>計算產品型合約服務內容的成本 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_


Dynamics 365 Project Operations 中的產品型合約服務內容包含 **成本價** 欄位，其中儲存用於計算下游獲利率的產品成本價。

建立目錄產品的產品型合約服務內容時，該合約服務內容的成本預設是源自產品目錄中的 **標準成本** 欄位。 產品類別目錄中的 **標準成本** 欄位是以組織的基準貨幣來設定。 合約服務內容預設使用單位成本時，此成本會轉換為合約上的銷售貨幣。

## <a name="unit-cost-on-a-product-based-contract-line"></a>產品型合約服務內容的單位成本

產品型合約服務內容上設有單位成本，可讓每個銷售單位各有不同的產品成本。 雖然不一定需要，但還是存在供應商可能給予客戶產品成本折扣的特定案例。 試想以下情況：

Fabrikam Robotics 正在 Adatum Corporation 的裝配線上安裝機器人手臂。 Fabrikam 提供安裝服務，但機器人手臂是來自 Trey Research。 如果在 Adatum Corporation 安裝機器人手臂會為 Trey Research 的機器人手臂開拓新市場，他們就可能會向 Fabrikam 提供這筆交易的特殊折扣。 在此案例中，Fabrikam 會為機器人手臂建立產品型合約服務內容。 此合約的單位成本已輸入。 此成本與 Trey Research 的機器人手臂成本不同。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]