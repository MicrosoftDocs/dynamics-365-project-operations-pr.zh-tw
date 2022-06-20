---
title: 專案資源排程效能
description: 本文提供有關如何改善大量專案資源排程效能的資訊。
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 072476d43fb3b3d4f96480ec2d3dc5f9db28e501
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921890"
---
# <a name="project-resource-scheduling-performance"></a>專案資源排程效能

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


專案數目達到數千個時，就會發生與資源排程相關的效能問題。 為了改善資源排程效能，有一項功能可讓使用者縮短啟動資源可用性表單所需的時間。 具體而言，這會移除資源產能彙總同步處理程序，而使用 **ResProjectResource** 資料表來加速資源查詢。 請注意，不再使用 **ResRollup** 資料表。

> [!IMPORTANT]
> 如果資源產能彙總同步處理程序或 **ResProjectResource** 資料表有相依性，請不要使用此功能。

## <a name="enable-resource-scheduling-performance-enhancement"></a>啟用資源排程效能增強功能
若要啟用資源排程效能增強功能，請完成下列步驟。

1. 移至 **功能管理** > **全部**，並在功能清單中找出 **啟用專案資源排程效能增強功能**。
2. 選取 **立即啟用**。

> [!NOTE]
> 如果清單中找不到此功能，請選取 **檢查更新** 以重新整理清單。

3. 重新整理瀏覽器，然後移至 **專案管理與會計** > **定期** > **專案資源** > **同步處理所有公司的資源行事曆產能**。
4. 將 **移除現有的產能記錄** 設定為 **是**，以移除先前的資料。 如果您想要產生增量資料，請將其設定為 **否**。
5. 在 **期間代碼** 欄位中，選取要產生資料的期間。 如果您選取期間代碼，則不需定義開始和結束日期。
6. 如果讓 **期間代碼** 欄位保持空白，請選取要產生資料的特定開始及結束日期。
7. 選取 **確定**。

 > [!NOTE]
 > 這會將一般資料發佈至您環境中所有公司之間的 **ResCalendarCapacity** 資料表，因此批次處理工作只需在一個法律實體中執行。 需要使用此批次作業中的資料，才能透過相關行事曆計算資源產能。

8. 移至 **專案管理與會計** > **定期** > **專案資源** > **填入所有公司之間的專案資源**，然後選取 **確定**。 這是適用於 **ResProjectResource**、**ResCalendarDateTimeRange** 和 **ResEffectiveDateTimeRange** 資料表中一般資料的資料升級指令碼。 **PSAPRojSchedRole.RootActivity** 欄位的值也會更新。 如果未執行此作業，您就會在嘗試執行資源排程作業時收到警告。
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>關閉資源排程效能增強功能

1. 移至 **功能管理** > **全部**，並搜尋 **啟用專案資源排程效能增強功能**。
2. 選取功能，然後選取 **停用** 按鈕。
3. 重新整理您的瀏覽器。
4. 移至 **專案管理與會計** > **定期** > **產能同步處理** > **同步處理資源產能彙總**。
5. 在 **產能彙總同步處理** 頁面上，將 **移除現有的產能記錄** 設定為 **是**，以移除先前的資料。 如果您想要產生增量資料，請將其設定為 **否**。
6. 在 **期間代碼** 欄位中，選取要產生資料的期間。 如果您選取期間代碼，則不需定義開始和結束日期。
7. 如果讓 **期間代碼** 欄位保持空白，請選取要產生資料的特定開始及結束日期。
8. 選取 **確定**。

> [!NOTE]
> 這會將一般資料發佈至您環境中所有公司之間的 **ResRollup** 資料表，因此批次處理工作只需在一個法律實體中執行。 所有 **資源可用性** 檢視表都需要這個批次工作。 如果此批次作業未執行，則會即時產生 **ResRollup** 資料，而這可能需要一些時間。


[!INCLUDE[footer-include](../includes/footer-banner.md)]