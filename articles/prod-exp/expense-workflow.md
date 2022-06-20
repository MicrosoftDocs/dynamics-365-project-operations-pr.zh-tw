---
title: 費用管理工作流程
description: 本文說明如何在 Microsoft Dynamics 365 Finance 中使用工作流程系統，以在費用管理中設定費用報表的審查程序。
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71efc89d9167ef1ee546c67c123efeb37125cc02
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929710"
---
# <a name="expense-management-workflow"></a>費用管理工作流程

您可以使用工作流程系統來設定費用管理中的費用報表審查程序。 您可以設定使用下列準則的工作流程，以判斷費用報表的核准者：

- 員工報告階層以及預先定義的核准限制
- 支援暫時核准者及最終核准者的多層核准
- 財務維度與專案責任
- 指派給特定使用者或使用者群組

您可以建立費用報表、差旅申請、預付現金和加值稅 (VAT) 退還的工作流程核准。

**範例**

下列程序是費用報表的費用管理工作流程範例。

1. 員工建立並儲存費用報表。
2. 員工提交費用報表以供核准。 根據設定工作流程時所定義的規則來識別核准者。
3. 核准者收到費用報表已準備好進行核准的通知。 核准者審查費用報表，並確認是否符合下列條件：

    - 費用未違反任何費用原則。 如果費用違反原則，則核准者會確認費用報表包含有效的業務理由。
    - 將電子收據附加至費用報表。

4. 核准者核准費用報表。
5. 將費用報表指派給應付帳款會計專員以進行過帳。
6. 根據是否已設定自動過帳，進行下列其中一個步驟：

    - 如果已設定自動過帳，則處理費用報表以進行付款，並更新費用報表的狀態。
    - 如果未設定自動過帳，則應付帳款會計專員會確認是否所有的原始收據都已提交，以及收據是否與費用報表中的費用相符。 所有在費用報表上輸入的稅碼也都必須確認為正確。

確認過這些這些需求之後，將費用報表過帳。

將費用報表過帳之後，費用報表的付款便會獲得授權，並撥款給員工。


[!INCLUDE[footer-include](../includes/footer-banner.md)]