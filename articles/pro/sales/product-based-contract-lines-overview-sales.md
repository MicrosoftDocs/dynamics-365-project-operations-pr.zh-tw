---
title: 產品型合約服務內容概觀 - 精簡
description: 此主題提供有關產品型合約服務內容的資訊。
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272648"
---
# <a name="product-based-contract-lines-overview---lite"></a>產品型合約服務內容概觀 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_

您可以在 Dynamics 365 Project Operations 中建立產品型合約服務內容。 產品型合約服務內容可以是手動建立的明細，也可以是產品類別目錄中的項目。

## <a name="product-catalog"></a>產品類別目錄

產品類別目錄中的產品有預設單位和單位群組。 如果有數種產品共用同一組屬性，您可以建立同樣有這些屬性的產品系列。 一個產品系列中所有的產品都會繼承同一組屬性。

例如，公司銷售各種不同軟體的訂閱授權。 所有訂閱軟體都有下列兩個屬性：

- 使用者數目
- 訂閱期間 (以月為單位)

若要維護此類型的目錄，請建立名為 **訂閱軟體** 的產品系列。 將 **使用者數目** 及 **訂閱期間** 屬性新增至產品系列。 然後，將個別產品新增至 **訂閱軟體** 產品系列。

## <a name="add-product-catalog-items-to-a-project-contract"></a>將產品類別目錄項目新增至專案合約

專案合約有兩種類型的明細區段，即專案型和產品型。 產品型明細包含合約中產品價目表的所有產品和單位。 您可以新增不屬於合約產品價目表的產品。

您可以從其他價目表選取產品，也可以直接從產品類別目錄選取產品。 直接從產品類別目錄選取產品時，該產品的預設價目表可用來取得產品的銷售價格。 如果未設定預設價目表，價格會設定為 0 (零)。

如果合約服務內容是根據產品類別目錄所建立，您可以直接在合約服務內容上覆寫銷售價格。 合約服務內容的 **定價** 欄位有兩個值：

- **自訂定價**
- **使用預設**

如果將 **定價** 欄位設定為 **自訂價格**，就不會設定預設價格。 輸入合約服務內容上的產品價格。 如果將此欄位設定為 **使用預設值**，則會使用預設銷售價，而且無法編輯欄位。

安裝 Project Operations 之後，合約的產品型明細上會輸入預設銷售價格。 **定價** 欄位會設定為 **自訂價格**，因此您可以編輯合約服務內容上的預設價格。 這是 Project Operations 覆寫 Dynamics 365 Sales 中產品型明細的特有行為。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]