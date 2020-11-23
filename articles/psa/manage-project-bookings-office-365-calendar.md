---
title: 管理 Office 365 行事曆中的專案和預約
description: 如何管理 Office 365 行事曆中的專案和預約
author: ruhercul
manager: kfend
ms.service: project-operations
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
- D365PS
- ProjectOperations
ms.openlocfilehash: 31ff541f5b817c29b162c38c282df8cfd866e375
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129038"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>管理行事曆中的專案和預約 (Project Service)

> [!Note]
> 取代：此功能已被取代，不再可用。

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

使用 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆，檢視私人約會、專案工作預約，以及現場服務工單指派。  
  
 所有一切都在同一個地方，方便您管理一天的工作。 您的會議、約會、預約及工作都可在 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆中處理。  
  
 如果您使用 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]，還可以在 Project Service 時間項目檢視表中輸入您的個人約會。 這可讓專案經理和資源管理員得知您是否有空處理專案。 它還能幫您節省時間，因為您不必重複輸入私人約會的資訊。 您只要從行事曆將私人約會匯入到 Project Service 時間項目檢視表即可。  
  
 您的行事曆會將今天到未來四週內的專案和工單預約同步。 此設定不可變更。  
  
 僅支援從 PSA 到 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆的單向同步處理。 您可以依相反順序進行同步處理。 
  
 若要了解如何使用 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆，請參閱[商務用 Outlook 網頁版中的行事曆](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)。  
  
## <a name="setup"></a>安裝程式  
 您需要先進行一些設定，才能在 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆上看見並管理您的預約。  
  
- 您必須有 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 全域管理員或系統管理員認證。  
  
- 您的系統管理員需要設定電子郵件伺服器設定檔，而且每個使用者都必須設定他們的信箱。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)][透過伺服器端同步處理設定電子郵件處理](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>開啟您的組織的同步處理 (系統管理員工作)  
  
1.  從主要功能表按一下 **設定** > **管理**。  
  
2.  按一下 **系統設定**。  
  
3.  按一下 **同步處理** 索引標籤。  
  
4.  在 **選取是否啟用同步處理資源預約** 底下，勾選 **與 Outlook 同步處理資源預約**。  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>開啟使用者設定檔的同步處理 (使用者工作)  
  
1.  按一下畫面右上角的 **設定** 按鈕。  
  
2.  按一下 **選項**。  
  
3.  按一下 **同步處理** 索引標籤。  
  
4.  在 **與 Outlook 同步處理資源預約** 底下，勾選 **與 Outlook 同步處理資源預約**。  
  
## <a name="import-your-personal-appointments-user-task"></a>匯入您的私人約會 (使用者工作)  
 您可以從行事曆將私人約會匯入到 Project Service Automation 時間項目檢視表即可。  
  
1. 開啟 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆，並按一下 **匯入資料**。  
  
2. 在 [篩選] 畫面中，選取 **來自 Exchange 的約會**，然後按一下 **套用**。  
  
3. 系統會將約會擷取到時間項目檢視表中，做為本週的建議項目。 若要新增其他週的項目，請按一下 **上一週** 或 **下一週**。  
  
4. 選取您要新增至 Project Service Automation 時間項目檢視表的約會。  
  
5. 在 **時間項目** 快顯方塊中，選取適當的選項，以將約會轉換成 Project Service Automation 時間項目檢視表。  
  
6. 按一下 **儲存**。  
  
### <a name="see-also"></a>請參閱  
 [時間、費用及共同作業指南](../psa/time-expense-collaboration-guide.md)
