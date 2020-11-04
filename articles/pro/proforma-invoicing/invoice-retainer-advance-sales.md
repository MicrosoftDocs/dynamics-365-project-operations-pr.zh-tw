---
title: 開立定額保留後隨用即扣型付款或預付金的發票
description: 本主題提供有關如何在 Project Operations 中開立定額保留後隨用即扣型付款 (保留款) 或預付金發票的資訊。
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ed3b71d5f0ac035403de9fa213f3f45d14038e0
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087838"
---
# <a name="invoice-a-retainer-or-an-advance"></a>開立定額保留後隨用即扣型付款或預付金的發票

_**適用於：** 精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 支援定額保留後隨用即扣型合約 (保留款型合約) 和一次性預付金。 在專案合約上，您可以記錄保留款排程或一次性預付金。 不過，在專案合約層級上所做的記錄並不會立即讓保留款或預付金變成可供使用。 若要在實際收取客戶費用的發票上使用保留款或預付金，必須先開立保留款或預付金的發票。

完成下列步驟，開立保留款或預付金的發票。

1. 選取 **銷售** > **帳單** > **保留款和預付金** 。 
2. 在 **預付金和保留款** 頁面上，使用篩選來選取要開立發票的特定保留款或預付金，並將其標示為 **已準備好開立發票** 。
3. 從 **專案合約** 清單或詳細資料頁面手動建立發票。 保留款或預付金會在 **發票** 頁面的 **預付金和保留款** 區段中，顯示於草稿發票。
4. 確認發票。 這會讓保留款或預付金變成可供使用。 您可以在 **保留款或預付金** 清單頁面上驗證發票。 已開發票預付金或保留款的可用金額會顯示在網格中。

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>從發票網格中建立保留款或預付金

您可以直接在發票上建立保留款或預付金。

1. 在草稿發票的 **預付金和保留款** 子格上，選取 **新增** 以建立新的保留款或預付金。 
2. 在 **快速建立** 頁面上，新增必要的資訊，然後選取 **儲存** 。 與發票相關的專案合約上會建立保留款或預付金。 保留款或預付金會自動標示為 **已準備好開立發票** ，然後新增至 **發票** 頁面的 **預付金和保留款** 子格。

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>協調已開發票的保留款或預付金

開立保留款或預付金的發票之後，即可在發票上使用，或是與時間、費用、里程碑或其他專案型費用進行差異協調。 客戶會看到他們的發票金額已扣減掉對此發票使用的保留款或預付金。

在每份為含有已開發票保留款或預付金之專案合約所產生的發票上，Project Operation 會自動將該保留款或預付金套用至發票。

這可在 **發票** 頁面的 **已套用的保留款和預付金** 網格中看到。 下表提供有關 **專案發票** 頁面的 **已套用的保留款和預付金** 網格中欄位的資訊。

| 欄位 | 地點 | 關聯性、目的和指引 | 下游影響 |
| --- | --- | --- | --- |
| 描述 | **專案發票** 頁面上的 **已套用的預付金和保留款** 網格 |此唯讀欄位提供此發票中所用保留款或預付金的描述。 您可以在發票上變更此值。 您可以在 **專案合約** 頁面的子格上更新此值。 | 此欄位可以在列印的發票上顯示給客戶，以指出發票上套用的是哪一筆保留款或預付金。 |
| 交付日期 | **專案發票** 頁面上的 **已套用的預付金和保留款** 網格  | 此唯讀欄位提供此發票中所用保留款或預付金的發票日期。 您可以在發票上變更此值。 您可以在 **專案合約** 頁面的子格上更新此值。 | 此欄位可以在列印的發票上顯示給客戶，以指示第一次開立保留款或預付金發票給客戶時的日期。 |
| 總數 | **專案發票** 頁面上的 **已套用的預付金和保留款** 網格  | 此唯讀欄位提供此發票中所用保留款或預付金的金額。 您可以在發票上變更此值。 您可以在 **專案合約** 頁面的子格上更新此值。 | 此欄位可以在列印的發票上顯示給客戶，以指示客戶所支付保留款或預付金的原始金額。 |
| 已用金額 | **專案發票** 頁面上的 **已套用的預付金和保留款** 網格  | 此唯讀欄位提供總結已使用多少保留款或預付金的計算值。 | 此欄位可以在列印的發票上顯示給客戶，以指示已從此保留款或預付金支用的金額。 |
| 應收金額 | **專案發票** 頁面上的 **已套用的預付金和保留款** 網格  | 此可編輯欄位提供此專案發票中所用保留款或預付金的金額。 這筆金額不可大於預付金的可用金額。 系統會自動將此金額計算為網格中 **金額** 與 **已使用金額** 欄位之間的差異。 您可以減少此金額來使用少於可用值的金額，但是無法增加金額來使用大於可用值的金額。 | 此欄位可以在列印的發票上顯示給客戶，以指示發票從此保留款或預付金中支用的金額。 |
| 保留款餘額。 | **專案發票** 頁面上的 **已套用的預付金和保留款** 網格  | 此唯讀欄位提供保留款或預付金在確認發票後所剩金額的值。 | 此欄位可以在列印的發票上顯示給客戶，以指示此保留款或預付金在發票經確認並付款後將會剩餘的金額。 |