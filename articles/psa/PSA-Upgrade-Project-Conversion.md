---
title: 從 Project Service Automation 到 Project Operations 的功能變更
description: 本文提供從 Microsoft Dynamics 365 Project Service Automation 到 Dynamics 365 Project Operations 的功能變更概觀。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621205"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>從 Project Service Automation 到 Project Operations 的功能變更

當專案成功從 Microsoft Dynamics 365 Project Service Automation 3.X 升級到 Dynamics 365 Project Operations Lite 後，就無法在工作網格分工結構圖 (WBS) 中編輯專案工作。 客戶將可以在追蹤網格中檢視 WBSs，其中新的欄位已新增，以提供和該工作相關的所有詳細資料。 對於需要進行 WBS 編輯的專案，您可以選擇性將符合條件的專案轉換為新的 Project for the web 排程體驗。

## <a name="project-conversion-process"></a>專案轉換過程

若要轉換專案，請依照這些步驟。

1. 打開專案的主頁面，並在動作窗格上選取 **轉換**。
1. 在確認訊息方塊中，選取 **確定** 以開始專案轉換。 會出現下列動作：

    1. 出現在專案主頁面狀態上的訊息列，是「專案排程正在轉換中。 在轉換完成之前，您無法變更專案。」
    1. 您會被重新導至專案清單。

    專案轉換完成後，會出現下列動作：

    1. 指派的專案經理會在應用程式的右側收到通知。
    1. 指出轉換正在進行的訊息列已移除。
    1. **排程** 索引標籤會顯示帶有 Project for the web 的新排程體驗。 任何具有適當授權和資訊安全角色的使用者，都可以編輯 WBS。
    1. **排程引擎** 欄位已更新為 **Project for the web**。
    1. **轉換** 按鈕會從動作窗格中移除。

> [!IMPORTANT]
> 不允許大量專案轉換。 任何想要同時更新大量專案的嘗試都會受到限制。 這項限制有助於確保所有客戶都能享有高效能。

## <a name="manual-tasks-vs-automatic-tasks"></a>手動工作與自動工作

當環境從 Project Service Automation 升級至 Project Operations 時，WBS 中的所有工作都會被視為自動排程。 Project for the web 中無法使用手動排程工作的概念。 不過，在您建立新專案時，可以使用[排程模式](/project-management/scheduling-modes.md)設定來定義專案的偏好排程行為。

## <a name="restricted-operations-for-pre-conversion-projects"></a>轉換前專案的受限作業

本節概述當專案未進行轉換時，您可以預見的功能差異。

### <a name="copy-project"></a>複製專案

只有轉換的專案才支援 **複製** 作業。 轉換之前，無法複製已升級的專案。

### <a name="move-project"></a>移動專案

變更專案的開始日期，不會按比例移動工作的開始日期 (除非專案已轉換)。

## <a name="frequently-asked-questions"></a>常見問題

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>已轉換的專案與升級完成後才建立的新專案有何不同？

對於環境升級後轉換的專案，將會設定標誌，指示排程只遵守專案行事曆。 此行為符合 Project Service Automation 中的行為。 但是，在升級後建立的新專案將不會設定該標誌。 因此，當資源指派給工作時，排程將會遵守資源的工作時數。

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>如果我的專案轉換失敗，我該怎麼辦？

如果您的專案轉換失敗，第一步是檢視錯誤紀錄，以找出與您的 WBS 相關的任何常見問題。 如果紀錄未指出您可以執行動作的特定錯誤，請與客戶支援部門聯繫，讓您的案例獲得進一步檢視。

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>在 Project for the web 中如何處理公休日？

Project for the web 並不遵守企業在組織層級定義的公休日。 但是，它會遵守在給定工作時數範本中定義的其他休假類型。

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Project for the web 的限制是什麼？

請參閱[建立分工結構圖：專案的限制](/project-management/create-wbs#project-limitations.md)。

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>我是否可以預期成本和銷售估計的變更？

在資源指派結構重新計算，或資源指派結構落在不同日期邊界，而非來源專案等罕見情況下，您可能會看到銷售和成本估計有所不同。 在升級過程中，客戶可望測試代表性的專案範例集，讓他們可以瞭解任何可能的排程變更。
