---
title: 商機設定 - 精簡
description: 本主題提供有關專案型交易和專案型商機明細的資訊。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c34817181b75b1b0079974f536e4d7b032ae87dd
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181018"
---
# <a name="opportunity-header---lite"></a>商機標題 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_

商機標題會擷取套用至專案型商機中所有明細之專案型交易的整體資訊。

Dynamics 365 Project Operations 中的專案型商機是 Dynamics 365 Sales 中的商機擴充。 這些擴充功能提供專案型商機所特有且必要的其他功能。 這些擴充功能可能會包含可專案型商機中使用的新欄位和功能區動作。 您可能會發現有些在 Sales 中提供的欄位、功能和預設邏輯，無法在 Project Operations 中使用。

下表包含專案型商機中的欄位，這些欄位若不是 Project Operations 所特有的欄位，就是有一些在行為上與 Sales 中的商機不同的重要變更。

| **欄位** | **位置** | **描述** | **下游影響** |
| --- | --- | --- | --- |
| 鍵入 | [一般] 索引標籤 (隱藏) | 此選項組欄位具有下列選項：</br>- 工作型 (只有 Project Operations 提供)</br>- 項目型 (只有在 Project Operations 和 Sales 已安裝時提供)</br>- 服務維護型 (安裝 Field Service 時提供) | 使用 Project Operations時，此欄位值會自動設定為 **工作型**，這會將商機分類為專案型商機。 商機必須是專案型商機，才能在此交易的下游銷售處理中啟用所有專案特定擴充及功能。 |
| 連絡人 | [一般] 索引標籤 | 參考此交易的客戶主要連絡人。 | |
| 帳戶 | [一般] 索引標籤 | 參考客戶的公司或客戶記錄。 | |
| 客戶經理 | [一般] 索引標籤 | 此專案型商機的客戶經理姓名。 | 客戶經理負責管理與客戶之間的關聯，直到此專案完成。 根據繫結至客戶經理的可預約資源記錄，預設會使用合約單位。 |
| 合約單位 | [一般] 索引標籤 | 負責交付專案或與此交易相關之專案的組織單位。 | 合約單位是要在完成交易後完成專案的公司部門。 每個合約單位都有貨幣，而此貨幣可用來報告專案期間所產生的估計和實際成本。 |

如需了解商機 **摘要** 索引標籤上的所有其他欄位和區段，請參閱[建立或編輯商機 (Sales 和銷售中心)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
