---
title: 檢閱提案的資源
description: 本主題提供有關如何提案建議專案資源的資訊。
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401163"
---
# <a name="review-proposed-resources"></a>檢閱提案的資源

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

資源管理員可以使用資源要求，提案向專案經理建議資源。

1. 從要求網格或要求本身中選取 **尋找資源**。
2. 在 **排程小幫手** 頁面上，選取資源，然後在 **建立資源預約** 窗格的 **預約狀態** 欄位中選取 **預約**。

發生下列狀態更新：

- 在 **排程小幫手** 頁面上，狀態指示器會更新，以指定該預約是提案所建議，而不是已確認預約。
- 在資源要求上，狀態已變更為 **需要檢閱**。
- 在專案的 **團隊** 索引標籤上，一般團隊成員的 **要求狀態** 值會變更為 **需要檢閱**。

專案經理可以接受或拒絕提案。

資源經理處理資源要求時，可以使用下列任一方法：

- 如果沒有單一資源可用來履行需要的時數，請提案建議多個資源以滿足需求。 提案的時數隨後會在多個可滿足所需時數的資源間進行分割。 在此案例中，時數不能重疊。
- 提案建議比所需資源還要少的資源。 在此案例中，提案的資源產能小於要求者所指定的需要時數。 因此，當要求者接受提案的資源時，就會建立未履行資源需求，以擷取剩餘的索求。
- 如果沒有單一資源可用來完成工作，請預約建議多個資源以滿足索求。
- 預約比所需資源還要少的資源。 在此案例中，預約的工時少於需要的時數。 系統會引導您提案建議的是資源而不是預約，這樣要求者才能驗證並追蹤剩餘的索求。

## <a name="resource-availability"></a>資源可用性

資源管理員要能夠檢視資源可用性並更新預約，至關重要。 在某些情況下，沒有正式索求 (資源要求)，但是資源管理員必須回應來自電子郵件、通話或立即訊息等管道的計劃外索求。 資源管理員會使用排程面板來更新資源和預約。

資源工作時數會用來做為計算資源可用性的基準。 資源預約會耗用資源的產能。

排程面板使用色彩與陰影來顯示預約、可用性和過量預約，以及預約的狀態。 排程面板中的設定可讓您顯示圖例。

如果排程面板上的個別可預約資源旁邊出現向右箭頭，則可以展開資源來顯示該資源所預約之工作的詳細資料。

因為 Dynamics 365 Project Operations 使用 Universal Resource Scheduling 引擎，如果您也已安裝 Dynamics 365 Field Service，則可以檢視專案、工單以及任何其他您已將排程功能擴展至之實體的資源預約詳細資料。

若要檢視更多關於個別資源的詳細資料，請在其上按滑鼠右鍵以開啟資源卡片。

