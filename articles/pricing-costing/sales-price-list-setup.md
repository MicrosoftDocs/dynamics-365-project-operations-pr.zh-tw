---
title: 設定銷售價目表
description: 本主題提供有關專案定價銷售價目表的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176241"
---
# <a name="set-up-a-sales-price-list"></a>設定銷售價目表

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

對於專案報價和合約，專案價目表的價格覆寫模式與產品價目表的不同。 在產品類別目錄型報價明細上，您可以直接在報價明細上覆寫角色和類別的價格，因為每個報價明細都只指向一個目錄項目。 不過，在專案型報價明細上，您無法直接在報價明細上覆寫角色和類別的價格。 您可以使用專案價目表來處理兩種不同的覆寫模式。

> [!NOTE]
> 建議您讓專案資源和目錄項目使用不同的價目表，因為覆寫定價時，兩者之間的行為有差異。

下列每個實體都可以有一個或多個用於專案定價的相關聯銷售價目表：

- 客戶 (帳戶) 
- 商機 
- 報價 
- 專案合約

這些實體與價目表的關聯是透過專案價目表來表示。 您可以將一個或多個價目表與客戶、商機、報價及專案合約銷售實體建立關聯。

系統不會自動在客戶記錄上輸入預設專案價目表。 不過，您可以手動將專案價目表附加至客戶記錄。 然而，只有在與客戶之間存在自訂定價合約時，您才應該手動附加專案價目表。 

將專案價目表附加至銷售實體時，系統會驗證下列資訊：

- 價目表的內容與 **銷售** 有關。 
- 價目表貨幣與客戶貨幣相符。 

在專案合約上，使用下列優先順序自動設定相關的專案價目表：

1. 報價
2. 商機​​
3. 客戶 
4. 全域設定 

預設會輸入專案價目表時，系統會驗證貨幣是否與客戶貨幣相符，以及所輸入預設價目表的內容是否與 **銷售** 有關。

您可以將或多個專案價目表與客戶、商機、報價及專案合約銷售實體建立關聯。 此功能支援長期專案合約的日期特定預設價格，您可能需要多個價目表來處理因通貨膨脹而進行的價格更新。 不過，如果與客戶、商機、報價或專案合約實體建立關聯的價目表有重疊的有效日期範圍，則預設價格可能不正確。 因此，您必須確保有效日期範圍重疊的專案價目表未與這些實體相關聯。


[!INCLUDE[footer-include](../includes/footer-banner.md)]