---
title: 貨幣不符錯誤
description: 本主題提供有關儲存特定記錄類型時所發生貨幣不符錯誤的疑難排解資訊。
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903360"
---
# <a name="currency-mismatch-error"></a>貨幣不符錯誤 

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

儲存專案、合約、報價或可預約資源時，您可能會收到這個錯誤 **擁有公司的貨幣與合約單位的貨幣不相符。請選擇其他擁有公司或合約單位以繼續**。 這是因為記錄的合約單位貨幣與擁有公司貨幣之間發生貨幣不相符的情況。


## <a name="resolution"></a>解決方法

若要解決此問題，請執行下列動作：
- 驗證此記錄的合約單位貨幣。 您可以開啟組織單位記錄，並在 **一般** 索引標籤中確認 **貨幣** 欄位的值，以查看貨幣。
- 確認擁有公司的貨幣。 您可以移至公司記錄中的 **相關** > **總帳** 來查看貨幣。 按兩下與公司相關聯的總帳記錄，並在 **一般** 索引標籤上確認 **會計貨幣** 欄位中的值。

如果合約單位中設定的貨幣與總帳記錄不相符，請調整設定，或在儲存記錄時選取不同的值。 系統要定這些記錄必須相符，才能確保公司間的開立發票流程正確。 如需公司間設定的詳細資訊，請參閱[建立公司間交易](../../project-accounting/create-intercompany-transactions.md)。

如果公司記錄沒有相關聯的總帳記錄，這表示設定環境時，有遺漏的設定。 必須由系統管理員來更正設定。 系統管理員必須移至 **雙重寫入設定**，然後透過 **總帳雙重寫入對應** 及其先決條件的初始同步停止並重新啟重此對應。 如需詳細資訊，請參閱 [Project Operations 雙重寫入對應版本](../../environment/resource-dual-write-maps.md)。
