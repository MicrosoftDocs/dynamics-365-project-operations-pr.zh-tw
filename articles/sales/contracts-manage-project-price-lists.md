---
title: 管理專案合約上的專案價目表
description: 本主題提供有關管理專案合約上的專案價目表的資訊。
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010371"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="f054f-103">管理專案合約上的專案價目表</span><span class="sxs-lookup"><span data-stu-id="f054f-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="f054f-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="f054f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f054f-105">Dynamics 365 Project Operations 中的專案合約是設計來支援合約上多個在有效期限內的銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="f054f-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="f054f-106">在 Project Operations 中，有一個新的名為 **專案價目表** 的相關實體。</span><span class="sxs-lookup"><span data-stu-id="f054f-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="f054f-107">此實體與專案合約有一對多關聯。</span><span class="sxs-lookup"><span data-stu-id="f054f-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="f054f-108">專案價目表可用於訂定專案中時間、材料及費用交易的價格。</span><span class="sxs-lookup"><span data-stu-id="f054f-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="f054f-109">當合約有一份或多份專案價目表時，這些價目表會在透過合約服務內容與合約產生關聯的專案上，用於訂定時間、材料、費用估計值及實際值的價格。</span><span class="sxs-lookup"><span data-stu-id="f054f-109">When a contract has one or more project price lists, these price lists are used to price for time, material, expense estimates, and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="f054f-110">當專案合約沒有專案價目表時，您會看到警告訊息，指出沒有專案價目表，無法為您的估計值、實際專案工作、材料以及已記錄的費用進行定價。</span><span class="sxs-lookup"><span data-stu-id="f054f-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, material, and expenses logged will not be priced.</span></span> <span data-ttu-id="f054f-111">銷售值不會有任何價格。</span><span class="sxs-lookup"><span data-stu-id="f054f-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="f054f-112">在專案合約上建立或解除與專案價目表的關聯</span><span class="sxs-lookup"><span data-stu-id="f054f-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a><span data-ttu-id="f054f-113">建立用於估計專案型工作、材料和費用的特定價目表，或與之產生關聯</span><span class="sxs-lookup"><span data-stu-id="f054f-113">Create or associate a specific price list for estimating project-based work, material, and expenses</span></span>

1. <span data-ttu-id="f054f-114">在專案合約上，選取 **專案價目表** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="f054f-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="f054f-115">在子格中，選取 **+ 新增專案價目表**。</span><span class="sxs-lookup"><span data-stu-id="f054f-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="f054f-116">在 **快速建立** 滑桿上，選取價目表。</span><span class="sxs-lookup"><span data-stu-id="f054f-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="f054f-117">下拉式清單會顯示所有其內容設定為 **銷售** 的價目表，其中價目表上的貨幣與合約上的貨幣相符。</span><span class="sxs-lookup"><span data-stu-id="f054f-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="f054f-118">輸入專案價目表關聯的描述、選取 **儲存**，然後關閉 **快速建立** 滑桿。</span><span class="sxs-lookup"><span data-stu-id="f054f-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="f054f-119">專案價目表關聯已建立。</span><span class="sxs-lookup"><span data-stu-id="f054f-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="f054f-120">重複步驟 1-4，將多個專案價目表關聯至專案合約。</span><span class="sxs-lookup"><span data-stu-id="f054f-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="f054f-121">只有您在每個關聯的專案價目表上各有不同的日期時效性時，才要建立多個專案價目表。</span><span class="sxs-lookup"><span data-stu-id="f054f-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="f054f-122">Project Operations 不支援專案價目表的日期時效性重疊。</span><span class="sxs-lookup"><span data-stu-id="f054f-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="f054f-123">如果包含指定日期的交易有多個專案價目表，該交易的價格會預設為零。</span><span class="sxs-lookup"><span data-stu-id="f054f-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="f054f-124">移除專案價目表關聯</span><span class="sxs-lookup"><span data-stu-id="f054f-124">Remove a project price list association</span></span>

- <span data-ttu-id="f054f-125">選取專案價目表，然後選取子格上的 **刪除合約專案價目表**。</span><span class="sxs-lookup"><span data-stu-id="f054f-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="f054f-126">價目表會從合約上的專案價目表中移除。</span><span class="sxs-lookup"><span data-stu-id="f054f-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="f054f-127">不會將價目表本身刪除。</span><span class="sxs-lookup"><span data-stu-id="f054f-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="f054f-128">只是刪除與合約的關聯。</span><span class="sxs-lookup"><span data-stu-id="f054f-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="f054f-129">在合約上設定專案價目表的自動設定預設</span><span class="sxs-lookup"><span data-stu-id="f054f-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="f054f-130">專案價目表可以設定為預設專案價目表。</span><span class="sxs-lookup"><span data-stu-id="f054f-130">A project price list can be set up as the default project price list.</span></span> <span data-ttu-id="f054f-131">這項設定可確保您組織中的所有合約一律都是以該價格期間的標準專案價目表為開始。</span><span class="sxs-lookup"><span data-stu-id="f054f-131">This setup ensures that all contracts in your organization always start with a standard project price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="f054f-132">設定專案價目表的組織預設值</span><span class="sxs-lookup"><span data-stu-id="f054f-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="f054f-133">移至 **設定** > **一般**，然後選取 **參數**。</span><span class="sxs-lookup"><span data-stu-id="f054f-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="f054f-134">在 **使用中參數** 清單頁面中，選取並按兩下記錄加以開啟。</span><span class="sxs-lookup"><span data-stu-id="f054f-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="f054f-135">按兩下時，請確定您所按下的欄位值不是超連結。</span><span class="sxs-lookup"><span data-stu-id="f054f-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="f054f-136">在 **使用中參數** 頁面上，選取 **價目表** 索引標籤。子格會顯示預設價目表的清單。</span><span class="sxs-lookup"><span data-stu-id="f054f-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="f054f-137">這是標準成本及銷售價目表的清單。</span><span class="sxs-lookup"><span data-stu-id="f054f-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="f054f-138">您銷售所用的每一種計價貨幣都有此處關聯的 **銷售** 價目表，可確保銷售價目表會是您為使用此貨幣進行交易之客戶所建立的任何合約上的預設值。</span><span class="sxs-lookup"><span data-stu-id="f054f-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="f054f-139">設定特定客戶適用的專案價目表</span><span class="sxs-lookup"><span data-stu-id="f054f-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="f054f-140">您也可以在與客戶議定主要定價合約時，設定客戶特定的專案價目表。</span><span class="sxs-lookup"><span data-stu-id="f054f-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="f054f-141">移至 **銷售** > **客戶**。</span><span class="sxs-lookup"><span data-stu-id="f054f-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="f054f-142">從現行客戶清單中，選取有特殊價目表的客戶。</span><span class="sxs-lookup"><span data-stu-id="f054f-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="f054f-143">選取要加以開啟的客戶記錄，然後選取 **專案價目表** 索引標籤。子格會顯示此客戶特有的專案價目表清單。</span><span class="sxs-lookup"><span data-stu-id="f054f-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="f054f-144">在此處建立新的價目表關聯，讓專案價目表專屬於此客戶。</span><span class="sxs-lookup"><span data-stu-id="f054f-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="f054f-145">專案合約上的自訂定價</span><span class="sxs-lookup"><span data-stu-id="f054f-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="f054f-146">有了組織和客戶特定的預設專案價目表之後，系統就會自動使用這些專案價目表關聯來建立您的專案合約。</span><span class="sxs-lookup"><span data-stu-id="f054f-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="f054f-147">不過，系統一律會複製專案合約上的專案價目表，並將日期和合約名稱附加至其複本。</span><span class="sxs-lookup"><span data-stu-id="f054f-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="f054f-148">客戶經理和專案經理接著即可開始編輯這些複本上的價格。</span><span class="sxs-lookup"><span data-stu-id="f054f-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="f054f-149">這些變更過的價格將只適用於此專案合約。</span><span class="sxs-lookup"><span data-stu-id="f054f-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
