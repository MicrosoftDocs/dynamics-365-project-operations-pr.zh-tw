---
title: 將具名可預約資源預約給專案團隊並指派工作
description: 本主題提供有關如何將具名資源預約給專案團隊以及將這些資源指派至工作的資訊。
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: e0f3957936e699fb2a9f570b9789924c55e12cc2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009336"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>將具名可預約資源預約給專案團隊並指派工作 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

您可以直接預約具名資源給團隊，以將此資源新增至團隊。 若要這麼做，請完成下列步驟。

1. 在 Project Service Automation 中，移至 **專案**，然後選取並開啟您要預約到的專案。
2. 在 **專案** 頁面的 **團隊** 索引標籤上，按一下 **新增**。 

![從團隊索引標籤新增團隊成員](media/RM-how-to-1.png)

3. 在 **快速建立專案團隊成員** 對話方塊中，選取可預約資源。 **角色** 欄位將會有資源的預設角色填入 (如果已指派此角色)。 您可以視需要變更角色。 
4. 選取需要資源的開始及結束日期，並選取資源產能的配置方法。 
5. 如果您要讓團隊成員成為專案核准者，請在 **專案核准者** 欄位中選取 **是**。 這表示團隊成員可以核准為此專案送出的時間和費用項目。 
6. 按一下 **儲存**。

![在快速建立表單上新增團隊成員](media/RM-how-to-2.png)


您現在可以將預約的資源指派給專案中的工作。 在 **專案** 頁面上，按一下 **排程** 索引標籤以將工作指派給新資源。 從工作網格中 **資源** 欄位啟動的資源選擇器將會顯示您可以選取的團隊成員。

![將團隊成員指派給排程索引標籤上的工作](media/RM-how-to-3.png)

在 Project Service Automation (PSA) 版本 3 中，資源預約和工作指派並非緊密聯繫。 這表示使用排程中的資源選擇器時，您可以將超過團隊成員預約對專案所能支援之時數的工作指派給該團隊成員。
您可以在 **團隊** 索引標籤或 **資源協調** 索引標籤上查看團隊成員預約與指派之間的差異。您也可以在更詳細的層級上協調資源預約與指派之間的差異。

![[資源協調] 索引標籤](media/RM-how-to-4.png)

您也可以使用 **排程** 索引標籤上的資源選擇器來搜尋和選取尚不屬於專案團隊的可預約資源。 這些資源會在資源選擇器中顯示為 **其他資源**。

![將非團隊成員資源指派給工作](media/RM-how-to-5.png)

這樣做時，資源會新增至專案團隊並指派給工作，但不會產生任何預約。

![有指派但無預約的團隊成員](media/RM-how-to-6.png)

您可以使用 **協調** 索引標籤的延長預約功能或是 **排程面板**，將資源的產能預約給專案。

![在資源協調索引標籤上，為團隊成員延長預約](media/RM-how-to-7.png)

在專案上預約您的團隊成員之後，您可以使用維護預約或直接使用排程面板來管理其預約。


[!INCLUDE[footer-include](../includes/footer-banner.md)]