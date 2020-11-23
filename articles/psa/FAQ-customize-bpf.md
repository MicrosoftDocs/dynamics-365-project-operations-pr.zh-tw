---
title: 如何自訂專案階段商務程序流程？
description: 有關如何自訂專案階段商務程序流程的概觀。
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125019"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>如何自訂專案階段商務程序流程？
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

舊版 Project Service 應用程式有一個已知的限制，也就是專案階段商務程序流程中的階段名稱必須與預期的英文名稱 (**Quote**、**Plan**、**Close**) 完全相符。 否則，需要使用英文階段名稱的商務規則就無法如預期般運作。 這正是您在專案表單上看不到熟悉的動作 (例如 **切換程序** 或 **編輯程序**)，而且也不建議自訂商務程序流程的原因。 

版本 2.4.5.48 及更新版本已解決這項限制。 如果您需要針對舊版自訂預設商務程序流程，本文有提供建議的因應措施。  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>商務規則必須與英文階段名稱完全相符

專案階段商務程序流程包含推動應用程式中下列行為的商務規則：
- 當專案與報價有關聯時，程式碼會將商務程序流程設定為 **Quote** 階段。
- 當專案與合約有關聯時，程式碼會將商務程序流程設定為 **Plan** 階段。
- 商務程序流程進展到 **Close** 階段時，專案記錄會停用。 停用專案時，系統會將專案表單和分工結構圖 (WBS) 設定為唯讀、將具名資源預約釋出，以及停用任何相關聯的價目表。

此商務規則必須使用專案階段的英文名稱。 這項對英文階段名稱的相依性就是我們為何不鼓勵自訂專案階段商務程序流程，以及您為何在專案實體上看不到常見商務程序流程動作 (如 **切換程序** 或 **編輯程序**) 的主要原因。

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>如果階段名稱與英文名稱不相符，會發生什麼情況？

在 8.2 平台的 Project Service 應用程式 1.x 版中，當商務程序流程中的階段名稱與英文名稱不完全相符時，會將設定報價或合約正確階段或關閉專案的商務規則略過。 不會顯示任何錯誤訊息。 因此，您似乎可以自訂專案階段商務程序流程。 然而，您不會看到任何處理報價、合約及專案的自動程序關閉。

在 9.0 平台的 Project Service 應用程式 2.4.4.30 版或更早版本中，商務程序流程發生了重大架構變更，而這需要改寫商務程序流程商務規則。 如此一來，要是程序階段名稱不符合預期的英文名稱，您就會收到錯誤訊息。 

因此，如果您想要自訂專案實體的專案階段商務程序流程，就只能將全新階段新增至專案實體的預設商務程序流程，同時讓 **報價**、**計劃** 和 **關閉** 階段保持原樣。 此限制可確保您不會從預期要在商務程序流程中使用英文階段名稱的商務規則上收到錯誤訊息。

在版本 2.4.5.48 或更新版本中，本文所述的商務規則已從專案實體的預設商務程序流程中移除。 升級至該版本或更新版本將可讓您自訂商務程序流程，或以您自己的商務程序流程來取代預設的。 

## <a name="workarounds-for-earlier-versions"></a>舊版適用的因應措施

如果您不考慮升級，則可以透過下列兩種方式之一來自訂專案實體的專案階段商務程序流程：

1. 新增其他階段至預設設定，同時保留 **報價**、**計劃** 和 **關閉** 的英文階段名稱。


![將階段新增至預設設定的螢幕擷取畫面](media/FAQ-Customize-BPF-1.png)
 
2. 建立您自己的商務程序流程，並將其設為專案實體的主要商務程序流程，這樣即可讓您使用任何您想要的階段名稱。 不過，如果您想要使用相同的標準專案階段 **報價**、**計劃** 和 **關閉**，就必須進行一些會移除自訂階段名稱的自訂。 較複雜的邏輯是在專案結尾的部分，您仍然可以只是藉由停用專案記錄來觸發。

![BPF 自訂](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>對於 9.0 平台的 Project Service 應用程式 2.4.4.30 版或更早版本的其他考量

在 9.0 平台的 Project Service 應用程式 2.4.4.30 版或更早版本中，**依階段的專案** 圖表及專案清單檢視表中所用專案實體上的 **階段名稱** 欄位不會隨自訂商務程序流程一併更新，因為該欄位與預設專案階段商務程序流程相聯繫。 您可以透過下列步驟解決此問題：

- 新增自訂欄位，以擷取目前隨著使用者進展通過自訂商務程序流程而更新的商務程序流程階段。

- 將 **依階段的專案** 圖表修改為使用自訂欄位，而不使用預設設定。

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>自行建立專案實體的商務程序流程的步驟

若要自行建立專案實體的商務程序流程，請執行下列動作：

1. 移至 **設定** > **程序中心**。 不要複製專案階段商務程序流程，因為這樣也會複製 Project Service 商務規則。

  ![建立程序](media/FAQ-Customize-BPF-3.png)

2. 使用程序設計師來建立您想要的階段名稱。 如果您想要使用與 **報價**、**計劃** 及 **關閉** 預設階段相同的功能，就必須以您的自訂商務程序流程的階段名稱為基礎建立該功能。

   ![用來自訂 BPF 的程序設計師螢幕擷取畫面](media/FAQ-Customize-BPF-4.png) 

3. 在程序設計師中，按一下 **程序流程順序**，向上移動自訂商務程序流程超過專案階段商務程序流程以至清單頂端，藉此將其設為專案實體的主要業務程序流程。


   [使用程序流程順序的螢幕擷取畫面](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>下列步驟適用於 9.0 平台的 Project Service 應用程式 2.4.4.30 版或更早版本

4. 將新的自訂欄位新增至專案實體，以擷取自訂商務程序流程中的自訂階段。 當自訂商務程序流程上的階段更新時，您必須新增商務規則 (外掛程式/工作流程)，才能更新此欄位。

   ![自訂專案實體的螢幕擷取畫面](media/FAQ-Customize-BPF-6-720.png)

5. 將 **依階段的專案** 圖表修改為使用階段的新自訂欄位。

   ![使用 [依階段的專案] 圖表的螢幕擷取畫面](media/FAQ-Customize-BPF-7-720.png)

6. 將專案實體的任何檢視表修改為使用階段的新自訂欄位。

   ![修改專案實體的檢視表的螢幕擷取畫面](media/FAQ-Customize-BPF-8-720.png)

