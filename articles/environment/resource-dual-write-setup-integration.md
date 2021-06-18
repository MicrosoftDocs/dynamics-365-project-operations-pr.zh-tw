---
title: Project Operations 設定和設定資料整合
description: 本主題提供有關設定和配置 Project Operations 雙重寫入對應的資訊。
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001056"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations 設定和設定資料整合

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本主題提供有關 Project Operations 雙重寫入設定和設定資料整合的資訊。

## <a name="project-contracts-contract-lines-and-projects"></a>專案合約、合約服務內容和專案

專案合約、合約服務內容和專案是在 Dataverse 中所建立，並同步處理至 Finance and Operations應用程式以用於其他會計。 您只能在 Dataverse 中建立和刪除這些實體中的記錄。 不過，在 Finance and Operations 應用程式中，可以將會計屬性 (例如銷售稅群組預設值和財務維度) 新增至這些記錄。

  ![專案合約整合概念](./media/1ProjectContract.jpg)

銷售活動潛在客戶、商機和報價是在 Dataverse 中進行追蹤，並不會同步處理至 Finance and Operations 應用程式，因為沒有與此活動相關聯的下游會計。

Dataverse 中的專案合約功能會使用 **專案合約標題 (salesorders)** 資料表對應，在 Finance and Operations 應用程式中建立專案合約記錄。 在 Dataverse 中儲存專案合約，也會開始建立專案合約客戶實體記錄。 此記錄會使用 **專案資金來源 (msdyn\_projectcontractssplitbillingrules)** 資料表對應來同步處理至 Finance and Operations 應用程式。 此對應也會同步處理專案合約客戶的新增、更新和刪除。 專案合約之間的分割帳單百分比只能以 Dataverse 來主控，並不會同步處理至 Finance and Operations 應用程式。

在 Dataverse 中建立專案合約之後，專案會計師可以移至 **專案管理與會計** > **專案合約** > **設定** > **顯示預設會計**，在 Finance and Operations 應用程式中更新此專案合約的會計屬性。 會計師可在 Finance and Operations 應用程式中選取專案合約識別碼 (這樣會在 Dataverse 中開啟相關的專案合約記錄)，以審查營運專案合約屬性，例如要求的交貨日期和合約金額。

專案實體會使用 **專案 V2 (msdyn\_projects)** 資料表對應來同步處理至 Finance and Operations 應用程式。 專案會計師可以：

  - 移至 **專案管理與會計** > **所有專案**，以審查 Finance and Operations 應用程式中的專案。 
  - 移至 **專案管理與會計** > **所有專案** > **設定** > **顯示預設會計**，以更新 Finance and Operations 應用程式中專案的會計屬性。  
  - 在 Finance and Operations 應用程式中選取專案識別碼 (這樣會在 Dataverse 中開啟相關的專案記錄)，以審查營運專案屬性，例如估計開始和結束日期。

專案是透過 **專案合約服務內容** 實體與專案合約建立關聯。

Dataverse 中的專案合約服務內容會使用 **專案合約服務內容 (salesorderdetails)** 資料表對應，在 Finance and Operations 應用程式中建立專案合約帳單規則。 帳務方式會在 Finance and Operations 應用程式中定義專案合約帳單規則類型：

  - 使用時間和材料帳務方式的專案合約服務內容建立時間和材料類型的帳單規則。
  - 固定價格帳務方式合約服務內容會建立里程碑帳單規則。

專案會計師可以在 Finance and Operations 應用程式中審查專案合約服務內容，方法是移至 **專案管理與會計** > **專案合約** > **設定** > **顯示預設會計**，然後檢閱 **合約服務內容** 索引標籤上的詳細資料。會計師也可以在此索引標籤上設定固定價格帳務方式合約服務內容的預設財務維度。

## <a name="billing-milestones"></a>帳單里程碑

使用固定價格帳務方式的專案合約服務內容會透過帳單里程碑開立發票。 帳單里程碑會使用 **Project Operations 整合合約服務內容里程碑 (msdyn\_contractlinescheduleofvalues)** 資料表對應，同步處理至 Finance and Operations 應用程式中的專案記帳交易，

  ![帳單里程碑整合](./media/2Milestones.jpg)

會計師可以審查記帳交易記錄並調整這些交易記錄的會計屬性，方法是移至 **專案管理與會計** > **專案合約** > **維護** > **記帳交易**，或移至 **專案管理與會計** > **所有專案** > **維護** > **記帳交易**。

第一次建立指定專案合約服務內容的帳單里程碑時，系統會自動為與此合約服務內容相關聯的專案建立固定價格營收估計專案。 您可移至 **專案管理與會計** > **固定價格營收估計專案**，以檢閱固定價格營收估計專案。

### <a name="project-tasks"></a>專案工作

專案工作會透過 **專案工作 (msdyn\_projecttasks)** 資料表對應同步處理至 Finance and Operations 應用程式，僅供參考之用。 建立、更新和刪除作業無法透過 Finance and Operations 應用程式來支援。

  ![專案工作整合](./media/3Tasks.jpg)

## <a name="project-resources"></a>專案資源

**專案資源角色** 實體會使用 **所有公司的專案資源角色 (bookableresourcecategories)** 資料表對應同步處理至 Finance and Operations 應用程式，僅供參考之用。 由於 Dataverse 中的資源角色不是公司所特有，因此系統會自動在 Finance and Operations 應用程式中，針對所有已納入雙重寫入整合範圍的法律實體，建立各自的公司特定資源角色記錄。

![資源角色整合](./media/5Resources.jpg)

Project Operations 中的專案資源會保留在 Dataverse 中，並不會同步處理至 Finance and Operations 應用程式。

### <a name="transaction-categories"></a>交易類別

交易類別會保留在 Dataverse 中，並使用 **專案交易類別 (msdyn\_transactioncategories)** 資料表對應同步處理至 Finance and Operations 應用程式。 同步處理交易類別記錄之後，系統會自動建立四個共用類別記錄。 每個記錄都對應至 Finance and Operations 應用程式中的交易類型，並將它們連結至交易類別記錄。

![交易類別整合](./media/4TransactionCategories.jpg)

對估計值和實際值使用交易類別時，需要專案會計師或系統管理員在每個法律實體中建立對應的專案類別。 如需詳細資訊，請參閱[設定專案類別](../project-accounting/configure-project-categories.md)。
