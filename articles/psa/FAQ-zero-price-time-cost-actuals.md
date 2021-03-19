---
title: 為什麼時間成本實際值上的價格會預設為零？
description: 排解時間成本實際值上的價格為何預設為 0 的問題。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 65f2bc773a376800928cc3746691061d8e290f74
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285788"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>為什麼時間成本實際值上的價格會預設為零？

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

本常見問題集適用於交易類別設為 [時間] 且交易類型為 [成本] 的實際值。 下列三項檢查可協助您對時間成本實際值的價格為何會預設為 0 的問題進行疑難排解。
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>檢查 1：找出專案的成本價目表

從實際值的專案欄位中尋找專案，然後移至專案頁面。 按一下欄位中的合約單位連結。 在 [合約單位] 頁面中，檢查合約單位在 [成本價目表] 網格中是否有價目表。

如果有一個以上的價目表，您就找到了問題所在。 Project Service 對每個組織單位僅支援一份價目表。 從此實體移除所有的價目表，直到只有一份價目表附加在組織單位的 [成本價目表] 網格中為止。

如果沒有任何價目表附加至組織單位，請記下組織單位的貨幣。 移至 Project Service，再移至 [參數]，然後開啟 [價目表] 索引標籤。檢查是否有任何內容設為 [成本] 且貨幣符合組織單位貨幣的價目表。
 
如果沒有任何符合該準則的價目表，您就找到了問題所在。 務必要有至少一個內容設為 [成本] 且貨幣符合組織單位貨幣的價目表。

如果有多份符合該準則的價目表，請繼續閱讀本文件以進行其他檢查。

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>檢查 2：前面找到的價目表是否在時間成本實際值的特定日期上有效？

若要讓 Project Service 考慮用於預設價格的價目表，該價目表必須適用於時間成本實際值的日期。 請檢查下列項目以了解前面找到的價目表是否適用：

- 檢查所附加價目表之一般索引標籤上的開始和結束日期是否不為空白。 如果前面找到的價目表，其開始和結束日期為空白時，您就找到了問題所在。 
- 記下時間成本實際值的開始日期欄位，並檢查任何找到的價目表是否適用於該日期。 例如，時間成本實際值的日期應落在價目表的開始日期和結束日期之內。 
    - 如果時間成本實際值上沒有任何涵蓋該日期的價目表，您就找到了問題所在。 修改價目表的開始和結束日期，以確保價目表涵蓋時間成本實際值的日期。 
    - 如果時間成本實際值上有多份涵蓋該日期的價目表，您就找到了問題所在。 您可以修正此問題，做法為編輯價目表的開始和結束日期，只留下一份涵蓋時間成本實際值日期的價目表。 
    - 如果只有一份涵蓋時間成本實際值日期的價目表，請移至本文件的下一項檢查。
完成必要的修正之後，請重新建立時間項目、加以核准，並確認時間成本實際值顯示有效的價格。

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>檢查 3：時間成本實際值的定價維度價目表中是否有價格？

如果您已順利完成「檢查 1」和「檢查 2」，現在應該只有一份適用於時間成本實際值日期的價目表。 開啟這份價目表，並移至 [角色價格] 索引標籤。確定時間成本實際值上有一列資料在定價維度的網格中。

如果時間成本實際值上沒有任何資料列在定價維度的角色價格網格中，您就找到了問題所在。 在時間成本實際值上的定價維度的 [角色價格] 網格中建立一列。 完成此動作之後，請重新建立時間項目、加以核准，並確認時間成本實際值顯示有效的價格。
 
如果執行上述三項檢查後，時間成本實際值上仍未看到有效價格，請記入支援票證。





[!INCLUDE[footer-include](../includes/footer-banner.md)]