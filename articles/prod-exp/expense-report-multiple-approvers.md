---
title: 費用報表上的多個核准者
description: 本主題提供有關需要多人核准之費用報表的資訊。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073152"
---
# <a name="multiple-approvers-on-an-expense-report"></a>費用報表上的多個核准者

[!include [banner](../includes/banner.md)]

根據您組織的費用核准原則，可能需要多人來核准員工所提交的費用報表。 設定費用報表核准工作流程程序時，您可以新增包含一個或多個費用報表核准者之工作或步驟的工作流程元素。 例如，您可能需要所有的費用報表先由提交報表之員工的經理核准，然後再由應付帳款協調員來核准。

如果您認為需要多名費用報表核准者，則可以透過下列任何方式新增工作流程元素：

- 新增一個含有一個步驟的核准元素。 例如，步驟可能需要將費用報表指派給使用者群組，並由使用者群組 50% 的成員進行核准。
- 新增一個含有多個步驟的核准元素。 例如，核准元素可能會有下列步驟：

    1. 提交費用報表之員工的經理會核准該報表。
    2. 應付帳款職員會驗證收據和費用報表項目。
    3. 預算負責人會核准費用報表。

- 新增多個核准元素，其中每個都有一個步驟。 例如，您可能會為下列每一個步驟新增不同的核准元素：

    1. 員工的經理會核准費用報表。
    2. 預算負責人會核准費用報表。
