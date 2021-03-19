---
title: 管理專案發票提案
description: 本主題提供有關使用資源/非庫存型案例適用的 Project Operations 處理客戶面向發票的詳細資料。
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4e663a9a0ca5b197e556d8c36233ab25affda876
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275843"
---
# <a name="manage-project-invoice-proposals"></a><span data-ttu-id="a9362-103">管理專案發票提案</span><span class="sxs-lookup"><span data-stu-id="a9362-103">Manage project invoice proposals</span></span>

<span data-ttu-id="a9362-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="a9362-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a9362-105">符合下列兩個條件時，您的帳務部門可以處理專案發票提案：</span><span class="sxs-lookup"><span data-stu-id="a9362-105">Project invoice proposals can be processed by your billing department when the following two conditions are met:</span></span>

  - <span data-ttu-id="a9362-106">專案經理確認 Microsoft Dataverse 中的預估發票。</span><span class="sxs-lookup"><span data-stu-id="a9362-106">The Project manager confirms the proforma invoice in Microsoft Dataverse.</span></span>
  - <span data-ttu-id="a9362-107">所有包含在預估發票中的時間和材料未開單銷售交易都是使用 Dynamics 365 **Project Operations 整合** 帳目進行過帳。</span><span class="sxs-lookup"><span data-stu-id="a9362-107">All time and material unbilled sales transactions that are included in the proforma invoice are posted using the Dynamics 365 **Project Operations Integration** journal.</span></span>

<span data-ttu-id="a9362-108">使用下列步驟，在 Dynamics 365 Finance 中完成專案發票提案。</span><span class="sxs-lookup"><span data-stu-id="a9362-108">Use the following steps to complete a project invoice proposal in Dynamics 365 Finance.</span></span>

1. <span data-ttu-id="a9362-109">檢閱時間和材料交易的計費資訊，並將 **Project Operations 整合** 帳目過帳。</span><span class="sxs-lookup"><span data-stu-id="a9362-109">Review billing information for time and material transactions and post the **Project Operations Integration** journal.</span></span>
2. <span data-ttu-id="a9362-110">檢閱固定價格帳單里程碑的計費資訊。</span><span class="sxs-lookup"><span data-stu-id="a9362-110">Review billing information for fixed price billing milestones.</span></span>
3. <span data-ttu-id="a9362-111">對專案發票提案進行審查和格式化。</span><span class="sxs-lookup"><span data-stu-id="a9362-111">Review and format a project invoice proposal.</span></span>
4. <span data-ttu-id="a9362-112">將專案發票過帳並加以列印。</span><span class="sxs-lookup"><span data-stu-id="a9362-112">Post and print project invoices.</span></span>

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a><span data-ttu-id="a9362-113">管理 Project Operations 整合帳目中的計費資訊</span><span class="sxs-lookup"><span data-stu-id="a9362-113">Manage billing information in the Project Operations Integration journal</span></span>

<span data-ttu-id="a9362-114">在 Dataverse 中建立的專案實際值會由專案會計師透過 Finance 進行審查和過帳。</span><span class="sxs-lookup"><span data-stu-id="a9362-114">Project actuals created in Dataverse are reviewed and posted in Finance by the Project accountant.</span></span> <span data-ttu-id="a9362-115">如需有關使用整合帳目的詳細資訊，請參閱 [Project Operations 中的整合帳目](../project-accounting/project-operations-integration-journal.md)。</span><span class="sxs-lookup"><span data-stu-id="a9362-115">For more information about working with the Integration journal, see [Integration journal in Project Operations](../project-accounting/project-operations-integration-journal.md).</span></span>

<span data-ttu-id="a9362-116">成本實際值與未開單銷售實際值會分別做為不同的明細項目新增至整合帳目：</span><span class="sxs-lookup"><span data-stu-id="a9362-116">Cost actuals and unbilled sales actuals are added to the Integration journal as separate lines:</span></span>

  - <span data-ttu-id="a9362-117">成本實際值上的單位成本價和成本金額會預設是源自 Dataverse 中的專案實際成本交易。</span><span class="sxs-lookup"><span data-stu-id="a9362-117">The unit cost price and cost amount on the Cost actual default from the project actual cost transaction in Dataverse.</span></span>
  - <span data-ttu-id="a9362-118">未開單銷售交易上的單位銷售價和銷售金額預設是源自 Dataverse 中的專案實際未開單銷售交易。</span><span class="sxs-lookup"><span data-stu-id="a9362-118">The unit sales price and sales amount on the Unbilled sales transaction defaults from the project actual unbilled sales transaction in Dataverse.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="a9362-119">帳單銷售稅</span><span class="sxs-lookup"><span data-stu-id="a9362-119">Billing sales tax</span></span>

<span data-ttu-id="a9362-120">帳單的銷售稅計算取決於 **Project Operations 整合** 帳目明細中未開單銷售記錄上的 **帳單銷售稅金群組** 和 **帳單項目銷售稅金群組** 欄位組合。</span><span class="sxs-lookup"><span data-stu-id="a9362-120">Sales tax calculation for billing is determined by the **Billing sales tax group** and **Billing item sales tax group** field combination on an unbilled sales record on the **Project Operations Integration** journal line.</span></span> <span data-ttu-id="a9362-121">系統會根據 **專案管理與會計參數** 頁面中 **財務** 索引標籤上的設定，來設定這些欄位值的預設值。</span><span class="sxs-lookup"><span data-stu-id="a9362-121">The system defaults these field values based on settings on the **Financials** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="a9362-122">**銷售稅金群組方法** 決定預設帳單銷售稅金群組的設定邏輯：</span><span class="sxs-lookup"><span data-stu-id="a9362-122">**Sales tax group method** determines the billing sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="a9362-123">**專案**：永遠預設使用專案中的帳單銷售稅金群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-123">**Project**: Will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="a9362-124">您可以選取 **所有專案** 頁面上的 **顯示預設會計**，來檢閱或變更專案上的預設帳單銷售稅金群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-124">You can review or change the default billing sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
  - <span data-ttu-id="a9362-125">**專案合約**：永遠預設使用專案合約中的帳單銷售稅金群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-125">**Project contract**: Will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="a9362-126">您可以選取 **專案合約** 頁面上的 **顯示預設會計**，來檢閱或變更專案合約上的預設帳單銷售稅金群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-126">You can review or change the default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
  - <span data-ttu-id="a9362-127">**客戶**：永遠預設使用客戶的帳單銷售稅金群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-127">**Customer**: Will always default the billing sales tax group from the customer.</span></span>
  - <span data-ttu-id="a9362-128">**搜尋**：將會在所有上述實體中搜尋，並選取第一個可用的值。</span><span class="sxs-lookup"><span data-stu-id="a9362-128">**Search**: Will search across all the above entities and select the first value available.</span></span> <span data-ttu-id="a9362-129">搜尋先從 **專案** 實體開始，接著是 **專案合約** 實體，最後是 **客戶** 實體。</span><span class="sxs-lookup"><span data-stu-id="a9362-129">Search starts with the **Project** entity, then the **Project contract** entity, and finally the **Customer** entity.</span></span>

- <span data-ttu-id="a9362-130">**項目銷售稅金群組方法** 決定預設帳單項目銷售稅金群組的設定邏輯：</span><span class="sxs-lookup"><span data-stu-id="a9362-130">**Item sales tax group method** determines the billing item sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="a9362-131">對於時間、費用和服務費交易類型，預設帳單項目銷售稅金群組永遠根據 **專案類別** 實體來設定。</span><span class="sxs-lookup"><span data-stu-id="a9362-131">For time, expense, and fee transaction types, the billing item sales tax group will always default from the **Project category** entity.</span></span>
  - <span data-ttu-id="a9362-132">對於物料交易類型，預設帳單項目銷售稅金群組會根據 **專案管理與會計參數** 中的 **項目銷售稅金群組方式** 設定來設定。</span><span class="sxs-lookup"><span data-stu-id="a9362-132">For material transaction types, the billing item sales tax group defaults based on the **Item sales tax group method** setting in **Project management and accounting parameters**.</span></span> <span data-ttu-id="a9362-133">項目銷售稅金群組的項目編號預設是源自 **發行的產品** 實體。</span><span class="sxs-lookup"><span data-stu-id="a9362-133">The item number defaults the item sales tax group from the **Released product** entity.</span></span> <span data-ttu-id="a9362-134">項目銷售稅金群組的類別預設是源自 **專案類別** 實體。</span><span class="sxs-lookup"><span data-stu-id="a9362-134">The category defaults the item sales tax group from the **Project category** entity.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="a9362-135">財務維度</span><span class="sxs-lookup"><span data-stu-id="a9362-135">Financial dimensions</span></span>

<span data-ttu-id="a9362-136">**Project Operations 整合** 帳目中未開單銷售記錄的財務維度預設是源自 **專案** 實際。</span><span class="sxs-lookup"><span data-stu-id="a9362-136">The financial dimensions for unbilled sales records in the **Project Operations Integration** journal default from the **Project** entity.</span></span> <span data-ttu-id="a9362-137">您可以選取 **分配金額** 來審查和調整財務維度。</span><span class="sxs-lookup"><span data-stu-id="a9362-137">Financial dimensions can be reviewed and adjusted by selecting **Distribute Amounts**.</span></span> <span data-ttu-id="a9362-138">如果您需要在整合帳目過帳後但在確認預估發票前變更未開單銷售記錄的財務維度，請移至 **所有專案** > **管理** > **已過帳的交易**、選取交易，然後選取 **程序** > **調整會計**。</span><span class="sxs-lookup"><span data-stu-id="a9362-138">If you need to change the financial dimensions of the unbilled sales record after the Integration journal is posted but before the Proforma invoice is confirmed, go to **All Projects** > **Manage** > **Posted transactions**, select the transaction, and then select **Process** > **Adjust accounting**.</span></span>

### <a name="exchange-rates"></a><span data-ttu-id="a9362-139">匯率</span><span class="sxs-lookup"><span data-stu-id="a9362-139">Exchange rates</span></span>

<span data-ttu-id="a9362-140">Dataverse 中的未開單交易貨幣會在 Finance 中用作交易貨幣，並使用 Finance 中定義的匯率轉換為公司的會計貨幣。</span><span class="sxs-lookup"><span data-stu-id="a9362-140">Unbilled transaction currency in Dataverse is used as transaction currency in Finance and converted to company's accounting currency using exchange rates defined in Finance.</span></span>


## <a name="manage-the-financial-attributes-of-billing-milestones"></a><span data-ttu-id="a9362-141">管理帳單里程碑的財務屬性</span><span class="sxs-lookup"><span data-stu-id="a9362-141">Manage the financial attributes of billing milestones</span></span> 

<span data-ttu-id="a9362-142">使用固定價格帳務方式的專案合約服務內容是透過[固定價格里程碑](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line)來開立單票。</span><span class="sxs-lookup"><span data-stu-id="a9362-142">Project contract lines using the fixed price billing method are invoiced through [Fixed price milestones](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line).</span></span> <span data-ttu-id="a9362-143">專案會計師可以移至 **專案管理與會計** > **所有專案** > **管理** > **賖帳交易**，對 Finance 中的帳單里程碑進行審查。</span><span class="sxs-lookup"><span data-stu-id="a9362-143">The Project accountant can review billing milestones in Finance by going to **Project management and accounting** > **All projects** > **Manage** > **On-account transactions**.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="a9362-144">帳單銷售稅</span><span class="sxs-lookup"><span data-stu-id="a9362-144">Billing sales tax</span></span>

<span data-ttu-id="a9362-145">在 Dataverse 中建立新的帳單里程碑時，**銷售稅金群組** 及 **項目銷售稅金群組** 值預設是源自這些設定。</span><span class="sxs-lookup"><span data-stu-id="a9362-145">The **Sales tax group** and **Item sales tax group**  values default from the settings when a new billing milestone is created in Dataverse.</span></span> <span data-ttu-id="a9362-146">系統會根據 **專案管理與會計參數** 頁面中 **財務** 索引標籤上的設定，來設定這些欄位的預設值。</span><span class="sxs-lookup"><span data-stu-id="a9362-146">The system defaults the values to these fields based on settings on the **Financial** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="a9362-147">**銷售稅金群組方法** 決定設定預設 **帳單銷售稅金群組** 的邏輯：</span><span class="sxs-lookup"><span data-stu-id="a9362-147">**Sales tax group method** determines the defaulting logic of the **Billing sales tax group**:</span></span>

    - <span data-ttu-id="a9362-148">**專案** 永遠預設使用專案中的帳單銷售稅金群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-148">**Project** will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="a9362-149">您可以選取 **所有專案** 頁面上的 **顯示預設會計**，來檢閱或變更專案上的預設銷售稅金群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-149">You can review or change the default sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
    - <span data-ttu-id="a9362-150">**專案合約** 永遠預設使用專案合約中的帳單銷售稅金群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-150">**Project contract** will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="a9362-151">您可以選取 **專案合約** 頁面上的 **顯示預設會計**，來檢閱或變更專案合約上的預設帳單銷售稅金群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-151">You can review or change default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
    - <span data-ttu-id="a9362-152">**客戶** 永遠預設使用客戶的帳單銷售稅金群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-152">**Customer** will always default to the billing sales tax group from the customer.</span></span>
    - <span data-ttu-id="a9362-153">**搜尋** 將會在此清單所有的實體中搜尋，並選取第一個可用的值。</span><span class="sxs-lookup"><span data-stu-id="a9362-153">**Search** will search across all the entities in this list and select the first value available.</span></span> <span data-ttu-id="a9362-154">搜尋先從 **專案** 實體開始，接著是 **專案合約** 實體，然後是 **客戶** 實體。</span><span class="sxs-lookup"><span data-stu-id="a9362-154">Search starts with the **Project** entity, then the **Project contract** entity, and then the **Customer** entity.</span></span>

- <span data-ttu-id="a9362-155">**固定價格里程碑項目銷售稅金群組** 會用來設定 **項目銷售稅金群組** 欄位的預設值。</span><span class="sxs-lookup"><span data-stu-id="a9362-155">**Fixed price milestone item sales tax group** is used to default the value to the **Item sales tax group** field.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="a9362-156">財務維度</span><span class="sxs-lookup"><span data-stu-id="a9362-156">Financial dimensions</span></span>

<span data-ttu-id="a9362-157">固定價格帳單里程碑的預設財務維度是在專案合約服務內容中設定。</span><span class="sxs-lookup"><span data-stu-id="a9362-157">Default financial dimensions for the fixed price billing milestone are set on Project contract lines.</span></span> <span data-ttu-id="a9362-158">移至 **專案合約** > **顯示預設會計**，並在 **合約服務內容** 索引標籤上，選取 **價格合約服務內容**，然後設定您要用來做為預設值的財務維度值。</span><span class="sxs-lookup"><span data-stu-id="a9362-158">Go to **Project contracts** > **Show default accounting** and on the **Contract lines** tab, select **price contract line**, then set the financial dimension values that you want to use as the default.</span></span>

<span data-ttu-id="a9362-159">專案會計師直到建立專案發票提案之前，都可以編輯發票里程碑上的銷售稅和財務維度資訊。</span><span class="sxs-lookup"><span data-stu-id="a9362-159">The Project accountant can edit the sales tax and financial dimensions information on invoice milestones up until the Project invoice proposal is created.</span></span>


## <a name="create-project-invoice-proposals"></a><span data-ttu-id="a9362-160">建立專案發票提案</span><span class="sxs-lookup"><span data-stu-id="a9362-160">Create project invoice proposals</span></span>

<span data-ttu-id="a9362-161">您可以移至 **專案發票** > **專案發票提案**，在 **專案管理與會計** 模組中審查專案發票提案。</span><span class="sxs-lookup"><span data-stu-id="a9362-161">Project invoice proposals can be reviewed in the **Project management and accounting** module by going to **Project invoices** > **Project invoice proposals**.</span></span>

<span data-ttu-id="a9362-162">在 Dataverse 中確認預估發票時，系統會在 Finance 中建立專案發票提案標題。</span><span class="sxs-lookup"><span data-stu-id="a9362-162">The Project invoice proposal header is created in Finance when the Proforma invoice is confirmed in Dataverse.</span></span> <span data-ttu-id="a9362-163">為了便於對帳，系統會將 Finance 中的專案發票提案編號設定為與 Dataverse 中的預估發票識別碼相同的數字。</span><span class="sxs-lookup"><span data-stu-id="a9362-163">For easier reconciliation, the system sets the Project invoice proposal number in Finance to the same number as the Proforma invoice ID in Dataverse.</span></span> <span data-ttu-id="a9362-164">由於預估發票不一定是依照其建立順序進行確認，因此 Finance 中的專案發票提案編號序列必須允許對較低和較高的編號進行變更。</span><span class="sxs-lookup"><span data-stu-id="a9362-164">Because Proforma invoices are not necessarily confirmed in the same order they are created, the Project invoice proposal number sequence in Finance must allow for changes to lower and higher numbers.</span></span> <span data-ttu-id="a9362-165">使用下列步驟來設定編號序列：</span><span class="sxs-lookup"><span data-stu-id="a9362-165">Configure number sequences using the following steps:</span></span>

1. <span data-ttu-id="a9362-166">在 Finance 中，移至 **組織管理** > **編號序列** > **編號序列**。</span><span class="sxs-lookup"><span data-stu-id="a9362-166">In Finance, go to **Organization Administration** > **Number sequences** > **Number sequences**.</span></span>
2. <span data-ttu-id="a9362-167">在 **區域** 篩選中，選取 **專案**。</span><span class="sxs-lookup"><span data-stu-id="a9362-167">In the **Area** filter, select **Projects**.</span></span>
3. <span data-ttu-id="a9362-168">在 **參考** 篩選中，選取 **發票提案**。</span><span class="sxs-lookup"><span data-stu-id="a9362-168">In the **Reference** filter, select **Invoice proposal**.</span></span>
4. <span data-ttu-id="a9362-169">使用 **公司** 欄位來篩選每個已啟用 Project Operations Dataverse 整合的法律實體。</span><span class="sxs-lookup"><span data-stu-id="a9362-169">Use the **Company** field to filter each legal entity with Project Operations Dataverse integration enabled.</span></span>
5. <span data-ttu-id="a9362-170">開啟 **編號序列詳細資料**，並在 **一般** 索引標籤上進行下列設定：</span><span class="sxs-lookup"><span data-stu-id="a9362-170">Open **Number Sequence details** and on the **General** tab set:</span></span>

    - <span data-ttu-id="a9362-171">**允許使用者變更：至較低編號** = **是**</span><span class="sxs-lookup"><span data-stu-id="a9362-171">**Allow user changes: To a lower number** = **Yes**</span></span>
    - <span data-ttu-id="a9362-172">**允許使用者變更：至較高編號** = **是**</span><span class="sxs-lookup"><span data-stu-id="a9362-172">**Allow user changes: To a higher number** = **Yes**</span></span>

<span data-ttu-id="a9362-173">專案發票提案明細是系統使用週期程序 **從暫存資料表匯入** (**專案管理與會計** > **定期** > **Project Operations 整合** > **從暫存資料表匯入**) 所新增。</span><span class="sxs-lookup"><span data-stu-id="a9362-173">Project invoice proposal lines are added by the system using the periodic process **Import from staging table** (**Project management and accounting** > **Periodic** > **Project Operations integration** > **Import from staging table**).</span></span> <span data-ttu-id="a9362-174">您可以使用手動方式或定期排程來執行此程序。</span><span class="sxs-lookup"><span data-stu-id="a9362-174">This process can be run manually or by using a periodic schedule.</span></span> <span data-ttu-id="a9362-175">在所有明細都已準備好開立發票之前，系統不會將明細加入至發票提案文件。</span><span class="sxs-lookup"><span data-stu-id="a9362-175">The system won't add lines to the invoice proposal document until all the lines are ready to be invoiced.</span></span> <span data-ttu-id="a9362-176">時間和材料交易只有在使用 **Project Operations 整合** 帳目過帳時，才算已準備好開立發票。</span><span class="sxs-lookup"><span data-stu-id="a9362-176">Time and material transactions are ready to be invoiced only when they are posted using the **Project Operations Integration** journal.</span></span>

## <a name="format-and-print-invoice-proposals"></a><span data-ttu-id="a9362-177">格式化並列印發票提案</span><span class="sxs-lookup"><span data-stu-id="a9362-177">Format and print invoice proposals</span></span>

<span data-ttu-id="a9362-178">專案會計師可以使用 **格式化發票提案** 頁面和列印管理功能來自訂專案發票列印成品。</span><span class="sxs-lookup"><span data-stu-id="a9362-178">The Project accountant can customize a project invoice printout by using the **Format invoice proposal** page and print management capabilities.</span></span>

### <a name="format-invoice-proposals"></a><span data-ttu-id="a9362-179">格式化發票提案</span><span class="sxs-lookup"><span data-stu-id="a9362-179">Format invoice proposals</span></span>

<span data-ttu-id="a9362-180">**格式化發票提案** 頁面可讓自訂群組交易顯示在客戶專案發票中。</span><span class="sxs-lookup"><span data-stu-id="a9362-180">The **Format invoice proposals** page allows custom grouping transactions to display in the customer project invoice.</span></span>

1. <span data-ttu-id="a9362-181">在 **專案發票提案** 頁面上，選取 **列印** > **格式化發票提案**。</span><span class="sxs-lookup"><span data-stu-id="a9362-181">On the **Project invoice proposal** page, select **Print** > **Format invoice proposal**.</span></span>
2. <span data-ttu-id="a9362-182">選取 **新增**，為專案發票列印成品建立新的群組。</span><span class="sxs-lookup"><span data-stu-id="a9362-182">Select **New** to create a new grouping for the Project invoice printout.</span></span>
3. <span data-ttu-id="a9362-183">在 **詳細資料/摘要** 欄位中，選取此群組的選項：</span><span class="sxs-lookup"><span data-stu-id="a9362-183">In the **Detail/Summary** field, select options for this grouping:</span></span>

    - <span data-ttu-id="a9362-184">選取 **詳細資料** 以列印客戶發票的交易詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a9362-184">Select **Detail** to print the transaction details of the customer invoice.</span></span>
    - <span data-ttu-id="a9362-185">選取 **摘要** 以列印客戶發票的交易摘要。</span><span class="sxs-lookup"><span data-stu-id="a9362-185">Select **Summary** to print the transaction summary of the customer invoice.</span></span>

> [!NOTE]
> <span data-ttu-id="a9362-186">**格式化發票提案** 頁面上的 **詳細資料/摘要** 欄位選取項目會覆寫在 **發票提案** 頁面上的 **發票格式** 欄位中選取的選項，以列印詳細的發票或摘要的發票。</span><span class="sxs-lookup"><span data-stu-id="a9362-186">The selection in the **Detail/Summary** field on the **Format invoice proposal** page overrides the option selected in the **Invoice format** field on the **Invoice proposals** page to print a detailed invoice or a summarized invoice.</span></span>

- <span data-ttu-id="a9362-187">在 **可用交易** 索引標籤中選取要包含在此區段的交易明細，並選取 **包含交易** 將這些交易移到 **選取的交易**。</span><span class="sxs-lookup"><span data-stu-id="a9362-187">Select the transaction lines to include in this section on the **Available transactions** tab and select **Include transactions** to move them to the **Selected transactions** tab.</span></span>
- <span data-ttu-id="a9362-188">選取 **上移** 和 **下移** 來變更區段的順序。</span><span class="sxs-lookup"><span data-stu-id="a9362-188">Select **Move up** and **Move down** to change the order of the sections.</span></span>
- <span data-ttu-id="a9362-189">選取 **預覽列印** 以預覽格式化的發票。</span><span class="sxs-lookup"><span data-stu-id="a9362-189">Select **Print preview** to preview formatted invoice.</span></span>

### <a name="print-management"></a><span data-ttu-id="a9362-190">列印管理</span><span class="sxs-lookup"><span data-stu-id="a9362-190">Print management</span></span>

<span data-ttu-id="a9362-191">列印管理使用不同的報表檔案來列印、指定目的地，以及自訂發票的頁尾文字。</span><span class="sxs-lookup"><span data-stu-id="a9362-191">Print management uses different report files to print, specify destinations, and customize footer text for the invoice.</span></span> <span data-ttu-id="a9362-192">您可以在模組層級設定列印管理，但是可以針對特定客戶、合約或發票提案覆寫這些設定。</span><span class="sxs-lookup"><span data-stu-id="a9362-192">Print management can be set up at the module level, however these settings can be overridden for a specific customer, contract, or invoice proposal.</span></span> <span data-ttu-id="a9362-193">若要在 **專案發票提案** 頁面上存取此功能，請選取 **列印** > **列印管理**。</span><span class="sxs-lookup"><span data-stu-id="a9362-193">To access this function on the **Project invoice proposal** page, select **Print** > **Print management**.</span></span>

<span data-ttu-id="a9362-194">列印管理安裝程式會顯示為樹狀檢視，其中每個節點層級都會顯示要調整的可用文件。</span><span class="sxs-lookup"><span data-stu-id="a9362-194">Print management setup is displayed as a tree view, where each node level displays the available documents to adjust.</span></span> <span data-ttu-id="a9362-195">您可以在模組、客戶、合約或發票提案文件層級指派自訂列印成品。</span><span class="sxs-lookup"><span data-stu-id="a9362-195">You can assign custom printouts at the module, customer, contract, or invoice proposal document level.</span></span> <span data-ttu-id="a9362-196">若要修改原始檔案列印成品，請展開所需的節點，然後選取 **原始項目**。</span><span class="sxs-lookup"><span data-stu-id="a9362-196">To modify the original document printout, expand the desired node and select **Original item**.</span></span> <span data-ttu-id="a9362-197">在 **報表格式** 欄位中，選取要用於列印的報表格式。</span><span class="sxs-lookup"><span data-stu-id="a9362-197">In the **Report format** field, select the report format to be used for printing.</span></span> <span data-ttu-id="a9362-198">您可以透過[商務文件管理架構](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management)來使用自訂報表格式。</span><span class="sxs-lookup"><span data-stu-id="a9362-198">You can use custom report formats by using [Business Document Management framework](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).</span></span>

## <a name="post-invoice-proposals"></a><span data-ttu-id="a9362-199">將發票提案過帳</span><span class="sxs-lookup"><span data-stu-id="a9362-199">Post invoice proposals</span></span>

<span data-ttu-id="a9362-200">審查並編輯過發票之後，而且您也滿意發票提案明細時，請檢查發票總額和銷售稅。</span><span class="sxs-lookup"><span data-stu-id="a9362-200">After the invoice has been reviewed and edited, and the invoice proposal lines are satisfactory, check the invoice totals and sales tax.</span></span> <span data-ttu-id="a9362-201">在 **詳細資料** 群組中，選取 **總計**，然後選 **過帳** 以將發票過帳。</span><span class="sxs-lookup"><span data-stu-id="a9362-201">In the **Details** group, select **Totals** and then select **Post** to post the invoice.</span></span>

<span data-ttu-id="a9362-202">若要在過帳前檢視發票，請清除 **過帳** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="a9362-202">To view the invoice before posting, clear the **Posting** check box.</span></span> <span data-ttu-id="a9362-203">發票上會列印 **估價**，表示這是範例發票。</span><span class="sxs-lookup"><span data-stu-id="a9362-203">**Pro forma** will be printed on the invoice to signify it is a sample invoice.</span></span> <span data-ttu-id="a9362-204">若要列印發票，請選取 **列印發票** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="a9362-204">To print the invoice, select the **Print invoice** check box.</span></span>

<span data-ttu-id="a9362-205">除了 **發票提案** 頁面之外，還可以執行定期作業 **過帳發票提案** 來對發票提案進行過帳。</span><span class="sxs-lookup"><span data-stu-id="a9362-205">In addition to the **Invoice proposal** page, invoice proposals can also be posted by running the periodic job, **Post invoice proposals**.</span></span> <span data-ttu-id="a9362-206">若要尋找此作業，請移至 **專案管理與會計** > **定期** > **專案發票** > **過帳發票提案**。</span><span class="sxs-lookup"><span data-stu-id="a9362-206">To find this job, go to **Project management and accounting** > **Periodic** > **Project invoices** > **Post invoice proposals**.</span></span>

<span data-ttu-id="a9362-207">此頁面會顯示所有已準備好進行過帳的發票提案。</span><span class="sxs-lookup"><span data-stu-id="a9362-207">This page shows all the invoice proposals that are ready for posting.</span></span> <span data-ttu-id="a9362-208">您可以選取 **批次** 來排定發票提案過帳。</span><span class="sxs-lookup"><span data-stu-id="a9362-208">You can schedule posting invoice proposals by selecting **Batch**.</span></span> <span data-ttu-id="a9362-209">將 **批次處理參數** 設定為 **是**，然後選取 **週期** 以設定批次處理的週期。</span><span class="sxs-lookup"><span data-stu-id="a9362-209">Set the **Batch processing parameter** to **Yes** and set the recurrence of batch processing by selecting **Recurrence**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]