---
title: 售前階段和業務開發中的實際值影響
description: 本主題提供有關業務開發在 Microsoft Dynamics 365 Project Operations 中處於售前階段時各種事件中對實際值資料表所產生影響的資訊。
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577226"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>售前階段和業務開發中的實際值影響

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

下表列出專案業務開發售前階段中各種事件發生時所建立之不同交易類型的實際值。

| 事件 | 成本實際值 | 範例 |
|---|---|---|
| 時間已建立。 | 不適用 | <p>Bob Kozack 來自成本費率為每小時 100 美元 (USD 100) 的 Fabrikam US 組織單位，他正在從事一個名為「在 Adatum 進行機械臂安裝」的專案。 此專案已對應至合約服務內容中的固定價格帳務方式。 以下是 Bob Kozak 的範例時間項目：</p><p>Bob Kozack - 8 小時</p> |
| 時間已提交。 | 不適用 | 時間項目的成本帳目明細已建立。 帳目分錄中已輸入預設成本費率。 |
| 此時間項目會在核准之前回收。 | 不適用 | |
| 時間已核准。 | 成本實際值已建立。 | <p>建立的新實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li></ul> |
| 時間核准已取消。 | <p>原始成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p> | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li></ul> |
| 此時間項目會在核准之後回收。 | <p>原始成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p> | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li></ul> |
| 報價已成交，且合約已建立。 | <p>舊成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p><p>重新評估合約規則之後，建立新的成本實際值。</p> | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li></ul><p>在報價已成交且合約建立時，為重新評估的財務影響所建立的新實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li><li>**未開單銷售實際值：** Bob Kozack，8 小時，美元 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
