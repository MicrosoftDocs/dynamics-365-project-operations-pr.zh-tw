---
title: 分工結構圖升級考量
description: 本文提供有關將 Project Service Automation 2.x 的分工結構圖升級至 3.x 的資訊。
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 42bf03b5e3be4b7bdce87148254ce69e381ffdf1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913104"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>分工結構圖升級考量

[!include [banner](../includes/psa-now-project-operations.md)]

本文提供有關將 Project Service Automation 2.x 的分工結構圖升級至 3.x 的資訊。 本文定義 Project Service Automation (PSA) 中專案成功升級所需的健全狀況。 此外，還提供有關導致升級失敗之常見阻礙情況的資訊。 如需有關在專案排程中定義專案工作及其功能的詳細資訊，請參閱[專案排程](project-creating.md)。

## <a name="key-entities"></a>主要實體
已載入資源的正確分工結構圖需要下列實體：

- [計畫](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [專案團隊](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [專案工作](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [資源指派](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [專案工作相依性](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [可預約資源](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

若要定義資源已載入的分工結構圖，您必須完成下列步驟：

1. 建立新專案： 如需有關如何建立新專案的詳細資訊，請參閱 [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)。
2. 建立一個或多個工作。 如需有關如何建立工作的詳細資訊，請參閱 [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)。
3. 定義工作相依性。 如需詳細資訊，請參閱[專案工作相依性](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)。
4. 將專案團隊成員指派給專案。 如需詳細資訊，請參閱 [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)。
5. 將專案團隊成員指派給工作。 如需詳細資訊，請參閱 [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)。

## <a name="project-team-relationships"></a>專案團隊關聯

為了確保升級成功，必須正確維護下列關聯：
- 所有的專案團隊成員都必須與可預約資源有關聯。
- 所有的專案團隊成員都必須與相同的專案有關聯。 

## <a name="project-task-relationships"></a>專案工作關聯
為了確保升級成功，必須正確維護下列關聯：

- 任何相關工作都必須與相同的專案有關聯。
- 每項明細工作都必須有上層工作。
- 每項工作都必須有上層專案。

### <a name="valid-conditions"></a>有效條件

- 所有工作期間都必須大於或等於 (>=) 1 個小時且小於 1,800,000 分鐘 (1,250 天)。*
- 所有工作的開始日期都必須有早於 2000/01/01。*
- 所有工作的開始日期都不得晚於今天起算 17 年之後。*
- 所有工作的開始日期都必須早於或等於其完成日期。
- 分類 (費用、材料、稅金和時間)上所有的交易類型都必須有 **預設單位** 及 **單位群組** 的值。
- 應避免使用含字母的日期格式。

### <a name="potential-mitigation-steps"></a>可能的風險降低步驟
- 使用 [進階尋找] 找出沒有包含專案識別碼的專案工作。
- 使用 [進階尋找] 找出排程期間大於 > 1,800,000 的專案工作。
- 在進行任何資料變更之前，必須先調查任何與實體相關聯的自訂，這個實體可能已致使資料進入錯誤狀態。 您必須先處理這些自訂，才能繼續進行任何資料相關更新。
- 對於找出的已孤立工作，如果這些工作是不需要的，或是必須與正確的上層專案建立關聯，請考慮加以刪除。
- 對於任何大於 1,250 天期間的工作，請考慮新增多個工作來表示總期間 (如果可行)。

> [!NOTE]
> 標示有星號 (\*) 的項目因客戶關係管理 (CRM) 僅支援 7,320 週期擴充而有限制。 您必須保持在此限制之下。

## <a name="resource-assignment-relationships"></a>資源指派關聯
為了確保升級成功，必須正確維護下列關聯：

- 分工結構圖中所有的資源指派都必須與同一個專案相關聯。
- 分工結構圖中所有的資源指派都必須與同一個專案中的專案團隊成員建立關聯。

### <a name="potential-mitigation-steps"></a>可能的風險降低步驟
- 找出所有不在上述條件範圍內的工作。  
- 任何不再有效的資源指派都必須加以刪除。

## <a name="project-task-dependency-relationships"></a>專案工作相依性關聯
為了確保升級成功，必須正確維護下列關聯：

- 所有專案工作相依性都必須與相同的專案相關聯。
- 工作不能有參照多次的相同相依性。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
