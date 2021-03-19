---
title: 為什麼時間成本實際值上的價格會預設為零？
description: 排解時間成本實際值上的價格為何預設為 0 的問題。
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
ms.openlocfilehash: 65f2bc773a376800928cc3746691061d8e290f74
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285788"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="aceb9-103">為什麼時間成本實際值上的價格會預設為零？</span><span class="sxs-lookup"><span data-stu-id="aceb9-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="aceb9-104">本常見問題集適用於交易類別設為 [時間] 且交易類型為 [成本] 的實際值。</span><span class="sxs-lookup"><span data-stu-id="aceb9-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="aceb9-105">下列三項檢查可協助您對時間成本實際值的價格為何會預設為 0 的問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="aceb9-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="aceb9-106">檢查 1：找出專案的成本價目表</span><span class="sxs-lookup"><span data-stu-id="aceb9-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="aceb9-107">從實際值的專案欄位中尋找專案，然後移至專案頁面。</span><span class="sxs-lookup"><span data-stu-id="aceb9-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="aceb9-108">按一下欄位中的合約單位連結。</span><span class="sxs-lookup"><span data-stu-id="aceb9-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="aceb9-109">在 [合約單位] 頁面中，檢查合約單位在 [成本價目表] 網格中是否有價目表。</span><span class="sxs-lookup"><span data-stu-id="aceb9-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="aceb9-110">如果有一個以上的價目表，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="aceb9-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="aceb9-111">Project Service 對每個組織單位僅支援一份價目表。</span><span class="sxs-lookup"><span data-stu-id="aceb9-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="aceb9-112">從此實體移除所有的價目表，直到只有一份價目表附加在組織單位的 [成本價目表] 網格中為止。</span><span class="sxs-lookup"><span data-stu-id="aceb9-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="aceb9-113">如果沒有任何價目表附加至組織單位，請記下組織單位的貨幣。</span><span class="sxs-lookup"><span data-stu-id="aceb9-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="aceb9-114">移至 Project Service，再移至 [參數]，然後開啟 [價目表] 索引標籤。檢查是否有任何內容設為 [成本] 且貨幣符合組織單位貨幣的價目表。</span><span class="sxs-lookup"><span data-stu-id="aceb9-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="aceb9-115">如果沒有任何符合該準則的價目表，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="aceb9-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="aceb9-116">務必要有至少一個內容設為 [成本] 且貨幣符合組織單位貨幣的價目表。</span><span class="sxs-lookup"><span data-stu-id="aceb9-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="aceb9-117">如果有多份符合該準則的價目表，請繼續閱讀本文件以進行其他檢查。</span><span class="sxs-lookup"><span data-stu-id="aceb9-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="aceb9-118">檢查 2：前面找到的價目表是否在時間成本實際值的特定日期上有效？</span><span class="sxs-lookup"><span data-stu-id="aceb9-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="aceb9-119">若要讓 Project Service 考慮用於預設價格的價目表，該價目表必須適用於時間成本實際值的日期。</span><span class="sxs-lookup"><span data-stu-id="aceb9-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="aceb9-120">請檢查下列項目以了解前面找到的價目表是否適用：</span><span class="sxs-lookup"><span data-stu-id="aceb9-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="aceb9-121">檢查所附加價目表之一般索引標籤上的開始和結束日期是否不為空白。</span><span class="sxs-lookup"><span data-stu-id="aceb9-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="aceb9-122">如果前面找到的價目表，其開始和結束日期為空白時，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="aceb9-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="aceb9-123">記下時間成本實際值的開始日期欄位，並檢查任何找到的價目表是否適用於該日期。</span><span class="sxs-lookup"><span data-stu-id="aceb9-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="aceb9-124">例如，時間成本實際值的日期應落在價目表的開始日期和結束日期之內。</span><span class="sxs-lookup"><span data-stu-id="aceb9-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="aceb9-125">如果時間成本實際值上沒有任何涵蓋該日期的價目表，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="aceb9-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="aceb9-126">修改價目表的開始和結束日期，以確保價目表涵蓋時間成本實際值的日期。</span><span class="sxs-lookup"><span data-stu-id="aceb9-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="aceb9-127">如果時間成本實際值上有多份涵蓋該日期的價目表，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="aceb9-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="aceb9-128">您可以修正此問題，做法為編輯價目表的開始和結束日期，只留下一份涵蓋時間成本實際值日期的價目表。</span><span class="sxs-lookup"><span data-stu-id="aceb9-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="aceb9-129">如果只有一份涵蓋時間成本實際值日期的價目表，請移至本文件的下一項檢查。</span><span class="sxs-lookup"><span data-stu-id="aceb9-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="aceb9-130">完成必要的修正之後，請重新建立時間項目、加以核准，並確認時間成本實際值顯示有效的價格。</span><span class="sxs-lookup"><span data-stu-id="aceb9-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="aceb9-131">檢查 3：時間成本實際值的定價維度價目表中是否有價格？</span><span class="sxs-lookup"><span data-stu-id="aceb9-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="aceb9-132">如果您已順利完成「檢查 1」和「檢查 2」，現在應該只有一份適用於時間成本實際值日期的價目表。</span><span class="sxs-lookup"><span data-stu-id="aceb9-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="aceb9-133">開啟這份價目表，並移至 [角色價格] 索引標籤。確定時間成本實際值上有一列資料在定價維度的網格中。</span><span class="sxs-lookup"><span data-stu-id="aceb9-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="aceb9-134">如果時間成本實際值上沒有任何資料列在定價維度的角色價格網格中，您就找到了問題所在。</span><span class="sxs-lookup"><span data-stu-id="aceb9-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="aceb9-135">在時間成本實際值上的定價維度的 [角色價格] 網格中建立一列。</span><span class="sxs-lookup"><span data-stu-id="aceb9-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="aceb9-136">完成此動作之後，請重新建立時間項目、加以核准，並確認時間成本實際值顯示有效的價格。</span><span class="sxs-lookup"><span data-stu-id="aceb9-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="aceb9-137">如果執行上述三項檢查後，時間成本實際值上仍未看到有效價格，請記入支援票證。</span><span class="sxs-lookup"><span data-stu-id="aceb9-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]