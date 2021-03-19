---
title: 建立專案團隊
description: 本主題提供有關如何建立和管理專案團隊的資訊。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270848"
---
# <a name="create-a-project-team"></a><span data-ttu-id="5842a-103">建立專案團隊</span><span class="sxs-lookup"><span data-stu-id="5842a-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5842a-104">若要使用先前已在專案中設定的角色，專案經理必須將角色與專案建立關聯。</span><span class="sxs-lookup"><span data-stu-id="5842a-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="5842a-105">您可以為專案指派多個角色。</span><span class="sxs-lookup"><span data-stu-id="5842a-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="5842a-106">為了避免混淆，保留期間會自動標示這些角色。</span><span class="sxs-lookup"><span data-stu-id="5842a-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="5842a-107">例如，如果專案經理需要三個軟體工程師，則會自動產生三個有 **軟體工程師 1**、**軟體工程師 2** 和 **軟體工程師 3** 標示的軟體工程師角色。</span><span class="sxs-lookup"><span data-stu-id="5842a-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="5842a-108">如果先前已為角色設定角色特性，則會在進行資源搜尋時套用這些特性做為篩選。</span><span class="sxs-lookup"><span data-stu-id="5842a-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="5842a-109">您可以視需要新增其他特性，進一步縮小搜尋範圍。</span><span class="sxs-lookup"><span data-stu-id="5842a-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="5842a-110">您也可以自訂檢視表設定，以便更清楚地了解資源可用性。</span><span class="sxs-lookup"><span data-stu-id="5842a-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="5842a-111">有選項可供您選擇顯示每小時、每天、每週、每月、每季和每年可用性。</span><span class="sxs-lookup"><span data-stu-id="5842a-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="5842a-112">還有選項可以選擇顯示資源的可用和剩餘產能。</span><span class="sxs-lookup"><span data-stu-id="5842a-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="5842a-113">當您要為活動或資源可用性估計可用時間時，此選項對時間管理很有幫助。</span><span class="sxs-lookup"><span data-stu-id="5842a-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="5842a-114">專案經理可以在頁面上選取角色，如果有符合需求的可用資源，便可選擇保留資源以承擔該角色。</span><span class="sxs-lookup"><span data-stu-id="5842a-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="5842a-115">請注意，不需要在規劃階段的這個時點保留資源。</span><span class="sxs-lookup"><span data-stu-id="5842a-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="5842a-116">建立 WBS 時，您可以將角色取代為專案的人員配置資源。</span><span class="sxs-lookup"><span data-stu-id="5842a-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="5842a-117">如果角色已在 WBS 中取代為人員配置資源，則資源設定會自動更新專案團隊清單及排程。</span><span class="sxs-lookup"><span data-stu-id="5842a-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="5842a-118">[![包含角色及實際資源的專案團隊清單](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="5842a-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="5842a-119">專案經理有許多可用來為專案預約資源的選項，例如 **剩餘產能**、**完整產能**、**產能百分比** 和 **指定時數**。</span><span class="sxs-lookup"><span data-stu-id="5842a-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="5842a-120">如果資源指派變更，就可以隨時取消這些預約選項。</span><span class="sxs-lookup"><span data-stu-id="5842a-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="5842a-121">支援兩種類型的預約：</span><span class="sxs-lookup"><span data-stu-id="5842a-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="5842a-122">**已確認預約** – 已核准並確認要在指定期間處理業務開發的資源保留。</span><span class="sxs-lookup"><span data-stu-id="5842a-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="5842a-123">**未確認預約** – 已暫時設定要在指定期間處理業務開發的資源保留。</span><span class="sxs-lookup"><span data-stu-id="5842a-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="5842a-124">下列程序說明如何建立專案團隊：</span><span class="sxs-lookup"><span data-stu-id="5842a-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="5842a-125">建立專案團隊</span><span class="sxs-lookup"><span data-stu-id="5842a-125">Create a project team</span></span>

1. <span data-ttu-id="5842a-126">在 **所有專案** 清單頁面上，選取專案，然後選取 **編輯**。</span><span class="sxs-lookup"><span data-stu-id="5842a-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="5842a-127">在 **專案團隊與排程** 索引標籤的 **排程結束日期** 欄位中，輸入排程開始日期加上一個月。</span><span class="sxs-lookup"><span data-stu-id="5842a-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="5842a-128">例如，如果排程開始日期是 2017 年 6 月 24 日 (2017/24/06)，請輸入 **2017/24/07**。</span><span class="sxs-lookup"><span data-stu-id="5842a-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="5842a-129">選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="5842a-129">Select **Add**.</span></span>
4. <span data-ttu-id="5842a-130">在 **將角色新增至專案** 窗格的 **角色** 欄位中，選取 **資深專案經理**。</span><span class="sxs-lookup"><span data-stu-id="5842a-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="5842a-131">選取 **需要的專長**。</span><span class="sxs-lookup"><span data-stu-id="5842a-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="5842a-132">在 **選擇特性** 頁面上，預設會選取您先前為資深專案經理角色設定的特性。</span><span class="sxs-lookup"><span data-stu-id="5842a-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="5842a-133">選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="5842a-133">Select **OK**.</span></span>
7. <span data-ttu-id="5842a-134">在 **將角色新增至專案** 頁面的 **資源數目** 欄位中，輸入 **1**。</span><span class="sxs-lookup"><span data-stu-id="5842a-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="5842a-135">在 **資源** 欄位中，查詢會顯示所有具有所需專長的資源。</span><span class="sxs-lookup"><span data-stu-id="5842a-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="5842a-136">選取 **Daniel Goldschmidt**，然後選取 **建立**。</span><span class="sxs-lookup"><span data-stu-id="5842a-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="5842a-137">在 **專案** 頁面上，選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="5842a-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="5842a-138">在 **將角色新增至專案** 窗格的 **角色** 欄位中，選取 **團隊成員**。</span><span class="sxs-lookup"><span data-stu-id="5842a-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="5842a-139">在 **資源數目** 欄位中，輸入 **5**。</span><span class="sxs-lookup"><span data-stu-id="5842a-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="5842a-140">選取 **建立**。</span><span class="sxs-lookup"><span data-stu-id="5842a-140">Select **Create**.</span></span>
12. <span data-ttu-id="5842a-141">在 **專案** 頁面上，選取 **履行資源**。</span><span class="sxs-lookup"><span data-stu-id="5842a-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="5842a-142">監視專案團隊</span><span class="sxs-lookup"><span data-stu-id="5842a-142">Monitor project teams</span></span>
1. <span data-ttu-id="5842a-143">在 **所有專案** 頁面上，選取 **XYZ 升級階段 2** 專案的 **專案識別碼** 連結。</span><span class="sxs-lookup"><span data-stu-id="5842a-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="5842a-144">在 **專案團隊與排程** 快速分頁上，確認列出的專案資源是否正確。</span><span class="sxs-lookup"><span data-stu-id="5842a-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]