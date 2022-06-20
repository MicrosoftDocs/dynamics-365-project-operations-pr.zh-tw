---
title: 將 Project Service Automation 中的專案工作直接同步處理至 Finance and Operations
description: 本文說明用來將 Microsoft Dynamics 365 Project Service Automation 中的專案工作直接同步處理至 Dynamics 365 Finance 的範本及基礎工作。
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7b8ba77bbb08052952a8a557bb71300652dca3b2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931136"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>將 Project Service Automation 中的專案工作直接同步處理至 Finance and Operations

[!include[banner](../includes/banner.md)]

本文說明用來將 Dynamics 365 Project Service Automation 中的專案工作直接同步處理至 Dynamics 365 Finance 的範本及基礎工作。

> [!NOTE]
> - 專案工作整合、費用交易類別、工時估計、費用估計和功能鎖定可在 8.0 版中使用。
> - 如果您使用的是 Enterprise Edition 7.3.0，則安裝 KB 4132657 和 KB 4132660 之後，您就可以使用範本來整合專案工作、費用交易類別、工時估計、費用估計與實際值，以及設定功能鎖定。 如果必須重設會計分配，建議您還要再安裝 KB 4131710。
> - 實際值整合可在 8.0.1 版或更新版本中使用。

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation 至 Finance 的資料流程

Project Service Automation 至 Finance 整合解決方案會使用資料整合功能，跨 Project Service Automation 與 Finance 的執行個體來同步處理資料。 可與資料整合功能搭配使用的整合範本會啟用有關專案工作從 Project Service Automation 到 Finance 的資料流程。

下圖這些顯示如何在 Project Service Automation 與 Finance 之間同步處理資料。

[![Project Service Automation 與 Finance 整合的資料流程。](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>範本與工作

若要存取範本，請在 Microsoft Power Apps 系統管理中心選取 **專案**，然後選取右上角的 **新增專案** 以選取公用範本。

下列範本與基礎工作會用來將專案工作從 Project Service Automation 同步處理至 Finance。

- **資料整合中範本的名稱：** 專案工作 (PSA 至 Fin 和 Ops)
- **專案中工作的名稱：** 專案工作

您必須先同步處理專案合約和專案，才能進行專案工作同步處理。

## <a name="entity-set"></a>實體集

| Project Service Automation | Finance                             |
|----------------------------|-------------------------------------|
| 專案工作              | 專案工作的整合實體 |

## <a name="entity-flow"></a>實體流程

專案工作是在 Project Service Automation 中進行管理，並同步處理至 Finance 做為專案活動。

## <a name="prerequisites-and-mapping-setup"></a>先決條件與對應設定

您必須先同步處理專案合約和專案，才能進行專案工作同步處理。

## <a name="power-query"></a>Power Query

如果符合此條件，則必須使用 Microsoft Power Query for Excel 來篩選資料：

- 您在專案工作中具有資源特定記錄。

如果您必須使用 Power Query，請遵循此準則：

- 「專案工作 (PSA 至 Fin 和 Ops)」範本具有預設篩選，此篩選將 **IsLineTask** 的篩選設定為 **False**，從專案工作中排除資源特定記錄 。 如果您自行建立範本，就必須新增此篩選。

## <a name="template-mapping-in-data-integration"></a>資料整合中的範本對應

下圖顯示資料整合中的範本工作對應範例。 此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。

[![範本對應。](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]