---
title: 估計專案報價明細
description: 本主題提供有關如何在專案報價明細上建立估計值的資訊。
author: rumant
manager: Annbe
ms.date: 04/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b941511f842a81764ddd1c05a437578b9fd902ce
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858778"
---
# <a name="estimate-a-project-quote-line"></a>估計專案報價明細

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

專案型報價明細的詳細資料可協助您估計提供報價明細所需工作的成本和可能營收。

若要估計專案報價明細，請選取報價明細上的 **報價明細詳細資料** 索引標籤。其中有兩種可在專案型報價上建立估計值的方法：

   - 使用報價明細詳細資料，直接在報價明細上手動建立估計值。 
   - 建立專案和專案計劃，然後將專案以及專案上的工作關聯至報價明細。 將會啟用根據您所提供資訊將專案計劃中估計值匯入至報價明細的程序。

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>直接在專案型報價明細上建立估計值

若要直接在專案型報價明細上建立估計值，請依照下列步驟進行：

1. 若要在專案型報價明細建立估計值，請選取 **報價明細詳細資料** 索引標籤。您在此索引標籤上建立的明細項目將會摘要列出此報價明細的報價值。 
2. 若要建立報價明細詳細資料，請選取 **報價明細詳細資料** 子格上的 **新增報價明細詳細資料**。 將會開啟快速建立滑桿。 下列在 **報價明細** 頁面中的欄位。

| **欄位** | **地點** | **描述** | **下游影響** |
| --- | --- | --- | --- |
| 描述 | 快速建立 | 特定估計值的描述。 | 此值預設為自動建立的成本相關報價明細詳細資料。 |
| 交易類別 | 快速建立 | 此下拉式清單提供專案型報價明細的 **一般** 索引標籤中所包含的交易類別。  | 此值預設為自動建立的成本相關報價明細詳細資料。 |
| 選取產品 | 快速建立 | 在交易分類為 **材料** 時套用。 您可以選取來指定適用此估計明細的是 **現有** (目錄) 產品還是 **目錄外** 產品。 | 此值預設為自動建立的成本相關報價明細詳細資料。 |
| 產品 | 快速建立 | 產品類別目錄中的產品識別碼。 只有在您選擇 **選取產品** 欄位中的 **現有** 時，才會啟用此欄位。 識別碼會用於從報價的專案價目表中擷取銷售價。 | 此值預設為自動建立的成本相關報價明細詳細資料。 |
| 目錄外產品 | 快速建立 | 要寫入目錄外產品名稱的文字方塊。 只有在您選擇 **選取產品** 欄位中的 **目錄外** 時，才會啟用此欄位。| 此值預設為自動建立的成本相關報價明細詳細資料。 |
| 角色 | 快速建立 | 執行此工作或產生此費用的人員角色。 | 此值預設為自動建立的成本相關報價明細詳細資料。 |
| 類別 | 快速建立 | 工作或費用的類別。 | 此值預設為自動建立的成本相關報價明細詳細資料。 |
| 開始日期 | 快速建立 | 工作的開始日期。 | 此欄位預設為自動建立的成本報價明細詳細資料。 |
| 結束日期 | 快速建立 | 工作的結束日期。 | 此欄位預設為自動建立的成本報價明細詳細資料。 |
| 資源供應公司 | 快速建立 | 承擔此成本且提供資源加以處理的資源供應公司或法律實體。 | 此值預設為自動建立的成本相關報價明細詳細資料，並且用於擷取成本價。 |
| 資源分配單位 | 快速建立 | 承擔此成本且提供資源加以處理的資源分配單位。 | 此值預設為自動建立的成本相關報價明細詳細資料，並且用於擷取成本價。 |
| 單位排程 | 快速建立 | 工作、產品或費用的單位群組。 屬於單位排程或單位群組的單位。 例如，英里和公里是屬於描述距離之單位群組的單位。 | 此值預設為自動建立的成本相關報價明細詳細資料。 |
| 單位 | 快速建立 | 工作、產品或費用的單位。 | 此值預設為自動建立的成本相關報價明細詳細資料。 |
| 數量 | 快速建立 | 工作、產品或費用的數量。 | 此值預設為自動建立的成本相關報價明細詳細資料。 |
| 單價 | 快速建立 |執行工作的角色帳單費率、產品的單價或是產品或費用類別的銷售價。 **時間** 的預設值是根據在開始日期有效之專案價目表中角色價格明細的定價維度值組合而定。 對於 **費用**，預設值是根據在開始日期有效之專案價目表中交易類別的價格設定而定。 如果交易類別的定價方式不是單價，就沒有預設值，且此欄位保留空白。 對於產品，此欄位的預設值是根據在開始日期有效之專案價目表中的 **價目表項目** 明細而定。| 執行工作的角色成本費率、費用類別的單位成本或產品的單位成本。 **時間** 的預設值是根據在開始日期有效且已附加至合約單位之成本價目表中角色價格明細的定價維度值組合而定。 對於費用，預設值是根據在開始日期有效且已附加至合約單位之成本價目表的類別價格明細而定。 如果交易類別的定價方式不是單價，則沒有預設值，且此欄位保留空白。 對於產品，此欄位的預設值是根據在開始日期有效且已附加至合約單位之成本價目表的 **價目表項目** 明細而定。|
| 估計稅額 | 快速建立 | 您可以手動輸入此工作或費用的估計稅金。 | 此欄位沒有任何下游影響。 |
| 總數 | 快速建立 | 如果 **數量** 和 **價格** 欄位保留空白，您可以在此欄位中手動輸入資訊。 如果這些欄位不是空白，則此欄位會變成唯讀，並且會依 (數量 \* 單價) + 稅金的方式進行計算。 | 此欄位沒有任何下游影響。 |

## <a name="update-prices-on-quote-line-details"></a>更新報價明細詳細資料的價格

如果您已變更在附加至報價之專案價目表或在合約單位之成本價目表上的價格，則可以選取 **報價** 頁面上的 **重新計算**，重新整理個別報價明細詳細資料上的價格，以反映此變更。 選取 **重新計算** 時，警告會出現，通知您此報價的所有報價明細都會重設報價明細詳細資料上的價格。 選取 **是**，以重新整理銷售及成本報價明細詳細資料的價格。

## <a name="access-quote-line-details-for-cost"></a>存取成本的報價明細詳細資料

若要存取成本的報價明細詳細資料，請依照下列步驟進行：

1. 在 **報價明細詳細資料** 索引標籤中，選取網格中的一列，以啟用子格工具列上的動作。 
2. 選取 **開啟成本詳細資料**，以查看此報價明細的相關成本費率及金額。

> [!NOTE]
> 在成本報價明細詳細資料中變更資源分配單位、數量、日期、角色或類別值，將會變更銷售報價明細詳細資料中對應的值。

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>成本及銷售報價明細詳細資料上的貨幣

銷售報價明細詳細資料的貨幣，是根據在報價明細詳細資料開始日期有效的專案價目表來設定預設值。

成本報價明細詳細資料的貨幣，是根據在成本報價明細詳細資料開始日期有效的報價合約單位價目表來設定預設值。

> [!NOTE]
> 獲利率計算會將成本及銷售報價明細詳細資料上的金額轉換成環境的基準貨幣，以報告報價的整體估計利潤。 貨幣捨入錯誤和變動利潤可能會因為缺少即日有效的匯率而發生。 這些計算只能用於專案報價，因為這些計算只是近似值，並不適用於在匯率上需要較多捨入有效位數且必須有更高日期時效性意識的實際法定報告或其他申報。


[!INCLUDE[footer-include](../includes/footer-banner.md)]