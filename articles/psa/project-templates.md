---
title: 專案範本
description: 此主題提供有關如何使用專案範本進行快速專案設定的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148048"
---
# <a name="project-templates"></a><span data-ttu-id="0bdae-103">專案範本</span><span class="sxs-lookup"><span data-stu-id="0bdae-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0bdae-104">專案範本是預先定義的架構，可協助您快速輕鬆地開始專案。</span><span class="sxs-lookup"><span data-stu-id="0bdae-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="0bdae-105">使用預先定義的範本，只需按一下即可建立新的專案。</span><span class="sxs-lookup"><span data-stu-id="0bdae-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="0bdae-106">至於專案，您必須定義專案範本的先決條件。</span><span class="sxs-lookup"><span data-stu-id="0bdae-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="0bdae-107">您必須為每個專案範本定義專案行事曆，而且必須在組織中預先定義角色和價目表，才能讓範本的元件具有實用的資料。</span><span class="sxs-lookup"><span data-stu-id="0bdae-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="0bdae-108">專案範本由三個元件組成：排程、專案估計值和專案團隊成員。</span><span class="sxs-lookup"><span data-stu-id="0bdae-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="0bdae-109">排程</span><span class="sxs-lookup"><span data-stu-id="0bdae-109">Schedule</span></span>

<span data-ttu-id="0bdae-110">專案範本的排程與專案的排程有相同的元素集合。</span><span class="sxs-lookup"><span data-stu-id="0bdae-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="0bdae-111">您可以建立工作階層、將角色與工作產生關聯、定義排程屬性，以及設定相依性。</span><span class="sxs-lookup"><span data-stu-id="0bdae-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="0bdae-112">專案範本中的排程還會支援個別工作的工作模式。</span><span class="sxs-lookup"><span data-stu-id="0bdae-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="0bdae-113">因此，它支援排程引擎。</span><span class="sxs-lookup"><span data-stu-id="0bdae-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="0bdae-114">您必須將專案行事曆與專案建立關聯。</span><span class="sxs-lookup"><span data-stu-id="0bdae-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="0bdae-115">建立作業排程時，專案範本和專案之間並無差異。</span><span class="sxs-lookup"><span data-stu-id="0bdae-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="0bdae-116">專案估計值</span><span class="sxs-lookup"><span data-stu-id="0bdae-116">Project estimates</span></span>

<span data-ttu-id="0bdae-117">專案範本的專案估計值與專案的專案估計值有相同的運作方式。</span><span class="sxs-lookup"><span data-stu-id="0bdae-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="0bdae-118">不過，成本價和銷售價是從參數所定義的預設成本和銷售價目表中提取而來。</span><span class="sxs-lookup"><span data-stu-id="0bdae-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="0bdae-119">從範本建立專案</span><span class="sxs-lookup"><span data-stu-id="0bdae-119">Creating a project from a template</span></span>
 
<span data-ttu-id="0bdae-120">有許多可以從專案範本建立專案的方法：</span><span class="sxs-lookup"><span data-stu-id="0bdae-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="0bdae-121">從報價建立專案時，您可以選取 **快速建立：專案** 對話方塊中的專案範本。</span><span class="sxs-lookup"><span data-stu-id="0bdae-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![[快速建立：專案] 對話方塊](media/project-11.png)

- <span data-ttu-id="0bdae-123">藉由選取 **新增專案** 建立專案時，**專案** 頁面會在儲存記錄之前出現。</span><span class="sxs-lookup"><span data-stu-id="0bdae-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="0bdae-124">在 **挑選範本** 欄位中，選取組織預先定義的其中一個專案範本。</span><span class="sxs-lookup"><span data-stu-id="0bdae-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="0bdae-125">使用 **範本實體** 頁面上的 **從範本建立專案**。</span><span class="sxs-lookup"><span data-stu-id="0bdae-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="0bdae-126">將範本的元件複製到專案</span><span class="sxs-lookup"><span data-stu-id="0bdae-126">Copying components of template to project</span></span>

<span data-ttu-id="0bdae-127">將專案範本的元件複製到專案時，視專案中的設定而定，可能會發生一些覆寫。</span><span class="sxs-lookup"><span data-stu-id="0bdae-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="0bdae-128">複製排程。</span><span class="sxs-lookup"><span data-stu-id="0bdae-128">Copying the schedule</span></span>

<span data-ttu-id="0bdae-129">從專案範本複製排程時，如果專案的專案行事曆與範本的不同，則專案行事曆中的工作時數會套用至工作排程。</span><span class="sxs-lookup"><span data-stu-id="0bdae-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="0bdae-130">如此一來，將會調整排程以符合支援的專案行事曆。</span><span class="sxs-lookup"><span data-stu-id="0bdae-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="0bdae-131">同樣地，排程上的第一項工作會採用專案的開始日期，而階層其餘工作的排程則依據範本中指定的期間和相依性進行更新。</span><span class="sxs-lookup"><span data-stu-id="0bdae-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="0bdae-132">複製專案估計值</span><span class="sxs-lookup"><span data-stu-id="0bdae-132">Copying project estimates</span></span> 

<span data-ttu-id="0bdae-133">在專案評估明細之間複製時，會更新價目表。</span><span class="sxs-lookup"><span data-stu-id="0bdae-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="0bdae-134">就成本價目表而言，這些更新是根據專案的擁有單位進行。</span><span class="sxs-lookup"><span data-stu-id="0bdae-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="0bdae-135">至於銷售價目表，則是根據客戶。</span><span class="sxs-lookup"><span data-stu-id="0bdae-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="0bdae-136">說到與銷售實體相關的專案，其單位成本和銷售價即是根據這些價目表來決定。</span><span class="sxs-lookup"><span data-stu-id="0bdae-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="0bdae-137">複製專案團隊</span><span class="sxs-lookup"><span data-stu-id="0bdae-137">Copying a project team</span></span>

<span data-ttu-id="0bdae-138">將專案團隊從專案範本複製到專案時，也會一併複製一般資源以及範本中定義的技能和熟練度。</span><span class="sxs-lookup"><span data-stu-id="0bdae-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="0bdae-139">一般資源指派也會維持與原先在專案範本中的一樣。</span><span class="sxs-lookup"><span data-stu-id="0bdae-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="0bdae-140">專案範本不支援具名資源。</span><span class="sxs-lookup"><span data-stu-id="0bdae-140">Named resources aren't supported in project templates.</span></span>
