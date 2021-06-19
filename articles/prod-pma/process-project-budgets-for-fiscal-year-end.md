---
title: 在會計年度結束時轉移專案預算
description: 本主題提供有關如何將剩餘預算金額轉移到未來年度並建立預算登記詳細資料的資訊。
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: be3dc039b92e88cac6f6b3b7f72bc32ecf587539
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008031"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="fe7b5-103">在會計年度結束時轉移專案預算</span><span class="sxs-lookup"><span data-stu-id="fe7b5-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe7b5-104">處理多年度專案時，您可能會在會計年度結束時有剩餘預算。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="fe7b5-105">您可以將剩餘預算金額轉移到未來年度，並為相關總帳科目中建立這些金額的預算登記詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="fe7b5-106">結轉剩餘金額之前，請審查並分析剩餘預算金額。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="fe7b5-107">審查並分析剩餘預算金額</span><span class="sxs-lookup"><span data-stu-id="fe7b5-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="fe7b5-108">完成下列步驟，以審查專案的年終預算金額，但不結轉金額。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="fe7b5-109">移至 **專案管理與會計** > **定期** > **預算** > **結轉預算**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="fe7b5-110">在 **專案預算結轉程序** 頁面的 **年終選項** 索引標籤上，確認未啟用 **結轉剩餘專案預算金額**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="fe7b5-111">在 **參數** 索引標籤的 **專案預算年度** 欄位中，選取您要檢視剩餘預算金額的會計年度。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="fe7b5-112">在 **開始會計年度** 欄位中，選取您要檢視剩餘預算金額的會計年度。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="fe7b5-113">在 **來源預測模型** 欄位中，選取 **剩餘預算**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="fe7b5-114">若要包含符合所選準則的專案，且沒有剩餘預算，請選取 **顯示零剩餘**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="fe7b5-115">在 **選取預算** 索引標籤上，選取 **擷取所有預算** 以載入所有符合所選準則的預算，然後選取 **程序**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="fe7b5-116">若要設計會在窗格中載入特定一組預算的資料庫查詢，請選取 **擷取選取的預算**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="fe7b5-117">如需窗格中特定一行的詳細資訊，請選取該行，然後選取 **檢視預算詳細資料** 或 **檢視科目**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="fe7b5-118">結轉剩餘預算金額</span><span class="sxs-lookup"><span data-stu-id="fe7b5-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="fe7b5-119">處理剩餘預算金額時，您可以在總帳中為您要結轉的金額建立交易。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="fe7b5-120">若要建立總帳交易，請完成[結轉預算金額並建立總帳交易](#carry-forward)一節中的步驟。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="fe7b5-121">結轉的預算金額會轉移至 **預測模型** 頁面中選取做為結轉預測模型的預測模型。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="fe7b5-122">結轉預算金額並建立總帳交易</span><span class="sxs-lookup"><span data-stu-id="fe7b5-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="fe7b5-123">選取 **專案管理與會計** > **定期** > **預算** > **結轉預算**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="fe7b5-124">在 **專案預算結轉程序** 頁面上，選取 **年終**，然後啟用 **結轉剩餘專案預算金額** 和 **在總帳中建立預算登記分錄**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="fe7b5-125">在 **參數** 索引標籤的 **專案參數** 欄位群組中，選取下列各項：</span><span class="sxs-lookup"><span data-stu-id="fe7b5-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="fe7b5-126">**專案預算年度**：選取您要檢視剩餘預算金額的會計年度開始日期。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="fe7b5-127">**損益**：在總帳中建立損益交易。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="fe7b5-128">**WIP**：在總帳中建立進行中工作 (WIP) 交易。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="fe7b5-129">**薪資**：在總帳中建立薪資分攤交易。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="fe7b5-130">在 **總帳** 欄位群組中，提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="fe7b5-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="fe7b5-131">在 **開始會計年度** 欄位中，選取您要轉移專案的剩餘預算金額所到的會計年度。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="fe7b5-132">預設值是 **專案預算年度** 欄位值之後的一年。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="fe7b5-133">在 **結轉期間** 欄位中，選取您要在總帳中建立預算登記詳細資料的期間。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="fe7b5-134">這通常是開始會計年度中的第一個期間。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="fe7b5-135">在 **複製來源/目標** 欄位群組中，提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="fe7b5-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="fe7b5-136">在 **來源預測模型** 欄位中，選取與您要轉移之專案剩餘預算金額相關聯的專案預算預測模型。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="fe7b5-137">在 **目標總帳預測模型** 欄位中，選取與您要轉移至總帳之剩餘預算金額相關聯的總帳預算模型。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="fe7b5-138">選取 **轉移銷售貨幣**，以使用您轉移專案預算金額時所建立之總帳交易的專案銷售貨幣。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="fe7b5-139">未選取此選項時，交易會使用會計貨幣。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="fe7b5-140">選取 **顯示零剩餘** 以包含沒有剩餘預算金額但符合您於下方窗格顯示專案中所選之其他準則的專案。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="fe7b5-141">在 **選取預算** 索引標籤上，選取 **擷取所有預算** 以載入所有符合您所選準則的預算。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="fe7b5-142">如果您想要設計會在窗格中載入特定一組專案預算的資料庫查詢，請選取 **擷取選取的預算**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="fe7b5-143">對於每個您要處理的專案，選取位於專案該行開頭的選項。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="fe7b5-144">若要選取全部或大部分專案，請選取頂端左上角的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="fe7b5-145">若要排除任何專案不予處理，請清除該專案的核取記號。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="fe7b5-146">若要將所選專案的剩餘預算金額轉移至選取的會計年度，並在總帳中建立預算登記詳細資料，請選取 **程序**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="fe7b5-147">結轉預算金額但不建立總帳交易</span><span class="sxs-lookup"><span data-stu-id="fe7b5-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="fe7b5-148">移至 **專案管理與會計** > **定期** > **預算** > **結轉預算**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="fe7b5-149">在 **專案預算結轉程序** 頁面的 **年終選項** 欄位中上，選取 **結轉剩餘專案預算金額**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="fe7b5-150">在 **參數** 群組的 **專案預算年度** 欄位中，選取您要檢視剩餘預算金額的會計年度。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="fe7b5-151">在 **複製來源/目標** 群組中，提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="fe7b5-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="fe7b5-152">在 **來源預測模型** 欄位中，選取與您要轉移之專案剩餘預算金額相關聯的專案預算預測模型。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="fe7b5-153">選取 **顯示零剩餘**，以包含沒有剩餘預算但符合您所選其他準則的專案。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="fe7b5-154">在 **選取預算** 群組中，選取 **擷取所有預算** 以載入所有符合您所選準則的預算。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="fe7b5-155">若要設計會在窗格中載入特定一組專案預算的資料庫查詢，請選取 **擷取選取的預算**。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="fe7b5-156">對於每個您要處理的專案，選取位於專案該行開頭的選項。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="fe7b5-157">選取 **程序**，將所選專案的剩餘預算金額轉移至選取的會計年度。</span><span class="sxs-lookup"><span data-stu-id="fe7b5-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]