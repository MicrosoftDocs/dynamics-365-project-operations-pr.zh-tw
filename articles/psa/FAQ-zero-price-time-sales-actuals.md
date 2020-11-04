---
title: 為什麼時間銷售實際值上的價格會預設為零？
description: 排解時間銷售實際值上的價格為何預設為 0 的問題。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c886c4a53b4ba47e381b891fe22a565ad8fd1ac6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073120"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>為什麼時間銷售實際值上的價格會預設為零？

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

本常見問題集適用於交易類別設為 [時間] 且交易類型為 [未開單銷售] 的實際值。 下列三項檢查可協助您對時間銷售實際值的價格 (帳單費率) 為何會預設為 0 的問題進行疑難排解。

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>檢查 1：找出專案的銷售價目表

從實際值的專案欄位中尋找專案，並移至專案頁面。 接著移至 [銷售] 索引標籤，並在 [專案合約服務內容] 網格中，按一下 [專案合約] 欄位中的連結。 [專案合約] 頁面將會開啟。 在 [專案合約] 頁面上，移至 [專案價目表] 索引標籤。檢查是否至少有一份價目表附加在這裡。 如果 [專案合約] 的 [專案價目表] 網格中沒有附加任何價目表，您就找到了問題所在。 將價目表附加至 [專案價目表] 網格。 允許在此處附加的價目表必須有設為 [銷售] 的內容欄位，而且價目表的貨幣欄位也應符合專案合約的貨幣欄位。 完成必要的修正之後，請重新建立時間項目、加以核准，並確認未開單銷售實際值顯示有效的價格。 

如果專案合約的 [專案價目表] 網格已附加一份或多份價目表，請繼續本文件的下一項檢查。

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>檢查 2：前面找到的價目表是否在時間銷售實際值的特定日期上有效？

若要讓 Project Service 考慮用於預設價格的價目表，該價目表必須適用於時間銷售實際值的日期。 請檢查下列項目以了解前面找到的價目表是否適用：
- 檢查所附加價目表之一般索引標籤上的開始和結束日期是否不為空白。 如果前面找到的價目表，其開始和結束日期為空白時，您就找到了問題所在。 
- 記下時間銷售實際值的開始日期欄位，並檢查任何找到的價目表是否適用於該日期。 例如，時間銷售實際值的日期應落在價目表的開始日期和結束日期之內。 
    - 如果時間銷售實際值上沒有任何涵蓋該日期的價目表，您就找到了問題所在。 修改價目表的開始和結束日期，以確保價目表涵蓋時間銷售實際值的日期。 
    - 如果時間銷售實際值上有多份涵蓋該日期的價目表，您就找到了問題所在。 您可以修正此問題，做法為編輯價目表的開始和結束日期，只留下一份涵蓋時間銷售實際值日期的價目表。 
    - 如果只有一份價目表涵蓋時間銷售實際值的那個日期，請移至「檢查 3」。
完成必要的修正之後，請重新建立時間項目、加以核准，並確認時間銷售實際值顯示有效的價格。

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>檢查 3：時間銷售實際值的定價維度價目表中是否有價格？

如果您已順利完成「檢查 1」和「檢查 2」，現在應該只有一份適用於時間銷售實際值日期的價目表。 開啟這份價目表，並瀏覽至 [角色價格] 索引標籤。確定時間銷售實際值上有一列資料在定價維度的網格中。

如果時間銷售實際值上沒有任何資料列在定價維度的角色價格網格中，您就找到了問題所在。 在時間銷售實際值上的定價維度的 [角色價格] 網格中建立一列。 完成此動作之後，請重新建立時間項目、加以核准，並確認時間銷售實際值顯示有效的價格。

如果依照上述三項檢查執行後，時間銷售實際值上仍未看到有效價格，請記入支援票證。 

