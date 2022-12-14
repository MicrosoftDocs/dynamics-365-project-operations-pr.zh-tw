---
title: 2022 年 11 月新增功能 - Project Operations 精簡部署
description: 本文提供有關 Microsoft Dynamics 365 Project Operations 精簡部署 2022 年 11 月發行版本中品質更新的資訊。
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: ed61f8c03c4ab1960aaf97712b3d46dc298ce96a
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831080"
---
# <a name="whats-new-november-2022---project-operations-lite-deployment"></a>2022 年 11 月新增功能 - Project Operations 精簡部署

_**適用於：** 精簡部署 - 交易至開立預估發票_

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.58.0.119 版中的 Project Operations


## <a name="quality-updates"></a>品質更新

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 帳單和定價 | 2781818 | 設定材料使用記錄的預設價格時發生的找不到索引鍵錯誤。 |
| 帳單和定價 | 2922373 | 無法將報價明細連結至已關閉為未成交報價的專案。 |
| 帳單和定價 | 2943206 | [專案實體必須可選用] 中的 **合約明細** 欄位。 |
| 帳單和定價 | 2953182 | 改善更正發票的錯誤訊息。|
| 帳單和定價 | 2959500 | 無法將報價明細連結至已與未成交報價相關聯的專案工作。|
| 帳單和定價 | 2959560 | 在特定地區設定中以成交關閉報價時收到的「此客戶已經在專案合約中」訊息。 |
| 帳單和定價 | 3031727 | 資源指派因必要欄位「msdyn_Company」遺失錯誤而失敗。 |
| 帳單和定價 | 3036905 | 擁有公司永遠不會對 ProjectTeamMember 進行初始化。 |
| 商機管理 | 2763519 | EnsureProjectContractAllowsUpdates 中的 Null 參考錯誤。 |
| 商機管理 | 2783798 | 匯入報價明細的專案估計值時，費用和材料估計值缺少工作描述。|
| 商機管理 | 2988635 | 改善刪除報價中客戶時的錯誤訊息描述。 |
| 商機管理 | 3001191 | 無法從帳務方式指定為 Null 的商機建立報價。 |
| 升級 | 3012324 | 專案轉換在專案中因其名稱中有 Tab 等控制字元而失敗。 || 專案規劃和追蹤 | 2790384 | 擱置中 OperationSet 逾時太短。 |
| 專案規劃和追蹤 | 3044275 | 缺少下列訊息的當地語系化：missingProjectSchedulerErrorMessage。 |
| 專案規劃和追蹤 | 3044277 | 排程取消設定時，專案協調網格未載入。|
| 資源管理 | 2943153 | 要為期間顯示兩位小數位數的 [更新追蹤] 索引標籤。|
| 轉承包 | 2932774 | 「廠商發票明細唯讀」不正確地擲回錯誤。 |
| 轉承包 | 2939556 | 如果廠商發票標題狀態未處於使用中狀態，則刪除明細時不應將該狀態設定為為 [草稿]。 |
| 時間和費用 | 2939998 | 了解 ProjOps 中的新 TESA 版本。 |
