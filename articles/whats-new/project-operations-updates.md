---
title: Project Operations 更新
description: 此主題提供 Dynamics 365 Project Operations 發行版本的資訊。
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d19148c868aa5be77db59e70fcf1fb8b7de6868c
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213435"
---
# <a name="project-operations-updates"></a>Project Operations 更新

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票，以及庫存/生產型案例適用的 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Project Operations 元件

Dynamics 365 Project Operations 由兩個元件組成：

- Dataverse 環境上的 Project Operations 涵蓋從商機到開立預估發票的功能。 Dataverse 用於 Project Operations 的精簡部署和資源/非庫存案例部署。
- Dynamics 365 Finance 環境中的專案管理與會計涵蓋費用管理功能、專案會計和營收確認。 Finance and Operations 應用程式環境用於資源/非庫存型案例適用的 Project Operations 以及庫存/生產型案例適用的 Project Operations。

## <a name="project-operations-release-notes"></a>Project Operations 版本資訊
- [資源/非庫存](whats-new-may-2021-resource-based.md)案例適用的 Project Operations 最新版本資訊。
- [精簡部署](../pro/whats-new/whats-new-may-2021-lite.md)案例適用的 Project Operations 最新版本資訊。
- [庫存/生產](../prod-pma/whats-new/whats-new-apr-2021-stocked.md)案例適用的 Project Operations 最新版本資訊。

## <a name="project-operations-latest-version"></a>Project Operations 最新版本

| Dataverse 環境上的 Project Operations | Finance and Operations 應用程式環境中的專案管理與會計 | 
| --- | --- |
| 4.10.0.186 | 10.0.18 |

對於 Project Operations 資源/非庫存案例，建議使用雙重寫入協調流程 2.2.2.60 版或更新版本。

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Dataverse 環境中 Project Operations 的發行排程

每月都會提供 Dataverse 環境中 Project Operations 的更新。 

| 站別 | 地區 | 目前版本號碼 | 精簡部署自動更新 | 資源/非庫存部署自動更新 | 下一個版本號碼 | 下一個版本正式發行 |
|-----------|-----------------------|-----------------|--------------|---------------------|---------------------|---------------------|
| 第 1 站 |   &nbsp;              |    &nbsp;       | &nbsp;       |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 第一個版本         |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 5 月 28 日           |
| 第 2 站 |   &nbsp;              |    &nbsp;       | &nbsp;       |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 南美洲         |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 5 月 28 日           |
|    &nbsp; | 加拿大                |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 5 月 28 日           |
|   &nbsp;  | 印度                 |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 5 月 28 日           |
|   &nbsp;  | 法國                |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 5 月 28 日           |
|   &nbsp;  | 阿拉伯聯合大公國  |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 5 月 28 日           |
|   &nbsp;  | 南非          |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 5 月 28 日           |
| 第 3 站 |      &nbsp;           |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 日本                 |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 6 月 4 日          |
|   &nbsp;  | 亞太地區          |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 6 月 4 日          |
|   &nbsp;  | 英國         |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 6 月 4 日          |
|   &nbsp;  | 大洋洲               |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 6 月 4 日          |
| 第 4 站 |     &nbsp;            |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 歐洲                |  4.10.0.186     | 完成     | 完成            | 待定                 | 2021 年 6 月 11 日          |
| 第 5 站 |     &nbsp;            |     &nbsp;      |     &nbsp;   |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | 北美洲         |  4.10.0.186     | 完成     | 2021 年 6 月 11 日          | 待定                 | 2021 年 6 月 18 日          |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Finance and Operations 應用程式環境中專案管理與會計的發行排程

專案管理與會計的更新一年發行八次。

|          支援的版本          | 預覽版可用性 (PEAP) | 正式推出（自我更新） | 自動更新排程 (透過 LCS 更新設定) 生產開始日期 |   終止服務   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.18          |        2021 年 3 月 5 日        |           2021 年 4 月 16 日          |                            2021 年 4 月 30 日                            |    2021 年 7 月 16 日   |
|          10.0.17          |       2021 年 2 月 1 日      |           2021 年 3 月 19 日          |                             2021 年 4 月 2 日                            |    2021 年 6 月 11 日   |

目標發行日期可能會變更。 如需詳細資訊，請參閱[服務更新可用性](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json)。

|          目標版本          | 預覽版可用性 (PEAP) | 正式推出（自我更新） | 自動更新排程 (透過 LCS 更新設定) 生產開始日期 |   終止服務   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.19          |        2021 年 4 月 23 日       |            2021 年 6 月 18 日           |                             2021 年 7 月 2 日                             | 2021 年 9 月 17 日 |
|          10.0.20          |         2021 年 5 月 28 日        |           2021 年 7 月 16 日           |                             2021 年 7 月 30 日                             |  2021 年 10 月 22 日  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
