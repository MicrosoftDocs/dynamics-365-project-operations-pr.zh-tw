---
title: 資源管理員指南
description: Project Service 的資源管理指南
author: JohnPBurrows
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
ms.openlocfilehash: 04ee87e5b1a2cf96434f4862e07d2b85bad9eace
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123998"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="8577c-103">資源管理員指南 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="8577c-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8577c-104">[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] 中的 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 功能可幫助您在理想的時機找到適合專案的正確資源，並確保有效使用所有資源。</span><span class="sxs-lookup"><span data-stu-id="8577c-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="8577c-105">使用 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]有效率且有效地部署公司的顧問。</span><span class="sxs-lookup"><span data-stu-id="8577c-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="8577c-106">這些功能可為您提供根據諮詢專案的需求和時間表，以及技能和顧問有空的時間，排程資源所需的工具。</span><span class="sxs-lookup"><span data-stu-id="8577c-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="8577c-107">您可以快速找到有空處理專案且最符合資格的顧問，而且可以輕鬆看到如何在每個專案的過程中以較佳的方式進行排程。</span><span class="sxs-lookup"><span data-stu-id="8577c-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="8577c-108">資源排程可幫助您執行下列事項：</span><span class="sxs-lookup"><span data-stu-id="8577c-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="8577c-109">將資源與專案配對，根據其技能和熟練度符合專案資源需求的程度。</span><span class="sxs-lookup"><span data-stu-id="8577c-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="8577c-110">比對資源的排程與專案行事曆，根據其可用性和排定的休假。</span><span class="sxs-lookup"><span data-stu-id="8577c-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="8577c-111">以色彩編碼的行事曆可提供有關資源可用性的視覺提示。</span><span class="sxs-lookup"><span data-stu-id="8577c-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="8577c-112">檢閱每位顧問的產能，並判斷該產能目前的使用情形。</span><span class="sxs-lookup"><span data-stu-id="8577c-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="8577c-113">這可協助您找出顧問可能未善加利用或過度利用的地方，或是否依產能工作。</span><span class="sxs-lookup"><span data-stu-id="8577c-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="8577c-114">指派百分比或特定小時數，做為工作者對專案的產能。</span><span class="sxs-lookup"><span data-stu-id="8577c-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="8577c-115">進行群組資源預訂。</span><span class="sxs-lookup"><span data-stu-id="8577c-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="8577c-116">未確認預約或已確認預約資源，並利用一個步驟將未確認預約的時數轉換成已確認預約的時數。</span><span class="sxs-lookup"><span data-stu-id="8577c-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="8577c-117">自動組成專案團隊，根據專案的分工結構圖中定義的資源。</span><span class="sxs-lookup"><span data-stu-id="8577c-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="8577c-118">履行資源要求 (預約、提案、尋找替代資源)。</span><span class="sxs-lookup"><span data-stu-id="8577c-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="8577c-119">根據集中 (資源管理員指派) 或混合模式 (資源管理員和其他經理可指派) 指派資源。</span><span class="sxs-lookup"><span data-stu-id="8577c-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="8577c-120">如需設定集中或混合資源管理模式的詳細資訊，請參閱[設定其他參數設定 (Project Service)](../psa/configure-additional-parameters-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="8577c-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="8577c-121">您可以在不同專案之間有效管理資源，並確認專案獲得適當的人員配置。</span><span class="sxs-lookup"><span data-stu-id="8577c-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="8577c-122">您將需要執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="8577c-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="8577c-123">[管理資源要求](../psa/manage-resource-requests.md)。</span><span class="sxs-lookup"><span data-stu-id="8577c-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="8577c-124">比對您的顧問的技能和熟練度與適合的專案。</span><span class="sxs-lookup"><span data-stu-id="8577c-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="8577c-125">[檢視資源可用性](../psa/view-resource-availability.md)。</span><span class="sxs-lookup"><span data-stu-id="8577c-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="8577c-126">在行事曆檢視中查看顧問的可用性。</span><span class="sxs-lookup"><span data-stu-id="8577c-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="8577c-127">[檢視資源使用率](../psa/view-resource-utilization.md)。</span><span class="sxs-lookup"><span data-stu-id="8577c-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="8577c-128">查看您的顧問目前已預約的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="8577c-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="8577c-129">[排程專案的資源](../psa/schedule-resources-project.md)。</span><span class="sxs-lookup"><span data-stu-id="8577c-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="8577c-130">排程專案的顧問。</span><span class="sxs-lookup"><span data-stu-id="8577c-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="8577c-131">如需針對個別專案送出資源要求的詳細資訊，請參閱[送出資源要求](../psa/submit-resource-requests.md)。</span><span class="sxs-lookup"><span data-stu-id="8577c-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="8577c-132">請參閱</span><span class="sxs-lookup"><span data-stu-id="8577c-132">See Also</span></span>  
 <span data-ttu-id="8577c-133">[Project Service 概觀](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="8577c-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="8577c-134">[系統管理員指南](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="8577c-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="8577c-135">[客戶經理指南](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="8577c-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="8577c-136">[專案經理指南](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="8577c-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="8577c-137">時間、費用及共同作業指南</span><span class="sxs-lookup"><span data-stu-id="8577c-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
