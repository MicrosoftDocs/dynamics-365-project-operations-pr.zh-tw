---
title: 升級考量 - 從 Microsoft Dynamics 365 Project Service Automation 2.x 或 1.x 版升級至版本 3
description: 本主題提供有關從 Project Service Automation 2.x 或 1.x 版升級至版本 3 時必須進行考量的資訊。
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c0c1e07bacb4867254a12436cf3bff58989e117f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144142"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>升級考量 - 從 PSA 2.x 或 1.x 版升級至版本 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation 和 Field Service
Dynamics 365 Project Service Automation 和 Dynamics 365 Field Service 都會使用 Universal Resourcing Scheduling (URS) 解決方案來進行資源排程。 如果您的執行個體中有 Project Service Automation 和 Field Service，請將這兩個解決方案升級至最新版本。 Project Service Automation 的最新版本是 3.x 版。 Field Service 的是 8.x 版。 升級 Project Service Automation 或 Field Service 時，將會安裝最新版本的 URS。 如果同一個執行個體中的 Project Service Automation 和 Field Service 解決方案都未升級至最新版本，可能會出現一些不一致的行為。

## <a name="resource-assignments"></a>資源指派
在 Project Service Automation 版本 2 和版本 1 中，工作指派已儲存為 **工作實體** 中的下層工作 (也稱為明細工作)，並且與 **資源指派** 實體間接相關。 明細工作過去可在分工結構圖 (WBS) 的指派快顯視窗中看到。

![Project Service Automation 版本 2 和版本 1 中 WBS 上的明細工作](media/upgrade-line-task-01.png)

在 Project Service Automation 版本 3 中，將可預約資源指派給工作的結構描述已變更。 明細工作已被取代，而且 **工作實體** 的工作與 **資源指派** 實體的團隊成員之間有直接 1:1 關聯。 指派給專案團隊成員的工作現在會直接儲存在資源指派實體中。  

這些變更會影響所有在專案團隊上有具名可預約資源及一般資源之資源指派的現有專案升級。 這主題提供當您將專案升級至版本 3 時，需要納入考量的注意事項。 

### <a name="tasks-assigned-to-named-resources"></a>已指派給具名資源的工作
版本 2 和版本 1 中的工作使用基礎工作實體，讓團隊成員可以描繪其預設定義角色以外的角色。 例如，可將預設獲指派「方案經理」角色的蔡美雪指派至具有開發人員角色的工作。 在版本 3 中，具名團隊成員的角色一律是預設，因此任何指派給美雪的工作都會使用她的方案經理預設角色。

如果您已將資源指派給版本 2 和版本 1 中預設角色以外的工作，當您升級時，不論版本 2 中的角色指派如何，都會將所有工作指派的預設角色指派給具名資源。 這個指派讓計算的估計值在版本 2 或版本 1 到版本 3 之間產生差異，因為估計值是根據資源的角色而非明細工作指派所計算得出。 例如，在版本 2 中，已將兩項工作指派給呂麗華。 工作 1 的明細工作角色是開發人員，而為工作 2 的是方案經理。 呂麗華會有方案經理的預設角色。

![多個指派給一個資源的角色](media/upgrade-multiple-roles-02.png)

因為開發人員與方案經理的角色不同，成本與銷售估計值如下：

![資源角色的成本估計值](media/upggrade-cost-estimates-03.png)

![資源角色的銷售估計值](media/upgrade-sales-estimates-04.png)

升級至版本 3 時，明細工作會取代為可預約資源團隊成員工作上的資源指派。 指派將會使用可預約資源的預設角色。 在下圖中，角色為方案經理的呂麗華即是該資源。

![資源指派](media/resource-assignment-v2-05.png)

因為估計是根據資源的預設角色所計算，銷售和成本估計值可能會變更。 您已無法在下圖中看到 **開發人員** 角色，因為角色現在是取自可預約資源的預設角色。

![預設角色的成本估計值](media/resource-assignment-cost-estimate-06.png)
![預設角色的銷售估計值](media/resource-assignment-sales-estimate-07.png)

升級完成之後，您可以將團隊成員的角色編輯成所指派預設值以外的角色。 不過，如果您變更團隊成員角色，就會在團隊成員所有已獲指派的工作上變更該角色，因為版本 3 無法將多個角色指派給團隊成員。

![更新資源角色](media/resource-role-assignment-08.png)

當您將資源的組織單位從預設值變更為其他組織單位時，已指派給具名資源的明細工作也會如此。 版本 3 升級完成後，指派將會使用的是資源的預設組織單位，而不是在明細工作中設定的組織單位。

### <a name="tasks-assigned-to-generic-resources"></a>已指派給一般資源的工作
在版本 2 和版本 1 中，您可以在工作中設定角色和組織單位，然後使用 **產生團隊** 功能，根據工作中設定的屬性來產生一般資源。 在版本 3 中，您會建立具有角色和組織單位的一般團隊成員，然後再將團隊成員指派給工作。

在版本 2 和版本 1 中，具有一般資源的專案在工作層級可能會有兩種狀態或兩者的混合。 例如，您可能會遇到下列情況：

- 工作已設定角色和組織單位，但尚未產生任何附屬的資源指派。
- 工作具有透過使用 **產生團隊** 功能建立一般資源方式所指派的一般團隊成員資源指派。

開始升級前，建議您針對每個已將工作指派給一般資源，或者尚未據以執行產生團隊程序的專案，重新產生團隊。

對於已指派給透過 **產生團隊** 所產生之一般團隊成員的工作，升級將會保留團隊中的一般資源，並保留對該一般團隊成員的指派。 我們建議您在升級後，但在預約或送出資源要求前，為一般團隊成員產生資源需求。 這會在與專案承包組織單位不同的一般團隊成員上保留任何組織單位指派。

例如，在 Project Z 專案中，承包組織單位為 Contoso US。 在專案計劃中，已將 [技術顧問] 角色指派給實作階段中的測試工作，而指派的組織單位是 Contoso India。

![實作階段組織指派](media/org-unit-assignment-09.png)

實作階段之後，將整合測試工作指派給 [技術顧問] 角色，但是組織是設定為 Contoso US。  

![整合測試工作組織指派](media/org-unit-generate-team-10.png)

當您為專案產生團隊時，會建立兩個一般團隊成員，因為工作上有不同的組織單位。 技術顧問 1 會指派給 Contoso India 工作，而技術顧問 2 則有 Contoso US 工作。  

![產生的一般團隊成員](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> 在 Project Service Automation 版本 2 和版本 1 中，團隊成員不會保留明細工作上所維護的組織單位。

![Project Service Automation 中的版本 2 和版本 1 明細工作](media/line-tasks-12.png)

您可以在估計值檢視表上查看組織單位。 

![組織單位估計值](media/org-unit-estimates-view-13.png)
 
升級完成時，與一般團隊成員對應之明細工作中的組織單位會新增至一般團隊成員，並移除該明細工作。 因此，建議您在升級前，為每個包含一般資源的專案產生或重新產生團隊。

對於已指派給組織單位不同於承包專案組織單位的角色且尚未產生團隊的工作，升級將會為該角色建立一般團隊成員，但會使用專案的承包單位做為團隊成員的組織單位。 回顧一下 Project Z 的範例，已將技術顧問角色指派給承包組織單位 Contoso US 以及實作階段中的專案計劃測試工作，並已將組織單位指派給 Contoso India。 已將實作階段之後完成的整合測試工作指派給 [技術顧問] 角色。 組織單位是 Contoso US，而且尚未產生團隊。 升級會建立一個一般團隊成員 (技術顧問，其所有三個工作都已指派時數) 和一個組織單位 Contoso US (專案的承包組織單位)。   
 
在未產生的團隊成員上變更不同資源分配組織單位的預設值，正是我們建議下列作法的原因：您應該在升級之前，針對每個包含一般資源的專案產生或重新產生團隊，以免組織單位指派遺失。

