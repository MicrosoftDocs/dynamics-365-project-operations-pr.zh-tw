---
title: 設定產品類別目錄產品的成本及銷售費率 - 精簡
description: 本主題提供有關如何為產品類別目錄中的項目設定成本及銷售費率的資訊。
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996021"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>設定產品類別目錄產品的成本及銷售費率 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_


在 Dynamics 365 Project Operations 中設定產品類別目錄項目定價的方式與在 Dynamics 365 Sales 中的相同。

在 Project Operations 中，無法在專案上估計或使用產品，因此不需要在報價和合約的專案價目表中設定產品類別目錄價格。

請使用報價、合約或客戶的 **產品價格** 欄位來設定產品類別目錄價格。 不要在專案價目表中設定產品類別目錄價格。 專案價目表是 Project Operations 所專有。 應用程式特定的商務規則會將報價的價目表複製到合約。 結果是合約特定專案價目表。 如果報價的專案價目表變得太大，則複製作業可能會延遲報價成交程序。 不會複製產品價目表，以在合約上建立自訂價目表。 因為沒有涉及複製，報價程序的效能不受影響。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]