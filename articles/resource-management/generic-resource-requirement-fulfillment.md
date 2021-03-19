---
title: 一般資源需求履行
description: 本主題提供有關如何為一般資源需求預約具名資源的資訊。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279578"
---
# <a name="generic-resource-requirement-fulfillment"></a>一般資源需求履行

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

您可以預約具名資源，以取代有資源需求的一般資源。

1. 在 **專案** 頁面上，選取 **團隊** 索引標籤。
2. 從清單中選取具有資源需求的一般資源，然後選取 **預約**。 或者，開啟資源需求，然後選取 **預約**。
3. 在 **排程小幫手** 頁面上，選取要預約到專案團隊的具名資源，然後選取 **預約**。

預約由具名資源完成並履行後，將會以具名資源取代一般資源。

排程上的指派也會以具名資源來更新。

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>使用多個履行具名資源履行一般資源
使用多個具名資源來履行一般資源的需求，類似於指派單一具名資源。 例如，有一項期間為五天且投入量為 120 小時的工作。 這項工作無法由一般以五天為一週、每天工作八小時的資源完成。 

此需求適合 120 小時為期五天 (每天 24 小時) 的機器人工程處理。

這是一個需要多個具名資源來完成一般資源要求的範例。 您需要預約多個資源來履行需求。

這種案例的主要區別在於，一般資源仍保留在指派給工作的團隊中，而預約的具名資源團隊成員並未指派為職位的一部分。 專案經理可以視需要指派工作至具名資源。 **協調** 檢視表可協助專案經理將跨多個資源的預約細分為工作指派。 系統不自動這樣做，因為在任何比上述簡單範例還要複雜的案例中 (例如您有大量產生需求的工作時，或專案經理要如何指派的意向)，都必須由系統進行假設。 因為系統無法了解意向，假設可能會與預期的不同，而且會發生不正確或不可預測的結果。 可預知的結果是，在專案經理透過 **協調** 檢視表的協助審慎建立指派之前，一般資源仍保留已指派的狀態。




[!INCLUDE[footer-include](../includes/footer-banner.md)]