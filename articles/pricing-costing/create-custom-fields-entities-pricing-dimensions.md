---
title: 將自訂欄位及實體建立為定價維度
description: 本主題提供有關如何建立自訂選項組或實體的資訊。
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000516"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>將自訂欄位及實體建立為定價維度

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

當您想要建立自訂選項組或實體以用作定價維度時，請完成下列步驟。 如需詳細資訊，請參閱[定價維度概觀](pricing-dimensions-overview.md)。  

> [!IMPORTANT]
> 建議您在不同的解決方案中進行所有自訂定價維度變更。 這個重要的最佳做法提供您日後視需要更新或移除變更的彈性。 有助於重複使用您的工作，以及讓您更便於將這些變更移植到另一個執行個體。進行所有必要變更之後，將此解決方案匯出為 **受管理的解決方案**，再將其匯入至其他執行個體，即可重複使用您的定價設定。

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>在定價維度解決方案中建立自訂欄位及選項組

定價維度可以是選項組或實體。 兩者預必須在定價解決方案中建立。 此程序中的步驟說明如何建立以實體為準的維度和以選項組為準的維度。

### <a name="entity-based-dimensions"></a>以實體為準的維度
若要建立以實體為準的維度，請執行下列步驟：

1. 移至 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。
2. 在方案總管的左導覽窗格中，選取 **實體**。
3. 選取 **新增** 以建立名為 **標準職稱** 的新實體。 
4. 輸入其餘必要資訊，然後選取 **儲存**。

> ![標準職稱實體定義](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>以選項組為準的維度 
您可以建立兩個以選項組為準的維度。 

- 使用 **資源工作地點** 來追蹤 **住家** 地點工作和 **現場** 工作的價格。 
- 使用 **資源工作時數** 搭配 **正常工時** 和 **加班工時** 值，在工作完成時套用加成。

下圖提供 **資源工作地點** 維度的檢視表。 

> ![以選項組為準的定價維度，名為「資源工作地點」](media/Option-set-PD-called-Resource-Work-Location.png)

下圖提供 **資源工作時數** 維度的檢視表。 

> ![以選項組為準的定價維度，名為「資源工作時數」](media/Option-set-PD-called-Resource-Work-Hours.png)

1. 移至 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。 
2. 在方案總管的左導覽窗格中，選取 **選項組**。 
3. 選取 **新增** 建立新的選項組、輸入其餘必要資訊，然後選取 **儲存**。

## <a name="create-data-for-entity-based-dimensions"></a>建立以實體為準維度的資料

您可以手動建立以實體為準維度的資料，或是使用 Microsoft Excel 匯入或服務通話來建立此資料 使用此程序中的步驟，從以實體為準的維度 **標準職稱** 建立兩個標準職稱 **系統工程師** 和 **資深系統工程師**。 如果要建立的資料不大 (如下列範例所示)，您可以使用標準表單。

1. 選取 **進階尋找**。
2. 選取 **標準職稱** 實體，然後選取 **結果**。 將會顯示 **標準職稱** 實體中所有的列。
3. 選取 **新增**，並在 **名稱** 欄位中輸入「系統工程師」，然後選取 **儲存**。
4. 關閉頁面。 
5. 重複步驟 1-3，為「資深系統工程師」建立另一個標準職稱。

> ![標準職稱實體的範例資料](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]