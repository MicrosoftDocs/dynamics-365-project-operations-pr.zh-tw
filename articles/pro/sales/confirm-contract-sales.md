---
title: 確認專案合約
description: 本主題提供有關如何在 Project Operations 中確認合約的資訊。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128273"
---
# <a name="confirm-a-project-contract"></a>確認專案合約

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 中的專案合約可以藉 **已確認** 的原因進入使用中狀態，或是以 **未成交** 的原因來關閉。 確認專案合約時，狀態會從 **草稿** 更新為 **使用中**，而且狀態原因為 **已確認**。 您無法編輯或重新開啟使用中或已關閉的合約。 

### <a name="financial-impact-of-confirming-a-project-contract"></a>確認專案合約所產生的財務影響

確認專案合約之後，應用程式會沖銷舊的成本實際值並建立新的成本實際值，以重新計算成本。 接著會根據相關聯專案合約服務內容的帳務方式處理新的成本實際值。 如果成本實際值參考時間和材料合約服務內容，則應用程式會自動重新建立對應的未開單銷售實際值。 如果成本實際值參考固定價格合約服務內容，則應用程式會停止重新處理成本實際值。

系統會評估對實際值的不得超過限制、可收費率設定、定價和成本計算，並在確認程序期間加以更新。

## <a name="close-a-project-contract-as-lost"></a>以未成交關閉專案合約

以未成交關閉專案合約時，合約狀態會更新為 **已關閉**，而且狀態原因為 **未成交**。 專案合約會變成唯讀。 因為您無法重新開啟已關閉的專案合約，系統會在變更完成之前提供確認對話方塊。

如果以未成交關閉的專案合約在其服務內容中參考某個專案，也會將這個專案標示為已關閉。 任何從那天以後的資源預約都會取消。 專案合約中任何尚未列於發票的未開單銷售實際值都將予以沖銷。

> [!NOTE]
> 在 Dynamics 365 Project Operations 中，以未成交關閉專案合約，並不會影響相關商機的狀態。 商機仍將保持開啟，並必須以手動方式關閉。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]