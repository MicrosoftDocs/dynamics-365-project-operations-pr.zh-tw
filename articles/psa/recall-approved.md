---
title: 回收核准的時間或費用項目
description: 本主題提供有關如何回收先前核准的時間或費用交易的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147823"
---
# <a name="recall-approved-time-or-expense-entries"></a>回收核准的時間或費用項目

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

專案團隊成員或其他提交時間或費用項目的人員，可在其獲得核准後回收該項目。 回收已核准時間或費用項目的程序有兩個步驟：

1. 提交者要求回收。
2. 核准者核准回收。

## <a name="request-a-recall"></a>要求回收

依照下列步驟，要求回收已核准的時間或費用項目。

1. 若為時間項目，移至 **專案** \> **我的工作** \> **時間項目**。

    -或-

    若為費用項目，移至 **專案** \> **我的工作** \> **費用**。

2. 針對時間項目，選取專案與工作特定組合的所有時間項目。 或者在網格中，選取特定專案特定日期的個別時間儲存格。

    -或-

    針對費用項目，選取要回收的費用項目。

3. 選取 **回收**。 確認對話方塊隨即出現。 如果選取的時間或費用項目已獲核准，系統會提示您輸入回收原因。
4. 輸入回收的原因，然後選取 **確定** 以確認操作。 系統會傳送要求給核准項目的人員以請求核准回收。

> [!NOTE]
> 雖然可以回收已核准的時間和費用項目，但若已核准的時間或費用項目已開發票給客戶，就無法建立回收要求。 嘗試建立回收要求的使用者將會收到訊息，指出該時間或費用項目因為已開發票而無法撤回。

## <a name="approve-or-reject-a-recall-request"></a>核准或拒絕回收要求

請依照下列步驟核准或拒絕回收要求。

1. 移至 **專案** \> **我的工作** \> **核准**。
2. 在 **核准** 清單頁面上，將檢視表變更到 **回收核准要求**。 隨即顯示已送出的回收要求清單。
3. 選取一個或多個項目，然後選取 **核准** 或 **拒絕**。
4. 如果選取了 **核准**，您會收到警告訊息，解釋核准的影響。 選取 **確定** 以確認操作。 回收要求已核准。

    -或-

    如果選取 **拒絕**，則會拒絕回收要求。

> [!NOTE]
> 要求回收時、回收獲核准時，系統會檢查時間或費用項目是否有任何開立發票活動。 如果項目已開具發票，或已記入草稿發票，則該核准者將收到錯誤訊息，指出因為已開發票而無法核准回收該時間或費用。

## <a name="impact-of-a-recall-request"></a>回收要求的影響

回收核准時，會產生營運影響和財務影響。

### <a name="operational-impact"></a>營運影響

如果回收要求獲核准，則會將核准記錄標示為 **已拒絕**。 項目的狀態會變更為 **已退回** 或 **已拒絕**，取決於它是時間項目還是費用項目。

專案團隊成員可以檢視項目、編輯項目，然後重新將其送出或整個刪除。

如果回收要求遭拒絕，該項目的狀態會保持 **已核准**，且專案團隊成員或專案核准者無法加以編輯。

### <a name="financial-impact"></a>財務影響

如果回收要求獲核准，成本和銷售的對應實際值會以下列方式更新：

- **調整狀態** 欄位會更新為 **已調整**。
- **帳單狀態** 欄位會更新為 **已取消**。

接下來，在 [實際值] 表格中建立沖回分錄。 為了建立沖回分錄，系統複製原始實際值中的欄位值。 唯一未複製的值是數量值。 這些值反而是進行沖回。 **成本** 與 **未開單銷售** 實際值都會建立已沖回的實際值。 已沖回實際值的 **調整狀態** 欄位會設定為 **不可調整**，且 **帳單狀態** 欄位會設定為 **已取消**。 由於有這些變更，專案中的已記錄支出和營收積存將不會再有這些實際值所占的金額。

如果回收要求遭拒絕，就不會對專案造成任何財務影響。

## <a name="changes-to-time-entry-records"></a>對時間項目記錄的變更

下圖顯示已核准時間項目在其被回收時發生的變更

![時間項目狀態轉換](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>對費用項目記錄的變更

下圖顯示已核准費用項目在其被回收時發生的變更

![費用項目狀態轉換](media/ExpenseEntryStateTransitions.png)
