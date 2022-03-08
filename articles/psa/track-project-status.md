---
title: 追蹤專案狀態
description: 如何追蹤 Project Service 中的專案狀態
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
ms.openlocfilehash: 32e5867a773206aaed532645302b7f7cc789d5074f9acdb3bbb95acf8492d25e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996696"
---
# <a name="track-a-projects-status-project-service"></a>追蹤專案狀態 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

使用 [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]追蹤客戶專案的進度。  

做為互動進度，專案階段會更新以反映互動的階段：  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **新增**    | 當您建立專案時，階段會設為 **新**。 如果您從範本建立專案，在此階段專案可能會有排程、估計值和團隊資料。 否則，它會是專案的簡述，而您需要手動輸入專案元件的其餘部分。 |
|  **報價**   |      當您將專案與報價建立關聯或從報價建立專案時，專案階段會設為 **報價**，且估計的開始和結束日期也會更新。 當專案處於報價階段時，報價上的詳細資料會顯示在 **專案** 頁面的 **銷售** 索引標籤上。      |
|   **計劃**   |                                     當您的專案報價成交，且互動進度來到合約階段時，專案階段會更新為 **計劃**。 合約詳細資料會顯示在 **專案** 頁面的 **銷售** 索引標籤上。                                      |
| **完成** |                    當專案工作完成時，您可以將階段轉換成 **完成**。 專案階段設定為完成時，表示工作已 100% 完成，但專案仍未結案，以便記錄任何剩餘時間或費用項目。                     |
|  **關閉**   |           當所有交易都已記錄在專案上，且不會再有任何需要記錄的項目時，您可以手動設定階段為 **結案**。 當專案設定為 **結案** 時，您就無法再於專案上記錄任何交易，且專案將變成唯讀。           |

## <a name="to-track-a-projects-status"></a>若要追蹤專案狀態  

1.  移至 **Project Service > 專案**。  

2.  按一下您要處理的專案。  

3.  在橫跨畫面頂端的列中，選取專案名稱旁的向下箭頭，然後按一下 **專案追蹤**。  

4.  在工作清單上方的下拉式清單中，選取 **努力追蹤** 或 **成本追蹤**。  

5.  按兩下任何工作進行編輯。 您也可以移動或調整甘特圖表中各列的大小，以變更工作的時間和進度。  

### <a name="see-also"></a>請參閱  
 [專案經理指南](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]