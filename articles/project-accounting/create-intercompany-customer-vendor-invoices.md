---
title: 建立公司間客戶與廠商發票
description: 此主題提供有關如何建立公司間客戶與廠商發票的資訊。
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 92d08537fe0c2a1deba486974db53e7ebe1ff2d8
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948379"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a><span data-ttu-id="7e931-103">建立公司間客戶與廠商發票</span><span class="sxs-lookup"><span data-stu-id="7e931-103">Create intercompany customer and vendor invoices</span></span>

<span data-ttu-id="7e931-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7e931-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7e931-105">貸方法律實體中的專案會計為要轉移至借方實體的專案成本建立公司間客戶發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-105">A project accountant in a lending legal entity creates an intercompany customer invoice for the project costs that are being transferred to the borrowing entity.</span></span> <span data-ttu-id="7e931-106">在已核准並過帳公司間客戶發票後，貸方法律實體將公司間發票傳送給借方法律實體。</span><span class="sxs-lookup"><span data-stu-id="7e931-106">After the intercompany customer invoice is approved and posted, the lending legal entity sends the intercompany invoice to the borrowing legal entity.</span></span>

<span data-ttu-id="7e931-107">貸方法律實體的專案會計可以設定批次處理，定期產生公司間發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-107">The project accountant for the lending legal entity can set up a batch process to generate intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="7e931-108">專案會計指定準則，例如特定專案，以在批次中建立公司間發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-108">The project accountant specifies the criteria, such as specific projects, to create intercompany invoices in a batch.</span></span>

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a><span data-ttu-id="7e931-109">手動建立專案交易的公司間客戶發票</span><span class="sxs-lookup"><span data-stu-id="7e931-109">Manually create an intercompany customer invoice for project transactions</span></span> 

<span data-ttu-id="7e931-110">使用此程序以手動建立專案交易的公司間客戶發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-110">Use this procedure to manually create an intercompany customer invoice for project transactions.</span></span> <span data-ttu-id="7e931-111">搜尋工作人員在借方法律實體中的專案所張貼的工作時數，以及由您的法律實體代表借方法律實體所發生的費用。</span><span class="sxs-lookup"><span data-stu-id="7e931-111">Search for hours that were posted by workers on projects in the borrowing legal entities and for expenses that were incurred by your legal entity on behalf of borrowing legal entities.</span></span> <span data-ttu-id="7e931-112">您可以依據法律實體名稱、專案合約編號、專案編號、日期範圍或這些選項的任何組合進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="7e931-112">You can search by legal entity name, project contract number, project number, date range, or any combination of these options.</span></span> <span data-ttu-id="7e931-113">在搜尋結果中，選取要新增至公司間發票的交易。</span><span class="sxs-lookup"><span data-stu-id="7e931-113">In the search results, select the transactions to add to an intercompany invoice.</span></span> 

<span data-ttu-id="7e931-114">貸方法律實體必須執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="7e931-114">The following steps must be performed in the lending legal entity.</span></span> 

1. <span data-ttu-id="7e931-115">在 Dynamics 365 Finance 中，移至 **專案管理與會計** > **專案發票** > **公司間客戶發票**。</span><span class="sxs-lookup"><span data-stu-id="7e931-115">In Dynamics 365 Finance, go to **Project management and accounting** > **Project invoices** > **Intercompany customer invoices**.</span></span> <span data-ttu-id="7e931-116">在 **公司間客戶發票** 清單頁面的 [動作] 窗格中，選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="7e931-116">On the **Intercompany customer invoices**  list page, on the Action Pane, select **New.**</span></span>
2. <span data-ttu-id="7e931-117">在 **建立公司間發票** 頁面的 **法律實體** 欄位中，選取借方法律實體。</span><span class="sxs-lookup"><span data-stu-id="7e931-117">On the **Create intercompany invoice** page, in the **Legal entity** field, select a borrowing legal entity.</span></span>
3. <span data-ttu-id="7e931-118">選擇性：輸入特定的專案合約與專案編號。</span><span class="sxs-lookup"><span data-stu-id="7e931-118">Optional: Enter a specific project contract and project number.</span></span>
4. <span data-ttu-id="7e931-119">選取日期範圍來縮小搜尋範圍。</span><span class="sxs-lookup"><span data-stu-id="7e931-119">Narrow the search by selecting a date range.</span></span> <span data-ttu-id="7e931-120">在 **開始日期** 和 **結束日期** 欄位中輸入特定日期。</span><span class="sxs-lookup"><span data-stu-id="7e931-120">Enter specific dates in the **Start date** and **End date** fields.</span></span> <span data-ttu-id="7e931-121">只有在此日期範圍中過帳的公司間交易資料才會顯示在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="7e931-121">Only intercompany transactions that are posted within this date range are displayed in the search results.</span></span>
5. <span data-ttu-id="7e931-122">將 **專案進階帳目明細參數** 設定為 **是**，並選取 **搜尋**。</span><span class="sxs-lookup"><span data-stu-id="7e931-122">Set **Project advanced journal line parameter** to **Yes** and select **Search**.</span></span>
6. <span data-ttu-id="7e931-123">在搜尋結果中，選取要納入公司間發票提案的交易，然後選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="7e931-123">In the search results, select the transactions to include in the intercompany invoice proposal, and then select **OK**.</span></span>
7. <span data-ttu-id="7e931-124">在 **公司間客戶發票** 頁面上，會顯示您在搜尋結果中選取的公司間專案交易。</span><span class="sxs-lookup"><span data-stu-id="7e931-124">On the **Intercompany customer invoice** page, the intercompany project transactions that you selected from the search results are displayed.</span></span> <span data-ttu-id="7e931-125">若要在將發票傳送至借方法律實體之前修改交易，請執行以下動作：</span><span class="sxs-lookup"><span data-stu-id="7e931-125">To modify the transactions before you send the invoice to the borrowing legal entity, do the following:</span></span>
  
    1. <span data-ttu-id="7e931-126">在 **公司間客戶發票** 頁面上，開啟發票詳細資訊，然後選取 **新增明細**。</span><span class="sxs-lookup"><span data-stu-id="7e931-126">On the **Intercompany customer invoice** page, open the invoice details, and then select **Add line**.</span></span>
    2. <span data-ttu-id="7e931-127">若要移除明細，請選取該明細，然後選取 **移除**。</span><span class="sxs-lookup"><span data-stu-id="7e931-127">To remove a line, select it, and then select **Remove**.</span></span>
    3. <span data-ttu-id="7e931-128">檢視留言、原因、財務維度，以及其他有關發票明細詳細資料中所選明細的資訊。</span><span class="sxs-lookup"><span data-stu-id="7e931-128">View comments, reasons, financial dimensions, and other information about a selected line on the invoice line details.</span></span>
    
8. <span data-ttu-id="7e931-129">若要過帳公司間客戶發票，請在 [動作] 窗格中選取 **過帳**。</span><span class="sxs-lookup"><span data-stu-id="7e931-129">To post the intercompany customer invoice, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="7e931-130">如果您的組織需要在過帳之前先審查公司間發票，則系統管理員可能會為公司間發票設定工作流程。</span><span class="sxs-lookup"><span data-stu-id="7e931-130">If your organization requires that intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="7e931-131">如果未針對公司間發票設定工作流程，您可以過帳公司間發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-131">If a workflow is not set up for intercompany invoices, you can post the intercompany invoice.</span></span>

## <a name="create-a-batch-job-for-intercompany-invoices"></a><span data-ttu-id="7e931-132">建立公司間發票的批次工作</span><span class="sxs-lookup"><span data-stu-id="7e931-132">Create a batch job for intercompany invoices</span></span>

<span data-ttu-id="7e931-133">您可以同時為所有借方法律實體建立多個公司間發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-133">You can create multiple intercompany invoices at the same time for all borrowing legal entities.</span></span> <span data-ttu-id="7e931-134">例如，您可以使用搜尋功能，搜尋由借方工作人員過帳並與其他法律實體管理的專案相關的所有交易。</span><span class="sxs-lookup"><span data-stu-id="7e931-134">Using search functionality, you can for example, search for all transactions that are posted by borrowed workers and related to projects that are managed by other legal entities.</span></span> <span data-ttu-id="7e931-135">然後，針對每個借方法律實體，您可以為搜尋結果中所提供的交易建立公司間發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-135">Then, for each borrowing legal entity, you can create an intercompany invoice for the transactions provided in the search results.</span></span>

1. <span data-ttu-id="7e931-136">移至 **專案管理與會計** > **週期性** > **專案發票** > **建立公司間客戶發票**。</span><span class="sxs-lookup"><span data-stu-id="7e931-136">Go to **Project management and accounting** > **Periodic** > **Project invoices** > **Create intercompany customer invoices**.</span></span>
2. <span data-ttu-id="7e931-137">在 **建立公司間客戶發票** 頁面的 **公司** 欄位中，選取要開立發票的法律實體。</span><span class="sxs-lookup"><span data-stu-id="7e931-137">On the **Create intercompany customer invoices** page, in the **Company**  field, select a legal entity to invoice.</span></span> <span data-ttu-id="7e931-138">如果您未選取公司，則會針對所有借方法律實體顯示符合搜尋準則的所有交易。</span><span class="sxs-lookup"><span data-stu-id="7e931-138">If you don't select a company, all transactions that meet the search criteria are displayed for all borrowing legal entities.</span></span>
3. <span data-ttu-id="7e931-139">在 **每個建立一張發票** 中，選取是要根據專案或是根據借方法律實體為公司間交易建立發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-139">In **Create one invoice per**, select whether to create an invoice for intercompany transactions based on a project or based on a borrowing legal entity.</span></span>
4. <span data-ttu-id="7e931-140">選擇性：若要選取特定的專案和專案合約以為其建立公司間發票，請按一下 **選取**。</span><span class="sxs-lookup"><span data-stu-id="7e931-140">Optional: To select a specific project and project contract to create intercompany invoices for, click **Select**.</span></span> <span data-ttu-id="7e931-141">在 **查詢** 頁面的 **準則** 欄位中，選取專案合約、專案編號或兩者，然後選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="7e931-141">On the **Inquiry** page, in the **Criteria** field, select the project contract, project number, or both, and then select **OK**.</span></span>
5. <span data-ttu-id="7e931-142">在 **批次** 索引標籤上，設定批次程序，定期建立公司間發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-142">On the **Batch** tab, set up a batch process to create intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="7e931-143">如需詳細資訊，請參閱[從表單提交批次處理工作](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form)。</span><span class="sxs-lookup"><span data-stu-id="7e931-143">For more information, see [Submit a batch processing job from a form](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).</span></span>
6. <span data-ttu-id="7e931-144">若要過帳公司間發票，請在 [動作] 窗格中選取 **過帳**。</span><span class="sxs-lookup"><span data-stu-id="7e931-144">To post the intercompany invoices, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="7e931-145">如果您的組織需要在過帳之前先審查公司間發票，則系統管理員可能會為公司間發票設定工作流程。</span><span class="sxs-lookup"><span data-stu-id="7e931-145">If your organization requires intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="7e931-146">如果未針對公司間發票設定工作流程，您可以過帳公司間發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-146">If a workflow is not set up for intercompany invoices, you can post the intercompany invoices.</span></span>

## <a name="post-the-intercompany-vendor-invoice"></a><span data-ttu-id="7e931-147">過帳公司間廠商發票</span><span class="sxs-lookup"><span data-stu-id="7e931-147">Post the intercompany vendor invoice</span></span>

<span data-ttu-id="7e931-148">在過帳對應的公司間客戶發票時，借方法律實體的專案會計可以複查公司間擱置的廠商發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-148">A project accountant in the borrowing legal entity can review intercompany pending vendor invoices when the corresponding intercompany customer invoice is posted.</span></span> <span data-ttu-id="7e931-149">在財務中，在借方法律實體中，移至 **應付帳款** > **發票** > **擱置的廠商發票**。</span><span class="sxs-lookup"><span data-stu-id="7e931-149">In Finance, in the borrowing legal entity, go to **Accounts payable** > **Invoices** > **Pending vendor invoice**.</span></span> <span data-ttu-id="7e931-150">擱置的發票號碼將符合公司間客戶發票號碼。</span><span class="sxs-lookup"><span data-stu-id="7e931-150">The pending invoice number will match the intercompany customer invoice number.</span></span> <span data-ttu-id="7e931-151">確認發票正確，然後過帳發票。</span><span class="sxs-lookup"><span data-stu-id="7e931-151">Verify that the invoice is correct and then post the invoice.</span></span> <span data-ttu-id="7e931-152">將公司間廠商發票過帳時，會建立專案分類帳和總帳交易，反映借方法律實體中的交易成本。</span><span class="sxs-lookup"><span data-stu-id="7e931-152">Posting intercompany vendor invoice creates a project subledger and a general ledger transaction that reflects the transaction costs in the borrowing legal entity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
