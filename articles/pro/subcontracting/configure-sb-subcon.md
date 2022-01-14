---
title: 設定排程面板，以顯示合約工作者和已轉包產能
description: 本主題說明如何在 Microsoft Dynamics 365 Project Operations 中設定排程面板，以在配置專案資源需求的人員時顯示已轉包的資源產能。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903352"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>設定排程面板，以顯示合約工作者和已轉包產能 

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

Microsoft Dynamics 365 Project Operations 的排程面板可以在兩種方式下搜尋資源：

- 一般資源搜尋 (沒有任何特定專案型資源需求的內容)。
- 需求特定資源搜尋 (專案需求會提供所建議之資源的內容)。

若要將已轉包資源產能和合約工作者通知給排程面板，您需要更新排程面板設定。 這些更新包括： 
- 更新一般資源搜尋的排程面板設定。
- 更新需求型資源搜尋的排程面板設定。

## <a name="update-schedule-board-settings-for-general-resource-search"></a>更新一般資源搜尋的排程面板設定
### <a name="update-filters-for-general-resource-search"></a>更新一般資源搜尋的篩選
搜尋資源時，必須更新排程面板上的可用篩選，讓您也可以指定下列任一或所有項目來搜尋外部資源：
  - 工作者類型 (所顯示的資源應是合約工作者還是員工)。
  - 資源應隸屬於的廠商公司。
  - 屬於特定轉包合約或轉包合約服務內容的資源。
    
### <a name="update-retrieve-resource-query"></a>更新擷取資源查詢
用於搜尋的查詢也必須更新為使用這些額外的篩選屬性。 使用下列步驟來更新一般資源搜尋的排程面板設定：  
1. 開啟特定排程面板的 **排程面板設定**。
2. 開啟 **一般設定** 索引標籤，然後捲動至 **其他設定**。
3. 在此區段的設定清單中，將 **篩選配置** 更新為 **Project Operations Lite 的預設篩選配置**。
4. 將 **擷取資源查詢** 更新為 **Project Operations Lite 的預設擷取資源查詢**。

![更新一般資源搜尋的排程面板設定](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>更新需求型資源搜尋的排程面板設定
### <a name="update-filters-for-requirement-specific-resource-search"></a>更新需求特定資源搜尋的篩選 
搜尋資源時，必須更新排程面板上的可用篩選，讓您也可以指定下列任一或所有項目來搜尋外部資源：
 - 工作者類型 (所顯示的資源應是合約工作者還是員工)。
 - 資源應隸屬於的廠商公司。
 - 屬於特定轉包合約或轉包合約服務內容的資源。

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>更新需求特定資源搜尋的擷取資源查詢 
用於搜尋的查詢也必須更新為使用這些額外的篩選屬性。 使用下列步驟來更新需求型資源搜尋的排程面板設定：

1. 開啟特定排程面板的 **排程面板設定**，然後選取 **開啟預設設定** 以開啟需求特定搜尋的設定。
2. 開啟 **一般設定** 索引標籤，然後捲動至 **其他設定**。
3. 在此區段的設定清單中，將 **篩選配置** 更新為 **Project Operations Lite 的預設篩選配置**。
4. 將 **擷取資源查詢** 更新為 **Project Operations Lite 的預設擷取資源查詢**。
5. 開啟 **排程類型** 索引標籤，然後移至 **專案**。
6. 在 **專案** 的設定底下，將 **排程小幫手擷取資源查詢** 更新為 **Project Operations Lite 的預設擷取資源查詢**，並將 **排程小幫手擷取限制查詢** 更新為 **Project Operations Lite 的預設擷取限制查詢**。

![更新需求型資源搜尋的排程面板設定](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
