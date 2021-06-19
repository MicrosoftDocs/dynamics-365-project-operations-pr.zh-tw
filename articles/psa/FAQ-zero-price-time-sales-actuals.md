---
title: 為什麼時間銷售實際值上的價格會預設為零？
description: 排解時間銷售實際值上的價格為何預設為 0 的問題。
author: rumant
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
ms.openlocfilehash: e32b4c8113afdc18d9b220b1a8daf5007be93ac8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011631"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a><span data-ttu-id="5b0a9-103">為什麼時間銷售實際值上的價格會預設為零？</span><span class="sxs-lookup"><span data-stu-id="5b0a9-103">Why is price defaulting to zero on time sales actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5b0a9-104">本常見問題集適用於交易類別設為 [時間] 且交易類型為 [未開單銷售] 的實際值。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="5b0a9-105">下列三項檢查可協助您對時間銷售實際值的價格 (帳單費率) 為何會預設為 0 的問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on time sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a><span data-ttu-id="5b0a9-106">檢查 1：找出專案的銷售價目表</span><span class="sxs-lookup"><span data-stu-id="5b0a9-106">Check 1: Identify the sales price list for the project</span></span>

<span data-ttu-id="5b0a9-107">從實際值的專案欄位中尋找專案，並移至專案頁面。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="5b0a9-108">接著移至 [銷售] 索引標籤，並在 [專案合約服務內容] 網格中，按一下 [專案合約] 欄位中的連結。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-108">Then go to the Sales tab and on Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="5b0a9-109">[專案合約] 頁面將會開啟。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-109">The project Contract page will open.</span></span> <span data-ttu-id="5b0a9-110">在 [專案合約] 頁面上，移至 [專案價目表] 索引標籤。檢查是否至少有一份價目表附加在這裡。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span> <span data-ttu-id="5b0a9-111">如果 [專案合約] 的 [專案價目表] 網格中沒有附加任何價目表，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-111">If there is no price list attached in the Project Price Lists grid of the Project Contract you have isolated the problem.</span></span> <span data-ttu-id="5b0a9-112">將價目表附加至 [專案價目表] 網格。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="5b0a9-113">允許在此處附加的價目表必須有設為 [銷售] 的內容欄位，而且價目表的貨幣欄位也應符合專案合約的貨幣欄位。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="5b0a9-114">完成必要的修正之後，請重新建立時間項目、加以核准，並確認未開單銷售實際值顯示有效的價格。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-114">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 

<span data-ttu-id="5b0a9-115">如果專案合約的 [專案價目表] 網格已附加一份或多份價目表，請繼續本文件的下一項檢查。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, proceed to the next check in the document.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a><span data-ttu-id="5b0a9-116">檢查 2：前面找到的價目表是否在時間銷售實際值的特定日期上有效？</span><span class="sxs-lookup"><span data-stu-id="5b0a9-116">Check 2: Are any of the price lists identified above valid for the specific date of the time sales actual?</span></span>

<span data-ttu-id="5b0a9-117">若要讓 Project Service 考慮用於預設價格的價目表，該價目表必須適用於時間銷售實際值的日期。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time sales actual.</span></span> <span data-ttu-id="5b0a9-118">請檢查下列項目以了解前面找到的價目表是否適用：</span><span class="sxs-lookup"><span data-stu-id="5b0a9-118">Check the following to see if the price list(s) identified above are applicable:</span></span>
- <span data-ttu-id="5b0a9-119">檢查所附加價目表之一般索引標籤上的開始和結束日期是否不為空白。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-119">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="5b0a9-120">如果前面找到的價目表，其開始和結束日期為空白時，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-120">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="5b0a9-121">記下時間銷售實際值的開始日期欄位，並檢查任何找到的價目表是否適用於該日期。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-121">Make a note of the start date field on your time sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="5b0a9-122">例如，時間銷售實際值的日期應落在價目表的開始日期和結束日期之內。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-122">For example, the date of the time sales actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="5b0a9-123">如果時間銷售實際值上沒有任何涵蓋該日期的價目表，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-123">If there is no price list that covers that date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="5b0a9-124">修改價目表的開始和結束日期，以確保價目表涵蓋時間銷售實際值的日期。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="5b0a9-125">如果時間銷售實際值上有多份涵蓋該日期的價目表，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-125">If there is more than one price list that covers the date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="5b0a9-126">您可以修正此問題，做法為編輯價目表的開始和結束日期，只留下一份涵蓋時間銷售實際值日期的價目表。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-126">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="5b0a9-127">如果只有一份價目表涵蓋時間銷售實際值的那個日期，請移至「檢查 3」。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-127">If there is only one price list that covers that date of the time sales actual, go to Check 3.</span></span>
<span data-ttu-id="5b0a9-128">完成必要的修正之後，請重新建立時間項目、加以核准，並確認時間銷售實際值顯示有效的價格。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-128">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a><span data-ttu-id="5b0a9-129">檢查 3：時間銷售實際值的定價維度價目表中是否有價格？</span><span class="sxs-lookup"><span data-stu-id="5b0a9-129">Check 3: Is there a price in the price list for the pricing dimensions on the time sales actual?</span></span>

<span data-ttu-id="5b0a9-130">如果您已順利完成「檢查 1」和「檢查 2」，現在應該只有一份適用於時間銷售實際值日期的價目表。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-130">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time sales actual.</span></span> <span data-ttu-id="5b0a9-131">開啟這份價目表，並瀏覽至 [角色價格] 索引標籤。確定時間銷售實際值上有一列資料在定價維度的網格中。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-131">Open this Price List and navigate to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the Time sales actual.</span></span>

<span data-ttu-id="5b0a9-132">如果時間銷售實際值上沒有任何資料列在定價維度的角色價格網格中，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-132">If there is no row in the role price grid for the pricing dimensions on the time sales actual, then you have isolated the problem.</span></span> <span data-ttu-id="5b0a9-133">在時間銷售實際值上的定價維度的 [角色價格] 網格中建立一列。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-133">Create a row in the Role prices grid for the pricing dimensions on your time sales actual.</span></span> <span data-ttu-id="5b0a9-134">完成此動作之後，請重新建立時間項目、加以核准，並確認時間銷售實際值顯示有效的價格。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-134">Once this is done, recreate time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

<span data-ttu-id="5b0a9-135">如果依照上述三項檢查執行後，時間銷售實際值上仍未看到有效價格，請記入支援票證。</span><span class="sxs-lookup"><span data-stu-id="5b0a9-135">If you still don't see a valid price on your time sales actual after following the three checks above, please log a support ticket.</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]