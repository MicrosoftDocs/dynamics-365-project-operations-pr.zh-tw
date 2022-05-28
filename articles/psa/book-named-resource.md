---
title: 透過資源需求預約具名資源
description: 本主題提供有關為一般資源需求預約具名資源的資訊。
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 92a61012beb9aa200f4ea65b777acb0fae04e7e6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590060"
---
# <a name="book-named-resources-from-resource-requirements"></a>透過資源需求預約具名資源

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

您可以預約具名資源，以取代有資源需求的一般資源。

1. 在 Project Service Automation (PSA) 的 **專案** 頁面上，按一下 **團隊** 索引標籤。
2. 從清單中選取具有資源需求的一般資源，然後按一下 **預約**。 或者，開啟資源需求，然後按一下 **預約**。


![預約一般團隊成員。](media/RM-how-to-14.png)


3. 在 **排程小幫手** 頁面上，選取要預約到專案團隊的具名資源，然後按一下 **預約**。

![使用排程小幫手預約一般團隊成員。](media/RM-how-to-15.png)

預約由具名資源完成並履行後，將會以具名資源取代一般資源。

![具名團隊成員取代一般團隊成員。](media/RM-how-to-16.png)

排程上的指派也會以具名資源來更新。

![指派給專案工作的具名團隊成員。](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>使用多個履行具名資源履行一般資源
使用多個具名資源來履行一般資源的需求，類似於指派單一具名資源。 例如，有一項期間為五天且投入量為 120 小時的工作。 這項工作無法由一週五天按一般八小時工作的資源完成。 

![一項需要在五天內投入 120 小時完成的工作。](media/RM-how-to-21.png)

此需求適合 120 小時為期五天 (每天 24 小時) 的機器人工程處理。

![每天需求。](media/RM-how-to-22.png)

這是一個需要多個具名資源來完成一般資源要求的範例。 您需要預約多個資源來履行需求。

![預約多個資源來履行需求。](media/RM-how-to-23.png)

這種案例的主要區別在於，一般資源仍保留在指派給工作的團隊中，而預約的具名資源團隊成員並未指派為職位的一部分。 專案經理可以視需要指派工作至具名資源。 **協調** 檢視表可協助專案經理將跨多個資源的預約細分為工作指派。 系統不自動這樣做，因為在任何較上述簡單範例的複雜的案例中，例如您有大量產生需求的工作時，專案經理要如何指派的意向，必須由系統進行假設。 因為系統無法了解意向，假設可能與預期有所不同，並且會發生不正確或不可預測的結果。 可預知的結果是，在專案經理透過 **協調** 檢視表的協助審慎建立指派之前，一般資源仍保留已指派的狀態。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
