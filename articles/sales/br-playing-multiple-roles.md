---
title: 可預約資源在專案中擔任多個角色時估計專案銷售和成本
description: 本主題說明如何使用定價維度來支援在專案中擔任多個角色的資源定價和成本估計值。
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7ef9765b7db1c6650fb0599bf5fb4b4b6304be69
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013656"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a><span data-ttu-id="49b9e-103">可預約資源在專案中擔任多個角色時估計專案銷售和成本</span><span class="sxs-lookup"><span data-stu-id="49b9e-103">Estimate project sales and costs when a bookable resource fills multiple roles on a project</span></span> 

<span data-ttu-id="49b9e-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票、庫存/生產型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="49b9e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing, Project Operations for stocked/production-based scenarios_</span></span> 

<span data-ttu-id="49b9e-105">專案型公司通常需要一個資源可擔任專案的多個角色。</span><span class="sxs-lookup"><span data-stu-id="49b9e-105">Project-based companies often have the need for one resource to fill multiple roles on a project.</span></span> <span data-ttu-id="49b9e-106">每個角色的定價和成本都可以不同。</span><span class="sxs-lookup"><span data-stu-id="49b9e-106">Each role can be priced and costed differently.</span></span> <span data-ttu-id="49b9e-107">這表示根據每個角色的帳單和成本費率，專案的相同資源時間會有不同的財務估計值。</span><span class="sxs-lookup"><span data-stu-id="49b9e-107">This means that the same resource's time on a project could get a different financial estimate depending on the bill and cost rates for each role.</span></span> <span data-ttu-id="49b9e-108">您可以在指派至團隊成員的每個工作上，使用不同的覆寫值，為命名資源的團隊成員記錄設定值。</span><span class="sxs-lookup"><span data-stu-id="49b9e-108">You can set up the values on the team member record for the named resource with different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="49b9e-109">下列範例將引導您值的簡單覆寫如何讓資源在具有不同成本和帳單費率的專案上擁有多個角色。</span><span class="sxs-lookup"><span data-stu-id="49b9e-109">The following example walks you through how the simple override of a value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="49b9e-110">建立工作</span><span class="sxs-lookup"><span data-stu-id="49b9e-110">Create tasks</span></span>
<span data-ttu-id="49b9e-111">若要建立工作，在新增工作期間之前，您必須先新增工作以及摘要工作，然後需要指派工作。</span><span class="sxs-lookup"><span data-stu-id="49b9e-111">To create tasks, you need to add tasks, as well as summary tasks, after which you need to assign the task before you add task duration.</span></span> 

### <a name="add-tasks-and-summary-tasks"></a><span data-ttu-id="49b9e-112">新增工作與摘要工作</span><span class="sxs-lookup"><span data-stu-id="49b9e-112">Add tasks and summary tasks</span></span>
<span data-ttu-id="49b9e-113">若要新增工作，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="49b9e-113">To add a task, complete the following steps.</span></span>

1. <span data-ttu-id="49b9e-114">移至 **專案**，並開啟您要新增工作的專案。</span><span class="sxs-lookup"><span data-stu-id="49b9e-114">Go to **Projects** and open the project to which you want to add tasks.</span></span>
2. <span data-ttu-id="49b9e-115">選取 **新增工作**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-115">Select **Add new task**.</span></span> <span data-ttu-id="49b9e-116">命名工作，然後按 **Enter**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-116">Name the task, and then press **Enter**.</span></span>
3. <span data-ttu-id="49b9e-117">輸入另一個工作名稱，然後按 **Enter**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-117">Enter another task name and press **Enter**.</span></span> <span data-ttu-id="49b9e-118">重複此步驟，直到有完整的工作清單為止。</span><span class="sxs-lookup"><span data-stu-id="49b9e-118">Repeat this until you have a full list of tasks.</span></span>
3. <span data-ttu-id="49b9e-119">若要在 **摘要** 工作下縮排工作，請選取工作名稱旁的三個垂直圓點，然後選取 **建立子工作**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-119">To indent tasks under **Summary** tasks, select the three vertical dots by the task name, and then select **Make subtask**.</span></span> 

  > [!TIP]
  > <span data-ttu-id="49b9e-120">若要選取多個工作，請選取一個工作，按住 **Ctrl** 鍵，然後選取另一個工作。</span><span class="sxs-lookup"><span data-stu-id="49b9e-120">To select more than one task, select a task, press and hold **Ctrl**, and then select another task.</span></span>
  >
  > <span data-ttu-id="49b9e-121">您也可以選擇 **升級子工作**，從 **摘要** 工作底下移出工作。</span><span class="sxs-lookup"><span data-stu-id="49b9e-121">You can also choose **Promote subtask** to move tasks out from under **Summary** tasks.</span></span>

### <a name="assign-tasks"></a><span data-ttu-id="49b9e-122">指派工作</span><span class="sxs-lookup"><span data-stu-id="49b9e-122">Assign tasks</span></span>

<span data-ttu-id="49b9e-123">完成下列步驟以指派工作。</span><span class="sxs-lookup"><span data-stu-id="49b9e-123">Complete the following steps to assign tasks.</span></span>

1. <span data-ttu-id="49b9e-124">在工作的 **指派至** 欄中，選取人員圖示。</span><span class="sxs-lookup"><span data-stu-id="49b9e-124">In the  **Assigned to**  column for a task, select the person icon.</span></span>
2. <span data-ttu-id="49b9e-125">從清單中選取團隊成員，或輸入文字以搜尋名稱。</span><span class="sxs-lookup"><span data-stu-id="49b9e-125">Choose a team member from the list or enter text to search for a name.</span></span>

### <a name="add-task-duration-and-columns"></a><span data-ttu-id="49b9e-126">新增工作期間和欄</span><span class="sxs-lookup"><span data-stu-id="49b9e-126">Add task duration and columns</span></span>

<span data-ttu-id="49b9e-127">使用期間開始建構您的專案通常最為簡單。</span><span class="sxs-lookup"><span data-stu-id="49b9e-127">It's often easiest to begin constructing your project with duration.</span></span> <span data-ttu-id="49b9e-128">完成下列步驟以新增工作期間。</span><span class="sxs-lookup"><span data-stu-id="49b9e-128">Complete the following steps to add a task duration.</span></span>

1. <span data-ttu-id="49b9e-129">在工作的 **期間** 欄中，輸入您認為完成該工作所花費的天數。</span><span class="sxs-lookup"><span data-stu-id="49b9e-129">In the **Duration** column for a task, type the number of days you think it will take to accomplish the task.</span></span> <span data-ttu-id="49b9e-130">如果您想要使用不同的時間單位，請輸入數字加上 **小時**、**週** 或 **月** 等字。</span><span class="sxs-lookup"><span data-stu-id="49b9e-130">If you want to use a different unit of time, enter a number plus the word **hours**, **weeks**, or **months**.</span></span>
2. <span data-ttu-id="49b9e-131">如果想要讓工作在 **時間表** 檢視中顯示為菱形里程碑，請在 **期間** 欄中輸入 **0 天**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-131">If you want your task to appear as a diamond-shaped milestone in the **Timeline** view, in the **Duration** column, enter **0 days** .</span></span>
3. <span data-ttu-id="49b9e-132">按 **Enter** 移至下一個工作的 **期間** 欄位，並繼續輸入期間。</span><span class="sxs-lookup"><span data-stu-id="49b9e-132">Press **Enter**  to go to the next task's **Duration** field and continue entering durations.</span></span>

  > [!NOTE]
  > <span data-ttu-id="49b9e-133">您不能輸入摘要工作的期間。</span><span class="sxs-lookup"><span data-stu-id="49b9e-133">You can't enter a duration for summary tasks.</span></span>

<span data-ttu-id="49b9e-134">您可以將欄新增至專案，以提供更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="49b9e-134">You can add columns to your project to provide more details.</span></span> <span data-ttu-id="49b9e-135">若要這樣做，請選取 **新增欄**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-135">To do this, select **Add column**.</span></span> 

<span data-ttu-id="49b9e-136">如需詳細資訊，請參閱[建立專案](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749)。</span><span class="sxs-lookup"><span data-stu-id="49b9e-136">For more information, see [Create a project](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).</span></span>

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="49b9e-137">為一般專案團隊成員設定角色與組織單位</span><span class="sxs-lookup"><span data-stu-id="49b9e-137">Set up the role and organization unit for a generic project team member</span></span>
<span data-ttu-id="49b9e-138">請完成下列步驟，為一般團隊成員設定角色和組織單位。</span><span class="sxs-lookup"><span data-stu-id="49b9e-138">Complete the following steps to set up a role and organizational unit for a generic team member.</span></span>

1. <span data-ttu-id="49b9e-139">在 **工作** 頁面上，選取 **工作 A** 的 **工作** 列。</span><span class="sxs-lookup"><span data-stu-id="49b9e-139">On the **Tasks** page, select the **Task** row for **Task A**.</span></span> 
2. <span data-ttu-id="49b9e-140">在 **指派至** 中，選取 **新增一般資源**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-140">In **Assigned To**, select **Add generic resource**.</span></span> <span data-ttu-id="49b9e-141">這會開啟 **團隊成員快速建立** 頁面。</span><span class="sxs-lookup"><span data-stu-id="49b9e-141">This opens the **Team Member Quick Create** page.</span></span>
3. <span data-ttu-id="49b9e-142">在 **團隊成員快速建立** 頁面上，指定可執行此工作之一般團隊成員的屬性。</span><span class="sxs-lookup"><span data-stu-id="49b9e-142">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="49b9e-143">選取適當的角色與組織單位，然後選取 **儲存後關閉**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-143">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="49b9e-144">隨即會建立一般團隊成員，並將其指派至此工作。</span><span class="sxs-lookup"><span data-stu-id="49b9e-144">A generic team member is created and assigned to this task.</span></span> 
5. <span data-ttu-id="49b9e-145">對於 **工作 B**，重複步驟 1-4。但是，**工作 B** 必須為一般團隊成員指派不同於 **工作 A** 的角色和組織單位。</span><span class="sxs-lookup"><span data-stu-id="49b9e-145">Repeat steps 1-4 for **Task B**. However, **Task B** must have a different role and organizational unit assigned for the generic team member than **Task A**.</span></span> 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="49b9e-146">為專案工作設定角色與組織單位</span><span class="sxs-lookup"><span data-stu-id="49b9e-146">Set up the role and organization unit for a project task</span></span>
<span data-ttu-id="49b9e-147">請完成下列步驟，為工作設定角色和組織單位。</span><span class="sxs-lookup"><span data-stu-id="49b9e-147">Complete the following steps to set up a role and organizational unit for a task.</span></span>

1. <span data-ttu-id="49b9e-148">建立 **工作 A** 之後，請選取該工作，然後選取 **i** 圖示，開啟 **工作詳細資料** 窗格。</span><span class="sxs-lookup"><span data-stu-id="49b9e-148">After you create **Task A**, select the task, and then select the **i** icon to open the **Task Details** pane.</span></span> 
2. <span data-ttu-id="49b9e-149">在 **工作詳細資料** 窗格中，捲動至底部，然後選取 **檢視詳細資料**，以開啟 **工作詳細資料** 頁面。</span><span class="sxs-lookup"><span data-stu-id="49b9e-149">On the **Task Details** pane, scroll to the bottom and select **View Details** to open the **Task Details** page.</span></span>
3. <span data-ttu-id="49b9e-150">在 **工作詳細資料** 頁面的 **角色** 與 **組織單位** 中，新增為資源執行此工作所需的值。</span><span class="sxs-lookup"><span data-stu-id="49b9e-150">On the **Task Details** page, in **Role** and **Organizational Unit**, add the values that are required to perform this task for the resource.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="49b9e-151">如果您使用 Project Operations 示範資料來完成此案例，請為角色選取 **諮詢主管**，然後選取 **Fabrikam US** 做為組織單位。</span><span class="sxs-lookup"><span data-stu-id="49b9e-151">If you complete this scenario using the Project Operations demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

4. <span data-ttu-id="49b9e-152">選取 **工作 B**，然後選取工作。</span><span class="sxs-lookup"><span data-stu-id="49b9e-152">Select **Task B**, and then select the task.</span></span>
5. <span data-ttu-id="49b9e-153">選取 **i** 圖示以開啟 **工作詳細資料** 窗格。</span><span class="sxs-lookup"><span data-stu-id="49b9e-153">Select the **i** icon to open **Task Details** pane.</span></span> 
6. <span data-ttu-id="49b9e-154">在 **工作詳細資料** 窗格中，捲動至底部，然後選取 **檢視詳細資料**，以開啟 **工作詳細資料** 頁面。</span><span class="sxs-lookup"><span data-stu-id="49b9e-154">On the **Task Details** pane, scroll to the bottom and select **View details** to open the **Task Details** page.</span></span>
7. <span data-ttu-id="49b9e-155">在 **工作詳細資料** 頁面的 **角色** 與 **組織單位** 中，新增執行此任務的資源所需的值。</span><span class="sxs-lookup"><span data-stu-id="49b9e-155">On the **Task Details** page, in **Role** and **Organizational Unit**, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="49b9e-156">**工作 B** 的 **角色** 與 **組織單位** 中的值必須與 **工作 A** 的不同。</span><span class="sxs-lookup"><span data-stu-id="49b9e-156">The values in **Role** and **Organizational Unit** for **Task B** must be different than those for **Task A**.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="49b9e-157">如果您使用 Project Operations 示範資料來完成此案例，請為角色選取 **網路技術人員**，然後選取 **Fabrikam US** 做為組織單位。</span><span class="sxs-lookup"><span data-stu-id="49b9e-157">If you complete this scenario using the Project Operations demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

8. <span data-ttu-id="49b9e-158">儲存並關閉 **工作詳細資料** 頁面。</span><span class="sxs-lookup"><span data-stu-id="49b9e-158">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="49b9e-159">團隊成員和估計行為</span><span class="sxs-lookup"><span data-stu-id="49b9e-159">Team member and estimates behavior</span></span> 
<span data-ttu-id="49b9e-160">若要瞭解 **團隊成員** 網格和估計的行為，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="49b9e-160">To understand the behavior on the **Team Member** grid and the estimates, complete the following steps.</span></span>

1. <span data-ttu-id="49b9e-161">在 **團隊成員** 網格中，選取兩個一般團隊成員，然後選取 **產生需求**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-161">On the **Team Member** grid, select the two generic team members, and then select **Generate Requirements**.</span></span> <span data-ttu-id="49b9e-162">這樣會產生一般資源需求。</span><span class="sxs-lookup"><span data-stu-id="49b9e-162">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="49b9e-163">選取 **諮詢主管** 的團隊成員列，然後選取 **預約**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-163">Select the team member row for **Consulting Lead**, and then select **Book**.</span></span> <span data-ttu-id="49b9e-164">排程面板隨即開啟，其中有一份資源清單。</span><span class="sxs-lookup"><span data-stu-id="49b9e-164">The schedule board opens with a list of resources.</span></span> <span data-ttu-id="49b9e-165">選取資源，然後選取 **預約**，將資源預約給該需求。</span><span class="sxs-lookup"><span data-stu-id="49b9e-165">Select a resource and then select **Book** to book the resource to that requirement.</span></span>
3. <span data-ttu-id="49b9e-166">選取 **網路技術人員** 的團隊成員列，然後選取 **預約**。</span><span class="sxs-lookup"><span data-stu-id="49b9e-166">Select the team member row for **Network Technician**, and then select **Book**.</span></span> <span data-ttu-id="49b9e-167">排程面板隨即開啟，其中有一份資源清單。</span><span class="sxs-lookup"><span data-stu-id="49b9e-167">The schedule board opens with a list of resources.</span></span> <span data-ttu-id="49b9e-168">選取與上述相同的資源，然後選取 **預約**，將資源預約給該需求。</span><span class="sxs-lookup"><span data-stu-id="49b9e-168">Select the same resource as above and then select **Book** to book the resource to that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="49b9e-169">團隊成員網格</span><span class="sxs-lookup"><span data-stu-id="49b9e-169">Team Member grid</span></span> 

<span data-ttu-id="49b9e-170">在 **團隊成員** 網格中，兩個一般團隊成員記錄會被刪除，並僅取代為一個資源。</span><span class="sxs-lookup"><span data-stu-id="49b9e-170">On the **Team Member** grid, the two generic team member records are deleted and replaced with only one resource.</span></span> <span data-ttu-id="49b9e-171">該資源有一組值，這是 **角色** 和 **組織單位** 的預設值集。</span><span class="sxs-lookup"><span data-stu-id="49b9e-171">There is one set of values for that resource, which are a default set of values for **Role** and **Organizational Unit**.</span></span>

<span data-ttu-id="49b9e-172">當您展開該團隊成員記錄的列時，您可以在團隊成員記錄上為這兩個工作顯示不同的工作表示。</span><span class="sxs-lookup"><span data-stu-id="49b9e-172">When you expand the row for that team member record, you can see distinct assignments on the team member record for both tasks.</span></span> <span data-ttu-id="49b9e-173">每個指派列在 **角色** 和 **組織單位** 中都會有工作特定的值。</span><span class="sxs-lookup"><span data-stu-id="49b9e-173">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="49b9e-174">估計值網格</span><span class="sxs-lookup"><span data-stu-id="49b9e-174">Estimates grid</span></span> 

<span data-ttu-id="49b9e-175">在 **估計值** 網格上，相同資源的這兩個指派的定價方式不同。</span><span class="sxs-lookup"><span data-stu-id="49b9e-175">On the **Estimates** grid, both assignments for the same resource are priced differently.</span></span> <span data-ttu-id="49b9e-176">**工作 A** 的資源指派是使用 **諮詢主管** 的 **角色** 屬性值來定價。</span><span class="sxs-lookup"><span data-stu-id="49b9e-176">The assignment for the resource on **Task A** is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="49b9e-177">同一個資源在 **工作 B** 上的指派是使用 **網路技術人員** 的 **角色** 屬性值來定價。</span><span class="sxs-lookup"><span data-stu-id="49b9e-177">The assignment for the same resource on **Task B** is priced using the **Role** attribute value of **Network Technician**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]