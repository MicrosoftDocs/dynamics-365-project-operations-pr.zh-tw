---
title: 產品型報價明細
description: 此主題提供有關產品型報價明細的資訊。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 76b90c95-1b3a-4704-a13f-9d7099b83f4c
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d8bb36fbfe8d01aa26faf5515ca218ad836126b7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749895"
---
# <a name="product-based-quote-lines"></a>產品型報價明細

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


您可以在 Dynamics 365 Project Service Automation 中建立產品型報價明細。 產品型報價明細可以是「目錄外項目」明細，也可以是產品類別目錄中的項目。

## <a name="product-catalog"></a>產品類別目錄

Dynamics 365 產品類別目錄中的產品有預設單位與單位群組。 如果有數種產品共用同一組屬性，您可以建立同樣有這些屬性的產品系列。 一個產品系列中所有的產品都會繼承同一組屬性。

例如，公司銷售各種軟體的訂閱授權。 所有訂閱軟體都有下列兩個屬性：

- 使用者數目 
- 訂閱期間 (以月為單位)

維護這種目錄類型的好方法是建立名為**訂閱軟體**，且有**使用者數目**和**訂閱期間**做為屬性的產品系列。 然後，您可以將個別產品 (例如 **Dynamics 365 Sales** 或 **Dynamics 365 Field Service**) 新增至**訂閱軟體**產品系列。

## <a name="adding-product-catalog-items-to-a-project-quote"></a>將產品類別目錄專案新增至專案報價

專案報價與專案合約頁面有兩種類型的明細區段：專案型和產品型明細。 對於產品型明細，使用 Dynamics 365 將項目從產品類別目錄新增至報價。 報價明細或專案合約服務內容的下拉式清單，包含附加至報價或專案合約之產品價目表中的所有產品和單位。 您也可以新增不屬於報價之產品價目表的產品。

此外，您還可以從其他價目表選取產品，或者直接從產品類別目錄選取產品。 直接從產品類別目錄選取產品時，會使用該產品的預設價目表來取得產品的銷售價格。 如果未設定預設價目表，價格會設定為 0 (零)。

如果報價明細是根據產品類別目錄所建立，您可以直接在報價明細上覆寫銷售價格。 請注意，Dynamics 365 中的報價明細有**定價**欄位。 有兩個值可用：

- 自訂定價  
- 使用預設

如果將此欄位設定為**自訂定價**，Dynamics 365 就不會設定預設價格。 您必須在報價明細上輸入產品的價格。 如果將此欄位設定為**使用預設**，則 Dynamics 365 會使用預設銷售價格，並鎖定欄位以防編輯。

安裝 PSA 之後，會在報價的產品型明細上輸入預設銷售價格。 **定價**欄位會接著設定為**自訂定價**，因此您可以編輯報價明細上的預設價格。

> ![設定自訂定價](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>產品的數量因數

PSA 使用數量因素來支援以訂閱型產品的銷售。 對於訂閱型產品，報價或專案合約服務內容上的數量會以使用者的月數來表示。

訂閱軟體的價格通常在目錄中儲存為每個月每個使用者的價格。 但是，您可以改用其他時間描述。 在銷售處理期間，報價明細的價格通常是由 IT 銷售專員議定並打折扣的每個使用者、每個月的價格。 每筆交易都有不同的使用者數目和不同的訂閱月數。 用來計算報價明細金額的數量，是使用者人數與訂閱月數的乘積。

為了支援此類型的銷售，PSA 引進了數量因數的概念。 數量因數依賴 Dynamics 365 中的產品屬性。 當您設定產品的特定屬性時，PSA 可讓您將這些屬性子集或所有屬性標示為數量因數。

PSA 會驗證只有含有數值資料類型的數值屬性或產品屬性，才會標記為數量因數。 將設定數量因數的產品新增至報價明細時，報價明細上的**數量**欄位會變成唯讀欄位。 輸入數量因數的產品屬性值之後，PSA 會計算報價明細的數量。

例如，Dynamics 365 可能有下列屬性： 

- **使用者數** - 使用者的數目 
- **月數** - 訂閱的月期數
- **產品 SKU** 

您可以編輯產品明細的屬性，將**使用者數**和**月數**屬性標示為數量因數。 

> ![將 [使用者數] 和 [月數] 標示為品質因數](media/basic-guide-11.png)
 
