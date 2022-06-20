---
title: 實際值概觀
description: 本文提供有關專案實際值的資訊。
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 35282e6c51fff28dbbb0a5a7de760788416ed0e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929066"
---
# <a name="actuals-overview"></a>實際值概觀

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

實際值是專案中已完成的工作量。 專案實際值可以追溯至其原始憑證。 這些原始憑證包括時間項目、費用項目與帳目分錄以及發票。

![如何將專案實際值追蹤至原始憑證。](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>送出時間項目

在 PSA 中，將對應至時間及材料合約服務內容之專案的時間項目送出時，會建立兩個帳目明細。 一項明細用於成本，而另一項用於未開單銷售。 將對應至固定價格合約服務內容之專案的時間項目送出時，只會建立成本的帳目明細。 

輸入預設價格的邏輯會存在於帳目明細。 時間項目中的所有欄位值都會複製到帳目明細。 這些欄位包括交易的日期、專案所對應至的合約服務內容，以及適當價目表中的貨幣結果。 

影響預設價格的欄位 (例如 **角色** 和 **組織單位**) 會產生要在帳目明細上依預設輸入的適當價格。 如果在時間項目上新增自訂欄位，而且您想要讓欄位值傳播至實際值，請在實際值實體上建立欄位，並使用欄位對應將欄位從時間項目複製到實際值。

## <a name="submitting-an-expense-entry"></a>送出費用項目

在 PSA 中，將對應至時間及材料合約服務內容之專案的費用項目送出時，會建立兩個帳目明細。 一項明細用於成本，而另一項用於未開單銷售。 將對應至固定價格合約服務內容之專案的費用項目送出時，只會建立成本的帳目明細。

輸入費用預設價格的邏輯是根據您在 **費用項目** 頁面上選取的費用類別。 交易日期、專案所對應至的合約服務內容以及貨幣都會用來決定適當的價目表。 不過，就價格本身而言，使用者輸入的金額預設會直接設定在成本和銷售的相關費用帳目明細上。

在目前的 PSA 版本中，依類別輸入的每單位預設價格無法在費用項目上使用。

## <a name="using-entry-journals-to-record-costs"></a>使用分錄帳目來記錄成本

在 PSA 中，您可以使用分錄帳目來記錄材料、費用、時間、支出或稅務交易分類中的成本或營收。 帳目有標題、明細和 **確認** 動作。 以下是一些您可能會使用帳目的情況：

- 您必須在專案上記錄材料實際成本和銷售。
- 您必須將交易實際值從其他系統移至 PSA。
- 您必須記錄其他系統中發生的成本 (例如採購或轉承包成本)。

> [!IMPORTANT]
> 使用分錄帳目建立實際值的工作，只能由完全了解實際值對專案所產生之會計影響的使用者來完成。 這是因為應用程式不會驗證帳目明細類型，或帳目明細上所輸入的相關價格。 由於會有這種帳目類型的影響，請在授與何人建立分錄帳目的存取權限時，特別小心。     


## <a name="recording-actuals-based-on-project-events"></a>根據專案事件記錄實際值

PSA 會記錄專案期間發生的財務交易。 這些交易記錄會以 **實際值** 來記錄。 下表顯示根據專案是時間及材料專案還是固定價格專案、是否在售前階段，或是否為內部專案，所建立的不同類型實際值。

**資源隸屬於與專案承包單位相同的組織單位**

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

**資源隸屬於與專案承包單位不同的組織單位**

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
