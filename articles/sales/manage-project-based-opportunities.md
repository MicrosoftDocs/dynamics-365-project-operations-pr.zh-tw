---
title: 管理專案型商機
description: 本主題提供有關如何使用與專案相關之商機的資訊。
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d1f9b29e0e9516ff78517e47694a2385c083ec7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277823"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="e5b36-103">管理專案型商機</span><span class="sxs-lookup"><span data-stu-id="e5b36-103">Manage project-based opportunities</span></span>

<span data-ttu-id="e5b36-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="e5b36-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5b36-105">以專案為主的公司通常都會分佈在多個國家/地區和地理位置，展開其交付作業。</span><span class="sxs-lookup"><span data-stu-id="e5b36-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="e5b36-106">專案執行及交付成本會根據管理交付的地理位置或部門不同而不同。</span><span class="sxs-lookup"><span data-stu-id="e5b36-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="e5b36-107">反過來，這可能會影響交易的利潤。</span><span class="sxs-lookup"><span data-stu-id="e5b36-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="e5b36-108">交付專案型服務通常需要大量人力資源時間、可觀差旅費用、材料成本及其他費用。</span><span class="sxs-lookup"><span data-stu-id="e5b36-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="e5b36-109">Dynamics 365 Project Operations 中的專案型商機是使用 Dynamics 365 Sales 的擴充功能所設計。</span><span class="sxs-lookup"><span data-stu-id="e5b36-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="e5b36-110">主題提供有關包含在專案型公司管理專案型商機所需之其他功能中的不同欄位與商務規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e5b36-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="e5b36-111">檢視所有專案型商機</span><span class="sxs-lookup"><span data-stu-id="e5b36-111">View all project-based opportunities</span></span>

<span data-ttu-id="e5b36-112">您可以從 **商機** 清單頁面查看所有專案型商機的清單。</span><span class="sxs-lookup"><span data-stu-id="e5b36-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="e5b36-113">移至 **銷售** > **商機**。</span><span class="sxs-lookup"><span data-stu-id="e5b36-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="e5b36-114">使用 **檢視表切換器** 來選取商機的其他篩選過的檢視。</span><span class="sxs-lookup"><span data-stu-id="e5b36-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="e5b36-115">若要設定這些檢視表和導覽選項，您可以使用自訂篩選準則來建立您自己的檢視表。</span><span class="sxs-lookup"><span data-stu-id="e5b36-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="e5b36-116">您可以從此清單頁面或詳細資料頁面建立或刪除專案商機。</span><span class="sxs-lookup"><span data-stu-id="e5b36-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="e5b36-117">專案型交易的商務程序流程</span><span class="sxs-lookup"><span data-stu-id="e5b36-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="e5b36-118">Project Operations 中的專案型交易支援下列商務程序流程：</span><span class="sxs-lookup"><span data-stu-id="e5b36-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="e5b36-119">潛在客戶變商機商務程序</span><span class="sxs-lookup"><span data-stu-id="e5b36-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="e5b36-120">商機銷售處理</span><span class="sxs-lookup"><span data-stu-id="e5b36-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="e5b36-121">潛在客戶變商機商務程序</span><span class="sxs-lookup"><span data-stu-id="e5b36-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="e5b36-122">潛在客戶變商機商務程序支援下列階段：</span><span class="sxs-lookup"><span data-stu-id="e5b36-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="e5b36-123">階段</span><span class="sxs-lookup"><span data-stu-id="e5b36-123">Stage</span></span> | <span data-ttu-id="e5b36-124">對應的實體</span><span class="sxs-lookup"><span data-stu-id="e5b36-124">Mapped entity</span></span> | <span data-ttu-id="e5b36-125">功能</span><span class="sxs-lookup"><span data-stu-id="e5b36-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e5b36-126">授與資格​​</span><span class="sxs-lookup"><span data-stu-id="e5b36-126">Qualify</span></span> | <span data-ttu-id="e5b36-127">潛在客戶​​</span><span class="sxs-lookup"><span data-stu-id="e5b36-127">Lead</span></span> | <span data-ttu-id="e5b36-128">授與潛在客戶資格以建立客戶、連絡人和商機。</span><span class="sxs-lookup"><span data-stu-id="e5b36-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="e5b36-129">開發</span><span class="sxs-lookup"><span data-stu-id="e5b36-129">Develop</span></span> | <span data-ttu-id="e5b36-130">商機​​</span><span class="sxs-lookup"><span data-stu-id="e5b36-130">Opportunity</span></span> | <span data-ttu-id="e5b36-131">開發商機以新增有關所涉及工作、主要利害關係人和競爭者的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e5b36-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="e5b36-132">提案</span><span class="sxs-lookup"><span data-stu-id="e5b36-132">Propose</span></span> | <span data-ttu-id="e5b36-133">商機​​</span><span class="sxs-lookup"><span data-stu-id="e5b36-133">Opportunity</span></span> | <span data-ttu-id="e5b36-134">開發提案，並取得內部審查團隊的核准。</span><span class="sxs-lookup"><span data-stu-id="e5b36-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="e5b36-135">關閉​​</span><span class="sxs-lookup"><span data-stu-id="e5b36-135">Close</span></span> | <span data-ttu-id="e5b36-136">商機​​</span><span class="sxs-lookup"><span data-stu-id="e5b36-136">Opportunity</span></span> | <span data-ttu-id="e5b36-137">贏得商機以完成交易。</span><span class="sxs-lookup"><span data-stu-id="e5b36-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="e5b36-138">商機銷售處理</span><span class="sxs-lookup"><span data-stu-id="e5b36-138">Opportunity sales process</span></span>
<span data-ttu-id="e5b36-139">Project Operations 中的商機銷售處理是 Sales 應用程式中商機銷售處理商業流程的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="e5b36-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="e5b36-140">此商務程序已設計為現成可用，以便在專案型商機中支援下列階段。</span><span class="sxs-lookup"><span data-stu-id="e5b36-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="e5b36-141">階段</span><span class="sxs-lookup"><span data-stu-id="e5b36-141">Stage</span></span> | <span data-ttu-id="e5b36-142">對應的實體</span><span class="sxs-lookup"><span data-stu-id="e5b36-142">Mapped entity</span></span> | <span data-ttu-id="e5b36-143">功能</span><span class="sxs-lookup"><span data-stu-id="e5b36-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e5b36-144">授與資格​​</span><span class="sxs-lookup"><span data-stu-id="e5b36-144">Qualify</span></span> | <span data-ttu-id="e5b36-145">商機​​</span><span class="sxs-lookup"><span data-stu-id="e5b36-145">Opportunity</span></span> | <span data-ttu-id="e5b36-146">授與潛在客戶資格以建立客戶、連絡人和商機。</span><span class="sxs-lookup"><span data-stu-id="e5b36-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="e5b36-147">提案</span><span class="sxs-lookup"><span data-stu-id="e5b36-147">Propose</span></span> | <span data-ttu-id="e5b36-148">報價</span><span class="sxs-lookup"><span data-stu-id="e5b36-148">Quote</span></span> | <span data-ttu-id="e5b36-149">使用專案報價開發提案，並取得內部審查團隊的核准。</span><span class="sxs-lookup"><span data-stu-id="e5b36-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="e5b36-150">合約</span><span class="sxs-lookup"><span data-stu-id="e5b36-150">Contract</span></span> | <span data-ttu-id="e5b36-151">專案合約</span><span class="sxs-lookup"><span data-stu-id="e5b36-151">Project Contract</span></span> | <span data-ttu-id="e5b36-152">贏得報價成交以建立合約，並開始專案的執行與交付。</span><span class="sxs-lookup"><span data-stu-id="e5b36-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="e5b36-153">關閉​​</span><span class="sxs-lookup"><span data-stu-id="e5b36-153">Close</span></span> | <span data-ttu-id="e5b36-154">專案合約</span><span class="sxs-lookup"><span data-stu-id="e5b36-154">Project Contract</span></span> | <span data-ttu-id="e5b36-155">成功完成工作並結束專案合約。</span><span class="sxs-lookup"><span data-stu-id="e5b36-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="e5b36-156">如果專案型交易是從潛在客戶起始，則優先考慮潛在客戶變商機商務程序。</span><span class="sxs-lookup"><span data-stu-id="e5b36-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="e5b36-157">如果專案型交易是從商機起始，則優先考慮商機銷售處理。</span><span class="sxs-lookup"><span data-stu-id="e5b36-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="e5b36-158">您可以編輯產品商務程序流程，也可以建立您自己的商務程序流程，視需要來追蹤銷售處理。</span><span class="sxs-lookup"><span data-stu-id="e5b36-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="e5b36-159">如需商務程序流程的詳細資訊，請參閱[商務程序流程概觀](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview)。</span><span class="sxs-lookup"><span data-stu-id="e5b36-159">For more information about the business process flow, see [Business process flows overview](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]