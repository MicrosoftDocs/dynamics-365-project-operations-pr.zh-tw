---
title: 商務交易
description: 本主題提供有關商務交易的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 3a8506effc453280177d74f94dcf9310e310c098
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149893"
---
# <a name="business-transactions"></a>商務交易

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

在 Dynamics 365 Project Service Automation 中，*商務交易* 是不由任何實體表示的抽象概念。 不過，實體上的一些通用欄位及程序是為了使用商務交易的概念而設計。 下列實體使用了這個概念：

- 報價明細詳細資料
- 合約服務內容詳細資料
- 估計明細
- 帳目明細
- 實際值

在這些實體中，報價明細詳細資料、合約服務內容詳細資料以及估計明細是對應至專案生命週期中的估計階段。 帳目明細和實際值實體對應至專案生命週期中的執行階段。

PSA 將這五個實體中的記錄視為商務交易。 唯一區別在於，對應至估計階段的實體中記錄視為財務預測，而對應至執行階段的實體中記錄則視為已發生的財務事實。

如需詳細資訊，請參閱[估計值](estimates.md)和[實際值](actuals.md)。

## <a name="concepts-that-are-unique-to-business-transactions"></a>商務交易所特有的概念
下列概念是商務交易概念所特有：

- 交易類型
- 交易分類
- 交易來源
- 交易關係

### <a name="transaction-type"></a>交易類型

交易類型代表對專案產生財務影響的時間和內容。 這由具有 PSA 中下列支援值的選項組所表示：
- 成本
- 專案合約
- 未開單銷售
- 已開單銷售
- 跨組織銷售
- 資源分配單位成本

### <a name="transaction-class"></a>交易分類

交易分類表示專案上產生的不同類型的成本。 這由具有 PSA 中下列支援值的選項組所表示：

- Time
- 費用
- 材料
- 服務費
- 里程碑
- 稅金

**里程碑** 值通常由商務規則用於 PSA 中的固定價格帳務。

### <a name="transaction-origin"></a>交易來源

交易來源是儲存每個商務交易來源的實體。 當專案執行開始進行時，每個商務交易都會引發另一個商務交易，而這又會建立另一個商務交易，依此類推。 交易來源實體的設計目的是要儲存有關每個交易來源的資料，以協助進行報告和追蹤。 

### <a name="transaction-connection"></a>交易關係

交易關係是儲存兩個類似商務交易 (例如成本與相關銷售實際值) 之間關係的實體，或是由帳務活動 (例如發票確認或發票更正) 所觸發的交易沖回。

交易來源與交易關係實體合起來協助您持續追蹤商務交易與導致建立特定商機交易的動作之間的關聯。

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>範例：交易來源如何與交易關係搭配使用

下列範例顯示 PSA 專案生命週期中時間項目的一般處理程序。

> ![在 Project Service 生命週期處理時間項目](media/basic-guide-17.png)
 
1. 送出時間項目會導致建立兩個帳目明細：一個用於成本，一個用於未開單銷售。
2. 最終核准時間項目會導致建立兩個實際值：一個用於成本，一個用於未開單銷售。
3. 使用者建立專案發票時，會使用來自未開單銷售的資料建立發票明細交易。 
4. 確認發票時，會建立兩個新的實際值：未開單銷售沖回和開單銷售實際值。

這其中每個事件都會觸發在交易來源和交易關係實體中建立記錄，以協助建立對這些跨時間項目、帳目明細、實際值和發票明細詳細資料所建立記錄之間關聯的追蹤。

下表顯示先前工作流程之交易來源實體中的記錄。

| Event                        | 來源                   | 來源類型                       | 交易                       | 交易類型         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| 時間項目送出        | 時間項目記錄 GUID   | 時間項目                        | 帳目明細記錄 GUID (成本)   | 帳目明細             |
| 時間項目記錄 GUID       | 時間項目               | 帳目明細記錄 GUID (銷售)  | 帳目明細                      |                          |
| 時間核准                | 帳目明細記錄 GUID | 帳目明細                      | 未開單銷售記錄 GUID        | 實際                   |
| 時間項目記錄 GUID       | 時間項目               | 未開單銷售記錄 GUID        | 實際                            |                          |
| 帳目明細記錄 GUID     | 帳目明細             | 成本實際記錄 GUID           | 實際                            |                          |
| 時間項目記錄 GUID       | 時間項目               | 成本實際記錄 GUID           | 實際                            |                          |
| 發票建立             | 時間項目記錄 GUID   | 時間項目                        | 發票明細交易 GUID     | 發票明細交易 |
| 帳目明細記錄 GUID     | 帳目明細             | 發票明細交易 GUID     | 發票明細交易          |                          |
| 發票確認         | 發票明細 GUID        | 發票明細                      | 已開單銷售記錄 GUID          | 實際                   |
| 發票 GUID                 | 發票                  | 已開單銷售記錄 GUID          | 實際                            |                          |
| 發票明細詳細資料 GUID     | 發票明細詳細資料      | 已開單銷售記錄 GUID          | 實際                            |                          |
| 時間項目記錄 GUID       | 時間項目               | 已開單銷售記錄 GUID          | 實際                            |                          |
| 帳目明細記錄 GUID     | 帳目明細             | 已開單銷售記錄 GUID          | 實際                            |                          |
| 時間項目記錄 GUID       | 時間項目               | 未開單銷售沖回 GUID      | 實際                            |                          |
| 帳目明細記錄 GUID     | 帳目明細             | 未開單銷售沖回 GUID      | 實際                            |                          |
| 草稿發票更正     | 舊的 ILD GUID             | 發票明細交易          | 更正 ILD GUID               | 發票明細交易 |
| 舊的 IL GUID                  | 發票明細             | 更正 ILD GUID               | 發票明細交易          |                          |
| 舊的發票 GUID             | 發票                  | 更正 ILD GUID               | 發票明細交易          |                          |
| 時間項目記錄 GUID       | 時間項目               | 更正 ILD GUID               | 發票明細交易          |                          |
| 帳目明細記錄 GUID     | 帳目明細             | 更正 ILD GUID               | 發票明細交易          |                          |
| 已確認發票更正 | 舊的 ILD GUID             | 發票明細交易          | 已沖回開單銷售實際值 GUID | 實際                   |
| 舊的 IL GUID                  | 發票明細             | 已沖回開單銷售實際值 GUID | 實際                            |                          |
| 舊的發票 GUID             | 發票                  | 已沖回開單銷售實際值 GUID | 實際                            |                          |
| 時間項目記錄 GUID       | 時間項目               | 已沖回開單銷售實際值 GUID | 實際                            |                          |
| 帳目明細記錄 GUID     | 帳目明細             | 已沖回開單銷售實際值 GUID | 實際                            |                          |
| 舊的 ILD GUID                 | 發票明細交易 | 新的未開單銷售實際值 GUID    | 實際                            |                          |
| 舊的 IL GUID                  | 發票明細             | 新的未開單銷售實際值 GUID    | 實際                            |                          |
| 舊的發票 GUID             | 發票                  | 新的未開單銷售實際值 GUID    | 實際                            |                          |
| 時間項目記錄 GUID       | 時間項目               | 新的未開單銷售實際值 GUID    | 實際                            |                          |
| 帳目明細記錄 GUID     | 帳目明細             | 新的未開單銷售實際值 GUID    | 實際                            |                          |
| 更正 ILD GUID          | 發票明細交易 | 新的未開單銷售實際值 GUID    | 實際                            |                          |
| 更正 IL GUID           | 發票明細             | 新的未開單銷售實際值 GUID    | 實際                            |                          |
| 更正發票 GUID      | 發票                  | 新的未開單銷售實際值 GUID    | 實際                            |                          |

下表顯示先前工作流程之交易關係實體中的記錄。

| Event                          | 交易 1                 | 交易 1 角色 | 交易 1 類型           | 交易 2                | 交易 2 角色 | 交易 2 類型 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| 時間項目送出          | 帳目明細 (銷售) GUID     | 未開單銷售     | msdyn_journalline            | 帳目明細 (成本) GUID     | 成本               | msdyn_journalline  |
| 時間核准                  | 未開單實際值 (銷售) GUID  | 未開單銷售     | msdyn_actual                 | 成本實際值 (成本) GUID       | 成本               | msdyn_actual       |
| 發票建立               | 發票明細詳細資料 GUID      | 已開單銷售       | msdyn_invoicelinetransaction | 未開單銷售實際值 GUID   | 未開單銷售     | msdyn_actual       |
| 發票確認           | 沖回實際值 GUID         | 沖回          | msdyn_actual                 | 原始未開單銷售 GUID | 原始           | msdyn_actual       |
| 已開單銷售 GUID              | 已開單銷售                  | msdyn_actual       | 未開單銷售實際值 GUID   | 未開單銷售               | msdyn_actual       |                    |
| 草稿發票更正       | 發票明細交易 GUID | 取代          | msdyn_invoicelinetransaction | 已開單銷售 GUID            | 原始           | msdyn_actual       |
| 確認發票更正     | 已開單銷售沖回 GUID    | 沖回          | msdyn_actual                 | 已開單銷售 GUID            | 原始           | msdyn_actual       |
| 新的未開單銷售實際值 GUID | 取代                     | msdyn_actual       | 已開單銷售 GUID            | 原始                     | msdyn_actual       |                    |
