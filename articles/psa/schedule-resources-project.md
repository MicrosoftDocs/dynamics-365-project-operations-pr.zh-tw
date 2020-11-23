---
title: 排程專案的資源
description: 如何在 Project Service 中排程專案的資源
author: JohnPBurrows
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1479bf920be897a6ee3498aada7a6c36692a01fc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132117"
---
# <a name="schedule-resources-for-a-project-project-service"></a>排程專案的資源 (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

您可以檢查資源可用性，以檢視資源預約的整體情況，或者您可以依技能、團隊、地點及其他選項篩選檢視。  
  
排程面板會顯示資源清單及其可用性。 選取檢視模式，依 **小時**、**日**、**週** 或 **月** 顯示可用性。  
  
在您使用排程面版之前，務必將它設定好。 如需詳細資訊，請參閱[設定排程面板 (Field Service 或 Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board)。
  
如果您使用的是舊版，請參閱[檢視資源可用性](../psa/view-resource-availability.md)以了解資源可用性。  

> [!IMPORTANT]
>  若要使用排程面板預約功能、地理編碼及位置服務，您需要開啟地圖。  
> 
> 1. 在主要功能表上，選取 **資源排程** > **管理**。  
> 2. 按一下 **排程參數**。  
> 3. 開啟記錄，然後向下捲動至 **Resource Scheduling Optimization** 區段。  
> 4. 在 **連線到地圖服務** 欄位中，選擇 **是**。  
> 5. 接受條款並儲存記錄。  
> 6. 在主要功能表上，選取 **Project Service** > **排程面板**。 在這裡，有數種不同方式可手動排程預約需求。 選擇適合您使用的方法。
  
## <a name="find-available-resources"></a>尋找可用資源

1.  在 **預約需求** 清單中，以滑鼠右鍵按一下未排程的預約，然後選擇下列其中一項︰  
  
- 選擇 **尋找可用性 - 目前資源**，從排程面板上的清單中尋找可用的資源。  
- 選擇 **尋找可用性 - 所有資源**，從系統中的資源尋找可用的資源。  
   > [!NOTE]
   >  當您這樣做時，篩選會顯示選取的預約需求的選項。  
  
2. 看到可用的時段時，以滑鼠右鍵按一下排程面板上的該時段，並選擇 **在這裡預約**。 或者，將預約需求拖曳到可用的時段。  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>使用每日檢視表預約資源，並尋找誰還能預約
  
1.  在排程面板上，選取 **檢視模式**，然後選取 **天**。  
  
    這會顯示資源每天預約的時數以及哪些天有空的網格檢視表。  
  
2.  按一下您想要預約的資源的名稱，然後選取 **預約**。  
  
3.  在 **資源預約 (建立)** 對話方塊中，選擇要預約資源來處理的專案，以及預約方法及開始和結束時間。  
  
4.  完成時，選取 **預約**。  
  
## <a name="view-to-the-schedule-board"></a>檢視排程面板
  
1.  從底部的清單中選取未排程的預約需求。  
  
2.  將預約需求拖曳至排程面板上可用的資源/時段。  
  
3.  完成時，選取 **預約**。  
  
### <a name="additional-resources"></a>其他資源  
 [資源管理員指南](../psa/resource-manager-guide.md)
