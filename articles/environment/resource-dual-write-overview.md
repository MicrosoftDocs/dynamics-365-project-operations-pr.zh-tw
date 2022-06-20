---
title: Project Operations 雙重寫入整合
description: 本文提供 Project Operations 雙重寫入整合的概觀。
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927962"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operations 雙重寫入整合概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

Project Operations 使用[雙重寫入功能](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page)，在 Microsoft Dataverse 和 Dynamics 365 Finance 之間同步處理資料。

下圖顯示資料如何在 Dataverse 與 Finance 之間整合的過程中進行同步處理。

![Project Operations 資料流程概觀。](./media/ProjectOperationsFlows.jpg)

Project Operations on Dataverse 使用 Power Platform 功能來提供新式使用者介面 (UI) 和簡易無程式碼/少量程式碼擴充性。 專案經理、資源管理員、專案團隊成員及其他前台系統角色會在 Dataverse 上的 Project Operations 中執行他們的活動。

Finance 中的 Project Operations 提供專案會計及收入認列支援。 Project Operations 會做為外掛程式插入 Finance 的銷售稅計算、貨幣匯率、財務維度報表等財務架構中。 專案會計師體驗大多以 Finance 為基準。

Project Operations 整合包含下列元件整合：


- [Project Operations 設定和設定資料整合](resource-dual-write-setup-integration.md) 
- [專案估計值和實際值](resource-dual-write-estimates-actuals.md)
- [專案發票](resource-dual-write-project-invoice.md)
- [費用管理](resource-dual-write-expense.md)
- [廠商發票](resource-dual-write-vendor-invoice.md)
