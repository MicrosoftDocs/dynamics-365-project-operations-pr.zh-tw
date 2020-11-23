---
title: 使用 Project Service 增益集在 Microsoft Project 中規劃您的工作 | MicrosoftDocs
description: 此主題提供有關如何新增、設定和使用 Microsoft Project Service 的 Microsoft Project 增益集的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129668"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="83328-103">使用 Project Service Automation 增益集在 Microsoft Project 中規劃您的工作</span><span class="sxs-lookup"><span data-stu-id="83328-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="83328-104">讓您更容易進行專案規劃，包括估計值。</span><span class="sxs-lookup"><span data-stu-id="83328-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="83328-105">您可以定義工作，在提交最終提案時清楚呈現成本、努力及銷售值。</span><span class="sxs-lookup"><span data-stu-id="83328-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="83328-106">現在您可以安裝 [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)]，並且在您熟悉的 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 環境中規劃工作。</span><span class="sxs-lookup"><span data-stu-id="83328-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="83328-107">使用 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 健全的規劃及管理功能，然後在 Project Service Automation 中更新您的專案計劃。</span><span class="sxs-lookup"><span data-stu-id="83328-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="83328-108">若要使用 SharePoint 文件管理儲存您的 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 檔案以用於 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 專案，[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 系統管理員必須開啟文件管理。</span><span class="sxs-lookup"><span data-stu-id="83328-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="83328-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] 僅與 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition 相容。</span><span class="sxs-lookup"><span data-stu-id="83328-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="83328-110">下載並安裝增益集</span><span class="sxs-lookup"><span data-stu-id="83328-110">Download and install the add-in</span></span>  
 <span data-ttu-id="83328-111">準備好 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 登入資訊。</span><span class="sxs-lookup"><span data-stu-id="83328-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="83328-112">您需要這項資訊從 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 連線至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。</span><span class="sxs-lookup"><span data-stu-id="83328-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="83328-113">您可以從「下載中心」下載支援的 Project Service 版本 [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) 或 [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) 的增益集。</span><span class="sxs-lookup"><span data-stu-id="83328-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="83328-114">按一下下載連結。</span><span class="sxs-lookup"><span data-stu-id="83328-114">Click the download link.</span></span>  

3.  <span data-ttu-id="83328-115">下載完成時，按一下 **是** 以安裝增益集。</span><span class="sxs-lookup"><span data-stu-id="83328-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="83328-116">設定增益集</span><span class="sxs-lookup"><span data-stu-id="83328-116">Configure the add-in</span></span>  

1. <span data-ttu-id="83328-117">開啟 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]，然後按一下 **Project Service** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="83328-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="83328-118">按一下 **連線**。</span><span class="sxs-lookup"><span data-stu-id="83328-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="83328-119">輸入您的登入資訊，然後按一下 **登入**。</span><span class="sxs-lookup"><span data-stu-id="83328-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="83328-120">現在您可以開始使用增益集。</span><span class="sxs-lookup"><span data-stu-id="83328-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="83328-121">從範本讀取</span><span class="sxs-lookup"><span data-stu-id="83328-121">Read from a template</span></span>  
 <span data-ttu-id="83328-122">從您在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中建立並複製到 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 的範本讀取，開始您的專案規劃。</span><span class="sxs-lookup"><span data-stu-id="83328-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)]<span data-ttu-id="83328-123">[建立專案範本 (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="83328-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="83328-124">從 **Project Service** 索引標籤按一下 **讀取** > **Project Service Automation 專案範本**。</span><span class="sxs-lookup"><span data-stu-id="83328-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="83328-125">從清單中選擇專案範本，然後按一下 **開啟**。</span><span class="sxs-lookup"><span data-stu-id="83328-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="83328-126">根據預設，從範本複製到 Project 的工作會設定為手動排程。</span><span class="sxs-lookup"><span data-stu-id="83328-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="83328-127">將 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 角色指派給專案資源</span><span class="sxs-lookup"><span data-stu-id="83328-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="83328-128">開啟專案，然後按一下 **工作** 功能區。</span><span class="sxs-lookup"><span data-stu-id="83328-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="83328-129">按一下 **甘特圖** 功能表，然後選擇 **資源工作表**。</span><span class="sxs-lookup"><span data-stu-id="83328-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="83328-130">在 [資源工作表] 上按一下 **Project Service 資源角色** 下拉式功能表，然後選擇 Project Service Automation 角色。</span><span class="sxs-lookup"><span data-stu-id="83328-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="83328-131">為您的專案配置資源</span><span class="sxs-lookup"><span data-stu-id="83328-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="83328-132">從 [Project Service] 索引標籤中選取一列，然後按一下 **尋找資源**。</span><span class="sxs-lookup"><span data-stu-id="83328-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="83328-133">在 **預約資源** 畫面中，選取要用於專案的資源。</span><span class="sxs-lookup"><span data-stu-id="83328-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="83328-134">按一下 **預約**，然後按一下 **確定**。</span><span class="sxs-lookup"><span data-stu-id="83328-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="83328-135">發行您的專案</span><span class="sxs-lookup"><span data-stu-id="83328-135">Publish your project</span></span>  
<span data-ttu-id="83328-136">專案規劃完成後，下一步是匯入專案並發行至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中。</span><span class="sxs-lookup"><span data-stu-id="83328-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="83328-137">專案將匯入到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。</span><span class="sxs-lookup"><span data-stu-id="83328-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="83328-138">定價和團隊產生程序會套用。</span><span class="sxs-lookup"><span data-stu-id="83328-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="83328-139">在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中開啟專案，會看見團隊、專案估計值及分工結構圖已產生。</span><span class="sxs-lookup"><span data-stu-id="83328-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="83328-140">下表顯示何處可找到結果：</span><span class="sxs-lookup"><span data-stu-id="83328-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="83328-141">**甘特圖**</span><span class="sxs-lookup"><span data-stu-id="83328-141">**Gantt Chart**</span></span>   | <span data-ttu-id="83328-142">匯入至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **分工結構圖** 畫面。</span><span class="sxs-lookup"><span data-stu-id="83328-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="83328-143">**資源工作表**</span><span class="sxs-lookup"><span data-stu-id="83328-143">**Resource Sheet**</span></span> |   <span data-ttu-id="83328-144">匯入至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **團隊成員** 畫面。</span><span class="sxs-lookup"><span data-stu-id="83328-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="83328-145">**使用方式**</span><span class="sxs-lookup"><span data-stu-id="83328-145">**Use Usage**</span></span>    |    <span data-ttu-id="83328-146">匯入至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **專案估計值** 畫面。</span><span class="sxs-lookup"><span data-stu-id="83328-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="83328-147">**若要匯入和發行您的專案**</span><span class="sxs-lookup"><span data-stu-id="83328-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="83328-148">從 **Project Service** 索引標籤按一下 **發行** > **新的 Project Service Automation 專案**。</span><span class="sxs-lookup"><span data-stu-id="83328-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="83328-149">在 **發行至 Project Service 中的新專案** 對話方塊中，輸入 **專案名稱**，然後選取 **客戶**。</span><span class="sxs-lookup"><span data-stu-id="83328-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="83328-150">選擇性地核取 **將專案計劃連結至 Project Service Automation**，將計劃專案檔案連結至 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="83328-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="83328-151">按一下 **發行**。</span><span class="sxs-lookup"><span data-stu-id="83328-151">Click **Publish**.</span></span>  

   <span data-ttu-id="83328-152">將專案檔案連結至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]，讓專案檔案成為主要，並且在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中將分工結構圖設為唯讀。</span><span class="sxs-lookup"><span data-stu-id="83328-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="83328-153">若要對專案計劃進行變更，您需要在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中進行變更，並將它們做為更新發行至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。</span><span class="sxs-lookup"><span data-stu-id="83328-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="83328-154">編輯已匯入的專案</span><span class="sxs-lookup"><span data-stu-id="83328-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="83328-155">若要對已匯入 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 的專案計劃進行變更，您有兩個選項︰</span><span class="sxs-lookup"><span data-stu-id="83328-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="83328-156">開啟主檔案，並在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中編輯。</span><span class="sxs-lookup"><span data-stu-id="83328-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="83328-157">取消連結檔案，並直接在 Project Service 中編輯。</span><span class="sxs-lookup"><span data-stu-id="83328-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="83328-158">根據預設，已從 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 上傳的專案會鎖定，且只能在 Project 中編輯。</span><span class="sxs-lookup"><span data-stu-id="83328-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="83328-159">若要在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中編輯檔案，必須將檔案取消連結。</span><span class="sxs-lookup"><span data-stu-id="83328-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="83328-160">在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中編輯</span><span class="sxs-lookup"><span data-stu-id="83328-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="83328-161">從主要功能表按一下 **Project Service** > **專案**。</span><span class="sxs-lookup"><span data-stu-id="83328-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="83328-162">從專案清單中，開啟您在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中建立的專案。</span><span class="sxs-lookup"><span data-stu-id="83328-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="83328-163">從功能區按一下 **在 MS Project 中開啟**。</span><span class="sxs-lookup"><span data-stu-id="83328-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="83328-164">這樣會在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟連結的主檔案。</span><span class="sxs-lookup"><span data-stu-id="83328-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="83328-165">取消連結檔案，並在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service 中編輯</span><span class="sxs-lookup"><span data-stu-id="83328-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="83328-166">從主要功能表按一下 **Project Service** > **專案**。</span><span class="sxs-lookup"><span data-stu-id="83328-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="83328-167">從專案清單中，開啟您在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中建立的專案。</span><span class="sxs-lookup"><span data-stu-id="83328-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="83328-168">從功能區按一下 **與 MS Project 取消連結**。</span><span class="sxs-lookup"><span data-stu-id="83328-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="83328-169">將專案檔案上傳至 SharePoint 或 Office 群組</span><span class="sxs-lookup"><span data-stu-id="83328-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="83328-170">您可以將專案檔案上傳到 SharePoint，它會位在您的 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 專案的相關聯文件底下。</span><span class="sxs-lookup"><span data-stu-id="83328-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="83328-171">您需要請系統管理員設定 SharePoint 文件管理功能，並開啟專案實體的這項功能。</span><span class="sxs-lookup"><span data-stu-id="83328-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="83328-172">如果您已設定 Office 群組，也可以將專案檔案上傳至[!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]。</span><span class="sxs-lookup"><span data-stu-id="83328-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="83328-173">上傳檔案以用於 SharePoint</span><span class="sxs-lookup"><span data-stu-id="83328-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="83328-174">從主要功能表按一下 **Project Service** > **上傳**。</span><span class="sxs-lookup"><span data-stu-id="83328-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="83328-175">選取 **至 Project Service Automation 專案文件**。</span><span class="sxs-lookup"><span data-stu-id="83328-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="83328-176">在 **啟用在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 對話方塊中，選取 **是** 或 **否**。</span><span class="sxs-lookup"><span data-stu-id="83328-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="83328-177">如果您按一下 **是**，就可以選取 Project Service Automation 中的 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 按鈕、啟動 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]，然後從 SharePoint 文件庫載入專案檔案。</span><span class="sxs-lookup"><span data-stu-id="83328-177">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="83328-178">如果按一下 **否**，則 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 按鈕的連結會沒有作用。</span><span class="sxs-lookup"><span data-stu-id="83328-178">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="83328-179">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 檔案位於 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中特定 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 專案的 **文件** 底下。</span><span class="sxs-lookup"><span data-stu-id="83328-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="83328-180">上傳用於 Office 群組的檔案</span><span class="sxs-lookup"><span data-stu-id="83328-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="83328-181">從主要功能表按一下 **Project Service** > **上傳**。</span><span class="sxs-lookup"><span data-stu-id="83328-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="83328-182">選取 **至 Project Service Automation 專案文件**。</span><span class="sxs-lookup"><span data-stu-id="83328-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="83328-183">在 **啟用在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 對話方塊中，選取 **是** 或 **否**。</span><span class="sxs-lookup"><span data-stu-id="83328-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="83328-184">如果您按一下 **是**，就可以選取 Project Service Automation 中的 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 按鈕、啟動 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]，然後從 SharePoint 文件庫載入專案檔案。</span><span class="sxs-lookup"><span data-stu-id="83328-184">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="83328-185">如果按一下 **否**，則 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 按鈕的連結會沒有作用。</span><span class="sxs-lookup"><span data-stu-id="83328-185">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="83328-186">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 檔案位於 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中特定 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 專案的 **文件** 底下。</span><span class="sxs-lookup"><span data-stu-id="83328-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="83328-187">將專案發行為範本</span><span class="sxs-lookup"><span data-stu-id="83328-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="83328-188">您可以儲存專案並重複使用，只要將它儲存為 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中的專案範本。</span><span class="sxs-lookup"><span data-stu-id="83328-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="83328-189">專案範本是 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中可重複使用的專案計劃。</span><span class="sxs-lookup"><span data-stu-id="83328-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)]<span data-ttu-id="83328-190">[建立專案範本 (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="83328-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="83328-191">從 **Project Service** 索引標籤按一下 **發行** > **新的 Project Service Automation 專案範本**。</span><span class="sxs-lookup"><span data-stu-id="83328-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="83328-192">在 **發行至 Project Service 中的新專案範本** 對話方塊中，輸入 **專案範本名稱**。</span><span class="sxs-lookup"><span data-stu-id="83328-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="83328-193">選擇性地核取 **將專案計劃連結至 Project Service Automation**，將專案檔案連結至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。</span><span class="sxs-lookup"><span data-stu-id="83328-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="83328-194">按一下 **發行**。</span><span class="sxs-lookup"><span data-stu-id="83328-194">Click **Publish**.</span></span>  

<span data-ttu-id="83328-195">將專案檔案連結至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]，讓專案檔案成為主要，並且在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 範本中將分工結構圖設為唯讀。</span><span class="sxs-lookup"><span data-stu-id="83328-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="83328-196">若要對專案計劃進行變更，您需要在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中進行變更，並將它們做為更新發行至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。</span><span class="sxs-lookup"><span data-stu-id="83328-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="83328-197">請參閱</span><span class="sxs-lookup"><span data-stu-id="83328-197">See Also</span></span>  
 [<span data-ttu-id="83328-198">專案經理指南</span><span class="sxs-lookup"><span data-stu-id="83328-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
