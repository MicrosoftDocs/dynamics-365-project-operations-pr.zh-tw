---
title: 處理費用報表上的個人費用
description: 本主題提供相關資訊，說明如何處理員工在出差時因業務目的所產生的個人費用。
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025674"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>處理費用報表上的個人費用

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

在商務差旅期間，員工可能會以公司信用卡來支付其個人費用。 如果尚未定義用來處理個人費用的程序，則員工提交其分項明列的費用報表時，可能會中斷費用報表核准程序。

有兩種方法可以用來處理員工的個人費用：

  - **由員工支付**：您的組織不支付出現在公司信用卡帳單的個人費用。 反而是員工將費用款項直接支付給信用卡供應商。 
  - **由公司支付**：您的組織支付公司信用卡的全額帳單，然後借記工作者的個人費用會計科目。

您可以在 **費用管理參數** 頁面上選取您的組織所使用的方法。


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>當個人金額欄位有已定義的值時，啟用分割費用功能

**當個人金額欄位的值已定義時，啟用分攤費用功能** 這項功能只會套用至使用 明細層級工作流程所核准的費用報表。 核准報表的方式是，移至 **處理費用報表** > **指派給我的費用報表** > **開啟費用報表**。 

若要啟用此功能，請移至 **工作區** > **功能管理**、選取 **當個人金額欄位有已定義的值時，啟用分割費用功能**，然後選取 **立即啟用**。 

啟用此功能時，使用此功能的費用明細會在提交報表時產生兩個明細。 產生兩個明細，讓核准者可以個別核准每個明細。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
