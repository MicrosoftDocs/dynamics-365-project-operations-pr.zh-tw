---
title: 大量更正由核准時間和費用分錄所建立的實際值
description: 本主題說明系統管理員如何對先前核准的時間或費用分錄進行單一或大量更正 (如果計費未完成)。
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 17d6648840e27a4e573985af2cdd74c4adf878e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290889"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="8b101-103">大量更正由核准時間和費用分錄所建立的實際值</span><span class="sxs-lookup"><span data-stu-id="8b101-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8b101-104">時間或費用分錄有時可能會輸入不正確。</span><span class="sxs-lookup"><span data-stu-id="8b101-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="8b101-105">例如，顧問可能會在建立時間分錄時選取錯誤的日期，或在輸入費用時顛倒數字順序。</span><span class="sxs-lookup"><span data-stu-id="8b101-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="8b101-106">如果顧問無法對已提交的分錄進行更新，管理員可以直接更正專案的分錄。</span><span class="sxs-lookup"><span data-stu-id="8b101-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="8b101-107">若要完成本主題中的程序，您需要系統管理員權限。</span><span class="sxs-lookup"><span data-stu-id="8b101-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="8b101-108">更正核准的時間分錄</span><span class="sxs-lookup"><span data-stu-id="8b101-108">Correct approved time entries</span></span>     

<span data-ttu-id="8b101-109">完成下列步驟以更正專案的單一或多個時間分錄。</span><span class="sxs-lookup"><span data-stu-id="8b101-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="8b101-110">在 **銷售** 區域中，選取 **交易**，然後選取 **核准的時間**。</span><span class="sxs-lookup"><span data-stu-id="8b101-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="8b101-111">在 **核准的時間** 清單中，尋找並選取一個或多個要更正的已核准時間分錄。</span><span class="sxs-lookup"><span data-stu-id="8b101-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="8b101-112">您可以使用篩選來找出相關的分錄。</span><span class="sxs-lookup"><span data-stu-id="8b101-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="8b101-113">例如，您可能會根據專案識別碼進行篩選，然後選取所有具有該專案識別碼的已核准時間分錄。</span><span class="sxs-lookup"><span data-stu-id="8b101-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="8b101-114">選取 **更正分錄**。</span><span class="sxs-lookup"><span data-stu-id="8b101-114">Select **Correct entries**.</span></span> <span data-ttu-id="8b101-115">系統會自動使用指派的類型 **時間更正** 建立新的更正帳目。</span><span class="sxs-lookup"><span data-stu-id="8b101-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="8b101-116">您選取的分錄會新增至此帳目。</span><span class="sxs-lookup"><span data-stu-id="8b101-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="8b101-117">在 **新增帳目** 頁面上，輸入更正帳目的 **描述**，然後選取 **時間分錄更正** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="8b101-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="8b101-118">在 **時間分錄的新值** 區段中，視需要以正確的資訊來更新欄位。</span><span class="sxs-lookup"><span data-stu-id="8b101-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="8b101-119">例如，您可以變更指派的專案或可預約資源。</span><span class="sxs-lookup"><span data-stu-id="8b101-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="8b101-120">選取 **預覽**。</span><span class="sxs-lookup"><span data-stu-id="8b101-120">Select **Preview**.</span></span> <span data-ttu-id="8b101-121">在對話方塊中選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="8b101-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="8b101-122">在 **帳目明細** 索引標籤中，您可以檢視與所選已沖回時間分錄相關的原始實際值清單以及所建立已更正的對應明細。</span><span class="sxs-lookup"><span data-stu-id="8b101-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="8b101-123">如果需要進行其他更正，請重複步驟 5 和 6。</span><span class="sxs-lookup"><span data-stu-id="8b101-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b101-124">所有已更正的實際值都會有與您在 **時間分錄的新值** 區段中所選值相同的值。</span><span class="sxs-lookup"><span data-stu-id="8b101-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="8b101-125">如果更正結果顯示如預期，請選取 **確認**。</span><span class="sxs-lookup"><span data-stu-id="8b101-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="8b101-126">在對話方塊中選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="8b101-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="8b101-127">返回 **銷售** 區域、選取 **專案**，然後開啟您剛為其更新時間分錄的專案。</span><span class="sxs-lookup"><span data-stu-id="8b101-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="8b101-128">在 **專案** 頁面的 **實際值** 索引標籤上，檢視您所進行的變更。</span><span class="sxs-lookup"><span data-stu-id="8b101-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b101-129">如果看不到 **實際值** 索引標籤，請選取 **相關** > **實際值**。</span><span class="sxs-lookup"><span data-stu-id="8b101-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="8b101-130">在 **實際值相關檢視表** 清單中，您可以看到仍然列出已沖回的原始時間分錄，就像是對應的已更正時間分錄一樣。</span><span class="sxs-lookup"><span data-stu-id="8b101-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="8b101-131">例如，下圖有兩個數量為 8.00 的明細項目，在 [金額] 欄中列出借記。</span><span class="sxs-lookup"><span data-stu-id="8b101-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="8b101-132">此外，還有兩項數量為 -8.00 的明細項目，在 [金額] 欄中顯示貸記金額。</span><span class="sxs-lookup"><span data-stu-id="8b101-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="8b101-133">這些更正會將數量顯示為零。</span><span class="sxs-lookup"><span data-stu-id="8b101-133">These corrections bring the quantity to zero.</span></span>

![實際值相關檢視表清單](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="8b101-135">更正核准的費用分錄</span><span class="sxs-lookup"><span data-stu-id="8b101-135">Correct approved expense entries</span></span>

<span data-ttu-id="8b101-136">完成下列步驟，以更正一個或多個費用分錄。</span><span class="sxs-lookup"><span data-stu-id="8b101-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="8b101-137">在 **銷售** 區域的左導覽窗格中，選取 **交易** 底下的 **核准的費用**。</span><span class="sxs-lookup"><span data-stu-id="8b101-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="8b101-138">在 **核准的費用** 清單中，選取您要更正的專案，然後選取 **更正分錄**。</span><span class="sxs-lookup"><span data-stu-id="8b101-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="8b101-139">系統會自動使用指派的類型 **費用更正** 建立新的更正帳目。</span><span class="sxs-lookup"><span data-stu-id="8b101-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="8b101-140">在 **新增帳目** 頁面上，輸入更正的 **描述**，然後在 **費用更正** 索引標籤的 **費用的新值** 區段中，選取要針對所選費用明細進行更正的資料欄位。</span><span class="sxs-lookup"><span data-stu-id="8b101-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="8b101-141">例如，您可以將費用指派給其他 **專案**，或是更正 **費用類別**、**費用日期** 或 **可預約資源**。</span><span class="sxs-lookup"><span data-stu-id="8b101-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="8b101-142">選取 **預覽**。</span><span class="sxs-lookup"><span data-stu-id="8b101-142">Select **Preview**.</span></span> <span data-ttu-id="8b101-143">在對話方塊中選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="8b101-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="8b101-144">確認 **帳目明細** 索引標籤上的更新結果。您可以檢視與所選已沖回費用分錄相關的原始實際值清單以及所建立已更正的對應明細。</span><span class="sxs-lookup"><span data-stu-id="8b101-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="8b101-145">如果更正的值符合預期，請選取 **確認**。</span><span class="sxs-lookup"><span data-stu-id="8b101-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="8b101-146">在對話方塊中選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="8b101-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="8b101-147">如果值顯示未如預期，請選取 **取消** 以返回 **核准的費用** 清單。</span><span class="sxs-lookup"><span data-stu-id="8b101-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="8b101-148">重複步驟 2 到 5。</span><span class="sxs-lookup"><span data-stu-id="8b101-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b101-149">已更正的實際值會有與您在 **費用的新值** 區段中所選值相同的值。</span><span class="sxs-lookup"><span data-stu-id="8b101-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="8b101-150">確認更正帳目之後，瀏覽回到您所更新的專案，以檢視您的變更。</span><span class="sxs-lookup"><span data-stu-id="8b101-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="8b101-151">在專案頁面的 **實際值** 索引標籤上，檢閱 **實際值相關檢視表**。</span><span class="sxs-lookup"><span data-stu-id="8b101-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="8b101-152">原始分錄和更正分錄會列出。</span><span class="sxs-lookup"><span data-stu-id="8b101-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="8b101-153">下圖顯示原始費用分錄金額以及對應的已更正費用分錄金額。</span><span class="sxs-lookup"><span data-stu-id="8b101-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![費用實際值](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]