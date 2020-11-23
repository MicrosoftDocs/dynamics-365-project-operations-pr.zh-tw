---
title: 專案範本
description: 此主題提供有關如何使用專案範本進行快速專案設定的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122998"
---
# <a name="project-templates"></a>專案範本 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

專案範本是預先定義的架構，可協助您快速輕鬆地開始專案。 使用預先定義的範本，只需按一下即可建立新的專案。 至於專案，您必須定義專案範本的先決條件。 您必須為每個專案範本定義專案行事曆，而且必須在組織中預先定義角色和價目表，才能讓範本的元件具有實用的資料。

專案範本由三個元件組成：排程、專案估計值和專案團隊成員。

## <a name="schedule"></a>排程

專案範本的排程與專案的排程有相同的元素集合。 您可以建立工作階層、將角色與工作產生關聯、定義排程屬性，以及設定相依性。 專案範本中的排程還會支援個別工作的工作模式。 因此，它支援排程引擎。 您必須將專案行事曆與專案建立關聯。 建立作業排程時，專案範本和專案之間並無差異。

## <a name="project-estimates"></a>專案估計值

專案範本的專案估計值與專案的專案估計值有相同的運作方式。 不過，成本價和銷售價是從參數所定義的預設成本和銷售價目表中提取而來。

## <a name="creating-a-project-from-a-template"></a>從範本建立專案
 
有許多可以從專案範本建立專案的方法：

- 從報價建立專案時，您可以選取 **快速建立：專案** 對話方塊中的專案範本。

> ![[快速建立：專案] 對話方塊](media/project-11.png)

- 藉由選取 **新增專案** 建立專案時，**專案** 頁面會在儲存記錄之前出現。 在 **挑選範本** 欄位中，選取組織預先定義的其中一個專案範本。
- 使用 **範本實體** 頁面上的 **從範本建立專案**。

## <a name="copying-components-of-template-to-project"></a>將範本的元件複製到專案

將專案範本的元件複製到專案時，視專案中的設定而定，可能會發生一些覆寫。

### <a name="copying-the-schedule"></a>複製排程。

從專案範本複製排程時，如果專案的專案行事曆與範本的不同，則專案行事曆中的工作時數會套用至工作排程。 如此一來，將會調整排程以符合支援的專案行事曆。 同樣地，排程上的第一項工作會採用專案的開始日期，而階層其餘工作的排程則依據範本中指定的期間和相依性進行更新。 

### <a name="copying-project-estimates"></a>複製專案估計值 

在專案評估明細之間複製時，會更新價目表。 就成本價目表而言，這些更新是根據專案的擁有單位進行。 至於銷售價目表，則是根據客戶。 說到與銷售實體相關的專案，其單位成本和銷售價即是根據這些價目表來決定。

### <a name="copying-a-project-team"></a>複製專案團隊

將專案團隊從專案範本複製到專案時，也會一併複製一般資源以及範本中定義的技能和熟練度。 一般資源指派也會維持與原先在專案範本中的一樣。 專案範本不支援具名資源。
