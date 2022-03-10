---
title: 建立工作時數範本
description: 本主題說明如何建立 Project Service 中的工作時數範本。
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
ms.openlocfilehash: 90525cf1e7cd487a03b064466ad1b13f8afb7819443fc4bacf9c7d3eee86f0b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987381"
---
# <a name="create-a-work-hours-template-project-service"></a>建立工作時數範本 (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

若要建立和管理專案，您必須將行事曆範本套用至專案。 行事曆範本會定義下列專案屬性：

- 工作時數，包括開始和結束時間
- 工作日
- 行事曆例外，例如非工作日

套用至專案的行事曆範本是組織設定中所定義行事曆範本的複本。

> [!NOTE]
> 如果您變更行事曆範本，這些變更不會傳播到專案的工作時數。 若要變更專案的工作時數，必須套用新的範本。

若要為您的組織建立行事曆範本，有兩個重要需求：

- 使用新的或現有的可預約資源定義範本所需的工作時數。
- 建立新的行事曆範本，並將範本與可預約資源產生關聯。

**定義範本的工作時數**

1. 移至 **資源** \> **資源**。
2. 建立要在行事曆範本中參考的新資源，或選取現有的資源。
3. 選擇 資源的 **工作時數** 索引標籤，並完成[設定資源的工作時數](/dynamics365/field-service/set-work-hours-resource.md)中的指示以設定行事曆規則。

**建立新的行事曆範本**

1. 移至 **設定** \> **事曆範本**。
2. 選取 **新增**，然後輸入名稱、描述和範本資源。


> [!NOTE]
> 在行事曆範本中參考資源時，資源行事曆的複本會與行事曆範本產生關聯。 如果複本範本的工作時數變更，這些變更不會傳播到行事曆範本。


### <a name="see-also"></a>請參閱  
 [設定資源](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
