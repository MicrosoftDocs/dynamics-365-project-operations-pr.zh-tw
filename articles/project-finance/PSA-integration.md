---
title: Project Service Automation 概觀
description: 本主題提供關於 Dynamics 365 Project Service Automation 至 Dynamics 365 Finance 整合解決方案的資訊。
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749937"
---
# <a name="project-service-automation-overview"></a>Project Service Automation 概觀

[!include[banner](../includes/banner.md)]

Project Service Automation 至 Finance 整合解決方案會使用資料整合功能，透過 Common Data Service 跨 Dynamics 365 Finance 與 Dynamics 365 Project Service Automation 的執行個體來同步處理資料。 可與資料整合功能搭配使用的整合範本會啟用從 Project Service Automation 到 Finance 的專案、專案合約、專案合約服務內容、專案合約服務內容里程碑、專案工作、費用交易類別、工時估計及費用估計流程。

> [!NOTE]
> - 如果您使用的是 7.3.0 版，則必須安裝 KB 4074835。 您可以接著整合固定價格專案。
> - 如果您使用 7.3.0 版，而且要將費用交易從 Project Service Automation 那裡帶過來，則必須安裝 KB 4345320，才能將這些費用包含在專案發票中。
> - 如果使用 8.0 版，您將可以使用專案工作整合、費用交易類別、工時估計、費用估計和功能鎖定。
> - 如果使用的是 8.0.1 版或更新版本，就可以同步處理實際值。

整合 Project Service Automation 與 Finance 之前，您必須先設定 Project Service Automation 整合參數。 如需詳細資訊，請參閱 [Project Service Automation 整合參數](PSA-parameters.md)。

此整合解決方案可在下列案例中啟用直接同步處理：

- 在 Project Service Automation 中維護專案合約，並將其直接從 Project Service Automation 同步處理至 Finance。
- 在 Project Service Automation 中建立專案，並將其直接從 Project Service Automation 同步處理至 Finance。
- 在 Project Service Automation 中維護合約服務內容，並將其直接從 Project Service Automation 同步處理至 Finance。
- 在 Project Service Automation 中維護合約服務內容里程碑，並將其直接從 Project Service Automation 同步處理至 Finance。
- 在 Project Service Automation 中維護專案工作，並將其直接從 Project Service Automation 同步處理至 Finance。
- 在 Finance 中維護費用交易類別，並將其直接從 Finance 同步處理至 Project Service Automation。
- 在 Project Service Automation 中建立專案工時估計，並將其直接從 Project Service Automation 同步處理至 Finance。
- 在 Project Service Automation 中建立專案費用估計，並將其直接從 Project Service Automation 同步處理至 Finance。
- 在 Project Service Automation 中建立專案時間、費用及服務費實際值，並在 Project Service Automation 整合日記帳中建立專案交易，讓這些可以在 Finance 中過帳。

## <a name="data-synchronization"></a>資料同步

下圖這些顯示如何將資料同步處理為 Project Service Automation 與 Finance 之間整合的一部分。

> [!NOTE]
> 目前並非所有的範本都有提供。 範本完成時，就會發行。

[![Project Service Automation 與 Finance 整合](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Finance 系統需求

若要使用 Project Service Automation 至 Finance 整合解決方案，您必須安裝 Enterprise Edition 7.3 (含平台更新 12) 或更新版本。

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation 系統需求

若要使 Project Service Automation 至 Finance 整合解決方案，您必須安裝下列元件：

- Dynamics 365 Project Service Automation 版本 9.0.0.0 或更新的版本
- Dynamics 365 Sales 1.14.0.0 版 (v14) 或更新版本的潛在客戶轉現金解決方案
- Dynamics 365 Project Service Automation 1.0.0.0 版或更新版本的 Project Service Automation 至 Finance 解決方案

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>在 Project Service Automation 執行個體中安裝 Project Service Automation 至 Finance 整合解決方案

從 [Microsoft 下載中心](https://www.microsoft.com/download/details.aspx?id=57016)下載 Project Service Automation 至 Finance 整合解決方案，並依照解決方案隨附的指示進行。
