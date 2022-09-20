---
title: 建立廠商發票
description: 本文說明廠商發票的概念，並闡述如何在 Microsoft Dynamics 365 Project Operations 中建立這些發票。
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475408"
---
# <a name="create-vendor-invoices"></a>建立廠商發票

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

若要使用本文所述的功能，您必須啟用 **功能管理** 工作區中的 **啟用使用資源型案例適用的 Project Operations 處理轉包合約實際值** 功能。

Microsoft Dynamics 365 Project Operations 中的廠商發票功能，可用來在廠商所完成的專案上記錄交付服務和/或材料的成本。

當服務和/或材料轉包給廠商時，轉包合約代表與該廠商的契約協議。 當廠商提供服務時，或是當材料經接收並用於專案工作時，會在專案上記錄成本。 廠商接著定期傳送發票。 這些發票會經過驗證，並與專案中記錄的成本相比對。 完成驗證程序後，確認並發放廠商發票以進行付款。

## <a name="scenarios-for-use"></a>使用案例

Project Operations 中的廠商發票可以用來支援兩種不同的案例：

- 客戶使用完整的轉承包體驗。
- 客戶不使用完整的轉承包體驗，但想要在 Project Operations 中對專案上的成本有整合的檢視。

### <a name="customers-use-the-full-subcontracting-experiences"></a>客戶使用完整的轉承包體驗

廠商發票體驗提供一種方法來驗證參考轉包元件的時間項目、材料使用情況和費用項目，並將這些項目與廠商發票明細比對。 此程序可用於驗證廠商發票明細的正確性。 完成驗證程序並確認廠商發票之後，系統會沖回由核准的時間、費用和材料使用記錄所記錄的實際值，然後使用廠商發票明細建立新的成本實際值。

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>客戶不使用完整的轉承包體驗，但想要在 Project Operations 中對專案中的成本有整合的檢視

如果您要在協力廠商系統中追蹤轉包合約程序，則可以建立未參考轉包合約的廠商發票，以將成本從該協力廠商系統記錄到 Project Operations。 如此一來，專案經理對指定專案中的所有成本就可以有單一整合的檢視。

## <a name="create-vendor-invoices-in-project-operations"></a>在 Project Operations 中建立廠商發票

廠商發票是在 Dynamics 365 Finance 中，使用 **應付帳款** 模組所建立。 您無法直接在 Dataverse 中建立廠商發票。

### <a name="set-up-vendor-invoice-verification"></a>設定廠商發票驗證

如果廠商發票是要用於 Dataverse 中的轉包合約，您必須啟用 **需要專案經理手動驗證** 參數。 此選項的設定決定廠商發票是要在 Dataverse 中自動確認，還是需要手動確認。 每個專案廠商發票的標題都包含名稱相同的選項。 所有專案廠商發票標題上的選項預設都會設定為您在此處設定的值。 不過，您可以視需要在個廠商發票的標題中更新此值。

如果選項設定為 **是**，則 Finance 中所建立且已同步處理至 Dataverse 的廠商發票會有 **草稿** 狀態。 專案經理接著必須先驗證並確認發票，才能在 Finance 中處理發票並將其過帳到特定專案和分類帳科目。

如果選項設為 **否**，則會自動確認廠商發票。 不需要進一步的動作。

若要設定廠商發票驗證，請執行以下步驟。

1. 在 Finance 中，移至 **專案管理與會計** \> **設定** \> **專案管理與會計參數**。
1. 在 **財務** 索引標籤上，如果公司原則需要驗證轉包商廠商發票，請將 **需要專案經理手動驗證** 選項設定為 **是**。 如果專案經理不需要在 Dataverse 中進行驗證，則讓選項組保持為 **否**。 **待處理廠商發票** 頁面上預設會使用此設定。

> [!NOTE]
> 只有在必須 **需要專案經理手動驗證** 選項設為 **是** 時，才能正確處理 Dataverse 中所建立轉包合約廠商發票。 只有在此選項設定為 **是** 時，才可以由專案經理手動將轉包商所建立的時間、材料和費用成本實際值與廠商發票明細行進行比對。

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>設定廠商發票的採購整合科目

在 Project Operations – 整合環境 (非庫存) 適用的 Finance 中過帳廠商發票時，財務資料會過帳至採購整合科目。 系統會在 Dataverse 中產生已過帳發票的實際值。 這些實際值是使用專案整合帳目在 Finance 中進行過帳。 專案整合帳目的過帳功能會過帳實際成本，並沖回採購整合科目。

若要設定廠商發票的採購整合科目，請執行下列步驟。

1. 在 Finance 中，移至 **專案管理與會計** \> **設定** \> **專案管理與會計參數**。
1. 在 **Dynamics 365 Customer Engagement 上的 Project Operations** 索引標籤中，選取 **材料** \> **採購整合科目**。

### <a name="create-and-post-subcontract-vendor-invoices"></a>建立和過帳轉包合約廠商發票

應付帳款記帳員從轉包商收到發票時，會在 Finance 中建立新發票。

1. 在 Finance 中，移至 **應付帳款** \> **發票** \> **待處理廠商發票**。
1. 在 **動作窗格** 上，選擇 **新增** 以建立廠商發票。
1. 在發票標題的 **發票帳戶** 欄位中，選取 **轉包商**。
1. 選取發票日期。
1. 在 **標題** 索引標籤上，將 **需要專案經理手動驗證** 選項設定為 **是**。 此選項的預設設定來自 **專案管理與會計參數** 頁面。 不過，您可以在廠商發票層級變更此設定。
1. 在 **發票明細** FastTab 上，選取 **新增明細** 以建立廠商發票明細。
1. 選取轉包合約服務內容已建立的採購類別，並輸入單價、度量單位和數量。
1. 在廠商發票明細區段的 **專案** 索引標籤上，選取轉包商共用轉包合約發票的專案。
1. 選取專案類別。 這可以是任何類型的 **項目**、**費用**、**材料** 或 **時數**。
1. 只有在所選專案類別的類型為 **時數** 時，才台選取角色。
1. 選取 **過帳** 以過帳廠商發票。

或者，也可以移至 **應付帳款**\>**發票**\>**未結廠商發票**，並選取 **新增**。

廠商發票過帳後，即可在 Dataverse 中找到以供專案經理驗證並處理。

## <a name="vendor-invoice-processing-in-dataverse"></a>Dataverse 中的廠商發票處理

在使用 Dataverse 所建立的廠商發票中，部分欄位值來自於 Finance 中記錄的廠商發票。 其他值是來自轉包合約的預設值。

下列欄位和相關記錄會從轉包合約複製到廠商發票的標題：

- 貨幣
- 合約單位
- 付款條件

在廠商發票明細中，Project Operations 會使用下列欄位值來輸入預設轉包合約和轉包合約服務內容參考：

- 交易分類
- 角色
- 交易類別
- 產品欄位
- 專案
- 工作

> [!NOTE]
> Project Operations 不支援固定價格轉包合約服務內容。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
