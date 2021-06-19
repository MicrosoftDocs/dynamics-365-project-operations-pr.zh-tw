---
title: 使用里程費率層級來設定里程
description: 本主題提供有關里程費率和里程費率層級的資訊。
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083661"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a><span data-ttu-id="c258d-103">使用里程費率層級來設定里程</span><span class="sxs-lookup"><span data-stu-id="c258d-103">Set up mileage using mileage rate tiers</span></span>

<span data-ttu-id="c258d-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="c258d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c258d-105">在報告費用且選取的費用類別為 **里程** 時，該費用明細的金額是根據 *每一里程部分* 金額來計算。</span><span class="sxs-lookup"><span data-stu-id="c258d-105">When an expense is reported and the selected expense category is **Mileage**, the amount for that expense line is calculated according to the *rate per mileage* amount.</span></span> <span data-ttu-id="c258d-106">此金額是使用定義的里程層級，或依照里程的標準費率 (如果未設定里程費率等級) 來決定。</span><span class="sxs-lookup"><span data-stu-id="c258d-106">This amount is determined by using defined mileage tiers or, if no mileage rate tiers are set up, by following a standard rate of mileage.</span></span> 

<span data-ttu-id="c258d-107">若要設定里程費率，請移至 **費用管理** > **設定** > **一般** > **費用類別** > **里程** > **類別設定**。</span><span class="sxs-lookup"><span data-stu-id="c258d-107">Mileage rate tiers can be set up by going to **Expense Management** > **Setup** > **General** > **Expense categories** > **Mileage** > **Category setup**.</span></span>

<span data-ttu-id="c258d-108">升級至 10.0.18 之後，如果您的組織使用里程費用類別，請在檢閱下列設計變更之後，考慮啟用里程功能。</span><span class="sxs-lookup"><span data-stu-id="c258d-108">After you upgrade to 10.0.18, if your organization uses the mileage expense category, consider enabling the mileage feature after reviewing the design changes below.</span></span> 

<span data-ttu-id="c258d-109">里程費率層級的新設計會影響處理 **數量** 欄位值的方式。</span><span class="sxs-lookup"><span data-stu-id="c258d-109">The new design of mileage rate tiers impacts how the value in the **Quantity** field is processed.</span></span> <span data-ttu-id="c258d-110">發行 10.0.18 之前，已將 **數量** 欄位中的值視為下限。</span><span class="sxs-lookup"><span data-stu-id="c258d-110">Prior to the release of 10.0.18, the value in the **Quantity** field was considered to be the lower limit.</span></span> <span data-ttu-id="c258d-111">當累計越過該值時，會使用對應的費率。</span><span class="sxs-lookup"><span data-stu-id="c258d-111">When accumulation crossed that value, the corresponding rate was used.</span></span>  <span data-ttu-id="c258d-112">自 10.0.18 起，則將 **數量** 欄位中的值視為上限。</span><span class="sxs-lookup"><span data-stu-id="c258d-112">As of 10.0.18, the value in the **Quantity** field is considered the upper limit.</span></span> <span data-ttu-id="c258d-113">當里程累計小於 **數量** 欄位中的值時，會使用對應的費率。</span><span class="sxs-lookup"><span data-stu-id="c258d-113">The corresponding rate is used when mileage accumulation is less than the value in the **Quantity** field.</span></span>  <span data-ttu-id="c258d-114">里程層級的新模型有助於維持各里程層級的一致性，並改善可用性。</span><span class="sxs-lookup"><span data-stu-id="c258d-114">The new model for mileage tiers helps with consistency across mileage tiers and better usability.</span></span>   

<span data-ttu-id="c258d-115">所有已核准的費用報表都會依據新的設計，在進行過帳時重新計算。</span><span class="sxs-lookup"><span data-stu-id="c258d-115">All approved expense reports will be recalculated during posting according to the new design.</span></span>

## <a name="example"></a><span data-ttu-id="c258d-116">範例</span><span class="sxs-lookup"><span data-stu-id="c258d-116">Example</span></span>
 
### <a name="before-version-10018"></a><span data-ttu-id="c258d-117">在 10.0.18 版之前</span><span class="sxs-lookup"><span data-stu-id="c258d-117">Before version 10.0.18</span></span>
<span data-ttu-id="c258d-118">在有兩個里程費率層級的情況下，每一層的 **數量** 欄位都代表里程下限。</span><span class="sxs-lookup"><span data-stu-id="c258d-118">With two mileage rate tiers, the **Quantity** field in each tier represents the lower mileage limit.</span></span> <span data-ttu-id="c258d-119">目前第一層的值為零 (0) 且費率為 0.45，而第二層的值為 1000 且費率為 0.25。</span><span class="sxs-lookup"><span data-stu-id="c258d-119">Currently, tier one has a value of zero (0) and a rate of 0.45, and tier two has a value of 1000 and a rate of 0.25.</span></span> <span data-ttu-id="c258d-120">如果累計英里或公里數越過欄位中的值，則會使用相關費率。</span><span class="sxs-lookup"><span data-stu-id="c258d-120">If the accumulated miles or kilometers crosses the value in the field, the related rate is used.</span></span> <span data-ttu-id="c258d-121">如果沒有任何數量為零的明細，則系統會使用 [費用管理] 中所定義的里程費率。</span><span class="sxs-lookup"><span data-stu-id="c258d-121">If there's no line with zero quantity, the system uses the rate of mileage that is defined in Expense management.</span></span> 
 
<span data-ttu-id="c258d-122">如果員工提交 1,500 英里的費用報表，則已過帳費用報表上的兩個里程明細將會是：1000 (費率 0.45) + 500 (費率 0.25) = 575.00。</span><span class="sxs-lookup"><span data-stu-id="c258d-122">If an employee submits an expense report with 1,500 miles, the two mileage lines on the posted expense report would be: 1000 (rate 0.45) +  500 (rate 0.25) = 575.00.</span></span>

### <a name="after-version-10018"></a><span data-ttu-id="c258d-123">在 10.0.18 版之後</span><span class="sxs-lookup"><span data-stu-id="c258d-123">After version 10.0.18</span></span>
<span data-ttu-id="c258d-124">在 10.0.18 中，每一層的 **數量** 欄位代表該層的上限。</span><span class="sxs-lookup"><span data-stu-id="c258d-124">In 10.0.18, the **Quantity** field in each tier represents the upper limit of the tier.</span></span> <span data-ttu-id="c258d-125">目前第一層的值為 999 且費率為 0.45，而第二層的值為 999,999,999.00 且費率為 0.25。</span><span class="sxs-lookup"><span data-stu-id="c258d-125">Currently, tier one has a value of 999 and a rate of 0.45, and tier two has a value of 999,999,999.00 and a rate of 0.25.</span></span> <span data-ttu-id="c258d-126">如果累計英里或公里數越過 **數量** 欄位中的值，則會使用相關費率。</span><span class="sxs-lookup"><span data-stu-id="c258d-126">If the accumulated miles or kilometers crosses the value in the **Quantity** field, the related rate is used.</span></span> <span data-ttu-id="c258d-127">如果所有上限都已超過，則系統會使用 [費用管理] 中所定義的里程費率。</span><span class="sxs-lookup"><span data-stu-id="c258d-127">If all upper limits are exceeded, the system uses the rate of mileage that is defined in Expense management.</span></span> 
 
<span data-ttu-id="c258d-128">若要正確計算相同的案例，必須變更層級設定。</span><span class="sxs-lookup"><span data-stu-id="c258d-128">To correctly calculate the same scenario, the tier set up must be changed.</span></span> <span data-ttu-id="c258d-129">第一層中 **數量** 欄位的值為 999.00，而第二層中的值為 999,999,999.00。</span><span class="sxs-lookup"><span data-stu-id="c258d-129">The **Quantity** field in tier one has a value of 999.00 and a value of 999,999,999.00 in tier two.</span></span> <span data-ttu-id="c258d-130">如果員工超過第一層中英里或公里數的總數量，則系統會使用在 [費用管理] 中定義的里程費率。</span><span class="sxs-lookup"><span data-stu-id="c258d-130">If an employee exceeds the total quantity of miles or kilometers in tier one, the system uses the rate of mileage that is defined in Expense management.</span></span> 
  
<span data-ttu-id="c258d-131">如果員工提交 1,500 英里的費用報表，則已過帳費用報表上的兩個里程明細將會是：1000 (費率 0.45) + 500 (費率 0.25) = 575</span><span class="sxs-lookup"><span data-stu-id="c258d-131">If an employee submits an expense report with 1,500 miles, the two mileage lines on the posted expense report would be: 1000 (rate 0.45) +  500 (rate 0.25) = 575</span></span>

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a><span data-ttu-id="c258d-132">[為多個相同費率的里程層級啟用里程金額計算] 功能</span><span class="sxs-lookup"><span data-stu-id="c258d-132">Enable the Mileage amount calculation for multiple mileage tiers with same rate feature</span></span>

<span data-ttu-id="c258d-133">**為多個相同費率的里程層級啟用里程金額計算** 功能可改善里程費率計算。</span><span class="sxs-lookup"><span data-stu-id="c258d-133">The **Mileage amount calculation for multiple mileage tiers with same rate** feature improves mileage rate calculation.</span></span> <span data-ttu-id="c258d-134">若要啟用此功能，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="c258d-134">Complete the following steps to enable this feature.</span></span>

1. <span data-ttu-id="c258d-135">移至 **工作區** > **功能管理**。</span><span class="sxs-lookup"><span data-stu-id="c258d-135">Go to **Workspaces** > **Feature Management**.</span></span> 
2. <span data-ttu-id="c258d-136">在清單中，找出並選取 **為多個相同費率的里程層級啟用里程金額計算**，然後選取 **立即啟用**。</span><span class="sxs-lookup"><span data-stu-id="c258d-136">In the list, locate and select **Mileage amount calculation for multiple mileage tiers with same rate**, and then select **Enable now**.</span></span>

<span data-ttu-id="c258d-137">啟用此功能之後，重設里程層級以正確反映 **數量** 欄位的值。</span><span class="sxs-lookup"><span data-stu-id="c258d-137">After you enable the feature, reset the mileage tiers to correctly reflect the value of the **Quantity** field.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
