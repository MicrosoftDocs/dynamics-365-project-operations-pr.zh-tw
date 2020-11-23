---
title: 產品
description: 本主題提供產品類別目錄的相關資訊，您可以使用類別目錄來向客戶提供有關組織所提供產品及定價的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 30633a7445baaf99af5be5c88e35b24824022b93
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121253"
---
# <a name="products"></a><span data-ttu-id="f2ebf-103">產品</span><span class="sxs-lookup"><span data-stu-id="f2ebf-103">Products</span></span>

<span data-ttu-id="f2ebf-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="f2ebf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f2ebf-105">產品是企業的骨幹。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-105">Products are the backbone of your business.</span></span> <span data-ttu-id="f2ebf-106">Dynamics 365 Sales Professional 中的產品類別目錄是產品與其價格資訊的集合。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-106">The product catalog in Dynamics 365 Sales Professional is a collection of products and pricing information.</span></span> <span data-ttu-id="f2ebf-107">快速建立產品類別目錄，讓銷售代表更容易提高其銷售。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-107">Make it easier for your sales reps to increase their sales by creating a product catalog quickly.</span></span>

## <a name="add-a-product"></a><span data-ttu-id="f2ebf-108">新增產品</span><span class="sxs-lookup"><span data-stu-id="f2ebf-108">Add a product</span></span>

1.  <span data-ttu-id="f2ebf-109">確定您具有 Sales Manager Professional 或系統管理員角色，以便在 Dynamics 365 Sales Professional 新增產品。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-109">Make sure you have the Sales Manager Professional or a System Administrator role so you can add products in Dynamics 365 Sales Professional.</span></span>
2.  <span data-ttu-id="f2ebf-110">在網站地圖的 **設定** 下方，選取 **產品**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-110">In the site map, under **Setup**, select **Products**.</span></span>
3.  <span data-ttu-id="f2ebf-111">選取 **新增產品**，並填入下列資訊：</span><span class="sxs-lookup"><span data-stu-id="f2ebf-111">Select **Add Product** and fill in the following information:</span></span>

    -  <span data-ttu-id="f2ebf-112">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f2ebf-112">**Name**</span></span>
    -  <span data-ttu-id="f2ebf-113">**產品識別碼**</span><span class="sxs-lookup"><span data-stu-id="f2ebf-113">**Product ID**</span></span>
    -  <span data-ttu-id="f2ebf-114">**上層**：選取產品的上層產品系列。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-114">**Parent**: Select a parent product family for the product.</span></span> <span data-ttu-id="f2ebf-115">如果您要在產品系列中建立下層產品，請在此處填入上層產品系列的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-115">If you're creating a child product in a product family, the name of the parent product family is populated here.</span></span> <span data-ttu-id="f2ebf-116">儲存記錄之後，無法變更此名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-116">This can't be changed after the record is saved.</span></span>
    -  <span data-ttu-id="f2ebf-117">**有效期自**/**有效期到**：選取 **有效期自** 和 **有效期到** 日期，以定義產品的有效期間。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-117">**Valid From**/**Valid To**: Define the period the product is valid for by selecting a **Valid From** and **Valid To** date.</span></span>
    -  <span data-ttu-id="f2ebf-118">**單位群組**：選取單位群組。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-118">**Unit Group**: Select a unit group.</span></span> <span data-ttu-id="f2ebf-119">單位群組是各種產品銷售單位的集合，用於定義個別項目如何組成更大的數量。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-119">A unit group is a collection of various units a product is sold in and defines how individual items are grouped into larger quantities.</span></span> <span data-ttu-id="f2ebf-120">例如，如果您新增種子做為產品，就可以建立稱為「種子」的單位群組，並將其主要單位定義為「包」。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-120">For example, if you're adding seeds as a product, you might have created a unit group called "Seeds" and defined its primary unit as "packet."</span></span>
    -  <span data-ttu-id="f2ebf-121">**預設單位**：選取產品銷售時最常使用的單位。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-121">**Default Unit**: Select the most common unit in which the product will be sold.</span></span> <span data-ttu-id="f2ebf-122">單位是用來計算您所銷售產品的數量或計量。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-122">Units are the quantities or measurements that you sell your products in.</span></span> <span data-ttu-id="f2ebf-123">例如，如果您新增種子做為產品，就可以採用包、盒或貨架做為銷售單位。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-123">For example, if you're adding seeds as a product, you can sell it in packets, boxes, or pallets.</span></span> <span data-ttu-id="f2ebf-124">這裡面每一種都會變成產品的單位。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-124">Each of these becomes a unit of the product.</span></span> <span data-ttu-id="f2ebf-125">如果種子幾乎都是以「包」為單位銷售，則選取它做為單位。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-125">If seeds are mostly sold in packets, select that as the unit.</span></span>
    -  <span data-ttu-id="f2ebf-126">**預設價目表**：如果這是新產品，則此欄位為唯讀。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-126">**Default Price List**: If this is a new product, this field is read-only.</span></span> <span data-ttu-id="f2ebf-127">您必須先完成所有必填欄位並儲存記錄之後，才能選取預設價目表。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-127">Before you can select a default price list, you must complete all the required fields and then save the record.</span></span> <span data-ttu-id="f2ebf-128">雖然預設價目表不是必要項目，但是在儲存產品記錄之後，最好設定每個產品的預設價目表。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-128">Although the default price list is not required, after you save the product record, it is a good idea to set a default price list for each product.</span></span> <span data-ttu-id="f2ebf-129">這樣，如果客戶記錄未含價目表，Sales 就可以使用預設價目表來產生報價、訂單和發票。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-129">Then, if a customer record does not contain a price list, Sales can use the default price list for generating quotes, orders, and invoices.</span></span>
    -  <span data-ttu-id="f2ebf-130">**支援小數點**：輸入介於 0 到 5 之間的整數。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-130">**Decimals Supported**: Enter a whole number between 0 and 5.</span></span> <span data-ttu-id="f2ebf-131">如果這項產品無法分成含小數點的數量，請輸入 0。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-131">If the product can't be divided into fractional quantities, enter 0.</span></span> <span data-ttu-id="f2ebf-132">如果產品沒有相關價目表，將針對此欄位中的值，驗證報價、訂單或發票產品記錄中 **數量** 欄位的有效位數。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-132">The precision of the **Quantity** field in the quote, order, or invoice product record is validated against the value in this field if the product does not have an associated price list.</span></span>
    -  <span data-ttu-id="f2ebf-133">**主題**：將產品與主題建立關聯。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-133">**Subject**: Associate this product with a subject.</span></span> <span data-ttu-id="f2ebf-134">您可以利用主體來分類您的產品以及篩選報表。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-134">You can use subjects to categorize your products and to filter reports.</span></span>

4.  <span data-ttu-id="f2ebf-135">選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-135">Select **Save**.</span></span>
5.  <span data-ttu-id="f2ebf-136">在 **其他詳細資料** 索引標籤的 **價目表項目** 區段中，選取 **更多命令** 圖示，然後選取 **新增價目表項目**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-136">On the **Additional Details** tab, in the **Price List Items** section, select **More commands**, and then select **Add New Price List Item**.</span></span>
7.  <span data-ttu-id="f2ebf-137">在 **其他詳細資料** 索引標籤的 **產品關聯** 區段中，選取 **更多命令** 圖示，然後選取 **新增產品關聯**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-137">On the **Additional Details** tab, in the **Product Relationship** section, select the **More commands** icon, and then select **Add New Product Relationship.**</span></span>
8.  <span data-ttu-id="f2ebf-138">在 **新增產品關聯** 表單中，輸入下列詳細資料，然後選取命令列上的 **儲存後關閉**：</span><span class="sxs-lookup"><span data-stu-id="f2ebf-138">In the **New Product Relationship** form, enter the following details, and on the command bar, select **Save and Close**:</span></span>

    -   <span data-ttu-id="f2ebf-139">**相關產品**：選取所需的產品以做為相關產品新增至您正在處理的現有產品記錄。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-139">**Related Product**: Select a product that you want to add as a related product to the existing product record you're working on.</span></span>
    -   <span data-ttu-id="f2ebf-140">**銷售關聯類型**：選取要新增產品為向上銷售、交叉銷售、配件或替代產品。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-140">**Sales Relation Type**: Select whether you want to add the product as an up-sell, cross-sell, accessory, or substitute product.</span></span>
    -   <span data-ttu-id="f2ebf-141">**方向**：選取產品之間的關聯為單向或雙向。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-141">**Direction**:Select whether the relationship between the products will be unidirectional or bidirectional.</span></span> <span data-ttu-id="f2ebf-142">當您選取單向時，您在 **相關產品** 中選取的產品將會顯示為現有產品的建議，但反向則不然。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-142">When you select unidirectional, the product that you select in **Related Product** will be shown as a recommendation for the existing product but not vice versa.</span></span>

9.  <span data-ttu-id="f2ebf-143">在產品表單上，選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-143">On the Product form, select **Save**.</span></span>

## <a name="import-products"></a><span data-ttu-id="f2ebf-144">匯入產品</span><span class="sxs-lookup"><span data-stu-id="f2ebf-144">Import products</span></span>

<span data-ttu-id="f2ebf-145">您可以使用匯入範本，將大量產品資料帶入 Dynamics 365 Sales。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-145">You can use import templates to bring bulk product data into Dynamics 365 Sales.</span></span>

## <a name="revise-a-product"></a><span data-ttu-id="f2ebf-146">修訂產品</span><span class="sxs-lookup"><span data-stu-id="f2ebf-146">Revise a product</span></span>

<span data-ttu-id="f2ebf-147">視需要快速修訂產品的屬性並重新發行資訊以保持產品存貨的最新狀態，讓銷售專員可以查看最新的庫存變更。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-147">Keep the product inventory updated by quickly revising properties for the products, as required, and republishing the information so that your sales agents can see the latest changes to the inventory.</span></span>

1.  <span data-ttu-id="f2ebf-148">請確定您具有下列其中一個資訊安全角色或同等的權限：系統管理員、系統自訂員、銷售經理、業務副總、行銷副總或 CEO 商務經理人。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-148">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="f2ebf-149">在網站地圖中，選取 **產品**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-149">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="f2ebf-150">開啟您要變更的使用中產品，然後在命令列上選取 **修訂**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-150">Open an active product that you want to change, and on the command bar, select **Revise**.</span></span>
4.  <span data-ttu-id="f2ebf-151">在 **確認修訂** 對話方塊中選取 **確認**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-151">In the **Confirm Revise** dialog box, select **Confirm**.</span></span> <span data-ttu-id="f2ebf-152">這樣會將產品狀態變更為 **修訂中**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-152">This will change the product status to **Under Revision**.</span></span>
5.  <span data-ttu-id="f2ebf-153">完成變更後，在命令列上選取 **發行**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-153">After you're done making changes, on the command bar, select **Publish**.</span></span>

    > [!TIP]
    > <span data-ttu-id="f2ebf-154">若要還原變更並繼續使用產品的最新使用中版本，請選取 **還原**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-154">To revert the changes and continue with the last active version of the product, select **Revert**.</span></span> <span data-ttu-id="f2ebf-155">這樣會將產品的狀態變更為 **使用中**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-155">This changes the status of the product back to **Active**.</span></span>

## <a name="clone-a-product"></a><span data-ttu-id="f2ebf-156">再製產品</span><span class="sxs-lookup"><span data-stu-id="f2ebf-156">Clone a product</span></span> 

<span data-ttu-id="f2ebf-157">當您建立新產品時，再製現有產品可以節省時間。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-157">When you're creating a new product, save time by cloning an existing one.</span></span> <span data-ttu-id="f2ebf-158">這樣做會建立原始記錄的複本，包含所有詳細資料，但不包括名稱和 ID。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-158">This creates a copy of the original record with all the details except for the name and ID.</span></span>

1.  <span data-ttu-id="f2ebf-159">請確定您具有下列其中一個資訊安全角色或同等的權限：系統管理員、系統自訂員、銷售經理、業務副總、行銷副總或 CEO 商務經理人。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-159">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="f2ebf-160">在網站地圖中，選取 **產品**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-160">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="f2ebf-161">選取要再製的產品記錄，然後選取命令列的 **再製**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-161">Select a product record that you want to clone, and on the command bar, select **Clone**.</span></span> <span data-ttu-id="f2ebf-162">確認對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-162">A confirmation dialog box appears.</span></span>
4.  <span data-ttu-id="f2ebf-163">選取 **確認**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-163">Select **Confirm**.</span></span>

<span data-ttu-id="f2ebf-164">新的產品記錄會開啟，其中顯示與原始產品記錄相同的詳細資料，但名稱和 ID 不同。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-164">A new product record opens with the same details as the original one except for the name and ID.</span></span>

## <a name="retire-a-product"></a><span data-ttu-id="f2ebf-165">淘汰產品</span><span class="sxs-lookup"><span data-stu-id="f2ebf-165">Retire a product</span></span> 

<span data-ttu-id="f2ebf-166">如果您的組織不再銷售某一項產品，請將該產品淘汰，以便不再對銷售人員提供該產品。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-166">If your organization doesn't sell a product anymore, retire it so that the product is no longer available to your sales agents.</span></span>

1.  <span data-ttu-id="f2ebf-167">請確定您具有系統管理員或 Sales Professional Manager 角色或同等的權限。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-167">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="f2ebf-168">在網站地圖中，選取 **產品**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-168">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="f2ebf-169">開啟您要淘汰的使用中產品，然後在命令列上選取 **淘汰**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-169">Open an active product that you want to retire, and on the command bar, select **Retire**.</span></span>
4.  <span data-ttu-id="f2ebf-170">在 **確認淘汰** 對話方塊中選取 **確認**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-170">In the **Confirm Retire** dialog box, select **Confirm**.</span></span>


## <a name="delete-a-product"></a><span data-ttu-id="f2ebf-171">刪除產品</span><span class="sxs-lookup"><span data-stu-id="f2ebf-171">Delete a product</span></span>

<span data-ttu-id="f2ebf-172">若要停止銷售產品，請將它刪除。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-172">To stop selling a product, delete it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2ebf-173">刪除的記錄無法復原。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-173">You can't recover a deleted record.</span></span>

1.  <span data-ttu-id="f2ebf-174">請確定您具有系統管理員或 Sales Professional Manager 角色或同等的權限。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-174">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="f2ebf-175">在網站地圖中，選取 **產品**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-175">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="f2ebf-176">選取要刪除的產品記錄，然後選取命令列的 **刪除**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-176">Select a product record you want to delete, and on the command bar, select **Delete**.</span></span>
4.  <span data-ttu-id="f2ebf-177">在 **確認刪除** 對話方塊中選取 **繼續**。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-177">In the **Confirm Deletion** dialog box, select **Continue**.</span></span>
 
 ## <a name="quantity-factors-for-products"></a><span data-ttu-id="f2ebf-178">產品的數量因數</span><span class="sxs-lookup"><span data-stu-id="f2ebf-178">Quantity factors for products</span></span>

<span data-ttu-id="f2ebf-179">數量因素支援訂閱型產品的銷售。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-179">Quantity factors support the sale of subscription-based products.</span></span> <span data-ttu-id="f2ebf-180">對於訂閱型產品，報價或專案合約服務內容上的數量會以使用者的月數來表示。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-180">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="f2ebf-181">訂閱軟體的價格通常在目錄中儲存為每個月每個使用者的價格。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-181">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="f2ebf-182">但是，您可以改用其他時間描述。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-182">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="f2ebf-183">在銷售處理期間，報價明細的價格通常是由 IT 銷售專員議定並打折扣的每個使用者、每個月的價格。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-183">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="f2ebf-184">每筆交易都有不同的使用者數目和不同的訂閱月數。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-184">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="f2ebf-185">用來計算報價明細金額的數量，是使用者人數與訂閱月數的乘積。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-185">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="f2ebf-186">數量因數依賴產品屬性。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-186">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="f2ebf-187">設定產品的特定屬性時，您可以將這其中一部分屬性或所有屬性標示為數量因數。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-187">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="f2ebf-188">系統會驗證是否只有含有數值資料類型的數值屬性或產品屬性，才會標記為數量因數。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-188">The system validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="f2ebf-189">將設定數量因數的產品新增至報價明細時，報價明細上的 **數量** 欄位會變成唯讀欄位。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-189">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="f2ebf-190">輸入數量因數的產品屬性值之後，系統會計算報價明細的數量。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-190">After you enter values for product properties that are quantity factors, the quantity of the quote line is calculated.</span></span>

<span data-ttu-id="f2ebf-191">例如 (若有下列屬性的話)：</span><span class="sxs-lookup"><span data-stu-id="f2ebf-191">For example, if there are the following properties:</span></span> 

- <span data-ttu-id="f2ebf-192">**使用者數**：使用者的數目</span><span class="sxs-lookup"><span data-stu-id="f2ebf-192">**No of users**: The number of users</span></span> 
- <span data-ttu-id="f2ebf-193">**月數**：訂閱的月期數</span><span class="sxs-lookup"><span data-stu-id="f2ebf-193">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="f2ebf-194">**產品 SKU**</span><span class="sxs-lookup"><span data-stu-id="f2ebf-194">**Product SKU**</span></span> 

<span data-ttu-id="f2ebf-195">您可以編輯產品明細的屬性，將 **使用者數** 和 **月數** 屬性標示為數量因數。</span><span class="sxs-lookup"><span data-stu-id="f2ebf-195">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 
