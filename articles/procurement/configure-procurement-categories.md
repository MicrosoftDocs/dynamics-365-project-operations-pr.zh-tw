---
title: 將採購類別與專案採購單及待處理廠商發票搭配使用
description: 本文說明如何設定可與專案採購單及待處理廠商發票搭配使用的採購類別。
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028600"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>將採購類別與專案採購單及待處理廠商發票搭配使用

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

採購專業人員可以建立和維護可在專案採購單和待處理廠商發票中使用的項目與服務目錄。 [採購目錄](/dynamics365/supply-chain/procurement/procurement-catalogs)提供一種方式，您不需要設定已發佈的產品類別目錄，也能輕鬆地分類購買項目。 每個採購類別都可以對應至時間、費用或項目交易的專案類別。 將使用採購類別的待處理廠商發票過帳之後，系統會建立時間、費用或材料專案實際值、專案交易以及明細分類帳分錄。

## <a name="minimum-version-requirements"></a>最小版本需求

若要將採購類別與專案採購單搭配用於 Microsoft Dynamics 365 Project Operations 非庫存/資源型案例，必須有下列版本：

- Project Operations Dataverse 解決方案 4.41.0.45 版或更新版本
- 財務和營運環境 10.0.26 版或更新版本

## <a name="run-dual-write-maps-for-procurement-category-support"></a>執行雙重寫入對應以取得採購類別支援

確定 **Project Operations 整合專案廠商發票明細匯出實體 msdyn\_projectvendorinvoicelines** 的對應使用的是 1.0.0.4 版或更新版本。

## <a name="enable-the-feature-key-for-procurement-categories"></a>啟用採購類別的功能金鑰

依照下列步驟，啟用可將採購類別與專案採購單搭配使用的功能。

1. 在 Dynamics 365 Finance 中，開啟 **功能管理** 工作區。
1. 在功能清單中，尋找 **在資源型/非庫存案例適用的 Project Operations 中使用採購類別** 功能，然後選取 **啟用**。

> [!IMPORTANT]
> 依照先決條件，您也必須啟用 **在資源型/非庫存案例適用的 Project Operations 中啟用待處理廠商發票** 功能。

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>對應採購類別階層中的專案類別

依照下列步驟，將專案類別對應至 **採購類別階層** 中的採購類別：

1. 移至 **採購和委外 \> 採購類別**。
1. 選取 **編輯類別階層**。
1. 選取所需的類別階層節點，然後在 **指派專案類別** 索引標籤上，將節點與 **時間**、**費用** 或 **項目專案** 類別 (即 **預設時間** 或 **預設費用** 類別) 中的專案類別建立關聯。
1. 選取 **儲存**。
1. 關閉頁面。

> [!NOTE]
> 將採購類別對應至專案類別是選擇性的。 如果未對應採購類別，則系統會使用 **專案管理與會計參數** 頁面 **Dynamics 365 Customer Engagement 上的 Project Operations** 索引標籤中 **專案類別預設值** 區段的 **項目** 欄位所設定的值。
