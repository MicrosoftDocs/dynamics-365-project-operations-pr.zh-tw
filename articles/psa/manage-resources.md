---
title: 管理資源
description: 本主題提供有關如何管理資源的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 37377367751592fc533447748b80b124cb6548ad
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151333"
---
# <a name="manage-resources"></a><span data-ttu-id="57c73-103">管理資源</span><span class="sxs-lookup"><span data-stu-id="57c73-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="57c73-104">Dynamics 365 Project Service Automation 包含資源管理員儀表板，提供整個組織之資源索求與使用率的視覺化概觀。</span><span class="sxs-lookup"><span data-stu-id="57c73-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="57c73-105">您可以使用此儀表板上的圖表，以視覺化方式呈現下列資訊：</span><span class="sxs-lookup"><span data-stu-id="57c73-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="57c73-106">**資源索求** – **使用中資源要求** 圖表顯示已送出的資源索求。</span><span class="sxs-lookup"><span data-stu-id="57c73-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="57c73-107">資源是依據角色或專案來彙總。</span><span class="sxs-lookup"><span data-stu-id="57c73-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="57c73-108">**未送出資源索求** – **未指派的資源索求** 圖表顯示所有尚未送出的資源需求。</span><span class="sxs-lookup"><span data-stu-id="57c73-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="57c73-109">它可協助資源管理員檢視未確定但可能會透過資源要求送出的索求。</span><span class="sxs-lookup"><span data-stu-id="57c73-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="57c73-110">**上週應收費使用率** – **依角色的使用率** 圖表顯示組織的實際依角色應收費使用率對照其目標依角色應收費使用率的百分比。</span><span class="sxs-lookup"><span data-stu-id="57c73-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57c73-111">若要讓 **依角色使用率** 圖表可供使用，請建立執行 UpdateRoleUtilization 工作流程的工作。</span><span class="sxs-lookup"><span data-stu-id="57c73-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="57c73-112">此週期性工作每隔七天執行一次，以計算前七天的應收費使用率。</span><span class="sxs-lookup"><span data-stu-id="57c73-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="57c73-113">結果是依角色彙總。</span><span class="sxs-lookup"><span data-stu-id="57c73-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="57c73-114">管理專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="57c73-114">Manage project team members</span></span>

<span data-ttu-id="57c73-115">專案經理可以使用資源管理員儀表板來管理專案的資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="57c73-116">例如，他們可以直接將團隊成員新增至專案，以及預約團隊成員來履行一般資源已擷取的資源需求。</span><span class="sxs-lookup"><span data-stu-id="57c73-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="57c73-117">將團隊成員直接新增至專案</span><span class="sxs-lookup"><span data-stu-id="57c73-117">Add a team member directly to a project</span></span>

<span data-ttu-id="57c73-118">若要直接將團隊成員新增至專案，請在 **專案** 頁面的 **團隊** 索引標籤上選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="57c73-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="57c73-119">**快速建立：專案團隊成員** 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="57c73-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="57c73-120">在此對話方塊中，您可以執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="57c73-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="57c73-121">**預約具名資源** – 在 **可預約資源** 欄位中，選取資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="57c73-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="57c73-122">然後選取角色、設定期間，並選取配置方法。</span><span class="sxs-lookup"><span data-stu-id="57c73-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="57c73-123">您選取的具名資源是使用選取的配置方法和資源行事曆來新增至專案。</span><span class="sxs-lookup"><span data-stu-id="57c73-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="57c73-124">**新增一般資源** – 讓 **可預約資源** 欄位保留空白、選取角色、設定期間，然後選取偏好的配置方法。</span><span class="sxs-lookup"><span data-stu-id="57c73-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="57c73-125">一般資源會新增至團隊做為預留位置，以保存用於預約團隊上具名資源的索求模式。</span><span class="sxs-lookup"><span data-stu-id="57c73-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="57c73-126">需求是根據專案行事曆所建立。</span><span class="sxs-lookup"><span data-stu-id="57c73-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="57c73-127">**將具名資源新增至團隊而不耗用資源產能** – 在 **可預約資源** 欄位中，選取資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="57c73-128">然後選取期間，並選取 **無** 做為配置方法。</span><span class="sxs-lookup"><span data-stu-id="57c73-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="57c73-129">資源會新增至團隊，但是無法透過預約來耗用資源產能。</span><span class="sxs-lookup"><span data-stu-id="57c73-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="57c73-130">預約團隊成員以履行一般資源的資源需求</span><span class="sxs-lookup"><span data-stu-id="57c73-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="57c73-131">在 PSA 中，您可以在專案團隊上預約一般資源，也可以指定角色、所需產能，以及該產能的發佈方式。</span><span class="sxs-lookup"><span data-stu-id="57c73-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="57c73-132">在資源需求上，您可以指定與一般資源相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="57c73-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="57c73-133">這些屬性包括必要技能、偏好的組織單位以及偏好的資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="57c73-134">請依照下列步驟，對開發人員的一般資源指定必要的技能。</span><span class="sxs-lookup"><span data-stu-id="57c73-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="57c73-135">在 **專案** 頁面的 **團隊** 索引標籤中，選取 **新增** 以預約一般資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![團隊中已預約的一般資源](media/Resource-Management-image9.png)

2. <span data-ttu-id="57c73-137">在 **所有團隊成員** 檢視表的 **資源需求** 欄中，選取可新增一般資源所需技能的連結。</span><span class="sxs-lookup"><span data-stu-id="57c73-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![需求連結](media/Resource-Management-image10.png)

3. <span data-ttu-id="57c73-139">在出現的 **資源需求** 頁面上，選取 **技能** 網格中的省略符號 (**...**)，然後選取 **新增需求特性** 以新增開發人員所需的技能。</span><span class="sxs-lookup"><span data-stu-id="57c73-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![新增需求特性命令](media/Resource-Management-image11.png)

4. <span data-ttu-id="57c73-141">在出現的 **快速建立：需求特性** 對話方塊上，於 **特性** 欄位中選取所需的技能。</span><span class="sxs-lookup"><span data-stu-id="57c73-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="57c73-142">然後在 **評等級值** 欄位中，選取該技能的熟練程度。</span><span class="sxs-lookup"><span data-stu-id="57c73-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="57c73-143">最後在 **資源需求** 欄位中，將需求設定為組織單位中的來源資源或甚至設為具名資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="57c73-144">完成之後，選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="57c73-144">When you've finished, select **Save**.</span></span>

    ![[快速建立：需求特性] 對話方塊](media/Resource-Management-image12.png)

5. <span data-ttu-id="57c73-146">在 **資源需求** 頁面上，選取 **預約** 以履行資源需求。</span><span class="sxs-lookup"><span data-stu-id="57c73-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![[資源需求] 頁面上的 [預約] 按鈕](media/Resource-Management-image13.png)

    <span data-ttu-id="57c73-148">您也可以選取 **所有團隊成員** 網格中的一般資源，然後選取 **預約**。</span><span class="sxs-lookup"><span data-stu-id="57c73-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![[所有團隊成員] 網格上方的 [預約] 按鈕](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="57c73-150">在此範例中，需要的時間是 40 小時，但沒有任何實際預約時數，因為一般資源沒有預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="57c73-151">此外，也沒有指派的時數，因為一般資源已直接新增至團隊。</span><span class="sxs-lookup"><span data-stu-id="57c73-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="57c73-152">這不是使用工作指派所新增的。</span><span class="sxs-lookup"><span data-stu-id="57c73-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="57c73-153">在 **排程小幫手** 頁面上，您可以依據資源需求所指定的需求來篩選可用資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="57c73-154">資源是根據在排程面板所指定的排序參數來排序。</span><span class="sxs-lookup"><span data-stu-id="57c73-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![排程小幫手頁面](media/Resource-Management-image15.png)

    <span data-ttu-id="57c73-156">以下是一些經常使用的篩選：</span><span class="sxs-lookup"><span data-stu-id="57c73-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="57c73-157">**特性與評等** – 依據技能、認證和其他資源品質以及熟練程度進行篩選。</span><span class="sxs-lookup"><span data-stu-id="57c73-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="57c73-158">**角色** – 依據指派給可預約資源的預設角色進行篩選。</span><span class="sxs-lookup"><span data-stu-id="57c73-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="57c73-159">**組織單位** – 依據將可預約資源指派至的組織單位篩選可預約資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="57c73-160">如果您不滿意初始需求搜尋的結果，可以變更篩選準則。</span><span class="sxs-lookup"><span data-stu-id="57c73-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="57c73-161">展開左側的 **篩選檢視表** 窗格，然後選取 **搜尋** 來尋找其他資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![[篩選檢視表] 窗格](media/Resource-Management-image16.png)

7. <span data-ttu-id="57c73-163">若要變更結果的排序方式，請選取 **排序**。</span><span class="sxs-lookup"><span data-stu-id="57c73-163">To change how the results are sorted, select **Sort**.</span></span>

    ![排序命令](media/Resource-Management-image17.png)

8. <span data-ttu-id="57c73-165">根據需求上指定的索求 (如網格頂端所示) 選取資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="57c73-166">您可以清除網格中的儲存格選取，並讓資源產能保持開啟。</span><span class="sxs-lookup"><span data-stu-id="57c73-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="57c73-167">一次只能將一項資源選取為已預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="57c73-168">選取 **預約** 以預約所選取資源，同時讓排程面板保持開啟，以便您再選取其他資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="57c73-169">或者，選取 **預約並結束** 以預約所選資源並關閉排程面板。</span><span class="sxs-lookup"><span data-stu-id="57c73-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![要預約的資源](media/Resource-Management-image19.png)

    <span data-ttu-id="57c73-171">您會收到有關已預約時數的通知。</span><span class="sxs-lookup"><span data-stu-id="57c73-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="57c73-172">索求指示器顯示已滿足多少預約需求以及還剩多少未滿足。</span><span class="sxs-lookup"><span data-stu-id="57c73-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="57c73-173">您還可以查看已耗用多少所選資源的產能。</span><span class="sxs-lookup"><span data-stu-id="57c73-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="57c73-174">選取 **展開** 以查看資源預約的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="57c73-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="57c73-175">返回 **所有團隊成員** 檢視表。</span><span class="sxs-lookup"><span data-stu-id="57c73-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="57c73-176">請注意，在網格中，一般資源已由具名資源取代，並且列出已預約該資源 40 小時。</span><span class="sxs-lookup"><span data-stu-id="57c73-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![已更新的 [所有團隊成員] 網格](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="57c73-178">沒有顯示指派的時數，因為是直接在團隊中預約的。</span><span class="sxs-lookup"><span data-stu-id="57c73-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="57c73-179">這些資源並非使用工作指派所預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="57c73-180">指派一般資源給工作，並產生資源需求</span><span class="sxs-lookup"><span data-stu-id="57c73-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="57c73-181">在 PSA 中，您可以建立工作，然後將一般資源指派給這些工作。</span><span class="sxs-lookup"><span data-stu-id="57c73-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="57c73-182">如此一來，當您估計排程和財務數字時，就能以預留位置來表示資源索求。</span><span class="sxs-lookup"><span data-stu-id="57c73-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="57c73-183">您可以接著為一般資源產生資源需求並履行這些需求。</span><span class="sxs-lookup"><span data-stu-id="57c73-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="57c73-184">在 **專案** 頁面的 **排程** 索引標籤上，選取 **新增** 以建立工作。</span><span class="sxs-lookup"><span data-stu-id="57c73-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![新工作已建立](media/Resource-Management-image21.png)

2. <span data-ttu-id="57c73-186">在 **資源** 欄位中，選取 **資源選擇器** 符號。</span><span class="sxs-lookup"><span data-stu-id="57c73-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="57c73-187">資源選擇器隨即出現，並顯示專案的現有團隊成員。</span><span class="sxs-lookup"><span data-stu-id="57c73-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![資源選擇器](media/Resource-Management-image22.png)

3. <span data-ttu-id="57c73-189">輸入新的一般資源的名稱，然後選取 **建立**。</span><span class="sxs-lookup"><span data-stu-id="57c73-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![輸入的新一般資源名稱](media/Resource-Management-image23.png)

4. <span data-ttu-id="57c73-191">在出現的 **快速建立：專案團隊成員** 對話方塊上，於 **角色** 欄位中選取一般資源的角色。</span><span class="sxs-lookup"><span data-stu-id="57c73-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="57c73-192">在 **資源分配單位** 欄位中，選取一般資源的組織單位。</span><span class="sxs-lookup"><span data-stu-id="57c73-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="57c73-193">然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="57c73-193">Then select **Save**.</span></span>

    ![[快速建立：專案團隊成員] 對話方塊](media/Resource-Management-image24.png)

    <span data-ttu-id="57c73-195">一般團隊成員現在已指派給工作。</span><span class="sxs-lookup"><span data-stu-id="57c73-195">The generic team member is now assigned to the task.</span></span>

    ![已指派給工作的一般團隊成員](media/Resource-Management-image25.png)

    <span data-ttu-id="57c73-197">在 **團隊** 索引標籤上，您會看到新的一般團隊成員。</span><span class="sxs-lookup"><span data-stu-id="57c73-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="57c73-198">請注意，其中只有指派的時數。</span><span class="sxs-lookup"><span data-stu-id="57c73-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="57c73-199">這些時數是所有指派至一般團隊成員之工作的總和。</span><span class="sxs-lookup"><span data-stu-id="57c73-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="57c73-200">一般團隊成員還沒有所需時數或資源需求。</span><span class="sxs-lookup"><span data-stu-id="57c73-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![[團隊] 索引標籤上的一般團隊成員](media/Resource-Management-image26.png)

5. <span data-ttu-id="57c73-202">您現在可以使用資源選擇器，將一般團隊成員指派給其他工作。</span><span class="sxs-lookup"><span data-stu-id="57c73-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![資源選擇器中的一般團隊成員](media/Resource-Management-image27.png)

    <span data-ttu-id="57c73-204">完成指派一般資源給工作的動作後，您可以為一般資源產生資源需求。</span><span class="sxs-lookup"><span data-stu-id="57c73-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="57c73-205">在 **團隊** 索引標籤上，選取一般資源，然後選取 **產生需求**。</span><span class="sxs-lookup"><span data-stu-id="57c73-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![產生需求命令](media/Resource-Management-image28.png)

    <span data-ttu-id="57c73-207">產生需要後，一般團隊成員就會有資源需求的所需時數和連結。</span><span class="sxs-lookup"><span data-stu-id="57c73-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![資源需求連結](media/Resource-Management-image29.png)

    <span data-ttu-id="57c73-209">預約具名資源之後，便會從團隊移除一般資源，並以具名資源取代該資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![已由具名資源取代的一般資源](media/Resource-Management-image30.png)

    <span data-ttu-id="57c73-211">在 **排程** 索引標籤上，一般資源指派已移除，並且已由具名資源取代。</span><span class="sxs-lookup"><span data-stu-id="57c73-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![[排程] 索引標籤上已由具名資源取代的一般資源指派](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="57c73-213">只有在針對一般資源需求完整預約具名資源時，才會發生此行為。</span><span class="sxs-lookup"><span data-stu-id="57c73-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="57c73-214">具名資源部分取代一般資源需求，或是多個具名資源取代一般資源需求時，一般資源仍會保留已指派至工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="57c73-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="57c73-215">在下圖中，一項 80 小時工作已規畫給一段五天期間 (五天內每日 16 小時)，並且已指派給名為 **職能** 的一般資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![五天內八十小時的工作已指派至「職能」一般資源](media/Resource-Management-image32.png)

    <span data-ttu-id="57c73-217">當您產生需求時，所需的即是五天內的 80 小時。</span><span class="sxs-lookup"><span data-stu-id="57c73-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![五天內 80 小時的需求已產生](media/Resource-Management-image33.png)

    <span data-ttu-id="57c73-219">由於可用資源每天只工作八小時，因此需要兩項資源來履行此一需求。</span><span class="sxs-lookup"><span data-stu-id="57c73-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![第二項資源](media/Resource-Management-image35.png)

    <span data-ttu-id="57c73-221">在 **團隊** 索引標籤上，現在可以看到一般資源沒有需要的時數，但是指派的時數仍然與兩個共同履行需求的具名資源一起顯示。</span><span class="sxs-lookup"><span data-stu-id="57c73-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![[團隊] 索引標籤上的兩個具名資源](media/Resource-Management-image36.png)

    <span data-ttu-id="57c73-223">在 **排程** 索引標籤上，一般資源仍保留已指派至工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="57c73-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![[排程] 索引標籤上的一般資源](media/Resource-Management-image37.png)

<span data-ttu-id="57c73-225">PSA 不會將這兩種資源指派給工作，因為這種行為產生的排程較難以預測。</span><span class="sxs-lookup"><span data-stu-id="57c73-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="57c73-226">在此簡單範例中，可以很輕鬆地在兩個資源之間均等劃分時數。</span><span class="sxs-lookup"><span data-stu-id="57c73-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="57c73-227">不過，在涉及多個工作和多項資源的複雜案例中，PSA 必須對如何在多個工作之間配置所獲多項資源的預約進行假設。</span><span class="sxs-lookup"><span data-stu-id="57c73-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="57c73-228">因此，在這些案例中，專案經理要負責剖析多個預約並視需要進行指派。</span><span class="sxs-lookup"><span data-stu-id="57c73-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="57c73-229">為了配置預約，專案經理會將一般資源的工作指派給具名資源，然後使用 **協調** 檢視表來確保該配置對預約有效。</span><span class="sxs-lookup"><span data-stu-id="57c73-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="57c73-230">編輯資源需求</span><span class="sxs-lookup"><span data-stu-id="57c73-230">Edit a resource requirement</span></span>

<span data-ttu-id="57c73-231">建立資源需求之後，專案經理或資源管理員可能需要編輯詳細資料，以便在使用排程面板時縮小搜尋準則範圍。</span><span class="sxs-lookup"><span data-stu-id="57c73-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="57c73-232">若要編輯資源需求，請依照下列步驟進行。</span><span class="sxs-lookup"><span data-stu-id="57c73-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="57c73-233">在 **專案** 頁面的 **團隊** 索引標籤中，選取一般資源上任何需求的連結。</span><span class="sxs-lookup"><span data-stu-id="57c73-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="57c73-234">在出現的 **資源需求** 頁面上，您可以更新數個屬性。</span><span class="sxs-lookup"><span data-stu-id="57c73-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="57c73-235">以下列出一些範例：</span><span class="sxs-lookup"><span data-stu-id="57c73-235">Here are some examples:</span></span>

    - <span data-ttu-id="57c73-236">名字</span><span class="sxs-lookup"><span data-stu-id="57c73-236">Name</span></span>
    - <span data-ttu-id="57c73-237">開始日期</span><span class="sxs-lookup"><span data-stu-id="57c73-237">From Date</span></span>
    - <span data-ttu-id="57c73-238">結束日期</span><span class="sxs-lookup"><span data-stu-id="57c73-238">To Date</span></span>
    - <span data-ttu-id="57c73-239">期間</span><span class="sxs-lookup"><span data-stu-id="57c73-239">Duration</span></span>
    - <span data-ttu-id="57c73-240">資源類型</span><span class="sxs-lookup"><span data-stu-id="57c73-240">Resource Type</span></span>

<span data-ttu-id="57c73-241">在 **資源需求** 頁面上，專案經理或資源管理員還可以定義下列資訊：</span><span class="sxs-lookup"><span data-stu-id="57c73-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="57c73-242">技能</span><span class="sxs-lookup"><span data-stu-id="57c73-242">Skills</span></span>
- <span data-ttu-id="57c73-243">Roles</span><span class="sxs-lookup"><span data-stu-id="57c73-243">Roles</span></span>
- <span data-ttu-id="57c73-244">資源喜好設定</span><span class="sxs-lookup"><span data-stu-id="57c73-244">Resource preferences</span></span>
- <span data-ttu-id="57c73-245">偏好的組織單位</span><span class="sxs-lookup"><span data-stu-id="57c73-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="57c73-246">在專案上預約資源之後更新的資源預約</span><span class="sxs-lookup"><span data-stu-id="57c73-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="57c73-247">將一般或具名資源新增至專案團隊之後，您可以變更資源的預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="57c73-248">在 **專案** 頁面的 **團隊** 索引標籤上，選取團隊成員，然後選取 **維護預約**。</span><span class="sxs-lookup"><span data-stu-id="57c73-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![針對所選團隊成員開啟的排程面板](media/Resource-Management-image40.png)

    <span data-ttu-id="57c73-250">排程面板隨即出現，並顯示專案團隊成員的預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="57c73-251">展開團隊成員的記錄，以檢視對此專案所預約的時數，以及其他耗用團隊成員產能的專案。</span><span class="sxs-lookup"><span data-stu-id="57c73-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="57c73-252">選取預約並拖曳以延長或縮短。</span><span class="sxs-lookup"><span data-stu-id="57c73-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="57c73-253">**建立資源預約** 對話方塊隨即顯示，讓您調整預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![[建立資源預約] 對話方塊](media/Resource-Management-image41.png)

3. <span data-ttu-id="57c73-255">以滑鼠右鍵按一下預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-255">Right-click the booking.</span></span> <span data-ttu-id="57c73-256">您可以使用捷徑功能表來完成下列動作：</span><span class="sxs-lookup"><span data-stu-id="57c73-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="57c73-257">變更預約狀態。</span><span class="sxs-lookup"><span data-stu-id="57c73-257">Change the booking status.</span></span>
    - <span data-ttu-id="57c73-258">編輯預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-258">Edit the booking.</span></span>
    - <span data-ttu-id="57c73-259">替代專案團隊上的資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="57c73-260">變更預約狀態</span><span class="sxs-lookup"><span data-stu-id="57c73-260">Change the booking status</span></span>

<span data-ttu-id="57c73-261">您可以變更任何預設或自訂預約狀態。</span><span class="sxs-lookup"><span data-stu-id="57c73-261">You can change any default or custom booking status.</span></span>

![變更狀態命令](media/Resource-Management-image42.png)

<span data-ttu-id="57c73-263">下列狀態已納入 PSA：</span><span class="sxs-lookup"><span data-stu-id="57c73-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="57c73-264">**已取消** – 此狀態會取消資源的預約並釋放資源的產能。</span><span class="sxs-lookup"><span data-stu-id="57c73-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="57c73-265">**已確認預約** – 此狀態會耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="57c73-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="57c73-266">當您從 **專案** 頁面的 **所有團隊成員** 網格中開啟 **維護預約** 時，預約通常會有此狀態。</span><span class="sxs-lookup"><span data-stu-id="57c73-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="57c73-267">**未確定預約** – 此狀態會將資源新增至團隊，但是不耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="57c73-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="57c73-268">這表示資源已保留給可能的工作，但其他工作有需要時，仍然會有產能。</span><span class="sxs-lookup"><span data-stu-id="57c73-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="57c73-269">從整體資源可用性看來，未確定預約的狀態與確定預約的狀態不同。</span><span class="sxs-lookup"><span data-stu-id="57c73-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="57c73-270">**已提案** – 此狀態表示資源管理員或專案經理對資源的提案。</span><span class="sxs-lookup"><span data-stu-id="57c73-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="57c73-271">提案不會耗用資源的產能，而且資源不會新增至專案團隊。</span><span class="sxs-lookup"><span data-stu-id="57c73-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="57c73-272">若要以已確認預約方式在團隊上預約資源，專案經理必須接受提案。</span><span class="sxs-lookup"><span data-stu-id="57c73-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="57c73-273">送出資源要求</span><span class="sxs-lookup"><span data-stu-id="57c73-273">Submit resource requests</span></span>

<span data-ttu-id="57c73-274">資源要求會用來執行必須由資源管理員來滿足的索求 (資源需求)。</span><span class="sxs-lookup"><span data-stu-id="57c73-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="57c73-275">對於已經在團隊上的一般資源，您可以直接送出資源要求。</span><span class="sxs-lookup"><span data-stu-id="57c73-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="57c73-276">資源要求可以用兩種方式來履行：</span><span class="sxs-lookup"><span data-stu-id="57c73-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="57c73-277">資源管理員直接履行要求。</span><span class="sxs-lookup"><span data-stu-id="57c73-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="57c73-278">在此情況下，一般資源會由含有具名資源的已確認預約所取代。</span><span class="sxs-lookup"><span data-stu-id="57c73-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="57c73-279">資源管理員向專案經理提案建議資源，而專案經理核准或拒絕建議的資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="57c73-280">直接履行資源要求</span><span class="sxs-lookup"><span data-stu-id="57c73-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="57c73-281">產生資源需求後，專案經理可以選取資源，然後選取 **送出要求**，送出對一般資料的資源要求。</span><span class="sxs-lookup"><span data-stu-id="57c73-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![[送出要求] 按鈕](media/Resource-Management-image45.png)

<span data-ttu-id="57c73-283">您可以將資源的相關註解提供給正在履行要求的資源管理員。</span><span class="sxs-lookup"><span data-stu-id="57c73-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="57c73-284">送出要求後，團隊成員的 **狀態** 欄位會變更為 **已送出**。</span><span class="sxs-lookup"><span data-stu-id="57c73-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![輸入選擇性註解](media/Resource-Management-image46.png)

<span data-ttu-id="57c73-286">資源管理員履行要求時，一般團隊成員會以 **所有團隊成員** 網格中的具名資源來取代。</span><span class="sxs-lookup"><span data-stu-id="57c73-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![[所有團隊成員] 網格中由具名資源所取代的一般團隊成員](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="57c73-288">針對資源要求使用資源提案</span><span class="sxs-lookup"><span data-stu-id="57c73-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="57c73-289">與直接根據資源要求預約資源相反，資源管理員可以提案將資源建議給專案經理。</span><span class="sxs-lookup"><span data-stu-id="57c73-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="57c73-290">當無法做到完全符合需求時，資源管理員可能會使用此選項。</span><span class="sxs-lookup"><span data-stu-id="57c73-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="57c73-291">當資源管理員提案建議資源時，專案經理會看到一般團隊成員的 **狀態** 欄位已變更為 **需要檢閱**。</span><span class="sxs-lookup"><span data-stu-id="57c73-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![一般團隊成員的狀態已變更為 [需要檢閱]](media/Resource-Management-image48.png)

<span data-ttu-id="57c73-293">若要檢視提議的資源以及提案預約所產生影響的視覺效果，請按兩下狀態為 **需要檢閱** 的團隊成員。</span><span class="sxs-lookup"><span data-stu-id="57c73-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="57c73-294">然後選取 **提案的資源** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="57c73-294">Then select the **Proposed Resources** tab.</span></span>

![[提案的資源] 索引標籤](media/Resource-Management-image49.png)

<span data-ttu-id="57c73-296">選取 **接受所有提案** 以接受所有提議的資源，或選取 **拒絕所有提案** 加以拒絕。</span><span class="sxs-lookup"><span data-stu-id="57c73-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="57c73-297">如果您接受提議的資源，則這些資源已確定在專案上預約為團隊成員，並取代一般資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="57c73-298">您必須接受或拒絕所有提議的資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="57c73-299">您無法部分接受或拒絕。</span><span class="sxs-lookup"><span data-stu-id="57c73-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="57c73-300">以專案團隊上的資源來替代</span><span class="sxs-lookup"><span data-stu-id="57c73-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="57c73-301">專案經理有時必須以專案上的已預約團隊成員來替代。</span><span class="sxs-lookup"><span data-stu-id="57c73-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="57c73-302">在 **專案** 頁面的 **團隊** 索引標籤上，選取需要替代資源的資源，然後選取 **維護預約**。</span><span class="sxs-lookup"><span data-stu-id="57c73-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="57c73-303">展開資源以檢視其所指派至的專案。</span><span class="sxs-lookup"><span data-stu-id="57c73-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![資源已展開來顯示指派的專案](media/Resource-Management-image50.png)

3. <span data-ttu-id="57c73-305">以滑鼠右鍵按一下專案，然後選取 **替代資源**。</span><span class="sxs-lookup"><span data-stu-id="57c73-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="57c73-306">如果您知道要替代目前資源的資源，請選取或輸入名稱，然後選取 **重新指派**。</span><span class="sxs-lookup"><span data-stu-id="57c73-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![指定替代資源](media/Resource-Management-image51.png)

    <span data-ttu-id="57c73-308">或者，依照下列步驟搜尋資源：</span><span class="sxs-lookup"><span data-stu-id="57c73-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="57c73-309">選取 **尋找替代資源**。</span><span class="sxs-lookup"><span data-stu-id="57c73-309">Select **Find Substitution**.</span></span>

        ![搜尋替代資源](media/Resource-Management-image52.png)

        <span data-ttu-id="57c73-311">排程小幫手會傳回可用的替代資源清單。</span><span class="sxs-lookup"><span data-stu-id="57c73-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="57c73-312">在排程小幫手中，您可以進一步篩選可用的資源，以尋找適當的替代資源。</span><span class="sxs-lookup"><span data-stu-id="57c73-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![可用替代資源的清單](media/Resource-Management-image53.png)

    2. <span data-ttu-id="57c73-314">若要替代資源，請選取您想要的資源，然後選取 **替代**。</span><span class="sxs-lookup"><span data-stu-id="57c73-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![已選取的替代資源](media/Resource-Management-image54.png)

    <span data-ttu-id="57c73-316">預約和指派會以新資源來替代。</span><span class="sxs-lookup"><span data-stu-id="57c73-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![以新資源替代的預約和指派](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="57c73-318">協調團隊成員預約與指派</span><span class="sxs-lookup"><span data-stu-id="57c73-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="57c73-319">在團隊成員中，預約與指派的聯繫鬆散。</span><span class="sxs-lookup"><span data-stu-id="57c73-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="57c73-320">換言之，資源可以有指派但沒有預約，或者可以有預約但沒有指派。</span><span class="sxs-lookup"><span data-stu-id="57c73-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="57c73-321">預約與指派最好要一致，讓資源有已認可產能來執行工作指派。</span><span class="sxs-lookup"><span data-stu-id="57c73-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="57c73-322">不過，預約可能會根據可用性，而工作計時可能會隨著專案持續而改變。</span><span class="sxs-lookup"><span data-stu-id="57c73-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="57c73-323">因此，鬆散聯繫的預約和指派提供了彈性。</span><span class="sxs-lookup"><span data-stu-id="57c73-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="57c73-324">PSA 有一個 **協調** 索引標籤，可讓專案經理協調團隊成員的預約及其對專案團隊的指派。</span><span class="sxs-lookup"><span data-stu-id="57c73-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![[協調] 索引標籤](media/Resource-Management-image56.png)

<span data-ttu-id="57c73-326">**協調** 索引標籤會顯示下至每個團隊成員個別工作指派層級的預約及指派。</span><span class="sxs-lookup"><span data-stu-id="57c73-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="57c73-327">它會在儲存格中顯示表示從月數下至天數時段期間的時數。</span><span class="sxs-lookup"><span data-stu-id="57c73-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="57c73-328">此索引標籤也會顯示專案的整體淨總數以及總計欄。</span><span class="sxs-lookup"><span data-stu-id="57c73-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="57c73-329">對於每項資源中，此索引標籤會計算團隊成員預約與團隊成員工作指派彙總之間的差異。</span><span class="sxs-lookup"><span data-stu-id="57c73-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="57c73-330">此差異最好是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="57c73-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="57c73-331">換句話說，預約與指派之間應該要沒有差異。</span><span class="sxs-lookup"><span data-stu-id="57c73-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="57c73-332">差異會著色並有明暗層次，以吸引對兩種狀況的注意：</span><span class="sxs-lookup"><span data-stu-id="57c73-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="57c73-333">**預約不足** – 當資源的指派數超過預約數時，就會發生預約短缺。</span><span class="sxs-lookup"><span data-stu-id="57c73-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="57c73-334">因為尚未保留此產能，專案經理可能需要延長資源的預約以彌補短缺來更正此情況。</span><span class="sxs-lookup"><span data-stu-id="57c73-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="57c73-335">**超額預約** – 當資源已預約給專案，但尚未指派給工作時，會發生超額預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="57c73-336">在資源已在進行工作指派之前預約給專案的情況下，此狀況可能會是可接受的。</span><span class="sxs-lookup"><span data-stu-id="57c73-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="57c73-337">不過，在其他情況下，資源並未規劃要指派給工作。</span><span class="sxs-lookup"><span data-stu-id="57c73-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="57c73-338">在這些情況下，專案經理應考慮取消資源的預約，讓該產能可以用於其他專案。</span><span class="sxs-lookup"><span data-stu-id="57c73-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="57c73-339">在某些情況下中，當您以高於日的層級來檢視時間 (例如，月層級) 時，您可能會看到資源的淨差異為零 (換句話說，預約 = 指派)。</span><span class="sxs-lookup"><span data-stu-id="57c73-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="57c73-340">不過，如果您以週層級檢視時間，您可能會在第一週看到零小時的指派以及 40 小時的預約，但在第二週看到 40 小時的指派以及零小時的預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="57c73-341">總而言之，預約和指派已協調，但它們在一週與下一週中不相同。</span><span class="sxs-lookup"><span data-stu-id="57c73-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="57c73-342">以較高層級檢視時間時，**調解** 索引標籤中的儲存格會有指示器，通知您較低層級上有差異。</span><span class="sxs-lookup"><span data-stu-id="57c73-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="57c73-343">在儲存格中按兩下，可以放大來檢視差異。</span><span class="sxs-lookup"><span data-stu-id="57c73-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="57c73-344">您可以接著按一下滑鼠右鍵來縮小。您可以選取資源，然後使用網格工具列的 **下一個差異** 控制項，移至該資源的預約與指派之間的下一個差異。</span><span class="sxs-lookup"><span data-stu-id="57c73-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="57c73-345">然後可以使用 **上一個差異** 控制項返回。</span><span class="sxs-lookup"><span data-stu-id="57c73-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="57c73-346">您也可以在 **設定** 底下關閉差異指示器和導覽行為。</span><span class="sxs-lookup"><span data-stu-id="57c73-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![差異指示器](media/Resource-Management-image57.png)

<span data-ttu-id="57c73-348">如果您資源有工作指派但沒有預約，請在 **專案** 頁面的 **協調** 索引標籤上，選取 [預訂不足]，然後選取 **延長預約**。</span><span class="sxs-lookup"><span data-stu-id="57c73-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="57c73-349">**延長預約** 對話方塊隨即出現，並顯示解決資源不足狀況所需的預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="57c73-350">其中也會顯示資源在所有專案或其他可排程實體中的現有預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="57c73-351">如果您選取 **確定** 建立資源的預約，不論該資源的可用性如何，都可能會造成過量預約。</span><span class="sxs-lookup"><span data-stu-id="57c73-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![[延長預約] 對話方塊](media/Resource-Management-image58.png)

<span data-ttu-id="57c73-353">專案經理或資源管理員可以接著使用排程面板，管理任何過量預約資源超過其產能的狀況。</span><span class="sxs-lookup"><span data-stu-id="57c73-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
