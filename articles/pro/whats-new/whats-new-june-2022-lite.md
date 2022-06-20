---
title: 2022 年 6 月新增功能 - Project Operations 精簡部署
description: 本文提供有關 Microsoft Dynamics 365 Project Operations 精簡部署 2022 年 6 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959390"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>2022 年 6 月新增功能 - Project Operations 精簡部署

_**適用於：** 精簡部署 - 交易至開立預估發票_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.43.0.77 版中的 Project Operations

## <a name="quality-updates"></a>品質更新

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 轉承包 | 2708885 | 修正使用者建立未填入可預約資源之可預約資源預約標題記錄時出現的錯誤訊息。 |
| 專案規劃和追蹤 | 2629441 | 更正工作流程觸發邏輯，以協助避免在更新專案工作時出現無限迴圈。 |
| 時間和費用 | 2641209 | 從指派/預約匯入的時間項目必須保留可預約資源參考。 |
| 專案規劃和追蹤 | 2651148 | 必須保護專案文件標頭。|
| 專案規劃和追蹤 | 2653145 | 新增驗證，以確保無法建立名稱中包含無效字元的專案記錄。 |
| 時間和費用 | 2654710 | 更正 **核准** 頁面上的篩選功能。 |
| 帳單和定價 | 2667805 | 新增驗證，以協助避免在沒有支援的未開單銷售實際值時建立已開單銷售實際值。 |
| 帳單和定價 | 2668378 | 新增驗證，以協助避免在未填入邏輯名稱和欄位名稱時新增自訂定價維度。 |
| 時間和費用 | 2700428 | 改善核准邏輯，以確保即使其中一個核准集停滯在系統作業中，也可以處理專案的其他核准集。 |
