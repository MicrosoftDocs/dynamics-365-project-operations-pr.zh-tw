---
title: 實際值
description: 本文提供有關如何在 Microsoft Dynamics 365 Project Operations 中使用實際值的資訊。
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924788"
---
# <a name="actuals"></a>實際值

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

實際值表示專案上已審查且核准的財務及排程進度。 這些值是在核准時間、費用和材料使用項目、帳目分錄和發票時所建立。

> [!IMPORTANT]
> 不可在系統中編輯或刪除實際值。 否則，財務健全狀況以及任何與其他財務及會計系統的整合都可能會受到負面影響。 Microsoft Dynamics 365 Project Operations 可讓您在專案商務程序生命週期中的不同時點，使用沖回和取代實際值的方式來編輯實際值。

## <a name="recording-actuals-based-on-project-events"></a>根據專案事件記錄實際值

Project Operations 會將專案業務開發生命週期中發生的財務交易記錄為實體值。 在生命週期的各種事件中建立實際值的作業各不相同，取決於專案業務開發使用的是時間和材料計費模型還是固定價格計費模型，以及此作業是在售前階段還是其本身為內部專案。

下列文章說明不同變化在各種事件中對實際值資料表的影響：

- [時間和材料業務開發中的實際值影響](ActualsonTM.md)
- [在固定價格業務開發中的影響](ActualonFP.md)
- [售前階段和業務開發中的實際值影響](ActualonPreSales.md)
- [內部專案的實際值影響](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
