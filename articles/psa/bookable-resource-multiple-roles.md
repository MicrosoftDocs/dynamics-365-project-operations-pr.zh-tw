---
title: 在可預約資源擔任專案的多個角色時，估計專案銷售和成本
description: 本主題提供相關資訊，說明如何使用定價維度支援專案中擔任多個角色之資源的定價和成本計算。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: be24bb3bdf2f3c8351fc396ae67457b5213e1cd800e9d2ad23d59d0d038f22b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987471"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>在可預約資源擔任專案的多個角色時，估計專案銷售和成本 

[!include [banner](../includes/psa-now-project-operations.md)]

專案型公司通常需要一個資源在專案上扮演多個角色。 其中每一個角色都可以用不同方式進行定價和成本計算，這表示視每個角色的帳單及成本費率而定，專案上同一個資源的工時會得出不同的財務估計值。 Project Service Automation 允許對具名資源的團隊成員記錄進行值設定，並允許每個指派至團隊成員的工作有不同的覆寫值。

下列範例說明簡單覆寫這個值，如何能讓資源在專案上擁有多個使用不同成本及帳單費率的角色。

## <a name="create-tasks"></a>建立工作
建立兩個各有時數為 40 小時的專案工作：工作 A 和工作 B。選取工作 A 做為工作 B 的前置任務。

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>設定一般專案團隊成員的角色與組織單位

1. 在 **排程** 頁面上，選取工作 A 的 **工作** 列。 
2. 在 **資源** 欄位中，選取下拉式清單中的 **建立**。
3. 在 **團隊成員快速建立** 頁面上，指定可執行此工作之一般團隊成員的屬性。
4. 選取適當的角色與組織單位，然後選取 **儲存後關閉**。 隨即會建立一般團隊成員，並將其指派至此工作。 

對工作 B 重複這些步驟，並確定工作 B 與工作 A 所建立的一般團隊成員，其角色及組織單位各不相同。 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>設定一般專案的角色及組織單位

1. 建立工作 A 之後，選取該工作，然後選取 **編輯工作**。
2. 在 **工作詳細資料** 頁面上，尋找 **角色** 和 **組織單位** 欄位，並新增執行此工作之資源所需的值。 

  > [!NOTE]
  > 如果您要使用 Project Service Automation 示範資料來完成此案例，請為角色選取 **諮詢主管**，並選取 **Fabrikam US** 做為組織單位。

3. 選取工作 B，然後選取 **編輯工作**。
4. 在 **工作詳細資料** 頁面上，尋找 **角色** 和 **組織單位** 欄位，並新增執行此工作之資源所需的值。 請確定工作 B 與工作 A 在 **角色** 及 **組織單位** 欄位中的值不相同。 

  > [!NOTE]
  > 如果您要使用 Project Service Automation 示範資料來完成此案例，請為角色選取 **網路技術人員**，並選取 **Fabrikam US** 做為組織單位。

5. 儲存並關閉 **工作詳細資料** 頁面。 

## <a name="team-member-and-estimates-behavior"></a>團隊成員和估計行為 

1. 在 **工作詳細資料** 頁面的 **團隊成員** 上，選取兩個一般團隊成員，然後選取 **產生需求**。 
2. 選取 **諮詢主管** 的團隊成員列 ，然後選取 **預約**。 排程面板會開啟，並將資源預約給該需求。
3. 選取 **網路技術人員** 的團隊成員列 ，然後選取 **預約**。 排程面板會開啟，並預約該需求上的相同資源。

### <a name="team-member-grid"></a>團隊成員網格 
在 **團隊成員** 網格上，您會發現已刪除這兩個一般團隊成員記錄，而且已取代其中一個資源。 該資源有一組值，會顯示一組預設的 **角色** 及 **組織單位** 值。
展開該團隊成員記錄的列時，您可以在這兩個工作的團隊成員記錄中看到不同的指派。 每個指派列在 **角色** 和 **組織單位** 中都會有工作特定的值。 

### <a name="estimates-grid"></a>估計值網格 
瀏覽至 **估計值** 網格時，您會發現同一個資源的這兩個指派各以不同的方式進行定價。
工作 A 的資源指派是使用 **諮詢主管** 的 **角色** 屬性值來定價。 同一個資源在工作 B 上的指派是使用 **網路技術人員** 的 **角色** 屬性值來定價。



[!INCLUDE[footer-include](../includes/footer-banner.md)]