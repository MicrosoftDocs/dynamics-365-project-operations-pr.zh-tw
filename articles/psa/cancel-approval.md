---
title: 取消先前核准的時間和費用項目
description: 本主題提供有關如何取消已核准專案時間或費用交易的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150568"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>取消先前核准的時間或費用項目

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

在最新版本的 Dynamics 365 Project Service Automation 中，核准者可以取消他們先前核准的時間或費用項目。

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>取消先前核准的時間或費用項目

依照下列步驟，取消先前已核准的時間或費用項目。

1. 移至 **專案** \> **我的工作** \> **核准**。
2. 在 **核准** 清單頁面上，將檢視表變更到 **我過去的核准**。 隨即顯示您先前已核准的時間和費用項目清單。
3. 選取一個或多個項目，然後選擇 **取消核准**。 您會收到警告訊息。
4. 選取 **確定** 以取消核准。

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>了解取消時間或費用項目核准的影響

取消核准時，會產生營運影響和財務影響。

### <a name="operational-impact"></a>營運影響

在營運面，取消核准時，會將該記錄的狀態重設為 **草稿**，而且該核准已不再出現於 **我過去的核准** 檢視表中。 相反地，取消的核准會出現在 **供核准的時間項目** 檢視表或 **供核准的費用項目** 檢視表中，視其為時間項目還是費用項目而定。 此外，相關時間或費用項目的狀態會變更為 **已送出**，使相關項目與狀態為 **草稿** 的核准一致。

身為核准者，您可以編輯狀態為 **草稿** 之核准的部分欄位。 這些欄位包括 **帳單類型** 和 **時間項目計費時數**。 進行變更之後，您可以重新核准該記錄。 或者，也可以拒絕該項目。 如果您拒絕核准時間項目，該項目的狀態會變更為 **已退回**。 如果您拒絕核准費用項目，狀態會變更為 **已拒絕**。 在功能上，已退回和已拒絕項目的行為與狀態為 **草稿** 的項目相同。 專案團隊成員可以對項目進行任何必要的變更，然後重新送出供核准，或是完全刪除。

### <a name="financial-impact"></a>財務影響

取消核准時，專案也會在財務上受到影響。 首先，成本和銷售的對應實際值會以下列方式更新：

- 調整狀態會設定為 **已調整**。
- 帳單狀態設定為 **已取消**。

接下來，在 [實際值] 表格中建立沖回分錄。 為了建立沖回分錄，系統複製原始實際值中的欄位值。 唯一未複製的值是數量值。 這些值反而是進行沖回。 **成本** 與 **未開單銷售** 實際值都會建立已沖回的實際值。 已沖回實際值的 **調整狀態** 欄位會設定為 **不可調整**，且帳單狀態欄位會設定為 **已取消**。

進行這些變更之後，專案上記錄為支出的金額以及專案的營收待辦項目將不會再有這些實際值所占的金額。


[!INCLUDE[footer-include](../includes/footer-banner.md)]