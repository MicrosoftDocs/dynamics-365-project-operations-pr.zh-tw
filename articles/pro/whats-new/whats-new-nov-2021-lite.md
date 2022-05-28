---
title: 2021 年 11 月新增功能 - Project Operations 精簡部署
description: 本主題提供有關 Project Operations 精簡部署 2021 年 11 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f3a19cddd1b91fc76c852153526fb7197a9f92c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587760"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>2021 年 11 月新增功能 - Project Operations 精簡部署

_適用於：精簡部署 - 交易至開立預估發票_

本主題適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.26.0.145、4.26.0.148、4.26.0.150、4.26.0.155 版中的 Project Operations
  
## <a name="features-included-in-this-release"></a>此版本包含的功能

此版本包含下列功能：

- 專案排程應用程式開發介面 (API) 現在支援建立和刪除專案貯體的功能

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-in-dataverse"></a>Dataverse 中的Project Operations

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 帳單和定價 | 2358236 | 發票更正必須允許進行價格為零之明細的修正。 |
| 資源管理 | 2410072 | 允許設定以專案經理身分指派至工作的資源。 |
| 帳單和定價 | 2430234 | 修正成本績效計算問題。 |
| 時間和費用 | 2436978 | 允許以 hh:mm 格式輸入時間。 |
| 帳單和定價 | 2448623 | 允許價目表在與組織單位建立關聯之後進行更新。 |
| 時間和費用 | 2460396 | 允許透過清除儲存格的方式刪除時間項目。 |
| 帳單和定價 | 2467386 | 即使在工作已與已成交報價產生關聯時，仍允許有工作要刪除的專案。 |
| 時間和費用 | 2461744 | **我失敗的核准** 檢視表僅包含狀態為 **已提交** 的專案核准。 |
| 時間和費用 | 2464082 | 當目標狀態符合時，移除從專案核准到核准集的連結。 |
| 時間和費用 | 2468108 | 排程工作不可為核准集設定 **處理中** 狀態。 |
| 時間和費用 | 2471503 | 刪除存留超過七天的核准集。 |
| 帳單和定價 | 2480687 | 建立報價明細里程碑時，不能移除報價明細參考。 |
