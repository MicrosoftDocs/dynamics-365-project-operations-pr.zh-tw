---
title: 2022 年 2 月新增功能 - Project Operations 精簡部署
description: 本主題提供有關 Project Operations 精簡部署 2022 年 2 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: af66a5f61adf4f016f3fa547bbdfc75d06b2711b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574558"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>2022 年 2 月新增功能 - Project Operations 精簡部署

_適用於：精簡部署 - 交易至開立預估發票_

本主題適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.28.0.120 版中的 Project Operations

## <a name="features-included-in-this-release"></a>此版本包含的功能

從此發行版本開始，您可以將最多可達 300 個的團隊成員新增至單一專案。 在此之前，團隊成員的數目限制為 150 個。 如需詳細資訊，請參閱[專案限制](../../project-management/create-wbs.md#project-limitations)。

## <a name="quality-updates"></a>品質更新

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 帳單和定價 | 2497369 | 材料更正必須遵循 **更正** 參數中的日期值。 |
| 帳單和定價 | 2498697 | 改善 **時間項目回收** 的安全性設定。 |
| 帳單和定價 | 2517455 | 不可允許多次同時對同一份發票觸發 **重新整理的發票明細交易** 動作。 |
| 帳單和定價 | 2517465 | **停用發票明細詳細資料** 動作已因不受支援而遭封鎖。 |
| 帳單和定價 | 2556660 | 修正對已附加至專案參數記錄之價目表進行的日期有效性檢查。 |
|   商機管理 | 2369202 | 更正商務規則，此規則確認是否可將有效性日期重疊的價目表附加至同一份專案合約。 |
|   商機管理 | 2385965 | 更正 **專案合約** 頁面的 **客戶** 索引標籤在您選取 **儲存後關閉** 時的行為。 |
