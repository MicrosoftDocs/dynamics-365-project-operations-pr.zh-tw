---
title: Project Operations 中的商務交易
description: 本文提供 Microsoft Dynamics 365 Project Operations 中商務交易概念的概觀。
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923270"
---
# <a name="business-transactions-in-project-operations"></a>Project Operations 中的商務交易

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

在 Microsoft Dynamics 365 Project Operations 中，*商務交易* 是一個沒有任何實體代表的抽象概念。 不過，實體上的一些通用欄位及程序是為了使用商務交易的概念而設計。 下列實體使用了這個概念：

- 報價明細詳細資料
- 合約服務內容詳細資料
- 估計明細
- 帳目明細
- 實際值

在這些實體中，報價明細詳細資料、合約服務內容詳細資料和估計明細是對應至專案生命週期中的 *估計階段*。 帳目明細和實際值實體是對應至專案生命週期中的 *執行階段*。

Project Operations 將所有這五個實體中的記錄視為商務交易。 唯一區別在於，對應至估計階段的實體 (報價明細詳細資料、合約服務內容詳細資料和估計明細) 中記錄視為 *財務預測*，而對應至執行階段的實體 (帳目明細和實際值) 中記錄則視為已發生的 *財務事實*。

如需詳細資訊，請參閱[估計值](../project-management/estimating-projects-overview.md)和[實際值](actuals-overview.md)。

## <a name="concepts-that-are-unique-to-business-transactions"></a>商務交易所特有的概念

下列概念是商務交易概念所特有：

- 交易類型
- 交易分類
- 交易來源
- 交易關係

### <a name="transaction-type"></a>交易類型

交易類型代表對專案產生財務影響的時間和內容。 這是以含有 Project Operations 中下列支援值的選項組來定義：

- 成本
- 專案合約
- 未開單銷售
- 已開單銷售
- 跨組織銷售
- 資源分配單位成本

### <a name="transaction-class"></a>交易分類

交易分類表示專案上產生的不同類型的成本。 這是以含有 Project Operations 中下列支援值的選項組來定義：

- 時間
- 費用
- 資料
- 費用
- 里程碑
- 稅額

> [!NOTE]
> Project Operations 中固定價格帳單的商務規則通常會使用此 **里程碑** 值。

### <a name="transaction-origin"></a>交易來源

交易來源是儲存每個商業交易來源的實體，有助於處理報表和可追蹤性。 當專案執行開始時，每個商務交易都會建立另一個商業交易，而這又會建立其他商務交易，等等。

### <a name="transaction-connection"></a>交易關係

交易關係是儲存兩個類似商務交易 (例如成本與相關銷售實際值) 之間關係的實體，或是由帳務活動 (例如發票確認或發票更正) 所觸發的交易沖回。

交易來源與交易關係實體合起來協助您追蹤商務交易與導致建立特定商務交易的動作之間的關聯。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
