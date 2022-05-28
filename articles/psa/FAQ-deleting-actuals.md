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
ms.reviewer: johnmichalak
ms.openlocfilehash: ff2c951905324d5d05722f399057c03d22f1a1c9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584402"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>為什麼我無法從實際值實體刪除記錄？

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) 不允許您刪除實際值，因為這些值可以做為對下游系統 (例如總帳) 有財務影響的交易事實原始資料。 如果可以刪除實際值，可能就會引發對財務報表交易完整性的質疑。 若要建立稽核線索，客戶必須使用帳目來建立補償交易。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
