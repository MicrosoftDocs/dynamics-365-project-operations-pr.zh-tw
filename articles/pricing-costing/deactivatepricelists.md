---
title: 停用價目表
description: 本主題說明如何停用或移除未使用或舊的價目表。
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701914"
---
# <a name="deactivate-price-lists"></a>停用價目表 

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

若要從 Dynamics 365 Project Operations 移除舊的或未使用的價目表，必須完成兩個步驟。 

1. 從特定頁面移除或刪除價目表。
2. 從 **價目表** 頁面的使用中價目表停用或刪除價目表。

>[!IMPORTANT]
> 您必須完成這兩個步驟才能完全移除價目表。 只執行步驟 2 (即直接從 [使用中價目表] 檢視表移除或停用價目表) 是不夠的。 您還必須從步驟 1 提到的所有位置中刪除此價目表的關聯。

## <a name="delete-the-price-list-from-specific-pages"></a>從特定頁面刪除價目表
1. 若要從 Project Operations 中刪除價目表，請移至下列頁面：  

      - **專案參數** 頁面 > **價目表** 索引標籤
      - **組織單位** 頁面 > **價目表** 網格
      - **客戶** 頁面 > **專案價目表** 網格
      - **專案報價** 頁面 > **專案價目表** 網格：這會套用至所有使用中專案報價。
      - **專案連絡人** 頁面 > **專案價目表** 網格：這會套用至所有使用中專案連絡人。

 2. 您必須在每個頁面中選取您要刪除的價目表，然後選取 **刪除**。 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>從價目表頁面刪除或停用價目表
 
1. 若要從使用中價目表中刪除價目表，請移至 **銷售** > **客戶** > **價目表**。 
2. 選取您要刪除的價目表，然後選取 **刪除**。 如果任何現有交易參考了價目表，就無法將其刪除。 如果發生這種情況，您可以停用價目表，使其不再出現於任何檢視表。 
3. 若要停用價目表，請再次選取價目表，然後選取 **停用**。   
