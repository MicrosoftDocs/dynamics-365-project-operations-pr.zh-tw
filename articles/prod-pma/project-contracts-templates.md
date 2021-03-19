---
title: 將專案合約和專案直接從 Project Service Automation 同步處理至 Finance
description: 本主題說明用於將專案合約和專案直接從 Microsoft Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 319000e6a826580049e8575def5790ab595a3165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289584"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>將專案合約和專案直接從 Project Service Automation 同步處理至 Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主題說明用於將專案合約和專案直接從 Dynamics 365 Project Service Automation 同步處理至 Dynamics 365 Finance 的範本與基礎工作。

> [!NOTE] 
> 如果您使用的是 Enterprise Edition 7.3.0，則必須安裝 KB 4074835。

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation 至 Finance 的資料流程

> [!NOTE]
> 使用 Project Service Automation to Finance 整合解決方案之前，您必須先熟悉 Dynamics 365 資料整合功能。

Project Service Automation 至 Finance 整合解決方案會使用資料整合功能，跨 Project Service Automation 與 Finance 的執行個體來同步處理資料。 可與資料整合功能搭配使用的整合範本會啟用有關從 Project Service Automation 到 Finance 的專案合約、專案、專案合約服務內容及專案合約服務內容里程碑的資料流程。

下圖這些顯示如何在 Project Service Automation 與 Finance 之間同步處理資料。

[![Project Service Automation 與 Finance 整合的資料流程](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>範本與工作

若要存取可用範本，請在 Microsoft Power Apps 系統管理中心選取 **專案**，然後選取右上角的 **新增專案** 以選取公用範本。

下列範本與基礎工作會用來將專案合約和專案從 Project Service Automation 同步處理至 Finance：

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>與 Dynamics 365 Project Service Automation v2.x 整合
- **資料整合中的範本名稱：** 專案和合約 (Project Service Automation 至 Finance)
- **專案中工作的名稱：**

    - 專案合約 Project Service Automation 至 Finance
    - 專案 Project Service Automation 至 Finance
    - 專案合約服務內容 Project Service Automation 至 Finance
    - 專案合約服務內容里程碑 Project Service Automation 至 Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>與 Dynamics 365 Project Service Automation v3.x 整合
Project Service Automation 中發生中繼資料變更，這會影響專案合約服務內容里程碑範本，並需要使用 v2 版本的範本，才能將 Project Service Automation v3.x 與 Dynamics 365 整合。

- **資料整合中的範本名稱：** 專案和合約 (Project Service Automation 3.x 至 Finance) - v2
- **專案中工作的名稱：**

    - 專案合約 Project Service Automation 至 Finance
    - 專案 Project Service Automation 至 Finance
    - 專案合約服務內容 Project Service Automation 至 Finance
    - 專案合約服務內容里程碑 Project Service Automation 至 Finance

您必須先同步處理帳戶，才能進行專案合約和專案同步處理。

## <a name="entity-set"></a>實體集

| Project Service Automation       | 財務                                                |
|----------------------------------|--------------------------------------------------------|
| 訂單                           | 專案合約的整合實體                |
| 專案                         | 專案的整合實體                         |
| 訂單明細                      | 專案合約服務內容的整合實體           |
| 專案合約服務內容里程碑 | 專案合約服務內容里程碑的整合實體 |

## <a name="entity-flow"></a>實體流程

專案合約是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案合約。 在整合範本中，您可以為專案合約設定 Finance 中的整合來源。

時間和材料專案以及固定價格專案是在 Project Service Automation 中進行管理，並當做物件同步處理至 Finance。 在範本整合過程中，您可以在 Finance 中設定專案的整合來源。 目前僅支援時間和材料專案以及固定價格專案。


專案合約服務內容是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案合約帳單規則。 如果帳務方式與預設專案類型不同，則同步處理會更新合約服務內容專案與專案群組的專案類型。

專案合約服務內容里程碑是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案合約帳單規則里程碑。

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation 至 Finance 整合解決方案

**專案合約識別碼** 欄位可在 **專案合約** 頁面上找到。 此欄位已設定為用來支援整合的自然對唯一索引鍵。

建立新的專案合約時，如果還沒有 **專案合約識別碼** 值，就會使用數字序列自動產生此值。 此值由後面跟著一個遞增數字序列的 **ORD** 以及再接著的六字元尾碼所組成。 以下是範例：**ORD-01022-Z4M9Q0**。

**專案編號** 欄位可在 **專案** 頁面上找到。 此欄位已設定為用來支援整合的自然對唯一索引鍵。

建立新的專案合約時，如果還沒有 **專案編號** 值，就會使用數字序列自動產生此值。 此值由後面跟著一個遞增數字序列的 **PRJ** 以及再接著的六字元尾碼所組成。 以下是範例：**PRJ-01049-CCNID0**。

套用 Project Service Automation 至 Finance 整合解決方案時，升級指令碼會在 Project Service Automation 中設定現有專案合約的 **專案合約識別碼** 以及現有專案的 **專案編號**。

## <a name="prerequisites-and-mapping-setup"></a>先決條件與對應設定

- 您必須先同步處理帳戶，才能進行專案合約和專案同步處理。
- 在您的連接集中，新增 **msdyn\_organizationalunits** 至 **msdyn\_name \[名稱\]** 的整合索引鍵欄位對應。 您可能需要先將專案新增至連接集。 如需詳細資訊，請參閱[將資料整合至應用程式適用的 Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)。
- 在您的連接集中，新增 **msdyn\_projects** 至 **msdynce\_projectnumber \[專案編號\]** 的整合索引鍵欄位對應。 您可能需要先將專案新增至連接集。 如需詳細資訊，請參閱[將資料整合至應用程式適用的 Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)。
- 專案合約和專案的 **SourceDataID** 可以更新為不同的值，或從對應中移除。 預設範本值是 **Project Service Automation**。
- **PaymentTerms** 對應必須更新，以便在 Finance 中反映有效的付款條件。 您也可以從專案工作移除對應。 預設值對應具有示範資料的預設值。 下表顯示 Project Service Automation 中的值。

    | 值 | 描述   |
    |-------|---------------|
    | 7     | 30 天內付款        |
    | 2     | 10 天內付款折扣 2%，30 天內付款 |
    | 3     | 45 天內付款        |
    | 4     | 60 天內付款        |

## <a name="power-query"></a>Power Query

如果符合下列條件，請使用 Microsoft Power Query for Excel 來篩選資料：

- 您在 Dynamics 365 Sales 中有銷售訂單。
- 您在 Project Service Automation 中有多個組織單位，而且這些組織單位將會對應至 Finance 中的多個法律實體。

如果您必須使用 Power Query，請遵循下列準則：

- 「專案與合約 (PSA 至 Fin 和 Ops)」範本有一個只會包含類型為 **工作項目 (msdyn\_ordertype = 192350001)** 之銷售訂單的預設篩選。 此篩選有助於保證不會為 Finance 中的銷售訂單建立專案合約。 如果您自行建立範本，就必須新增此篩選。
- 建立只包含合約組織的 Power Query 篩選，這些組織應同步處理至整合關係組的法律實體。 例如，您與合約組織單位 Contoso US 之間的專案合約，必須同步處理至 USSI 法律實體，但是您與合約組織單位 Contoso Global 之後專案合約則應同步處理至 USMF 法律實體。 如果您未將此篩選新增至工作對應，則會將所有專案合約都同步處理至針對連接集所定義的法律實體，而不考慮合約組織單位。

## <a name="template-mapping-in-data-integration"></a>資料整合中的範本對應

> [!NOTE] 
> **CustomerReference**、**AddressCity**、**AddressCountryRegionID**、**AddressDescription**、**AddressLine1**、**AddressLine2**、**AddressState** 和 **AddressZipCode** 欄位不會包含在專案合約的預設對應中。 如果專案合約需要同步處理此資料，您可以新增對應。
>
> **描述**、**ParentID**、**ProjectGroup**、**ProjectManagerPersonnelNumber** 和 **ProjectType** 欄位不會包含在專案的預設對應中。 如果專案需要同步處理此資料，您可以新增對應。

下圖顯示資料整合中的範本工作對應範例。 此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。

[![專案合約範本對應](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![專案範本對應](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![專案合約服務內容範本對應](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![專案合約服務內容里程碑範本對應](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>「專案與合約 (PSA 3.x 至 Dynamics) - v2」範本中的專案合約服務內容里程碑：

[![專案合約服務內容里程碑與版本 2 範本的對應](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]