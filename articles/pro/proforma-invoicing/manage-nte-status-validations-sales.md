---
title: 管理不得超過狀態和驗證
description: 此主題提供有關在 Project Operations 中執行的不得超過限制檢查的資訊。
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7026ff654a9db8e8a22bcef544b043af39865559
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866717"
---
# <a name="manage-not-to-exceed-status-and-validations"></a><span data-ttu-id="5c2e8-103">管理不得超過狀態和驗證</span><span class="sxs-lookup"><span data-stu-id="5c2e8-103">Manage not-to-exceed status and validations</span></span> 

<span data-ttu-id="5c2e8-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="5c2e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="not-to-exceed-on-approvals"></a><span data-ttu-id="5c2e8-105">核准時不得超過</span><span class="sxs-lookup"><span data-stu-id="5c2e8-105">Not-to-exceed on approvals</span></span>

<span data-ttu-id="5c2e8-106">送出時間、費用或材料使用項目時，會建立核准記錄。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-106">When a time, expense, or material usage entry is submitted, an approval record is created.</span></span> <span data-ttu-id="5c2e8-107">如果核准為應收費，並對應至時間和資料合約服務內容，則系統會在下列層級完成不得超過驗證檢查：</span><span class="sxs-lookup"><span data-stu-id="5c2e8-107">If the approval is chargeable and maps to a time and material contract line, the system completes a not-to-exceed validation check at the following levels:</span></span>

  - <span data-ttu-id="5c2e8-108">檢查為專案合約服務內容中的客戶設定的限制</span><span class="sxs-lookup"><span data-stu-id="5c2e8-108">Check against the limit set up for the customer on the project contract line</span></span>
  - <span data-ttu-id="5c2e8-109">檢查為合約服務內容設定的限制</span><span class="sxs-lookup"><span data-stu-id="5c2e8-109">Check against the limit set up on the contract line</span></span>
  - <span data-ttu-id="5c2e8-110">檢查為客戶設定的限制</span><span class="sxs-lookup"><span data-stu-id="5c2e8-110">Check against the limit set up for the customer</span></span>
  - <span data-ttu-id="5c2e8-111">檢查為合約設定的限制</span><span class="sxs-lookup"><span data-stu-id="5c2e8-111">Check against the limit set up on the contract</span></span>

<span data-ttu-id="5c2e8-112">每個層級的檢查都涉及在考慮到已記錄的帳務積存金額以及該層級迄今為止已開發票的金額後，確保此核准的銷售金額不違反該層級的不得超過限制。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-112">The checks at each level involve ensuring that the amount of sales value on this approval will not violate the not-to-exceed limit at that level after accounting for the amount of billing backlog already recorded, and the amount invoiced to date at that level.</span></span>

<span data-ttu-id="5c2e8-113">如果檢查通過，則核准將具有 **成功** 的驗證狀態。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-113">If the check passes, the approval is given a validation status of **Success**.</span></span>

<span data-ttu-id="5c2e8-114">如果檢查失敗，則核准將具有 **失敗** 的驗證狀態。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-114">If the check fails, the approval is given a validation status of **Failed**.</span></span> <span data-ttu-id="5c2e8-115">不得超過驗證詳細資料將通知使用者驗證失敗的層級。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-115">The not-to-exceed validation detail will inform the user at which level the validation failed.</span></span>

<span data-ttu-id="5c2e8-116">將送出的時間、費用或材料使用項目視為不應收費時，「不得超過」驗證狀態會設定為 **不適用**，且驗證詳細資料等於 **不適用**。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-116">When the submitted time, expense, or material usage entry is considered non-chargeable, the not-to-exceed validation status is set to **Not Applicable** with the validation detail equal to **Not applicable**.</span></span>

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a><span data-ttu-id="5c2e8-117">未開單銷售實際值不得超過</span><span class="sxs-lookup"><span data-stu-id="5c2e8-117">Not-to-exceed on unbilled sales actuals</span></span>

<span data-ttu-id="5c2e8-118">核准時間、費用或材料使用項目時，會建立成本與未開單銷售實際值記錄。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-118">When a time, expense, or material usage entry is approved, cost and unbilled sales actuals records are created.</span></span> <span data-ttu-id="5c2e8-119">如果要建立的未開單銷售實際值為應收費，並對應至時間和資料合約服務內容，則應用程式會在下列層級執行不得超過驗證檢查：</span><span class="sxs-lookup"><span data-stu-id="5c2e8-119">If the unbilled sales actual being created is chargeable and maps to a time and material contract line, the application performs a not-to-exceed validation check at the following levels:</span></span>

  - <span data-ttu-id="5c2e8-120">檢查為專案合約服務內容的客戶設定的限制</span><span class="sxs-lookup"><span data-stu-id="5c2e8-120">Check against the limit set up for the customer of the project contract line</span></span>
  - <span data-ttu-id="5c2e8-121">檢查為合約服務內容設定的限制</span><span class="sxs-lookup"><span data-stu-id="5c2e8-121">Check against the limit set up on the contract line</span></span>
  - <span data-ttu-id="5c2e8-122">檢查為客戶設定的限制</span><span class="sxs-lookup"><span data-stu-id="5c2e8-122">Check against the limit set up for the customer</span></span>
  - <span data-ttu-id="5c2e8-123">檢查為合約設定的限制</span><span class="sxs-lookup"><span data-stu-id="5c2e8-123">Check against the limit set up on the contract</span></span>

<span data-ttu-id="5c2e8-124">每個層級的檢查都會在考慮到已記錄的帳務積存金額以及該層級迄今為止已開發票的金額後，確保實際值的銷售金額不違反該層級的不得超過限制。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-124">The checks at each level ensure that the amount of sales value on the actual will not violate the not-to-exceed limit at that level after accounting for the amount of billing backlog already recorded, and the amount invoiced to date at that level.</span></span>

<span data-ttu-id="5c2e8-125">如果檢查通過，則未開單的銷售實際值將獲得 **已認可** 的不得超過狀態。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-125">If the check passes, the unbilled sales actual is given a not-to-exceed status of **Committed**.</span></span>

<span data-ttu-id="5c2e8-126">如果檢查失敗，則未開單的銷售實際值將獲得 **失敗** 的不得超過狀態。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-126">If the check fails, the unbilled sales actual is given a not-to-exceed status of **Failed**.</span></span> <span data-ttu-id="5c2e8-127">驗證詳細資料會通知使用者驗證失敗的層級。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-127">The validation detail informs the user at which level the validation failed.</span></span>

<span data-ttu-id="5c2e8-128">當未開單的銷售實際值被視為不應收費或免費時，如果在四個層級中的任何一個層級中沒有不得超過限制設定，或者實際值建立為成本、保留款、資源分配單位或跨組織銷售，則必須將 **不得超過狀態** 和 **不得超過驗證詳細資料** 欄位設定為 **不適用**。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-128">When the unbilled sales actual is considered non-chargeable or complimentary, if there is no not-to-exceed limit setup at any of the four levels, or if the actual being created is Cost, Retainer, Resourcing Unit, or Inter-organization Sales, the **Not-to-Exceed Status** and **Not-to-Exceed Validation Detail** fields must be set to **Not Applicable**.</span></span>

## <a name="reset-the-not-to-exceed-status"></a><span data-ttu-id="5c2e8-129">重設不得超過狀態</span><span class="sxs-lookup"><span data-stu-id="5c2e8-129">Reset the not-to-exceed status</span></span>

<span data-ttu-id="5c2e8-130">您可以對不得超過狀態執行大量重設。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-130">You can perform a bulk reset of the not-to-exceed status.</span></span> <span data-ttu-id="5c2e8-131">專案經理可以調整「不得超過」驗證，將工作、時間、費用或材料使用方式其中一個特定主體的開立發票優先順序設定為高於其他已根據可用「不得超過」金額認可的主體。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-131">Project managers can adjust the not-to-exceed validation to prioritize invoicing of one particular body of work, time, expense, or material usage over others that are already committed from the available not-to-exceed amount.</span></span>

<span data-ttu-id="5c2e8-132">在未開單銷售實際值上重設不得超過狀態後，認可金額將減少。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-132">After the not-to-exceed status is reset on unbilled sales actuals, the committed amount is reduced.</span></span> <span data-ttu-id="5c2e8-133">專案經理可以選取另一個先前未通過「不得超過」驗證而重新評估的工作、時間、費用或材料使用項目主體。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-133">The Project manager can select another body of work, time, expense, or material usage entry that previously failed the not-to-exceed validation and reevaluate.</span></span> <span data-ttu-id="5c2e8-134">縮減認可的金額後，這些實際值現在會通過驗證，這可協助專案經理對該期間的可開票交易施加更大的影響和控制。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-134">With the reduction in the committed amount, these actuals now pass the validation which helps the Project manager exert greater influence and control over the invoiceable transactions for that period.</span></span>

<span data-ttu-id="5c2e8-135">若要重設不得超過狀態，請從 **時間和資料帳務積存** 或 **實際值** 檢視中選擇一個或多個實際值，然後選取 **重設不得超過狀態**。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-135">To reset the not-to-exceed status, select one or more actuals from the **Time and Material Billing Backlog** or **Actuals** view, and then select **Reset Not-to-Exceed Status**.</span></span>

<span data-ttu-id="5c2e8-136">在所有相關選定實際值上，不得超過狀態將重設為 **未評估**。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-136">The not-to-exceed status is reset to **Not Evaluated** on all of the relevant selected actuals.</span></span> <span data-ttu-id="5c2e8-137">重設不得超過狀態的實際值是尚未開立發票的未開單銷售實際值，不是草稿發票，並標示為應收費。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-137">Actuals that have their not-to-exceed status reset are unbilled sales actuals that aren't already invoiced, not on a draft invoice, and are marked as chargeable.</span></span> <span data-ttu-id="5c2e8-138">將忽略任何其他選定的實際值。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-138">Any other selected actuals are ignored.</span></span>

## <a name="reevaluate-not-to-exceed-status"></a><span data-ttu-id="5c2e8-139">重新評估不得超過狀態</span><span class="sxs-lookup"><span data-stu-id="5c2e8-139">Reevaluate not-to-exceed status</span></span>

<span data-ttu-id="5c2e8-140">您可以對不得超過狀態執行大量重新評估。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-140">You can perform a bulk re-evaluation of the not-to-exceed status.</span></span> <span data-ttu-id="5c2e8-141">在以下情況重新評估不得超過狀態非常有用：</span><span class="sxs-lookup"><span data-stu-id="5c2e8-141">Re-evaluation of the not-to-exceed status is useful when:</span></span>

  - <span data-ttu-id="5c2e8-142">與客戶重新談判了不得超過限制，且需要重新評估實際值。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-142">There was a renegotiation of not-to-exceed limits with the customer and actuals will need to be reevaluated.</span></span>
  - <span data-ttu-id="5c2e8-143">專案經理希望透過將一件工作優先於另一件工作來微調未開單銷售積存的開票。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-143">The Project manager wants to fine-tune the invoicing of unbilled sales backlog by prioritizing one body of work over another.</span></span>

<span data-ttu-id="5c2e8-144">若要重新評估不得超過狀態，請從 **時間和資料帳務積存** 或 **實際值** 檢視中選擇一個或多個實際值，然後選取 **重新評估不得超過狀態**。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-144">To reevaluate the not-to-exceed status, select one or more actuals from the **Time and Material Billing Backlog** or **Actuals** view, and select **Reevaluate Not-to-Exceed Status**.</span></span>

<span data-ttu-id="5c2e8-145">所有具有不得超過限制的相關選定實際值都將根據不得超過限制設定進行評估。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-145">All of the relevant selected actuals with a not-to-exceed limit will be evaluated against the not-to-exceed limit setup.</span></span> <span data-ttu-id="5c2e8-146">與重新評估不得超過狀態相關的實際值是尚未開立發票的未開單銷售實際值，不是草稿發票，並標示為應收費。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-146">Actuals that are relevant for re-evaluating the not-to-exceed status are unbilled sales actuals that are not invoiced, not on a draft invoice, and are marked as chargeable.</span></span> <span data-ttu-id="5c2e8-147">選取了任何其他選取實際值。</span><span class="sxs-lookup"><span data-stu-id="5c2e8-147">Any other select actuals selected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
