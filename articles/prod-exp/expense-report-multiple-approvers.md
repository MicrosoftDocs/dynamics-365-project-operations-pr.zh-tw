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
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271703"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="62de3-103">費用報表上的多個核准者</span><span class="sxs-lookup"><span data-stu-id="62de3-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="62de3-104">根據您組織的費用核准原則，可能需要多人來核准員工所提交的費用報表。</span><span class="sxs-lookup"><span data-stu-id="62de3-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="62de3-105">設定費用報表核准工作流程程序時，您可以新增包含一個或多個費用報表核准者之工作或步驟的工作流程元素。</span><span class="sxs-lookup"><span data-stu-id="62de3-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="62de3-106">例如，您可能需要所有的費用報表先由提交報表之員工的經理核准，然後再由應付帳款協調員來核准。</span><span class="sxs-lookup"><span data-stu-id="62de3-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="62de3-107">如果您認為需要多名費用報表核准者，則可以透過下列任何方式新增工作流程元素：</span><span class="sxs-lookup"><span data-stu-id="62de3-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="62de3-108">新增一個含有一個步驟的核准元素。</span><span class="sxs-lookup"><span data-stu-id="62de3-108">Add one approval element that has one step.</span></span> <span data-ttu-id="62de3-109">例如，步驟可能需要將費用報表指派給使用者群組，並由使用者群組 50% 的成員進行核准。</span><span class="sxs-lookup"><span data-stu-id="62de3-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="62de3-110">新增一個含有多個步驟的核准元素。</span><span class="sxs-lookup"><span data-stu-id="62de3-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="62de3-111">例如，核准元素可能會有下列步驟：</span><span class="sxs-lookup"><span data-stu-id="62de3-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="62de3-112">提交費用報表之員工的經理會核准該報表。</span><span class="sxs-lookup"><span data-stu-id="62de3-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="62de3-113">應付帳款職員會驗證收據和費用報表項目。</span><span class="sxs-lookup"><span data-stu-id="62de3-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="62de3-114">預算負責人會核准費用報表。</span><span class="sxs-lookup"><span data-stu-id="62de3-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="62de3-115">新增多個核准元素，其中每個都有一個步驟。</span><span class="sxs-lookup"><span data-stu-id="62de3-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="62de3-116">例如，您可能會為下列每一個步驟新增不同的核准元素：</span><span class="sxs-lookup"><span data-stu-id="62de3-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="62de3-117">員工的經理會核准費用報表。</span><span class="sxs-lookup"><span data-stu-id="62de3-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="62de3-118">預算負責人會核准費用報表。</span><span class="sxs-lookup"><span data-stu-id="62de3-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]