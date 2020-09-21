---
title: 建立專案範本
description: 如何建立 Project Service 中的專案範本
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749874"
---
# <a name="create-a-project-template-project-service"></a>建立專案範本 (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

專案範本節省您的時間，如果公司定期投標類似類型的專案。 它們為一種專案類型提供一組標準的角色和預估時數。 客戶經理和專案經理可以依據專案範本建立專案，或是複製專案範本並製作自己的範本。  
  
## <a name="components-of-project-template"></a>專案範本的元件
 專案範本包含三個元件：  
  
- **分工結構圖**：專案範本中的分工結構圖有一組與專案相同的元素。 您可以建立工作階層、關聯角色與工作、定義排程屬性、設定相依性，並檢視甘特圖中的所有資料。 專案範本中的分工結構圖也支援每項工作的工作模式。 建立工作排程時，專案範本和專案之間並無差異。  
  
- **專案估計值**：專案估計值在範本中與專案中的運作方式相同，除了預設成本和售價的價目表一律會預設[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]參數中定義的成本和銷售價目表。 其餘功能與專案中相同。  
  
- **專案團隊形成**：形成專案範本的專案團隊時，您無法預約範本中的具名資源。 您可以使用分工結構圖中的**產生專案團隊**產生一組一般資源。 您也可以為一般資源指定必要的技能和熟練度。 您無法將一般資源替代為專案範本中可預約的資源。  
  
## <a name="create-a-project-from-a-template"></a>從範本建立專案  
 您可以遵循下列方式從範本建立專案：  
  
-   從報價建立專案時，您可以從專案快速建立表單中選擇專案範本。  
  
-   按一下**新專案**建立專案時，專案表單會在您儲存記錄前顯示。 您可以從這裡按一下**挑選範本**欄位，從組織內預先定義的專案範本清單中選擇。  
  
-   按一下**專案範本**頁面上的**從範本建立專案**，可從範本建立專案。  
  
## <a name="copying-components-of-a-template-to-a-project"></a>將範本的元件複製到專案  
 當您將範本的元件複製到專案中時，應先了解幾件事情。  
  
 **複製分工結構圖**：當您從專案範本複製分工結構圖時，如果專案的專案行事曆與範本不同，則專案行事曆上的工作時數將會套用至工作的排程。 這會將排程調整為支援的專案行事曆。 同樣地，分工結構圖上的第一項工作會採用專案的開始日期，如此其餘工作階層排程就會依據範本的分工結構圖中指定的期間和相依性進行更新。  
  
 **複製專案估計值**：如果您跨專案估計明細複製，價目表就會根據成本價目表的專案和銷售價目表的客戶的擁有單位更新。 單位成本和售價是從專案上與銷售實體關聯的這些價目表決定。  
  
 **複製專案團隊**：您將專案團隊從範本複製到專案時，一般資源也會一併複製，還包括範本中定義的技能和熟練度。 一般資源指派也會維持與專案範本中一樣。  
  
### <a name="see-also"></a>請參閱  
 [專案經理指南](../project-service/project-manager-guide.md)
