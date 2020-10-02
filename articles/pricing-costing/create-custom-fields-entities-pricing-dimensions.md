---
title: 將自訂欄位及實體建立為定價維度
description: 本主題提供有關如何建立自訂選項組或實體的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898251"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>將自訂欄位及實體建立為定價維度

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

每當您想要建立自訂選項組或實體時，請完成下列步驟。

> [!IMPORTANT]
> 建議您在不同的解決方案中進行所有自訂定價維度變更。 這個重要的最佳做法提供您日後視需要更新或移除變更的彈性、有助於重複使用您的工作，以及讓您更便於將這些變更移植到另一個執行個體。 進行所有必要變更之後，將此解決方案匯出為**受管理的解決方案**，再將其匯入至其他執行個體，即可重複使用您的定價設定。


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>建立自訂定價維度解決方案
1. 移至**設定** > **解決方案**，然後選取**新增**建立新的解決方案。 
2. 將解決方案命名為 **\<your organization name> 定價維度**、輸入其餘必要資訊，然後選取**儲存**。
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>在定價維度解決方案中建立自訂欄位及選項組

定價維度可以是選項組或實體。 兩者預必須在定價解決方案中建立。 此程序中的步驟說明如何建立以實體為準的維度和以選項組為準的維度。

### <a name="entity-based-dimensions"></a>以實體為準的維度

1. 移至**設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。
2. 在方案總管的左導覽窗格中，選取**實體**。
3. 選取**新增**以建立名為**標準職稱**的新實體。 
4. 輸入其餘必要資訊，然後選取**儲存**。


### <a name="option-set-based-dimensions"></a>以選項組為準的維度 
您可以建立兩個以選項組為準的維度。 使用**資源工作地點**來追蹤**住家**地點工作和**現場**工作的價格，以及使用**資源工作時數**搭配**正常工時**和**加班工時**值，在工作完成時套用加成。


1. 移至**設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。 
2. 在方案總管的左導覽窗格中，選取**選項組**。 
3. 選取**新增**建立新的選項組、輸入其餘必要資訊，然後選取**儲存**。

## <a name="create-data-for-entity-based-dimensions"></a>建立以實體為準維度的資料

您可以手動建立以實體為準維度的資料，或是使用 Microsoft Excel 匯入或服務通話來建立此資料 使用此程序中的步驟，從以實體為準的維度**標準職稱**建立兩個標準職稱**系統工程師**和**資深系統工程師**。 如果要建立的資料不大 (如下列範例所示)，您可以使用標準表單。

1. 選取**進階尋找**、選取**標準職稱**實體，然後選取**結果**。 將會顯示**標準職稱**實體中所有的列。
2. 選取**新增**，並在**名稱**欄位中輸入「系統工程師」，然後選取**儲存**。
3. 關閉此表單。 
4. 重複步驟 1-3，為「資深系統工程師」建立另一個標準職稱。

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>將所有必要的體及相關元件新增至定價維度解決方案
您必須將下列實體新增至您的定價方案。 使用此程序中的步驟，在定價方案中進行一些重要的結構描述變更，讓實體得知新的定價維度。

1. 選取**設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。 
2. 在方案總管的左導覽窗格中，選取**新增現有的** >  **實體**。
3. 在**解決方案元件**對話方塊中，選取下列實體：

  - 實際
  - 可預約資源
  - 估計明細
  - 發票明細詳細資料
  - 帳目明細
  - 專案合約服務內容詳細資料
  - 專案團隊成員
  - 報價明細詳細資料
  - 角色價格加成
  - 角色價格 
  - 時間項目 


> [!NOTE]
> 請務必包含所選每個實體的所有表單和檢視表。

4. 系統提示您包含上述所選實體的任何相依實體時，選取**否**。

