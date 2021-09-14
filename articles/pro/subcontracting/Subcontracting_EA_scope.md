---
title: 2021 年 10 月搶先體驗版本中的轉承包
description: 本主題提供 Project Operations 中屬於 2021 年 10 月搶先體驗版本之轉承包功能的概觀。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383685"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>2021 年 10 月搶先體驗版本中的轉承包

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

本主題提供 Dynamics 365 Project Operations 中屬於 2021 年 10 月搶先體驗版本之轉承包功能的概觀。 此功能集尚未就緒，無法用於生產環境或即時環境，因此在發行完整功能集之前，這些功能仍將保留在搶先體驗版本中。 在預覽版橫幅移除之前，強烈建議您不要將轉承包功能集用於即時生產案例。 

下列清單提供 2021 年 10 月搶先體驗版本中目前可用功能的大綱。

1. 專案經理建立廠商的轉包合約。 根據預設，轉包合約使用附加至廠商記錄的價目表。 廠商帳戶的關聯類型為 **廠商** 或 **供應商**。

2. 專案經理可以將所有購買項目逐條列舉為轉包合約上的服務內容項目。 轉包合約服務內容可以是時間、費用或產品的承攬項目。 轉包合約服務內容的交易分類決定該服務內容的承攬項目。

3. 廠商帳戶管理員和專案經理可以逐一查看轉包合約。 定價可以在附加至轉包合約的購買價目表中進行調整。

4. 在此時或之後的程序中，如果轉包合約承攬的是時間，則廠商帳戶管理員會將廠商連絡人與每項轉包合約服務內容產生關聯。 此關聯為處理轉包合約的專案經理提供資訊。 廠商連絡人與轉包合約服務內容有關聯時，如果可預約資源還不存在，系統就會自動從該連絡人建立可預約資源。

5. 每項轉包合約服務內容的帳務方式可以是 **固定價格** 或 **時間和材料**。 對於固定價格轉包合約服務內容，會設定按里程碑請款的發票排程。

「概觀」中所述轉承包商務程序流程的其餘步驟目前無法使用。 本主題會隨著新功能的加入進行更新。 

下圖呈現與端對端商務程序相比之下的轉承包功能搶先體驗版本。

![轉包程序流程](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>數量型或工作型轉包合約服務內容搶先體驗版本
在 2021 年 10 月搶先體驗版本中，僅支援數量型轉包合約服務內容。 這表示轉包合約服務內容可用來從廠商那裡購買的是時間、費用或材料，而不是一整套完整的工作。 這也意味著，透過轉包合約服務內容所購買的數量 (時間單位數、費用單位數或材料數量料) 可用於系統中的任何專案。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
