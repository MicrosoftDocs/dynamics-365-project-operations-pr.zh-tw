---
title: 費用管理工作流程
description: 本主題說明如何使用 Microsoft Dynamics 365 Finance 中的工作流程系統，以設定費用管理中的費用報表審查程序。
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073151"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="48b15-103">費用管理工作流程</span><span class="sxs-lookup"><span data-stu-id="48b15-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48b15-104">您可以使用工作流程系統來設定費用管理中的費用報表審查程序。</span><span class="sxs-lookup"><span data-stu-id="48b15-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="48b15-105">您可以設定使用下列準則的工作流程，以判斷費用報表的核准者：</span><span class="sxs-lookup"><span data-stu-id="48b15-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="48b15-106">員工報告階層以及預先定義的核准限制</span><span class="sxs-lookup"><span data-stu-id="48b15-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="48b15-107">支援暫時核准者及最終核准者的多層核准</span><span class="sxs-lookup"><span data-stu-id="48b15-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="48b15-108">財務維度與專案責任</span><span class="sxs-lookup"><span data-stu-id="48b15-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="48b15-109">指派給特定使用者或使用者群組</span><span class="sxs-lookup"><span data-stu-id="48b15-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="48b15-110">您可以建立費用報表、差旅申請、預付現金和加值稅 (VAT) 退還的工作流程核准。</span><span class="sxs-lookup"><span data-stu-id="48b15-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="48b15-111">**範例**</span><span class="sxs-lookup"><span data-stu-id="48b15-111">**Example**</span></span>

<span data-ttu-id="48b15-112">下列程序是費用報表的費用管理工作流程範例。</span><span class="sxs-lookup"><span data-stu-id="48b15-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="48b15-113">員工建立並儲存費用報表。</span><span class="sxs-lookup"><span data-stu-id="48b15-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="48b15-114">員工提交費用報表以供核准。</span><span class="sxs-lookup"><span data-stu-id="48b15-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="48b15-115">根據設定工作流程時所定義的規則來識別核准者。</span><span class="sxs-lookup"><span data-stu-id="48b15-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="48b15-116">核准者收到費用報表已準備好進行核准的通知。</span><span class="sxs-lookup"><span data-stu-id="48b15-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="48b15-117">核准者審查費用報表，並確認是否符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="48b15-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="48b15-118">費用未違反任何費用原則。</span><span class="sxs-lookup"><span data-stu-id="48b15-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="48b15-119">如果費用違反原則，則核准者會確認費用報表包含有效的業務理由。</span><span class="sxs-lookup"><span data-stu-id="48b15-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="48b15-120">將電子收據附加至費用報表。</span><span class="sxs-lookup"><span data-stu-id="48b15-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="48b15-121">核准者核准費用報表。</span><span class="sxs-lookup"><span data-stu-id="48b15-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="48b15-122">將費用報表指派給應付帳款會計專員以進行過帳。</span><span class="sxs-lookup"><span data-stu-id="48b15-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="48b15-123">根據是否已設定自動過帳，進行下列其中一個步驟：</span><span class="sxs-lookup"><span data-stu-id="48b15-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="48b15-124">如果已設定自動過帳，則處理費用報表以進行付款，並更新費用報表的狀態。</span><span class="sxs-lookup"><span data-stu-id="48b15-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="48b15-125">如果未設定自動過帳，則應付帳款會計專員會確認是否所有的原始收據都已提交，以及收據是否與費用報表中的費用相符。</span><span class="sxs-lookup"><span data-stu-id="48b15-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="48b15-126">所有在費用報表上輸入的稅碼也都必須確認為正確。</span><span class="sxs-lookup"><span data-stu-id="48b15-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="48b15-127">確認過這些這些需求之後，將費用報表過帳。</span><span class="sxs-lookup"><span data-stu-id="48b15-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="48b15-128">將費用報表過帳之後，費用報表的付款便會獲得授權，並撥款給員工。</span><span class="sxs-lookup"><span data-stu-id="48b15-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
