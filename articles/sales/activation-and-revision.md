---
title: 啟動和修訂專案報價
description: 本文提供有關如何在 Microsoft Dynamics 365 Project Operations 中啟動和修訂報價的資訊。
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410318"
---
# <a name="activate-and-revise-a-project-quote"></a>啟動和修訂專案報價

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

啟動和修訂功能可協助您在估計和交涉階段追蹤專案型報價的版本。 報價草稿會在啟動後變成唯讀。

啟動及修訂功能可讓您執行下列工作：

- 讓報價僅在啟動後成交或不成交。
- 修訂報價以變更現有報價或建立新版本。

> [!NOTE]
> 啟用報價的啟動和修正功能後，無法停用此功能。

若要開啟啟動和修訂專案報價的功能，請執行下列步驟。

1. 移至 **設定**\>**參數**。
1. 開啟 **參數** 記錄。
1. 在動作窗格的 **功能控制** 索引標籤上，選取 **啟用報價啟動及修訂**。
1. 在確認對話方塊選取 **確定**。
1. 片刻之後，重新整理瀏覽器。 現在應該可以使用啟動和修訂功能。 如果動作窗格中不再出現 **啟用報價啟動及修訂** 按鈕，即可知這些功能已啟用。

## <a name="activating-a-quote"></a>啟動報價

啟用報價的啟動及修訂功能之後，動作窗格中的 **以成交關閉報價** 和 **以未成交關閉報價** 按鈕無法用於草稿專案報價。 只有在啟動報價後，才能使用這些按鈕。

啟動表示您要預防在報價程序中對報價進行其他變更的階段。 報價會在此階段送出供內部審查或發送給客戶。

動作窗格中的 **以成交關閉報價** 和 **以未成交關閉報價** 按鈕可用於已啟動的報價。 視內部或客戶審查的結果而定，您可以使用這其中一個按鈕來關閉已啟動的報價。 您可以選取 **修訂報價**，對啟動的報價進行交涉和變更。

## <a name="revising-a-quote"></a>修訂報價

如果您必須變更已啟動的報價，請選取 **修訂報價**。 報價已關閉，並使用 **已修訂** 原因代碼。 接著會建立識別碼相同但修訂編號遞增的新報價。 原始報價的所有詳細資料都會複製到新報價。 新報價會處於草稿狀態，並且可以視需要進行編輯。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
