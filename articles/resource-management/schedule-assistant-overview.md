---
title: 排程小幫手概觀
description: 本主題提供有關使用排程小幫手來預約資源的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279218"
---
# <a name="schedule-assistant-overview"></a>排程小幫手概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

排程小幫手會根據專案經理定義的需求來預約資源。 排程小幫手依賴資源需求中提供的參數來尋找資源。 排程小幫手會建議符合相關需求 (例如時間範圍或所需技能) 的資源。

找出適當的資源後，資源管理員或專案經理就可以將資源預約給工作。

## <a name="prerequisites"></a>先決條件

排程小幫手是 Universal Resource Scheduling 解決方案的一部分。 此解決方案隨附於 Dynamics 365 Project Operations、Dynamics 365 Field Service 和 Dynamics 365 Customer Service，並隨這些應用程式一起安裝。

## <a name="matching-requirements-and-resources"></a>比對需求與資源

產生的資源需求是根據一些詳細資料，例如：

-   特性
-   角色
-   業務單位
-   資源喜好設定
-   投入量分佈
-   時區

排程小幫手使用這些詳細資料來篩選資源。

## <a name="launch-the-schedule-assistant"></a>啟動排程小幫手

有兩種方式可以用來啟動排程小幫手。 如果您使用的是混合模式，則可以在團隊成員網格中選取任何有未履行資源需求的團隊成員，然後選取 **預約**。 如果您使用的是集中模式，則資源管理員會尋找並選取資源。

## <a name="schedule-assistant-filters"></a>排程小幫手篩選

排程小幫手執行之後，資源需求的詳細資料會在左窗格中顯示為篩選後的值。 資源管理員或專案經理可將篩選調整成符合排程需求以微調結果。

篩選窗格會顯示工作相關選項，包括：

-   工作開始和結束
-   特性
-   角色
-   組織單位
-   資源供應公司
-   資源類型
-   偏好的資源


[!INCLUDE[footer-include](../includes/footer-banner.md)]