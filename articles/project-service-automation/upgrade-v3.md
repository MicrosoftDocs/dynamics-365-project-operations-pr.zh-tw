---
title: 升級考量 - 從 Microsoft Dynamics 365 Project Service Automation 2.x 或 1.x 版升級至版本 3
description: 本主題提供有關從 Project Service Automation 2.x 或 1.x 版升級至版本 3 時必須進行考量的資訊。
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: e4fae2ea-9013-488e-a666-f7192dd42c0b
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: ba710eb8c07df7dac97e8b911184c00b87b14548
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749949"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a><span data-ttu-id="2e29e-103">升級考量 - 從 PSA 2.x 或 1.x 版升級至版本 3</span><span class="sxs-lookup"><span data-stu-id="2e29e-103">Upgrade considerations - PSA version 2.x or 1.x to version 3</span></span>
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a><span data-ttu-id="2e29e-104">Project Service Automation 和 Field Service</span><span class="sxs-lookup"><span data-stu-id="2e29e-104">Project Service Automation and Field Service</span></span>
<span data-ttu-id="2e29e-105">Dynamics 365 Project Service Automation 和 Dynamics 365 Field Service 都會使用 Universal Resourcing Scheduling (URS) 解決方案來進行資源排程。</span><span class="sxs-lookup"><span data-stu-id="2e29e-105">Both Dynamics 365 Project Service Automation and Dynamics 365 Field Service use the Universal Resourcing Scheduling (URS) solution for resource scheduling.</span></span> <span data-ttu-id="2e29e-106">如果您的執行個體中同時有 Project Service Automation 和 Field Service，則應該規劃將這兩個解決方案都升級為最新的版本 (Project Service Automation 的 3. x 版、Field Service 的 8. x 版)。</span><span class="sxs-lookup"><span data-stu-id="2e29e-106">If you have both Project Service Automation and Field Service in your instance, you should plan on upgrading both solutions to the latest version (version 3.x for Project Service Automation, version 8.x for Field Service).</span></span> <span data-ttu-id="2e29e-107">升級 Project Service Automation 或 Field Service 時，將會安裝最新版本的 URS，這表示如果同一個執行個體中的 Project Service Automation 和 Field Service 解決方案未升級為最新版本，則可能會產生不一致的行為。</span><span class="sxs-lookup"><span data-stu-id="2e29e-107">Upgrading Project Service Automation or Field Service will install the latest version of URS, which means that inconsistent behavior is possible if both Project Service Automation and Field Service solutions in the same instance aren’t upgraded to the latest version.</span></span>

## <a name="resource-assignments"></a><span data-ttu-id="2e29e-108">資源指派</span><span class="sxs-lookup"><span data-stu-id="2e29e-108">Resource assignments</span></span>
<span data-ttu-id="2e29e-109">在 Project Service Automation 版本 2 和版本 1 中，工作指派已儲存為**工作實體**中的下層工作 (也稱為明細工作)，並且與**資源指派**實體間接相關。</span><span class="sxs-lookup"><span data-stu-id="2e29e-109">In Project Service Automation version 2 and version 1, task assignments were stored as child tasks (also called line tasks) in the **Task entity**, and indirectly related to the **Resource Assignment** entity.</span></span> <span data-ttu-id="2e29e-110">明細工作過去可在分工結構圖 (WBS) 的指派快顯視窗中看到。</span><span class="sxs-lookup"><span data-stu-id="2e29e-110">The line task was visible in the assignment pop-up window on the Work Breakdown Structure (WBS).</span></span>

![Project Service Automation 版本 2 和版本 1 中 WBS 上的明細工作](media/upgrade-line-task-01.png)

<span data-ttu-id="2e29e-112">在 Project Service Automation 版本 3 中，將可預約資源指派給工作的結構描述已變更。</span><span class="sxs-lookup"><span data-stu-id="2e29e-112">In version 3 of Project Service Automation, the underlying schema of assigning bookable resources to tasks has changed.</span></span> <span data-ttu-id="2e29e-113">明細工作已被取代，而且**工作實體**的工作與**資源指派**實體的團隊成員之間有直接 1:1 關聯。</span><span class="sxs-lookup"><span data-stu-id="2e29e-113">The line task has been deprecated and there is a direct 1:1 relationship between the task in the **Task entity** and the team member in the **Resource Assignment** entity.</span></span> <span data-ttu-id="2e29e-114">指派給專案團隊成員的工作現在會直接儲存在資源指派實體中。</span><span class="sxs-lookup"><span data-stu-id="2e29e-114">Tasks that are assigned to a project team member are now stored directly in the Resource Assignment entity.</span></span>  

<span data-ttu-id="2e29e-115">這些變更會影響所有在專案團隊上有具名可預約資源及一般資源之資源指派的現有專案升級。</span><span class="sxs-lookup"><span data-stu-id="2e29e-115">These changes impact the upgrade of any existing projects that have resource assignments for named bookable resources and generic resources on a project team.</span></span> <span data-ttu-id="2e29e-116">這主題提供當您將專案升級至版本 3 時，需要納入考量的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2e29e-116">This topic provides the considerations that you will need to take into account for your projects when you upgrade to version 3.</span></span> 

### <a name="tasks-assigned-to-named-resources"></a><span data-ttu-id="2e29e-117">已指派給具名資源的工作</span><span class="sxs-lookup"><span data-stu-id="2e29e-117">Tasks assigned to named resources</span></span>
<span data-ttu-id="2e29e-118">版本 2 和版本 1 中的工作使用基礎工作實體，讓團隊成員可以描繪其預設定義角色以外的角色。</span><span class="sxs-lookup"><span data-stu-id="2e29e-118">Using the underlying task entity, tasks in version 2 and version 1 allowed team members to portray a role other than their default defined role.</span></span> <span data-ttu-id="2e29e-119">例如，可將預設獲指派「方案經理」角色的蔡美雪指派至具有開發人員角色的工作。</span><span class="sxs-lookup"><span data-stu-id="2e29e-119">For example, Gracie George, who’s by default assigned the role of Program Manager, could be assigned to a task with the role of Developer.</span></span> <span data-ttu-id="2e29e-120">在版本 3 中，具名團隊成員的角色一律是預設，因此任何指派給蔡美雪的工作都會使用她的方案經理預設角色。</span><span class="sxs-lookup"><span data-stu-id="2e29e-120">In version 3, the role of a named team member is always the default, so any task that Gracie George is assigned to uses her default role of Program Manager.</span></span>

<span data-ttu-id="2e29e-121">如果您已將資源指派給版本 2 和版本 1 中預設角色以外的工作，當您升級時，不論版本 2 中的角色指派如何，都會將所有工作指派的預設角色指派給具名資源。</span><span class="sxs-lookup"><span data-stu-id="2e29e-121">If you have assigned a resource to a task outside of their default role in version 2 and version 1, when you upgrade, the named resource will be assigned the default role for all task assignments, regardless of role assignment in version 2.</span></span> <span data-ttu-id="2e29e-122">這會讓計算的估計值在版本 2 或版本 1 到版本 3 之間產生差異，因為估計值是根據資源的角色而非明細工作指派所計算得出。</span><span class="sxs-lookup"><span data-stu-id="2e29e-122">This will result in differences in the calculated estimates from version 2 or version 1 to version 3 because estimates are calculated based on the role of the resource and not the line task assignment.</span></span> <span data-ttu-id="2e29e-123">例如，在版本 2 中，已將兩項工作指派給呂麗華。</span><span class="sxs-lookup"><span data-stu-id="2e29e-123">For example, in version 2, two tasks have been assigned to Ashley Chinn.</span></span> <span data-ttu-id="2e29e-124">工作 1 的明細工作角色是開發人員，而為工作 2 的是方案經理。</span><span class="sxs-lookup"><span data-stu-id="2e29e-124">The role on the line task for task 1 is Developer and for task 2, Program Manager.</span></span> <span data-ttu-id="2e29e-125">呂麗華會有方案經理的預設角色。</span><span class="sxs-lookup"><span data-stu-id="2e29e-125">Ashley Chinn has the default role of Program Manager.</span></span>

![多個指派給一個資源的角色](media/upgrade-multiple-roles-02.png)

<span data-ttu-id="2e29e-127">因為開發人員與方案經理的角色不同，成本與銷售估計值如下：</span><span class="sxs-lookup"><span data-stu-id="2e29e-127">Because the roles of Developer and Program Manager differ, the cost and sales estimates are as follows:</span></span>

![資源角色的成本估計值](media/upggrade-cost-estimates-03.png)

![資源角色的銷售估計值](media/upgrade-sales-estimates-04.png)

<span data-ttu-id="2e29e-130">升級至版本 3 時，明細工作會取代為可預約資源團隊成員工作上的資源指派。</span><span class="sxs-lookup"><span data-stu-id="2e29e-130">When you upgrade to version 3, line tasks are replaced with resource assignments on the task of the bookable resource team member.</span></span> <span data-ttu-id="2e29e-131">指派將會使用可預約資源的預設角色。</span><span class="sxs-lookup"><span data-stu-id="2e29e-131">The assignment will use the default role of the bookable resource.</span></span> <span data-ttu-id="2e29e-132">在下圖中，角色為方案經理的呂麗華即是該資源。</span><span class="sxs-lookup"><span data-stu-id="2e29e-132">In the following graphic, Ashley Chinn who has a role of Program Manager, is the resource.</span></span>

![資源指派](media/resource-assignment-v2-05.png)

<span data-ttu-id="2e29e-134">因為估計是根據資源的預設角色所計算，銷售和成本估計值可能會變更。</span><span class="sxs-lookup"><span data-stu-id="2e29e-134">Because the estimates are based on the default role for the resource, the sales and cost estimates may change.</span></span> <span data-ttu-id="2e29e-135">請注意，您已無法在下圖中看到**開發人員**角色，因為角色現在是取自可預約資源的預設角色。</span><span class="sxs-lookup"><span data-stu-id="2e29e-135">Note that in the following graphic, you no longer see the **Developer** role as the role is now taken from the bookable resource’s default role.</span></span>

<span data-ttu-id="2e29e-136">![預設角色的成本估計值](media/resource-assignment-cost-estimate-06.png)
![預設角色的銷售估計值](media/resource-assignment-sales-estimate-07.png)</span><span class="sxs-lookup"><span data-stu-id="2e29e-136">![Cost estimates for default roles](media/resource-assignment-cost-estimate-06.png)
![Sales estimate for default roles](media/resource-assignment-sales-estimate-07.png)</span></span>

<span data-ttu-id="2e29e-137">升級完成之後，您可以將團隊成員的角色編輯成所指派預設值以外的角色。</span><span class="sxs-lookup"><span data-stu-id="2e29e-137">After upgrade is complete, you can edit a team member's role to be something other than the assigned default.</span></span> <span data-ttu-id="2e29e-138">不過，如果您變更團隊成員角色，就會在團隊成員所有已獲指派的工作上變更該角色，因為版本 3 不再允許將多個角色指派給團隊成員。</span><span class="sxs-lookup"><span data-stu-id="2e29e-138">However, if you change a team members role, it will be changed on all of their assigned tasks because team members are no longer allowed to be assigned multiple roles in version 3.</span></span>

![更新資源角色](media/resource-role-assignment-08.png)

<span data-ttu-id="2e29e-140">當您將資源的組織單位從預設值變更為其他組織單位時，已指派給具名資源的明細工作也會如此。</span><span class="sxs-lookup"><span data-stu-id="2e29e-140">This is also true for line tasks that were assigned to named resources when you change the resource’s organization unit from the default to another organization unit.</span></span> <span data-ttu-id="2e29e-141">版本 3 升級完成後，指派將會使用的是資源的預設組織單位，而不是在明細工作中設定的組織單位。</span><span class="sxs-lookup"><span data-stu-id="2e29e-141">After the version 3 upgrade is complete, the assignment will use the resource’s default organization unit instead of the one set on the line task.</span></span>

### <a name="tasks-assigned-to-generic-resources"></a><span data-ttu-id="2e29e-142">已指派給一般資源的工作</span><span class="sxs-lookup"><span data-stu-id="2e29e-142">Tasks assigned to generic resources</span></span>
<span data-ttu-id="2e29e-143">在版本 2 和版本 1 中，您可以在工作中設定角色和組織單位，然後使用**產生團隊**功能，根據工作中設定的屬性來產生一般資源。</span><span class="sxs-lookup"><span data-stu-id="2e29e-143">In version 2 and version 1, you can set the role and org unit on a task and then use the **Generate team** feature to generate generic resources based on the attributes set on the task.</span></span> <span data-ttu-id="2e29e-144">在版本 3 中，您會建立具有角色和組織單位的一般團隊成員，然後再將團隊成員指派給工作。</span><span class="sxs-lookup"><span data-stu-id="2e29e-144">In version 3, you create the generic team members with role and org unit, and then assign the team members to tasks.</span></span>

<span data-ttu-id="2e29e-145">在版本 2 和版本 1 中，具有一般資源的專案在工作層級可能會有兩種狀態或兩者的混合。</span><span class="sxs-lookup"><span data-stu-id="2e29e-145">In version 2 and version 1, projects with generic resources can be in two states, or a mix of both at the task level.</span></span> <span data-ttu-id="2e29e-146">例如，您可能會遇到下列情況：</span><span class="sxs-lookup"><span data-stu-id="2e29e-146">For example, you can have the following scenarios:</span></span>

- <span data-ttu-id="2e29e-147">工作已設定角色和組織單位，但尚未產生任何附屬的資源指派。</span><span class="sxs-lookup"><span data-stu-id="2e29e-147">Tasks with roles and org units set, but no affiliated resource assignment has been generated.</span></span>
- <span data-ttu-id="2e29e-148">工作具有透過使用**產生團隊**功能建立一般資源方式所指派的一般團隊成員資源指派。</span><span class="sxs-lookup"><span data-stu-id="2e29e-148">Tasks with generic team member resource assignments that were assigned by creating generic resource using the **Generate team** feature.</span></span>

<span data-ttu-id="2e29e-149">開始進行升級之前，我們建議您針對每個已將工作指派給一般資源，或者尚未據以執行產生團隊程序的專案，重新產生團隊。</span><span class="sxs-lookup"><span data-stu-id="2e29e-149">Before you begin your upgrade, we recommend that you re-generate the team for each project that has tasks assigned to generic resources or has yet to have the generate team process run on them.</span></span>

<span data-ttu-id="2e29e-150">對於已指派給透過**產生團隊**所產生之一般團隊成員的工作，升級將會保留團隊中的一般資源，並保留對該一般團隊成員的指派。</span><span class="sxs-lookup"><span data-stu-id="2e29e-150">For tasks that are assigned to generic team members that were generated with **Generate Team**, the upgrade will leave the generic resource on the team and leave the assignment to that generic team member.</span></span> <span data-ttu-id="2e29e-151">我們建議您在升級後，但在預約或送出資源要求前，為一般團隊成員產生資源需求。</span><span class="sxs-lookup"><span data-stu-id="2e29e-151">We recommend that you generate the resource requirement for the generic team member after the upgrade but before you book or submit a resource request.</span></span> <span data-ttu-id="2e29e-152">這會在與專案承包組織單位不同的一般團隊成員上保留任何組織單位指派。</span><span class="sxs-lookup"><span data-stu-id="2e29e-152">This will preserve any org unit assignments on the generic team members that are different than the project’s contracting org unit.</span></span>

<span data-ttu-id="2e29e-153">例如，在 Project Z 專案中，承包組織單位為 Contoso US。</span><span class="sxs-lookup"><span data-stu-id="2e29e-153">For example, in the Project Z project, the contracting org unit is Contoso US.</span></span> <span data-ttu-id="2e29e-154">在專案計劃中，已將 [技術顧問] 角色指派給實作階段中的測試工作，而指派的組織單位是 Contoso India。</span><span class="sxs-lookup"><span data-stu-id="2e29e-154">In the project plan, testing tasks within the Implementation phase have been assigned the role Technical Consultant and the assigned org unit is Contoso India.</span></span>

![實作階段組織指派](media/org-unit-assignment-09.png)

<span data-ttu-id="2e29e-156">實作階段之後，將整合測試工作指派給 [技術顧問] 角色，但是組織是設定為 Contoso US。</span><span class="sxs-lookup"><span data-stu-id="2e29e-156">After the implementation phase, the integration test task is assigned to the role Technical consultant, but the org is set to Contoso US.</span></span>  

![整合測試工作組織指派](media/org-unit-generate-team-10.png)

<span data-ttu-id="2e29e-158">當您為專案產生團隊時，會建立兩個一般團隊成員，因為工作上有不同的組織單位。</span><span class="sxs-lookup"><span data-stu-id="2e29e-158">When you generate a team for the project, two generic team members are created due to the different org units on the tasks.</span></span> <span data-ttu-id="2e29e-159">技術顧問 1 會指派給 Contoso India 工作，而技術顧問 2 則有 Contoso US 工作。</span><span class="sxs-lookup"><span data-stu-id="2e29e-159">Technical consultant 1 will be assigned the Contoso India tasks and Technical consultant 2 will have the Contoso US tasks.</span></span>  

![產生的一般團隊成員](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> <span data-ttu-id="2e29e-161">在 Project Service Automation 版本 2 和版本 1 中，團隊成員不會保留明細工作上所維護的組織單位。</span><span class="sxs-lookup"><span data-stu-id="2e29e-161">In Project Service Automation version 2 and version 1, the team member does not hold the organization unit, that is maintained on the line task.</span></span>

![Project Service Automation 中的版本 2 和版本 1 明細工作](media/line-tasks-12.png)

<span data-ttu-id="2e29e-163">您可以在估計值檢視表上查看組織單位。</span><span class="sxs-lookup"><span data-stu-id="2e29e-163">You can see the organization unit on the estimates view.</span></span> 

![組織單位估計值](media/org-unit-estimates-view-13.png)
 
<span data-ttu-id="2e29e-165">升級完成時，與一般團隊成員對應之明細工作中的組織單位會新增至一般團隊成員，並移除該明細工作。</span><span class="sxs-lookup"><span data-stu-id="2e29e-165">When the upgrade is complete, the organization unit on the line task that corresponds to the generic team member is added to the generic team member and the line task is removed.</span></span> <span data-ttu-id="2e29e-166">因此，建議您在升級之前，為每個包含一般資源的專案產生或重新產生團隊。</span><span class="sxs-lookup"><span data-stu-id="2e29e-166">Because of this, we recommend that before you upgrade, you generate or re-generate the team on each project that contains generic resources.</span></span>

<span data-ttu-id="2e29e-167">對於已指派給組織單位不同於承包專案組織單位的角色且尚未產生團隊的工作，升級將會為該角色建立一般團隊成員，但會使用專案的承包單位做為團隊成員的組織單位。</span><span class="sxs-lookup"><span data-stu-id="2e29e-167">For tasks that are assigned to a role with an org unit that differs from the org unit of the contracting project, and a team has not been generated, upgrade will create a generic team member for the role, but will use the contracting unit of the project for the team member's org unit.</span></span> <span data-ttu-id="2e29e-168">回顧一下 Project Z 的範例，這表示已將 [技術顧問] 角色指派給承包組織單位 Contoso US 以及實作階段中的專案計劃測試工作，並已將組織單位指派給 Contoso India。</span><span class="sxs-lookup"><span data-stu-id="2e29e-168">Referring back to the example with Project Z, this means that the contracting org unit Contoso US, and the project plan testing tasks within the Implementation phase have been assigned the role Technical Consultant with the org unit assigned to Contoso India.</span></span> <span data-ttu-id="2e29e-169">已將實作階段之後完成的整合測試工作指派給 [技術顧問] 角色。</span><span class="sxs-lookup"><span data-stu-id="2e29e-169">The Integration test task that is completed after the Implementation phase has been assigned to the role Technical consultant.</span></span> <span data-ttu-id="2e29e-170">組織單位是 Contoso US，而且尚未產生團隊。</span><span class="sxs-lookup"><span data-stu-id="2e29e-170">The org unit is Contoso US and a team has not been generated.</span></span> <span data-ttu-id="2e29e-171">升級會建立一個一般團隊成員 (技術顧問，其所有三個工作都已指派時數) 和一個組織單位 Contoso US (專案的承包組織單位)。</span><span class="sxs-lookup"><span data-stu-id="2e29e-171">Upgrade will create one generic team member, a Technical consultant that has the assigned hours of all three tasks, and an org unit of Contoso US, the project’s contracting org unit.</span></span>   
 
<span data-ttu-id="2e29e-172">在未產生的團隊成員上變更不同資源分配組織單位的預設值，即是我們建議下列作法的理由：您應該在升級之前，針對每個包含一般資源的專案產生或重新產生團隊，以免組織單位指派遺失。</span><span class="sxs-lookup"><span data-stu-id="2e29e-172">Changing the default of the different resourcing org units on un-generated team members is the reason we recommend that you generate or re-generate the team on each project that contains generic resources prior to the upgrade so that the org unit assignments are not lost.</span></span>

