---
title: 過帳費用報表
description: 本文說明如何過帳費用報表。
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524859"
---
# <a name="post-expense-reports"></a>過帳費用報表

費用報表經核准並轉入一般帳目之後，即可進行過帳。 將費用報表過帳時，系統會識別符合退還加值稅 (VAT) 資格的費用。 驗證和退還加值稅付款的工作會指派給負責驗證費用報表的員工。

如果費用報表上的費用是向該員工雇用公司以外的公司收取，您必須驗證應付和應收這些費用的兩家公司。 例如，提交費用報表的員工任職於 DAT 公司，但是向 DIR 公司收取了費用。 在這種情況下，DAT 是應付費用的公司，而 DIR 是應收費用的公司。 驗證這些帳目明細之後，您可以將費用明細過帳至總帳。

若要將費用報表過帳，請在 **核准的費用報表** 頁面上選取費用報表，然後在動作窗格中選取 **過帳**。

您也可以同時將清單中所有的費用報表過帳。 選取所有費用報表，然後選取 **過帳**。

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>啟用「以廠商貨幣針對現金支付方式過帳費用負債」的功能

**以廠商貨幣針對現金支付方式過帳費用負債** 的功能，可讓費用報表以現金支付方式依廠商貨幣過帳。

目前，當您提交現金費用時，會以記帳貨幣來過帳支出報表。 因涉及交易貨幣、記帳貨幣和廠商貨幣之間的金額轉換，所以如果費用和實際付款日期的匯率不同，則支付給廠商金額可能會不正確。

這項功能將確保在過帳費用報表時，以廠商貨幣記錄廠商餘額。

1. 移至 **工作區** \> **功能管理**。
2. 在清單中尋找並選取 **以現金支付方式依產商貨幣過帳費用負債** 來張貼廠商貨幣的費用責任，然後選取 **立即啟用**。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
