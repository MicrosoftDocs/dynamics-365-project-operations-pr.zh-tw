---
title: 為什麼我無法從實際值實體刪除記錄？
description: 本主題提供有關為何您無法從實際值實體刪除記錄的資訊。
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002861"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>為什麼我無法從實際值實體刪除記錄？

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) 不允許您刪除實際值，因為這些值可以做為對下游系統 (例如總帳) 有財務影響的交易事實原始資料。 如果可以刪除實際值，可能就會引發對財務報表交易完整性的質疑。 若要建立稽核線索，客戶必須使用帳目來建立補償交易。



[!INCLUDE[footer-include](../includes/footer-banner.md)]