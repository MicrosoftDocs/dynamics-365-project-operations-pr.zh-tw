---
title: 設定費用管理工作流程
description: 您可以設定工作流程程序來審查和核准差旅及費用單據。
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
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073150"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="86e2c-103">設定費用管理工作流程</span><span class="sxs-lookup"><span data-stu-id="86e2c-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86e2c-104">您可以設定用來審查和核准差旅及費用單據的工作流程程序。</span><span class="sxs-lookup"><span data-stu-id="86e2c-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="86e2c-105">可為其定義工作流程的單據包括費用報表、差旅申請及預付現金要求。</span><span class="sxs-lookup"><span data-stu-id="86e2c-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="86e2c-106">工作流程代表商務程序。</span><span class="sxs-lookup"><span data-stu-id="86e2c-106">A workflow represents a business process.</span></span> <span data-ttu-id="86e2c-107">此程序定義單據在系統中流動的方式，並指出必須完成工作或核准單據的人員。</span><span class="sxs-lookup"><span data-stu-id="86e2c-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="86e2c-108">在組織中使用工作流程系統會有幾個好處：</span><span class="sxs-lookup"><span data-stu-id="86e2c-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="86e2c-109">**一致的程序** — 您可以定義特定單據 (例如採購申請和費用報表) 的審查程序。</span><span class="sxs-lookup"><span data-stu-id="86e2c-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="86e2c-110">使用工作流程系統有助於確保單據是依照一致且有效率的方式進行處理和核准。</span><span class="sxs-lookup"><span data-stu-id="86e2c-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="86e2c-111">程序可見度 — 您可以追蹤特定工作流程執行個體的狀態、歷程記錄和效能計量。</span><span class="sxs-lookup"><span data-stu-id="86e2c-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="86e2c-112">這可協助您判斷工作流程是否應進行變更以改善效率。</span><span class="sxs-lookup"><span data-stu-id="86e2c-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="86e2c-113">集中式工作清單 — 使用者可以查看集中式工作清單來檢視指派給他們的工作流程工作與核准。</span><span class="sxs-lookup"><span data-stu-id="86e2c-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="86e2c-114">**您可以建立的工作流程類型**</span><span class="sxs-lookup"><span data-stu-id="86e2c-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="86e2c-115">下表列出您可在 **費用** 中建立的工作流程類型。</span><span class="sxs-lookup"><span data-stu-id="86e2c-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="86e2c-116"><strong>輸入</strong></span><span class="sxs-lookup"><span data-stu-id="86e2c-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="86e2c-117"><strong>使用此類型，可以</strong></span><span class="sxs-lookup"><span data-stu-id="86e2c-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="86e2c-118"><strong>費用報表</strong></span><span class="sxs-lookup"><span data-stu-id="86e2c-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="86e2c-119">建立費用報表的核准工作流程。</span><span class="sxs-lookup"><span data-stu-id="86e2c-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="86e2c-120"><strong>費用報表自動過帳</strong></span><span class="sxs-lookup"><span data-stu-id="86e2c-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="86e2c-121">建立費用報表的自動過帳工作流程。</span><span class="sxs-lookup"><span data-stu-id="86e2c-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="86e2c-122"><strong>費用明細項目</strong></span><span class="sxs-lookup"><span data-stu-id="86e2c-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="86e2c-123">建立費用報表明細項目的核准工作流程。</span><span class="sxs-lookup"><span data-stu-id="86e2c-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="86e2c-124"><strong>費用明細項目自動過帳</strong></span><span class="sxs-lookup"><span data-stu-id="86e2c-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="86e2c-125">建立費用報表明細項目的自動過帳工作流程。</span><span class="sxs-lookup"><span data-stu-id="86e2c-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="86e2c-126"><strong>差旅申請</strong></span><span class="sxs-lookup"><span data-stu-id="86e2c-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="86e2c-127">建立差旅申請的核准工作流程。</span><span class="sxs-lookup"><span data-stu-id="86e2c-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="86e2c-128"><strong>預付現金要求</strong></span><span class="sxs-lookup"><span data-stu-id="86e2c-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="86e2c-129">建立預付現金要求的核准工作流程。</span><span class="sxs-lookup"><span data-stu-id="86e2c-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="86e2c-130"><strong>加值稅退還</strong></span><span class="sxs-lookup"><span data-stu-id="86e2c-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="86e2c-131">建立退還加值稅 (VAT) 的核准工作流程。</span><span class="sxs-lookup"><span data-stu-id="86e2c-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

