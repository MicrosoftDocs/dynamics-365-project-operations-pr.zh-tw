---
title: 關閉定價維度
description: 本主題提供有關如何關閉定價維度的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274718"
---
# <a name="turning-off-a-pricing-dimension"></a>關閉定價維度

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

您可能每隔幾年就需要檢閱並更新您的定價策略。 任何您所進行的更新可能都需要您關閉現有的定價維度，並建立新的定價維度。 例如，您可能先前已依 **角色** 定價，但現在決定依據 **工作經驗** 進行定價。 這可能會要求您必須關閉以 **角色** 為定價維度的設定，並將 **工作經驗** 建立為新的定價維度。 

關閉定價維度 (不論是預設還是自訂否) 的動作，都可以藉由將定價維度的 **適用於成本** 和 **適用於銷售** 欄位設定為 **否** 來完成。

不過，這樣做時，您可能會收到錯誤訊息 **如果有相關聯的價格記錄，則無法更新或刪除定價維度。**

![關閉定價維度時可能發生商務程序錯誤](media/Business-Process-Error.png)

此錯誤訊息表示存在先前為所要關閉維度設定的價格記錄。 必須先刪除參照該維度的所有 **角色價格** 和 **角色價格加成** 記錄，才能將維度的適用性設為 **否**。 此規則適用於內建定價維度以及任何您可能已建立的自訂定價維度。 這項驗證的原因是，每個 **角色價格** 記錄都必須有一個唯一的維度組合。 例如，在名為 **2018 年美國成本費率** 的價目表中，您有下列 **角色價格** 列。 

| 標準職稱         | 組織單位    |單位   |價格  |貨幣  |
| -----------------------|-------------|-------|-------|----------|
| 系統工程師|Contoso US|Hour| 100|USD|
| 資深系統工程師|Contoso US|Hour| 150| USD|


當您關閉以 **標準職稱** 為定價維度的設定，而定價引擎搜尋價格時，只會使用輸入內容中的 **組織單位** 值。 如果輸入內容的 **組織單位** 是「Contoso US」，則結果並非決定性，因為這兩個列都會相符。 為了避免這種案例，當您建立 **角色價格** 記錄時，系統會驗證維度組合是否為唯一。 如果維度在建立 **角色價格** 記錄後已關閉，則可能會違反此限制。 因此，關閉維度之前，必須先刪除所有已填入該維度值的 **角色價格** 和 **角色價格加成** 列。


[!INCLUDE[footer-include](../includes/footer-banner.md)]