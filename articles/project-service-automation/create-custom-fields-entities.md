---
title: 建立自訂欄位和實體
description: 本主題說明如何在 Power Apps 平台建立自己解決方案中的選項組與實體。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749980"
---
# <a name="create-custom-fields-and-entities"></a>建立自訂欄位和實體 

每當您想要在 Power Apps 平台建立自訂選項組或實體時，請完成下列步驟。  
本主題中的程序應使用 Project Service Automation (PSA) 的 Web 介面來完成。

> [!IMPORTANT]
> 建議您在不同的解決方案中進行所有自訂定價維度變更。 這個重要的最佳做法提供您日後視需要更新或移除變更的彈性、有助於重複使用您的工作，以及讓您更便於將這些變更移植到另一個執行個體。 進行所有必要變更之後，將此解決方案匯出為**受管理的解決方案**，再將其匯入至其他執行個體，即可重複使用您的定價設定。


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>建立自訂定價維度解決方案
1. 在 PSA 中，按一下**設定** > **解決方案**，然後按一下**新增**建立新的解決方案。 
2. 將解決方案命名為 **\<您的組織名稱> 定價維度**、輸入其餘必要資訊，然後按一下**儲存**。

> ![建立自訂定價維度解決方案](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>在定價維度解決方案中建立自訂欄位及選項組

定價維度可以是選項組或實體。 兩者預必須在定價解決方案中建立。 此程序中的步驟說明如何建立以實體為準的維度和以選項組為準的維度。

### <a name="entity-based-dimensions"></a>以實體為準的維度

1. 在PSA 中，按一下**設定** > **解決方案**，然後按兩下 **\<您的組織名稱> 定價維度**。
2. 在方案總管的左導覽窗格中，選取**實體**。
3. 按一下**新增**建立名為**標準職稱**的新實體。 輸入其餘必要資訊，然後按一下**儲存**。

> ![標準職稱實體定義](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>以選項組為準的維度 
您可以建立兩個以選項組為準的維度。 使用**資源工作地點**來追蹤**住家**地點工作和**現場**工作的價格，以及使用**資源工作時數**搭配**正常工時**和**加班工時**值，在工作完成時套用加成。


1. 在PSA 中，按一下**設定** > **解決方案**，然後按兩下 **\<您的組織名稱> 定價維度**。 
2. 在方案總管的左導覽窗格中，選取**選項組**。 
3. 按一下**新增**建立新的選項組、輸入其餘必要資訊，然後按一下**儲存**。

> ![以選項組為準的定價維度，名為「資源工作地點」 ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![以選項組為準的定價維度，名為「資源工作時數」 ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>建立以實體為準維度的資料

您可以手動建立以實體為準維度的資料，或是使用 Microsoft Excel 匯入或服務通話來建立此資料 使用此程序中的步驟，從以實體為準的維度**標準職稱**建立兩個標準職稱**系統工程師**和**資深系統工程師**。 如果要建立的資料不大 (如下列範例所示)，您可以使用標準表單。

1. 在 PSA, 中，按一下**進階尋找**。 選取**標準職稱**實體，然後按一下**結果**。 將會顯示**標準職稱**實體中所有的列。
2. 按一下 **新增**。 在**名稱**欄位中輸入「系統工程師」，然後按一下**儲存**。
3. 關閉表單。 
4. 重複步驟 1-3，為「資深系統工程師」建立另一個標準職稱。

> ![標準職稱實體的範例資料 ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>將所有必要的 PSA 實體及相關元件新增至定價維度解決方案
您必須將下列 Project Service 實體新增至您的定價方案。 使用此程序中的步驟，在定價方案中進行一些重要的結構描述變更，讓實體得知新的定價維度。

1. 在PSA 中，按一下**設定** > **解決方案**，然後按兩下 **\<您的組織名稱> 定價維度**。 
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

> ![將現有實體新增至定價維度解決方案](media/Existing-entities-to-PD-solution.png)

> ![選取解決方案元件](media/Dimension-Components.png)

> [!NOTE]
> 請務必包含所選每個實體的所有表單和檢視表。

4. 當系統提示您包含上述所選實體的任何相依實體時，按一下**否**。

> ![不要包括所有相關元件。](media/Do-not-include-required.png)


