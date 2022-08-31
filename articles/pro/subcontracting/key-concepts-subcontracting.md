---
title: 轉承包中的重要概念
description: 本文說明一些適用於 Microsoft Dynamics 365 Project Operations 中的轉承包的重要概念。
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e75f2cf9c1092604e43e5cb60dda0e2a1b7dcd64
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262159"
---
# <a name="key-concepts-in-subcontracting"></a>轉承包中的重要概念


_**適用於：** 精簡部署 - 交易至開立預估發票_

這篇文章說明一些在您開始使用 Microsoft Dynamics 365 Project Operations 的轉承包功能之前，應該了解的重要概念。

## <a name="contracting-unit-on-the-subcontract"></a>轉包合約上的合約單位

合約單位表示負責交付最終專案的部門或事務所。 合約單位也是與廠商締結合約關係的部門。

## <a name="purchase-currency"></a>採購貨幣

在 Project Operations 中，採購貨幣是建立轉包合約時所用的貨幣。 這也是在專案上記錄轉包商成本所用的貨幣。 採購貨幣可與專案貨幣不同，而專案貨幣又可以不同於銷售貨幣。

## <a name="billing-methods-on-subcontract-lines"></a>轉包合約服務內容的帳務方式

專案通常有固定服務費和按用量計費合約模型。 Project Operations 在銷售和採購內容中支援這些帳務方式。 針對採購，帳務方式以下列方式運作：

- **時間和材料** – 當轉包合約服務內容使用 **時間和材料** 帳務方式時，時間成本會在專案上記錄為轉包商在該專案和記錄時間上的工作。 轉包商的這些成本交易接著與廠商發票上的明細項目相比對。 在此模型中，使用 Project Operations 的專案經理可以將廠商發票明細與已記錄且核准的轉包商時間相比對並驗證。 驗證完成後，會沖銷核准後記錄的先前成本實際值，並在專案上建立以廠商發票為依據的新成本實際值。
- **固定價格** – 在此固定服務費合約模型中，廠商發票是根據固定里程碑所建立。 不過，轉包商資源也可以報告時間。 然後由專案經理審查並核准此時間。 核准時，Project Operations 會在專案上建立暫時成本實際值。 廠商傳送里程碑的發票後，專案經理可以將先前所記錄的成本實際值與里程碑進行比對。 驗證完成時，沖銷成本實際值，並記錄按里程碑列計的成本。

## <a name="project-price-lists-on-subcontracts"></a>轉包合約上的專案價目表

專案價目表是用於設定時間、費用及其他專案相關元件之購買價格的價目表。 可以有多份價目表，其中每一份在 Project Operations 中皆可有各自的限期生效轉包合約。 Project Operations 對於轉包合約不支援專案價目表的有效日期重疊。

## <a name="transaction-classes-on-subcontracts"></a>轉包合約上的交易分類

Project Operations 支援四種類型的交易分類：

- 時間
- 費用
- 材料
- 費用

只能在 **時間**、**費用** 和 **材料** 交易分類上估計和產生採購成本。 **服務費** 是僅以收入列計的交易分類，無法在採購內容中使用。

## <a name="purchase-pricing-dimensions"></a>採購定價維度

定價維度可讓您決定將哪些屬性用於購買價格設定和時間交易預設設定。 在採購方面，Project Operations 僅支援購買價格設定及預設設定的固定維度集。 對轉包合約服務內容和轉包合約時間交易進行購買價設定與預設設定時，這些屬性是 **角色** 和 **可預約資源**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
