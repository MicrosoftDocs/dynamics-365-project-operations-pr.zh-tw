---
title: 資源管理變更 (Project Service Automation 3.x)
description: 本主題提供有關資源管理區域變更的資訊。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148633"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>資源管理變更 (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

本主題的各節提供有關已對 Dynamics 365 Project Service Automation 3.x 版資源管理區域所做變更的資訊。

## <a name="project-estimates"></a>專案估計值

專案估計值所根據的不是 **msdyn\_projecttask** entity (**Project Task**)，而是 **msdyn\_resourceassignment** entity (**Resource Assignment**)。 資源指派已成為工作排程和定價的「事實原始資料」。

## <a name="line-tasks"></a>明細工作

在 PSA 3.x 中，明細工作已淘汰 (已被取代)。 指派現在會指向整個工作，而不是明細工作。

下列範例顯示名為「測試工作」的工作在舊版 PSA 以及 PSA 3.x 中如何指派給團隊成員 A 和 B。

- **在 PSA 3.x 之前：**

    - 測試工作

        - 測試工作 – 明細工作 1

            - 指派給 A

        - 測試工作 – 明細工作 2

            - 指派給 B

- **PSA 3.x：**

    - 測試工作

        - 指派給 A
        - 指派給 B

## <a name="unassigned-assignment"></a>未分派指派

在 PSA 3.x 中，未分派指派是指派給 **Null** 團隊成員和 **Null** 資源的指派。 未分派指派可能會在幾個案例中發生：

- 如果已建立工作，但尚未將其指派給任何團隊成員，則一律會建立未分派指派。 
- 如果將工作上的所有被指定者移除，就會為該工作重新建立未分派指派。

## <a name="scheduling-fields-on-the-project-task-entity"></a>專案工作實體的排程欄位

**msdyn\_projecttask** 實體的欄位已被取代或已移到 **msdyn\_resourceassignment** 實體，或者現在是從 **msdyn\_projectteam** 實體 (**專案團隊成員**) 中參照這些實體。

| msdyn\_projecttask (專案工作) 上已被取代的欄位 | msdyn\_resourceassignment (資源指派) 上的新欄位 | 註解 |
|---|---|---|
| msdyn\_assignedresources | 無 | |
| msdyn\_assignedteammembers | 無 | |
| msdyn\_numberofresources | 無 | |
| msdyn\_scheduledhours | 無 | |
| msdyn\_effortcontour | msdyn\_plannedwork | 欄位中所儲存 JavaScript 物件標記法 (JSON) 資料結構的格式已變更。 |

## <a name="schedule-contour"></a>排程分佈

排程分佈是儲存在每個 **資源指派** 實體 (**msdyn\_resourceassignment**) 的 **計劃的工作** 欄位 (**msdyn\_plannedwork**)。

### <a name="structure"></a>結構

排程分佈的新結構由針對排程中每一天定義的彈性時間配量所組成。 每個時間配量都有下列屬性：

- **開始** – 根據專案行事曆，當天工作時數的開始時間。
- **結束** – 根據專案行事曆，當天工作時數的結束時間。
- **時數** – 指派的當天時數。

**範例**

此範例使用專案行事曆，其中工作日為 UTC-8 時區上午 9 點到下午 5 點。

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>自動排程和手動排程

如果工作是自動排程，則以前重後輕方式分配時數，而且工作期間可能會減少。

**範例**

下列工作自動排程在三天 (2018 年 12 月 3 日到 2018 年 12 月 5 日) 期間的 18 個小時。

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

如果手動排程工作，則時數會平均分佈到所有日期。

**範例**

下列工作手動排程在三天 (2018 年 12 月 3 日到 2018 年 12 月 5 日) 期間的 18 個小時。

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>指派單位

指派單位在 PSA 3.x 中已被取代。 工作投入時數現在會在所有指派的資源中按天數均分。

**範例**

在此範例中，工作已指派給兩個資源，且自動排程在三天 (2018 年 12 月 3 日到 2018 年 12 月 5 日) 期間的 36 個小時。

- 指派 1：

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- 指派 2：

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>定價維度

在 PSA 3.x 中，資源特有定價維度欄位 (例如 **角色** 和 **組織單位**) 已從 **msdyn\_projecttask** 實體中移除。 這些欄位目前可以在產生專案估計值時，從資源指派 (**msdyn\_resourceassignment**) 的對應專案團隊成員 (**msdyn\_projectteam**) 中擷取。 新的欄位 **msdyn\_organizationalunit** 已新增至 **msdyn\_projectteam** 實體。

| msdyn\_projecttask (專案工作) 上已被取代的欄位 | 改用的 msdyn\_projectteam (專案團隊成員) 中的欄位。 |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>分佈

定價與估計分佈欄位在 **msdyn\_projecttask** 實體上已被取代。 這些欄位已移到 **msdyn\_resourceassignment** 實體。

| msdyn\_projecttask (專案工作) 上已被取代的欄位 | msdyn\_resourceassignment (資源指派) 上的新欄位 |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

下列欄位已新增至 **msdyn\_resourceassignment** 實體：

* msdyn\_plannedcost
* msdyn\_plannedsales

下列規劃、實際和剩餘成本與銷售的欄位在 **msdyn\_projecttask** 實體上保持不變：

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales
