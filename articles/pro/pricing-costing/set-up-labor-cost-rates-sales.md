---
title: 設定人力成本費率 - 精簡
description: 本文提供有關如何在 Project Operations 中設定人力成本費率的資訊。
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 77e47fb1e76229bb7f52deb9b5472d04bb180623
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925984"
---
# <a name="set-up-labor-cost-rates---lite"></a>設定人力成本費率 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_

每個價目表都有一組與價目表內容及日期有效性一致的人力費率 (角色價格)。

1. 建立價目表，並在 **角色價格** 索引標籤的子格中，選取 **新增角色**。
2. 在 **快速建立** 頁面上，選取角色和組織單位。
3. 輸入任何其他必要欄位資訊。

下表包括一些在成本價目表上建立人力費率時很重要的欄位。

| 欄位 | 地點 | 描述 | 下游影響 |
| --- | --- | --- | --- |
| 角色 | **一般** 索引標籤和 **快速建立** 頁面 | 選取套用成本費率的角色。 | 新加入估計值或實際值的角色將會根據此明細進行比對，以設定角色的成本預設值。 |
| 資源分配單位 | **一般** 索引標籤和 **快速建立** 頁面 | 選取將使用此角色的公司組織單位或部門。 例如，Fabrikam India 機器人部門的開發人員或 Fabrikam USA 軟體部門的開發人員。 | 新加入估計值或實際值的資源分配單位將會根據此明細進行比對，以設定角色的成本預設值。 |
| 價格 | **一般** 索引標籤和 **快速建立** 頁面 | 設定角色、資源供應公司與資源分配單位組合的成本費率。 例如，Fabrikam India 開發人員的成本為 1000 印度幣，或 Fabrikam USA 開發人員的成本為 150 美元。 | 價格是 **時間** 交易分類新加入估計或實際明細的每單位成本預設使用的成本費率。 |
| 貨幣 | **一般** 索引標籤和 **快速建立** 頁面 | 根據預設，貨幣值來自成本價目表標題的貨幣，但是可以覆寫。 例如，Fabrikam India 開發人員的成本為 1000 印度幣。 Fabrikam USA 開發人員的成本為 150 美元。 | **時間** 交易分類新加入實際成本明細的每單位成本預設會使用此貨幣。 在專案估計值上，貨幣值會轉換成專案貨幣，並顯示在估計值的分時期檢視表中。 |
| 單位排程 | **一般** 索引標籤和 **快速建立** 頁面 | 單位排程預設為 [時間] 且無法在 [角色價格] 實體上進行變更，因為這會用來依時間單位表示費率。 | 沒有任何下游影響。 |
| 單位 | **一般** 索引標籤和 **快速建立** 頁面 | 根據預設，此值來自成本價目表標題上的 **時間單位** 欄位。 此值可以覆寫。 例如，Fabrikam India 開發人員的成本為每個 **印度日** 1000 印度幣。 Fabrikam USA 開發人員的成本為每個 **美國日** 150 美元。 | 系統會使用依照基礎單位的單位制及轉換方式，計算每個單位成本，以核算出新加入估計或實際明細的預設單價。 例如，對印度開發人員的估計為需時 10 個 **印度日** 的工作，而 **印度日** 這個單位則定義為 10 小時。 計算估計明細的成本時，應用程式計算估計值單位成本的方式為：1000 印度幣/ 10 小時 = 每小時 100 印度幣，這會轉換成美元，並顯示為 **專案估計值** 頁面上的單位成本。 |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>您的部門或法律實體以外資源的轉撥定價及成本

在以專案為主的公司中，通常會在專案上任用來自不同法律實體或部門的員工。 專案可以由一個法律實體執行，但是在專案上工作的員工或顧問則可能來自相同法律實體或不同法律實體，或是兩者的組合。 在 Dynamics 365 Project Operations 中，負責交付專案的法律實體是 **負責公司**，而負責交付的部門則是 **合約單位**。 其他提供資源的法律實體是 **資源供應公司**，而提供資源的部門則是 **資源分配單位**。 在大部分國家/地區中，公司必須確保提供資源的法律實體或部門向負責公司或合約單位收取使用資源的費用。

例如，Fabrikam 公司必須確保 Fabrikam India-Robotics 已與 Fabrikam US-Robotics 或 Fabrikam UK-Robotics 之間議定成本費率卡。

Fabrikam India-Robotics 的開發人員，出借給 Fabrikam US-Robotics 時收費 $100，出借給 Fabrikam UK-Robotics 時收費 $150。

### <a name="set-up-costs-for-outside-resources"></a>設定外部資源的成本

1. 建立名為 *Fabrikam US-Robotics 成本費率* 的成本價目表，並設定有效日期範圍。
2. 在成本價目表中，使用下表中的資訊來設定費率。 

| 角色 | 資源供應公司 | 資源分配單位 | 成本費率 |
| --- | --- | --- | --- |
| Developer | Fabrikam India | Fabrikam India-Robotics | $100 |
| Developer | Fabrikam Philippines | Fabrikam Philippines-Robotics | $90 |
| Developer | Fabrikam US | Fabrikam US-Robotics | $150 |

3. 將此成本價目表附加至 Fabrikam US-Robotics 組織單位。

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>以適當的貨幣設定資源的轉撥價格 

在 Project Operations 中，可以使用任何貨幣來設定資源定價。 貨幣會預設為價目表標題上的貨幣，但是可加以變更。

使用轉撥價格設定範例，此資訊可以變更為：

例如，Fabrikam 公司必須確保 Fabrikam India-Robotics 已與 Fabrikam US-Robotics 或 Fabrikam UK-Robotics 之間議定成本費率。

Fabrikam India-Robotics 的開發人員，出借給 Fabrikam US-Robotics 時的成本為 $5000，出借給 Fabrikam UK-Robotics 時的成本為 $5500。

在 Fabrikam US-Robotics 的成本價目表中，可將成本費率表示為：

| 角色 | 資源供應公司 | 成本 |
| --- | --- | --- |
| Developer | Fabrikam India | 5000 印度幣 |
| Developer | Fabrikam US | 115 美元 |

在 Fabrikam UK-Robotics 的成本價目表中，可將成本費率表示如下：

| 角色 | 資源供應公司 | 成本 |
| --- | --- | --- |
| Developer | Fabrikam India | 5500 印度幣 |
| Developer | Fabrikam UK | 115 英鎊 |

成本價目表可以用多種貨幣提供人力費率。 產生對專案的成本估計值時，Project Operations 會將成本費率轉換成專案貨幣，並將其顯示給使用者。 當時間項目獲核准且成本實際值已建立時，此成本實際值是以該相應角色價格在成本價目表上的貨幣來計價。 單一專案的時間成本實際值可以用多種貨幣來記錄。 不過，在專案層級上彙總或總結實際人力成本時，Project Operations 會將所有人力成本金額轉換為使用者可以檢視的專案貨幣。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]