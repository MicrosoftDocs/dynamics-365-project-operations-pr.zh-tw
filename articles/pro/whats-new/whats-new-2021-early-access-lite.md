---
title: 2021 年第 2 段浪潮搶先體驗的新增功能 - Project Operations 精簡部署
description: 本文提供有關 Project Operations 精簡部署 2021 年第 2 段浪潮搶先體驗中所提供之功能的資訊。
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924098"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>2021 年第 2 段浪潮搶先體驗的新增功能 - Project Operations 精簡部署

_適用於：精簡部署 - 交易至開立預估發票_

這篇文章適用於下列 Dynamics 365 Project Operations 元件和版本：

  - Dataverse 環境的 Project Operations 版本 4.23.0.4

此版本只有在環境已[選擇加入搶先體驗](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates)時才適用。

## <a name="features-included-in-this-release"></a>此版本包含的功能

[轉包合約管理](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - 此功能可讓您進一步了解並控制專案工作的所有層面。 轉包合約管理預覽版包含下列功能：

  - 專案經理可以建立廠商的轉包合約。 根據預設，轉包合約使用附加至廠商記錄的價目表。 廠商帳戶的關聯類型為 **廠商** 或 **供應商**。
  - 專案經理可以將所有的購買項目逐條列舉為轉包合約上的服務內容項目。 轉包合約服務內容可以是時間、費用或產品的承攬項目。 轉包合約服務內容的交易分類決定該服務內容的承攬項目。
  - 廠商帳戶管理員和專案經理可以逐一查看轉包合約。 定價可以在附加至轉包合約的購買價目表中進行調整。
  - 在此程序中，如果轉包合約服務內容承攬的是時間，則廠商帳戶管理員可以將廠商連絡人與每項轉包合約服務內容建立關聯。 此關聯為處理轉包合約的專案經理提供資訊。 廠商連絡人與轉包合約服務內容有關聯時，如果可預約資源還不存在，系統就會自動從該連絡人建立可預約資源。
  - 每項轉包合約服務內容的計費方式可以是固定價格或時間和材料。 對於固定價格轉包合約服務內容，會設定按里程碑請款的發票排程。
