---
title: 重要概念
description: 本主題提供有關 Project Service Automation 中資源管理重要概念的資訊。
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
ms.openlocfilehash: 75b2d2c520cc48eb59c266289ca2bdc1288f2920
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147733"
---
# <a name="key-concepts"></a>重要概念

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

下表定義 Dynamics 365 Project Service Automation 應用程式中使用的重要概念。

| 概念                    | 定義 |
|----------------------------|------------|
| 專案團隊成員        | 身為專案團隊的一分子，專案團隊成員可以是有預約的具名資源、沒有預約的具名資源，或是一般資源。 一般資源沒有預約、適用範圍局限於專案，並且在整個專案中沒有產能限制。 |
| 專案一般資源   | 資源預留位置，可讓您形成團隊並配置專案計劃的人員，而不需知道具名資源。 專案行事曆會用作一般資源的行事曆。 您可以將一般資源新增至專案團隊並指派給工作。 |
| 已預約時數               | 資源時數是以確定方式針對專案所預約，有助於保證完成專案工作。 已預約的時數會耗用資源的整體資源。 預約只對具名資源進行，而不針對一般資源。 |
| 已指派的時數             | 資源時數是在專案排程中指派給工作。 指派可以對具名資源或一般資源進行。 指派與預約無關，互不影響。 |
| 需要的時數             | 需要但尚未由具名資源履行的產能。 需要的時數只與已產生資源需求的一般團隊成員相關。 |
| 索求                     | 目前和近期工作負載。 在 Project Service Automation 中，索求會顯示為資源需求或資源要求。 |
| 資源需求       | 用來為所需資源擷取需要時數、開始和結束日期、技能、地理位置及其他定價維度的實體。 資源需求是由專案團隊成員所產生，或是個別建立的。 |
| 資源要求           | 用來當做「信封」傳遞必須由資源管理員履行之資源需求的實體。 |
| 資源預設角色      | 資源據以分為群組供計算使用率的角色。 已假定資源具有角色所需的技能，且符合該角色的目標使用率。 |
| 資源組織單位 | 將資源指派至的組織單位。 |
| 分佈                    | 工作、需求或指派時數在細分成每日分佈時的說法。 例如，一項為期五天的 40 小時工作，可在五天期間內分佈為每天 8 小時的工作。 |
| 協調檢視表        | 顯示每個專案團隊成員預約與指派的檢視表。 此檢視表可讓專案經理尋找預約與指派之間是否有任何不相符，如果出現任何不相符，即採取更正動作。 |
| 工作時數                 | 用來識別資源產能以及工作時間和非工作時間的實體。 此實體也稱為資源行事曆。 |
