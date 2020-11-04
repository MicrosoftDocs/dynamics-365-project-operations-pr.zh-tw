---
title: 專案資源排程效能
description: 本主題提供有關如何改善大量專案資源排程效能的資訊。
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072979"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="6eb48-103">專案資源排程效能</span><span class="sxs-lookup"><span data-stu-id="6eb48-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="6eb48-104">專案數目達到數千個時，就會發生與資源排程相關的效能問題。</span><span class="sxs-lookup"><span data-stu-id="6eb48-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="6eb48-105">為了改善資源排程效能，有一項功能可讓使用者縮短啟動資源可用性表單所需的時間。</span><span class="sxs-lookup"><span data-stu-id="6eb48-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="6eb48-106">具體而言，這會移除資源產能彙總同步處理程序，而使用 **ResProjectResource** 資料表來加速資源查詢。</span><span class="sxs-lookup"><span data-stu-id="6eb48-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="6eb48-107">請注意，不再使用 **ResRollup** 資料表。</span><span class="sxs-lookup"><span data-stu-id="6eb48-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6eb48-108">如果資源產能彙總同步處理程序或 **ResProjectResource** 資料表有相依性，請不要使用此功能。</span><span class="sxs-lookup"><span data-stu-id="6eb48-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="6eb48-109">啟用資源排程效能增強功能</span><span class="sxs-lookup"><span data-stu-id="6eb48-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="6eb48-110">若要啟用資源排程效能增強功能，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="6eb48-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="6eb48-111">移至 **功能管理** > **全部** ，並在功能清單中找出 **啟用專案資源排程效能增強功能** 。</span><span class="sxs-lookup"><span data-stu-id="6eb48-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="6eb48-112">選取 **立即啟用** 。</span><span class="sxs-lookup"><span data-stu-id="6eb48-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="6eb48-113">如果清單中找不到此功能，請選取 **檢查更新** 以重新整理清單。</span><span class="sxs-lookup"><span data-stu-id="6eb48-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="6eb48-114">重新整理瀏覽器，然後移至 **專案管理與會計** > **定期** > **專案資源** > **同步處理所有公司的資源行事曆產能** 。</span><span class="sxs-lookup"><span data-stu-id="6eb48-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="6eb48-115">將 **移除現有的產能記錄** 設定為 **是** ，以移除先前的資料。</span><span class="sxs-lookup"><span data-stu-id="6eb48-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="6eb48-116">如果您想要產生增量資料，請將其設定為 **否** 。</span><span class="sxs-lookup"><span data-stu-id="6eb48-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="6eb48-117">在 **期間代碼** 欄位中，選取要產生資料的期間。</span><span class="sxs-lookup"><span data-stu-id="6eb48-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="6eb48-118">如果您選取期間代碼，則不需定義開始和結束日期。</span><span class="sxs-lookup"><span data-stu-id="6eb48-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="6eb48-119">如果讓 **期間代碼** 欄位保持空白，請選取要產生資料的特定開始及結束日期。</span><span class="sxs-lookup"><span data-stu-id="6eb48-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="6eb48-120">選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="6eb48-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="6eb48-121">這會將一般資料發佈至您環境中所有公司之間的 **ResCalendarCapacity** 資料表，因此批次處理工作只需在一個法律實體中執行。</span><span class="sxs-lookup"><span data-stu-id="6eb48-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="6eb48-122">需要使用此批次作業中的資料，才能透過相關行事曆計算資源產能。</span><span class="sxs-lookup"><span data-stu-id="6eb48-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="6eb48-123">移至 **專案管理與會計** > **定期** > **專案資源** > **填入所有公司之間的專案資源** ，然後選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="6eb48-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="6eb48-124">這是適用於 **ResProjectResource** 、 **ResCalendarDateTimeRange** 和 **ResEffectiveDateTimeRange** 資料表中一般資料的資料升級指令碼。</span><span class="sxs-lookup"><span data-stu-id="6eb48-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="6eb48-125">**PSAPRojSchedRole.RootActivity** 欄位的值也會更新。</span><span class="sxs-lookup"><span data-stu-id="6eb48-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="6eb48-126">如果未執行此作業，您就會在嘗試執行資源排程作業時收到警告。</span><span class="sxs-lookup"><span data-stu-id="6eb48-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="6eb48-127">關閉資源排程效能增強功能</span><span class="sxs-lookup"><span data-stu-id="6eb48-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="6eb48-128">移至 **功能管理** > **全部** ，並搜尋 **啟用專案資源排程效能增強功能** 。</span><span class="sxs-lookup"><span data-stu-id="6eb48-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="6eb48-129">選取功能，然後選取 **停用** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="6eb48-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="6eb48-130">重新整理您的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="6eb48-130">Refresh your browser.</span></span>
4. <span data-ttu-id="6eb48-131">移至 **專案管理與會計** > **定期** > **產能同步處理** > **同步處理資源產能彙總** 。</span><span class="sxs-lookup"><span data-stu-id="6eb48-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="6eb48-132">在 **產能彙總同步處理** 頁面上，將 **移除現有的產能記錄** 設定為 **是** ，以移除先前的資料。</span><span class="sxs-lookup"><span data-stu-id="6eb48-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="6eb48-133">如果您想要產生增量資料，請將其設定為 **否** 。</span><span class="sxs-lookup"><span data-stu-id="6eb48-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="6eb48-134">在 **期間代碼** 欄位中，選取要產生資料的期間。</span><span class="sxs-lookup"><span data-stu-id="6eb48-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="6eb48-135">如果您選取期間代碼，則不需定義開始和結束日期。</span><span class="sxs-lookup"><span data-stu-id="6eb48-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="6eb48-136">如果讓 **期間代碼** 欄位保持空白，請選取要產生資料的特定開始及結束日期。</span><span class="sxs-lookup"><span data-stu-id="6eb48-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="6eb48-137">選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="6eb48-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="6eb48-138">這會將一般資料發佈至您環境中所有公司之間的 **ResRollup** 資料表，因此批次處理工作只需在一個法律實體中執行。</span><span class="sxs-lookup"><span data-stu-id="6eb48-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="6eb48-139">所有 **資源可用性** 檢視表都需要這個批次工作。</span><span class="sxs-lookup"><span data-stu-id="6eb48-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="6eb48-140">如果此批次作業未執行，則會即時產生 **ResRollup** 資料，而這可能需要一些時間。</span><span class="sxs-lookup"><span data-stu-id="6eb48-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
