---
title: 管理產品型合約服務內容的複雜單位 - 精簡
description: 本主題提供有關支援訂閱型產品銷售的資訊。
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86da5a96919438e883b56fc8ecfe765f70a789ff
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003171"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>管理產品型合約服務內容的複雜單位 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 使用數量因素來支援訂閱型產品的銷售。 對於訂閱型產品，合約或專案合約服務內容上的數量會以使用者月數來表示。

訂閱軟體的價格在目錄中儲存為每個月每個使用者的價格。 在銷售處理期間，合約服務內容的價格通常是由 IT 銷售專員所議定且給予折扣優惠的每個使用者、每個月的價格。 每筆交易都有不同的使用者數目和不同的訂閱月數。 用來計算合約服務內容金額的數量，是使用者人數與訂閱月數的乘積。

為了支援此類型的銷售，Project Operations 支援 *數量因數* 的概念。 數量因數依賴產品屬性。 設定產品的特定屬性時，您可以將這其中一部分屬性或所有屬性標示為數量因數。

Project Operations 會驗證是否只有含有數值資料類型的數值屬性或產品屬性，才會標記為數量因數。 將已設定數量因數的產品新增至合約服務內容時，**數量** 欄位會變成唯讀。 輸入數量因數的產品屬性值之後，Project Operations 會計算合約服務內容的數量。

例如，Dynamics 365 Sales 可能有下列屬性：

- **使用者數**：使用者的數目。
- **月數**：訂閱的月期數。
- **產品 SKU**：產品的庫存單位 (SKU)。

您可以編輯產品明細的屬性，將 **使用者數** 和 **月數** 屬性標示為數量因數。

若要從產品屬性建立數量因數，請完成下列步驟。

1. 在 **Project Operations** 中，選取 **銷售 - 產品**。
2. 開啟需要設定數量因數的產品。 確定已設定該產品的屬性。
3. 在 **專案資訊** 頁面上，選取 **數量因數** 索引標籤。
4. 在子格中，選取 **+ 新增欄位計算**。
5. 輸入 **數量因數** 的名稱，並選取對應至欄位計算的屬性值。
6. 儲存後關閉表單。
7. 針對所有共同構成產品型合約服務內容數量的屬性，重複步驟 2-6。

設定了數量因數後，當使用者建立此產品的合約服務內容時，就會鎖定合約服務內容的數量。 此數量接著會計算成該合約服務內容的屬性值乘積。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]