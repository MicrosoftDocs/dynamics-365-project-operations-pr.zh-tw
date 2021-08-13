---
title: 公司間費用
description: 本主題提供相關資訊，說明如何使用公司間費用，以將工作者的費用指派給執行工作所效勞的法律實體。
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001196"
---
# <a name="intercompany-expenses"></a>公司間費用

組織中的一個法律實體所雇用的工作者，可能會為同一個組織中的其他法律實體執行工作。 您可以使用公司間費用，將工作者的費用指派給執行工作所效勞的法律實體。 雇用該工作者的法律實體稱為出借法律實體。 承擔工作者所產生費用的法律實體稱為借用法律實體。 

在工作者可以建立並提交公司間費用之前，您必須先啟用公司間費用明細。 在出借法律實體的 **費用管理參數** 頁面上，選取 **允許公司間費用明細**。 

## <a name="tax-posting-for-intercompany-expenses"></a>公司間費用的稅金過帳

[!include [banner](../includes/banner.md)]

您必須先啟用總帳銷售稅設定中的功能，才能在費用報表中使用與出借 (來源) 法律實體 (而非借用 (目的地) 法律實體) 相關的課稅群組。 當 **公司間稅務過帳法律實體** 參數設定為 **來源**，且 **套用銷售稅課稅規則** 設定為 **否** 時，會使用出借法律實體的稅務組合。 如果將這同一個參數設定為 **目的地**，則會使用借用法律實體的稅務組合。 如果是在美國的法律實體，將此參數設定為 **來源** 時，也必須在新的 **總帳過帳群組** 頁面上設定 **應收銷售稅** 欄位。 會計引擎將會將此欄位中的資訊用於稅務相關的會計分錄。   
不論過帳的費用明細是否與專案有關，其行為都是一致的。  

## <a name="new-expense-expression-builder"></a>新的費用運算式產生器

新的費用運算式產生器可解決使用專案之公司間費用案例的問題。 此功能可確保您建立公司間費用時，已根據費用明細中所選取的專案正確驗證費用原則，而且可以成功提交該費用報表。

若要讓費用運算式產生器功能正常運作，必須先開啟該功能。 此外，也必須設定具有專案識別碼的費用原則。

如果您已經設定對費用明細驗證專案識別碼的原則，則必須停止使用這些原則。 您可以接著開啟此功能，並重新設定原則。

若要開啟功能，請執行下列步驟。

1. 移至 **工作區** \> **功能管理**。
2. 在清單中，選取 **新的費用運算式產生器，用於解決使用專案之公司間費用案例的問題**。 然後選取 **立即啟用**。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
