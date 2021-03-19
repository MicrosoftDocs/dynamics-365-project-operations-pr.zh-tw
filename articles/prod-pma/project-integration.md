---
title: Microsoft Project Client 整合
description: 規劃和維護專案排程可能會很複雜，因此專案經理必須使用可協助他們管理這項工作的工具。 與 Microsoft Project Client 的整合可提供支援來開啟和管理專案分工結構圖。
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289314"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="96f98-104">Microsoft Project Client 整合</span><span class="sxs-lookup"><span data-stu-id="96f98-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96f98-105">規劃和維護專案排程可能會很複雜，因此專案經理必須使用可協助他們管理這項工作的工具。</span><span class="sxs-lookup"><span data-stu-id="96f98-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="96f98-106">與 Microsoft Project Client 的整合可提供支援來開啟和管理專案分工結構圖。</span><span class="sxs-lookup"><span data-stu-id="96f98-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="96f98-107">專案經理可以將任何變更發佈回 Dynamics 365 Finance 專案分工結構圖。</span><span class="sxs-lookup"><span data-stu-id="96f98-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="96f98-108">如果您使用的是 7 月更新 (10.0.4 版)，則必須安裝 KB 4054797 和 4055884。</span><span class="sxs-lookup"><span data-stu-id="96f98-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="96f98-109">設定 Microsoft Project Client 增益集</span><span class="sxs-lookup"><span data-stu-id="96f98-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="96f98-110">若要啟用與 Microsoft Project Client 的整合，您必須在使用者的用戶端 Microsoft Project 應用程式中安裝 Microsoft Dynamics 365 增益集。</span><span class="sxs-lookup"><span data-stu-id="96f98-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="96f98-111">這可以藉由開啟 **專案管理工作區** 來完成。</span><span class="sxs-lookup"><span data-stu-id="96f98-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="96f98-112">•   在工作區的 **連結** > **設定** 區段中按一下 **設定 Project Client 增益集**。</span><span class="sxs-lookup"><span data-stu-id="96f98-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="96f98-113">•   按一下 **開啟**，然後在出現提示時按一下 **執行**。</span><span class="sxs-lookup"><span data-stu-id="96f98-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="96f98-114">在 Microsoft Project Client 中開啟並編輯現有的草稿分工結構圖</span><span class="sxs-lookup"><span data-stu-id="96f98-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="96f98-115">如果 Dynamics 365 Finance 中的專案已建立分工結構圖，且分工結構圖為草稿狀態，則可以在 Microsoft Project Client 應用程式中開啟該分工結構圖。</span><span class="sxs-lookup"><span data-stu-id="96f98-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="96f98-116">若要從 **專案** 頁面中開啟，請按一下 **計劃** 索引標籤中的 **在 Microsoft Project 中開啟** 連結。您也可以按一下 **Microsoft Dynamics 365** 索引標籤中的 **開啟**，從 Microsoft Project Client 應用程式中開啟此頁面。從清單選取 **實體** 和 **專案**。</span><span class="sxs-lookup"><span data-stu-id="96f98-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="96f98-117">如果您使用的瀏覽器是 Internet Explorer，則需要按一下 **儲存**，以手動方式從下載檔案的位置開啟。</span><span class="sxs-lookup"><span data-stu-id="96f98-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="96f98-118">或者，按一下 **儲存後開啟**，以在 Microsoft Project Client 中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="96f98-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="96f98-119">不要在儲存時將將檔案名稱重新命名。</span><span class="sxs-lookup"><span data-stu-id="96f98-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="96f98-120">使用 Microsoft Project Client 對檔案進行編輯前，必須先將其簽出。按一下 **Microsoft Dynamics 365** 索引標籤中的 **簽出**。這可防止其他使用者同時從 Finance 中編輯分工結構圖。</span><span class="sxs-lookup"><span data-stu-id="96f98-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="96f98-121">若要在完成任何編輯後發佈分工結構圖，請按一下 **Microsoft Dynamics 365** 索引標籤上的 **簽入**。</span><span class="sxs-lookup"><span data-stu-id="96f98-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="96f98-122">如果已在 Finance 中新增專案團隊至專案，則會以團隊成員填入資源清單中。</span><span class="sxs-lookup"><span data-stu-id="96f98-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="96f98-123">如果尚未將專案團隊新增至專案，您可以按一下 **Microsoft Dynamics 365** 索引標籤上的 **資源** 按鈕選取資源，並在 Microsoft Project Client 中建立團隊。</span><span class="sxs-lookup"><span data-stu-id="96f98-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="96f98-124">下列資料會在進行簽入程序時同步回到 Finance：</span><span class="sxs-lookup"><span data-stu-id="96f98-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="96f98-125">•   任務名稱</span><span class="sxs-lookup"><span data-stu-id="96f98-125">•   Task name</span></span>

<span data-ttu-id="96f98-126">•   開始日期</span><span class="sxs-lookup"><span data-stu-id="96f98-126">•   Start date</span></span>

<span data-ttu-id="96f98-127">•   完成日期</span><span class="sxs-lookup"><span data-stu-id="96f98-127">•   Finish date</span></span>

<span data-ttu-id="96f98-128">•   前置任務</span><span class="sxs-lookup"><span data-stu-id="96f98-128">•   Predecessors</span></span>

<span data-ttu-id="96f98-129">Predecessors資源名稱</span><span class="sxs-lookup"><span data-stu-id="96f98-129">•   Resource names</span></span>

<span data-ttu-id="96f98-130">•   類別</span><span class="sxs-lookup"><span data-stu-id="96f98-130">•   Category</span></span>

<span data-ttu-id="96f98-131">•   資源類別</span><span class="sxs-lookup"><span data-stu-id="96f98-131">•   Resource category</span></span>

<span data-ttu-id="96f98-132">•   工作時數</span><span class="sxs-lookup"><span data-stu-id="96f98-132">•   Work hours</span></span>

<span data-ttu-id="96f98-133">•   附註</span><span class="sxs-lookup"><span data-stu-id="96f98-133">•   Notes</span></span>

<span data-ttu-id="96f98-134">•   優先順序</span><span class="sxs-lookup"><span data-stu-id="96f98-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="96f98-135">如果您將任何其他欄新增至 Microsoft Project Client 檔案，則這些欄不會儲存至此檔案，也不會在重新開啟檔案時顯示該檔案。</span><span class="sxs-lookup"><span data-stu-id="96f98-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="96f98-136">使用 Microsoft Project Client 建立現有專案的分工結構圖</span><span class="sxs-lookup"><span data-stu-id="96f98-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="96f98-137">若要使用 Microsoft Project Client 建立新的分工結構圖，請依照下列步驟進行：</span><span class="sxs-lookup"><span data-stu-id="96f98-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="96f98-138">開啟 Microsoft Project Client。</span><span class="sxs-lookup"><span data-stu-id="96f98-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="96f98-139">在 **Microsoft Dynamics 365** 索引標籤中，按一下 **開啟**。</span><span class="sxs-lookup"><span data-stu-id="96f98-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="96f98-140">選取專案的 **舊版實體**。</span><span class="sxs-lookup"><span data-stu-id="96f98-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="96f98-141">選取 **專案**。</span><span class="sxs-lookup"><span data-stu-id="96f98-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="96f98-142">按一下 **Microsoft Dynamics 365** 索引標籤上的 **簽出**。</span><span class="sxs-lookup"><span data-stu-id="96f98-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="96f98-143">準備好發佈至 Finance 時，按一下 **Microsoft Dynamics 365** 索引標籤上的 **簽入**。</span><span class="sxs-lookup"><span data-stu-id="96f98-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="96f98-144">使用 Microsoft Project Client 取代現有專案的現有分工結構圖</span><span class="sxs-lookup"><span data-stu-id="96f98-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="96f98-145">若要使用 Microsoft Project Client 建立新的分工結構圖，並取代現有專案的現有分工結構圖，請依照下列步驟進行：</span><span class="sxs-lookup"><span data-stu-id="96f98-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="96f98-146">開啟 Microsoft Project Client。</span><span class="sxs-lookup"><span data-stu-id="96f98-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="96f98-147">在 Microsoft Project Client 中建立排程。</span><span class="sxs-lookup"><span data-stu-id="96f98-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="96f98-148">在 **Microsoft Dynamics 365** 索引標籤中，按一下 **儲存變更** > **取代現有的專案**。</span><span class="sxs-lookup"><span data-stu-id="96f98-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="96f98-149">選取專案的 **舊版實體**。</span><span class="sxs-lookup"><span data-stu-id="96f98-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="96f98-150">選取 **專案**。</span><span class="sxs-lookup"><span data-stu-id="96f98-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="96f98-151">按一下 **確定**。</span><span class="sxs-lookup"><span data-stu-id="96f98-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="96f98-152">從 Microsoft Project Client 中建立新專案</span><span class="sxs-lookup"><span data-stu-id="96f98-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="96f98-153">開啟 Microsoft Project Client。</span><span class="sxs-lookup"><span data-stu-id="96f98-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="96f98-154">在 Microsoft Project Client 中建立排程。</span><span class="sxs-lookup"><span data-stu-id="96f98-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="96f98-155">在 **Microsoft Dynamics 365** 索引標籤中，按一下 **儲存變更** > **儲存至新專案**。</span><span class="sxs-lookup"><span data-stu-id="96f98-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="96f98-156">選取專案的 **舊版實體**。</span><span class="sxs-lookup"><span data-stu-id="96f98-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="96f98-157">如有需要，輸入 **專案識別碼**。</span><span class="sxs-lookup"><span data-stu-id="96f98-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="96f98-158">輸入 **專案名稱**。</span><span class="sxs-lookup"><span data-stu-id="96f98-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="96f98-159">選取 **專案類型**、**專案群組** 和 **專案合約識別碼**。</span><span class="sxs-lookup"><span data-stu-id="96f98-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="96f98-160">或者，也可以按一下 **新增** 來建立新的專案合約。</span><span class="sxs-lookup"><span data-stu-id="96f98-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="96f98-161">選取要用於資源分配的 **行事曆**。</span><span class="sxs-lookup"><span data-stu-id="96f98-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="96f98-162">按一下 **確定**。</span><span class="sxs-lookup"><span data-stu-id="96f98-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]