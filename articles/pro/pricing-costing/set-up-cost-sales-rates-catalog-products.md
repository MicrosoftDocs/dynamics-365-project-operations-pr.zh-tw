---
title: 設定產品類別目錄產品的成本及銷售費率 - 精簡
description: 本主題提供有關如何為產品類別目錄中的項目設定成本及銷售費率的資訊。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176691"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>設定產品類別目錄產品的成本及銷售費率 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_


在 Dynamics 365 Project Operations 中設定產品類別目錄項目的定價，與在 Dynamics 365 Sales 中設定的方式相同。

由於無法在 Project Operations 中估計或使用專案上的產品，因此不需要在報價和合約的專案價目表上設定產品類別目錄價格。

產品類別目錄價格必須在報價、合約或客戶的 **產品價格** 欄位中進行設定。 不要在這些實體的專案價目表中設定產品類別目錄價格。 專案價目表是 Project Operations 所專有。 其中有可將價目表從報價複製到合約的應用程式特定商務邏輯。 結果是合約特定專案價目表。 如果報價的專案價目表變得太大，則複製作業可能會延遲報價成交程序。 不會複製產品價目表，以在合約上建立自訂價目表。 這表示產品價目表不會影響報價成交程序的效能。
