---
title: 交易來源 - 將實際值連結至其來源
description: 本主題說明如何使用交易來源的概念，將實際值連結至原始來源記錄，例如時間項目、費用項目或材料使用記錄。
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584816"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>交易來源 - 將實際值連結至其來源

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

建立交易來源記錄是要將實際值連結至其來源，例如時間項目、費用項目、材料使用記錄和專案發票。

下列範例顯示 Project Operations 專案生命週期中時間項目的一般處理程序。

> ![處理 Project Operations 中的時間項目。](media/basic-guide-17.png)
 
1. 提交時間項目會導致建立兩個帳目明細：一個用於成本，一個用於未開單銷售。
2. 最終核准時間項目會導致建立兩個實際值：一個用於成本，一個用於未開單銷售。
3. 使用者建立專案發票時，會使用來自未開單銷售的資料建立發票明細交易。
4. 確認發票時，會建立兩個新的實際值：未開單銷售沖回和開單銷售實際值。

此處理工作流程中的每個事件都會觸發建立交易來源實體中的記錄，以協助建立對這些跨時間項目、帳目明細、實際值和發票明細詳細資料所建立記錄之間關聯性的追蹤。

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


下圖顯示使用 Project Operations 中的時間項目範例，在發生各種事件時建立實際值與其來源之間的連結。

> ![在 Project Operations 中將實際值連結至來源記錄的方式。](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
