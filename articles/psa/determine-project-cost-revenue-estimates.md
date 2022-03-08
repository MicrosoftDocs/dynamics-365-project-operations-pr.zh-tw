---
title: 決定專案成本與營收預估值
description: 如何決定 Project Service 中的專案成本與營收預估值
author: ruhercul
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 38de99680f4ba67b8eb593ec575c2a796fcfb59436fea5323dd1d86d7cf3d797
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002591"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>決定專案成本與營收預估值 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

專案預估值為專案的分工結構圖中預估和排程的工作提供財務檢視表。 估計值檢視表會通知您規劃的工作對成本和營收的影響。 估計值檢視表提供一項工具，可查看許多預先定義維度的資訊，以便通知您專案的財務影響。  
  
## <a name="cost-and-sales-value-of-the-project"></a>專案的成本和銷售值  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]價目表定義角色專案使用的成本與帳單費率。 根據與專案的分工結構圖中的工作相關的角色，您可以判斷所涉及工作的成本與營收影響。  
  
## <a name="cost-price-defaulting"></a>預設成本價  
每一個專案都屬於組織 (在專案的 **擁有單位** 中指出)。 與擁有組織單位相關的價目表決定成本單價。 [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]決定角色的成本價，藉由搜尋成本價目表中角色、單位和組織單位的組合，取得估計明細生效日期的正確成本價。  
  
如果角色、單位與組織單位的組合未從擁有單位的價目表產生成本價，則會忽略單位，而採納角色和組織單位的組合。 如果有成本價，此價格會轉換成您在估計明細上選擇的單位。  
  
如果角色和組織單位的組合未產生成本價，則會忽略組織單位，而採納角色和單位的組合，如有需要，還會在套用任何轉換之後設定預設價格。  
  
 如果該角色沒有價格，則估計明細中的成本價會預設為 0.00。  
  
 在專案成本估計明細上的所有成本金額都是採用擁有組織單位的貨幣。  
  
## <a name="sales-price-defaulting"></a>預設售價  
銷售價目表是根據專案附屬的銷售實體而定。 與報價或合約相關的銷售價目表決定銷售單價。 如果報價或合約有自訂價目表，這就是專案估計值的預設銷售價目表。 如果與銷售實體沒有關聯，則在參數設定中設定的預設銷售價目表會是專案的預設銷售價目表。 每個估計明細都有相關的資源組織單位，表示將從中預約資源來完成工作的組織單位。 相關角色的售價的決定方式，是藉由搜尋銷售價目表中角色、單位和資源單位的組合，取得估計明細生效日期的正確售價。  
  
如果角色、單位和資源組織單位的組合未從銷售價目表產生售價，系統將忽略單位，並搜尋角色和資源組織單位的組合。 如果找到售價，則將其轉換為您在銷售估計明細上選擇的單位。  
  
如果系統未找到角色的價格，則估計明細中的售價必須預設為 0.00。  
  
估計值檢視表包含網格檢視表，會顯示估計明細的固定網格，當中包含單位和總成本和售價。  
  
## <a name="time-phased-view-of-project-estimates"></a>專案估計值的分時期檢視表  
在專案估計值的分時期檢視表中，根據預設網格檢視表中的估計值資料會依角色進行樞紐分析，並顯示估計值資料散佈在所選擇時幅的時間表上。  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>根據工作模式的努力估計值配置  
在分時期檢視表中，估計投入工作的總努力程度會藉由配置每單位所選擇時幅的時段的特定努力時數分散。 在 Project Service 中，工作模式決定努力在工作期間的配置方式。 兩種配置方式分別是平均配置和根據配置的工作時數。 
  
## <a name="work-hours-based-allocation"></a>根據工作時數配置  
工作的自動排程工作模式會控制對工作估計的資源數，這些資源估計為在每天的完整工作時數期間利用。 這也適用於配置努力，將它分割到分時期檢視表中各項工作的期間。 例如，在「天」時幅，用於估計由一個資源完成的工作，每天配置的努力將不會超過專案行事曆中定義的每天工作時數。 因此，努力配置永遠可確保資源估計為整天使用。  
  
## <a name="even-distribution"></a>平均分佈  
手動排程工作模式不會採用工作時數、專案行事曆，或工作上定義的資源數。 工作排程是根據使用者輸入而定。 對於這類工作，所選擇時幅的每單位時段的努力配置沒有任何限制因素。 投入工作的總努力程度會平均分割，並配置給所選擇時幅的每單位時段。  
  
如此一來，工作上定義的工作模式會決定分時期估計值中，每單位時段的努力分佈或努力配置。  
  
## <a name="grouping-and-time-phasing-options"></a>分組和分時期選項  
此檢視表可協助您了解以每天、每週、每個月或每年為基礎的努力、成本和銷售估計值的分佈。 [群組依據] 選項可在另外兩個維度上樞紐分析估計值資料：類別及資源。 在網格檢視表和分時期檢視表上，您都可以選擇要顯示的欄位。 每個時間區塊的總計會顯示在底部，指出日、週、月或年的總估計投入量、成本和銷售。  
  
成本價和銷售價預設值是在有效期限內。 角色的費率變更時，它在分時期檢視表中將會更透明，當檢視「資源」上樞紐分析的且依週分時期的估計值資料時。  
  
## <a name="expense-estimates"></a>費用估計值  
任何在專案中所產生並非直接與所要擴充人力相關的費用，都可以記錄在網格檢視表的專案估計值中。 使用網格檢視表中的 **新增費用估計值** 選項，就可以完成這項操作。 您可以記錄特定工作或整個專案的費用估計值。 您可以選擇這些明細上的費用類別，並在預計要產生費用時選擇暫定日期。 如果相關的成本和銷售價目表有預設的價格，或針對費用類別定義的加成百分比，它會在估計明細上依關聯預設。  
  
### <a name="see-also"></a>請參閱  
 [專案經理指南](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]