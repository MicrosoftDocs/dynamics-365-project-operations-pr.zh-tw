---
title: 實際值
description: 本主題提供有關如何在 Microsoft Dynamics 365 Project Operations 中處理實際值的資訊。
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072986"
---
# <a name="actuals"></a>實際值 

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

實際值是專案中已完成的工作量。 這些實際值是因時間和費用項目以及帳目分錄和發票而建立的。

## <a name="journal-lines-and-time-submission"></a>帳目明細和時間提交

如需時間項目的詳細資訊，請參閱 [時間項目概觀 ](../time/time-entry-overview.md)。

### <a name="time-and-materials"></a>時間及材料

將提交的時間項目連結至對應到時間及材料合約服務內容的專案時，系統會建立兩個帳目明細，一個用於成本，另一個用於未開單銷售。

### <a name="fixed-price"></a>固定價格

將提交的時間項目連結至對應到固定價格合約服務內容的專案時，系統會為成本建立一個帳目明細。

### <a name="default-pricing"></a>預設定價

建立預設價格的邏輯會存在於帳目明細。 時間項目中的欄位值都會複製到帳目明細。 這些值包含交易日期、專案所對應至的合約服務內容，以及適當價目表中的貨幣結果。

影響預設定價的欄位 (例如 **角色** 和 **組織單位**) 會在帳目明細上用來決定適當價格。 您可以在時間項目上新增自訂欄位。 如果您想要讓欄位值傳播至實際值，請在實際值實體上建立欄位，並使用欄位對應將欄位從時間項目複製到實際值。

## <a name="journal-lines-and-basic-expense-submission"></a>帳目明細和基本費用提交

如需費用項目的詳細資訊，請參閱 [費用概觀 ](../expense/expense-overview.md)。

### <a name="time-and-materials"></a>時間及材料

將提交的基本費用項目連結至對應到時間及材料合約服務內容的專案時，系統會建立兩個帳目明細，一個用於成本，另一個用於未開單銷售。

### <a name="fixed-price"></a>固定價格

將提交的基本費用項目連結至對應到固定價格合約服務內容的專案時，系統會為成本建立一個帳目明細。

### <a name="default-pricing"></a>預設定價

輸入費用的預設價格的邏輯是根據費用類別而定。 交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。 不過，使用者就價格本身所輸入的金額預設會直接在成本和銷售的相關費用帳目明細上設定。

依類別輸入的每單位預設價格無法在費用項目上使用。

## <a name="use-entry-journals-to-record-costs"></a>使用分錄帳目來記錄成本

您可以使用分錄帳目來記錄材料、服務費、時間、費用或稅務交易分類中的成本或營收。 帳目可用於下列用途：

- 記錄專案上的材料及銷售實際成本。
- 將交易實際值從系統移至 Microsoft Dynamics 365 Project Operations。
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
