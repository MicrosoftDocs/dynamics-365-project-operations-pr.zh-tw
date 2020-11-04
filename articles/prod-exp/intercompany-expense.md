---
title: 公司間費用
description: 組織中的一個法律實體所雇用的工作者，可能會為同一個組織中的其他法律實體執行工作。 在這種情況下，您可以使用公司間費用功能，將工作者的費用指派給為之執行工作的法律實體。
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073147"
---
# <a name="intercompany-expenses"></a>公司間費用

[!include [banner](../includes/banner.md)]

組織中的一個法律實體所雇用的工作者，可能會為同一個組織中的其他法律實體執行工作。 在這種情況下，您可以使用公司間費用功能，將工作者的費用指派給為之執行工作的法律實體。 雇用該工作者的法律實體稱為出借法律實體。 承擔工作者所產生費用的法律實體稱為借用法律實體。 

工作者在出借法律實體的 **費用管理參數** 頁面上針對他為不同法律實體執行的工作建立並提交費用之前，請選取 **允許公司間的費用明細** 選項。 

## <a name="tax-posting-for-intercompany-expenses"></a>公司間費用的稅金過帳

[!include [banner](../includes/banner.md)]

如果您想要在費用報表中使用與出借 (來源) 法律實體相關，而不是與借用 (目的地) 法律實體相關的課稅群組，就必須在總帳銷售稅設定中設定此關聯。 將總帳參數 **公司間稅金過帳法律實體** 設定為 **來源** ，並將 **套用銷售稅課稅規則** 設定為 **否** 時，將會使用出借法律實體的稅務組合。 如果將這同一個參數設定為 **目的地** ，則會使用借用法律實體的稅務組合。 如果是在美國的法律實體，將此參數設定為 **來源** 時，也必須在新的 **總帳過帳群組** 頁面上設定 **應收銷售稅** 欄位。 會計引擎將會將此欄位中的資訊用於稅務相關的會計分錄。   
不論過帳的費用明細是否與專案有關，其行為都是一致的。  
