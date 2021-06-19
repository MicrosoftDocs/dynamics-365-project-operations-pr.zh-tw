---
title: 啟用 Project Finder Mobile 應用程式功能
description: 如何啟用 Project Service 的 Project Finder Mobile 應用程式功能
author: JohnPBurrows
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
ms.openlocfilehash: f068c32ac957dc5921ccabc989b3b7a347585c19
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007716"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>啟用 Project Finder Mobile 應用程式功能 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

您的資源可以透過 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 使用手機上的 Project Finder Mobile 應用程式，尋找新專案進行處理及更新其技能集。  
  
 應用程式適用於 [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]、[!INCLUDE[tn_android](../includes/tn-android.md)] 手機和 [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]。  
    
 若要允許使用者檢視專案資源需求並更新技能，您必須在組織單位的參數設定中選取選項。
  
> [!NOTE]
>  Project Finder Mobile 應用程式僅適用於 [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)]，無法搭配內部部署安裝使用。  
  
1. 移至 **Project Service > 參數**。  
  
2. 按一下您要使用的參數設定，允許 Project Finder Mobile 應用程式功能。  
  
3. 在 **一般** 區域中，將 **資源看得到資源需求** 設定為 **是**。  
  
4. 將 **允許資源更新技能** 設定為 **是**。  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   這是全域設定。 專案經理可以設定個別專案是否可在該專案的 **專案團隊** 頁面上看見。  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>電子郵件通知  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]會傳送關於資源要求的電子郵件給下列收件者，於下列時機：  
  
|收件者|活動|  
|---------------|-----------|  
|專案經理|- 資源使用 Project Finder Mobile 應用程式註冊專案。|  
|資源|- 資源註冊的專案工作已由另一個資源履行。<br />- 其技能核准要求已核准或遭拒。<br />- 專案註冊要求已核准或遭拒。|  
  
## <a name="privacy-notice"></a>隱私權通知  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>請參閱  
 [設定資源](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]