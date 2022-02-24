---
title: 時間與材料專案的專案銷售訂單
description: 本主題說明如何為時間與材料專案建立專案型銷售訂單。
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
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
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072981"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>時間與材料專案的專案銷售訂單

[!include[banner](../includes/banner.md)]

本主題說明如何建立專案的銷售訂單。 您只能為 **時間與材料** 類型的專案建立銷售訂單。

如果時間與材料專案在專案合約上有多個資金來源，您必須在 **專案管理與會計參數** 頁面上啟用 **允許具有多個資金來源的專案銷售訂單**。 

> [!NOTE]
> - 對具有多個資金來源的專案銷售訂單的支援，是從應用程式版本 10.0.2 和更新版本開始提供。
> - 用來啟用支援具有多個資金來源的專案銷售訂單的參數會在 2020 年 4 月發行浪潮中移除，此後一律啟用這項功能。

您可以用兩種方式建立專案型銷售訂單：

- 移至專案本身。 在動作窗格中，選取 **管理 > 專案工作 > 銷售訂單**。 專案資訊會預設為專案中的銷售訂單。 如果專案合約有多個資金來源，您必須選取資金來源，才能設定銷售訂單的客戶。 如果專案只有一個資金來源，就會自動設定客戶。
- 移至 **所有銷售訂單** 清單頁面，並建立新的銷售訂單。 您需要選取銷售訂單的專案。 選取專案之後，將會從資金來源設定客戶，如果專案合約有多個資金來源，則需要選取資金來源。

