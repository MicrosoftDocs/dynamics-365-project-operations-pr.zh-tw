---
title: 組織單位
description: 本主題提供有關 Dynamics 365 Project Service Automation 中組織單位的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
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
ms.openlocfilehash: c1c86ce98213fba54fd2b477d4df6f8dc5409d55
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145619"
---
# <a name="organizational-units"></a>組織單位 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

在 Dynamics 365 Project Service Automation 中，組織單位是專業服務公司的不同群組或部門，雇用有成本費率的計費資源。

對雇用各種業務範圍或行業別中技術資源的專業服務公司來說，在不同業務範圍或行業別中填補職能角色所需付出的成本可能會各不相同。 組織單位這個概念在此案例中有其用處，提供了一種可在公司賦予這些角色不同成本結構的部門中將一組計費角色設為群組的方法

## <a name="key-attributes-and-associations-of-organizational-units"></a>組織單位的主要屬性與關聯

在 PSA 中，PSA 的組織單位有特定貨幣和特定成本價目表。

組織單位的貨幣是用來追蹤成本的主要貨幣。

可以將一個或多個成本價目表附加至每個組織單位。 PSA 對於可附加至組織單位的價目表施加下列限制：

- 價目表必須以組織單位的貨幣計價
- 價目表必須是成本價目表

此外，資源實體上還有組織單位專用的屬性。 每個資源只能指派至一個組織單位。

## <a name="roles-of-organizational-units"></a>組織單位中的角色

組織單位在 PSA 中扮演兩種角色：

- **承包單位** – 代表公司中主要負責贏得銷售和管理客戶工作與服務交付之群組或部門的組織單位。 承包單位是依據 **商機**、**報價**、**專案合約** 及 **專案** 頁面標頭區段中的 **承包單位** 欄位來識別。
- **資源分配單位** – 資源所隸屬於或指派至的組織單位。 此組織單位可以為工作說明書 (SOW) 上的一些角色以及承包單位負責的專案提供其資源。

> ![承包單位和資源分配單位](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>組織單位常見問題集

以下是一些有關組織單位的最常見問題。

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>PSA 中的組織單位實體與 Dynamics 365 中既存的組織實體有什麼關聯？

Microsoft Dynamics 365 中的組織實體代表全域 Dynamics 365 執行個體的名稱。 此名稱通常是全域企業的名稱。

組織單位實體代表全域企業中的群組或部門。 此群組或部門有一組角色以及這些角色專用的成本價目表，而這些角色及價目表與企業中其他群組或部門的角色及價目表不同。

安裝 PSA 時，會根據組織建立預設組織單位。 所有現有資源都會指派至預設組織單位。 如果將任何新的 Active Directory 使用者或資源匯入 Dynamics 365，則使用者匯入程序會將其指派給 PSA 中的預設組織單位。
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>組織單位實體與業務單位實體有何不同？

在 Dynamics 365 中，業務單位實體是一個安全性建構。 使用者與業務單位的關聯決定使用者有權存取的實體和實體記錄。 此關聯也決定了使用者對這些實體記錄所擁有的權限 (建立、讀取、寫入、刪除、附加、附加至、指派或共用)。

組織單位實體代表將不同成本費率賦予指派至此實體之員工的公司群組或部門。 資源與組織單位的關聯決定資源的專案業務開發成本。

實作 Dynamics 365 時，請最佳化業務單位階層的安全性授權以及對業務單位的使用者指派。 將所有通常必須存取同一組記錄的使用者指派給相同的業務單位。 組織單位對安全性授權或存取權沒有任何影響。

#### <a name="example-of-organizational-units-and-business-units"></a>組織單位和業務單位的範例

Contoso, Ltd. 有業績興旺的 Microsoft 技術業務營運。 允章和美玲都是 C\# 開發人員，但是美玲在美國，而允章在印度。 大部分專案業務開發都需要來自 Contoso India 和 Contoso US 的資源，而允章和美玲對此業務範圍中的專案需要相同的安全性存取層級。 不過，Contoso India 的開發人員成本與 Contoso US 的開發人員成本明顯不同。

以下是使用 Dynamics 365 和 PSA 設計此案例的最佳方式。

1. 建立 Microsoft 技術業務營運做為業務單位，並建立允章及美玲與其之間的關聯。 如此一來，就有助於保證這兩位員工對該業務範圍中的任何專案都有相同的安全性存取層級。 他們都可以檢查進度並報告時間、費用及工作更新。 
2. 建立兩個組織單位以保證正確反映專案的成本。 
3. 將美玲與 Contoso US 建立關聯，並將允章與 Contoso India 建立關聯。
4. 將適當的成本價目表指派給這兩個組織單位。 如此一來，就有助於保證允章和美玲專案中記錄的成本準確反映 Contoso US 與 Contoso India 之間的成本差異。

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>組織單位與 Dynamics 365 中的銷售領域有關聯嗎？

銷售領域與組織單位之間不存在關聯或關係。 銷售領域通常是進行銷售的地理區域。 銷售價目表可以與每個銷售領域產生關聯。

組織單位是公司的內部群組或部門，會追蹤其出售一組角色給其他部目或外部客戶的成本。

#### <a name="example-of-organizational-units-and-sales-territories"></a>組織單位和銷售領域的範例

Contoso, Ltd. 有兩個開發中心：Contoso US 和 Contoso India。 這兩個開發中心之間的資源成本大幅不同。

Contoso 在許多國際市場上銷售其 IT 服務，例如拉丁美洲、北美洲、亞太地區、西歐和中東。 相同專案角色的帳單費率在這些不同市場上可能會有很大變化。

您應將 Contoso US 和 Contoso India 設定為組織單位，而且每個組織單位都必須有其本身的成本價目表。 亞太地區、拉丁美洲、北美洲、西歐和中東地區應設定為銷售領域，而且每個銷售領域都必須有其本身的銷售價目表。

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>為什麼價目表與組織單位的關聯會有限制？ 

銷售定價通常是售出服務的目標地理區域或市場所獨有。 公司的內部部門對相同類型的服務，通常不會有其本身的銷售定價。 不過，內部部門會有不同的銷貨成本 (COGS)，取決於他們所雇用人員的技能以及其營業所在地區的勞動條件。 由於組織單位以公司內部部門為模型，因此只能有成本價目表。

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>為什麼無法將銷售價目表與組織單位建立關聯？

在 PSA 中，銷售價目表可以與客戶及銷售領域產生關聯。 商機、報價、專案合約和專案等交易實體會使用附加至客戶帳戶或銷售領域的銷售價目表，來判斷專案業務開發的帳單費率和可能營收。

成本價目表與組織單位產生關聯。 商機、報價、專案合約和專案等交易實體會使用會使用附加至承包單位的成本價目表，來判斷專案業務開發的成本。

### <a name="are-organizational-units-hierarchical-in-psa"></a>PSA 中的組織單位是階層式嗎？

編號 在目前的 PSA 版本中，組織單位不是階層式。 這表示您無法執行下列動作：

- 設定用於預設成本價、向上周遊階層的模式。 
- 報告組織單位階層在不同層級上彙總的營收或成本。

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>我們是一家大型跨國公司，有複雜的多級階層成本中心、部門和帳務辦公室。 如何充分利用此版本 Project Service 應用程式中的組織單位概念？

當您有階層複雜的成本中心、部門、帳務辦公室及其他時，請將該階層的分葉節點設定為不同的組織單位。
下列範例顯示一般的階層：

**Contoso India**

  - SAP 業務營運 

    - 技術顧問 
    - 職能顧問 
    
  - Microsoft 技術業務營運 

    - 技術顧問
    - 職能顧問 
    
**Contoso US**

 - SAP 業務營運 

    - 技術顧問 
    - 職能顧問 
    
 - Microsoft 技術業務營運 

    - 技術顧問 
    - 職能顧問 
 
如果您的階層也類似，您必須將其設定為一般清單，如下所示：
- Contoso India - SAP 業務營運 - 技術顧問 
- Contoso India - SAP 業務營運 - 職能顧問       
- Contoso India - Microsoft 技術業務營運 - 職能顧問 
- Contoso India - Microsoft 技術業務營運 - 職能顧問 
- Contoso US - SAP 業務營運 - 技術顧問  
- Contoso US - SAP 業務營運 - 職能顧問  
- Contoso US - Microsoft 技術業務營運 - 技術顧問 
- Contoso US - Microsoft 技術業務營運 - 職能顧問

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>我們是一家只以一個部門來營運的小型專業服務公司。 如何妥善運用最新 PSA 版本中的組織單位概念？

如果您公司只以一個有一份成本價目表的單位來營運，則不需要設定任何組織單位。 進行 PSA 安裝時，Dynamics 365 會建立一個與組織同名的預設組織單位。 所有使用者預設都會指派至此組織單位。 每當系統要求選取組織單位時，預設都會選取此組織單位。

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>從報價或專案合約服務內容建立專案時，預設承包單位來自報價或專案合約。 如果在銷售實體 (例如報價或專案合約) 之前建立專案，預設承包單位是什麼？

自行建立專案時，專案的預設承包單位是以建立該專案的使用者為準。 該使用者也是預設專案經理。 如果專案已對應至銷售實體 (例如報價或專案合約)，則專案的承包單位改以銷售實體為準。 在此案例中，可能會重新計算專案估計值，因為如果承包單位已變更，則會使用成本價目表來計算成本估計變更。 銷售價目表會用來計算為了與報價相關專案價目表同步而變更的銷售估計。

專案的 **承包單位** 和 **貨幣** 欄位已鎖定，無法編輯，因為這些欄位必須與專案所對應至銷售實體 (報價或專案合約) 的值同步。
