---
title: 專案價目表
description: 本主題提供有關專案價目表實體的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: d09a0dd8234641ca106c37a38d1d721dfb07236c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898656"
---
# <a name="project-price-lists"></a>專案價目表

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 會延伸 Dynamics 365 Sales 中的價目表實體。 

## <a name="key-entities"></a>主要實體

價目表包含四種不同實體所提供的資訊：

- **價目表**：此實體儲存有關定價時間的內容、貨幣、日期有效性和時間單位的資訊。 內容顯示價目表所表示的是成本費率還是銷售費率。 
- **貨幣**：此實體會在價目表上儲存價格的貨幣。 
- **日期**：系統會在嘗試輸入交易的預設價格時使用此實體。 選取的會是其有效日期包含交易日期的價目表。 如果找到多個對交易日期有效且已附加至相關報價、合約或組織單位的價目表，則不會預設使用任何價格。 
- **時間**：此實體會儲存表示價格所指的時間單位，例如每天或每小時費率。 

價目表實體有三個儲存價格的相關表格：

  - **角色價格**：此表格儲存角色與組織單位值的組合費率，並用於設定人力資源的角色型價格。
  - **交易類別價格**：此表格依交易類別儲存價格，並用於設定費用類別價格。
  - **價目表項目**：此表格儲存目錄產品的價格。
 
價目表是費率卡。 費率卡是價目表實體與 [角色價格]、[交易類別價格] 及 [價目表項目] 表格中相關列的組合。

## <a name="resource-roles"></a>資源角色

*資源角色*一詞是指人員必須具備才能執行專案中一組特定工作的一組技能、專長和認證。

人力資源時間是根據資源在特定專案上所擔任的角色進行報價。 人力資源時間是根據資源角色來估算成本並開單收費。 時間可按照**時間**單位群組中的任何單位來定價。

**時間**單位群組是在您安裝 Project Operations 時所建立。 其預設單位是**小時**。 您無法刪除、重新命名或編輯**時間**單位群組的屬性或**小時**單位。 不過，您可以將其他單位新增至**時間**單位群組。 如果嘗試刪除**時間**單位群組或**小時**單位，您可能會在商務規則中造成失敗。
 
## <a name="transaction-categories-and-expense-categories"></a>交易類別與費用類別

專案顧問的差旅及其他費用開支可向客戶收費。 使用價目表完成對費用類別的定價。 機票、旅館和租車是費用類別的範例。 費用的每個價目表明細會指定特定費用類別的定價。 下列三種方法會用來對費用類別進行定價：

- **依照成本**：向客戶收取費用成本，不套用任何加成。
- **加成百分比**：向客戶收取超過實際成本的百分比。 
- **單價**：針對費用類別的每個單位來設定帳單價格。 向客戶收取的金額是根據顧問所報銷的費用單位數來計算。 里程會使用單價定價方式。 例如，里程費用類別可以設定為每天 30 美元 (USD) 或每英里 2 USD。 當顧問報銷專案上的里程時，要收取的帳單金額是根據顧問所報的英里數來計算。
 
## <a name="project-sales-pricing-and-overrides"></a>專案銷售定價和覆寫

對於專案報價和合約，專案價目表的價格覆寫模式與產品價目表的不同。 在產品類別目錄型報價明細上，您可以直接在報價明細上覆寫角色和類別的價格，因為每個報價明細都只指向一個目錄項目。 不過，在專案型報價明細上，您無法直接在報價明細上覆寫角色和類別的價格。 使用專案價目表來支援兩種不同的覆寫模式。

> [!NOTE]
> 建議您讓專案資源和目錄項目使用不同的價目表，因為覆寫定價時，兩者之間的行為有差異。

下列每個實體都可以有一個或多個用於專案定價的相關聯銷售價目表：

- 客戶 (帳戶) 
- 商機 
- 報價 
- 專案合約

這些實體與價目表的關聯是透過專案價目表來表示。 您可以將一個或多個價目表與客戶、商機、報價及專案合約銷售實體建立關聯。

系統不會自動在客戶記錄上輸入預設專案價目表。 不過，您可以手動將專案價目表附加至客戶記錄。 然而，只有在與客戶之間存在自訂定價合約時，您才應該手動附加專案價目表。 

將專案價目表附加至銷售實體時，系統會驗證下列資訊：

- 價目表的內容與**銷售**有關。 
- 價目表貨幣與客戶貨幣相符。 

在專案合約上，使用下列優先順序自動設定相關的專案價目表：

1. 報價
2. 商機​​
3. 客戶 
4. 全域設定 

預設會輸入專案價目表時，系統會驗證貨幣是否與客戶貨幣相符，以及所輸入預設價目表的內容是否與**銷售**有關。

您可以將或多個專案價目表與客戶、商機、報價及專案合約銷售實體建立關聯。 此功能支援長期專案合約的日期特定預設價格，您可能需要多個價目表來處理因通貨膨脹而進行的價格更新。 不過，如果與客戶、商機、報價或專案合約實體建立關聯的價目表有重疊的有效日期範圍，則預設價格可能不正確。 因此，您必須確保有效日期範圍重疊的專案價目表未與這些實體相關聯。

### <a name="deal-specific-price-overrides"></a>交易特定價格覆寫

您可以為在報價或專案合約上預設輸入的專案價目表建立交易特定覆寫。

專案合約預設一律要取得主要銷售價目表的複本，而不是與該價格直接連結。 此行為有助於保證即使主要價目表變更時，針對工作說明書 (SOW) 與客戶達成的價格協議也不會變更。

不過，在報價上，您可以使用主要價目表。 或者，也可以複製主要價目表後再進行編輯，以建立只適用於該報價的自訂價目表。 若要建立專屬於報價的新價目表，請在**報價**頁面上選取**建立自訂定價**。 您只能從報價存取交易特定的專案價目表。 

當您建立自訂專案價目表時，只會複製價目表的專案元件。 換句話說，新價目表已建立為報價上所附加現有專案價目表的複本，而這個新的價目表只有相關的角色價格和交易類別價格
  
## <a name="tracking-costs"></a>追蹤成本

Project Operations 會追蹤專案的人力資源時間使用成本。 還會追蹤專案期間產生的其他費用成本，例如差旅費。

與帳單費率一樣，人力資源也會使用價目表來設定。 以下是成本價目表和銷售價目表在行為上的主要區別：

- 資源的成本費率在特定專案、合約或報價上無法被覆寫。 不過，如果所做變更是交易性質所特有，則可以在每次交易時覆寫帳單比率。 

- 以下順序會用來解析成本價目表：

    1. 附加至組織單位的成本價目表。
    2. 附加至 Project Operations 參數 的成本價目表。 因為可以將使用許多不同貨幣的成本價目表附加至參數，貨幣比較是在專案、合約或報價承包組織單位貨幣與成本價目表貨幣之間完成。
    3. 如果是費用，則依照成本和成本加成定價方式不適用於成本價目表。 即使這些定價方式是在成本價目表明細上用來設定交易類別成本，系統還是會予以忽略，而不會輸入預設成本價。