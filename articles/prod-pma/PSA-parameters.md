---
title: Project Service Automation 整合參數
description: 本主題說明設定如何在整合 Microsoft Dynamics 365 for Project Service Automation 與 Microsoft Dynamics 365 Finance 時輸入預設資料的方法。
author: ruhercul
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 1a0cee090e0ecb306aa3bda62c79a57dfade93c0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073136"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation 整合參數

[!include[banner](../includes/banner.md)]

在 **Project Service Automation 整合參數** 頁面上，您可以設定如何在整合 Dynamics 365 Project Service Automation 與 Dynamics 365 Finance 時輸入預設資料。 若要讓專案成功地從 Project Service Automation 同步處理至 Finance，您必須設定下列欄位。

若要開啟 **Project Service Automation 整合參數** 頁面，請移至 **專案管理與會計** \> **設定** \> **Dynamics 365 for Project Service Automation 整合參數** 。 

> [!NOTE]
> - 專案工作整合、費用交易類別、工時估計、費用估計和功能鎖定可在 8.0 版中使用。
> - 實際值整合可在 8.0.1 版或更新版本中使用。


| 索引標籤                    | 欄位                | 描述 |
|------------------------|----------------------|-------------|
| 一般                | 預設專案類型 | 選取預設專案類型。 從 Project Service Automation 同步處理專案時，如果您未在整合範本中提供預設值，則會使用此值。 進行同步處理時，新專案的 **專案類型** 欄位會設定為此值。 不過，從 Project Service Automation 同步處理專案合約服務內容時，此值可能會更新。 |
|                        | 時間類別        | 選取預設時間類別。 從 Project Service Automation 同步處理工時估計時，會使用此值。 從 Project Service Automation 同步處理工時估計與工時實際值時，Finance 中新專案工時預測的 **類別** 欄位會設定為此值。 |
|                        | 服務費類別         | 選取預設服務費類別。 從 Project Service Automation 同步處理服務費實際值時，會使用此值。 從 Project Service Automation 同步處理服務費實際值時，Finance 中新服務費交易的 **類別** 欄位會設定為此值。 |
| 專案群組預設值 | 專案類型         | 按一下 **新增** 以新增一列，您可在此列中選取需要設定預設專案群組的專案類型。 特定專案類型在設定中只能選取一次。 |
|                        | 專案群組        | 選取所選專案類型的預設專案群組。 從 Project Service Automation 同步處理新專案時，如果未在整合範本中提供預設值，則 **專案群組** 欄位會設為專案類型的預設值。 |
| 帳單類型預設值  | 帳單類型         | 按一下 **新增** 以新增一列，您可在此列中選取需要設定預設明細屬性的帳單類型。 特定帳單類型在設定中只能選取一次。 |
|                        | 明細屬性        | 選取所選帳單類型的預設明細屬性。 從 Project Service Automation 同步處理新工時估計、新費用估計或新實際值時， **明細屬性** 欄位會設定為帳單類型的預設值。 |
| 功能鎖定  | 不適用       | 選取要在 Finance 中針對源自 Project Service Automation 之專案與合約停用的功能。 例如，您可以關閉用於編輯合約與專案、建立分工結構圖以及在 Finance 中輸入時程表的功能。 即使參數設定已將會計相關欄位設定為無法使用，仍然會繼續啟用這些欄位。 預設會啟用所有功能。 |
