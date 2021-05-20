---
title: 設定非庫存材料和待處理廠商發票
description: 本主題說明如何啟用非庫存材料和待處理廠商發票。
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a84245a246f49ab69466aba0fec332f0489eec6c
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880627"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a><span data-ttu-id="80fb7-103">設定非庫存材料和待處理廠商發票</span><span class="sxs-lookup"><span data-stu-id="80fb7-103">Configure non-stocked materials and pending vendor invoices</span></span>

<span data-ttu-id="80fb7-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="80fb7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="minimum-version-requirement"></a><span data-ttu-id="80fb7-105">最小版本需求</span><span class="sxs-lookup"><span data-stu-id="80fb7-105">Minimum version requirement</span></span>

<span data-ttu-id="80fb7-106">針對 Dynamics 365 Project Operations 非庫存/資源型案例使用非庫存材料和待處理廠商發票時，需要下列版本：</span><span class="sxs-lookup"><span data-stu-id="80fb7-106">Using non-stocked materials and pending vendor invoices for Dynamics 365 Project Operations non-stocked/resource based scenarios requires the following versions:</span></span>

<span data-ttu-id="80fb7-107">Dynamics 365 Dataverse 解決方案：</span><span class="sxs-lookup"><span data-stu-id="80fb7-107">Dynamics 365 Dataverse solutions:</span></span>

- <span data-ttu-id="80fb7-108">Project Operations – 4.9.0.221 或更新版本</span><span class="sxs-lookup"><span data-stu-id="80fb7-108">Project Operations – 4.9.0.221 or higher</span></span>
- <span data-ttu-id="80fb7-109">雙重寫入應用程式協調流程解決方案 - 2.2.2.23 或更新版本</span><span class="sxs-lookup"><span data-stu-id="80fb7-109">Dual-write application orchestration solution - 2.2.2.23 or higher</span></span>

<span data-ttu-id="80fb7-110">Dynamics 365 Finance：</span><span class="sxs-lookup"><span data-stu-id="80fb7-110">Dynamics 365 Finance:</span></span>
- <span data-ttu-id="80fb7-111">10.0.18 (10.0.793.52) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="80fb7-111">10.0.18 (10.0.793.52) or higher.</span></span> <span data-ttu-id="80fb7-112">確定您的 Finance 環境是最新的，且已套用所有品質更新以符合最小版本需求。</span><span class="sxs-lookup"><span data-stu-id="80fb7-112">Make sure that your Finance environment is current and all quality updates are applied to meet the minimum version requirements.</span></span>

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a><span data-ttu-id="80fb7-113">對非庫存材料與待處理廠商發票整合執行雙重寫入對應</span><span class="sxs-lookup"><span data-stu-id="80fb7-113">Run Dual-write maps for non-stocked materials and vendor invoice integration</span></span>

<span data-ttu-id="80fb7-114">本節提供有關非庫存材料和待處理廠商發票所需之特定對應的資訊。</span><span class="sxs-lookup"><span data-stu-id="80fb7-114">This section provides information about specific the maps required for non-stocked materials and vendor invoices.</span></span> <span data-ttu-id="80fb7-115">確認[佈建新環境](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps)主題中列出的先決條件對應是否正在您的環境中執行。</span><span class="sxs-lookup"><span data-stu-id="80fb7-115">Verify that the prerequisite maps listed in the [Provision a new environment](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) topic are running on your environment.</span></span>

1. <span data-ttu-id="80fb7-116">前往 Lifecycle Services (LCS)、瀏覽至您的 LCS 專案，然後移至 **環境詳細資料** 頁面。</span><span class="sxs-lookup"><span data-stu-id="80fb7-116">Go to Lifecycle Services (LCS), navigate to your LCS project, and go to the **Environment details** page.</span></span>
2. <span data-ttu-id="80fb7-117">在 **Common Data Service 環境資訊** 區段中，選取 **連結至 CDS for Apps**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-117">In the **Common Data Service Environment Information** section, select **Link to CDS for Apps**.</span></span> <span data-ttu-id="80fb7-118">選取連結之後，您會重新導向至對應中實體的清單。</span><span class="sxs-lookup"><span data-stu-id="80fb7-118">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="80fb7-119">確定下列對應正在執行。</span><span class="sxs-lookup"><span data-stu-id="80fb7-119">Make sure the following maps are running.</span></span> <span data-ttu-id="80fb7-120">如果未在執行，請啟動這些對應，並務必將所有相關的資料表對應都加入。</span><span class="sxs-lookup"><span data-stu-id="80fb7-120">If they aren't running, start them and make sure to include all related table maps.</span></span>

    - <span data-ttu-id="80fb7-121">CDS 已發行相異的產品 (產品)</span><span class="sxs-lookup"><span data-stu-id="80fb7-121">CDS released distinct products (products)</span></span>
    - <span data-ttu-id="80fb7-122">廠商 v2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="80fb7-122">Vendors v2 (msdyn_vendors)</span></span>
    - <span data-ttu-id="80fb7-123">Project Operations 材料估計值資料表 (msdyn_estimatelines)</span><span class="sxs-lookup"><span data-stu-id="80fb7-123">Project Operations table for material estimates (msdyn_estimatelines)</span></span>
    - <span data-ttu-id="80fb7-124">Project Operations 整合專案廠商發票匯出實體 (msdyn_projectvendorinvoices)</span><span class="sxs-lookup"><span data-stu-id="80fb7-124">Project Operations integration project vendor invoice export entity (msdyn_projectvendorinvoices)</span></span>
    - <span data-ttu-id="80fb7-125">Project Operations 整合專案廠商發票明細匯出實體 (msdyn_projectvendorinvoicelines)</span><span class="sxs-lookup"><span data-stu-id="80fb7-125">Project Operations integration project vendor invoice line export entity (msdyn_projectvendorinvoicelines)</span></span>
    - <span data-ttu-id="80fb7-126">Project Operations 整合實際值 (msdyn_actuals)。</span><span class="sxs-lookup"><span data-stu-id="80fb7-126">Project Operations integration actuals (msdyn_actuals).</span></span> <span data-ttu-id="80fb7-127">確定您正在執行對應版本 1.0.0.14 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="80fb7-127">Make sure you are running map version 1.0.0.14 or higher.</span></span> <span data-ttu-id="80fb7-128">您可以在 **雙重寫入** 頁面的 **版本** 欄中查看對應的使用中版本。</span><span class="sxs-lookup"><span data-stu-id="80fb7-128">You can see the active version of the map in the **Version** column on the **Dual Write** page.</span></span> <span data-ttu-id="80fb7-129">您可以選取 **資料表對應版本**，然後儲存選取的版本來啟用新的對應版本。</span><span class="sxs-lookup"><span data-stu-id="80fb7-129">You can activate a new version of the map by selecting **Table map version** and then saving the selected version.</span></span>

<span data-ttu-id="80fb7-130">如果您使用的是標準範本資料，則可能還需要透過初始同步停止並重新啟動下列實體對應：</span><span class="sxs-lookup"><span data-stu-id="80fb7-130">If you are using standard demo data, you might also need to stop and restart the following entity maps with initial sync:</span></span>
  - <span data-ttu-id="80fb7-131">付款日 CDS V2 (msdyn_paymentdays)</span><span class="sxs-lookup"><span data-stu-id="80fb7-131">Payment days CDS V2 (msdyn_paymentdays)</span></span>
  - <span data-ttu-id="80fb7-132">付款排程 (msdyn_paymentschedules)</span><span class="sxs-lookup"><span data-stu-id="80fb7-132">Payment schedule (msdyn_paymentschedules)</span></span>
  - <span data-ttu-id="80fb7-133">付款條件 (msdyn_paymentterms)</span><span class="sxs-lookup"><span data-stu-id="80fb7-133">Terms of payment (msdyn_paymentterms)</span></span>
  - <span data-ttu-id="80fb7-134">廠商群組 (msdyn_vendorgroups)</span><span class="sxs-lookup"><span data-stu-id="80fb7-134">Vendor groups (msdyn_vendorgroups)</span></span>
  - <span data-ttu-id="80fb7-135">單位 (uom)</span><span class="sxs-lookup"><span data-stu-id="80fb7-135">Units (uom)</span></span>

> [!NOTE]
> <span data-ttu-id="80fb7-136">廠商群組與單位的初始同步可能會因為現有示範資料集中的一些記錄而失敗。</span><span class="sxs-lookup"><span data-stu-id="80fb7-136">The initial sync for vendor groups and units might fail for a few records in the existing demo data set.</span></span> <span data-ttu-id="80fb7-137">您可以忽略失敗，因為這些失敗不會阻止您搭配 Project Operations 使用示範資料。</span><span class="sxs-lookup"><span data-stu-id="80fb7-137">You can ignore the failures as they won't prevent you from using demo data with Project Operations.</span></span>

## <a name="configure-prerequisites-in-dataverse"></a><span data-ttu-id="80fb7-138">設定 Dataverse 中的先決條件</span><span class="sxs-lookup"><span data-stu-id="80fb7-138">Configure prerequisites in Dataverse</span></span>

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a><span data-ttu-id="80fb7-139">啟用工作流程以根據廠商實體建立科目</span><span class="sxs-lookup"><span data-stu-id="80fb7-139">Activate workflow to create accounts based on vendor entity</span></span>

<span data-ttu-id="80fb7-140">雙重寫入協調流程解決方案提供[廠商主機整合](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping)。</span><span class="sxs-lookup"><span data-stu-id="80fb7-140">The Dual Write Orchestration solution provides [Vendors master integration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping).</span></span> <span data-ttu-id="80fb7-141">做為此功能的先決條件，廠商資料必須是在 **客戶** 實體中建立。</span><span class="sxs-lookup"><span data-stu-id="80fb7-141">As a prerequisite for this feature, vendor data must be created in the **Accounts** entity.</span></span> <span data-ttu-id="80fb7-142">啟用範本工作流程程序，以便在 **客戶** 資料表中建立廠商，如[在廠商設計之間切換](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch#use-the-extended-vendor-design-for-vendors-of-the-organization-type)中所述。</span><span class="sxs-lookup"><span data-stu-id="80fb7-142">Activate a template workflow process to create vendors in the **Accounts** table as described in [Switch between vendor designs](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch#use-the-extended-vendor-design-for-vendors-of-the-organization-type).</span></span>

### <a name="set-products-to-be-created-as-active"></a><span data-ttu-id="80fb7-143">將所要建立的產品設定為使用中</span><span class="sxs-lookup"><span data-stu-id="80fb7-143">Set products to be created as active</span></span>

<span data-ttu-id="80fb7-144">非庫存材料必須在 Finance 中設定為 **已發行的產品**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-144">Non-stocked materials must be configured as **Released products** in Finance.</span></span> <span data-ttu-id="80fb7-145">雙重寫入協調流程解決方案提供現成可用的 [Dataverse 產品類別目錄的已發行產品整合](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping)。</span><span class="sxs-lookup"><span data-stu-id="80fb7-145">The Dual Write Orchestration solution provides an out-of-the-box [Released products integration to Dataverse Product catalog](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping).</span></span> <span data-ttu-id="80fb7-146">預設會以草稿狀態將產品從 Finance 同步處理至 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="80fb7-146">By default, products from Finance are synchronized to Dataverse in a draft state.</span></span> <span data-ttu-id="80fb7-147">若要將產品同步處理為使用中狀態，以便直接使用於材料使用單據或待處理廠商發票，請移至 **系統** > **管理** > **系統管理** > **系統設定**，並在 **銷售** 索引標籤上，將 **以使用中狀態建立產品** 設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-147">To synchronize the product to an active state so that it can be directly used in material usage documents or pending vendor invoices, go to **System** > **Administration** > **System administration** > **System settings**, and on the **Sales** tab, set **Create products in active state** to **Yes**.</span></span>

## <a name="configure-prerequisites-in-finance"></a><span data-ttu-id="80fb7-148">設定 Finance 中的先決條件</span><span class="sxs-lookup"><span data-stu-id="80fb7-148">Configure prerequisites in Finance</span></span>

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a><span data-ttu-id="80fb7-149">啟用待處理廠商發票的功能金鑰</span><span class="sxs-lookup"><span data-stu-id="80fb7-149">Enable the feature key for pending vendor invoices</span></span>

<span data-ttu-id="80fb7-150">完成下列步驟，啟用可在待處理廠商發票明細上新增專案詳細資料的功能。</span><span class="sxs-lookup"><span data-stu-id="80fb7-150">Complete the following steps to enable functionality to add project details on pending vendor invoice lines.</span></span>

1. <span data-ttu-id="80fb7-151">在 Finance 中，移至 **功能管理** 工作區。</span><span class="sxs-lookup"><span data-stu-id="80fb7-151">In Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="80fb7-152">在功能清單中，下列 **在資源型/非庫存案例適用的 Project Operations 上啟用待處理廠商發票**，然後選取 **啟用**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-152">In the feature list, find **Enable pending vendor invoices on Project Operations for resource based/non-stocked scenarios** feature and select **Enable**.</span></span>

### <a name="define-category-groups-and-project-categories-for-items"></a><span data-ttu-id="80fb7-153">定義項目的類別群組和專案類別</span><span class="sxs-lookup"><span data-stu-id="80fb7-153">Define category groups and project categories for items</span></span>

<span data-ttu-id="80fb7-154">為 **項目** 交易類型設定至少一個類別群組，以及至少一個使用此群組的專案類別。</span><span class="sxs-lookup"><span data-stu-id="80fb7-154">Configure at least one category group for the **Item** transaction type , and at least one project category using this group.</span></span> <span data-ttu-id="80fb7-155">如需詳細資訊，請參閱[設定專案類別](../project-accounting/configure-project-categories.md#category-groups)。</span><span class="sxs-lookup"><span data-stu-id="80fb7-155">For more information, see [Configure project categories](../project-accounting/configure-project-categories.md#category-groups).</span></span>

<span data-ttu-id="80fb7-156">檢閱專案成本和 營收設定檔，並設定項目交易的總帳過帳設定。</span><span class="sxs-lookup"><span data-stu-id="80fb7-156">Review the project cost and revenue profiles, and configure ledger posting setup for item transactions.</span></span> <span data-ttu-id="80fb7-157">如需詳細資訊，請參閱[設定計費專案會計](../project-accounting/configure-accounting-billable-projects.md)。</span><span class="sxs-lookup"><span data-stu-id="80fb7-157">For more information, see [Configure accounting for billable projects](../project-accounting/configure-accounting-billable-projects.md).</span></span>

### <a name="set-up-a-write-in-product"></a><span data-ttu-id="80fb7-158">設定目錄外產品</span><span class="sxs-lookup"><span data-stu-id="80fb7-158">Set up a write-in product</span></span>

<span data-ttu-id="80fb7-159">在 Project Operations 中，您可以針對已發行產品類別目錄中所設定的產品類別目錄以及針對目錄外產品，記錄其材料估計值和使用方式。</span><span class="sxs-lookup"><span data-stu-id="80fb7-159">In Project Operations, you can record material estimates and usage for catalog products that are configured in the released product catalog and for write-in products.</span></span> <span data-ttu-id="80fb7-160">使用目錄外產品需要已在 Finance 中針對此目的所設定的單一已發行產品。</span><span class="sxs-lookup"><span data-stu-id="80fb7-160">Using write-in products requires a single released product that's configured in Finance for this purpose.</span></span> <span data-ttu-id="80fb7-161">完成下列步驟以設定目錄外產品。</span><span class="sxs-lookup"><span data-stu-id="80fb7-161">Complete the following steps to configure a write-in product.</span></span> <span data-ttu-id="80fb7-162">在每個使用資源/非庫存案例適用的 Project Operations 的法律實體中重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="80fb7-162">Repeat these steps in each legal entity that is using Project Operations for resource/non-stocked scenarios.</span></span>

1. <span data-ttu-id="80fb7-163">在 Finance 中，移至 **產品資訊管理** > **產品** > **已發行產品**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-163">In Finance, go to **Product Information Management** > **Products** > **Released products**, and select **New**.</span></span>
2. <span data-ttu-id="80fb7-164">在 **產品類型** 欄位中，選取 **項目**，並在 **產品子類型** 欄位中選取 **產品**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-164">In the **Product type** field, select **Item** and in the **Product subtype** field, select **Product**.</span></span>
3. <span data-ttu-id="80fb7-165">輸入產品編號 (WRITEIN) 和產品名稱 (目錄外產品)。</span><span class="sxs-lookup"><span data-stu-id="80fb7-165">Enter the product number (WRITEIN) and the product name (Write-in Product).</span></span>
4. <span data-ttu-id="80fb7-166">選取項目模型群組。</span><span class="sxs-lookup"><span data-stu-id="80fb7-166">Select  the item model group.</span></span> <span data-ttu-id="80fb7-167">產品您所選項目模型群組的 **庫存原則庫存產品** 欄位已設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-167">Make sure that the item model group you select has the **Inventory policy Stocked product** field set to **False**.</span></span>
5. <span data-ttu-id="80fb7-168">選取 **項目群組**、**儲存體維度群組** 和 **追蹤維度群組** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="80fb7-168">Select values in the **Item group**, **Storage dimension group**, and **Tracking dimension group** fields.</span></span> <span data-ttu-id="80fb7-169">僅使用 **地點** 的 **儲存體維度**，且不要設定任何追蹤維度。</span><span class="sxs-lookup"><span data-stu-id="80fb7-169">Use the **Storage dimension** for **Site** only, and do not set any tracking dimensions.</span></span>
6. <span data-ttu-id="80fb7-170">選取 **庫存單位**、**採購單位** 和 **銷售單位** 欄位中的值，然後儲存您的變更。</span><span class="sxs-lookup"><span data-stu-id="80fb7-170">Select values in the **Inventory unit**, **Purchase unit**, and **Sales unit** field, and then save your changes.</span></span>
7. <span data-ttu-id="80fb7-171">在 **計劃** 索引標籤中，設定預設訂單設定，並在 **庫存** 索引標籤上設定預設地點和倉庫。</span><span class="sxs-lookup"><span data-stu-id="80fb7-171">In the **Plan** tab, set the default order settings, and on the **Inventory** tab, set the default site and warehouse.</span></span>
8. <span data-ttu-id="80fb7-172">移至 **專案管理與會計** > **設定** > **專案管理與會計參數**，並開啟 **Dynamics 365 Dataverse 上的 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-172">Go to **Project management and accounting** > **Setup** > **Project management and accounting parameters** and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
9. <span data-ttu-id="80fb7-173">在 **材料** 索引標籤的 **目錄外產品** 欄位中，選取您所建立的產品。</span><span class="sxs-lookup"><span data-stu-id="80fb7-173">On the **Materials** tab, in the **Write-in product** field, select the product you created.</span></span>
10. <span data-ttu-id="80fb7-174">在 Dataverse 環境的網站地圖中，開啟 **產品** 實體並尋找目錄外產品記錄。</span><span class="sxs-lookup"><span data-stu-id="80fb7-174">In your Dataverse environment, in the site map, open the **Products** entity and find the write-in product record.</span></span> 
11. <span data-ttu-id="80fb7-175">開啟記錄詳細資料，並將產品狀態設定為 **已淘汰**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-175">Open the record details and set product state to **Retired**.</span></span> <span data-ttu-id="80fb7-176">此產品狀態可防止任何人不慎在材料估計值及使用單據中直接使用此記錄。</span><span class="sxs-lookup"><span data-stu-id="80fb7-176">This product state prevents anyone from accidentally using this record directly in material estimates and usage documents.</span></span>

### <a name="set-up-a-procurement-integration-account"></a><span data-ttu-id="80fb7-177">設定採購整合科目</span><span class="sxs-lookup"><span data-stu-id="80fb7-177">Set up a procurement integration account</span></span>

<span data-ttu-id="80fb7-178">採購整合科目會在以歸屬於專案的明細進行待處理廠商發票過帳時，做為結算科目。</span><span class="sxs-lookup"><span data-stu-id="80fb7-178">The procurement integration account is used as a clearing account when posting a pending vendor invoice with lines attributed to a project.</span></span>

<span data-ttu-id="80fb7-179">系統將待處理廠商發票過帳時，專案成本金額會使用此科目。</span><span class="sxs-lookup"><span data-stu-id="80fb7-179">When the system posts a pending vendor invoice, this account is used for the project cost amount.</span></span> <span data-ttu-id="80fb7-180">系統會在 Dataverse 中處理廠商發票詳細資料，並且建立對應的專案實際值。</span><span class="sxs-lookup"><span data-stu-id="80fb7-180">The vendor invoice details are processed in Dataverse, and a corresponding project actual is created.</span></span> <span data-ttu-id="80fb7-181">專案實際值的資訊會新增至 Project Operations 整合帳目。</span><span class="sxs-lookup"><span data-stu-id="80fb7-181">The information from the project actual is added to the Project Operations Integration journal.</span></span> <span data-ttu-id="80fb7-182">將整合帳目過帳時，金額會從採購整合科目結清並記錄至專案成本。</span><span class="sxs-lookup"><span data-stu-id="80fb7-182">When you post the integration journal, the amount is cleared from the procurement integration account and recorded to the project cost.</span></span>

1. <span data-ttu-id="80fb7-183">若要設定採購整合科目，請移至 **專案管理與會計** > **設定** > **專案管理與會計參數**，並開啟 **Dynamics 365 Dataverse 上的 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-183">To set up the procurement integration account, go to **Project management and accounting** > **Setup** > **Project management and accounting parameters**, and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
2. <span data-ttu-id="80fb7-184">選取 **材料** 索引標籤，並選取 **採購整合科目** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="80fb7-184">Select the **Materials** tab, and select a value in the **Procurement integration account** field.</span></span>

#### <a name="set-up-project-category-defaults-for-an-item"></a><span data-ttu-id="80fb7-185">設定項目的專案類別預設值</span><span class="sxs-lookup"><span data-stu-id="80fb7-185">Set up project category defaults for an item</span></span>

1. <span data-ttu-id="80fb7-186">在 Finance 中，移至 **專案管理與會計** > **設定** > **專案管理與會計參數**，並開啟 **Dynamics 365 Dataverse 上的 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="80fb7-186">In Finance, go to **Project management and accounting** > **Setup** > **Project management and accounting parameters**, and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
2. <span data-ttu-id="80fb7-187">在 **專案類別預設值** 索引標籤的 **項目** 欄位中，選取值。</span><span class="sxs-lookup"><span data-stu-id="80fb7-187">On the **Project category defaults** tab, in the **Item** field, select a value.</span></span> <span data-ttu-id="80fb7-188">如果專案實際值記錄中未設定專案類別，則材料交易會使用此專案類別。</span><span class="sxs-lookup"><span data-stu-id="80fb7-188">This project category is used for material transactions if the project category wasn't set on the project actuals record.</span></span>
