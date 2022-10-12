---
title: 2022 年 9 月新增功能 - Project Operations 精簡部署
description: 本文提供有關 Microsoft Dynamics 365 Project Operations 精簡部署 2022 年 9 月發行版本中品質更新的資訊。
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621223"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>2022 年 9 月新增功能 - Project Operations 精簡部署

_**適用於：** 精簡部署 - 交易至開立預估發票_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.46.0.60 版中的 Project Operations

## <a name="features-included-in-this-release"></a>此版本包含的功能

| 功能區域 | 功能名稱 | 更多資訊 |
| --- | --- | --- |
| 商機管理 | **報價的修訂與啟用**<br>Project Operations 會提供銷售處理的完整支援。 可啟動專案報價來代表一個狀態，在此狀態中報價是唯讀且正被檢閱中。 可以修訂已啟動的報價，以建立具有遞增修訂版本編號的新報價。 啟用的專案報價或報價修訂可以成交或未成交狀態來關閉。 | [啟動和修訂專案報價](/dynamics365/project-operations/sales/activation-and-revision) |
| 帳單和定價 | **時區互通的價格預設**<br>Project Operations 在所有專案實際值上引進了時區互通日期的概念。 新的欄位 (**交易日期**) 現在可在帳目明細和實際值上使用，並將用來儲存交易發生的日期，但是不會將該日期轉換為國際標準時間。 此日期將用於下游處理，例如價格預設和發票建立。 | <p>[決定專案估計值及實際值的成本費率](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[判斷專案估計值及實際值的銷售價](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| 帳單和定價 | **Project Operations 中的日期有效價格覆寫**<br>有效期限內價格覆寫提供覆寫或變更價目表中特定價格的方法。 | [有效期限內價格覆寫](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| 時間和費用 | **全域核准者**<br>此功能啟用獨立軟體廠商 (ISV) 和集中核准，無論專案中的專案或團隊成員狀態為何。 | [安全性與核准](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>品質更新

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 帳單和定價 | 2754422 | 當專案在 Dataverse 中複製時，原料和費用估算不會流向 Dynamics 365 Finance。 |
| 時間和費用 | 2787409 | 非有效的核准者可以核准非專案時間項目。 |
| 商機管理 | 2788907 | 在包含標誌之訂單內容的唯一性驗證上，更新錯誤訊息。 |
| 時間和費用 | 2842253 | 用於時間審核的空例外狀況處理。 |
| 帳單和定價 | 2844181 | 無法取得關聯性識別碼，阻礙了發票建立。 |
| 帳單和定價 | 2876628 | QLD，CLD -估計價目表解決方案應使用價目表的舊版日期範圍欄位。 |
| 轉承包 | 2893222 | 如果未指定轉包合約服務內容的角色，則應該可以為任何角色在團隊成員上選取該內容。 |
