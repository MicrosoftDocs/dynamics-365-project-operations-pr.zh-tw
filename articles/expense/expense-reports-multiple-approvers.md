---
title: 費用報表和多個核准者
description: 本主題提供有關需要多人核准之費用報表的資訊。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120983"
---
# <a name="expense-reports-and-multiple-approvers"></a>費用報表和多個核准者

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

根據您組織的費用核准原則，可能需要多人來核准已提交的費用報表。 設定費用報表核准工作流程程序時，您可以新增包含一個或多個費用報表核准者之工作或步驟的工作流程元素。 例如，您可能需要由兩名不同的人員 (提交報表之員工經理以及應付帳款協調員) 來核准所有費用報表。

如果您認為需要多名費用報表核准者，則可以透過下列任何方式新增工作流程元素：

- 新增一個含有一個步驟的核准元素。 例如，步驟可能需要將費用報表指派給使用者群組，並由使用者群組 50% 的成員進行核准。
- 新增一個含有多個步驟的核准元素。 例如，核准元素可能會有下列步驟：

    1. 提交費用報表之員工的經理會核准該報表。
    2. 應付帳款職員會驗證收據和費用報表項目。
    3. 預算負責人會核准費用報表。

- 新增多個核准元素，其中每個都有一個步驟。 例如，您可能會為下列每一個步驟新增不同的核准元素：

    1. 員工的經理會核准費用報表。
    2. 預算負責人會核准費用報表。


[!INCLUDE[footer-include](../includes/footer-banner.md)]