---
title: 建立新專案
description: 本主題提供有關如何建立新專案的資訊。
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006231"
---
# <a name="create-a-new-project"></a><span data-ttu-id="afa99-103">建立新專案</span><span class="sxs-lookup"><span data-stu-id="afa99-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afa99-104">完成下列步驟以建立新的專案。</span><span class="sxs-lookup"><span data-stu-id="afa99-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="afa99-105">在 **專案管理** 頁面上，選取 **新增專案**，並輸入下列值：</span><span class="sxs-lookup"><span data-stu-id="afa99-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="afa99-106">**專案類型：** 時間和材料</span><span class="sxs-lookup"><span data-stu-id="afa99-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="afa99-107">**專案名稱：** XYZ 升級階段 2</span><span class="sxs-lookup"><span data-stu-id="afa99-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="afa99-108">**專案群組：** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="afa99-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="afa99-109">**專案合約識別碼：** 00000002</span><span class="sxs-lookup"><span data-stu-id="afa99-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="afa99-110">選取 **建立專案**。</span><span class="sxs-lookup"><span data-stu-id="afa99-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="afa99-111">將資源指派至專案</span><span class="sxs-lookup"><span data-stu-id="afa99-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="afa99-112">在 **工作者** 頁面的 **工作者** 清單中，選取先前已設定專長之工作者的記錄，然後開啟工作者記錄。</span><span class="sxs-lookup"><span data-stu-id="afa99-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="afa99-113">在動作窗格的 **專案** 索引標籤上，選取 **設定** 群組中的 **指派專案**。</span><span class="sxs-lookup"><span data-stu-id="afa99-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="afa99-114">在 **資源驗證專案指派** 頁面的 **專案** 索引標籤上，篩選 **將專案新增至選取的專案** 欄位中的 **XYZ 升級階段 2** 專案。</span><span class="sxs-lookup"><span data-stu-id="afa99-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="afa99-115">在 **剩餘專案** 窗格中，選取專案並選取箭頭按鈕，將該專案新增至 **選取的專案** 窗格。</span><span class="sxs-lookup"><span data-stu-id="afa99-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="afa99-116">您也可以視需要指派資源的類別。</span><span class="sxs-lookup"><span data-stu-id="afa99-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="afa99-117">類別類型會是 **成本** 或 **營收**。</span><span class="sxs-lookup"><span data-stu-id="afa99-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="afa99-118">類別類型是由您的組織所決定。</span><span class="sxs-lookup"><span data-stu-id="afa99-118">The category type is determined by your organization.</span></span> <span data-ttu-id="afa99-119">如果未指派資源的類別，Finance 會針對成本與營收查詢工時價格的預設類別。</span><span class="sxs-lookup"><span data-stu-id="afa99-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="afa99-120">設定專案資源和角色特性</span><span class="sxs-lookup"><span data-stu-id="afa99-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="afa99-121">專案經理可以使用專案資源分配功能來建立專案所需的角色。</span><span class="sxs-lookup"><span data-stu-id="afa99-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="afa99-122">如果已確認的資源在保留資源時仍然未知，則可以使用角色。</span><span class="sxs-lookup"><span data-stu-id="afa99-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="afa99-123">角色可以暫時保留為規劃的資源，讓您可以繼續專案規劃階段。</span><span class="sxs-lookup"><span data-stu-id="afa99-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="afa99-124">[![角色的範例](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="afa99-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="afa99-125">**案例：** 已雇用 Contoso 來完成專案章程已獲核准的時間和材料專案。</span><span class="sxs-lookup"><span data-stu-id="afa99-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="afa99-126">專案襄理仍在完成專案的範圍。</span><span class="sxs-lookup"><span data-stu-id="afa99-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="afa99-127">資源管理員目前正在識別要保留來處理新專案的特定資源。</span><span class="sxs-lookup"><span data-stu-id="afa99-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="afa99-128">由於專案的性質至關重要，專案贊助者要求資深專案經理成為其中一個角色。</span><span class="sxs-lookup"><span data-stu-id="afa99-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="afa99-129">專案襄理在專案規劃期間說不定需要資源資訊，資源管理員必須取得新資源，並定義系統中的角色。</span><span class="sxs-lookup"><span data-stu-id="afa99-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="afa99-130">下列步驟顯示資源管理員如何設定資深專案經理角色，並建立資源特性與該角色的關聯。</span><span class="sxs-lookup"><span data-stu-id="afa99-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="afa99-131">此角色隨後即可用於搜尋符合所需資源專長的可用資源。</span><span class="sxs-lookup"><span data-stu-id="afa99-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="afa99-132">在 **設定角色** 頁面上，選取 **新增**，並輸入下列值：</span><span class="sxs-lookup"><span data-stu-id="afa99-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="afa99-133">**角色識別碼：** 資深專案經理</span><span class="sxs-lookup"><span data-stu-id="afa99-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="afa99-134">**描述：** 資深專案經理</span><span class="sxs-lookup"><span data-stu-id="afa99-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="afa99-135">選取 **建立**。</span><span class="sxs-lookup"><span data-stu-id="afa99-135">Select **Create**.</span></span>
3. <span data-ttu-id="afa99-136">選取 **資深專案經理** 角色，然後選取 **設定特性**。</span><span class="sxs-lookup"><span data-stu-id="afa99-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="afa99-137">在 **特性類型** 欄位中，選取 **技能**。</span><span class="sxs-lookup"><span data-stu-id="afa99-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="afa99-138">在 **可用特性** 欄位中，輸入要搜尋的技能。</span><span class="sxs-lookup"><span data-stu-id="afa99-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="afa99-139">在 **特性類型** 欄位中，選取 **認證**。</span><span class="sxs-lookup"><span data-stu-id="afa99-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="afa99-140">在 **可用特性** 欄位中，輸入要搜尋的認證類型。</span><span class="sxs-lookup"><span data-stu-id="afa99-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="afa99-141">將專案資源指派至專案</span><span class="sxs-lookup"><span data-stu-id="afa99-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="afa99-142">在 **所有專案** 頁面上，選取 **XYZ 升級階段 2** 專案。</span><span class="sxs-lookup"><span data-stu-id="afa99-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="afa99-143">在 **專案團隊與排程** 索引標籤上，選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="afa99-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="afa99-144">在 **角色** 欄位中，選取 **團隊成員**。</span><span class="sxs-lookup"><span data-stu-id="afa99-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="afa99-145">選取 **從行事曆預約**。</span><span class="sxs-lookup"><span data-stu-id="afa99-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="afa99-146">在 **資源可用性** 頁面上，選取 **檢視設定**。</span><span class="sxs-lookup"><span data-stu-id="afa99-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="afa99-147">在 **調整檢視設定** 頁面上，輸入下列值：</span><span class="sxs-lookup"><span data-stu-id="afa99-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="afa99-148">**日期範圍檢視格式：** 日</span><span class="sxs-lookup"><span data-stu-id="afa99-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="afa99-149">**顯示可用性描述：** 是</span><span class="sxs-lookup"><span data-stu-id="afa99-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="afa99-150">**顯示剩餘產能：** 是</span><span class="sxs-lookup"><span data-stu-id="afa99-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="afa99-151">在資源清單中選取資源。</span><span class="sxs-lookup"><span data-stu-id="afa99-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="afa99-152">選取 **已確認預約** 和 **完整產能**。</span><span class="sxs-lookup"><span data-stu-id="afa99-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="afa99-153">將資源指派給預設角色</span><span class="sxs-lookup"><span data-stu-id="afa99-153">Assign a resource to a default role</span></span>

<span data-ttu-id="afa99-154">為了協助專案經理或資源管理員，您可以進一步向下切入可為專案保留的資源。</span><span class="sxs-lookup"><span data-stu-id="afa99-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="afa99-155">您可以將預設角色與現有資源或新取得資源建立關聯。</span><span class="sxs-lookup"><span data-stu-id="afa99-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="afa99-156">例如，雇用 Daniel 時，他具備承擔商務分析員角色的經驗和技能。</span><span class="sxs-lookup"><span data-stu-id="afa99-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="afa99-157">資源管理員已將此角色指派為 Daniel 的預設角色。</span><span class="sxs-lookup"><span data-stu-id="afa99-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="afa99-158">因此，資源管理員已將 Daniel 加入適用於處理專案的業務分析師備選名單中。</span><span class="sxs-lookup"><span data-stu-id="afa99-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="afa99-159">進行資源保留時，專案經理可以篩選適用於處理專案的角色資源。</span><span class="sxs-lookup"><span data-stu-id="afa99-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="afa99-160">在資源履行期間執行多重準則決策分析時，他們可以使用此資訊做為一項準則。</span><span class="sxs-lookup"><span data-stu-id="afa99-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="afa99-161">他們也可以將其他資源特性新增至篩選，以搜尋具備指定專案所需特定技能、教育和經驗的資源。</span><span class="sxs-lookup"><span data-stu-id="afa99-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="afa99-162">**案例：** 獲核准的專案已開始進展，而資深專案經理角色已專案規劃階段中保留為規劃的資源。</span><span class="sxs-lookup"><span data-stu-id="afa99-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="afa99-163">資源經理現在已取得資源來履行資深專案經理角色的職責。</span><span class="sxs-lookup"><span data-stu-id="afa99-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="afa99-164">在 **資源清單** 頁面中，選取 **Daniel Goldschmidt**。</span><span class="sxs-lookup"><span data-stu-id="afa99-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="afa99-165">在 **資源角色** 頁面上，選取 **新增**，並輸入下列值：</span><span class="sxs-lookup"><span data-stu-id="afa99-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="afa99-166">**生效日：** 輸入目前的日期。</span><span class="sxs-lookup"><span data-stu-id="afa99-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="afa99-167">**到期日：** 輸入 **永不**。</span><span class="sxs-lookup"><span data-stu-id="afa99-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="afa99-168">**角色：** 輸入 **資深專案經理**。</span><span class="sxs-lookup"><span data-stu-id="afa99-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="afa99-169">選取 **儲存**，然後關閉頁面。</span><span class="sxs-lookup"><span data-stu-id="afa99-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="afa99-170">在 **專長** 索引標籤中，新增 **ProjectMgmt** 技能和 **PMP** 認證。</span><span class="sxs-lookup"><span data-stu-id="afa99-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]