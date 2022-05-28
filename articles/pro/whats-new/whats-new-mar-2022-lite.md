---
title: 2022 年 3 月 - Project Operations 精簡部署新增功能
description: 本主題提供有關 Project Operations 精簡部署 2022 年 3 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583740"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>2022 年 3 月 - Project Operations 精簡部署新增功能

_適用於：精簡部署 - 交易至開立預估發票_

本主題適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.30.0.99 版中的 Project Operations

## <a name="features-included-in-this-release"></a>此版本包含的功能

- 轉包：廠商發票建立及比對體驗

## <a name="quality-updates"></a>品質更新

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 時間和費用 | 2388011 | 進行大量核准時，向時間項目提交者顯示拒絕註解。 |
| 專案規劃和追蹤 | 2495294 | **工作詳細資料** 頁面上的專案詳細資料必須是不可編輯。 |
| 帳單和定價 | 2499605 | 從報價里程碑建立的合約里程碑錯誤地標示為唯讀。 |
| 專案規劃和追蹤 | 2506050 | 如果沒有要儲存的變更，則作業集會保持暫止一小時。 接著會錯誤地將此項作業集標示為 **失敗**，然而必須立即將其完成。 |
| 帳單和定價 | 2507401 | 因快取不正確而在專案中錯誤地輸入預設合約單位。 |
| 帳單和定價 | 2541660 | 雙重寫入中的 **銷售訂單建立驗證** 只能用於專案型訂單。 |
| 帳單和定價 | 2552745 | 稅金未在已設定分割帳單規則的客戶之間分攤。 |
| 帳單和定價 | 2558859 | 改善進行定價維度設定時的錯誤訊息。 |
| 帳單和定價 | 2558933 | 將 **msdyn\_project** 新增為定價維度時，**從專案估計值匯入** 失敗。 |
| 帳單和定價 | 2559101 | 專案參數刪除作業未封鎖，並造成問題。 |
| 商機管理 | 2570390 | 雙重寫入外掛程式強制報價、訂單及商機上的帳戶類型做為 **客戶**，即使該帳戶類型不正確。 |
| 帳單和定價 | 2586097 | 從專案合約服務內容移除專案時，未沖回分割的已開單成本實際值。 |
| 帳單和定價 | 2589619 | 目錄外材料上的稅金會傳播至未開單銷售實際值和發票。 |
|   商機管理 | 2594015 | 對於付款條件為 **Net60** 的客戶，無法以成交關閉報價。 |
| 專案規劃和追蹤 | 2595841 | 在 Project for the Web 中，使用者會在建立新的資源要求時收到有關遺失 **msdyn\_actualstart** 的錯誤訊息。 |
| 時間和費用 | 2602511 | 時間項目的 **拒絕者** 欄位會顯示的拒絕者是 **系統**，而不是具名使用者。 |
| 時間和費用 | 2602528 | 專案核准者可以在其未列為核准者的專案上核准時間。 |
| 帳單和定價 | 2608550 | 即使原始發票沒有發生變更，也可以確認更正發票。 |

## <a name="removed-and-deprecated-features"></a>已移除和已取代的功能

[Project Operations 中已移除或已取代的功能](../../whats-new/removed-depreciated-features-project.md)主題說明 Dynamics 365 Project Operations 已移除或已取代的功能。

- 已移除的功能在產品中不復存在。
- 取代的功能不在主動開發之列，可能會在未來的更新中遭移除。

將任何功能從產品移除之前 12 個月，取代公告會出現在 [Project Operations 中已移除或已取代的功能](../../whats-new/removed-depreciated-features-project.md)主題中。
