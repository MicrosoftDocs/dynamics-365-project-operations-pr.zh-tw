---
title: 在銷售處理期間提供專案的工作估計值
description: 如何在 Project Service 的銷售處理期間提供專案的工作估計值
author: ruhercul
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
ms.openlocfilehash: d1daff101f9f0342bb691253fee1290d2335318c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998221"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>在銷售處理期間提供專案的工作估計值 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

在銷售處理期間，您可以使用報價明細從頭計算出銷售估計值。 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] 中的[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]功能提供更科學且更決定性的方式擬訂銷售估計值，藉由在分工結構圖中細分工作項目和建立相關屬性的關聯供專案估計值使用。  
  
 當您成功銷售時，可以使用專案計劃中關聯的分工結構圖，視需要微調以順利完成您的專案。  
  
## <a name="link-a-project-to-a-quote-line"></a>連結專案與報價明細  
 建立專案為主的報價明細時，可以從報價明細建立新專案。 然後可以使用專案範本，這些範本是組織常用的預先設定標準專案計劃和財務估計值，或者過去專案的專案計劃和估計值複本。 當您建立專案時，選擇專案範本會提供微調專案規劃、估計值與角色需求的基礎。 透過從報價建立自己的專案，專案會自動與報價明細建立關聯。  
  
## <a name="project-estimate-components"></a>專案估計元件  
 專案中的分工結構圖提供細分工作的方式，會維護工作階層，以及指派完成每項工作所需的努力估計值。 您也可以將角色與工作建立關聯，以指出完成工作和排程所需的資源類型的估計值。  
  
 分工結構圖可幫助您判斷工作量和排程估計值。 根據預設，專案會使用您先前定義的預設價目表。 價目表中定義的成本和售價有助於判斷專案工作細項的財務估計值。  
  
 如果您的專案與報價相關，而報價的價目表與預設不同，則報價的價目表會用於財務估計值。  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>從專案將估計值匯入至報價  
 一旦專案中有專案估計值，就可以將這些估計值匯入報價明細中：  
  
-   在 **報價明細詳細資料** 中，按一下 **從估計值匯入**。 

-   選取要匯入依交易類型、角色或分工結構圖節點層級摘要的專案估計值。  
  
### <a name="see-also"></a>請參閱  
 [專案經理指南](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]