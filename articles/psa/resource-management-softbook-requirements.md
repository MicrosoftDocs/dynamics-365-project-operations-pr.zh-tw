---
title: 未確認預約需求
description: 本主題提供有關如何以未確認預約方式預約需求的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 736d59976ad0f456a694cedbb28b516c90632fe6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282908"
---
# <a name="soft-book-requirements"></a>未確認預約需求

[!include [banner](../includes/psa-now-project-operations.md)]

資源需求可以進行已確認預約。 已確認預約會建立耗用資源產能的提案。 提案接著會傳送回到要求者以取得核准。 未確認預約會暫時將資源新增至專案團隊，並且在排程面板上的狀態有所不同，但不會耗用資源的產能。 若要以未確認預約方式從排程面板預約資源，請將 **預約狀態** 欄位設定為 **未確認**。

![預約狀態設定為 [未確認]](media/Resource-Management-image77.png)

當 **團隊** 索引標籤進入 **具名團隊成員** 檢視表時，資源就會顯示在其中。 **未確認預約時數** 欄會報告未確認預約時數。

![[具名團隊成員] 檢視表中的未確認預約時數](media/Resource-Management-image78.png)

無法將未確認預約的團隊成員指派給工作。

![指派給工作的未確認預約團隊成員](media/Resource-Management-image79.png)

在 **協調** 索引標籤上，不會顯示未確認預約資源的任何預約，因為 **協調** 索引標籤只會考慮已確認預約。

![未確認預約資源在 [協調] 索引標籤上沒有預約](media/Resource-Management-image80.png)

> [!NOTE]
> 您無法從一般團隊成員所產生的需求對資源進行未確認預約。

在排程面板上，資源的未確認預約會使用不同的色彩來標示。

![排程面板上的未確認預約](media/Resource-Management-image81.png)

若要將未確認預約轉換成已確認預約，請在排程板上以滑鼠右鍵按一下未確認預約，然後選取 **變更狀態** \> **已確認預約** \> **已確認**。

![將預約狀態變更為 [已確認]](media/Resource-Management-image82.png)

預約已變更，而且排程面板上的狀態也已變更。 預約狀態現在是 **已確認**，因此資源會顯示為已預約，而且其產能和可用性也會進行調整。

您可以使用相同的方法，從排程面板中取消已確認預約或未確認預約。

若要在專案的 **團隊** 索引標籤上將未確認預約資源轉換會已確認預約，請選取該資源，然後選取 **確認**。

![確認命令](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]