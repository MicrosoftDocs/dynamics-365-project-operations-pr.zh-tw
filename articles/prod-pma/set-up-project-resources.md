---
title: 設定專案資源
description: 本主題提供有關設定或要求專案資源的資訊。
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997681"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="422fd-103">設定專案資源</span><span class="sxs-lookup"><span data-stu-id="422fd-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="422fd-104">您必須設定行事曆，並將其與員工或工作者建立關聯。</span><span class="sxs-lookup"><span data-stu-id="422fd-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="422fd-105">行事曆會用來排定專案以及專案所保留資源的工作時間。</span><span class="sxs-lookup"><span data-stu-id="422fd-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="422fd-106">在行事曆設定期間，專案經理可以在資源最佳化的過程中進行資源撫平。</span><span class="sxs-lookup"><span data-stu-id="422fd-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="422fd-107">根據行事曆排程，可以對資源加以限制。</span><span class="sxs-lookup"><span data-stu-id="422fd-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="422fd-108">您可以在 **行事曆** 頁面上設定行事曆。</span><span class="sxs-lookup"><span data-stu-id="422fd-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="422fd-109">將工作者設定為專案資源時，您可以選取任職於資源需要進行設定之公司中的工作者。</span><span class="sxs-lookup"><span data-stu-id="422fd-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="422fd-110">或者，也可以從您組織中的其他公司選取工作者。</span><span class="sxs-lookup"><span data-stu-id="422fd-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="422fd-111">這些工作者稱為公司間的資源。</span><span class="sxs-lookup"><span data-stu-id="422fd-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="422fd-112">下列程序說明如何將工作者設定為公司中的專案資源，以及如何設定公司間的專案資源。</span><span class="sxs-lookup"><span data-stu-id="422fd-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="422fd-113">將工作者設定為專案資源</span><span class="sxs-lookup"><span data-stu-id="422fd-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="422fd-114">在 **工作者** 頁面的 **工作者** 清單中，選取您要新增為專案資源的工作者，然後開啟工作者記錄。</span><span class="sxs-lookup"><span data-stu-id="422fd-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="422fd-115">在動作窗格中，選取 **專案** &gt; **設定** &gt; **專案設定**。</span><span class="sxs-lookup"><span data-stu-id="422fd-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="422fd-116">選取行事曆，然後關閉頁面。</span><span class="sxs-lookup"><span data-stu-id="422fd-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="422fd-117">您也可以將資源的預設專案指定為預先指派的類型。</span><span class="sxs-lookup"><span data-stu-id="422fd-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="422fd-118">當資源管理員或專案經理預先知道資源要處理哪些專案時，可以使用預先指派。</span><span class="sxs-lookup"><span data-stu-id="422fd-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="422fd-119">也可以根據專案贊助者或客戶的要求使用預先指派。</span><span class="sxs-lookup"><span data-stu-id="422fd-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="422fd-120">若要預先指派專案，請在 **指派專案** 頁面的 **專案** 索引標籤上，從 **剩餘專案** 清單中選取適當的專案。</span><span class="sxs-lookup"><span data-stu-id="422fd-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="422fd-121">設定公司間的資源</span><span class="sxs-lookup"><span data-stu-id="422fd-121">Set up an intercompany resource</span></span>

<span data-ttu-id="422fd-122">將工作者設定為公司間的資源時，您在出借公司和借用公司中都必須完成設定。</span><span class="sxs-lookup"><span data-stu-id="422fd-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="422fd-123">在出借公司中</span><span class="sxs-lookup"><span data-stu-id="422fd-123">In the lending company</span></span>

1. <span data-ttu-id="422fd-124">在 Finance 中，確認已選取出借公司，然後完成上一節「將工作者設定為專案資源」中的程序。</span><span class="sxs-lookup"><span data-stu-id="422fd-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="422fd-125">在 **公司間會計** 頁面，選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="422fd-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="422fd-126">在 **法律實體識別碼** 欄位中，選取出借公司。</span><span class="sxs-lookup"><span data-stu-id="422fd-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="422fd-127">適當填入剩餘欄位，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="422fd-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="422fd-128">在 **轉撥價格** 頁面，選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="422fd-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="422fd-129">在 **借用法律實體** 欄位中，選取適當的公司。</span><span class="sxs-lookup"><span data-stu-id="422fd-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="422fd-130">若只要出借您在本節開始時所建立的資源給借用公司，請在 **資源** 欄位中，選取您所建立資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="422fd-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="422fd-131">若要讓出借公司的所有資源皆可供借用公司使用，請讓 **資源** 欄位保持空白。</span><span class="sxs-lookup"><span data-stu-id="422fd-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="422fd-132">在 **專案管理與會計參數** 頁面的 **公司之間** 索引標籤上，將 **啟用公司間的資源排程和時程表** 選項設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="422fd-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="422fd-133">在借用公司中</span><span class="sxs-lookup"><span data-stu-id="422fd-133">In the borrowing company</span></span>

- <span data-ttu-id="422fd-134">在 **資源清單** 頁面的搜尋篩選中，輸入出借公司所建立資源的名稱，以確認該名稱是否已包含在借用公司的資源清單中。</span><span class="sxs-lookup"><span data-stu-id="422fd-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="422fd-135">要求專案資源</span><span class="sxs-lookup"><span data-stu-id="422fd-135">Request project resources</span></span>
<span data-ttu-id="422fd-136">專案資源排程的功能只能讓資源管理員在業務開發或專案上發佈人員配置資源。</span><span class="sxs-lookup"><span data-stu-id="422fd-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="422fd-137">若要啟用此功能，請完成下列工作，或確認這些工作是否已完成：</span><span class="sxs-lookup"><span data-stu-id="422fd-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="422fd-138">設定編號序列。</span><span class="sxs-lookup"><span data-stu-id="422fd-138">Set up number sequences.</span></span>
- <span data-ttu-id="422fd-139">設定專案管理與會計工作流程。</span><span class="sxs-lookup"><span data-stu-id="422fd-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="422fd-140">啟用資源要求工作流程。</span><span class="sxs-lookup"><span data-stu-id="422fd-140">Enable resource request workflows.</span></span>

<span data-ttu-id="422fd-141">完成上述工作之後，您可以視需要完成下列工作：</span><span class="sxs-lookup"><span data-stu-id="422fd-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="422fd-142">從未確認預約的人員配置資源建立資源要求。</span><span class="sxs-lookup"><span data-stu-id="422fd-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="422fd-143">監視資源要求。</span><span class="sxs-lookup"><span data-stu-id="422fd-143">Monitor resource requests.</span></span>
- <span data-ttu-id="422fd-144">履行資源要求。</span><span class="sxs-lookup"><span data-stu-id="422fd-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="422fd-145">從 WBS 要求人員配置資源。</span><span class="sxs-lookup"><span data-stu-id="422fd-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="422fd-146">在沒有要求人員配置資源的情況下，將資源預約給專案。</span><span class="sxs-lookup"><span data-stu-id="422fd-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]