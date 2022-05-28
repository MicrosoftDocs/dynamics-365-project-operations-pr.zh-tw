---
title: 管理專案合約
description: 本主題提供檢視專案型合約的相關資訊。
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 64e81593065d97272af6261e17175c76bd8dca7a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590474"
---
# <a name="manage-project-contracts"></a>管理專案合約

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 中的專案合約，會擷取和管理專案的合約同意承諾和帳單詳細資料。 在 Project Operations 中，專案合約的結構是使用下列元件根據專案量身訂做：

- 合約服務內容，識別將在專案發票上呈現為高階元件之工作的離散元件。
- 合約服務內容詳細資料，識別並估計每個高階元件或合約服務內容的工作。 估計包括關聯至合約服務內容的工作排程和財務方面。
- 合約模型與應收費元件為每個合約服務內容設定，並保持每個合約服務內容和整體合約的帳單安排。

## <a name="view-all-project-based-contracts"></a>檢視所有專案型合約

您可以在 **合約** 清單頁面上看到所有專案合約的清單。 

1. 移至 **銷售** > **合約**。 會顯示系統中所有專案合約的清單。 
2. 選取 **檢視表切換器**（檢視表名稱旁邊的下拉式箭頭）以選取其他篩選過的檢視。 您可以使用自訂篩選準則來建立您自己的檢視。

您可以從此清單頁面或詳細資料頁面建立或刪除合約。

> [!NOTE]
> 無法刪除含有專案、工作、估計值、帳目和/或相關聯實際值的合約。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
