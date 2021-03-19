---
title: 估計值
description: 本主題提供有關 Dynamics 365 Project Service Automation 中估計值的資訊。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
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
ms.openlocfilehash: 1596964edb39f20d1dc26c7a61cb9fb294d1f0ba
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284483"
---
# <a name="estimates"></a><span data-ttu-id="383f4-103">估計值</span><span class="sxs-lookup"><span data-stu-id="383f4-103">Estimates</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="383f4-104">在專案型報價上，您可以使用報價明細詳細資料實體來估計交付專案所需的工作。</span><span class="sxs-lookup"><span data-stu-id="383f4-104">On a project-based quote, you can use the Quote line detail entity to estimate the work that is required to deliver a project.</span></span> <span data-ttu-id="383f4-105">然後就可以與客戶分享該估計值。</span><span class="sxs-lookup"><span data-stu-id="383f4-105">You can then share that estimate with the customer.</span></span>

<span data-ttu-id="383f4-106">專案型報價單明細不必有任何報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="383f4-106">Project-based quote lines don't have to have any quote line details.</span></span> <span data-ttu-id="383f4-107">或者，可以有許多報價明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="383f4-107">Alternatively, they can have many quote line details.</span></span> <span data-ttu-id="383f4-108">報價明細詳細資料可用來估計時間、費用或服務費。</span><span class="sxs-lookup"><span data-stu-id="383f4-108">Quote line details are used to estimate time, expenses, or fees.</span></span> <span data-ttu-id="383f4-109">PSA 不允許估計報價明細詳細資料上的材料。</span><span class="sxs-lookup"><span data-stu-id="383f4-109">PSA doesn't allow for material estimates on quote line details.</span></span> <span data-ttu-id="383f4-110">這些稱為交易分類。</span><span class="sxs-lookup"><span data-stu-id="383f4-110">These are called transaction classes.</span></span> <span data-ttu-id="383f4-111">估計的稅額也可以在交易分類上輸入。</span><span class="sxs-lookup"><span data-stu-id="383f4-111">Estimated tax amounts can also be entered on a transaction class.</span></span>

<span data-ttu-id="383f4-112">除了交易分類之外，報價明細詳細資料還有一種交易類型。</span><span class="sxs-lookup"><span data-stu-id="383f4-112">In addition to transaction classes, quote line details have a transaction type.</span></span> <span data-ttu-id="383f4-113">PSA 支援報價明細詳細資料的兩種交易類型：**成本** 和 **專案合約**。</span><span class="sxs-lookup"><span data-stu-id="383f4-113">PSA support two transaction types for quote line details: **Cost** and **Project Contract**.</span></span>

## <a name="estimate-by-using-a-contract"></a><span data-ttu-id="383f4-114">使用合約進行估計</span><span class="sxs-lookup"><span data-stu-id="383f4-114">Estimate by using a contract</span></span>

<span data-ttu-id="383f4-115">如果建立專案型合約時使用了 PSA 報價，則會將報價中針對每個報價明細所做的估計複製到專案合約。</span><span class="sxs-lookup"><span data-stu-id="383f4-115">If you used a PSA quote when you created a project-based contract, the estimate that you did for each quote line on the quote is copied to the project contract.</span></span> <span data-ttu-id="383f4-116">專案合約的結構就像專案報價的結構一樣，也有明細、明細詳細資料和發票清單。</span><span class="sxs-lookup"><span data-stu-id="383f4-116">The structure of a project contract is like the structure of project quote that has lines, line details, and invoice schedules.</span></span>

<span data-ttu-id="383f4-117">評估可以直接在專案合約中完成，就像在專案報價中一樣。</span><span class="sxs-lookup"><span data-stu-id="383f4-117">Estimates can be done directly in a project contract, as in a project quote.</span></span> <span data-ttu-id="383f4-118">就專案報價而言，估計是使用合約服務內容和合約服務內容詳細資料來完成。</span><span class="sxs-lookup"><span data-stu-id="383f4-118">For a project quotation, the estimate is done by using contract lines and contract line details.</span></span> <span data-ttu-id="383f4-119">合約服務內容詳細資料也可以從使用由下而上估計方式所建立的專案計劃中產生。</span><span class="sxs-lookup"><span data-stu-id="383f4-119">Contract line details can also be generated from a project plan that was created by using the bottom-up estimate approach.</span></span>

<span data-ttu-id="383f4-120">合約服務內容詳細資料可用來估計時間、費用或服務費。</span><span class="sxs-lookup"><span data-stu-id="383f4-120">Contract line details can be used to estimate time, expenses, or fees.</span></span> <span data-ttu-id="383f4-121">估計的稅額也可以在合約服務內容詳細資料上輸入。</span><span class="sxs-lookup"><span data-stu-id="383f4-121">Estimated tax amounts can also be entered on a contract line detail.</span></span>

<span data-ttu-id="383f4-122">PSA 不允許估計合約服務內容詳細資料上的材料。</span><span class="sxs-lookup"><span data-stu-id="383f4-122">PSA doesn't allow for material estimates on contract line details.</span></span>

<span data-ttu-id="383f4-123">專案合約支援的程序是發票建立與確認作業。</span><span class="sxs-lookup"><span data-stu-id="383f4-123">The processes that are supported on a project contract are invoice creation and confirmation.</span></span> <span data-ttu-id="383f4-124">發票建立作業會建立包含目前日期以前所有未開單銷售之專案型發票的草稿。</span><span class="sxs-lookup"><span data-stu-id="383f4-124">Invoice creation creates a draft of a project-based invoice that includes all unbilled sales actuals until the current date.</span></span>

<span data-ttu-id="383f4-125">確認作業會讓合約變成唯讀，並將其狀態從 **草稿** 變更為 **已確認**。</span><span class="sxs-lookup"><span data-stu-id="383f4-125">Confirmation makes the contract read-only and changes its status from **Draft** to **Confirmed**.</span></span> <span data-ttu-id="383f4-126">執行此動作之後，您無法加以復原。</span><span class="sxs-lookup"><span data-stu-id="383f4-126">After you take this action, you can't undo it.</span></span> <span data-ttu-id="383f4-127">因為此動作為永久性，最佳做法是讓合約保持在 **草稿** 狀態。</span><span class="sxs-lookup"><span data-stu-id="383f4-127">Because this action is permanent, it's a best practice to keep the contract in a **Draft** status.</span></span>

<span data-ttu-id="383f4-128">草稿合約與已確認合約之間的區別在於其狀態，以及在於草稿合約可編輯但已確認合約卻不能編輯的事實。</span><span class="sxs-lookup"><span data-stu-id="383f4-128">The only differences between draft contracts and confirmed contracts are their status and the fact that draft contracts can be edited whereas confirmed contracts can't.</span></span> <span data-ttu-id="383f4-129">在草稿合約和已確認合約上都可以執行發票建立作業和追蹤實際值作業。</span><span class="sxs-lookup"><span data-stu-id="383f4-129">Invoice creation and tracking actuals can be done on both draft contracts and confirmed contracts.</span></span>

<span data-ttu-id="383f4-130">PSA 不支援變更合約或專案上的訂單。</span><span class="sxs-lookup"><span data-stu-id="383f4-130">PSA doesn't support change orders on contracts or projects.</span></span>

## <a name="estimating-projects"></a><span data-ttu-id="383f4-131">估計專案</span><span class="sxs-lookup"><span data-stu-id="383f4-131">Estimating projects</span></span>

<span data-ttu-id="383f4-132">您可以估計專案的時間和費用。</span><span class="sxs-lookup"><span data-stu-id="383f4-132">You can estimate time and expenses on projects.</span></span> <span data-ttu-id="383f4-133">PSA 不允許估計專案上的材料或服務費。</span><span class="sxs-lookup"><span data-stu-id="383f4-133">PSA doesn't allow for estimates of materials or fees on projects.</span></span>

<span data-ttu-id="383f4-134">時間估計會在您建立工作時產生，並且可識別執行工作所需一般資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="383f4-134">Time estimates are generated when you create a task and identify the attributes of a generic resource that is required to perform the task.</span></span> <span data-ttu-id="383f4-135">時間估計值是從排程工作產生。</span><span class="sxs-lookup"><span data-stu-id="383f4-135">Time estimates are generated from schedule tasks.</span></span> <span data-ttu-id="383f4-136">如果在排程的內容範圍外建立一般團隊成員，就不會建立時間估計值。</span><span class="sxs-lookup"><span data-stu-id="383f4-136">Time estimates aren't created if you create generic team members outside the context of the schedule.</span></span>

<span data-ttu-id="383f4-137">您可以在 **估計值** 頁面的網格中輸入費用估計值。</span><span class="sxs-lookup"><span data-stu-id="383f4-137">Expense estimates are entered in the grid on the **Estimates** page.</span></span>

## <a name="understanding-estimation"></a><span data-ttu-id="383f4-138">了解估計值</span><span class="sxs-lookup"><span data-stu-id="383f4-138">Understanding estimation</span></span>

<span data-ttu-id="383f4-139">使用下表做為了解估計階段中商務規則的指南。</span><span class="sxs-lookup"><span data-stu-id="383f4-139">Use the following table as a guide for understanding the business logic in the estimation phase.</span></span>

| <span data-ttu-id="383f4-140">情況</span><span class="sxs-lookup"><span data-stu-id="383f4-140">Scenario</span></span>                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="383f4-141">實體記錄</span><span class="sxs-lookup"><span data-stu-id="383f4-141">Entity record</span></span>                                                                                                                                                                                                       | <span data-ttu-id="383f4-142">交易類型</span><span class="sxs-lookup"><span data-stu-id="383f4-142">Transaction Type</span></span> | <span data-ttu-id="383f4-143">交易分類</span><span class="sxs-lookup"><span data-stu-id="383f4-143">Transaction Class</span></span> | <span data-ttu-id="383f4-144">其他資訊</span><span class="sxs-lookup"><span data-stu-id="383f4-144">Additional information</span></span>                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="383f4-145">當您需要估計報價的時間銷售值時：</span><span class="sxs-lookup"><span data-stu-id="383f4-145">When you need to estimate the sales value of time on a quote</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="383f4-146">報價明細詳細資料 (QLD) 記錄已建立</span><span class="sxs-lookup"><span data-stu-id="383f4-146">Quote line detail (QLD) record is created</span></span>                                                                                                                                                                               | <span data-ttu-id="383f4-147">專案合約</span><span class="sxs-lookup"><span data-stu-id="383f4-147">Project contract</span></span> | <span data-ttu-id="383f4-148">時間</span><span class="sxs-lookup"><span data-stu-id="383f4-148">Time</span></span>        | <span data-ttu-id="383f4-149">銷售面 QLD 列上的 [交易來源] 欄位會參考成本面 QLD</span><span class="sxs-lookup"><span data-stu-id="383f4-149">Transaction origin field on the sales side QLD row references the Cost side QLD</span></span> |
|                                                                                                                                                                                                                                                                                     | <span data-ttu-id="383f4-150">第二個 QLD 記錄是由系統建立，用來儲存對應成本值。</span><span class="sxs-lookup"><span data-stu-id="383f4-150">A second QLD record is created by the system to store the corresponding cost values.</span></span> <span data-ttu-id="383f4-151">系統會從銷售 QLD 將所有的非金額欄位都複製到成本 QLD。</span><span class="sxs-lookup"><span data-stu-id="383f4-151">All non-money fields are copied from the sales QLD to the Cost QLD by the system.</span></span>                                                                                                                                                                               | <span data-ttu-id="383f4-152">成本</span><span class="sxs-lookup"><span data-stu-id="383f4-152">Cost</span></span> | <span data-ttu-id="383f4-153">時間</span><span class="sxs-lookup"><span data-stu-id="383f4-153">Time</span></span>        | <span data-ttu-id="383f4-154">銷售面明細詳細資料 (QLD) 列上的 [交易來源] 欄位會參考成本面 QLD</span><span class="sxs-lookup"><span data-stu-id="383f4-154">Transaction origin field on the sales side quote line detail (QLD) row references the Cost side QLD</span></span> |
| <span data-ttu-id="383f4-155">當您需要估計合約的時間銷售值時：</span><span class="sxs-lookup"><span data-stu-id="383f4-155">When you need to estimate the sales value of time on a contract</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="383f4-156">專案合約服務內容詳細資料 (CLD) 記錄已建立</span><span class="sxs-lookup"><span data-stu-id="383f4-156">Project contract line detail (CLD) record is created</span></span>                                                                                                                                                                    | <span data-ttu-id="383f4-157">專案合約</span><span class="sxs-lookup"><span data-stu-id="383f4-157">Project Contract</span></span> | <span data-ttu-id="383f4-158">時間</span><span class="sxs-lookup"><span data-stu-id="383f4-158">Time</span></span>        | <span data-ttu-id="383f4-159">銷售面 CLD 列上的 [交易來源] 欄位會參考成本 CLD</span><span class="sxs-lookup"><span data-stu-id="383f4-159">Transaction origin field on the sales side CLD row references the cost CLD</span></span>      |
|                                                                                                                                                                                                                                                                                  | <span data-ttu-id="383f4-160">第二個 CLD 記錄是由系統建立，用來儲存對應成本值。</span><span class="sxs-lookup"><span data-stu-id="383f4-160">A second CLD record is created by the system to store the corresponding cost values.</span></span> <span data-ttu-id="383f4-161">系統會從銷售 CLD 將所有的非金額欄位都複製到成本 CLD。</span><span class="sxs-lookup"><span data-stu-id="383f4-161">All non-money fields are copied from the sales CLD to the cost CLD by the system.</span></span>                                                                                                                                                                    | <span data-ttu-id="383f4-162">成本</span><span class="sxs-lookup"><span data-stu-id="383f4-162">Cost</span></span> | <span data-ttu-id="383f4-163">時間</span><span class="sxs-lookup"><span data-stu-id="383f4-163">Time</span></span>        | <span data-ttu-id="383f4-164">銷售面 CLD 列上的 [交易來源] 欄位會參考成本 CLD</span><span class="sxs-lookup"><span data-stu-id="383f4-164">Transaction origin field on the sales side CLD row references the cost CLD</span></span>      |
| <span data-ttu-id="383f4-165">當使用者描述專案工作的資源時</span><span class="sxs-lookup"><span data-stu-id="383f4-165">When the user describes a resource on a project task</span></span>                                                                                                                                                                                                                                                                                            | <span data-ttu-id="383f4-166">使用所有必要的定價維度建立工作時，會建立用來顯示工作銷售值的估計明細記錄。</span><span class="sxs-lookup"><span data-stu-id="383f4-166">Estimate line record to show the sales value of the task is created when a task is created with all required pricing dimensions.</span></span> <span data-ttu-id="383f4-167">角色和組織單位是預設 (OOB) Project Service 定價維度</span><span class="sxs-lookup"><span data-stu-id="383f4-167">Role and organizational units are the OOB Project Service pricing dimensions</span></span> | <span data-ttu-id="383f4-168">專案合約</span><span class="sxs-lookup"><span data-stu-id="383f4-168">Project Contract</span></span> | <span data-ttu-id="383f4-169">時間</span><span class="sxs-lookup"><span data-stu-id="383f4-169">Time</span></span>        |                                                                                   |
|     | <span data-ttu-id="383f4-170">使用所有必要的定價維度建立工作時，會建立用來顯示工作成本值的估計明細記錄。</span><span class="sxs-lookup"><span data-stu-id="383f4-170">The estimate line record to show the cost value of the task is created when a task is created with all required pricing dimensions.</span></span> <span data-ttu-id="383f4-171">系統會從銷售估計明細將所有的非金額欄位都複製到成本估計明細。</span><span class="sxs-lookup"><span data-stu-id="383f4-171">All non-money fields are copied from the sales estimate line to the cost estimate line by the system.</span></span> <span data-ttu-id="383f4-172">角色和組織單位是成本及帳單費率的預設 (OOB) PSA 定價維度。</span><span class="sxs-lookup"><span data-stu-id="383f4-172">Role and organizational unit are the OOB PSA pricing dimensions for both cost and bill rates.</span></span>                                                                                                                                                                                                                | <span data-ttu-id="383f4-173">成本</span><span class="sxs-lookup"><span data-stu-id="383f4-173">Cost</span></span>             | <span data-ttu-id="383f4-174">時間</span><span class="sxs-lookup"><span data-stu-id="383f4-174">Time</span></span>           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a><span data-ttu-id="383f4-175">自訂報價明細詳細資料和合約服務內容詳細資料實體</span><span class="sxs-lookup"><span data-stu-id="383f4-175">Customizing the Quote line detail and Contract line detail entities</span></span>

<span data-ttu-id="383f4-176">如果您在報價明細詳細資料中新增自訂欄位，並且希望系統輸入欄位值做為其所建立相關成本明細的預設值時，請使用 PreOperationContractLineDetailUpdate 和 PreOperationQuoteLineDetailUpdate 外掛程式註冊工具。</span><span class="sxs-lookup"><span data-stu-id="383f4-176">If you added a custom field on the quote line detail and want the system to enter the value of the field as a default value on the related cost line that it creates, use the PreOperationContractLineDetailUpdate and PreOperationQuoteLineDetailUpdate plug-in registration tools.</span></span> <span data-ttu-id="383f4-177">變更報價明細詳細資料或合約服務內容詳細資料之後，您必須重新註冊這些外掛程式。</span><span class="sxs-lookup"><span data-stu-id="383f4-177">These plug-ins must be re-registered after the quote line detail or the contract line detail is changed.</span></span> <span data-ttu-id="383f4-178">請依照下列步驟完成此程序：</span><span class="sxs-lookup"><span data-stu-id="383f4-178">Follow these steps to complete the process.</span></span>

1. <span data-ttu-id="383f4-179">開啟 PluginRegistrationTool，並連接至您的線上執行個體。</span><span class="sxs-lookup"><span data-stu-id="383f4-179">Open PluginRegistrationTool, and connect to your online instance.</span></span>
2. <span data-ttu-id="383f4-180">選取 **搜尋**，然後搜尋要更新的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="383f4-180">Select **Search**, and search for the plug-in to update.</span></span>

    ![搜尋樹狀結構對話方塊](media/basic-guide-19.png)

3. <span data-ttu-id="383f4-182">選取外掛程式，然後選取主要頁面上的 **選取**。</span><span class="sxs-lookup"><span data-stu-id="383f4-182">Select the plug-in, and then, on the main page, select **Select**.</span></span>
4. <span data-ttu-id="383f4-183">選取要更新外掛程式的步驟、按一下滑鼠右鍵，然後選取 **更新**。</span><span class="sxs-lookup"><span data-stu-id="383f4-183">Select the step of the plug-in to update, right-click, and then select **Update**.</span></span>

    ![選取外掛程式中的步驟](media/basic-guide-20.png)

5. <span data-ttu-id="383f4-185">在 **更新現有步驟** 對話方塊的 **篩選屬性** 欄位中，選取省略符號按鈕 (**...**)：</span><span class="sxs-lookup"><span data-stu-id="383f4-185">In the **Update Existing Step** dialog box, in the **Filtering Attributes** field, select the ellipsis button (**...**):</span></span>
 
    ![[更新現有步驟] 對話方塊](media/basic-guide-21.png)

6. <span data-ttu-id="383f4-187">在 **選取屬性** 對話方塊中，選取自訂屬性的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="383f4-187">In the **Select Attributes** dialog box, select check boxes for custom attributes.</span></span>

    ![[選取屬性] 對話方塊](media/basic-guide-22.png)

7. <span data-ttu-id="383f4-189">選取 **確定** 關閉對話方塊，然後選取 **更新步驟**。</span><span class="sxs-lookup"><span data-stu-id="383f4-189">Select **OK** to close the dialog box, and then select **Update Step**.</span></span>
 
    ![[更新步驟] 按鈕](media/basic-guide-23.png)

8. <span data-ttu-id="383f4-191">對第二個外掛程式重複步驟 1 到 7。</span><span class="sxs-lookup"><span data-stu-id="383f4-191">Repeat steps 1 through 7 for the second plug-in.</span></span>
9. <span data-ttu-id="383f4-192">關閉 PluginRegistrationTool。</span><span class="sxs-lookup"><span data-stu-id="383f4-192">Close the PluginRegistrationTool.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]