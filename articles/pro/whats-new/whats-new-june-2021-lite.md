---
title: 2021 年 6 月新增功能 - Project Operations 精簡部署
description: 本主題提供有關 Project Operations 精簡部署 2021 年 6 月發行版本所提供品質更新的資訊。
author: sigitac
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 06ea83152e4f601ef842a0f8d975c16c2be95612
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583896"
---
# <a name="whats-new-june-2021---project-operations-lite-deployment"></a>2021 年 6 月新增功能 - Project Operations 精簡部署

_適用於：精簡部署 - 交易至開立預估發票_

此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

  - Dataverse 環境版本 4.11.0.156 或 4.11.0.164 上的 Project Operations。

## <a name="quality-updates"></a>品質更新

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 帳單和定價 | 2281417 | 修正有關透過發票排程自動建立發票之動作失敗的問題。 |
| 帳單和定價 | 2287835 |   改善發票確認效能。 |
| 商機管理 | 2222555 | 使用 **從專案估計匯入** 時，必須將材料估計可收費率選正確複製到報價明細詳細資料。 |
| 商機管理 | 2223427 | **GenerateRetainersFromRetainerScheduleOptions** 動作現在允許自訂。 |
| 商機管理 | 2277528 | 修正對包含多個客戶的專案合約服務內容的帳單里程碑值計算。 |
| 專案規劃和追蹤 | 2226110 | 修正 **專案團隊** 網格中 **產生需求** 功能的間歇性問題。 |
| 專案規劃和追蹤 | 2208109 | 使用者無法建立使用一種貨幣但其相關工作卻使用另一種貨幣的專案。 |
| 專案規劃和追蹤 | 2258228 | 允許使用排程 API 修改 **排程** 實體的欄位清單已更新。 |
| 專案規劃和追蹤 | 2293989 | 必須將正確的語言和地區設定傳遞至 **專案工作** 網格。|
| 資源管理 | 2220493 | 修正 **工作** 網格在快速將資源要求標示為完成時的使用者體驗。 |
| 資源管理 | 2330496 | 修正 **排程面板** 載入問題。 (品質更新可在版本 4.11.0.164 中取得) |
| 時間和費用 | 2194431 | **時間項目** 網格必須遵循 **系統設定** 中所設定的當週開始日。 |
| 時間和費用 | 2277311 | 刪除 **時間項目** 網格中儲存格的值之後，游標仍然留在網格中。 |
