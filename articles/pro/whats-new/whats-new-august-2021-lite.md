---
title: 2021 年 8 月新增功能 - Project Operations 精簡部署
description: 本主題提供有關 Project Operations 精簡部署 2021 年 8 月發行版本所提供品質更新的資訊。
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e1e0842edaa6153a4780bc799d8df3b6ebb12bba
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323496"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>2021 年 8 月新增功能 - Project Operations 精簡部署

_適用於：精簡部署 - 交易至開立預估發票_

此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

  - Dataverse 環境的 Project Operations 版本 4.13.0.152

## <a name="features-included-in-this-release"></a>此版本包含的功能

此版本包含下列功能：

- **核准集**：核准集會將時間、費用或材料使用核准要求群組成較小的作業子集。 此群組功能允許由專案依特定順序處理核准，並允許重試和排序。 將要求群組在一起，可改善大量核准處理工作的可靠性和可追蹤性。 如需詳細資訊，請參閱[核准集](../../approvals/approval-sets.md)。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 帳單和定價 | 2295625 | 里程碑名稱必須是從發票排程複製到發票明細詳細資料。 |
| 帳單和定價 | 2316323 | 在資源型案例適用的 Project Operations 中，預估發票上的折扣應為不可編輯。 |
|   商機管理 | 2338619 | **商機** 和 **報價** 商務規則只能在頁面上進行叫用。 |
| 資源管理 | 2316523 | 從已附加角色的資源需求中使用 **傳送要求** 時，不應顯示錯誤。 |
| 資源管理 | 2326885 | 透過專案建立資源需求時，不應顯示錯誤。 |
| 時間和費用 | 2335584 | 時間項目中已取代的工作流程。 |
| 時間和費用 | 2336884 | **複製週次** 時間項目按鈕必須不只是對目前的使用者有作用。 |
