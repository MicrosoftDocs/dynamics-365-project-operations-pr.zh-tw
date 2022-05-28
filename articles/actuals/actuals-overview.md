---
title: 實際值
description: 本主題提供有關如何在 Microsoft Dynamics 365 Project Operations 中處理實際值的資訊。
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581274"
---
# <a name="actuals"></a>實際值

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

實際值表示專案上已審查且核准的財務及排程進度。 這些值是在核准時間、費用和材料使用項目、帳目分錄和發票時所建立。

> [!IMPORTANT]
> 不可在系統中編輯或刪除實際值。 否則，財務健全狀況以及任何與其他財務及會計系統的整合都可能會受到負面影響。 Microsoft Dynamics 365 Project Operations 可讓您在專案商務程序生命週期中的不同時點，使用沖回和取代實際值的方式來編輯實際值。

## <a name="recording-actuals-based-on-project-events"></a>根據專案事件記錄實際值

Project Operations 會將專案業務開發生命週期中發生的財務交易記錄為實體值。 在生命週期的各種事件中建立實際值的作業各不相同，取決於專案業務開發使用的是時間和材料計費模型還是固定價格計費模型，以及此作業是在售前階段還是其本身為內部專案。

下列主題說明不同變化在各種事件中對實際值資料表的影響：

- [時間和材料業務開發中的實際值影響](ActualsonTM.md)
- [在固定價格業務開發中的影響](ActualonFP.md)
- [售前階段和業務開發中的實際值影響](ActualonPreSales.md)
- [內部專案的實際值影響](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
