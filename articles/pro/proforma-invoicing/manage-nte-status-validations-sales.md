---
title: 管理不得超過狀態和驗證
description: 此主題提供有關在 Project Operations 中執行的不得超過限制檢查的資訊。
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129983"
---
# <a name="manage-not-to-exceed-status-and-validations"></a><span data-ttu-id="ee3b7-103">管理不得超過狀態和驗證</span><span class="sxs-lookup"><span data-stu-id="ee3b7-103">Manage not-to-exceed status and validations</span></span> 

<span data-ttu-id="ee3b7-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="ee3b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="not-to-exceed-on-approvals"></a><span data-ttu-id="ee3b7-105">核准時不得超過</span><span class="sxs-lookup"><span data-stu-id="ee3b7-105">Not-to-exceed on approvals</span></span>

<span data-ttu-id="ee3b7-106">提交時間或費用項目時，將建立核准記錄。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-106">When a time or expense entry is submitted, an approval record is created.</span></span> <span data-ttu-id="ee3b7-107">如果核准為應收費，並對應至時間和資料合約服務內容，則系統會在下列層級完成不得超過驗證檢查：</span><span class="sxs-lookup"><span data-stu-id="ee3b7-107">If the approval is chargeable and maps to a time and material contract line, the system completes a not-to-exceed validation check at the following levels:</span></span>

  - <span data-ttu-id="ee3b7-108">檢查為專案合約服務內容中的客戶設定的限制</span><span class="sxs-lookup"><span data-stu-id="ee3b7-108">Check against the limit set up for the customer on the project contract line</span></span>
  - <span data-ttu-id="ee3b7-109">檢查為合約服務內容設定的限制</span><span class="sxs-lookup"><span data-stu-id="ee3b7-109">Check against the limit set up on the contract line</span></span>
  - <span data-ttu-id="ee3b7-110">檢查為客戶設定的限制</span><span class="sxs-lookup"><span data-stu-id="ee3b7-110">Check against the limit set up for the customer</span></span>
  - <span data-ttu-id="ee3b7-111">檢查為合約設定的限制</span><span class="sxs-lookup"><span data-stu-id="ee3b7-111">Check against the limit set up on the contract</span></span>

<span data-ttu-id="ee3b7-112">每個層級的檢查都涉及在考慮到已記錄的帳務積存金額以及該層級迄今為止已開發票的金額後，確保此核准的銷售金額不違反該層級的不得超過限制。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-112">The checks at each level involve ensuring that the amount of sales value on this approval will not violate the not-to-exceed limit at that level after accounting for the amount of billing backlog already recorded, and the amount invoiced to date at that level.</span></span>

<span data-ttu-id="ee3b7-113">如果檢查通過，則核准將具有 **成功** 的驗證狀態。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-113">If the check passes, the approval is given a validation status of **Success**.</span></span>

<span data-ttu-id="ee3b7-114">如果檢查失敗，則核准將具有 **失敗** 的驗證狀態。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-114">If the check fails, the approval is given a validation status of **Failed**.</span></span> <span data-ttu-id="ee3b7-115">不得超過驗證詳細資料將通知使用者驗證失敗的層級。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-115">The not-to-exceed validation detail will inform the user at which level the validation failed.</span></span>

<span data-ttu-id="ee3b7-116">當提交的時間或費用項目被視為不應收費時，不得超過驗證狀態設定為 **不適用**，驗證詳細資料等於 **不適用**。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-116">When the submitted time or expense entry is considered non-chargeable, the not-to-exceed validation status is set to **Not Applicable** with the validation detail equal to **Not applicable**.</span></span>

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a><span data-ttu-id="ee3b7-117">未開單銷售實際值不得超過</span><span class="sxs-lookup"><span data-stu-id="ee3b7-117">Not-to-exceed on unbilled sales actuals</span></span>

<span data-ttu-id="ee3b7-118">核准時間或費用項目時，將建立成本和未開單銷售實際值記錄。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-118">When a time or expense entry is approved, cost and unbilled sales actuals records are created.</span></span> <span data-ttu-id="ee3b7-119">如果要建立的未開單銷售實際值為應收費，並對應至時間和資料合約服務內容，則應用程式會在下列層級執行不得超過驗證檢查：</span><span class="sxs-lookup"><span data-stu-id="ee3b7-119">If the unbilled sales actual being created is chargeable and maps to a time and material contract line, the application performs a not-to-exceed validation check at the following levels:</span></span>

  - <span data-ttu-id="ee3b7-120">檢查為專案合約服務內容的客戶設定的限制</span><span class="sxs-lookup"><span data-stu-id="ee3b7-120">Check against the limit set up for the customer of the project contract line</span></span>
  - <span data-ttu-id="ee3b7-121">檢查為合約服務內容設定的限制</span><span class="sxs-lookup"><span data-stu-id="ee3b7-121">Check against the limit set up on the contract line</span></span>
  - <span data-ttu-id="ee3b7-122">檢查為客戶設定的限制</span><span class="sxs-lookup"><span data-stu-id="ee3b7-122">Check against the limit set up for the customer</span></span>
  - <span data-ttu-id="ee3b7-123">檢查為合約設定的限制</span><span class="sxs-lookup"><span data-stu-id="ee3b7-123">Check against the limit set up on the contract</span></span>

<span data-ttu-id="ee3b7-124">每個層級的檢查都會在考慮到已記錄的帳務積存金額以及該層級迄今為止已開發票的金額後，確保實際值的銷售金額不違反該層級的不得超過限制。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-124">The checks at each level ensure that the amount of sales value on the actual will not violate the not-to-exceed limit at that level after accounting for the amount of billing backlog already recorded, and the amount invoiced to date at that level.</span></span>

<span data-ttu-id="ee3b7-125">如果檢查通過，則未開單的銷售實際值將獲得 **已認可** 的不得超過狀態。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-125">If the check passes, the unbilled sales actual is given a not-to-exceed status of **Committed**.</span></span>

<span data-ttu-id="ee3b7-126">如果檢查失敗，則未開單的銷售實際值將獲得 **失敗** 的不得超過狀態。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-126">If the check fails, the unbilled sales actual is given a not-to-exceed status of **Failed**.</span></span> <span data-ttu-id="ee3b7-127">驗證詳細資料會通知使用者驗證失敗的層級。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-127">The validation detail informs the user at which level the validation failed.</span></span>

<span data-ttu-id="ee3b7-128">當未開單的銷售實際值被視為不應收費或免費時，如果在四個層級中的任何一個層級中沒有不得超過限制設定，或者實際值建立為成本、保留款、資源分配單位或跨組織銷售，則必須將 **不得超過狀態** 和 **不得超過驗證詳細資料** 欄位設定為 **不適用**。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-128">When the unbilled sales actual is considered non-chargeable or complimentary, if there is no not-to-exceed limit setup at any of the four levels, or if the actual being created is Cost, Retainer, Resourcing Unit, or Inter-organization Sales, the **Not-to-Exceed Status** and **Not-to-Exceed Validation Detail** fields must be set to **Not Applicable**.</span></span>

## <a name="reset-the-not-to-exceed-status"></a><span data-ttu-id="ee3b7-129">重設不得超過狀態</span><span class="sxs-lookup"><span data-stu-id="ee3b7-129">Reset the not-to-exceed status</span></span>

<span data-ttu-id="ee3b7-130">您可以對不得超過狀態執行大量重設。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-130">You can perform a bulk reset of the not-to-exceed status.</span></span> <span data-ttu-id="ee3b7-131">這可讓專案經理調整不得超過驗證，以優先開立某件特定工作、時間或費用的發票，而非已從可用不得超過金額中認可的其他工作、時間或費用。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-131">This allows Project managers to adjust not-to-exceed validation to prioritize invoicing of one particular body of work, time, or expenses over others that are already committed from the available not-to-exceed amount.</span></span>

<span data-ttu-id="ee3b7-132">在未開單銷售實際值上重設不得超過狀態後，認可金額將減少。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-132">After the not-to-exceed status is reset on unbilled sales actuals, the committed amount is reduced.</span></span> <span data-ttu-id="ee3b7-133">專案經理可以選擇以前未通過不得超過驗證的另一件工作、時間或費用，並重新評估它們。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-133">The Project manager can select another body of work, time, or expenses that previously failed the not-to-exceed validation and reevaluate them.</span></span> <span data-ttu-id="ee3b7-134">隨著認可金額的減少，這些實際值現在將通過驗證。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-134">With the reduction in the committed amount, these actuals will now pass the validation.</span></span> <span data-ttu-id="ee3b7-135">這有助於專案經理對該期間可開票交易記錄施加更大的影響和控制。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-135">This helps the Project manager exert greater influence and control over the invoiceable transactions for that period.</span></span>

<span data-ttu-id="ee3b7-136">若要重設不得超過狀態，請從 **時間和資料帳務積存** 或 **實際值** 檢視中選擇一個或多個實際值，然後選取 **重設不得超過狀態**。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-136">To reset the not-to-exceed status, select one or more actuals from the **Time and Material Billing Backlog** or **Actuals** view, and then select **Reset Not-to-Exceed Status**.</span></span>

<span data-ttu-id="ee3b7-137">在所有相關選定實際值上，不得超過狀態將重設為 **未評估**。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-137">The not-to-exceed status is reset to **Not Evaluated** on all of the relevant selected actuals.</span></span> <span data-ttu-id="ee3b7-138">重設不得超過狀態的實際值是尚未開立發票的未開單銷售實際值，不是草稿發票，並標示為應收費。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-138">Actuals that have their not-to-exceed status reset are unbilled sales actuals that aren't already invoiced, not on a draft invoice, and are marked as chargeable.</span></span> <span data-ttu-id="ee3b7-139">將忽略任何其他選定的實際值。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-139">Any other selected actuals are ignored.</span></span>

## <a name="reevaluate-not-to-exceed-status"></a><span data-ttu-id="ee3b7-140">重新評估不得超過狀態</span><span class="sxs-lookup"><span data-stu-id="ee3b7-140">Reevaluate not-to-exceed status</span></span>

<span data-ttu-id="ee3b7-141">您可以對不得超過狀態執行大量重新評估。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-141">You can perform a bulk re-evaluation of the not-to-exceed status.</span></span> <span data-ttu-id="ee3b7-142">在以下情況重新評估不得超過狀態非常有用：</span><span class="sxs-lookup"><span data-stu-id="ee3b7-142">Re-evaluation of the not-to-exceed status is useful when:</span></span>

  - <span data-ttu-id="ee3b7-143">與客戶重新談判了不得超過限制，且需要重新評估實際值。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-143">There was a renegotiation of not-to-exceed limits with the customer and actuals will need to be reevaluated.</span></span>
  - <span data-ttu-id="ee3b7-144">專案經理希望透過將一件工作優先於另一件工作來微調未開單銷售積存的開票。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-144">The Project manager wants to fine-tune the invoicing of unbilled sales backlog by prioritizing one body of work over another.</span></span>

<span data-ttu-id="ee3b7-145">若要重新評估不得超過狀態，請從 **時間和資料帳務積存** 或 **實際值** 檢視中選擇一個或多個實際值，然後選取 **重新評估不得超過狀態**。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-145">To reevaluate the not-to-exceed status, select one or more actuals from the **Time and Material Billing Backlog** or **Actuals** view, and select **Reevaluate Not-to-Exceed Status**.</span></span>

<span data-ttu-id="ee3b7-146">所有具有不得超過限制的相關選定實際值都將根據不得超過限制設定進行評估。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-146">All of the relevant selected actuals with a not-to-exceed limit will be evaluated against the not-to-exceed limit setup.</span></span> <span data-ttu-id="ee3b7-147">與重新評估不得超過狀態相關的實際值是尚未開立發票的未開單銷售實際值，不是草稿發票，並標示為應收費。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-147">Actuals that are relevant for re-evaluating the not-to-exceed status are unbilled sales actuals that are not invoiced, not on a draft invoice, and are marked as chargeable.</span></span> <span data-ttu-id="ee3b7-148">選取了任何其他選取實際值。</span><span class="sxs-lookup"><span data-stu-id="ee3b7-148">Any other select actuals selected.</span></span>
