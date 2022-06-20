---
title: 交易關係 - 連結不同交易類型的實際值
description: 本文說明如何使用交易關係來連結不同類型的實際值，以協助追蹤獲利能力、帳務積存以及已開單與未開單營收計算。
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926076"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>交易關係 - 連結不同交易類型的實際值

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

建立交易關係記錄是要在時間、費用或材料使用在其生命週期中從報價或售前階段移往合約階段、核准和/或回收、開立發票以及可能的貸記或更正發票處理時，連結不同類型的實際值。

下列範例顯示 Project Operations 專案生命週期中時間項目的一般處理程序。

> ![處理 Project Operations 中的時間項目。](media/basic-guide-17.png)

處理 Project Operations 專案生命週期中的時間項目時，會遵循下列步驟： 

1. 提交時間項目會導致建立兩個帳目明細：一個用於成本，一個用於未開單銷售。 
2. 最終核准時間項目會導致建立兩個實際值：一個用於成本，一個用於未開單銷售。 這兩個實際值是使用交易關係來連結。
3. 使用者建立專案發票時，會使用來自未開單銷售的資料建立發票明細交易。
4. 確認發票時，這會建立兩個新的實際值：未開單銷售沖回和已開單銷售實際值。 未開單銷售沖回與原始未開單銷售實際值是使用沖回交易關係進行連接。 已開單銷售和原始未開單銷售實際值也會連接在一起，以顯示曾經積存或在製品 (WIP) 營收與現已開單營收之間的連結。   

此處理工作流程中的每個事件都會觸發建立 **交易關係** 資料表中的記錄。 這有助於建立對這些跨時間項目、帳目明細、實際值和發票明細詳細資料所建立記錄之間關聯性的追蹤。

下表顯示先前工作流程之 **交易關係** 實體中的記錄。

|Event                   |交易 1                 |交易 1 角色 |交易 1 類型       |交易 2          |交易 2 角色 |交易 2 類型 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|時間項目送出   |帳目明細 (銷售) GUID     |未開單銷售 |msdyn_journalline            |帳目明細 (成本) GUID     |成本            |msdyn_journalline  |
|時間核准           |未開單實際值 (銷售) GUID  |未開單銷售 |msdyn_actual                 |成本實際值 (成本) GUID       |成本            |msdyn_actual       |
|發票建立        |發票明細詳細資料 GUID      |已開單銷售   |msdyn_invoicelinetransaction |未開單銷售實際值 GUID   |未開單銷售  |msdyn_actual       |
|發票確認    |沖回實際值 GUID         |沖回      |msdyn_actual                 |原始未開單銷售 GUID |原始        |msdyn_actual       |
|                        |已開單銷售 GUID             |已開單銷售   |msdyn_actual                 |未開單銷售實際值 GUID   |未開單銷售  |msdyn_actual       |
|草稿發票更正 |發票明細交易 GUID|取代      |msdyn_invoicelinetransaction |已開單銷售 GUID            |原始        |msdyn_actual       |
|確認發票更正|已開單銷售沖回 GUID  |沖回      |msdyn_actual                 |已開單銷售 GUID            |原始        |msdyn_actual       |
|                        |新的未開單銷售 GUID |取代            |msdyn_actual                 |已開單銷售 GUID            |原始        |msdyn_actual       |


下圖顯示使用 Project Operations 中的時間項目範例，在發生各種事件時建立不同類型實際值之間的連結。

> ![在 Project Operations 中將不同類型實際值相互連結的方式。](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
