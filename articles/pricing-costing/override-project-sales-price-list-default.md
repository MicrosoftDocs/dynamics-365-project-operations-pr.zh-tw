---
title: 覆寫專案銷售價目表
description: 此主題提供建立自訂銷售價目表的相關資訊。
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672221"
---
# <a name="override-project-sales-price-lists"></a>覆寫專案銷售價目表

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

## <a name="customer-specific-project-price-lists"></a>客戶特定的專案價目表

客戶特定的價格合約可以設定為 Dynamics 365 Project Operations 中客戶記錄上的專案價目表。

若要設定客戶特定的專案價目表，請在 **銷售** 區域中瀏覽至客戶記錄。

1. 開啟 **帳戶** 清單頁面。
2. 找到並按兩下客戶記錄以開啟 **帳戶** 詳細資料頁面。
3. 在 **專案價目表** 索引標籤上，選擇 **+ 新增專案價目表**。
4. 在 **新的專案價目表** 頁面上，從下拉清單中選擇價目表。 只會包含內容已設定為 **銷售** 且其貨幣符合帳戶貨幣的價目表。
5. 命名關聯，然後選取 **儲存**。 隨即建立客戶特定的專案價目表。 如果報價或專案合同的建立日期落在價目表的有效期內，則此價目表將用於為此客戶建立的專案報價或合約的預設專案價格。

## <a name="custom-pricing-on-project-quotes"></a>專案報價的自訂定價

在專案報價中，您可以有以預設標準價目表開頭的專案定價，該價目表預設為客戶或專案參數的預設值。

當您需要針對特定報價進行與專案相關工作的自訂定價時，可以從專案價目表關聯實體獲取。

完成以下步驟以設定報價特定的專案定價。

1. 開啟專案報價並選擇 **專案價目表** 索引標籤。
2. 在子格中，選取 **建立自訂定價**。

附加到報價的所有專案價目表都會複製到新的價目表。 新價目表的名稱會反映報價的名稱，並具有建立這些價目表的日期時間戳記。

您可以使用每個價目表，並更新人力 (角色價格) 和費用 (類別價格) 價格。 這些價格僅適用於此專案報價。

## <a name="price-lists-on-a-project-contract"></a>專案合約上的專案清單

在專案合約中，專案定價始終預設為自訂價目表，其中附有合約名稱和附加到名稱的建立日期時間戳記。 無論合約是在贏得報價時建立的，還是從零開始建立合約，都是如此。 如果需要，您可以移除與自訂價目表的此關聯，並將標準價目表關聯至專案合約。

當您將標準價目表與報價或合約上的專案價目表關聯時，對價目表中的價格所做的任何變更都將影響使用價目表的所有報價和合約。


[!INCLUDE[footer-include](../includes/footer-banner.md)]