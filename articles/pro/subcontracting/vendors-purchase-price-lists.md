---
title: Project Operations 中的廠商及購買價目表管理
description: 本主題提供的資訊，可協助您建立並維護轉承包的廠商資料及購買價目表。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994131"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Project Operations 中的廠商及購買價目表管理

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

## <a name="vendors-in-project-operations"></a>Project Operations 中的廠商

在 Microsoft Dynamics 365 Project Operations 中，廠商帳戶的關聯類型為 **廠商** 或 **供應商**。 您只能選取轉包合約上的廠商屬於這其中一個關聯類型的客戶記錄。

您可以將一份或多份購買價目表與廠商記錄建立關聯。 不過，每份與廠商記錄相關聯的購買價目表都必須有明顯不同的有效日期範圍。 Project Operations 對於購買價目表不支援重疊的有效日期範圍。

根據預設，廠商記錄的下列欄位和概念會用於任何針對該廠商建立的轉包合約：

- 付款條款
- 帳單連絡人
- 主要連絡人

    > [!NOTE]
    > 根據預設，廠商的主要連絡人是用來做為轉包合約廠商帳戶管理員。

- 貨幣
- 目前的購買價目表

## <a name="purchase-price-lists-in-project-operations"></a>Project Operations 中的購買價目表

**內容** 欄位設定為 **購買** 的價目表視為購買價目表。 可以定義購買價目表來表示時間、費用和材料的採購費率目錄。 購買價目表與 Project Operations 中的成本及銷售價目表相似。 下列概念適用於成本及銷售價目表，同樣也適用於購買價目表：

- **日期時效性** – 購買價目表具有日期有效範圍。 日期時效性以每份價目表上的 [開始日期] 和 [結束日期] 欄位來表示。 開始日期與結束日期之間的時間即是日期有效期間。
- **貨幣** – 價目表標題上的貨幣是目錄中人力、費用類別和產品用來做為表示購買價格所用的貨幣。
- **預設時間單位** – 預設時間單位表示購買項目的人力價格。 價目表的時間單位欄位只是用來提供預設值。 該值可以在個別角色價格列上變更。

購買價目表可以附加至廠商記錄做為稱為專案價目表的關聯。 這些價目表是用來在轉包合約服務內容上輸入預設價格。 有多份購買價目表附加至廠商記錄時，預設會將最新的價目表用於為廠商建立的轉包合約。 只有 **內容** 欄位設定為 **購買** 的價目表才能附加至廠商記錄。

### <a name="subcontract-specific-purchase-price-lists"></a>轉包合約專屬的購買價目表

購買價目表也可以附加至轉包合約做為稱為專案價目表的關聯。 這些價目表是用來在轉包合約服務內容上輸入預設價格。 有多份採購價目表附加至轉包合約時，每一份都必須有明顯不同的日期有效範圍。 Project Operations 不支援有效日期範圍重疊的購買價目表。 只有 **內容** 欄位設定為 **購買** 的價目表才能附加至轉包合約。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
