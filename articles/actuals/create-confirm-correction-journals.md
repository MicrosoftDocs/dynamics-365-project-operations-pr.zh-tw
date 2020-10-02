---
title: 建立和確認更正帳目
description: 本主題提供有關如何建立和確認更正帳目的資訊。
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
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896946"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="1c29b-103">建立和確認更正帳目</span><span class="sxs-lookup"><span data-stu-id="1c29b-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="1c29b-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="1c29b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1c29b-105">時間或費用分錄有時可能會輸入不正確。</span><span class="sxs-lookup"><span data-stu-id="1c29b-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="1c29b-106">例如，顧問可能會在建立時間分錄時選取錯誤的日期，或在輸入費用時顛倒數字順序。</span><span class="sxs-lookup"><span data-stu-id="1c29b-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="1c29b-107">如果顧問無法對已提交的分錄進行更新，管理員可以直接更正專案的分錄。</span><span class="sxs-lookup"><span data-stu-id="1c29b-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="1c29b-108">若要完成本主題中的程序，您需要系統管理員權限。</span><span class="sxs-lookup"><span data-stu-id="1c29b-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="1c29b-109">更正核准的時間分錄</span><span class="sxs-lookup"><span data-stu-id="1c29b-109">Correct approved time entries</span></span>     

<span data-ttu-id="1c29b-110">完成下列步驟以更正專案的單一或多個時間分錄。</span><span class="sxs-lookup"><span data-stu-id="1c29b-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="1c29b-111">在**銷售**區域中，選取**交易**，然後選取**核准的時間**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="1c29b-112">在**核准的時間**清單中，尋找並選取一個或多個要更正的已核准時間分錄。</span><span class="sxs-lookup"><span data-stu-id="1c29b-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="1c29b-113">您可以使用篩選來找出相關的分錄。</span><span class="sxs-lookup"><span data-stu-id="1c29b-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="1c29b-114">例如，您可能會根據專案識別碼進行篩選，然後選取所有具有該專案識別碼的已核准時間分錄。</span><span class="sxs-lookup"><span data-stu-id="1c29b-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="1c29b-115">選取**更正分錄**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-115">Select **Correct entries**.</span></span> <span data-ttu-id="1c29b-116">系統會自動使用指派的類型**時間更正**建立新的更正帳目。</span><span class="sxs-lookup"><span data-stu-id="1c29b-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="1c29b-117">您選取的分錄會新增至此帳目。</span><span class="sxs-lookup"><span data-stu-id="1c29b-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="1c29b-118">在**新增帳目**頁面上，輸入更正帳目的**描述**，然後選取**時間分錄更正**索引標籤。</span><span class="sxs-lookup"><span data-stu-id="1c29b-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="1c29b-119">在**時間分錄的新值**區段中，視需要以正確的資訊來更新欄位。</span><span class="sxs-lookup"><span data-stu-id="1c29b-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="1c29b-120">例如，您可以變更指派的專案或可預約資源。</span><span class="sxs-lookup"><span data-stu-id="1c29b-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="1c29b-121">選取**預覽**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-121">Select **Preview**.</span></span> <span data-ttu-id="1c29b-122">在對話方塊中選取**確定**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="1c29b-123">在**帳目明細**索引標籤中，您可以檢視與所選已沖回時間分錄相關的原始實際值清單以及所建立已更正的對應明細。</span><span class="sxs-lookup"><span data-stu-id="1c29b-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="1c29b-124">如果需要進行其他更正，請重複步驟 5 和 6。</span><span class="sxs-lookup"><span data-stu-id="1c29b-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="1c29b-125">所有已更正的實際值都會有與您在**時間分錄的新值**區段中所選值相同的值。</span><span class="sxs-lookup"><span data-stu-id="1c29b-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="1c29b-126">如果更正結果顯示如預期，請選取**確認**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="1c29b-127">在對話方塊中選取**確定**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="1c29b-128">返回**銷售**區域、選取**專案**，然後開啟您剛為其更新時間分錄的專案。</span><span class="sxs-lookup"><span data-stu-id="1c29b-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="1c29b-129">在**專案**頁面的**實際值**索引標籤上，檢視您所進行的變更。</span><span class="sxs-lookup"><span data-stu-id="1c29b-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="1c29b-130">如果看不到**實際值**索引標籤，請選取**相關** > **實際值**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="1c29b-131">在**實際值相關檢視表**清單中，您可以看到仍然列出已沖回的原始時間分錄，就像是對應的已更正時間分錄一樣。</span><span class="sxs-lookup"><span data-stu-id="1c29b-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="1c29b-132">例如，下圖有兩個數量為 8.00 的明細項目，在 [金額] 欄中列出借記。</span><span class="sxs-lookup"><span data-stu-id="1c29b-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="1c29b-133">此外，還有兩項數量為 -8.00 的明細項目，在 [金額] 欄中顯示貸記金額。</span><span class="sxs-lookup"><span data-stu-id="1c29b-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="1c29b-134">這些更正會將數量顯示為零。</span><span class="sxs-lookup"><span data-stu-id="1c29b-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="1c29b-135">更正核准的費用分錄</span><span class="sxs-lookup"><span data-stu-id="1c29b-135">Correct approved expense entries</span></span>

<span data-ttu-id="1c29b-136">完成下列步驟，以更正一個或多個費用分錄。</span><span class="sxs-lookup"><span data-stu-id="1c29b-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="1c29b-137">在**銷售**區域的左導覽窗格中，選取**交易**底下的**核准的費用**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="1c29b-138">在**核准的費用**清單中，選取您要更正的專案，然後選取**更正分錄**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="1c29b-139">系統會自動使用指派的類型**費用更正**建立新的更正帳目。</span><span class="sxs-lookup"><span data-stu-id="1c29b-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="1c29b-140">在**新增帳目**頁面上，輸入更正的**描述**，然後在**費用更正**索引標籤的**費用的新值**區段中，選取要針對所選費用明細進行更正的資料欄位。</span><span class="sxs-lookup"><span data-stu-id="1c29b-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="1c29b-141">例如，您可以將費用指派給其他**專案**，或是更正**費用類別**、**費用日期**或**可預約資源**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="1c29b-142">選取**預覽**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-142">Select **Preview**.</span></span> <span data-ttu-id="1c29b-143">在對話方塊中選取**確定**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="1c29b-144">確認**帳目明細**索引標籤上的更新結果。您可以檢視與所選已沖回費用分錄相關的原始實際值清單以及所建立已更正的對應明細。</span><span class="sxs-lookup"><span data-stu-id="1c29b-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="1c29b-145">如果更正的值符合預期，請選取**確認**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="1c29b-146">在對話方塊中選取**確定**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="1c29b-147">如果值顯示未如預期，請選取**取消**以返回**核准的費用**清單。</span><span class="sxs-lookup"><span data-stu-id="1c29b-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="1c29b-148">重複步驟 2 到 5。</span><span class="sxs-lookup"><span data-stu-id="1c29b-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="1c29b-149">已更正的實際值會有與您在**費用的新值**區段中所選值相同的值。</span><span class="sxs-lookup"><span data-stu-id="1c29b-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="1c29b-150">確認更正帳目之後，瀏覽回到您所更新的專案，以檢視您的變更。</span><span class="sxs-lookup"><span data-stu-id="1c29b-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="1c29b-151">在專案頁面的**實際值**索引標籤上，檢閱**實際值相關檢視表**。</span><span class="sxs-lookup"><span data-stu-id="1c29b-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="1c29b-152">原始分錄和更正分錄會列出。</span><span class="sxs-lookup"><span data-stu-id="1c29b-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="1c29b-153">下圖顯示原始費用分錄金額以及對應的已更正費用分錄金額。</span><span class="sxs-lookup"><span data-stu-id="1c29b-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


