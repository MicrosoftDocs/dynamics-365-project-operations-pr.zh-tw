---
title: 管理產品型報價明細的複雜單位，例如按使用者、按月為單位 - 精簡
description: 本主題提供有關管理產品型報價明細複雜單位的資訊。
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 78bdb64d901cf68ce02c168987c2386e1416f6ee
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994756"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>管理產品型報價明細的複雜單位，例如按使用者、按月為單位 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 使用數量因素來支援訂閱型產品的銷售。 對於訂閱型產品，報價或專案合約服務內容上的數量會以使用者的月數來表示。

訂閱軟體的價格通常在目錄中儲存為每個月每個使用者的價格。 在銷售處理期間，報價明細的價格通常是由 IT 銷售專員議定並打折扣的每個使用者、每個月的價格。 每筆交易都有不同的使用者數目和不同的訂閱月數。 用來計算報價明細的數量，是使用者人數與訂閱月數的乘積。

為了支援此類型的銷售，Project Operations 引進了數量因數的概念。 數量因數依賴 Dynamics 365 中的產品屬性。 設定產品的特定屬性時，Project Operations 可讓您將這些屬性子集或所有屬性標記為數量因數。

Project Operations 會驗證是否只有含有數值資料類型的數值屬性或產品屬性，才會標記為數量因數。 當您將含有數量因數的產品新增至報價明細時，**數量** 欄位會變成唯讀。 輸入數量因數的產品屬性值之後，Project Operations 會計算報價明細的數量。

例如，Dynamics 365 Sales 可能有下列屬性：

- **使用者數**：使用者的數目
- **月數**：訂閱的月期數
- **產品 SKU**

您可以編輯產品明細的屬性，將 **使用者數** 和 **月數** 屬性標記為數量因數。

若要從產品屬性建立數量因數，請依照下列步驟進行：

1. 在 Project Operations 左導覽窗格上，移至 **銷售** > **產品**。
2. 開啟需要設定數量因數的產品。 確定已設定產品的屬性。
3. 在產品的 **專案資訊** 頁面上，選取 **數量因數** 索引標籤。
4. 在子格中，選取 **+ 新增欄位計算**。
5. 輸入數量因數的名稱，並選取對應至欄位計算的屬性值。
6. 儲存後關閉表單。 針對所有要用於計算產品型報價明細數量的屬性，重複這些步驟。

建立產品的產品型報價明細時，會鎖定報價明細的數量。 計算所得數量會是您針對該報價明細所輸入各個屬性值的乘積。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]