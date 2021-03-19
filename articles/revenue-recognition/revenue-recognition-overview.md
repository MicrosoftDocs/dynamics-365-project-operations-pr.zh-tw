---
title: 收入認列概觀
description: 本主題提供 Project Operations 中收入認列的資訊。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278858"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="87ba0-103">收入認列概觀</span><span class="sxs-lookup"><span data-stu-id="87ba0-103">Revenue recognition overview</span></span>

<span data-ttu-id="87ba0-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="87ba0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="87ba0-105">在 Dynamics 365 Project Operations 中，收入認列原則會根據專案或專案的一部分所選取的帳務方式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="87ba0-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="87ba0-106">本主題提供 Project Operations 中收入認列的資訊。</span><span class="sxs-lookup"><span data-stu-id="87ba0-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="87ba0-107">使用時間和資料帳務方式記帳的交易</span><span class="sxs-lookup"><span data-stu-id="87ba0-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="87ba0-108">成本和收入認列是關聯的。</span><span class="sxs-lookup"><span data-stu-id="87ba0-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="87ba0-109">交易成本與未開單銷售使用 [Project Operations 整合帳目](../project-accounting/project-operations-integration-journal.md)過帳。</span><span class="sxs-lookup"><span data-stu-id="87ba0-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="87ba0-110">專案成本和營收設定檔判斷未開單銷售交易記錄是否已過帳至總帳。</span><span class="sxs-lookup"><span data-stu-id="87ba0-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="87ba0-111">如果已選取 **應計營收**，系統會在過帳期間使用 **WIP 銷售值** 和 **應計收入銷售值** 科目。</span><span class="sxs-lookup"><span data-stu-id="87ba0-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="87ba0-112">以下是此方法的範例。</span><span class="sxs-lookup"><span data-stu-id="87ba0-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="87ba0-113">交易類型</span><span class="sxs-lookup"><span data-stu-id="87ba0-113">Transaction type</span></span> | <span data-ttu-id="87ba0-114">轉帳卡/信用卡</span><span class="sxs-lookup"><span data-stu-id="87ba0-114">Debit/Credit</span></span> | <span data-ttu-id="87ba0-115">總數</span><span class="sxs-lookup"><span data-stu-id="87ba0-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="87ba0-116">WIP 銷售值</span><span class="sxs-lookup"><span data-stu-id="87ba0-116">WIP Sales value</span></span> | <span data-ttu-id="87ba0-117">轉帳卡</span><span class="sxs-lookup"><span data-stu-id="87ba0-117">Debit</span></span> | <span data-ttu-id="87ba0-118">100</span><span class="sxs-lookup"><span data-stu-id="87ba0-118">100</span></span> |
  | <span data-ttu-id="87ba0-119">應計收入銷售值</span><span class="sxs-lookup"><span data-stu-id="87ba0-119">Accrued revenue sales value</span></span> | <span data-ttu-id="87ba0-120">信用卡</span><span class="sxs-lookup"><span data-stu-id="87ba0-120">Credit</span></span> | <span data-ttu-id="87ba0-121">100</span><span class="sxs-lookup"><span data-stu-id="87ba0-121">100</span></span> |

- <span data-ttu-id="87ba0-122">開立發票時認列收入。</span><span class="sxs-lookup"><span data-stu-id="87ba0-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="87ba0-123">在過帳期間，系統使用 **已開立發票營收** 科目。</span><span class="sxs-lookup"><span data-stu-id="87ba0-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="87ba0-124">以下是此方法的範例。</span><span class="sxs-lookup"><span data-stu-id="87ba0-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="87ba0-125">交易類型</span><span class="sxs-lookup"><span data-stu-id="87ba0-125">Transaction type</span></span> | <span data-ttu-id="87ba0-126">轉帳卡/信用卡</span><span class="sxs-lookup"><span data-stu-id="87ba0-126">Debit/Credit</span></span> | <span data-ttu-id="87ba0-127">總數</span><span class="sxs-lookup"><span data-stu-id="87ba0-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="87ba0-128">客戶餘額</span><span class="sxs-lookup"><span data-stu-id="87ba0-128">Customer balance</span></span> | <span data-ttu-id="87ba0-129">轉帳卡</span><span class="sxs-lookup"><span data-stu-id="87ba0-129">Debit</span></span> | <span data-ttu-id="87ba0-130">120</span><span class="sxs-lookup"><span data-stu-id="87ba0-130">120</span></span> |
  | <span data-ttu-id="87ba0-131">應付銷售稅</span><span class="sxs-lookup"><span data-stu-id="87ba0-131">Sales tax payable</span></span> | <span data-ttu-id="87ba0-132">信用卡</span><span class="sxs-lookup"><span data-stu-id="87ba0-132">Credit</span></span> | <span data-ttu-id="87ba0-133">20</span><span class="sxs-lookup"><span data-stu-id="87ba0-133">20</span></span> |
  | <span data-ttu-id="87ba0-134">已開發票營收</span><span class="sxs-lookup"><span data-stu-id="87ba0-134">Invoiced Revenue</span></span> | <span data-ttu-id="87ba0-135">信用卡</span><span class="sxs-lookup"><span data-stu-id="87ba0-135">Credit</span></span> | <span data-ttu-id="87ba0-136">100</span><span class="sxs-lookup"><span data-stu-id="87ba0-136">100</span></span> |

- <span data-ttu-id="87ba0-137">如果在過帳未開單銷售時營收已累計，系統將在開立發票時沖銷應計收入。</span><span class="sxs-lookup"><span data-stu-id="87ba0-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="87ba0-138">交易類型</span><span class="sxs-lookup"><span data-stu-id="87ba0-138">Transaction type</span></span> | <span data-ttu-id="87ba0-139">轉帳卡/信用卡</span><span class="sxs-lookup"><span data-stu-id="87ba0-139">Debit/Credit</span></span> | <span data-ttu-id="87ba0-140">總數</span><span class="sxs-lookup"><span data-stu-id="87ba0-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="87ba0-141">WIP 銷售值</span><span class="sxs-lookup"><span data-stu-id="87ba0-141">WIP Sales value</span></span> | <span data-ttu-id="87ba0-142">信用卡</span><span class="sxs-lookup"><span data-stu-id="87ba0-142">Credit</span></span> | <span data-ttu-id="87ba0-143">100</span><span class="sxs-lookup"><span data-stu-id="87ba0-143">100</span></span> |
  | <span data-ttu-id="87ba0-144">應計收入銷售值</span><span class="sxs-lookup"><span data-stu-id="87ba0-144">Accrued revenue sales value</span></span> | <span data-ttu-id="87ba0-145">轉帳卡</span><span class="sxs-lookup"><span data-stu-id="87ba0-145">Debit</span></span> | <span data-ttu-id="87ba0-146">100</span><span class="sxs-lookup"><span data-stu-id="87ba0-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="87ba0-147">使用固定價格帳務方式記帳的交易</span><span class="sxs-lookup"><span data-stu-id="87ba0-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="87ba0-148">成本和收入認列是分開的。</span><span class="sxs-lookup"><span data-stu-id="87ba0-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="87ba0-149">交易成本使用 [Project Operations 整合帳目](../project-accounting/project-operations-integration-journal.md)過帳。</span><span class="sxs-lookup"><span data-stu-id="87ba0-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="87ba0-150">不會建立未開單銷售交易。</span><span class="sxs-lookup"><span data-stu-id="87ba0-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="87ba0-151">如果專案成本和收入設定檔將 **用於專案完成計算的原則** 設定為 **無 WIP**，則可在開立發票時認列收入。</span><span class="sxs-lookup"><span data-stu-id="87ba0-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="87ba0-152">只將此方法用於短期、簡單專案。</span><span class="sxs-lookup"><span data-stu-id="87ba0-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="87ba0-153">可以使用固定價格營收預估值來認列收入（使用 **全部完工法** 或 **完成百分比營收認列** 方法）。</span><span class="sxs-lookup"><span data-stu-id="87ba0-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87ba0-154">其他資源</span><span class="sxs-lookup"><span data-stu-id="87ba0-154">Additional resources</span></span>
[<span data-ttu-id="87ba0-155">設定計費專案會計文章</span><span class="sxs-lookup"><span data-stu-id="87ba0-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="87ba0-156">固定價格營收估計專案</span><span class="sxs-lookup"><span data-stu-id="87ba0-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="87ba0-157">管理營收預估值</span><span class="sxs-lookup"><span data-stu-id="87ba0-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="87ba0-158">完工成本法</span><span class="sxs-lookup"><span data-stu-id="87ba0-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]