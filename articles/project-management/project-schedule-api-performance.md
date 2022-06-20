---
title: 專案排程 API 效能
description: 本文提供有關專案排程 API 效能評定的資訊，並找出最佳做法以達最有效利用。
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911172"
---
# <a name="project-schedule-api-performance"></a>專案排程 API 效能

_**適用於：** 資源/非庫存型案例適用的 Project Operations 精簡部署 - 交易至開立預估發票、Project for the Web_

本文提供有關專案排程應用程式開發介面 (API) 效能評定的資訊，並找出最佳做法以發揮最大的使用效益。

## <a name="project-scheduling-service"></a>專案排程服務
專案排程服務是在 Microsoft Azure 中執行的多組織用戶共享服務。 其設計目的是要在使用者處理專案時提供快速且流暢的體驗，以改善互動。 達成這項改善的方法是，接受變更要求、處理這些要求，然後立即傳回結果。 服務以非同步方式保存至 Dataverse，不會封鎖使用者，使其無法執行其他作業。

專案排程 API 依賴專案排程服務，以執行本文稍後幾節中詳加說明的要求。

專案排程 API 是專門為了與下列分工結構圖 (WBS) 實體搭配使用而設計：

  - Project
  - 專案工作
  - 專案工作相依性
  - 專案團隊成員
  - 資源指派
  
對現成可用欄位和自訂欄位都有支援。 除非另有說明，所有的一般作業 (例如建立、更新和刪除) 一律受支援。 如需詳細資訊，請參閱[使用專案排程 API 來執行作業及排程實體](schedule-api-preview.md)。

在專案排程 API 中，已新增工作單元模式。 此模式稱為 OperationSet，當您必須在單一交易中處理多個要求時，可以使用此模式。

下圖顯示使用此功能時，合作夥伴將會體驗的流程。

![Dataverse 和專案排程服務流程。](./media/dataverse-project-scheduling-service-flow.png)

**步驟 1**：用戶端對 Dataverse 中的開放式資料通訊協定 (OData) 端點進行 API 呼叫，以建立 OperationSet。

**步驟 2**：建立新的 OperationSet 之後，傳回 **OperationSetId** 值。

**步驟 3**：用戶端使用 **OperationSetId** 值，提出另一次專案排程 API 要求。 結果是對排程實體的建立、更新或刪除要求。 提出此要求時，服務會執行中繼資料驗證。 如果驗證失敗，則終止要求，並傳回錯誤。

**步驟 4a–4c**：這些步驟代表「接受」階段。 用戶端呼叫 **ExecuteOperationSetV1** API，這會以單一批次將所有的變更傳送至專案排程服務。 專案排程服務對該批次中的要求執行其本身的驗證。 任何驗證失敗都會復原該批次作業，並將例外狀況傳回呼叫端。 如果專案排程服務順利接受了該批次，則會更新 OperationSet 狀態，以反映 OperationSet 正在由專案排程服務處理中。

**步驟 5**：此步驟代表「保存」階段。 專案排程服務會以非同步方式在一次交易中將批次寫入 Dataverse。 如果寫入作業成功，則會將 OperationSet 標示為 **已完成**。 任何錯誤都會將交易和批次復原，並將 OperationSet 標示為 **失敗**。

## <a name="performance-methodology"></a>效能方法
執行時間定義為一段從呼叫 **ExecuteOperationSetV1** API 直到專案排程服務完成寫入 Dataverse 為止的時間。 所有作業執行共計 2,200 次，系統會報告 P99 執行時間測量。 單一記錄和大量作業會經過測量。

如果是單一記錄作業，OperationSet 會包含一個要求。 至於大量作業，則包含 20、50 或 100 個要求。 每個大量作業大小都會分別回報。

這些作業會在北美洲的 UR 15 Project Operations 精簡部署上執行。

## <a name="results"></a>結果
### <a name="create-operations"></a>建立作業
#### <a name="single-record-create-operations"></a>單一記錄建立作業
下表顯示建立單一記錄的執行時間。 時間以秒為單位。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">記錄&nbsp;&nbsp;&nbsp;類型</th>
    <th class="tg-0lax" colspan="2">時間</th>
  </tr>
  <tr>
    <th class="tg-0lax">必填欄位</th>
    <th class="tg-0lax">所有支援的欄位</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">工作</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">指派</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">團隊成員</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">相依性</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>大量建立作業
下表顯示建立許多記錄的執行時間。 具體說來，Microsoft 已測量建立單一 OperationSet 中 20、50 和 100 筆記錄的執行時間。 時間以秒為單位。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">記錄&nbsp;&nbsp;&nbsp;類型</th>
    <th class="tg-0lax" colspan="6">時間</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 筆記錄</th>
    <th class="tg-0lax" colspan="2">50 筆記錄</th>
    <th class="tg-0lax" colspan="2">100 筆記錄</th>
  </tr>
  <tr>
    <th class="tg-0lax">必填欄位</th>
    <th class="tg-0lax">所有支援的欄位</th>
    <th class="tg-0lax">必填欄位</th>
    <th class="tg-0lax">所有支援的欄位</th>
    <th class="tg-0lax">必填欄位</th>
    <th class="tg-0lax">所有支援的欄位</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">工作</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">指派</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">相依性</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> **專案** 與 **團隊成員** 實體的大量建立作業未列入表中，因為這些作業的執行階段類似於多次呼叫 API 進行單一記錄建立作業時的執行階段。 這些 API 會在 Dataverse 中立即執行。

下圖顯示 **工作**、**指派** 和 **相依性** 實體在建立 20、50 和 100 筆記錄且所有受支援欄位都已用上時的執行時間圖。

![建立記錄執行時間圖表。](./media/create-record-execution-time.png)

### <a name="update-operations"></a>更新作業
#### <a name="single-record-update-operations"></a>單一記錄更新作業
下表顯示更新單一記錄的執行時間。 時間以秒為單位。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">記錄&nbsp;&nbsp;&nbsp;類型</th>
    <th class="tg-0lax" colspan="2">時間</th>
  </tr>
  <tr>
    <th class="tg-0lax">必填欄位 </th>
    <th class="tg-0lax">所有支援的欄位</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">工作</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">團隊成員</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> 不支援對 **資源指派** 和 **專案工作相依性** 實體的更新作業。

#### <a name="bulk-update-operations"></a>大量更新作業
下表顯示更新許多記錄的執行時間。 具體說來，Microsoft 已測量更新單一 OperationSet 中 20、50 和 100 筆記錄的執行時間。 時間以秒為單位。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">記錄&nbsp;&nbsp;&nbsp;類型</th>
    <th class="tg-0lax" colspan="6">時間</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 筆記錄</th>
    <th class="tg-0lax" colspan="2">50 筆記錄</th>
    <th class="tg-0lax" colspan="2">100 筆記錄</th>
  </tr>
  <tr>
    <th class="tg-0lax">必填欄位</th>
    <th class="tg-0lax">所有支援的欄位</th>
    <th class="tg-0lax">必填欄位</th>
    <th class="tg-0lax">所有支援的欄位</th>
    <th class="tg-0lax">必填欄位</th>
    <th class="tg-0lax">所有支援的欄位</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">工作</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">團隊成員</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> 不支援對 **資源指派** 和 **專案工作相依性** 實體的更新作業。

下圖顯示工作和團隊成員實體在更新 20、50 和 100 筆記錄且所有受支援欄位都已用上時的執行時間圖。

![更新記錄執行時間圖表。](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>刪除作業
#### <a name="single-record-delete-operations"></a>單一記錄刪除作業
下表顯示刪除單一記錄的執行時間。 時間以秒為單位。

| 記錄類型 | 時間  |
|-------------|-------|
| 工作        | 20.12 |
| 指派  | 10.86 |
| 團隊成員 | 12.52 |
| 相依性  | 20.89 |

> [!NOTE]
> 不支援對 **專案** 實體的刪除作業。

#### <a name="bulk-delete-operations"></a>大量刪除作業
下表顯示刪除許多記錄的執行時間。 具體說來，Microsoft 已測量刪除單一 OperationSet 中 20、50 和 100 筆記錄的執行時間。 時間以秒為單位。

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">記錄&nbsp;&nbsp;&nbsp;類型</th>
    <th class="tg-0lax" colspan="3">時間</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 筆記錄</th>
    <th class="tg-0lax">50 筆記錄</th>
    <th class="tg-0lax">100 筆記錄</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">工作</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">指派</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">團隊成員</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">相依性</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> 不支援對 **專案** 實體的刪除作業。

下圖顯示 **工作**、**指派**、**團隊成員** 和 **相依性** 實體在刪除 20、50 和 100 筆記錄且所有受支援欄位都已用上時的執行時間圖。

![刪除記錄執行時間圖表。](./media/delete-record-execution-time.png)

## <a name="observations"></a>檢驗報告
在每項記錄作業中，**ExecuteOperationSet** API 都需要約 800 毫秒的時間，才能將要求傳送至專案排程服務。 專案排程服務接著需要約五秒時間來處理承載並呼叫 Dataverse。 其餘執行時間則花費在執行商務規則以及將資料寫入 Dataverse 中的資料庫。

建立、更新或刪除 100 筆記錄時，**ExecuteOperationSet** API 需要約三秒鐘的時間，才能將要求傳送至專案排程服務。 專案排程服務接著需要約五秒時間來處理要求並呼叫 Dataverse。 大量作業必須為 OperationSet 中所有的記錄支付 **專案排程服務稅** 一次。 因此，大量作業的平均執行時間顯然比單一記錄作業還要低。

## <a name="scenarios"></a>案例
下表顯示使用專案排程 API 完成特定案例的執行時間。 時間以秒為單位。

| 案例                                                                   | 時間  |
|----------------------------------------------------------------------------|-------|
| 建立含有 40 項工作的專案。                                      | 36.01 |
| 建立含有 40 項工作和 20 個相依性的專案。                  | 38.11 |
| 建立含有 40 項工作和 30 個指派的專案。                   | 60.17 |
| 建立含有 40 項工作、20 個相依性和 30 個指派的專案。 | 60.27 |

## <a name="best-practices"></a>最佳做法
根據前述案例結果，API 在下列情況中表現得更好：

  - 盡可能將許多項作業群組在一起。 大量作業的平均執行階段優於單一記錄作業的平均執行階段。 使用中的 OperationSet 數目越少，平均執行時間就越快。
  - 只設定完成案例所需的最少屬性。 對加入 OperationSet 要求中的非必要欄位類型要有所選擇。 包含外部索引鍵的欄位或彙總欄位會對效能造成負面影響。
