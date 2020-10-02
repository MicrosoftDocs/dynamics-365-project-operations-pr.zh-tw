---
title: 已更正的發票
description: 本主題提供有關已更正發票的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898071"
---
# <a name="corrected-invoices"></a><span data-ttu-id="277e0-103">已更正的發票</span><span class="sxs-lookup"><span data-stu-id="277e0-103">Corrected invoices</span></span>

<span data-ttu-id="277e0-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="277e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="277e0-105">您可以編輯已確認的發票。</span><span class="sxs-lookup"><span data-stu-id="277e0-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="277e0-106">編輯已確認的發票時，會建立已更正發票的草稿。</span><span class="sxs-lookup"><span data-stu-id="277e0-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="277e0-107">因為假設您要從原始發票中沖回所有交易和數量，已更正的發票會包含原始發票中所有的交易，而其中所有的數量皆為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="277e0-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="277e0-108">交易不需要更正時，您可以從草稿更正發票移除這些交易。</span><span class="sxs-lookup"><span data-stu-id="277e0-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="277e0-109">若只是要沖回或回復部分數量，則可以編輯明細詳細資料上的 [數量] 欄位。</span><span class="sxs-lookup"><span data-stu-id="277e0-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="277e0-110">如果開啟發票明細詳細資料，您可以查看原始發票數量。</span><span class="sxs-lookup"><span data-stu-id="277e0-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="277e0-111">然後就可以編輯目前發票數量，使其小於或等於原始發票數量。</span><span class="sxs-lookup"><span data-stu-id="277e0-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="277e0-112">確認更正發票時，會沖回原始已開單銷售實際值，並建立新的已開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="277e0-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="277e0-113">如果數量已減少，則差額也會導致建立新的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="277e0-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="277e0-114">例如，如果原始已開單銷售是八小時，且已更正的發票明細詳細資料的數量已減少為六小時，則會沖回原始已開單銷售明細，並建立兩個新的實際值：</span><span class="sxs-lookup"><span data-stu-id="277e0-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="277e0-115">六小時的已開單銷售實際。</span><span class="sxs-lookup"><span data-stu-id="277e0-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="277e0-116">剩餘兩個小時的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="277e0-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="277e0-117">依據與客戶的協商，此交易可以稍後再開帳單，或標示為不應收費。</span><span class="sxs-lookup"><span data-stu-id="277e0-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
