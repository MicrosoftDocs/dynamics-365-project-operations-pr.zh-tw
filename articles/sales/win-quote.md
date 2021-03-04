---
title: 關閉報價
description: 本主題提供有關在 Project Operations 中關閉報價的資訊。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 47804db0144c2b0f9dee2c60518e8aba6fb27473
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124673"
---
# <a name="close-a-quote"></a>關閉報價

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

專案報價可以當做 [成交] 或 [未成交] 來關閉。 Microsoft Dynamics 365 Project Operations 中的報價不支援啟用和修訂功能，因此您可以關閉草稿報價。

## <a name="close-a-quote-as-won"></a>以成交關閉報價

以 [成交] 狀態關閉專案報價，會將報價的狀態設定為 **已關閉**，並將狀態原因設定為 **成交**。 關閉報價會將其設定為唯讀，並建立包含所有報價資訊的草稿專案合約。 已關閉的報價無法重新開啟，因此關閉報價之前，確認對話方塊將會確認您的變更。

Project Operations 的 [專案管理與會計] 模組也已提供根據專案合約所建立的專案報價。 如果專案合約未對應至其任何明細上的專案，則此專案合約會提供做為非使用中專案合約，並在專案至少對應到其中一項合約明細時變成使用中狀態。

如果報價已附加至商機，商機上的任何其他專案報價都會自動以 [未成交] 關閉。

### <a name="financial-impact-of-closing-a-quote-as-won"></a>以成交關閉報價的財務影響

如果專案仍附加至草稿報價時，已有任何記錄在其中的時間實際值，則只會記錄時間或費用的成本。 以 [成交] 關閉報價之後，應用程式會沖銷舊的成本實際值並重新建立新的成本實際值，以重構成本。 應用程式會根據相關聯專案合約服務內容的帳務方式處理這些成本實際值。 如果成本實際值參考時間和材料合約服務內容，系統就會自動在關閉報價並建立專案合約時建立對應的未開單銷售實際值。 如果成本實際值參考固定價格固定價格專案，則應用程式會根據專案合約客戶的分割帳單規則停止重新處理成本實際值。

所有重新處理的實際值皆可在 [專案管理與稽核] 模組中取得，以供專案會計師審查、更新並過帳至總帳。 

## <a name="close-a-quote-as-lost"></a>以未成交關閉報價

以 [未成交] 關閉專案報價，會將狀態設定為 **已關閉**，而將狀態原因設定為 **未成交**。 關閉報價會將其設定為唯讀。 已關閉的報價無法重新開啟，因此關閉報價之前，確認對話方塊會確認您的變更。

如果以 [未成交] 關閉的專案報價有任何明細參考專案時，該專案也會標示為 [已關閉]，而且還會取消那天以後的所有資源預約。

> [!NOTE]
> 在 Project Operations 中，以 [成交] 或 [未成] 交關閉報價並不會影響商機的狀態，商機仍將保持開啟，直到手動將其關閉為止。


[!INCLUDE[footer-include](../includes/footer-banner.md)]