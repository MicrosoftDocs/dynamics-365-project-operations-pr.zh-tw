---
title: 專案報價分析
description: 此主題提供專案報價分析的相關資訊。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f3bff90f91e1df8bda495912a4aad0fa69342396
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592406"
---
# <a name="analysis-of-project-quotes"></a>專案報價分析

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation 會分析專案報價，以估計獲利能力。 它也會分析報價與客戶對交付日期或完成日期以及預算的期望相符程度。

## <a name="profitability-analysis"></a>獲利率分析

Project Service Automation 使用毛利率和調整後毛利率來分析獲利率。

- 毛利率使用下列公式計算：

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- 調整後毛利率使用下列公式計算：

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

如果毛利率和調整後毛利率的值相差幅度很大，表示報價中有一大部分的工作是歸類為非應收費。

## <a name="analysis-of-customer-expectations"></a>分析客戶期望

如果您輸入下列欄位的值，就可以分析報價並產生客戶對排程和預算的期望圖表：

- 報價標頭上的 **要求的交貨日期** 欄位。
- 每個報價明細的 **客戶預算** 欄位 (適用於專案型明細和產品型明細)。

分析客戶對排程的期望的作法是，在報價的所有報價明細中，將報價明細詳細資料的最後結束日期與要求的交貨日期進行比較。

分析客戶對排程的預算的作法是，在所有報價明細中，將客戶預算總計的總和與報價金額進行比較


[!INCLUDE[footer-include](../includes/footer-banner.md)]
