---
title: 管理專案合約上的專案價目表
description: 本主題提供有關管理專案合約上的專案價目表的資訊。
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824026d0620de809c0366c86c2d4d13fe83d4d1ddd4c0dc1cc2645ff712705d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996471"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>管理專案合約上的專案價目表

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 中的專案合約是設計來支援合約上多個在有效期限內的銷售價目表。 在 Project Operations 中，有一個新的名為 **專案價目表** 的相關實體。 此實體與專案合約有一對多關聯。

專案價目表可用於訂定專案中時間、材料及費用交易的價格。 當合約有一份或多份專案價目表時，這些價目表會在透過合約服務內容與合約產生關聯的專案上，用於訂定時間、材料、費用估計值及實際值的價格。

當專案合約沒有專案價目表時，您會看到警告訊息，指出沒有專案價目表，無法為您的估計值、實際專案工作、材料以及已記錄的費用進行定價。 銷售值不會有任何價格。

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>在專案合約上建立或解除與專案價目表的關聯

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>建立用於估計專案型工作、材料和費用的特定價目表，或與之產生關聯

1. 在專案合約上，選取 **專案價目表** 索引標籤。
2. 在子格中，選取 **+ 新增專案價目表**。
3. 在 **快速建立** 滑桿上，選取價目表。 

  下拉式清單會顯示所有其內容設定為 **銷售** 的價目表，其中價目表上的貨幣與合約上的貨幣相符。
  
4. 輸入專案價目表關聯的描述、選取 **儲存**，然後關閉 **快速建立** 滑桿。

   專案價目表關聯已建立。
   
5. 重複步驟 1-4，將多個專案價目表關聯至專案合約。 只有您在每個關聯的專案價目表上各有不同的日期時效性時，才要建立多個專案價目表。

> [!NOTE]
> Project Operations 不支援專案價目表的日期時效性重疊。 如果包含指定日期的交易有多個專案價目表，該交易的價格會預設為零。

### <a name="remove-a-project-price-list-association"></a>移除專案價目表關聯

- 選取專案價目表，然後選取子格上的 **刪除合約專案價目表**。 

  價目表會從合約上的專案價目表中移除。 不會將價目表本身刪除。 只是刪除與合約的關聯。

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>在合約上設定專案價目表的自動設定預設

專案價目表可以設定為預設專案價目表。 這項設定可確保您組織中的所有合約一律都是以該價格期間的標準專案價目表為開始。

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>設定專案價目表的組織預設值

1. 移至 **設定** > **一般**，然後選取 **參數**。
2. 在 **使用中參數** 清單頁面中，選取並按兩下記錄加以開啟。 按兩下時，請確定您所按下的欄位值不是超連結。 
3. 在 **使用中參數** 頁面上，選取 **價目表** 索引標籤。子格會顯示預設價目表的清單。 這是標準成本及銷售價目表的清單。 您銷售所用的每一種計價貨幣都有此處關聯的 **銷售** 價目表，可確保銷售價目表會是您為使用此貨幣進行交易之客戶所建立的任何合約上的預設值。

### <a name="set-up-a-customer-specific-project-price-list"></a>設定特定客戶適用的專案價目表

您也可以在與客戶議定主要定價合約時，設定客戶特定的專案價目表。

1. 移至 **銷售** > **客戶**。
2. 從現行客戶清單中，選取有特殊價目表的客戶。
3. 選取要加以開啟的客戶記錄，然後選取 **專案價目表** 索引標籤。子格會顯示此客戶特有的專案價目表清單。 
4. 在此處建立新的價目表關聯，讓專案價目表專屬於此客戶。

## <a name="custom-pricing-on-a-project-contract"></a>專案合約上的自訂定價

有了組織和客戶特定的預設專案價目表之後，系統就會自動使用這些專案價目表關聯來建立您的專案合約。 不過，系統一律會複製專案合約上的專案價目表，並將日期和合約名稱附加至其複本。 客戶經理和專案經理接著即可開始編輯這些複本上的價格。 這些變更過的價格將只適用於此專案合約。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
