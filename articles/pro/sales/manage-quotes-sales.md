---
title: 管理專案報價
description: 本文提供專案報價的相關資訊。
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b9dad9ab9b6cef11ad337f9c3f536fe467b6a347
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911632"
---
# <a name="manage-project-quotes"></a>管理專案報價

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

在 Dynamics 365 Project Operations 中，專案報價的設計目的是為了協助建置專案工作的提案。 在 Project Operations 中，專案報價的結構是針對具有以下元件的專案提案而建構的：

  - 報價明細，識別將呈現為高階元件之工作的離散元件。
  - 報價明細詳細資料，識別並估計每個高階元件或報價明細的工作。 排程或日期估計，以及關聯至報價明細的工作財務方面。
  - 會為每個報價明細設定合約模型與應收費元件。 此設定有助於估計每個報價明細和整體報價的營收、支出和獲利率的分佈。

## <a name="view-all-project-based-quotes"></a>檢視所有專案型報價

您可以在 **報價** 清單頁面上看到所有專案報價的清單。 

1. 移至 **銷售** > **報價**。 會顯示系統中所有專案報價的清單。 
2. 使用 **檢視表切換器** 選取報價的其他篩選過的檢視。 您可以使用自訂篩選準則來設定自己的檢視和導覽選項。

您可以從此清單頁面或詳細資料頁面建立或刪除報價。

 > [!NOTE]
 > 無法刪除含有專案、工作、估計值、帳目和/或相關聯實際值的報價。 此外，當報價以成交或未成交關閉時，也無法再加以刪除或修改。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
