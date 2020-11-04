---
title: 定義費用原則
description: 您可以定義您的工作者在輸入和提交費用報表和差旅申請時必須遵循的費用原則。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 30b3a0e1547ca7043b1433da2b4ebf02f2b473a1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073066"
---
# <a name="define-expense-policies"></a><span data-ttu-id="278de-103">定義費用原則</span><span class="sxs-lookup"><span data-stu-id="278de-103">Define expense policies</span></span>

<span data-ttu-id="278de-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="278de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="278de-105">您可以定義您的工作者在輸入和提交費用報表和差旅申請時必須遵循的原則。</span><span class="sxs-lookup"><span data-stu-id="278de-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="278de-106">實行費用原則可以協助您有效管理費用。</span><span class="sxs-lookup"><span data-stu-id="278de-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="278de-107">例如，您可以設定紐約市住宿費用的原則，規定每夜費用不能超過美元 250。</span><span class="sxs-lookup"><span data-stu-id="278de-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="278de-108">如果工作者提交住房費超過此金額的費用報表或差旅申請，系統就會通知</span><span class="sxs-lookup"><span data-stu-id="278de-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="278de-109">工作者已超過費用原則的金額。</span><span class="sxs-lookup"><span data-stu-id="278de-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="278de-110">您可以在定義原則時設定工作者會收到的訊息</span><span class="sxs-lookup"><span data-stu-id="278de-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="278de-111">。</span><span class="sxs-lookup"><span data-stu-id="278de-111">define the policy.</span></span>      
        
<span data-ttu-id="278de-112">您可以定義三種類型的原則：</span><span class="sxs-lookup"><span data-stu-id="278de-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="278de-113">**警告** ：允許工作者提交費用報表或差旅申請，但會標示費用給所有核准者處理並</span><span class="sxs-lookup"><span data-stu-id="278de-113">**Warning** : Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="278de-114">供稍後提報。</span><span class="sxs-lookup"><span data-stu-id="278de-114">for later reporting.</span></span>        

- <span data-ttu-id="278de-115">**錯誤** ：要求工作者必須先將費用修訂成符合原則，才能提交費用報表或差旅申請。</span><span class="sxs-lookup"><span data-stu-id="278de-115">**Error** : Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="278de-116">**正當理由** ：要求工作者或經理必須先輸入超出原則金額的正當理由，才能提交費用報表或差旅申請。</span><span class="sxs-lookup"><span data-stu-id="278de-116">**Justification** : Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="278de-117">原則提示</span><span class="sxs-lookup"><span data-stu-id="278de-117">Policy tips</span></span>
<span data-ttu-id="278de-118">以下是一些可在建立費用管理新原則時協助您的建議：</span><span class="sxs-lookup"><span data-stu-id="278de-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="278de-119">原則有生效日期，這表示如果原則的建立日期是在費用發生日期之後，則原則無法生效。</span><span class="sxs-lookup"><span data-stu-id="278de-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="278de-120">例如，您今天建立新原則以強制 $50 的餐費上限。</span><span class="sxs-lookup"><span data-stu-id="278de-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="278de-121">任何截至昨天的現有費用都不會根據此原則進行檢查。</span><span class="sxs-lookup"><span data-stu-id="278de-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="278de-122">針對可逐條列舉的費用類別建立原則時，請考慮新增費用明細類型的條件。</span><span class="sxs-lookup"><span data-stu-id="278de-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="278de-123">有些原則 (例如，要求附上收據) 可能對逐條列舉的明細沒有意義。</span><span class="sxs-lookup"><span data-stu-id="278de-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="278de-124">在這種情況下，只會將原則套用至標題列或非逐條列舉的明細。</span><span class="sxs-lookup"><span data-stu-id="278de-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="278de-125">預設會依據來源實體評估費用管理原則。</span><span class="sxs-lookup"><span data-stu-id="278de-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="278de-126">在公司間交易案例中，您可以將原則設定為改依目的地實體 (借用實體) 進行評估。</span><span class="sxs-lookup"><span data-stu-id="278de-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="278de-127">若要依據目的地實體執行原則，請開啟 **功能管理** 工作區中的 **依據借用法律實體評估費用原則** 功能。</span><span class="sxs-lookup"><span data-stu-id="278de-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="278de-128">評估原則的時機</span><span class="sxs-lookup"><span data-stu-id="278de-128">When to evaluate policies</span></span>

<span data-ttu-id="278de-129">在費用管理參數中，您可以選擇在儲存明細時或在提交費用報表時評估費用管理原則。</span><span class="sxs-lookup"><span data-stu-id="278de-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="278de-130">如果您選擇在儲存明細時進行評估，則使用者可以較早了解一次全部完成其費用報表所需執行的工作。</span><span class="sxs-lookup"><span data-stu-id="278de-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="278de-131">否則您可以在提交至工作流程的過程中，將原則評估延遲，並透過在結束時驗證的方式節省時間。</span><span class="sxs-lookup"><span data-stu-id="278de-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
