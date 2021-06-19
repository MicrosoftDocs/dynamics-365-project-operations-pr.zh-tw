---
title: 資源管理常見問題集
description: 本主題提供關於資源管理的常見問題解答。
author: ruhercul
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
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008751"
---
# <a name="resource-management-faq"></a>資源管理常見問題集

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>團隊成員與資源需求之間有何區別？

專案團隊成員可以指派給工作、預約或過量預約，以及設定為核准者。 資源需求沒有專案團隊成員也能存在，就像索求的草稿附註一樣。 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>提案時數與未確認預約時數之間有何區別？

提案時數與未確認預約時數在顯示性上不同。 提案的時數僅顯示給資源管理員以及使用資源要求提出索求的專案經理。 未確認預約時數可顯示給任何有權存取排程面板的使用者。

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>如何在團隊中看到資源的未確認預約時數？

在您預約資源需求時，可以進行未確認預約。 在專案團隊上未確認預約的資源，會顯示為具有未確認預約時數的團隊成員。 這些成員也會在排程面板上出現。

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>如何變更我已預約之資源 (一般或具名) 的需要時數以及開始和結束日期？

預約資源之後，選取 **維護預約** 即可進行任何必要的變更。

## <a name="what-resources-types-does-project-service-automation-support"></a>Project Service Automation 支援哪些資源類型？

**使用者** 和 **連絡人** 是唯一在 Dynamics 365 Project Service Automation 中支援的資源類型。 雖然您可以建立其他類型的資源 (例如, **設備** 和 **群組**)，但是不支援這些資源的端對端使用案例。

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>指派與預約之間有何區別？

指派是在專案排程中對專案工作的資源指派。 資源可以是實際或一般資源。 預約是為專案進行的已確認或未確認資源配置。 已確認預約會耗用資源的產能。 對於實際資源，預約與指派最好要一致，因為兩者並無差別。 但是，PSA 不會強制這樣的一致性。 協調檢視表會向專案經理顯示資源預約與指派不一致的地方。


[!INCLUDE[footer-include](../includes/footer-banner.md)]