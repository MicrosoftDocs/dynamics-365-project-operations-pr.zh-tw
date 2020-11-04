---
title: 定價和成本維度首頁
description: 本主題提供定價維度的概觀。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073037"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>定價和成本維度首頁

在專案型組織中用來設定人力定價和成本估算的維度，受到下列屬性影響：

- 從事與其經驗、角色或地理區域類似之工作的人員
- 要以類似其複雜度或每天時間來執行的工作

考慮到工作的這些屬性的獨特性質以及執行工作所需的人員，Project Service Automation 有兩種類型的定價維度值可供使用： 

- **選項組** - 本身是一組固定列舉值的屬性。
- **以實體為準的值** - 本身可以包含有限但可能隨時間變更之各不相同值集的屬性。

## <a name="pricing-dimensions"></a>定價維度

PSA 隨附一組預設定價維度。 您可以移至 **Project Service** > **參數** 來檢視這些維度。 在參數記錄的 **以金額為準的定價維度** 索引標籤上，確認角色 **msdyn_resourcecategory** 和資源分配單位 **msdyn_organizationalunit** 的 **適用於銷售** 及 **適用於成本** 欄位已設定為 **是** 。 這可讓您設定每個角色與組織單位組合的價格和成本。

![反白顯示「適用於銷售」的 Project Service 參數螢幕擷取畫面](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> 如果您在 PSA 版本 3 之前一直都使用角色和組織單位的預設欄位做為定價維度，就不會有任何看得出的變更。 您可以繼續照常使用 Project Service。 

如果您需要使用其他屬性來為資源定訂價格或估算成本，則可以建立自訂欄位、實體和維度。 如需詳細資訊，請參閱下列主題，但請注意，您必須依照下列順序完成程序：

- [建立自訂欄位和實體](create-custom-fields-entities.md)
- [將自訂欄位新增至價格設定與交易實體](field-references.md)
- [將自訂欄位設定為定價維度](set-up-pricing-dimensions.md)
- [更新外掛程式屬性以包含新的定價維度](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>定訂人力資源時間價格
組織對人力資源時間的定價方式通常是直接影響組織獲利能力的重要策略考量。 當您的組織準備好要確定其設定人力資源時間帳單及成本費率所需的方式時，請與財務團隊和執業負責人合作。

其他定價考量包括是否要重複使用並非目前定價維度但套用做為組織定價維度的欄位或實體。 像 **交易類別** ( **msdyn_transactioncategory** ) 和 **可預約資源** ( **bookableresource** ) 等欄位即是候選維度的範例。 

考慮定價維度要使用的是表格還是選項組。 如果您預料維度值的變動會超過 10 或 12，而您在這些值上需要其他屬性時，請建立實體，而不是選項組。 維護選項組 (例如新增或移除值) 時，需要系統管理員或開發人員，而將新的列新增至表格則可由大多數商務使用者來完成。

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
