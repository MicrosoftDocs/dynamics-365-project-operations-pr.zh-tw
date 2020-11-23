---
title: 設定 Project Service Automation
description: 設定 Project Service 的步驟
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129173"
---
# <a name="configure-project-service"></a><span data-ttu-id="7c962-103">設定 Project Service</span><span class="sxs-lookup"><span data-stu-id="7c962-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="7c962-104">在使用 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] 中的[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]自動化功能管理客戶、專案及資源之前，您需要先完成幾個設定步驟，確保[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]解決方案符合貴組織的需求。</span><span class="sxs-lookup"><span data-stu-id="7c962-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="7c962-105">這些步驟包括：</span><span class="sxs-lookup"><span data-stu-id="7c962-105">These steps include:</span></span>  
  
-   <span data-ttu-id="7c962-106">[設定時間單位](../psa/set-up-time-units.md)。</span><span class="sxs-lookup"><span data-stu-id="7c962-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="7c962-107">設定產品類別目錄中的時間單位，用來當做專案排程和計費的基準。</span><span class="sxs-lookup"><span data-stu-id="7c962-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="7c962-108">[設定貨幣和匯率](../psa/set-up-currencies-exchange-rates.md)。</span><span class="sxs-lookup"><span data-stu-id="7c962-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="7c962-109">設定專案使用的貨幣。</span><span class="sxs-lookup"><span data-stu-id="7c962-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="7c962-110">[建立組織單位](../psa/create-organizational-units.md)。</span><span class="sxs-lookup"><span data-stu-id="7c962-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="7c962-111">設定公司用來分割業務的群組，無論是依地理區域、業務功能或其他邏輯部門。</span><span class="sxs-lookup"><span data-stu-id="7c962-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="7c962-112">[設定發票週期](../psa/set-up-invoice-frequencies.md)。</span><span class="sxs-lookup"><span data-stu-id="7c962-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="7c962-113">設定要用於向客戶收費的時段。</span><span class="sxs-lookup"><span data-stu-id="7c962-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="7c962-114">[設定交易類別](../psa/configure-transaction-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="7c962-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="7c962-115">設定您的顧問可針對其可計費和不可計費的費用收費的交易類別。</span><span class="sxs-lookup"><span data-stu-id="7c962-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="7c962-116">[設定費用類別](../psa/configure-expense-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="7c962-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="7c962-117">設定您的顧問可針對其可計費和不可計費的費用收費的類別。</span><span class="sxs-lookup"><span data-stu-id="7c962-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="7c962-118">[建立產品類別目錄項目](../psa/create-product-catalog-items.md)。</span><span class="sxs-lookup"><span data-stu-id="7c962-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="7c962-119">新增您銷售的產品至產品類別目錄，例如軟體授權。</span><span class="sxs-lookup"><span data-stu-id="7c962-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="7c962-120">[建立價目表](../psa/create-price-list.md)。</span><span class="sxs-lookup"><span data-stu-id="7c962-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="7c962-121">設定不同的價目表，根據要針對客戶專案所需的每個角色向客戶收取的費用。</span><span class="sxs-lookup"><span data-stu-id="7c962-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="7c962-122">[設定資源](../psa/set-up-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="7c962-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="7c962-123">新增專案所需的技能、熟練度、資源角色及其他資源資訊。</span><span class="sxs-lookup"><span data-stu-id="7c962-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7c962-124">請參閱</span><span class="sxs-lookup"><span data-stu-id="7c962-124">See Also</span></span>  
 <span data-ttu-id="7c962-125">[Project Service Automation 概觀](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="7c962-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="7c962-126">[設定 Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="7c962-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="7c962-127">[客戶經理指南](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="7c962-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="7c962-128">[專案經理指南](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="7c962-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="7c962-129">[資源管理員指南](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="7c962-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="7c962-130">時間、費用及共同作業指南</span><span class="sxs-lookup"><span data-stu-id="7c962-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
