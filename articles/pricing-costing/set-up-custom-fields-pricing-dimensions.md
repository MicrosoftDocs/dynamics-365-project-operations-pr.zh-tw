---
title: 將自訂欄位設定為定價維度
description: 本主題提供有關如何使用自訂欄位進行定價維度設定的資訊。
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 67e891d8576cd92f48466929fc53fe8a4203d72d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119408"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>將自訂欄位設定為定價維度

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

開始之前，本主題假設您已完成[建立自訂欄位和實體](create-custom-fields-entities-pricing-dimensions.md)以及[將必要的自訂欄位新增至價格設定與交易實體](add-custom-fields-price-setup-transactional-entities.md)主題中的程序。 如果您尚未完成這些程序，請返回並加以完，然後再回到本主題。 

本主題提供有關設定自訂定價維度的資訊。 在 **參數** 頁面上，**以金額為準的定價維度** 索引標籤會顯示定價維度實體中的記錄。 此索引標籤中的網格預設會有兩列：

- **msdyn_resourcecategory** (角色)
- **msdyn_OrganizationalUnit** (組織單位)

> [!IMPORTANT]
> 請勿刪除這些列。 不過，如果您不需要這些列，則可以將 **適用於成本**、**適用於銷售** 和 **適用於購買** 都設定為 **否**，將其設定為不適用於特定內容。 將這些屬性值設定為 **否**，效果如同未將欄位設定為定價維度。

若要讓欄位變成定價維度，該欄位必須：

- 建立為 **角色價格** 和 **角色價格加成** 實體中的欄位。 如需執行此動作的詳細資訊，請參[將自訂欄位新增至價格設定與交易實體](add-custom-fields-price-setup-transactional-entities.md)。
- 建立為 **定價維度** 表格中的一列。 例如，新增如下圖形所示的定價維度列。 

資源工作時數 (**msdyn_resourceworkhours**) 已新增為以加成為準的定價維度，並已新增至 **以加成為準的定價維度** 索引標籤上的網格。

> [!IMPORTANT]
> 任何對此表格中定價維度資料 (現有或新增) 的變更，只有在重新整理快取之後，才會傳播至定價商務規則。 快取重新整理時間可能需要長達 10 分鐘。 請等待這段時間過後，再查看必須從定價維度資料變更產生之價格預設邏輯中的變更。


## <a name="attributes-of-the-pricing-dimensions-table"></a>定價維度表格的屬性
以下各節提供有關 **定價維度** 表格中不同屬性的資訊。

### <a name="pricing-dimension-name"></a>定價維度名稱
此值應與新增至自訂定價維度之 **角色價格** 表格中的欄位結構描述名稱相同。 如需有關將欄位新增至 **角色價格** 表格的詳細資訊，請參閱[將自訂欄位新增至價格設定與交易實體](add-custom-fields-price-setup-transactional-entities.md)。

### <a name="type-of-dimension"></a>維度的類型
定維度有兩種類型：
  
  - **以金額為準的維度**：輸入內容中的維度值會與 **角色價格** 明細上的維度值相符合，而且直接由 **角色價格** 表格預設價格/成本。
  - **以加成為準的維度**：這些維度是使用下列三步驟程序取得價格/成本的維度。
 
    1. 來自輸入內容的非以加成為準的維度值會與角色價格明細進行比對以取得基準費率。
    2. 來自輸入內容的維度值會與 **角色價格加成** 明細進行比對以取得加成百分比。
    3. 第二個步驟產生的加成百分比會套用至第一個步驟從 **角色價格** 表格所取得的基準費率，以決定最終價格/成本。
   
   下表說明價格加成的計算。
  
| 角色        | 組織單位    |工作地點      |標準職稱      |資源工作時數      |  加成|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|現場            |                    |加班時間                 |15     |
|             | Contoso India|本機             |                    |加班時間                 |10     |
|             | Contoso US   |本機             |                    |加班時間                 |20     |


如果來自 Contoso India、基準費率為 100 美元的資源在現場工作，而他們在時間項目上記入了 8 小時正常工時與 2 小時加班工時，此定價引擎將會使用 8 小時的基準費率 100，將 800 美元列入記錄。 至於 2 小時加班工時，則將 15% 的加成套用至基準費率 100 以取得 115 美元的單價，並記錄 230 美元的總成本。

### <a name="applicable-to-cost"></a>適用於成本 
如果此選項設定為 **是**，即表示擷取成本及加成費率時，應使用來自輸入內容的維度值，與 **角色價格** 和 **角色價格加成** 進行比對。

### <a name="applicable-to-sales"></a>適用於銷售
如果此選項設定為 **是**，即表示擷取帳單及加成費率時，應使用來自輸入內容的維度值，與 **角色價格** 和 **角色價格加成** 進行比對。

### <a name="applicable-to-purchase"></a>適用於購買
如果此選項設定為 **是**，即表示擷取購買價時，應使用來自輸入內容的維度值，與 **角色價格** 和 **角色價格加成** 進行比對。 不支援轉承包案例，因此不使用此欄位。 

### <a name="priority"></a>優先順序
設定維度優先順序有助於定價，即使在輸入維度值與 **角色價格** 或 **角色價格加成** 表格中的值之間找不到完全相符的項目時，也能產生價格。 此案例依照維度優先順序對這些維度進行加權，並使用 Null 值表示不相符的維度值。

- **成本優先順序**：依據成本價設定比對相符時，維度的成本優先順序值將指示該維度的權數。 **成本優先順序** 值在所有 **適用於成本** 的維度中須是唯一的。
- **銷售優先順序**：依據銷售價或帳單費率設定比對相符時，維度的銷售優先順序值將指示該維度的權數。 **銷售優先順序** 值在所有 **適用於銷售** 的維度中須是唯一的。
