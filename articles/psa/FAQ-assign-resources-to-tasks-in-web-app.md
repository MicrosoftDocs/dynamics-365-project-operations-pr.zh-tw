---
title: 如何在 Web 應用程式中將可預約資源指派給工作
description: 有關如何指派可預約資源的概觀。
author: JohnPBurrows
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
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286283"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>如何在 Web 應用程式 (Project Service 應用程式 2.x 版) 中將可預約資源指派給工作？

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

有兩種方法可以在 Project Service 中指派資源給工作。 您可以預約資源做為團隊成員，再將該資源指派給工作。 或者，也可以在工作上透過角色指派建立一般團隊成員、產生團隊，然後使用具名資源履行支援需求。

請注意，如果您想要將可預約資源指派給工作，則可預約資源團隊成員必須足夠的可用預約。 預約的狀態必須是 [認可類型為已確認預約] 和 [狀態已認可]。 如果資源沒有足夠的預約，Project Service 就會移除指派，並顯示下列錯誤訊息：

*無法指派資源給工作 - 下列資源對專案沒有充足的預約時數*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>預約資源做為團隊成員，再將該資源指派給工作

您可以使用此方法，將資源新增至專案團隊，然後將工作指派給專案排程中的資源。 以下說明如何執行此動作：
1.  在團隊成員網格中，選取 **新增** 以將新的團隊成員加入。
2.  在 [團隊成員快速建立] 畫面中，選取可預約資源名稱並設定角色。
3.  選取 **開始** 和 **結束** 日期。

    > [!div class="mx-imgBorder"] 
    > ![新增團隊成員的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-1.png "新增團隊成員的螢幕擷取畫面")
 
4.  選取下列其中一個配置方法以進行資源預約：
    - **完整產能** 會預約資源在指定之開始和結束日期的完整產能。
    - **產能百分比** 會預約資源在指定之開始和結束日期一定百分比資源的產能。
    - **依時數平均分配** 會預約指定時數的資源，並在指定之開始和結束日期內平均分配每日的時數。
    - **依時數前重後輕** 會預約指定時數的資源，並在指定之開始和結束日期內以前重後輕的方式分配每日的時數。

    不要選取 **無**，因為這會將資源新增至團隊，但不會建立任何吸收資源產能的預約。
5.  選取 **儲存**。

    請注意，預約的時數必須足以涵蓋獲指派此資源之工作的努力時數和日期範圍。 如果其間有不一致的情況，就無法將資源指派給工作。

6.  在工作的分工結構圖 (WBS) 上，按一下資源儲存格下拉式清單。 接下來： 

    1. 選取 **新增**。
    2. 選取 **資源** 下方的下拉式清單，並選取您先前新增的團隊成員。
    3. 選取 **確定**。 團隊成員現在已指派給工作。

    > [!div class="mx-imgBorder"] 
    > ![透過 WBS 新增資源的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-2.png "透過 WBS 新增資源的螢幕擷取畫面")
 
在團隊成員網格中，您會在 [指派的時數] 底下看到資源指派時數的彙總。 這會小於或等於資源的預約時數。 

> [!div class="mx-imgBorder"] 
> ![資源指派時數的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-3.png "資源指派時數的螢幕擷取畫面")
 
如果您嘗試指派給資源的工作是在資源預約的結束日期之後開始，則該資源不會出現在下拉式清單中。

請注意，如果資源還剩餘一些未指派的產能，您可以將資源指派給較其預約時數更多的時數。 在這種情況下，只會部分指派資源，最多以其預約數為限。 您可將 [無配置人員的時數] 欄新增至分工結構圖，以查看這些剩餘未指派的工作時數。

如果資源已指派給其預約時數 (其預約時數等於其指派時數)，您將會在嘗試將這些時數指派給更多工作時看到下列錯誤訊息：

*無法指派資源給工作 - 下列資源對專案沒有充足的預約時數。*

此外，還會在沒有任何預約的情況下新增您建立專案時所新增至團隊的預設專案經理團隊成員，而此成員也無法指派給任何工作。 這些成員不會顯示在工作的資源下拉式清單中。

如果您想要指派此資源，就必須將這些資源從團隊移除，然後使用 [無] 以外的配置方法重新加入團隊中。 建立專案時將這些資源新增至團隊的原因是，為了讓專案預設會有至少一個專案核准者。

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>透過在工作上指派角色建立一般團隊成員

此方法可確保資源有足夠的預約提供給工作。 首先，您可在指派角色給工作後產生團隊，以建立描述您最終要在工作上使用之具名資源特性的預留位置或一般資源。 以下說明如何執行此動作：

1. 在分工結構圖中，選取一項工作。
2. 選取資源儲存格中的 **指派的角色** 下拉式清單圖示。
3. 選取 **角色** 下拉式清單，並為一般資源選取角色。
4. 選取 **確定**。

    > [!div class="mx-imgBorder"] 
    > ![使用 WBS 新增資源的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-4.png "使用 WBS 新增資源的螢幕擷取畫面")
 
當您完成指派角色給 WBS 中的工作後，選取 **產生專案團隊**。 Project Service 會彙總工作指派，以根據角色、資源分配組織單位和專案行事曆，建立最小數目的一般團隊成員。

> [!div class="mx-imgBorder"] 
> ![產生專案團隊的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-5.png "產生專案團隊的螢幕擷取畫面")
 
在 [團隊成員] 網格中，您會看到包含角色及位置名稱且類型為 [一般資源] 的資源。 如果一個角色需要兩項資源才能完成工作，[產生團隊] 功能就會建立兩個團隊成員，並使用位置名稱來區別這些成員。

> [!div class="mx-imgBorder"] 
> ![新增兩項一般資源的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-6.png "新增兩項一般資源的螢幕擷取畫面")
 
您可選取 [資源需求] 下方的連結，以開啟一般團隊成員的支援資源需求。

> [!div class="mx-imgBorder"] 
> ![開啟支援資源需求的螢幕擷取畫面](media/FAQ-Resources-to-Tasks2-7.png "開啟支援資源需求的螢幕擷取畫面")

選取一般資源的 **預約**，然後您就可以使用排程面板來尋找並預訂實際資源。 您也可以選取 **送出要求**，送出要求資源管理員履行的需求。

使用具名資源履行一般資源時，一般資源將會從團隊中移除，而且一般資源的工作指派會指派給履行一般資源之資源需求的具名資源。
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]