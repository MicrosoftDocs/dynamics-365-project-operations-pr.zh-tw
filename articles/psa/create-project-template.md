---
title: 建立專案範本
description: 如何建立 Project Service 中的專案範本
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
ms.openlocfilehash: e8a9b75aa0721c6e7c85c2bca8796bf9f2c6d3db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285113"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="c612b-103">建立專案範本 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c612b-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c612b-104">專案範本節省您的時間，如果公司定期投標類似類型的專案。</span><span class="sxs-lookup"><span data-stu-id="c612b-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="c612b-105">它們為一種專案類型提供一組標準的角色和預估時數。</span><span class="sxs-lookup"><span data-stu-id="c612b-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="c612b-106">客戶經理和專案經理可以依據專案範本建立專案，或是複製專案範本並製作自己的範本。</span><span class="sxs-lookup"><span data-stu-id="c612b-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="c612b-107">專案範本的元件</span><span class="sxs-lookup"><span data-stu-id="c612b-107">Components of project template</span></span>
 <span data-ttu-id="c612b-108">專案範本包含三個元件：</span><span class="sxs-lookup"><span data-stu-id="c612b-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="c612b-109">**分工結構圖**：專案範本中的分工結構圖有一組與專案相同的元素。</span><span class="sxs-lookup"><span data-stu-id="c612b-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="c612b-110">您可以建立工作階層、關聯角色與工作、定義排程屬性、設定相依性，並檢視甘特圖中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="c612b-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="c612b-111">專案範本中的分工結構圖也支援每項工作的工作模式。</span><span class="sxs-lookup"><span data-stu-id="c612b-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="c612b-112">建立工作排程時，專案範本和專案之間並無差異。</span><span class="sxs-lookup"><span data-stu-id="c612b-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="c612b-113">**專案估計值**：專案估計值在範本中與專案中的運作方式相同，除了預設成本和售價的價目表一律會預設[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]參數中定義的成本和銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="c612b-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="c612b-114">其餘功能與專案中相同。</span><span class="sxs-lookup"><span data-stu-id="c612b-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="c612b-115">**專案團隊形成**：形成專案範本的專案團隊時，您無法預約範本中的具名資源。</span><span class="sxs-lookup"><span data-stu-id="c612b-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="c612b-116">您可以使用分工結構圖中的 **產生專案團隊** 產生一組一般資源。</span><span class="sxs-lookup"><span data-stu-id="c612b-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="c612b-117">您也可以為一般資源指定必要的技能和熟練度。</span><span class="sxs-lookup"><span data-stu-id="c612b-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="c612b-118">您無法將一般資源替代為專案範本中可預約的資源。</span><span class="sxs-lookup"><span data-stu-id="c612b-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="c612b-119">從範本建立專案</span><span class="sxs-lookup"><span data-stu-id="c612b-119">Create a project from a template</span></span>  
 <span data-ttu-id="c612b-120">您可以遵循下列方式從範本建立專案：</span><span class="sxs-lookup"><span data-stu-id="c612b-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="c612b-121">從報價建立專案時，您可以從專案快速建立表單中選擇專案範本。</span><span class="sxs-lookup"><span data-stu-id="c612b-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="c612b-122">按一下 **新專案** 建立專案時，專案表單會在您儲存記錄前顯示。</span><span class="sxs-lookup"><span data-stu-id="c612b-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="c612b-123">您可以從這裡按一下 **挑選範本** 欄位，從組織內預先定義的專案範本清單中選擇。</span><span class="sxs-lookup"><span data-stu-id="c612b-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="c612b-124">按一下 **專案範本** 頁面上的 **從範本建立專案**，可從範本建立專案。</span><span class="sxs-lookup"><span data-stu-id="c612b-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="c612b-125">將範本的元件複製到專案</span><span class="sxs-lookup"><span data-stu-id="c612b-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="c612b-126">當您將範本的元件複製到專案中時，應先了解幾件事情。</span><span class="sxs-lookup"><span data-stu-id="c612b-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="c612b-127">**複製分工結構圖**：當您從專案範本複製分工結構圖時，如果專案的專案行事曆與範本不同，則專案行事曆上的工作時數將會套用至工作的排程。</span><span class="sxs-lookup"><span data-stu-id="c612b-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="c612b-128">這會將排程調整為支援的專案行事曆。</span><span class="sxs-lookup"><span data-stu-id="c612b-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="c612b-129">同樣地，分工結構圖上的第一項工作會採用專案的開始日期，如此其餘工作階層排程就會依據範本的分工結構圖中指定的期間和相依性進行更新。</span><span class="sxs-lookup"><span data-stu-id="c612b-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="c612b-130">**複製專案估計值**：如果您跨專案估計明細複製，價目表就會根據成本價目表的專案和銷售價目表的客戶的擁有單位更新。</span><span class="sxs-lookup"><span data-stu-id="c612b-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="c612b-131">單位成本和售價是從專案上與銷售實體關聯的這些價目表決定。</span><span class="sxs-lookup"><span data-stu-id="c612b-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="c612b-132">**複製專案團隊**：您將專案團隊從範本複製到專案時，一般資源也會一併複製，還包括範本中定義的技能和熟練度。</span><span class="sxs-lookup"><span data-stu-id="c612b-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="c612b-133">一般資源指派也會維持與專案範本中一樣。</span><span class="sxs-lookup"><span data-stu-id="c612b-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c612b-134">請參閱</span><span class="sxs-lookup"><span data-stu-id="c612b-134">See Also</span></span>  
 [<span data-ttu-id="c612b-135">專案經理指南</span><span class="sxs-lookup"><span data-stu-id="c612b-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]