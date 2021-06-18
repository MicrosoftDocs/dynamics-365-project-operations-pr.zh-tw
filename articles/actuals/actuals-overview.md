---
title: 實際值
description: 本主題提供有關如何在 Microsoft Dynamics 365 Project Operations 中處理實際值的資訊。
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996601"
---
# <a name="actuals"></a>實際值 

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

實際值表示專案上已審查且核准的財務及排程進度。 這些值是因為核准時間、費用、材料使用項目以及帳目分錄和發票而產生。

## <a name="journal-lines-and-time-submission"></a>帳目明細和時間提交

如需時間項目的詳細資訊，請參閱 [時間項目概觀 ](../time/time-entry-overview.md)。

### <a name="time-and-materials"></a>時間及材料

將提交的時間項目連結至對應到時間及材料合約服務內容的專案時，系統會建立兩個帳目明細，一個用於成本，另一個用於未開單銷售。

### <a name="fixed-price"></a>固定價格

將提交的時間項目連結至對應到固定價格合約服務內容的專案時，系統會為成本建立一個帳目明細。

### <a name="default-pricing"></a>預設定價

建立預設價格的邏輯會存在於帳目明細。 時間項目中的欄位值都會複製到帳目明細。 這些值包含交易日期、專案所對應至的合約服務內容，以及適當價目表中的貨幣結果。

影響預設定價的欄位 (例如 **角色** 和 **資源分配單位**) 會用來決定帳目明細上的適當價格。 您可以在時間項目上新增自訂欄位。 如果您希望欄位值傳播至實際值，請在 **實際值** 和 **帳目明細** 資料表中建立欄位。 利用自訂程式碼，使用交易來源透過帳目明細將選取的欄位值從時間項目傳播至實際值。 如需交易來源及人脈的詳細資訊，請參閱[將實際值連結至原始記錄](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。

## <a name="journal-lines-and-basic-expense-submission"></a>帳目明細和基本費用提交

如需費用項目的詳細資訊，請參閱 [費用概觀 ](../expense/expense-overview.md)。

### <a name="time-and-materials"></a>時間及材料

將提交的基本費用項目連結至對應到時間及材料合約服務內容的專案時，系統會建立兩個帳目明細，一個用於成本，另一個用於未開單銷售。

### <a name="fixed-price"></a>固定價格

當送出的基本費用項目已與對應至固定價格合約服務內容的專案連結時，系統會為成本建立一個帳目明細。

### <a name="default-pricing"></a>預設定價

輸入費用的預設價格的邏輯是根據費用類別而定。 交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。 影響預設定價的欄位 (例如 **角色** 和 **交易類別**) 會用來決定帳目明細上的適當價格。 不過，這只有在價目表的定價方式是 **單價** 時才適用。 如果定價方式是 **依照成本** 或 **成本加成**，則成本會使用建立費用項目時所輸入的價格，而銷售帳目明細的價格則是根據定價方式進行計算。 

您可以在費用項目上新增自訂欄位。 如果您希望欄位值傳播至實際值，請在 **實際值** 和 **帳目明細** 資料表中建立欄位。 利用自訂程式碼，使用交易來源透過帳目明細將選取的欄位值從時間項目傳播至實際值。 如需交易來源及人脈的詳細資訊，請參閱[將實際值連結至原始記錄](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。

## <a name="journal-lines-and-material-usage-log-submission"></a>帳目明細及材料使用記錄送出

如需費用項目的詳細資訊，請參閱[材料使用記錄](../material/material-usage-log.md)。

### <a name="time-and-materials"></a>時間及材料

將送出的材料使用記錄項目與對應至時間及材料合約服務內容的專案連結時，系統會建立兩個帳目明細，一個用於成本，一個用於未開單銷售。

### <a name="fixed-price"></a>固定價格

當送出的材料使用記錄項目已與對應至固定價格合約服務內容的專案連結時，系統會為成本建立一個帳目明細。

### <a name="default-pricing"></a>預設定價

輸入材料預設價格的邏輯是根據產品與單位組合而定。 交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。 影響預設定價的欄位 (例如 **角色** 和 **產品識別碼**) 會用來決定帳目明細上的適當價格。 不過，這只適用於目錄產品。 如果是目錄外產品，則將建立材料使用記錄項目時所輸入的價格用於帳目明細上的成本和售價。 

您可以在 **材料使用記錄** 項目上新增自訂欄位。 如果您希望欄位值傳播至實際值，請在 **實際值** 和 **帳目明細** 資料表中建立欄位。 利用自訂程式碼，使用交易來源透過帳目明細將選取的欄位值從時間項目傳播至實際值。 如需交易來源及人脈的詳細資訊，請參閱[將實際值連結至原始記錄](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。

## <a name="use-entry-journals-to-record-costs"></a>使用分錄帳目來記錄成本

您可以使用分錄帳目來記錄材料、服務費、時間、費用或稅務交易分類中的成本或營收。 帳目可用於下列用途：

- 將交易實際值從其他系統移到 Microsoft Dynamics 365 Project Operations。
- 記錄其他系統中發生的成本。 這些成本可以包含採購或轉承包成本。

> [!IMPORTANT]
> 應用程式不會驗證帳目明細類型或是帳目明細上所輸入的相關定價。 因此，只有完全了解實際值對專案所產生之會計影響的使用者，才應使用帳目來建立實際值。 由於會有這種帳目類型的影響，您必須小心選擇有存取權限可建立分錄帳目的人員。

## <a name="record-actuals-based-on-project-events"></a>根據專案事件記錄實際值

Project Operations 會記錄專案期間發生的財務交易。 這些交易記錄會以實際值來記錄。 下表顯示根據專案是時間及材料專案還是固定價格專案、是否在售前階段，或是否為內部專案，所建立的不同類型實際值。

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>資源隸屬於與專案承包單位相同的組織單位

<table>
<thead>
<tr>
<th rowspan="3">Event</th>
<th colspan="4">計費或已售出專案</th>
<th rowspan="3">在售前階段的專案</th>
<th rowspan="3">內部專案</th>
</tr>
<tr>
<th colspan="2">時間及材料</th>
<th colspan="2">固定價格</th>
</tr>
<tr>
<th>實際值</th>
<th>交易貨幣</th>
<th>固定價格</th>
<th>交易貨幣</th>
</tr>
</thead>
<tbody>
<tr>
<td>時間項目已建立。</td>
<td colspan="6">實際值實體中沒有活動</td>
</tr>
<tr>
<td>時間項目已送出。</td>
<td colspan="6">實際值實體中沒有活動</td>
</tr>
<tr>
<td rowspan="2">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</td>
<td>成本實際值</td>
<td>承包單位貨幣</td>
<td rowspan="2">成本實際值</td>
<td rowspan="2">承包單位貨幣
<td rowspan="2">成本實際值</td>
<td rowspan="2">成本實際值</td>
</tr>
<tr>
<td>未開單銷售實際值 – 應收費</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td rowspan="3">時間已核准，且核准期間發生的計費時數有減少。</td>
<td>成本實際值</td>
<td>承包單位貨幣</td>
<td rowspan="3">成本實際值</td>
<td rowspan="3">承包單位貨幣</td>
<td rowspan="3">成本實際值</td>
<td rowspan="3">成本實際值</td>
</tr>
<tr>
<td>未開單銷售實際值 – 新數量應收費</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td>未開單銷售實際值 – 差異不應收費</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td rowspan="2">發票已確認，且發生的計費時數沒有任何變更或增加。</td>
<td>未開單銷售沖回</td>
<td>專案合約貨幣</td>
<td rowspan="2">里程碑已開單銷售</td>
<td rowspan="2">專案合約貨幣</td>
<td rowspan="2">不適用</td>
<td rowspan="2">不適用</td>
</tr>
<tr>
<td>已開單銷售</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td rowspan="3">發票已確認，且發生的計費時數有減少。</td>
<td>未開單銷售沖回</td>
<td>專案合約貨幣</td>
<td rowspan="3">不適用</td>
<td rowspan="3">不適用</td>
<td rowspan="3">不適用</td>
<td rowspan="3">不適用</td>
</tr>
<tr>
<td>已開單銷售 – 新數量應收費</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td>已開單銷售 – 差異不應收費</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td rowspan="2">已更正發票以增加應收費數量。</td>
<td>已開單銷售 – 沖回</td>
<td>專案合約貨幣</td>
<td rowspan="5">
<ul>
<li>里程碑已開單銷售沖回</li>
<li>里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</li>
</ul>
</td>
<td rowspan="5">專案合約貨幣</td>
<td rowspan="5">不適用</td>
<td rowspan="5">不適用</td>
</tr>
<tr>
<td>已開單銷售</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td rowspan="3">已更正發票以減少應收費數量。</td>
<td>已開單銷售 – 沖回</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td>新數量已開單銷售</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td>未開單銷售 – 差異應收費</td>
<td>專案合約貨幣</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>資源隸屬於與專案承包單位不同的組織單位

<table>
<thead>
<tr>
<th rowspan="3">Event</th>
<th colspan="4">計費或已售出專案</th>
<th rowspan="3">在售前階段的專案</th>
<th rowspan="3">內部專案</th>
</tr>
<tr>
<th colspan="2">時間及材料</th>
<th colspan="2">固定價格</th>
</tr>
<tr>
<th>實際值</th>
<th>交易貨幣</th>
<th>固定價格</th>
<th>交易貨幣</th>
</tr>
</thead>
<tbody>
<tr>
<td>時間項目已建立。</td>
<td colspan="6">實際值實體中沒有活動</td>
</tr>
<tr>
<td>時間項目已送出。</td>
<td colspan="6">實際值實體中沒有活動</td>
</tr>
<tr>
<td rowspan="4">時間已核准，且核准期間發生的計費時數沒有任何變更或增加。</td>
<td>成本實際值</td>
<td>承包單位貨幣</td>
<td rowspan="4">成本實際值</td>
<td rowspan="4">承包單位貨幣</td>
<td rowspan="4">成本實際值</td>
<td rowspan="4">成本實際值</td>
</tr>
<tr>
<td>未開單銷售實際值 – 應收費</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td>資源分配單位成本</td>
<td>資源分配單位貨幣</td>
</tr>
<tr>
<td>跨組織銷售</td>
<td>承包單位貨幣</td>
</tr>
<tr>
<td rowspan="5">時間已核准，且核准期間發生的計費時數有減少。</td>
<td>成本實際值</td>
<td>承包單位貨幣</td>
<td rowspan="5">成本實際值</td>
<td rowspan="5">承包單位貨幣</td>
<td rowspan="5">成本實際值</td>
<td rowspan="5">成本實際值</td>
</tr>
<tr>
<td>資源分配單位成本</td>
<td>資源分配單位貨幣</td>
</tr>
<tr>
<td>跨組織銷售</td>
<td>承包單位貨幣</td>
</tr>
<tr>
<td>未開單銷售實際值 – 新數量應收費</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td>未開單銷售實際值 – 差異不應收費</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td rowspan="2">發票已確認，且發生的計費時數沒有任何變更或增加。</td>
<td>未開單銷售沖回</td>
<td>專案合約貨幣</td>
<td rowspan="2">里程碑已開單銷售</td>
<td rowspan="2">專案合約貨幣</td>
<td rowspan="2">不適用</td>
<td rowspan="2">不適用</td>
</tr>
<tr>
<td>已開單銷售</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td rowspan="3">發票已確認，且發生的計費時數有減少。</td>
<td>未開單銷售沖回</td>
<td>專案合約貨幣</td>
<td rowspan="3">不適用</td>
<td rowspan="3">不適用</td>
<td rowspan="3">不適用</td>
<td rowspan="3">不適用</td>
</tr>
<tr>
<td>已開單銷售 – 新數量應收費</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td>已開單銷售 – 差異不應收費</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td rowspan="2">已更正發票以增加應收費數量。</td>
<td>已開單銷售 – 沖回</td>
<td>專案合約貨幣</td>
<td rowspan="5">
<ul>
<li>里程碑已開單銷售沖回</li>
<li>里程碑狀態從<strong>已開立發票</strong>到<strong>已準備好開立發票</strong>的變更</li>
</ul>
</td>
<td rowspan="5">專案合約貨幣</td>
<td rowspan="5">不適用</td>
<td rowspan="5">不適用</td>
</tr>
<tr>
<td>已開單銷售</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td rowspan="3">已更正發票以減少應收費數量。</td>
<td>已開單銷售 – 沖回</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td>新數量已開單銷售</td>
<td>專案合約貨幣</td>
</tr>
<tr>
<td>未開單銷售 – 差異應收費</td>
<td>專案合約貨幣</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
