---
title: 產品型報價明細概觀 - 精簡
description: 本主題提供有關使用產品型報價明細的資訊。
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272558"
---
# <a name="product-based-quote-lines-overview---lite"></a>產品型報價明細概觀 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_

您可以在 Dynamics 365 Project Operations 中建立產品型報價明細。 產品型報價明細可以手動新增，也可以是產品類別目錄中的項目。

## <a name="product-catalog"></a>產品類別目錄

產品類別目錄中的每個產品都有預設單位與單位群組。 如果有數種產品共用同一組屬性，您可以建立共用這些屬性的產品系列。 

例如，公司銷售各種不同軟體的訂閱授權。 所有訂閱軟體都有下列兩個屬性：

- 使用者數目
- 訂閱期間 (以月為單位)

若要維護這種目錄類型，請建立名為 **訂閱軟體** 的產品系列，並新增使用者數目和訂閱期間做為屬性。 接下來，您可以將個別產品新增至 **訂閱軟體** 產品系列。

## <a name="add-product-catalog-items-to-a-project-quote"></a>將產品類別目錄專案新增至專案報價

**專案報價** 與 **專案合約** 頁面有專案型和產品型明細的區段。 對於產品型明細，報價明細或專案合約服務內容的下拉式清單產品價目表中的所有產品和單位。 您也可以新增不屬於產品價目表的產品。

此外，您還可以從其他價目表或者直接從產品類別目錄選取產品。 直接從產品類別目錄選取產品時，會使用該產品的預設價目表來取得產品的銷售價格。 如果未設定預設價目表，價格會設定為零 (0)。

當報價明細是根據產品類別目錄所建立，您可以直接在報價明細上覆寫銷售價格。 **定價** 欄位中的報價明細有兩個可用值：

- **覆寫定價**
- **預設價格**

如果您選取 **覆寫定價**，將不會設定預設價格。 反之，您必須在報價明細上輸入產品的價格。 如果您選取 **使用預設值**，則會使用預設售價，而且欄位會鎖定無法編輯。

在報價的產品型明細上輸入預設售價。 **定價** 欄位會接著設定為 **覆寫定價**，因此您可以編輯報價明細上的預設價格。 這是 Dynamics 365 Sales 中，針對產品型明細行為的 Project Operations 特有覆寫功能。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]