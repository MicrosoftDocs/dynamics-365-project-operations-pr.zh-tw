---
title: 設定貨幣轉換以根據成本費率計算銷售價
description: 本文說明如何設定從成本交易記錄產生銷售交易時，Microsoft Dynamics 365 Project Operations 中使用的貨幣轉換行為。
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816660"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>設定貨幣轉換以根據成本費率計算銷售價

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

在 Microsoft Dynamics 365 Project Operations 中，可以將費用類別的銷售價設定為數值，也可以將其設定為根據產生的成本來計算。

設定為根據產生的成本進行計算時，有下列選項可用：

- 依照成本
- 成本加成百分比

在費用成本是以不同於專案合約銷售貨幣的貨幣所產生的案例中，必須進行貨幣轉換，才能根據成本計算銷售價。

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>使用原生 Dataverse 匯率的貨幣轉換行為

Project Operations 預設會使用 Dataverse 的貨幣資料表中所儲存的貨幣匯率。 若要將 Project Operations 設定為使用原生匯率來計算成本的銷售價，請執行下列步驟。

1. 移至 **Project Operations \> 設定 \> 參數**。
1. 開啟 **專案參數** 詳細資料頁面。
1. 將 **貨幣轉換邏輯** 欄位設定為空白值。

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>使用財務和營運應用程式中匯率的貨幣轉換行為

Dataverse 本身既有貨幣資料表中的匯率並非即日有效的匯率。 因此，不一定符合您對根據成本費率計算銷售價的需求。

您可以使用財務和營運環境中的匯率，根據以成本貨幣計價的成本費率來計算以銷售貨幣計價的銷售價。 若要設定此貨幣轉換行為，請執行下列步驟。

1. 在 **專案參數** 頁面上，新增 **貨幣轉換邏輯** 欄位。 接著儲存並發佈自訂。
1. 移至 **Project Operations \> 設定 \> 參數**。
1. 開啟 **專案參數** 詳細資料頁面。 
1. 將 **貨幣轉換行為** 欄位設定為 **透過回退至預設值進行擴展**。
1. 將 **雙重寫入應用程式使用者** 資訊安全角色 **全域讀取** 權限提供給下列資料表：

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. 在財務和營運環境中，執行下列雙重寫入對應，並進行初始同步處理：

    - 匯率類型 (msdyn\_exchangeratetypes)
    - 匯率貨幣對 (msdyn\_currencyexchangeratepairs)
    - CDS 匯率 (msdyn\_currencyexchangerates)

完成這些變更之後，雙重寫入會從 Dataverse 提供的財務和運營環境中建立匯率。 Project Operations 接著使用這些匯率將成本率轉換成合約的銷售貨幣。

> [!NOTE]
> 此貨幣換算行為僅適用於根據成本費率的銷售價計算。 這不會用於進行基準貨幣值的一般計算。 不論您是否完成此程序，基準貨幣一律使用原生 Dataverse 匯率。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
