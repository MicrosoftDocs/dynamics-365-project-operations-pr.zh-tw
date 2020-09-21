---
title: 專案資源分配
description: 本主題提供有關專案資源分配的資訊。
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749851"
---
# <a name="project-resourcing"></a><span data-ttu-id="06dba-103">專案資源分配</span><span class="sxs-lookup"><span data-stu-id="06dba-103">Project resourcing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06dba-104">本主題提供有關專案資源分配的資訊。</span><span class="sxs-lookup"><span data-stu-id="06dba-104">This topic provides information about project resourcing.</span></span>

<span data-ttu-id="06dba-105">專案規劃階段對專案經理和資源管理員的一項挑戰是資源配置，他們必須在其中判斷和保留要在專案上使用的正確資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-105">One challenge for project managers and resource managers during the project planning stage is resource allocation, where they must determine and reserve the correct resource to work on a project.</span></span> <span data-ttu-id="06dba-106">在 Dynamics 365 Finance 中 ，專案的資源分配功能可讓您定義視為暫時資源 (可保留用作特定業務開發或業務開發的一部分) 的角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-106">In Dynamics 365 Finance, resourcing capabilities for projects let you define roles that are treated as temporary resources that can be reserved for a specific engagement or part of an engagement.</span></span> <span data-ttu-id="06dba-107">此類型的資源分配可讓專案經理和資源管理員完成下列工作：</span><span class="sxs-lookup"><span data-stu-id="06dba-107">This type of resourcing lets project managers and resource managers complete the following tasks:</span></span>

- <span data-ttu-id="06dba-108">定義具備所需專長的角色，這樣就可以輕鬆地找到適配的資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-108">Define a role that has the required competencies, so that it's easy to match resources.</span></span>
- <span data-ttu-id="06dba-109">使用角色來定義以保留的資源為基礎的初始業務開發排程。</span><span class="sxs-lookup"><span data-stu-id="06dba-109">Use roles to define an initial engagement schedule that is based on reserved resources.</span></span>
- <span data-ttu-id="06dba-110">根據指派給專案的角色和資源，估計成本並決定初始預算。</span><span class="sxs-lookup"><span data-stu-id="06dba-110">Estimate costs and determine an initial budget, based on assigned roles and resources for a project.</span></span>
- <span data-ttu-id="06dba-111">使用角色來估計每項業務開發所需的資源保留數目。</span><span class="sxs-lookup"><span data-stu-id="06dba-111">Use roles to estimate the number of resource reservations that are required for each engagement.</span></span>
- <span data-ttu-id="06dba-112">估計專案整個生命週期所需的資源數目。</span><span class="sxs-lookup"><span data-stu-id="06dba-112">Estimate the number of resources that are required for the whole life cycle of a project.</span></span>
- <span data-ttu-id="06dba-113">使用初始資源指派來草擬分工結構圖 (WBS)。</span><span class="sxs-lookup"><span data-stu-id="06dba-113">Draft a work breakdown structure (WBS) by using the initial resource assignments.</span></span>

<span data-ttu-id="06dba-114">[![專案生命週期](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span><span class="sxs-lookup"><span data-stu-id="06dba-114">[![Project life cycle](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)</span></span>

<span data-ttu-id="06dba-115">在專案規劃繼續進行的過程中，可將規劃的資源取代為人員配置資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-115">As project planning proceeds, planned resources can be replaced with staffed resources.</span></span> <span data-ttu-id="06dba-116">專案經理也可以在任何專案階段返回並更新資源分配保留。</span><span class="sxs-lookup"><span data-stu-id="06dba-116">The project manager can also go back and update the resourcing reservations during any project stage.</span></span>

## <a name="set-up-project-resources"></a><span data-ttu-id="06dba-117">設定專案資源</span><span class="sxs-lookup"><span data-stu-id="06dba-117">Set up project resources</span></span>
<span data-ttu-id="06dba-118">您必須設定行事曆，並將其與員工或工作者建立關聯。</span><span class="sxs-lookup"><span data-stu-id="06dba-118">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="06dba-119">行事曆會用來排定專案以及專案所保留資源的工作時間。</span><span class="sxs-lookup"><span data-stu-id="06dba-119">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="06dba-120">在行事曆設定期間，專案經理可以在資源最佳化的過程中進行資源撫平。</span><span class="sxs-lookup"><span data-stu-id="06dba-120">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="06dba-121">根據行事曆排程，可以對資源加以限制。</span><span class="sxs-lookup"><span data-stu-id="06dba-121">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="06dba-122">您可以在**行事曆**頁面上設定行事曆。</span><span class="sxs-lookup"><span data-stu-id="06dba-122">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="06dba-123">將工作者設定為專案資源時，您可以選取任職於資源需要進行設定之公司中的工作者。</span><span class="sxs-lookup"><span data-stu-id="06dba-123">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="06dba-124">或者，也可以從您組織中的其他公司選取工作者。</span><span class="sxs-lookup"><span data-stu-id="06dba-124">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="06dba-125">這些工作者稱為公司間的資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-125">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="06dba-126">下列程序說明如何將工作者設定為公司中的專案資源，以及如何設定公司間的專案資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-126">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

### <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="06dba-127">將工作者設定為專案資源</span><span class="sxs-lookup"><span data-stu-id="06dba-127">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="06dba-128">在**工作者**頁面的**工作者**清單中，選取您要新增為專案資源的工作者，然後開啟工作者記錄。</span><span class="sxs-lookup"><span data-stu-id="06dba-128">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="06dba-129">在動作窗格中，選取**專案** &gt; **設定** &gt; **專案設定**。</span><span class="sxs-lookup"><span data-stu-id="06dba-129">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="06dba-130">選取行事曆，然後關閉頁面。</span><span class="sxs-lookup"><span data-stu-id="06dba-130">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="06dba-131">您也可以將資源的預設專案指定為預先指派的類型。</span><span class="sxs-lookup"><span data-stu-id="06dba-131">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="06dba-132">當資源管理員或專案經理預先知道資源要處理哪些專案時，可以使用預先指派。</span><span class="sxs-lookup"><span data-stu-id="06dba-132">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="06dba-133">也可以根據專案贊助者或客戶的要求使用預先指派。</span><span class="sxs-lookup"><span data-stu-id="06dba-133">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="06dba-134">若要預先指派專案，請在**指派專案**頁面的**專案**索引標籤上，從**剩餘專案**清單中選取適當的專案。</span><span class="sxs-lookup"><span data-stu-id="06dba-134">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

### <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="06dba-135">設定公司間的資源</span><span class="sxs-lookup"><span data-stu-id="06dba-135">Set up an intercompany resource</span></span>

<span data-ttu-id="06dba-136">將工作者設定為公司間的資源時，您在出借公司和借用公司中都必須完成設定。</span><span class="sxs-lookup"><span data-stu-id="06dba-136">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

<span data-ttu-id="06dba-137">**在出借公司中**</span><span class="sxs-lookup"><span data-stu-id="06dba-137">**In the lending company**</span></span>

1. <span data-ttu-id="06dba-138">在 Finance 中，確認已選取出借公司，然後完成上一節「將工作者設定為專案資源」中的程序。</span><span class="sxs-lookup"><span data-stu-id="06dba-138">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="06dba-139">在**公司間會計**頁面，選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="06dba-139">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="06dba-140">在**法律實體識別碼**欄位中，選取出借公司。</span><span class="sxs-lookup"><span data-stu-id="06dba-140">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="06dba-141">適當填入剩餘欄位，然後選取**儲存**。</span><span class="sxs-lookup"><span data-stu-id="06dba-141">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="06dba-142">在**轉撥價格**頁面，選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="06dba-142">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="06dba-143">在**借用法律實體**欄位中，選取適當的公司。</span><span class="sxs-lookup"><span data-stu-id="06dba-143">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="06dba-144">若只要出借您在本節開始時所建立的資源給借用公司，請在**資源**欄位中，選取您所建立資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06dba-144">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="06dba-145">若要讓出借公司的所有資源皆可供借用公司使用，請讓**資源**欄位保持空白。</span><span class="sxs-lookup"><span data-stu-id="06dba-145">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="06dba-146">在**專案管理與會計參數**頁面的**公司之間**索引標籤上，將**啟用公司間的資源排程和時程表**選項設定為**是**。</span><span class="sxs-lookup"><span data-stu-id="06dba-146">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

<span data-ttu-id="06dba-147">**在借用公司中**</span><span class="sxs-lookup"><span data-stu-id="06dba-147">**In the borrowing company**</span></span>

- <span data-ttu-id="06dba-148">在**資源清單**頁面的搜尋篩選中，輸入出借公司所建立資源的名稱，以確認該名稱是否已包含在借用公司的資源清單中。</span><span class="sxs-lookup"><span data-stu-id="06dba-148">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="manage-resource-competencies"></a><span data-ttu-id="06dba-149">管理資源專長</span><span class="sxs-lookup"><span data-stu-id="06dba-149">Manage resource competencies</span></span>
<span data-ttu-id="06dba-150">資源專長是資源管理不可缺少的一部分。</span><span class="sxs-lookup"><span data-stu-id="06dba-150">Resource competencies are an essential part of resource management.</span></span> <span data-ttu-id="06dba-151">專長可做為基準，用以判定其技能、教育、認證和專案經驗達到適當平衡的資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-151">Competencies can be used as a baseline to determine resources that have the correct balance of skills, education, certification, and project experience.</span></span> <span data-ttu-id="06dba-152">您應該為每個資源設定此資訊，並定期更新。</span><span class="sxs-lookup"><span data-stu-id="06dba-152">You should set up this information for each resource and update it on a regular basis.</span></span> <span data-ttu-id="06dba-153">如此一來，您就可以在專案資源指派期間找到適配的特定資源專長時，使其能力發揮最大效益。</span><span class="sxs-lookup"><span data-stu-id="06dba-153">In this way, you can maximize capabilities when specific resource competencies are matched during project resource assignment.</span></span>

<span data-ttu-id="06dba-154">[![技能、認證、教育和專案經驗的範例](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span><span class="sxs-lookup"><span data-stu-id="06dba-154">[![Examples of skills, certifications, education, and project experience](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span></span>

<span data-ttu-id="06dba-155">下列程序說明如何設定資源的一些專長。</span><span class="sxs-lookup"><span data-stu-id="06dba-155">The following procedures explain how to set up some of the competencies for a resource.</span></span>

<span data-ttu-id="06dba-156">若要設定工作者的專長，您可以使用 [人力資源] 中的**工作者**清單或 [專案管理與會計] 中的**資源**清單。</span><span class="sxs-lookup"><span data-stu-id="06dba-156">To set up competencies for a worker, you can use either the **Workers** list page in Human resources or the **Resources** list page in Project management and accounting.</span></span> <span data-ttu-id="06dba-157">在下列程序中，使用 [人力資源] 中的**工作者**清單頁面。</span><span class="sxs-lookup"><span data-stu-id="06dba-157">For the following procedures, the **Workers** list page in Human resources is used.</span></span>

### <a name="set-up-competencies-certificates"></a><span data-ttu-id="06dba-158">設定專長：認證</span><span class="sxs-lookup"><span data-stu-id="06dba-158">Set up competencies: Certificates</span></span>

1. <span data-ttu-id="06dba-159">在**工作者**清單頁面上，選取工作者的一行以新增其認證資訊。</span><span class="sxs-lookup"><span data-stu-id="06dba-159">On the **Workers** list page, select the line for the worker to add certificate information for.</span></span>
2. <span data-ttu-id="06dba-160">在動作窗格的**工作者**索引標籤上，選取**專長**群組中的**認證**。</span><span class="sxs-lookup"><span data-stu-id="06dba-160">On the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Certificates**.</span></span>
3. <span data-ttu-id="06dba-161">選取**新增**，然後在**認證類型**欄位中選取 **PMP**。</span><span class="sxs-lookup"><span data-stu-id="06dba-161">Select **New**, and then, in the **Certificate type** field, select **PMP**.</span></span>
4. <span data-ttu-id="06dba-162">在**開始日期**欄位中，選取 **2015/10/1**，然後選取**儲存**。</span><span class="sxs-lookup"><span data-stu-id="06dba-162">In the **Start date** field, select **10/1/2015**, and select **Save**.</span></span>

### <a name="set-up-competencies-skills"></a><span data-ttu-id="06dba-163">設定專長：技能</span><span class="sxs-lookup"><span data-stu-id="06dba-163">Set up competencies: Skills</span></span>

1. <span data-ttu-id="06dba-164">在**工作者**清單頁面上，確定您在先前程序中使用的工作者仍處於已選取狀態。</span><span class="sxs-lookup"><span data-stu-id="06dba-164">On the **Workers** list page, make sure that the worker that you used in the previous procedure is still selected.</span></span> <span data-ttu-id="06dba-165">然後，在動作窗格的**工作者**索引標籤上，選取**專長**群組中的**技能**。</span><span class="sxs-lookup"><span data-stu-id="06dba-165">Then, on the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Skills**.</span></span>
2. <span data-ttu-id="06dba-166">選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="06dba-166">Select **New**.</span></span>
3. <span data-ttu-id="06dba-167">在**技能**欄位中，選取**專案管理**。</span><span class="sxs-lookup"><span data-stu-id="06dba-167">In the **Skill** field, select **Project management**.</span></span>
4. <span data-ttu-id="06dba-168">在**等級**欄位中，選取 **5 專家**。</span><span class="sxs-lookup"><span data-stu-id="06dba-168">In the **Level** field, select **5 Expert**.</span></span>
5. <span data-ttu-id="06dba-169">在**等級日期**欄位中，選取 **1-/14/2014**。</span><span class="sxs-lookup"><span data-stu-id="06dba-169">In the **Level date** field, select **1-/14/2014**.</span></span>
6. <span data-ttu-id="06dba-170">在**經驗年數**欄位中，輸入 **10**。</span><span class="sxs-lookup"><span data-stu-id="06dba-170">In the **Years of experience** field, enter **10**.</span></span>
7. <span data-ttu-id="06dba-171">選取**儲存**，然後關閉頁面。</span><span class="sxs-lookup"><span data-stu-id="06dba-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-new-project"></a><span data-ttu-id="06dba-172">建立新專案</span><span class="sxs-lookup"><span data-stu-id="06dba-172">Create a new project</span></span>
1. <span data-ttu-id="06dba-173">在**專案管理**頁面上，選取**新增專案**，並輸入下列值：</span><span class="sxs-lookup"><span data-stu-id="06dba-173">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="06dba-174">**專案類型：** 時間和材料</span><span class="sxs-lookup"><span data-stu-id="06dba-174">**Project type:** Time and material</span></span>
    - <span data-ttu-id="06dba-175">**專案名稱：** XYZ 升級階段 2</span><span class="sxs-lookup"><span data-stu-id="06dba-175">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="06dba-176">**專案群組：** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="06dba-176">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="06dba-177">**專案合約識別碼：** 00000002</span><span class="sxs-lookup"><span data-stu-id="06dba-177">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="06dba-178">選取**建立專案**。</span><span class="sxs-lookup"><span data-stu-id="06dba-178">Select **Create project**.</span></span>

### <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="06dba-179">將資源指派至專案</span><span class="sxs-lookup"><span data-stu-id="06dba-179">Assign a resource to a project</span></span>

1. <span data-ttu-id="06dba-180">在**工作者**頁面的**工作者**清單中，選取先前已設定專長之工作者的記錄，然後開啟工作者記錄。</span><span class="sxs-lookup"><span data-stu-id="06dba-180">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="06dba-181">在動作窗格的**專案**索引標籤上，選取**設定**群組中的**指派專案**。</span><span class="sxs-lookup"><span data-stu-id="06dba-181">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="06dba-182">在**資源驗證專案指派**頁面的**專案**索引標籤上，篩選**將專案新增至選取的專案**欄位中的 **XYZ 升級階段 2** 專案。</span><span class="sxs-lookup"><span data-stu-id="06dba-182">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="06dba-183">在**剩餘專案**窗格中，選取專案並選取箭頭按鈕，將該專案新增至**選取的專案**窗格。</span><span class="sxs-lookup"><span data-stu-id="06dba-183">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="06dba-184">您也可以視需要指派資源的類別。</span><span class="sxs-lookup"><span data-stu-id="06dba-184">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="06dba-185">類別類型會是**成本**或**營收**。</span><span class="sxs-lookup"><span data-stu-id="06dba-185">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="06dba-186">類別類型是由您的組織所決定。</span><span class="sxs-lookup"><span data-stu-id="06dba-186">The category type is determined by your organization.</span></span> <span data-ttu-id="06dba-187">如果未指派資源的類別，Finance 會針對成本與營收查詢工時價格的預設類別。</span><span class="sxs-lookup"><span data-stu-id="06dba-187">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

### <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="06dba-188">設定專案資源和角色特性</span><span class="sxs-lookup"><span data-stu-id="06dba-188">Set up project resource and role characteristics</span></span>

<span data-ttu-id="06dba-189">專案經理可以使用專案資源分配功能來建立專案所需的角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-189">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="06dba-190">如果已確認的資源在保留資源時仍然未知，則可以使用角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-190">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="06dba-191">角色可以暫時保留為規劃的資源，讓您可以繼續專案規劃階段。</span><span class="sxs-lookup"><span data-stu-id="06dba-191">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="06dba-192">[![角色的範例](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="06dba-192">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="06dba-193">**案例：** 吳先生受聘來完成專案章程已獲核准的時間與材料專案。</span><span class="sxs-lookup"><span data-stu-id="06dba-193">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="06dba-194">專案襄理仍在完成專案的範圍。</span><span class="sxs-lookup"><span data-stu-id="06dba-194">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="06dba-195">資源管理員目前正在識別要保留來處理新專案的特定資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-195">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="06dba-196">由於專案的性質至關重要，專案贊助者要求資深專案經理成為其中一個角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-196">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="06dba-197">專案襄理在專案規劃期間說不定需要資源資訊，資源管理員必須取得新資源，並定義系統中的角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-197">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="06dba-198">下列步驟顯示資源管理員如何設定資深專案經理角色，並建立資源特性與該角色的關聯。</span><span class="sxs-lookup"><span data-stu-id="06dba-198">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="06dba-199">此角色隨後即可用於搜尋符合所需資源專長的可用資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-199">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="06dba-200">在**設定角色**頁面上，選取**新增**，並輸入下列值：</span><span class="sxs-lookup"><span data-stu-id="06dba-200">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="06dba-201">**角色識別碼：** 資深專案經理</span><span class="sxs-lookup"><span data-stu-id="06dba-201">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="06dba-202">**描述：** 資深專案經理</span><span class="sxs-lookup"><span data-stu-id="06dba-202">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="06dba-203">選取**建立**。</span><span class="sxs-lookup"><span data-stu-id="06dba-203">Select **Create**.</span></span>
3. <span data-ttu-id="06dba-204">選取**資深專案經理**角色，然後選取**設定特性**。</span><span class="sxs-lookup"><span data-stu-id="06dba-204">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="06dba-205">在**特性類型**欄位中，選取**技能**。</span><span class="sxs-lookup"><span data-stu-id="06dba-205">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="06dba-206">在**可用特性**欄位中，輸入要搜尋的技能。</span><span class="sxs-lookup"><span data-stu-id="06dba-206">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="06dba-207">在**特性類型**欄位中，選取**認證**。</span><span class="sxs-lookup"><span data-stu-id="06dba-207">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="06dba-208">在**可用特性**欄位中，輸入要搜尋的認證類型。</span><span class="sxs-lookup"><span data-stu-id="06dba-208">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

### <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="06dba-209">將專案資源指派至專案</span><span class="sxs-lookup"><span data-stu-id="06dba-209">Assign a project resource to a project</span></span>

1. <span data-ttu-id="06dba-210">在**所有專案**頁面上，選取 **XYZ 升級階段 2** 專案。</span><span class="sxs-lookup"><span data-stu-id="06dba-210">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="06dba-211">在**專案團隊與排程**索引標籤上，選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="06dba-211">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="06dba-212">在**角色**欄位中，選取**團隊成員**。</span><span class="sxs-lookup"><span data-stu-id="06dba-212">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="06dba-213">選取**從行事曆預約**。</span><span class="sxs-lookup"><span data-stu-id="06dba-213">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="06dba-214">在**資源可用性**頁面上，選取**檢視設定**。</span><span class="sxs-lookup"><span data-stu-id="06dba-214">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="06dba-215">在**調整檢視設定**頁面上，輸入下列值：</span><span class="sxs-lookup"><span data-stu-id="06dba-215">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="06dba-216">**日期範圍檢視格式：** 日</span><span class="sxs-lookup"><span data-stu-id="06dba-216">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="06dba-217">**顯示可用性描述：** 是</span><span class="sxs-lookup"><span data-stu-id="06dba-217">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="06dba-218">**顯示剩餘產能：** 是</span><span class="sxs-lookup"><span data-stu-id="06dba-218">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="06dba-219">在資源清單中選取資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-219">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="06dba-220">選取**已確認預約**和**完整產能**。</span><span class="sxs-lookup"><span data-stu-id="06dba-220">Select **Hard book** and **Full capacity**.</span></span>


### <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="06dba-221">將資源指派給預設角色</span><span class="sxs-lookup"><span data-stu-id="06dba-221">Assign a resource to a default role</span></span>

<span data-ttu-id="06dba-222">為了協助專案經理或資源管理員，您可以進一步向下切入可為專案保留的資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-222">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="06dba-223">您可以將預設角色與現有資源或新取得資源建立關聯。</span><span class="sxs-lookup"><span data-stu-id="06dba-223">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="06dba-224">例如，雇用 Daniel 時，他具備承擔商務分析員角色的經驗和技能。</span><span class="sxs-lookup"><span data-stu-id="06dba-224">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="06dba-225">資源管理員已將此角色指派為 Daniel 的預設角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-225">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="06dba-226">因此，資源管理員已將 Daniel 加入適用於處理專案的業務分析師備選名單中。</span><span class="sxs-lookup"><span data-stu-id="06dba-226">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="06dba-227">進行資源保留時，專案經理可以篩選適用於處理專案的角色資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-227">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="06dba-228">在資源履行期間執行多重準則決策分析時，他們可以使用此資訊做為一項準則。</span><span class="sxs-lookup"><span data-stu-id="06dba-228">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="06dba-229">他們也可以將其他資源特性新增至篩選，以搜尋具備指定專案所需特定技能、教育和經驗的資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-229">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="06dba-230">**案例：** 獲核准的專案已開始進展，而資深專案經理角色已專案規劃階段中保留為規劃的資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-230">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="06dba-231">資源經理現在已取得資源來履行資深專案經理角色的職責。</span><span class="sxs-lookup"><span data-stu-id="06dba-231">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="06dba-232">在**資源清單**頁面中，選取 **Daniel Goldschmidt**。</span><span class="sxs-lookup"><span data-stu-id="06dba-232">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="06dba-233">在**資源角色**頁面上，選取**新增**，並輸入下列值：</span><span class="sxs-lookup"><span data-stu-id="06dba-233">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="06dba-234">**生效日：** 輸入目前的日期。</span><span class="sxs-lookup"><span data-stu-id="06dba-234">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="06dba-235">**到期日：** 輸入**永不**。</span><span class="sxs-lookup"><span data-stu-id="06dba-235">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="06dba-236">**角色：** 輸入**資深專案經理**。</span><span class="sxs-lookup"><span data-stu-id="06dba-236">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="06dba-237">選取**儲存**，然後關閉頁面。</span><span class="sxs-lookup"><span data-stu-id="06dba-237">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="06dba-238">在**專長**索引標籤中，新增 **ProjectMgmt** 技能和 **PMP** 認證。</span><span class="sxs-lookup"><span data-stu-id="06dba-238">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>

## <a name="set-up-role-based-pricing"></a><span data-ttu-id="06dba-239">設定角色定價</span><span class="sxs-lookup"><span data-stu-id="06dba-239">Set up role-based pricing</span></span>
<span data-ttu-id="06dba-240">所有成本、銷售和轉撥價格都可以用來設定角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-240">All cost, sales, and transfer prices can be set up for roles.</span></span>

1. <span data-ttu-id="06dba-241">在**售價 (小時)** 頁面上，選取**新增**，然後輸入生效日期。</span><span class="sxs-lookup"><span data-stu-id="06dba-241">On the **Sales price (hour)** page, select **New**, and enter an effective date.</span></span>
2. <span data-ttu-id="06dba-242">在**角色**欄中，選取角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-242">In the **Role** column, select a role.</span></span>
3. <span data-ttu-id="06dba-243">在**定價**欄中，輸入所選資源角色的價格。</span><span class="sxs-lookup"><span data-stu-id="06dba-243">In the **Pricing** column, enter a price for the selected resource role.</span></span>

## <a name="form-a-project-team"></a><span data-ttu-id="06dba-244">組成專案團隊</span><span class="sxs-lookup"><span data-stu-id="06dba-244">Form a project team</span></span>
<span data-ttu-id="06dba-245">若要使用先前已在專案中設定的角色，專案經理必須將角色與專案建立關聯。</span><span class="sxs-lookup"><span data-stu-id="06dba-245">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="06dba-246">您可以為專案指派多個角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-246">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="06dba-247">為了避免混淆，保留期間會自動標示這些角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-247">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="06dba-248">例如，如果專案經理需要三個軟體工程師，則會自動產生三個有**軟體工程師 1**、**軟體工程師 2** 和**軟體工程師 3** 標示的軟體工程師角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-248">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="06dba-249">如果先前已為角色設定角色特性，則會在進行資源搜尋時套用這些特性做為篩選。</span><span class="sxs-lookup"><span data-stu-id="06dba-249">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="06dba-250">您可以視需要新增其他特性，進一步縮小搜尋範圍。</span><span class="sxs-lookup"><span data-stu-id="06dba-250">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="06dba-251">您也可以自訂檢視表設定，以便更清楚地了解資源可用性。</span><span class="sxs-lookup"><span data-stu-id="06dba-251">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="06dba-252">有選項可供您選擇顯示每小時、每天、每週、每月、每季和每年可用性。</span><span class="sxs-lookup"><span data-stu-id="06dba-252">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="06dba-253">還有選項可以選擇顯示資源的可用和剩餘產能。</span><span class="sxs-lookup"><span data-stu-id="06dba-253">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="06dba-254">當您要為活動或資源可用性估計可用時間時，此選項對時間管理很有幫助。</span><span class="sxs-lookup"><span data-stu-id="06dba-254">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="06dba-255">專案經理可以在頁面上選取角色，如果有符合需求的可用資源，便可選擇保留資源以承擔該角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-255">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="06dba-256">請注意，不需要在規劃階段的這個時點保留資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-256">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="06dba-257">建立 WBS 時，您可以將角色取代為專案的人員配置資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-257">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="06dba-258">如果角色已在 WBS 中取代為人員配置資源，則資源設定會自動更新專案團隊清單及排程。</span><span class="sxs-lookup"><span data-stu-id="06dba-258">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="06dba-259">[![包含角色及實際資源的專案團隊清單](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="06dba-259">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="06dba-260">專案經理有許多可用來為專案預約資源的選項，例如**剩餘產能**、**完整產能**、**產能百分比**和**指定時數**。</span><span class="sxs-lookup"><span data-stu-id="06dba-260">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="06dba-261">如果資源指派變更，就可以隨時取消這些預約選項。</span><span class="sxs-lookup"><span data-stu-id="06dba-261">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="06dba-262">支援兩種類型的預約：</span><span class="sxs-lookup"><span data-stu-id="06dba-262">Two types of booking are supported:</span></span>

- <span data-ttu-id="06dba-263">**已確認預約** – 已核准並確認要在指定期間處理業務開發的資源保留。</span><span class="sxs-lookup"><span data-stu-id="06dba-263">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="06dba-264">**未確認預約** – 已暫時設定要在指定期間處理業務開發的資源保留。</span><span class="sxs-lookup"><span data-stu-id="06dba-264">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="06dba-265">下列程序說明如何建立專案團隊：</span><span class="sxs-lookup"><span data-stu-id="06dba-265">The following procedure explains how to create a project team.</span></span>

### <a name="create-a-project-team"></a><span data-ttu-id="06dba-266">建立專案團隊</span><span class="sxs-lookup"><span data-stu-id="06dba-266">Create a project team</span></span>

1. <span data-ttu-id="06dba-267">在**所有專案**清單頁面上，選取專案，然後選取**編輯**。</span><span class="sxs-lookup"><span data-stu-id="06dba-267">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="06dba-268">在**專案團隊與排程**索引標籤的**排程結束日期**欄位中，輸入排程開始日期加上一個月。</span><span class="sxs-lookup"><span data-stu-id="06dba-268">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="06dba-269">例如，如果排程開始日期是 2017 年 6 月 24 日 (2017/24/06)，請輸入 **2017/24/07**。</span><span class="sxs-lookup"><span data-stu-id="06dba-269">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="06dba-270">選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="06dba-270">Select **Add**.</span></span>
4. <span data-ttu-id="06dba-271">在**將角色新增至專案**窗格的**角色**欄位中，選取**資深專案經理**。</span><span class="sxs-lookup"><span data-stu-id="06dba-271">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="06dba-272">選取**需要的專長**。</span><span class="sxs-lookup"><span data-stu-id="06dba-272">Select **Required competencies**.</span></span>
6. <span data-ttu-id="06dba-273">在**選擇特性**頁面上，預設會選取您先前為資深專案經理角色設定的特性。</span><span class="sxs-lookup"><span data-stu-id="06dba-273">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="06dba-274">選取**確定**。</span><span class="sxs-lookup"><span data-stu-id="06dba-274">Select **OK**.</span></span>
7. <span data-ttu-id="06dba-275">在**將角色新增至專案**頁面的**資源數目**欄位中，輸入 **1**。</span><span class="sxs-lookup"><span data-stu-id="06dba-275">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="06dba-276">在**資源**欄位中，查詢會顯示所有具有所需專長的資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-276">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="06dba-277">選取 **Daniel Goldschmidt**，然後選取**建立**。</span><span class="sxs-lookup"><span data-stu-id="06dba-277">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="06dba-278">在**專案**頁面上，選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="06dba-278">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="06dba-279">在**將角色新增至專案**窗格的**角色**欄位中，選取**團隊成員**。</span><span class="sxs-lookup"><span data-stu-id="06dba-279">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="06dba-280">在**資源數目**欄位中，輸入 **5**。</span><span class="sxs-lookup"><span data-stu-id="06dba-280">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="06dba-281">選取**建立**。</span><span class="sxs-lookup"><span data-stu-id="06dba-281">Select **Create**.</span></span>
12. <span data-ttu-id="06dba-282">在**專案**頁面上，選取**履行資源**。</span><span class="sxs-lookup"><span data-stu-id="06dba-282">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="resource-capacity-synchronization"></a><span data-ttu-id="06dba-283">資源產能同步處理</span><span class="sxs-lookup"><span data-stu-id="06dba-283">Resource capacity synchronization</span></span>
<span data-ttu-id="06dba-284">資源同步處理的程序有助於保證行事曆及基準行事曆的資訊會逐漸滲入專案資源排程中。</span><span class="sxs-lookup"><span data-stu-id="06dba-284">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="06dba-285">如果行事曆已變更，此程序就會對專案資源排程進行必要的更新。</span><span class="sxs-lookup"><span data-stu-id="06dba-285">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="06dba-286">此程式也有助於改善效能，因為會提前同步處理行事曆的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="06dba-286">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="06dba-287">因此會加快進行對資源排程資訊的更新。</span><span class="sxs-lookup"><span data-stu-id="06dba-287">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="06dba-288">建議您以批次方式排定這些程序，而不是逐次排定。</span><span class="sxs-lookup"><span data-stu-id="06dba-288">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="06dba-289">否則，會有人忘記上次同步處理資訊時包含的日期。</span><span class="sxs-lookup"><span data-stu-id="06dba-289">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="06dba-290">如果沒有使用包含的日期，就會在進行日期同步處理時出現期間缺口。</span><span class="sxs-lookup"><span data-stu-id="06dba-290">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![行事曆同步處理](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="06dba-292">同步處理資源產能彙總</span><span class="sxs-lookup"><span data-stu-id="06dba-292">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="06dba-293">同步處理程序是專為同步處理所有資源行事曆資訊而設計。</span><span class="sxs-lookup"><span data-stu-id="06dba-293">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="06dba-294">此資訊包含有關任何對專案資源行事曆產能資料表所做變更的基準行事曆資訊。</span><span class="sxs-lookup"><span data-stu-id="06dba-294">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="06dba-295">如果專案中新增了新資源，同步處理有助於保證有更新過的行事曆資訊可供使用。</span><span class="sxs-lookup"><span data-stu-id="06dba-295">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="06dba-296">此同步處理作業隨時都可以進行。</span><span class="sxs-lookup"><span data-stu-id="06dba-296">This synchronization can be done at any time.</span></span>

<span data-ttu-id="06dba-297">建議您使用批次。</span><span class="sxs-lookup"><span data-stu-id="06dba-297">We recommend that you use a batch.</span></span> <span data-ttu-id="06dba-298">有選項可在產能保留同步處理期間使用。</span><span class="sxs-lookup"><span data-stu-id="06dba-298">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="06dba-299">選取**專案管理與會計** &gt; **定期** &gt; **產能同步處理** &gt; **同步處理資源產能彙總**。</span><span class="sxs-lookup"><span data-stu-id="06dba-299">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="06dba-300">設定下表中的選項。</span><span class="sxs-lookup"><span data-stu-id="06dba-300">Set the options in the following table.</span></span>

    | <span data-ttu-id="06dba-301">選項</span><span class="sxs-lookup"><span data-stu-id="06dba-301">Option</span></span>      | <span data-ttu-id="06dba-302">描述</span><span class="sxs-lookup"><span data-stu-id="06dba-302">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="06dba-303">期間代碼</span><span class="sxs-lookup"><span data-stu-id="06dba-303">Period code</span></span> | <span data-ttu-id="06dba-304">選擇性選取總帳日期間隔代碼，以設定資源產能彙總同步處理程序的開始和結束日期。</span><span class="sxs-lookup"><span data-stu-id="06dba-304">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="06dba-305">開始日期</span><span class="sxs-lookup"><span data-stu-id="06dba-305">Start date</span></span>  | <span data-ttu-id="06dba-306">輸入資源產能彙總同步處理程序的開始日期。</span><span class="sxs-lookup"><span data-stu-id="06dba-306">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="06dba-307">結束日期</span><span class="sxs-lookup"><span data-stu-id="06dba-307">End date</span></span>    | <span data-ttu-id="06dba-308">輸入資源產能彙總同步處理程序的結束日期。</span><span class="sxs-lookup"><span data-stu-id="06dba-308">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="06dba-309">[![同步處理程序](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="06dba-309">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>

## <a name="set-up-roles-on-wbs-templates"></a><span data-ttu-id="06dba-310">在 WBS 範本上設定角色</span><span class="sxs-lookup"><span data-stu-id="06dba-310">Set up roles on WBS templates</span></span>
<span data-ttu-id="06dba-311">專案經理可以設定可在他們為新專案建立 WBS 時套用的 WBS 範本。</span><span class="sxs-lookup"><span data-stu-id="06dba-311">Project managers can set up WBS templates that they can apply when they create a WBS for new projects.</span></span> <span data-ttu-id="06dba-312">專案經理可以在建立範本時新增角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-312">Project managers can add roles when they create a template.</span></span> <span data-ttu-id="06dba-313">使用下列程序，將角色指派至 WBS 範本。</span><span class="sxs-lookup"><span data-stu-id="06dba-313">Use the following procedure to assign a role to a WBS template.</span></span>

1. <span data-ttu-id="06dba-314">選取**專案管理與會計** &gt; **設定** &gt; **專案** &gt; **分工結構圖範本**。</span><span class="sxs-lookup"><span data-stu-id="06dba-314">Select **Project management and accounting** &gt; **Setup** &gt; **Projects** &gt; **Work breakdown structure templates**.</span></span>
2. <span data-ttu-id="06dba-315">選取所選 WBS 範本的**詳細資料**。</span><span class="sxs-lookup"><span data-stu-id="06dba-315">Select **Details** for a selected WBS template.</span></span>
3. <span data-ttu-id="06dba-316">選取清單中的工作，然後在**角色**欄位中，選取要指派給工作的角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-316">Select a task in the list, and then, in the **Role** field, select a role to assign to the task.</span></span>

### <a name="work-with-a-wbs"></a><span data-ttu-id="06dba-317">使用 WBS</span><span class="sxs-lookup"><span data-stu-id="06dba-317">Work with a WBS</span></span>

<span data-ttu-id="06dba-318">您可以建立新的 WBS，也可以從現有 WBS 範本複製 WBS。</span><span class="sxs-lookup"><span data-stu-id="06dba-318">You can create a new WBS, or you can copy a WBS from an existing WBS template.</span></span> <span data-ttu-id="06dba-319">專案經理可以將角色指派至 WBS 中的新工作，輕鬆地管理資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-319">A project manager can easily manage the resources by assigning roles to new tasks on the WBS.</span></span> <span data-ttu-id="06dba-320">取得資源後，或找出可用於工作的已確認資源後，您可以取代角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-320">Roles can be replaced either after a resource is acquired or after a confirmed resource to work on the task is identified.</span></span> <span data-ttu-id="06dba-321">這項彈性讓專案經理可以執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="06dba-321">This flexibility lets project managers perform the following tasks:</span></span>

- <span data-ttu-id="06dba-322">確定 WBS 工作封裝所需的資源數目。</span><span class="sxs-lookup"><span data-stu-id="06dba-322">Identify the number of resources that are required for WBS work packages.</span></span>
- <span data-ttu-id="06dba-323">估計專案成本。</span><span class="sxs-lookup"><span data-stu-id="06dba-323">Estimate project costs.</span></span>
- <span data-ttu-id="06dba-324">決定初步預算。</span><span class="sxs-lookup"><span data-stu-id="06dba-324">Determine a preliminary budget.</span></span>
- <span data-ttu-id="06dba-325">根據角色和資源估計活動期間。</span><span class="sxs-lookup"><span data-stu-id="06dba-325">Estimate activity duration, based on roles and resources.</span></span>
- <span data-ttu-id="06dba-326">根據可用的專案資訊，擬定一些專案管理計劃。</span><span class="sxs-lookup"><span data-stu-id="06dba-326">Develop some project management plans, based on the available project information.</span></span>

<span data-ttu-id="06dba-327">WBS 新增了其他選項，以便善加運用功能。</span><span class="sxs-lookup"><span data-stu-id="06dba-327">Additional options have been added in the WBS to better use the resourcing functionality.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06dba-328">選項</span><span class="sxs-lookup"><span data-stu-id="06dba-328">Option</span></span></th>
<th><span data-ttu-id="06dba-329">描述</span><span class="sxs-lookup"><span data-stu-id="06dba-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06dba-330">資源指派</span><span class="sxs-lookup"><span data-stu-id="06dba-330">Resource assignments</span></span></td>
<td><span data-ttu-id="06dba-331">在 WBS 中檢視工作的已指派資源、日期、工作時數和預約類型。</span><span class="sxs-lookup"><span data-stu-id="06dba-331">View the assigned resources, dates, number of hours, and booking type for tasks on the WBS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06dba-332">自動產生團隊</span><span class="sxs-lookup"><span data-stu-id="06dba-332">Auto generate team</span></span></td>
<td><span data-ttu-id="06dba-333">使用與工作相關聯的角色，自動新增規劃的資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-333">Automatically add planned resources by using roles that are associated with a task.</span></span> <span data-ttu-id="06dba-334">Finance 會使用根據角色的多重準則決策分析，自動建議規劃的資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-334">Finance automatically suggests planned resources by using multi-criteria decision analysis that is based on roles.</span></span> <span data-ttu-id="06dba-335">為 WBS 中的工作設定角色和投入量 (小時) 之後，並在結構已發行之後，選取<strong>自動產生團隊</strong>。</span><span class="sxs-lookup"><span data-stu-id="06dba-335">After the roles and effort (hours) have been set for the tasks in a WBS, and after the structure has been released, select <strong>Auto generate team</strong>.</span></span> <span data-ttu-id="06dba-336">所需數目的已規劃資源會新增至 WBS 和<strong>專案與團隊排程</strong>索引標籤 。</span><span class="sxs-lookup"><span data-stu-id="06dba-336">The required number of planned resources is added to the WBS and the <strong>Project and team scheduling</strong> tab.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06dba-337">資源 (下拉式清單)</span><span class="sxs-lookup"><span data-stu-id="06dba-337">Resource (drop-down list)</span></span></td>
<td><span data-ttu-id="06dba-338">在<strong>啟動資源指派</strong>頁面上，您可以根據指定的期間，選取要進行最確認預約或未確認預約的資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-338">On the <strong>Launch resource assignment</strong> page, you can select resources to hard-book or soft-book, based on the specified duration.</span></span> <span data-ttu-id="06dba-339">您可以調整檢視設定，以查看並設定資源活動的期間。</span><span class="sxs-lookup"><span data-stu-id="06dba-339">You can adjust the view settings to see and set the duration of resource activities.</span></span> <span data-ttu-id="06dba-340">您可以使用下列選項，在工作封裝層級選取並指派資源：</span><span class="sxs-lookup"><span data-stu-id="06dba-340">You can select and assign resources at the work package level by using the following options:</span></span>
<ul>
<li><span data-ttu-id="06dba-341"><strong>接受</strong> – 確認對指派至工作的資源所做的變更。</span><span class="sxs-lookup"><span data-stu-id="06dba-341"><strong>Accept</strong> – Confirm changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="06dba-342"><strong>取消</strong> – 取消對指派至工作的資源所做的變更。</span><span class="sxs-lookup"><span data-stu-id="06dba-342"><strong>Cancel</strong> – Cancel changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="06dba-343"><strong>自動指派</strong> – 自動選取找到適配角色的可用人員配置資源，並將其指派至所選取的工作。</span><span class="sxs-lookup"><span data-stu-id="06dba-343"><strong>Assign automatically</strong> – An available staffed resource that has a matching role is automatically selected and assigned to the selected task.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

1. <span data-ttu-id="06dba-344">在**所有專案**頁面上，選取 **XYZ 升級階段 2** 專案。</span><span class="sxs-lookup"><span data-stu-id="06dba-344">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="06dba-345">選取**計劃** &gt; **活動** &gt; **分工結構圖**。</span><span class="sxs-lookup"><span data-stu-id="06dba-345">Select **Plan** &gt; **Activities** &gt; **Work breakdown structure**.</span></span>
3. <span data-ttu-id="06dba-346">選取**新增**以已下列等級一的活動新增至 WBS：</span><span class="sxs-lookup"><span data-stu-id="06dba-346">Select **New** to add the following level-one activities to the WBS:</span></span>

    - <span data-ttu-id="06dba-347">起始</span><span class="sxs-lookup"><span data-stu-id="06dba-347">Initiating</span></span>
    - <span data-ttu-id="06dba-348">規劃</span><span class="sxs-lookup"><span data-stu-id="06dba-348">Planning</span></span>
    - <span data-ttu-id="06dba-349">正在執行</span><span class="sxs-lookup"><span data-stu-id="06dba-349">Executing</span></span>
    - <span data-ttu-id="06dba-350">監視與控制</span><span class="sxs-lookup"><span data-stu-id="06dba-350">Monitoring and Control</span></span>
    - <span data-ttu-id="06dba-351">關閉​​</span><span class="sxs-lookup"><span data-stu-id="06dba-351">Close</span></span>

4. <span data-ttu-id="06dba-352">設定日期和投入量 (小時)，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="06dba-352">Set the dates and effort (hours), as shown in the following illustration.</span></span>

    <span data-ttu-id="06dba-353">[![設定日期和投入量](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span><span class="sxs-lookup"><span data-stu-id="06dba-353">[![Setting the dates and effort](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span></span>

5. <span data-ttu-id="06dba-354">選取**起始**工作列，然後在**角色**欄位中選取**資深專案經理**。</span><span class="sxs-lookup"><span data-stu-id="06dba-354">Select the **Initiating** task line, and then, in the **Role** field, select **Senior Project Manager**.</span></span>
6. <span data-ttu-id="06dba-355">選取**發行**。</span><span class="sxs-lookup"><span data-stu-id="06dba-355">Select **Publish**.</span></span>
7. <span data-ttu-id="06dba-356">在同一列的**資源**欄位中，選取 **Daniel Goldschmidt**，然後選取**接受**。</span><span class="sxs-lookup"><span data-stu-id="06dba-356">On the same line, in the **Resource** field, select **Daniel Goldschmidt**, and then select **Accept**.</span></span>
8. <span data-ttu-id="06dba-357">選取**規劃**工作列，然後在**角色**欄位中選取**商務分析師**。</span><span class="sxs-lookup"><span data-stu-id="06dba-357">Select the **Planning** task line, and then, in the **Role** field, select **Business analyst**.</span></span>
9. <span data-ttu-id="06dba-358">選取**發佈**，然後選取**自動產生團隊**。</span><span class="sxs-lookup"><span data-stu-id="06dba-358">Select **Publish**, and then select **Auto generate team**.</span></span>
10. <span data-ttu-id="06dba-359">在出現的訊息方塊中，選取**是**。</span><span class="sxs-lookup"><span data-stu-id="06dba-359">In the message box that appears, select **Yes**.</span></span>
11. <span data-ttu-id="06dba-360">在**資源**欄位中，確認值是否為**商務分析師 1**。</span><span class="sxs-lookup"><span data-stu-id="06dba-360">In the **Resource** field, verify that the value is **Business analyst 1**.</span></span>
12. <span data-ttu-id="06dba-361">對於**商務分析師 1** 資源，開啟其查詢，然後選取**啟動資源指派**。</span><span class="sxs-lookup"><span data-stu-id="06dba-361">For the **Business analyst 1** resource, open the lookup, and select **Launch resource assignments**.</span></span> <span data-ttu-id="06dba-362">然後選取工作的工作者。</span><span class="sxs-lookup"><span data-stu-id="06dba-362">Then select a worker for the task.</span></span>
13. <span data-ttu-id="06dba-363">選取**未確認指派** &gt; **完整產能**。</span><span class="sxs-lookup"><span data-stu-id="06dba-363">Select **Soft assign** &gt; **Full capacity**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="06dba-364">您不會收到指出指定的資源目前為 2 的警告，因為資源數目仍保持為 1。</span><span class="sxs-lookup"><span data-stu-id="06dba-364">You don't receive a warning that the specified resource is now 2, because the number of resources remains 1.</span></span>

14. <span data-ttu-id="06dba-365">在**分工結構圖**頁面上，驗證 WBS 中的資源指派，然後選取**儲存**。</span><span class="sxs-lookup"><span data-stu-id="06dba-365">On the **Work breakdown structure** page, validate the resource assignment on the WBS, and then select **Save**.</span></span>

## <a name="resource-fulfillment-for-planned-resources"></a><span data-ttu-id="06dba-366">規劃資源的資源履行</span><span class="sxs-lookup"><span data-stu-id="06dba-366">Resource fulfillment for planned resources</span></span>
<span data-ttu-id="06dba-367">專案經理可以規劃專案所需的資源角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-367">A project manager can plan required resource roles for a project.</span></span> <span data-ttu-id="06dba-368">資源管理員會將這些規劃的資源視為**資源履行**頁面上的要求，並且可以指派實際資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-368">The resource manager will see these planned resources as requests on the **Resource fulfillment** page and can assign actual resources.</span></span>

1. <span data-ttu-id="06dba-369">在**所有專案**頁面上，選取 **XYZ 升級階段 2** 專案。</span><span class="sxs-lookup"><span data-stu-id="06dba-369">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="06dba-370">選取**專案**，然後選取**編輯**。</span><span class="sxs-lookup"><span data-stu-id="06dba-370">Select **Project**, and then select **Edit**.</span></span>
3. <span data-ttu-id="06dba-371">在**專案團隊與排程**索引標籤上，選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="06dba-371">On the **Project team and scheduling** tab, select **Add**.</span></span>
4. <span data-ttu-id="06dba-372">在**新增角色**對話方塊中，選取**軟體開發人員**角色。</span><span class="sxs-lookup"><span data-stu-id="06dba-372">In the **Add roles** dialog box, select the **Software developer** role.</span></span>
5. <span data-ttu-id="06dba-373">選取**建立**，然後關閉專案頁面。</span><span class="sxs-lookup"><span data-stu-id="06dba-373">Select **Create**, and then close the project page.</span></span>
6. <span data-ttu-id="06dba-374">在**資源履行**頁面上，為 **XYZ 升級專案階段 2** 專案選取**軟體開發人員 1**。</span><span class="sxs-lookup"><span data-stu-id="06dba-374">On the **Resource fulfillment** page, select **Software developer 1** for the **XYZ Upgrade project Phase 2** project.</span></span>
7. <span data-ttu-id="06dba-375">選取工作者，然後選取**指派**。</span><span class="sxs-lookup"><span data-stu-id="06dba-375">Select a worker, and then select **Assign**.</span></span>
8. <span data-ttu-id="06dba-376">確認是否已移除 **XYZ 升級專案階段 2** 專案的**軟體開發人員 1** 這一列。</span><span class="sxs-lookup"><span data-stu-id="06dba-376">Verify that the line for **Software developer 1** has been removed for the **XYZ Upgrade project Phase 2** project.</span></span>
9. <span data-ttu-id="06dba-377">在**專案團隊與排程**索引標籤上，針對 **XYZ 升級階段 2** 專案，確認您在先前步驟所選取的工作者是否已新增為**軟體開發人員**。</span><span class="sxs-lookup"><span data-stu-id="06dba-377">On the **Project team and scheduling** tab, for the **XYZ Upgrade Phase 2** project, verify that the worker that you selected in the previous step has been added as **Software developer**.</span></span>

## <a name="requests-for-project-resources"></a><span data-ttu-id="06dba-378">對專案資源的要求</span><span class="sxs-lookup"><span data-stu-id="06dba-378">Requests for project resources</span></span>
<span data-ttu-id="06dba-379">專案資源排程的功能只能讓資源管理員在業務開發或專案上發佈人員配置資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-379">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="06dba-380">若要啟用此功能，請完成下列工作，或確認這些工作是否已完成：</span><span class="sxs-lookup"><span data-stu-id="06dba-380">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="06dba-381">設定編號序列。</span><span class="sxs-lookup"><span data-stu-id="06dba-381">Set up number sequences.</span></span>
- <span data-ttu-id="06dba-382">設定專案管理與會計工作流程。</span><span class="sxs-lookup"><span data-stu-id="06dba-382">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="06dba-383">啟用資源要求工作流程。</span><span class="sxs-lookup"><span data-stu-id="06dba-383">Enable resource request workflows.</span></span>

<span data-ttu-id="06dba-384">完成上述工作之後，您可以視需要完成下列工作：</span><span class="sxs-lookup"><span data-stu-id="06dba-384">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="06dba-385">從未確認預約的人員配置資源建立資源要求。</span><span class="sxs-lookup"><span data-stu-id="06dba-385">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="06dba-386">監視資源要求。</span><span class="sxs-lookup"><span data-stu-id="06dba-386">Monitor resource requests.</span></span>
- <span data-ttu-id="06dba-387">履行資源要求。</span><span class="sxs-lookup"><span data-stu-id="06dba-387">Fulfill resource requests.</span></span>
- <span data-ttu-id="06dba-388">從 WBS 要求人員配置資源。</span><span class="sxs-lookup"><span data-stu-id="06dba-388">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="06dba-389">在沒有要求人員配置資源的情況下，將資源預約給專案。</span><span class="sxs-lookup"><span data-stu-id="06dba-389">Book resources to a project without having a request for a staffed resource.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="06dba-390">監視專案團隊</span><span class="sxs-lookup"><span data-stu-id="06dba-390">Monitor project teams</span></span>
1. <span data-ttu-id="06dba-391">在**所有專案**頁面上，選取 **XYZ 升級階段 2** 專案的**專案識別碼**連結。</span><span class="sxs-lookup"><span data-stu-id="06dba-391">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="06dba-392">在**專案團隊與排程**快速分頁上，確認列出的專案資源是否正確。</span><span class="sxs-lookup"><span data-stu-id="06dba-392">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
