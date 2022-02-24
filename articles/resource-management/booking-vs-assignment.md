---
title: 預約與指派的比較
description: 本主題提供有關資源預約與資源指派之間差異的資訊。
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841162"
---
# <a name="bookings-vs-assignments"></a>預約與指派的比較

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

預約是為專案進行的已確認或未確認資源配置。 已確認預約會耗用資源的產能。 預約代表團隊的組織概念，以便其了解資源如何參與各種專案。 Dynamics 365 Project Operations 將預約視為專案層級概念。 

與預約不同的是，指派是資源對專案排程中工作的承諾用量。 資源可以具名或一般資源。  當資源需求是衍生自專案工作指派時，Project Operations 會使用資源指派的努力分佈，來建置資源需求詳細資料的分佈。 但是，不會保留資源指派參考。 對衍生自資源需求的預約進行更新不會更新任何資源指派。

資源預約的加總通常等於資源在一個或多個工作中的指派總和。 不過，Project Operations 不會強制這樣的一致性。 **協調** 檢視表會向專案經理顯示資源預約與指派不一致的地方。


