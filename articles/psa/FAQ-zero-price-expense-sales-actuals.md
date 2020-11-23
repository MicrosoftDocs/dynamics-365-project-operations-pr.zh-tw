---
title: 為什麼費用銷售實際值上的價格會預設為零？
description: 下列三項檢查可協助您對費用銷售實際值的價格為何會預設為 0 的問題進行疑難排解。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8c2270b07b6f8765a6ec1f506fe1767a1841950b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122063"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a><span data-ttu-id="0fe8c-103">為什麼費用銷售實際值上的價格會預設為零？</span><span class="sxs-lookup"><span data-stu-id="0fe8c-103">Why is the price defaulting to zero on expense sales actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0fe8c-104">本常見問題集適用於交易類別設為 [費用] 且交易類型為 [未開單銷售] 的費用實際值。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="0fe8c-105">下列三項檢查可協助您對費用銷售實際值的價格 (帳單費率) 為何會預設為 0 的問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on expense sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-project"></a><span data-ttu-id="0fe8c-106">檢查 1：找出專案的銷售價目表</span><span class="sxs-lookup"><span data-stu-id="0fe8c-106">Check 1: Identify the sales price list for project</span></span>

<span data-ttu-id="0fe8c-107">從實際值的專案欄位中尋找專案，並移至專案頁面。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="0fe8c-108">接著移至 [銷售] 索引標籤。在 [專案合約服務內容] 網格中，按一下 [專案合約] 欄位中的連結。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-108">Then go to the Sales tab. On the Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="0fe8c-109">[專案合約] 頁面將會開啟。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-109">The Project Contract page will open.</span></span> <span data-ttu-id="0fe8c-110">在 [專案合約] 頁面上，移至 [專案價目表] 索引標籤。檢查是否至少有一份價目表附加在這裡。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span>

<span data-ttu-id="0fe8c-111">如果 [專案合約] 的 [專案價目表] 網格中沒有附加任何價目表，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="0fe8c-111">If there is no price list attached in the Project Price Lists grid of the Project Contract do the following:</span></span>

- <span data-ttu-id="0fe8c-112">將價目表附加至 [專案價目表] 網格。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="0fe8c-113">允許在此處附加的價目表必須有設為 [銷售] 的內容欄位，而且價目表的貨幣欄位也應符合專案合約的貨幣欄位。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="0fe8c-114">進行必要的修正之後，請重新建立費用項目、加以核准，並確認未開單銷售實際值顯示有效的價格。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-114">Once you’ve made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>
- <span data-ttu-id="0fe8c-115">如果專案合約的 [專案價目表] 網格已附加一份或多份價目表，請移至「檢查 2」。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, go to Check 2.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a><span data-ttu-id="0fe8c-116">檢查 2：前面找到的價目表是否在費用實際值的特定日期上有效？</span><span class="sxs-lookup"><span data-stu-id="0fe8c-116">Check 2: Are any of the price lists identified above valid for the specific date of the expense actual?</span></span>

<span data-ttu-id="0fe8c-117">若要讓 Project Service 考慮用於預設價格的價目表，該價目表必須適用於費用銷售實際值的日期。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the expense sales actual.</span></span> <span data-ttu-id="0fe8c-118">請檢查下列項目以了解前面找到的價目表是否適用：</span><span class="sxs-lookup"><span data-stu-id="0fe8c-118">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="0fe8c-119">首先從檢查所附加價目表之一般索引標籤上的開始和結束日期是否不為空白開始。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-119">Start by checking if start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="0fe8c-120">如果前面找到的價目表，其開始和結束日期為空白時，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-120">If the start and end dates on the price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="0fe8c-121">記下費用銷售實際值的開始日期欄位，並檢查任何找到的價目表是否適用於該日期。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-121">Make a note of the start date field on your expense sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="0fe8c-122">例如，費用實際值的日期應落在價目表的開始日期和結束日期之內。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-122">For example, the date of the expense actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="0fe8c-123">如果費用銷售實際值上沒有任何涵蓋該日期的價目表，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-123">If there is no price list that covers that date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="0fe8c-124">修改價目表的開始和結束日期，以確保價目表涵蓋費用實際值的日期。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="0fe8c-125">如果費用銷售實際值上有多份涵蓋該日期的價目表，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-125">If there is more than one price list that covers the date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="0fe8c-126">您可以修正此問題，做法為編輯價目表的開始和結束日期，只留下一份涵蓋費用實際值日期的價目表。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-126">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="0fe8c-127">如果只有一份價目表涵蓋費用實際值的那個日期，請移至「檢查 3」。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-127">If there is only one price list that covers that date of the expense actual, move to Check 3.</span></span>
<span data-ttu-id="0fe8c-128">完成必要的修正之後，請重新建立費用項目、加以核准，並確認未開單銷售實際值顯示有效的價格。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-128">Once you’ve done made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a><span data-ttu-id="0fe8c-129">檢查 3：適用專案價目表中是否有適用於費用類別的有效價格？</span><span class="sxs-lookup"><span data-stu-id="0fe8c-129">Check 3: Is there a valid price for the expense category in the applicable project price list?</span></span> 

<span data-ttu-id="0fe8c-130">如果您已順利完成「檢查 1」和「檢查 2」，現在應該只有一份適用於費用銷售實際值日期的專案價目表。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-130">If you have successfully completed Check 1 and Check 2, you should now have only one project price list that is applicable for the date of the expense sales actual.</span></span> <span data-ttu-id="0fe8c-131">開啟這份專案價目表，並移至 [類別價格] 索引標籤。確定費用實際值上有一列資料在特定費用類別的網格中。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-131">Open this Project Price List and go to the Category Prices tab. Make sure that there is a row in the grid for the specific expense category on the Expense actual.</span></span>
 
- <span data-ttu-id="0fe8c-132">如果沒有任何資料列，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-132">If there is no row, then you have isolated the problem.</span></span> <span data-ttu-id="0fe8c-133">在費用實際值類別的 [類別價格] 網格中建立一列。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-133">Create a row in the Category price grid for the category on your expense actual.</span></span> <span data-ttu-id="0fe8c-134">完成此動作之後，請重新建立費用項目、加以核准，並確認未開單銷售實際值顯示有效的價格。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-134">Once this is done, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 
- <span data-ttu-id="0fe8c-135">如果 [類別價格] 網格中有費用類別的一列資料，請檢查其中價格是否有效。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-135">If there is a row for the expense category in the category prices grid, check if it has a valid price.</span></span>

<span data-ttu-id="0fe8c-136">若要了解什麼是有效價格，請使用下列方法：</span><span class="sxs-lookup"><span data-stu-id="0fe8c-136">To understand what a valid price is, use these methods:</span></span>

- <span data-ttu-id="0fe8c-137">如果 [類別價格明細] 的 [定價方式] 欄位設為 [依照成本]，則費用銷售實際值的單位率費將會預設為費用項目中的值。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-137">If the Pricing Method field on the Category price line is set to At Cost, then the unit rate on your Expense sales actual will be defaulted to the value in the Expense entry.</span></span>
- <span data-ttu-id="0fe8c-138">如果 [類別價格明細] 的 [定價方式] 欄位設為 [加成百分比]，請檢查 [百分比] 欄位是否設定為有效值。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-138">If the Pricing Method field on the Category price line is set to Markup Percentage, then check if the Percent field is set to a valid value.</span></span> <span data-ttu-id="0fe8c-139">費用銷售實際值的單位費率是透過將此加成百分比套用至費用項目中的價格所預設。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-139">The unit rate on your Expense sales actual is defaulted by applying this markup percent to the price in the Expense entry.</span></span>
- <span data-ttu-id="0fe8c-140">如果 [類別價格明細] 的 [定價方式] 欄位設為 [單價]，請檢查 [價格] 欄位是否設定為有效值。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-140">If the Pricing Method field on the Category price line is set to Price per Unit, then check if the Price field is set to a valid value.</span></span> <span data-ttu-id="0fe8c-141">費用銷售實際值的單位費率將會預設為 [價格] 欄位所指定的貨幣金額。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-141">The unit rate on your Expense sales actual will be defaulted to the currency amount specified in the Price field.</span></span>

<span data-ttu-id="0fe8c-142">如果針對費用類別所設定的價格無效，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-142">If the price setup for the expense category isn't valid, then you have isolated the problem.</span></span> <span data-ttu-id="0fe8c-143">解決方案就是依據上述規則使用費用類別的有效價格來編輯類別價格明細。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-143">The solution is to edit the category price line with a valid price for the expense category in accordance with the rules above.</span></span> <span data-ttu-id="0fe8c-144">完成該動作之後，請重新建立費用項目、加以核准，然後確認未開單銷售實際值顯示有效的價格。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-144">Once you’ve done that, recreate an expense entry, approve it, and then check that the unbilled sales actual gets a valid price.</span></span>

<span data-ttu-id="0fe8c-145">如果執行上述三項檢查後，費用銷售實際值上仍未看到有效價格，請記入支援票證。</span><span class="sxs-lookup"><span data-stu-id="0fe8c-145">If you still don't see a valid price on your expense sales actual after doing the three checks above, please log a support ticket.</span></span>


