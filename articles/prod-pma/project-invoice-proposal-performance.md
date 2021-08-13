---
title: 專案發票提案效能
description: 本主題提供有關專案發票提案效能改善的資訊。
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b6df8baf1013720778308ce536b037dec4775f040d2925a47508fb373900f81
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005696"
---
# <a name="project-invoice-proposal-performance"></a>專案發票提案效能

[!include [banner](../includes/banner.md)]

建立新的發票提案時，您可能會在專案和子專案數目增加時遇到效能問題。 為了改善效能，可以使用縮短為已過帳專案交易建立新發票提案所需時間的功能。

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>啟用專案發票提案效能增強功能
若要啟用專案發票提案效能增強功能，請完成下列步驟。

1.  移至 **功能管理** > **全部**。 在功能清單中，尋找 **專案發票提案效能增強功能**。
2.  選取 **立即啟用**。
3.  重新整理瀏覽器，然後建立新的發票提案。

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>關閉專案發票提案效能增強功能
完成下列步驟以關閉專案發票提案效能增強功能。

1.  移至 **功能管理** > **全部**。 在功能清單中，尋找 **專案發票提案效能增強功能**。
2.  選取 **停用**。
3.  重新整理您的瀏覽器。

> [!NOTE]
> 啟用帳單規則時，無法套用發票提案績效。
> 
> 進行建立發票提案的批次程序時，不論您輸入了什麼數量，子工作數量都會根據可開票交易記錄的合約數目，將工作分割成最大數量。 例如，如果您輸入 **3** 表示批次建立發票提案時的子工作數量，且只有兩個合約有可開票交易，則只會建立兩個子工作。
