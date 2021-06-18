---
title: 結束報價 - 精簡
description: 本主題提供有關在 Project Operations 中關閉報價的資訊。
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994126"
---
# <a name="close-a-quote---lite"></a>結束報價 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_

專案報價可以當做 [成交] 或 [未成交] 來關閉。 您可以關閉草稿報價，因為 Microsoft Dynamics 365 Project Operations 不支援對報價進行的啟用和修訂作業。

## <a name="close-a-quote-as-won"></a>以成交關閉報價

將專案報價關閉為 [成交] 時，狀態會設定為 [已關閉]，而狀態原因是 [成交]。 關閉報價會將專案報價變成唯讀，並建立包含報價資訊的草稿專案合約。 因為無法重新開啟已關閉的報價，確認對話方塊將會確認您的變更。

如果報價已附加至商機，商機上的任何其他專案報價都會自動以 [未成交] 關閉。

### <a name="financial-impact-of-closing-a-quote-as-won"></a>以成交關閉報價的財務影響

如果仍附加至草稿報價時，專案上的時間有任何實際值，則只會記錄時間或費用的成本。 以 [成交] 關閉報價之後，應用程式會沖銷舊的成本實際值並重新建立新的成本實際值，以重構成本。 應用程式會根據相關聯專案合約服務內容的帳務方式處理這些成本實際值。 如果成本實際值參考時間和材料合約服務內容，就會在關閉報價並建立專案合約時，建立其對應的未開單銷售實際值。 如果成本實際值參考固定價格合約服務內容，則應用程式會停止重新處理根據專案合約客戶分割帳單規則所定的成本實際值。

## <a name="closing-a-quote-as-lost"></a>以未成交關閉報價：

將專案報價關閉為 [未成交] 時，狀態會設定為 [已關閉]，而狀態原因是 [未成交]。 關閉報價會將專案報價設定為唯讀。 已關閉的報價無法重新開啟，因此關閉報價之前，確認對話方塊會確認您的變更。

如果以 [未成交] 關閉的專案報價參考其任一明細上專案，該專案也會標示為 [已關閉]。 任何從那天以後的資源預約都會取消。

> [!NOTE]
> 在 Project Operations 中，以 [成交] 或 [未成] 交關閉報價並不會影響商機的狀態，商機仍將保持開啟，直到手動將其關閉為止。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]