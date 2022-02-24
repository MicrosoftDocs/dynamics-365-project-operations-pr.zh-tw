---
title: 將實際值連結至原始記錄
description: 本主題說明有關如何將實際值連結至原始記錄，例如時間項目、費用項目或材料使用記錄。
author: rumant
manager: tfehr
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 545775c4eae6c3dc689f264e7f662471c17b2340
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852579"
---
# <a name="link-actuals-to-original-records"></a>將實際值連結至原始記錄

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_


在 Dynamics 365 Project Operations 中，*商務交易* 不是實體所表示的抽象概念。 不過，實體上的一些通用欄位及程序是為了使用商務交易的概念而設計。 下列實體會使用此概念：

- 報價明細詳細資料
- 合約服務內容詳細資料
- 估計明細
- 帳目明細
- 實際值

在這些實體中，**報價明細詳細資料**、**合約服務內容詳細資料** 以及 **估計明細** 是對應至專案生命週期中的估計階段。 **帳目明細** 和 **實際值實體** 對應至專案生命週期中的執行階段。

Project Operations 將這五個實體中的記錄視為商務交易。 唯一區別在於，對應至估計階段的實體中記錄視為財務預測，而對應至執行階段的實體中記錄則視為已發生的財務事實。

## <a name="concepts-that-are-unique-to-business-transactions"></a>商務交易所特有的概念
下列概念是商務交易概念所特有：

- 交易類型
- 交易分類
- 交易來源
- 交易關係

### <a name="transaction-type"></a>交易類型

交易類型代表對專案產生財務影響的時間和內容。 這是由具有 Project Operations 中下列支援值的選項組所表示：

  - 成本
  - 專案合約
  - 未開單銷售
  - 已開單銷售
  - 跨組織銷售
  - 資源分配單位成本

### <a name="transaction-class"></a>交易分類

交易分類表示專案上產生的不同類型的成本。 這是由具有 Project Operations 中下列支援值的選項組所表示：

  - 時間
  - 費用
  - 材料
  - 費用
  - 里程碑
  - 稅額

**里程碑** 通常由商務規則用於 Project Operations 中的固定價格帳務。

### <a name="transaction-origin"></a>交易來源

**交易來源** 是儲存每個商務交易來源的實體。 隨著專案的進展，每一筆商務交易都會導致產生另一筆商業務交易，而這又會建立其他商務交易，依此類推。 交易來源實體是設計來儲存關於每筆交易之來源的資料，有助於提供報表和可追蹤性。 

### <a name="transaction-connection"></a>交易關係

**交易關係** 是儲存兩筆類似商務交易 (例如成本與相關銷售實際值) 之間關聯的實體，或是由帳務活動 (例如發票確認或發票更正) 所觸發的交易沖回。

**交易來源** 與 **交易關係** 實體合起來協助您持續追蹤商務交易與產生特定商務交易的動作之間的關聯。

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>範例：交易來源如何與交易關係搭配使用

下列範例顯示 Project Operations 專案生命週期中時間項目的一般處理程序。

> ![在 Project Service 生命週期處理時間項目](media/basic-guide-17.png)
 
1. 送出時間項目會建立兩個帳目明細：一個明細用於成本，另一個明細用於未開單銷售。
2. 最終核准時間項目時，會建立兩個實際值：一個實際值用於成本，另一個實際值用於未開單銷售。
3. 建立新的專案發票時，會使用來自未開單銷售的資料建立發票明細交易。 
4. 確認發票時，會建立兩個新的實際值：未開單銷售沖回實際值和開單銷售實際值。

這其中每一個事件都會在 **交易來源** 和 **交易關係** 實體中建立一個記錄。 這些新記錄有助於建立各種時間項目、帳目明細、實際值和發票明細詳細資料上所建立記錄之間關聯的歷程記錄。

下表顯示工作流程之 **交易來源** 實體中的記錄。

| 活動                        | 原始來源                   | 來源類型                       | 交易                       | 交易類型         |
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

下表顯示工作流程之 **交易關係** 實體中的記錄。

| 活動                          | 交易 1                 | 交易 1 角色 | 交易 1 類型           | 交易 2                | 交易 2 角色 | 交易 2 類型 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| 時間項目送出          | 帳目明細 (銷售) GUID     | 未開單銷售     | msdyn_journalline            | 帳目明細 (成本) GUID     | 成本               | msdyn_journalline  |
| 時間核准                  | 未開單實際值 (銷售) GUID  | 未開單銷售     | msdyn_actual                 | 成本實際值 (成本) GUID       | 成本               | msdyn_actual       |
| 發票建立               | 發票明細詳細資料 GUID      | 已開單銷售       | msdyn_invoicelinetransaction | 未開單銷售實際值 GUID   | 未開單銷售     | msdyn_actual       |
| 發票確認           | 沖回實際值 GUID         | 沖回          | msdyn_actual                 | 原始未開單銷售 GUID | 原始           | msdyn_actual       |
| 已開單銷售 GUID              | 已開單銷售                  | msdyn_actual       | 未開單銷售實際值 GUID   | 未開單銷售               | msdyn_actual       |                    |
| 草稿發票更正       | 發票明細交易 GUID | 取代          | msdyn_invoicelinetransaction | 已開單銷售 GUID            | 原始           | msdyn_actual       |
| 確認發票更正     | 已開單銷售沖回 GUID    | 沖回          | msdyn_actual                 | 已開單銷售 GUID            | 原始           | msdyn_actual       |
| 新的未開單銷售實際值 GUID | 取代                     | msdyn_actual       | 已開單銷售 GUID            | 原始                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
