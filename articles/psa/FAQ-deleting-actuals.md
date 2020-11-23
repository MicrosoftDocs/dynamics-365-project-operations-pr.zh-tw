---
title: 為什麼我無法從實際值實體刪除記錄？
description: 本主題提供有關為何您無法從實際值實體刪除記錄的資訊。
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127148"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="41fe4-103">為什麼我無法從實際值實體刪除記錄？</span><span class="sxs-lookup"><span data-stu-id="41fe4-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="41fe4-104">Project Service Automation (PSA) 不允許您刪除實際值，因為這些值可以做為對下游系統 (例如總帳) 有財務影響的交易事實原始資料。</span><span class="sxs-lookup"><span data-stu-id="41fe4-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="41fe4-105">如果可以刪除實際值，可能就會引發對財務報表交易完整性的質疑。</span><span class="sxs-lookup"><span data-stu-id="41fe4-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="41fe4-106">若要建立稽核線索，客戶必須使用帳目來建立補償交易。</span><span class="sxs-lookup"><span data-stu-id="41fe4-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

