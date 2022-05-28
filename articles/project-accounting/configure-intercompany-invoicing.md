---
title: 設定公司間開立發票
description: 此主題提供設定專案的公司間開立發票的資訊與範例。
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ad6022670048e5aa3635998852b78c49af461d4e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591578"
---
# <a name="configure-intercompany-invoicing"></a>設定公司間開立發票

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

完成下列步驟，在 Dynamics 365 Project Operations 中設定專案的公司間開立發票。 公司間交易是專案合約中屬於一個公司或組織單位的時間和費用交易，而專案合約上的資源是另一公司或組織單位的一部分。

## <a name="example-configure-intercompany-invoicing"></a>範例：設定公司間開立發票

在下列範例中，Contoso Robotics USA (USPM) 是借方法律實體，Contoso Robotics UK (GBPM) 是貸方法律實體。 

1. **設定法律實體之間的公司間會計**。 必須在總帳[公司間會計](/dynamics365/finance/general-ledger/intercompany-accounting-setup)頁面中設定每一對借方和貸方法律實體。
    
    1. 在 Dynamics 365 Finance 中，移至 **總帳** > **過帳設定** > **公司間會計**。 建立包含下列資訊的記錄：

        - **起源公司** = **GBPM**
        - **目的地公司** = **USPM**

2. **設定法律實體之間的貿易關係**。 必須在貸方法律實體中建立代表借方法律實體的客戶記錄。 必須在借方法律實體中建立代表貸方法律實體的廠商記錄。

     1. 在 [財務] 中，選取法律實體 **GBPM**。
     2. 移至 **應收帳款** > **客戶** > **所有客戶**。 建立法律實體 **USPM** 的新記錄。
     3. 展開 **名稱**、依據 **類型** 篩選記錄並選取 **法律實體**。 
     4. 尋找並選取 **Contoso Robotics USA (USPM)** 的客戶記錄。
     5. 選取 **使用符合項**。 
     6. 選取客戶群組 **50 - 公司間客戶**，然後儲存記錄。
     7. 選取法律實體 **USPM**。
     8. 移至 **應付帳款** > **廠商** > **所有廠商**。 建立法律實體 **GBPM** 的新記錄。
     9. 展開 **名稱**、依據 **類型** 篩選記錄並選取 **法律實體**。 
     10. 尋找並選取 **Contoso Robotics UK (GBPM)** 的客戶記錄。
     11. 選取 **使用符合項**、選取廠商群組，然後儲存該記錄。
     12. 在廠商記錄中，選取 **一般** > **設定** > **公司間**。
     13. 在 **貿易關係** 索引標籤上，將 **使用中** 設定為 **是**。
     14. 將 **客戶公司** 欄位設定為 **GBPM**，並在 **我的客戶記錄** 中，選取您先前在程序中建立的客戶記錄。

3. **在專案管理與會計參數中設定公司間設定**。 

    1. 選取法律實體 **USPM**，然後移至 **專案管理和會計** > **設定** > **專案管理和會計參數**。
    2. 在 **公司間** 索引標籤上，選取採購類別，以符合自動產生的廠商發票。
    3. 在 **預設類別** 中，選取 **公司間資源**。
    4. 選取法律實體 **GBPM**，然後移至 **專案管理和會計** > **設定** > **專案管理和會計參數**。
    5. 在 **公司間** 索引標籤 中，為每個交易類型選取預設專案類別。 當公司間交易的發票類別只存在於借用法律實體時，使用專案類別進行稅務設定。 您可以選擇計提公司間交易的營收。 當交易是透過貸方法律實體中的 Project Operations 整合帳目來過帳時，便會發生應計值。 在過帳公司間發票時，會沖銷該日記帳。
    6. 在 **當貸方資源** 群組中，選取 **...** > **新增**。 
    7. 在網格中選取下列資訊：

          - **借方法律實體** = **USPM**
          - **應計營收** = **是**
          - **預設時程表類別** = **預設 – 工時**
          - **預設費用類別** = **預設 – 費用**

4. **在分類帳過帳設定中設定公司間成本與營收科目**。 當公司間客戶發票在貸方法律實體中過帳時，公司間營收科目會記入貸項。 當相符的擱置中廠商發票在借方法律實體中過帳時，公司間成本科目會記入借項。 這些科目是在對應的法律實體中設定的。 
      
     1. 在財務中，選取借方法律實體 **USPM**。 
     2. 移至 **專案管理與會計** > **設定** > **過帳** > **分類帳過帳設定**。 
     3. 在 **成本科目** 索引標籤的 **總帳科目類型** 中，選取 **公司間成本**。 建立包含下列資訊的新記錄：
      
        - **貸方法律實體** = **GBPM**
        - **主要科目** = 選取公司間成本的主要科目。 這是必要的設定。 此設定用於 Finance 中的公司間流程，但不會在與專案相關的公司間流程中使用。 此選取項目沒有下游影響。 
        
     4. 選取貸方法律實體 **GBPM**。 
     5. 移至 **專案管理與會計** > **設定** > **過帳** > **分類帳過帳設定**。 
     6. 在 **營收科目** 索引標籤的 **總帳科目類型** 中，選取 **公司間營收**。 建立包含下列資訊的新記錄：

        - **借方法律實體** = **USPM**
        - **主要科目** = 選取公司間營收的主要科目。 這是必要的設定。 此設定用於 Finance 中的公司間流程，但不會在與專案相關的公司間流程中使用。 此選取項目沒有下游影響。 

5. **設定人力的轉移定價**。 在 Dataverse 的 Project Operations 中設定公司間轉移定價。 設定公司間開立發票的[人力成本費率](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity)和[人力帳單費率](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions)。 公司間費用交易不支援轉移定價。 組織間的單位銷售價格永遠會設定成與資源分配單位成本價相同的值。

      Contoso Robotics UK 中的開發人員資源成本為每小時 88 GBP。 Contoso Robotics UK 將為此資源在美國專案上的工作向 Contoso Robotics USA 收取每小時 120 美元。 Contoso Robotics USA 將針對 Contoso Robotics UK 開發人員資源完成的工作，向客戶 Adventure Works 收取 200 美元。

      1. 在 Dataverse 上的 Project Operations 中，移至 **銷售** > **價目表**。 建立稱為 **Contoso Robotics UK 成本費率** 的新成本價目表。 
      2. 在成本價目表中，使用下列資訊建立記錄：
         - **角色** = **開發人員**
         - **成本** = **88 英鎊**
      3. 移至 **設定** > **組織單位**，並將此成本價目表附加至 **Contoso Robotics UK** 組織單位。
      4. 移至 **銷售** > **價目表**。 建立稱為 **Contoso Robotics USA 成本費率** 的成本價目表。 
      5. 在成本價目表中，使用下列資訊建立記錄：
          - **角色** = **開發人員**
          - **資源供應公司** = **Contoso Robotics UK**
          - **成本** = **120 美元**
      6. 移至 **設定** > **組織單位**，並將 **Contoso Robotics USA 成本費率** 成本價目表附加至 **Contoso Robotics USA** 組織單位。
      7. 移至 **銷售** > **價目表**。 建立名為 **Adventure Works 帳單費率** 的銷售價目表。 
      8. 在銷售價目表中，使用下列資訊建立記錄：
          - **角色** = **開發人員**
          - **資源供應公司** = **Contoso Robotics UK**
          - **帳單費率** = **200 美元**
      9. 移至 **銷售** > **專案合約**，並將 **Adventure Works 帳單費率** 價目表附加至專案合約的 Adventure Works 專案價目表。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
