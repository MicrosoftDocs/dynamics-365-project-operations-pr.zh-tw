---
title: 定價維度概觀
description: 本主題提供有關 Dynamics 365 Project Operations 中定價維度的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128453"
---
# <a name="pricing-dimensions-overview"></a>定價維度概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

設定人力資源所用定價及成本的維度分為兩個類別：

- 人員
- 計劃的工作

因此，有兩種類型的定價維度值可用：

- **選項組**：本身是一組固定列舉值的維度。
- **以實體為準的值**：本身可以是各不相同值集的維度。

## <a name="pricing-dimensions"></a>定價維度

Dynamics 365 Project Operations 隨附一組預設的定價維度。 您可以移至 **Project Operations** > **參數** 來檢視這些定價維度。 在參數記錄的 **以金額為準的定價維度** 索引標籤上，確認角色 **msdyn_resourcecategory** 和資源分配單位 **msdyn_organizationalunit** 的 **適用於銷售** 及 **適用於成本** 欄位已設定為 **是**。 啟用這些欄位後，您就可以設定每個角色與組織單位組合的價格和成本。

如果您需要使用其他屬性來為資源定訂價格或估算成本，則可以建立自訂欄位、實體和維度。

## <a name="pricing-human-resource-time"></a>定訂人力資源時間價格
組織對人力資源時間的定價方式通常是直接影響組織獲利能力的重要策略考量。 當您的組織準備好要確定其設定人力資源時間帳單及成本費率所需的方式時，請與財務團隊和執業負責人合作。

其他定價考量包括是否要重複使用並非目前定價維度但套用做為組織定價維度的欄位或實體。 像 **交易類別** (**msdyn_transactioncategory**) 和 **可預約資源** (**bookableresource**) 等欄位即是候選維度的範例。 

考慮定價維度要使用的是表格還是選項組。 如果您預料維度值的變動會超過 10 或 12，而您在這些值上需要其他屬性時，您可以建立實體，而不是選項組。 維護選項組 (例如新增或移除值) 時，需要系統管理員或開發人員，而將新的列新增至表格則可由大多數使用者來完成。

下列範例顯示根據角色以及資源所隸屬資源分配組織單位所設定的帳單費率。 成本費率通常是根據員工的薪資範圍以及他們所屬組織單位來設定。 在此範例中，帳單費率表和成本費率表看起來如下。

**範例帳單費率**

| 角色        | 組織單位    |單位      |價格      |貨幣  |
| ------------|-------------|----------|----------:|----------|
| 開發人員   | Contoso US  |Hour | 200|USD     |
| 開發人員   | Contoso India |Hour|   112|USD     |


**範例成本費率**

| 薪資範圍     | 組織單位    |單位      |價格      |貨幣  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso US  |Hour | 145|USD     |
| My company_Band2 | Contoso India |Hour|   67|USD     |
