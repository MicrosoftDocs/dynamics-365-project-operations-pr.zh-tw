---
title: Project Operations 中的轉包合約管理
description: 本主題提供 Microsoft Dynamics 365 Project Operations 中端對端轉包合約管理程序的概觀。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994221"
---
# <a name="subcontract-management-in-project-operations"></a>Project Operations 中的轉包合約管理

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

Microsoft Dynamics 365 Project Operations 支援下列商務程序流程。

![轉包程序流程](../media/SubcontractingProcessFlow.png)

以下逐步說明轉包程序。

1. 專案經理建立廠商的轉包合約。 根據預設，轉包合約使用附加至廠商記錄的價目表。 廠商帳戶的關聯類型為 **廠商** 或 **供應商**。
2. 專案經理可以將所有購買項目逐條列舉為轉包合約上的服務內容項目。 轉包合約服務內容可以是時間、費用或產品的承攬項目。 每項轉包合約服務內容所選取的交易分類決定該服務內容的承攬項目。
3. 廠商帳戶管理員和專案經理可以逐一查看轉包合約。 定價可以在附加至轉包合約的購買價目表中進行調整。
4. 在此時或之後的程序中，如果轉包合約承攬的是時間，則廠商帳戶管理員會將連絡人與每項轉包合約服務內容產生關聯。 此關聯為處理轉包合約的專案經理提供資訊。 當連絡人與轉包合約服務內容有關聯時，如果可預約資源還不存在，系統就會自動從該連絡人建立可預約資源。
5. 每項轉包合約服務內容的帳務方式可以是 **固定價格** 或 **時間和材料**。 對於固定價格轉包合約服務內容，您可以設定按里程碑請款的發票排程。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
