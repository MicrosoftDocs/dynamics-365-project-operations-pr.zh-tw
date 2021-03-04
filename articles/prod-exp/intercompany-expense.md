---
title: 公司間費用
description: 本主題提供相關資訊，說明如何使用公司間費用，以將工作者的費用指派給執行工作所效勞的法律實體。
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960822"
---
# <a name="intercompany-expenses"></a>公司間費用

組織中的一個法律實體所雇用的工作者，可能會為同一個組織中的其他法律實體執行工作。 您可以使用公司間費用，將工作者的費用指派給執行工作所效勞的法律實體。 雇用該工作者的法律實體稱為出借法律實體。 承擔工作者所產生費用的法律實體稱為借用法律實體。 

在工作者可以建立並提交公司間費用之前，您必須先啟用公司間費用明細。 在出借法律實體的 **費用管理參數** 頁面上，選取 **允許公司間費用明細**。 

## <a name="tax-posting-for-intercompany-expenses"></a>公司間費用的稅金過帳

[!include [banner](../includes/banner.md)]

您必須先啟用總帳銷售稅設定中的功能，才能在費用報表中使用與出借 (來源) 法律實體 (而非借用 (目的地) 法律實體) 相關的課稅群組。 當 **公司間稅務過帳法律實體** 參數設定為 **來源**，且 **套用銷售稅課稅規則** 設定為 **否** 時，會使用出借法律實體的稅務組合。 如果將這同一個參數設定為 **目的地**，則會使用借用法律實體的稅務組合。 如果是在美國的法律實體，將此參數設定為 **來源** 時，也必須在新的 **總帳過帳群組** 頁面上設定 **應收銷售稅** 欄位。 會計引擎將會將此欄位中的資訊用於稅務相關的會計分錄。   
不論過帳的費用明細是否與專案有關，其行為都是一致的。  


[!INCLUDE[footer-include](../includes/footer-banner.md)]