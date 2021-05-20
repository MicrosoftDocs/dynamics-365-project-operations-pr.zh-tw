---
title: Project Operations 設定和設定資料整合
description: 本主題提供有關設定和配置 Project Operations 雙重寫入對應的資訊。
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938958"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a><span data-ttu-id="51f25-103">Project Operations 設定和設定資料整合</span><span class="sxs-lookup"><span data-stu-id="51f25-103">Project Operations setup and configuration data integration</span></span>

<span data-ttu-id="51f25-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="51f25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="51f25-105">本主題提供有關 Project Operations 雙重寫入設定和設定資料整合的資訊。</span><span class="sxs-lookup"><span data-stu-id="51f25-105">This topic provides information about Project Operations dual-write integration for setup and configuration entities.</span></span>

## <a name="project-contracts-contract-lines-and-projects"></a><span data-ttu-id="51f25-106">專案合約、合約服務內容和專案</span><span class="sxs-lookup"><span data-stu-id="51f25-106">Project contracts, contract lines, and projects</span></span>

<span data-ttu-id="51f25-107">專案合約、合約服務內容和專案是在 Dataverse 中所建立，並同步處理至 Finance and Operations應用程式以用於其他會計。</span><span class="sxs-lookup"><span data-stu-id="51f25-107">Project contracts, contract lines, and projects are created in Dataverse and synchronized to Finance and Operations apps for additional accounting.</span></span> <span data-ttu-id="51f25-108">您只能在 Dataverse 中建立和刪除這些實體中的記錄。</span><span class="sxs-lookup"><span data-stu-id="51f25-108">The records in these entities can be created and deleted only in Dataverse.</span></span> <span data-ttu-id="51f25-109">不過，在 Finance and Operations 應用程式中，可以將會計屬性 (例如銷售稅群組預設值和財務維度) 新增至這些記錄。</span><span class="sxs-lookup"><span data-stu-id="51f25-109">However, accounting attributes such as sales tax group defaults and financial dimensions can be added to these records in the Finance and Operations apps.</span></span>

  ![專案合約整合概念](./media/1ProjectContract.jpg)

<span data-ttu-id="51f25-111">銷售活動潛在客戶、商機和報價是在 Dataverse 中進行追蹤，並不會同步處理至 Finance and Operations 應用程式，因為沒有與此活動相關聯的下游會計。</span><span class="sxs-lookup"><span data-stu-id="51f25-111">Sales activity leads, opportunities, and quotes are tracked in Dataverse and don't synchronize to Finance and Operations apps because there is no downstream accounting associated with this activity.</span></span>

<span data-ttu-id="51f25-112">Dataverse 中的專案合約功能會使用 **專案合約標題 (salesorders)** 資料表對應，在 Finance and Operations 應用程式中建立專案合約記錄。</span><span class="sxs-lookup"><span data-stu-id="51f25-112">The project contract functionality in Dataverse creates a project contract record in Finance and Operations apps using the **Project contract headers (salesorders)** table map.</span></span> <span data-ttu-id="51f25-113">在 Dataverse 中儲存專案合約，也會開始建立專案合約客戶實體記錄。</span><span class="sxs-lookup"><span data-stu-id="51f25-113">Saving a project contract in Dataverse also starts the creation of a project contract customer entity record.</span></span> <span data-ttu-id="51f25-114">此記錄會使用 **專案資金來源 (msdyn\_projectcontractssplitbillingrules)** 資料表對應來同步處理至 Finance and Operations 應用程式。</span><span class="sxs-lookup"><span data-stu-id="51f25-114">This record is synchronized to Finance and Operations apps using the **Project funding source (msdyn\_projectcontractssplitbillingrules)** table map.</span></span> <span data-ttu-id="51f25-115">此對應也會同步處理專案合約客戶的新增、更新和刪除。</span><span class="sxs-lookup"><span data-stu-id="51f25-115">This map also synchronizes project contract customer additions, updates, and deletions.</span></span> <span data-ttu-id="51f25-116">專案合約之間的分割帳單百分比只能以 Dataverse 來主控，並不會同步處理至 Finance and Operations 應用程式。</span><span class="sxs-lookup"><span data-stu-id="51f25-116">Split billing percentages between project contract customers are mastered only in Dataverse and not synchronized to Finance and Operations apps.</span></span>

<span data-ttu-id="51f25-117">在 Dataverse 中建立專案合約之後，專案會計師可以移至 **專案管理與會計** > **專案合約** > **設定** > **顯示預設會計**，在 Finance and Operations 應用程式中更新此專案合約的會計屬性。</span><span class="sxs-lookup"><span data-stu-id="51f25-117">After a project contract is created in Dataverse, the project accountant can update the accounting attributes for this project contract in Finance and Operations apps by going to **Project management and accounting** > **Project contracts** > **Set up** > **Show default accounting**.</span></span> <span data-ttu-id="51f25-118">會計師可在 Finance and Operations 應用程式中選取專案合約識別碼 (這樣會在 Dataverse 中開啟相關的專案合約記錄)，以審查營運專案合約屬性，例如要求的交貨日期和合約金額。</span><span class="sxs-lookup"><span data-stu-id="51f25-118">The accountant can review operational project contract attributes, such as requested delivery date and contract amount by selecting the project contract ID in Finance and Operations apps which opens the related project contract record in Dataverse.</span></span>

<span data-ttu-id="51f25-119">專案實體會使用 **專案 V2 (msdyn\_projects)** 資料表對應來同步處理至 Finance and Operations 應用程式。</span><span class="sxs-lookup"><span data-stu-id="51f25-119">The project entity is synchronized to Finance and Operations apps using the **Projects V2 (msdyn\_projects)** table map.</span></span> <span data-ttu-id="51f25-120">專案會計師可以：</span><span class="sxs-lookup"><span data-stu-id="51f25-120">The project accountant can:</span></span>

  - <span data-ttu-id="51f25-121">移至 **專案管理與會計** > **所有專案**，以審查 Finance and Operations 應用程式中的專案。</span><span class="sxs-lookup"><span data-stu-id="51f25-121">Review projects in Finance and Operations apps by going to **Project management and accounting** > **All projects**.</span></span> 
  - <span data-ttu-id="51f25-122">移至 **專案管理與會計** > **所有專案** > **設定** > **顯示預設會計**，以更新 Finance and Operations 應用程式中專案的會計屬性。</span><span class="sxs-lookup"><span data-stu-id="51f25-122">Update accounting attributes for the project in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Set up** > **Show default accounting**.</span></span>  
  - <span data-ttu-id="51f25-123">在 Finance and Operations 應用程式中選取專案識別碼 (這樣會在 Dataverse 中開啟相關的專案記錄)，以審查營運專案屬性，例如估計開始和結束日期。</span><span class="sxs-lookup"><span data-stu-id="51f25-123">Review operational project attributes, such as estimated start and end dates, by selecting the project ID in Finance and Operations apps which opens the related project record in Dataverse.</span></span>

<span data-ttu-id="51f25-124">專案是透過 **專案合約服務內容** 實體與專案合約建立關聯。</span><span class="sxs-lookup"><span data-stu-id="51f25-124">A project is associated with a project contract through the **Project contract line** entity.</span></span>

<span data-ttu-id="51f25-125">Dataverse 中的專案合約服務內容會使用 **專案合約服務內容 (salesorderdetails)** 資料表對應，在 Finance and Operations 應用程式中建立專案合約帳單規則。</span><span class="sxs-lookup"><span data-stu-id="51f25-125">Project contract lines in Dataverse creates a project contract billing rule in Finance and Operations apps using the **Project contract lines (salesorderdetails)** table map.</span></span> <span data-ttu-id="51f25-126">帳務方式會在 Finance and Operations 應用程式中定義專案合約帳單規則類型：</span><span class="sxs-lookup"><span data-stu-id="51f25-126">The billing method defines the project contract billing rule type in Finance and Operations apps:</span></span>

  - <span data-ttu-id="51f25-127">使用時間和材料帳務方式的專案合約服務內容建立時間和材料類型的帳單規則。</span><span class="sxs-lookup"><span data-stu-id="51f25-127">Project contract lines with a billing method of time and material create a billing rule of time and material type.</span></span>
  - <span data-ttu-id="51f25-128">固定價格帳務方式合約服務內容會建立里程碑帳單規則。</span><span class="sxs-lookup"><span data-stu-id="51f25-128">Fixed price billing method contract lines create a milestone billing rule.</span></span>

<span data-ttu-id="51f25-129">專案會計師可以在 Finance and Operations 應用程式中審查專案合約服務內容，方法是移至 **專案管理與會計** > **專案合約** > **設定** > **顯示預設會計**，然後檢閱 **合約服務內容** 索引標籤上的詳細資料。會計師也可以在此索引標籤上設定固定價格帳務方式合約服務內容的預設財務維度。</span><span class="sxs-lookup"><span data-stu-id="51f25-129">Project contract lines can be reviewed by the project accountant in Finance and Operations apps by going to **Project management and accounting** > **Project contracts** > **Set up** > **Show default accounting**, and reviewing the details on the **Contract lines** tab. The accountant can also set default financial dimensions for the fixed price billing method contract lines on this tab.</span></span>

## <a name="billing-milestones"></a><span data-ttu-id="51f25-130">帳單里程碑</span><span class="sxs-lookup"><span data-stu-id="51f25-130">Billing milestones</span></span>

<span data-ttu-id="51f25-131">使用固定價格帳務方式的專案合約服務內容會透過帳單里程碑開立發票。</span><span class="sxs-lookup"><span data-stu-id="51f25-131">Project contract lines using the fixed price billing method are invoiced through billing milestones.</span></span> <span data-ttu-id="51f25-132">帳單里程碑會使用 **Project Operations 整合合約服務內容里程碑 (msdyn\_contractlinescheduleofvalues)** 資料表對應，同步處理至 Finance and Operations 應用程式中的專案記帳交易，</span><span class="sxs-lookup"><span data-stu-id="51f25-132">Billing milestones are synchronized to project on-account transactions in Finance and Operations apps by using the **Project Operations integration contract line milestones (msdyn\_contractlinescheduleofvalues)** table map.</span></span>

  ![帳單里程碑整合](./media/2Milestones.jpg)

<span data-ttu-id="51f25-134">會計師可以審查記帳交易記錄並調整這些交易記錄的會計屬性，方法是移至 **專案管理與會計** > **專案合約** > **維護** > **記帳交易**，或移至 **專案管理與會計** > **所有專案** > **維護** > **記帳交易**。</span><span class="sxs-lookup"><span data-stu-id="51f25-134">The accountant can review on-account transactions and adjust the accounting attributes for those transactions by going to **Project management and accounting** > **Project contracts** > **Maintain** > **On-account transactions** or **Project management and accounting** > **All projects** > **Maintain** > **On-account transactions**.</span></span>

<span data-ttu-id="51f25-135">第一次建立指定專案合約服務內容的帳單里程碑時，系統會自動為與此合約服務內容相關聯的專案建立固定價格營收估計專案。</span><span class="sxs-lookup"><span data-stu-id="51f25-135">When you first create a billing milestone for a given project contract line, the system automatically creates a fixed price revenue estimate project for the project associated with this contract line.</span></span> <span data-ttu-id="51f25-136">您可移至 **專案管理與會計** > **固定價格營收估計專案**，以檢閱固定價格營收估計專案。</span><span class="sxs-lookup"><span data-stu-id="51f25-136">Fixed-price revenue estimate projects can be reviewed by going to **Project management and accounting** > **Fixed-price revenue estimate projects**.</span></span>

### <a name="project-tasks"></a><span data-ttu-id="51f25-137">專案工作</span><span class="sxs-lookup"><span data-stu-id="51f25-137">Project tasks</span></span>

<span data-ttu-id="51f25-138">專案工作會透過 **專案工作 (msdyn\_projecttasks)** 資料表對應同步處理至 Finance and Operations 應用程式，僅供參考之用。</span><span class="sxs-lookup"><span data-stu-id="51f25-138">Project tasks are synchronized to Finance and Operations apps through the **Project tasks (msdyn\_projecttasks)** table map for reference purposes only.</span></span> <span data-ttu-id="51f25-139">建立、更新和刪除作業無法透過 Finance and Operations 應用程式來支援。</span><span class="sxs-lookup"><span data-stu-id="51f25-139">Creating, updating, and deleting operations isn't supported through Finance and Operations apps.</span></span>

  ![專案工作整合](./media/3Tasks.jpg)

## <a name="project-resources"></a><span data-ttu-id="51f25-141">專案資源</span><span class="sxs-lookup"><span data-stu-id="51f25-141">Project resources</span></span>

<span data-ttu-id="51f25-142">**專案資源角色** 實體會使用 **所有公司的專案資源角色 (bookableresourcecategories)** 資料表對應同步處理至 Finance and Operations 應用程式，僅供參考之用。</span><span class="sxs-lookup"><span data-stu-id="51f25-142">The **Project resource roles** entity is synchronized to Finance and Operations apps using the **Project resource roles for all companies (bookableresourcecategories)** table map for reference purposes only.</span></span> <span data-ttu-id="51f25-143">由於 Dataverse 中的資源角色不是公司所特有，因此系統會自動在 Finance and Operations 應用程式中，針對所有已納入雙重寫入整合範圍的法律實體，建立各自的公司特定資源角色記錄。</span><span class="sxs-lookup"><span data-stu-id="51f25-143">Because resource roles in Dataverse are not company-specific, the system automatically creates respective company-specific resource roles records in Finance and Operations apps automatically for all legal entities included into dual-write integration scope.</span></span>

![資源角色整合](./media/5Resources.jpg)

<span data-ttu-id="51f25-145">Project Operations 中的專案資源會保留在 Dataverse 中，並不會同步處理至 Finance and Operations 應用程式。</span><span class="sxs-lookup"><span data-stu-id="51f25-145">Project resources in Project Operations are maintained in Dataverse and aren't synchronized to Finance and Operations apps.</span></span>

### <a name="transaction-categories"></a><span data-ttu-id="51f25-146">交易類別</span><span class="sxs-lookup"><span data-stu-id="51f25-146">Transaction categories</span></span>

<span data-ttu-id="51f25-147">交易類別會保留在 Dataverse 中，並使用 **專案交易類別 (msdyn\_transactioncategories)** 資料表對應同步處理至 Finance and Operations 應用程式。</span><span class="sxs-lookup"><span data-stu-id="51f25-147">Transaction categories are maintained in Dataverse and synchronized to Finance and Operations apps using the **Project transaction categories (msdyn\_transactioncategories)** table map.</span></span> <span data-ttu-id="51f25-148">同步處理交易類別記錄之後，系統會自動建立四個共用類別記錄。</span><span class="sxs-lookup"><span data-stu-id="51f25-148">After the transaction category record is synchronized, the system automatically creates four shared category records.</span></span> <span data-ttu-id="51f25-149">每個記錄都對應至 Finance and Operations 應用程式中的交易類型，並將它們連結至交易類別記錄。</span><span class="sxs-lookup"><span data-stu-id="51f25-149">Each record corresponds to a transaction type in Finance and Operations apps and links them to the transaction category record.</span></span>

![交易類別整合](./media/4TransactionCategories.jpg)

<span data-ttu-id="51f25-151">對估計值和實際值使用交易類別時，需要專案會計師或系統管理員在每個法律實體中建立對應的專案類別。</span><span class="sxs-lookup"><span data-stu-id="51f25-151">Using transaction categories for estimates and actuals requires the project accountant or system administrator to create corresponding project categories in every legal entity.</span></span> <span data-ttu-id="51f25-152">如需詳細資訊，請參閱[設定專案類別](../project-accounting/configure-project-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="51f25-152">For more information, see [Configure project categories](../project-accounting/configure-project-categories.md).</span></span>
