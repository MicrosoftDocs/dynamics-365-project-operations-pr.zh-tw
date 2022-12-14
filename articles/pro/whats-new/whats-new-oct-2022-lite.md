---
title: 2022 年 10 月新增功能 - Project Operations 精簡部署
description: 本文提供有關 Microsoft Dynamics 365 Project Operations 精簡部署在 2022 年 10 月發行版本中，所提供之品質更新的資訊。
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806598"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>2022 年 10 月新增功能 - Project Operations 精簡部署

_**適用於：** 精簡部署 - 交易至開立預估發票_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.57.0.176 版中的 Project Operations

## <a name="features-included-in-this-release"></a>此版本包含的功能

| 功能區域 | 功能名稱 | 更多資訊 |
| --- | --- | --- |
| 專案規劃和追蹤 | **Project Operations 外部排程**<br>外部排程模式可讓客戶在沒有 Project for the Web 目前所強制之限制的情況下，使用原生 Dataverse API，以原生方式建立、更新和刪除與分工結構圖 (WBS) 相關的實體。 | [外部排程](/dynamics365/project-operations/project-management/external-scheduling) |
| 部署和設定 | <p>**允許客戶選擇部署類型**<br>在環境中安裝雙重寫入核心和協調流程解決方案時，Project Operations 的產品驅動更新 (PDU) 可用來自動安裝 Project Operations 雙重寫入解決方案。</p><p>此功能會在專案參數中引入新的 **解決方案升級行為** 參數。 將此參數設定為 **僅精簡版** 時，即使環境中已安裝雙重寫入核心和協調流程解決方案，PUD 都不再自動安裝 Project Operations 雙重寫入解決方案。 此行為會讓計劃使用雙重寫入解決方案將銷售訂單整合至財務和運營應用程式中但又想要在精簡模式下 (也就是，在不整合至財務和營運應用程式的情況下) 使用 Project Operations 的客戶受益。</p> | |

## <a name="quality-updates"></a>品質更新

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 帳單和定價 | 2316317 | 系統允許建立沒有收費交易的發票。 |
| 帳單和定價 | 2737300 | 在存取表單之前，驗證客戶欄位可用性。 |
| 帳單和定價 | 2744948 | 新增對帳務方式的 Null 檢查。 |
| 帳單和定價 | 2763515 | 當發票的銷售合約遺失時出現的 Null 參考錯誤控制代碼。 |
| 帳單和定價 | 2844301 | 批次發票建立作業因發生錯誤而失敗。 |
| 帳單和定價 | 2845869 | 組織服務的儲存體不正確。 |
| 帳單和定價 | 2853729 | 修改帳單類型時，會更新角色和價格詳細資料。 |
| 帳單和定價 | 2940350 | 為實際值定價時，系統應該只會自動輸入有效的價目表。 |
| 部署和設定 | 3001206 | msdyn\_replaylogheader 實體在阻礙客戶組織的升級。 |
| 商機管理 | 2755582 | 分割帳單規則協助程式中的 Null 參考例外狀況控制代碼。 |
| 商機管理 | 2761477 | 使用分割帳單時，刪除里程碑 (標頭) 會留下孤立里程碑。 |
| 商機管理 | 2767595 | 在主要表單中開啟材料使用記錄時，此記錄的可預約資源會變更為目前已登入的使用者。 |
| 專案規劃和追蹤 | 2790384 | 擱置中 OperationSet 逾時太短。 |
| 資源管理 | 2751560 | 資源需求中偏好的組織單位不一致。 |
| 轉承包 | 2907231 | 廠商發票的程序階段無法進展。 |
| 時間和費用 | 2867363 | 當記錄在佇列中等待核准時，記錄未從 [需核准的缺勤/休假] 檢視表中移出。 |
| 時間和費用 | 2894405 | TESA：未使用的 POC 目錄造成合規性問題。 |
