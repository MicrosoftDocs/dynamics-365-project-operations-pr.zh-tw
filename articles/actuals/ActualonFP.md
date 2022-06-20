---
title: 在固定價格業務開發中的影響
description: 本文提供有關業務開發在 Microsoft Dynamics 365 Project Operations 中處於固定價格業務開發生命週期時各種事件中對實際值資料表所產生影響的資訊。
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918118"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>在固定價格業務開發中的影響

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

下表列出固定價格業務開發中各種事件發生時所建立之不同交易類型的實際值。

| 事件 | 成本實際值 | 未開單銷售實際值 | 已開單銷售實際值 | 範例 |
|---|---|---|---|---|
| 時間已建立。 | 不適用 | 不適用 | 不適用 | <p>Bob Kozack 來自成本費率為每小時 100 美元 (USD 100) 的 Fabrikam US 組織單位，他正在從事一個名為「在 Adatum 進行機械臂安裝」的專案。 此專案已對應至合約服務內容中的固定價格帳務方式。 以下是 Bob Kozak 的範例時間項目：</p><p>Bob Kozack - 8 小時</p> |
| 時間已提交。 | 不適用 | 不適用 | 不適用 | 時間項目的成本帳目明細已建立。 帳目分錄中已輸入預設成本費率。 |
| 此時間項目會在核准之前回收。 | 不適用 | 不適用 | 不適用 | |
| 時間已核准。 | 成本實際值已建立。 | 不適用 | 不適用 | <p>建立的新實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li></ul> |
| 時間核准已取消。 | <p>原始成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p> | 不適用 | 不適用 | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li></ul> |
| 此時間項目會在核准之後回收。 | <p>原始成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p> | 不適用 | 不適用 | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li></ul> |
| 合約已確認。 | <p>舊成本實際值的調整狀態更新為 **已調整**。</p><p>建立調整狀態為 **不可調整** 的沖回成本實際值。</p><p>重新評估合約規則之後，建立新的成本實際值。</p> | 不適用 | 不適用 | <p>已更新的現有實際值：</p><ul><li>**成本實際值**：Bob Kozack，8 小時，美元 800，*已調整*</li></ul><p>為了沖回先前財務影響而建立的新實際值：</p><ul><li>**成本實際值**：Bob Kozack，(8 小時)，(美元 800)，*已調整*</li></ul><p>針對已重新評估的財務影響所建立的新實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li></ul> |
| 發票已建立。 | 不適用 | 不適用 | 不適用 | |
| 發票已透過里程碑進行確認。 | 不適用 | 不適用 | 建立新的依里程碑計費的銷售實際值。 | <p>保持不變的現有實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，美元 800</li></ul><p>為了記錄已開單銷售值而建立的新實際值：</p><ul><li>**已開單銷售實際值：** 里程碑，美元 5,000</li></ul> |
| 發票已更正為貸記里程碑。 | 不適用 | 不適用 | 沖回已開單銷售實際值已建立。 | <p>保持不變的現有實際值：</p><ul><li>**成本實際值：** Bob Kozack，8 小時，800 美元</li></ul><p>已更新的現有實際值：</p><ul><li>**已開單銷售實際值：** 里程碑，美元 5,000，*已調整*</li></ul><p>為了沖回先前已開單銷售值而建立的新實際值：</p><ul><li>**已開單銷售實際值：** 里程碑，(美元 5,000)，*不可調整*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
