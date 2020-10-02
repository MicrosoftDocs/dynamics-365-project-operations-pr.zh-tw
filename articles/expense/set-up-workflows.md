---
title: 設定費用管理的工作流程
description: 您可以設定用來審查和核准差旅及費用單據的工作流程程序。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896541"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="3e276-103">設定費用管理的工作流程</span><span class="sxs-lookup"><span data-stu-id="3e276-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="3e276-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="3e276-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3e276-105">您可以設定工作流程程序來審查和核准差旅及費用單據。</span><span class="sxs-lookup"><span data-stu-id="3e276-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="3e276-106">您可以定義費用報表、差旅申請及預付現金要求的工作流程。</span><span class="sxs-lookup"><span data-stu-id="3e276-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="3e276-107">工作流程代表商務程序，並定義單據在系統中流動的方式。</span><span class="sxs-lookup"><span data-stu-id="3e276-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="3e276-108">工作流程也會指出必須完成工作或核准單據的人員。</span><span class="sxs-lookup"><span data-stu-id="3e276-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="3e276-109">在組織中使用工作流程系統會有幾個好處：</span><span class="sxs-lookup"><span data-stu-id="3e276-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="3e276-110">**一致的程序**：您可以定義特定單據 (例如採購申請和費用報表) 的審查程序。</span><span class="sxs-lookup"><span data-stu-id="3e276-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="3e276-111">使用工作流程系統有助於確保單據是依照一致且有效率的方式進行處理和核准。</span><span class="sxs-lookup"><span data-stu-id="3e276-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="3e276-112">**程序可見度**：您可以追蹤特定工作流程執行個體的狀態、歷程記錄和效能計量。</span><span class="sxs-lookup"><span data-stu-id="3e276-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="3e276-113">這可協助您判斷工作流程是否應進行變更以改善效率。</span><span class="sxs-lookup"><span data-stu-id="3e276-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="3e276-114">**集中式工作清單**：使用者可以查看集中式工作清單來檢視指派給他們的工作流程工作與核准。</span><span class="sxs-lookup"><span data-stu-id="3e276-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="3e276-115">工作流程類型</span><span class="sxs-lookup"><span data-stu-id="3e276-115">Workflow types</span></span>

<span data-ttu-id="3e276-116">下表列出您可在**費用管理**中建立的工作流程類型。</span><span class="sxs-lookup"><span data-stu-id="3e276-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="3e276-117"><strong>類型</strong></span><span class="sxs-lookup"><span data-stu-id="3e276-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="3e276-118"><strong>使用此類型，可以</strong></span><span class="sxs-lookup"><span data-stu-id="3e276-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="3e276-119"><strong>費用報表自動核准</strong></span><span class="sxs-lookup"><span data-stu-id="3e276-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="3e276-120">建立費用報表的核准工作流程。</span><span class="sxs-lookup"><span data-stu-id="3e276-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="3e276-121"><strong>費用報表自動過帳</strong></span><span class="sxs-lookup"><span data-stu-id="3e276-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="3e276-122">建立費用報表的自動過帳工作流程。</span><span class="sxs-lookup"><span data-stu-id="3e276-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="3e276-123"><strong>費用明細項目</strong></span><span class="sxs-lookup"><span data-stu-id="3e276-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="3e276-124">建立費用報表明細項目的核准工作流程。</span><span class="sxs-lookup"><span data-stu-id="3e276-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="3e276-125"><strong>費用明細項目自動過帳</strong></span><span class="sxs-lookup"><span data-stu-id="3e276-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="3e276-126">建立費用報表明細項目的自動過帳工作流程。</span><span class="sxs-lookup"><span data-stu-id="3e276-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="3e276-127"><strong>差旅申請</strong></span><span class="sxs-lookup"><span data-stu-id="3e276-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="3e276-128">建立差旅申請的核准工作流程。</span><span class="sxs-lookup"><span data-stu-id="3e276-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="3e276-129"><strong>預付現金要求</strong></span><span class="sxs-lookup"><span data-stu-id="3e276-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="3e276-130">建立預付現金要求的核准工作流程。</span><span class="sxs-lookup"><span data-stu-id="3e276-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="3e276-131"><strong>加值稅退還</strong></span><span class="sxs-lookup"><span data-stu-id="3e276-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="3e276-132">建立退還加值稅 (VAT) 的核准工作流程。</span><span class="sxs-lookup"><span data-stu-id="3e276-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
