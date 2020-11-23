---
title: 佈建新的環境
description: 本主題提供有關如何佈建新的 Project Operations 環境的資訊。
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 044a942a068b33318b98041cc94944d90c1d63c3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121163"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="67009-103">佈建新的環境</span><span class="sxs-lookup"><span data-stu-id="67009-103">Provision a new environment</span></span>

<span data-ttu-id="67009-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="67009-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="67009-105">本主題提供有關如何為資源/非庫存型案例佈建新的 Dynamics 365 Project Operations 環境的資訊。</span><span class="sxs-lookup"><span data-stu-id="67009-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="67009-106">在 LCS 專案中啟用 Project Operations 自動化佈建</span><span class="sxs-lookup"><span data-stu-id="67009-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="67009-107">使用下列步驟，為您的 LCS 專案啟用 Project Operations 自動化佈建流程。</span><span class="sxs-lookup"><span data-stu-id="67009-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="67009-108">前往 [LCS](https://lcs.dynamics.com/v2)，並選取 **預覽功能管理** 圖標。</span><span class="sxs-lookup"><span data-stu-id="67009-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="67009-109">在 **預覽功能** 清單中，選取 **Project Operations 功能**，然後選取 **預覽功能已啟用** 以啟用 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="67009-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="67009-110">每個 LCS 專案都只會執行此步驟一次。</span><span class="sxs-lookup"><span data-stu-id="67009-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="67009-111">佈建 Project Operations 環境</span><span class="sxs-lookup"><span data-stu-id="67009-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="67009-112">開啟新的 Dynamics 365 Finance [示範環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)或[沙箱/生產環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)部署。</span><span class="sxs-lookup"><span data-stu-id="67009-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="67009-113">逐步解說 **環境佈建** 精靈。</span><span class="sxs-lookup"><span data-stu-id="67009-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="67009-114">請確定選取的應用程式版本是 10.0.13 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="67009-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="67009-115">若要佈建 Project Operations，請選取 **進階設定** 下方的 **Common Data Service**。</span><span class="sxs-lookup"><span data-stu-id="67009-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="67009-116">選取 **是**，然後在必要欄位中輸入資訊，以啟用 **Common Data Service 設定**：</span><span class="sxs-lookup"><span data-stu-id="67009-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="67009-117">名字</span><span class="sxs-lookup"><span data-stu-id="67009-117">Name</span></span>
  - <span data-ttu-id="67009-118">地區</span><span class="sxs-lookup"><span data-stu-id="67009-118">Region</span></span>
  - <span data-ttu-id="67009-119">語言</span><span class="sxs-lookup"><span data-stu-id="67009-119">Language</span></span>
  - <span data-ttu-id="67009-120">貨幣</span><span class="sxs-lookup"><span data-stu-id="67009-120">Currency</span></span>
 
5. <span data-ttu-id="67009-121">在 **Common Data Service 範本** 欄位中，選取 **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="67009-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="67009-122">選取部署的環境類型。</span><span class="sxs-lookup"><span data-stu-id="67009-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="67009-123">以訂閱為主的試用可讓您 部署為期 30 天的 CDS 環境。</span><span class="sxs-lookup"><span data-stu-id="67009-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![部署設定](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="67009-125">選取 **同意** 確認服務條款，然後選取 **完成** 以返回部署設定。</span><span class="sxs-lookup"><span data-stu-id="67009-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![部署同意](./media/2DeploymentConsent.png)

7. <span data-ttu-id="67009-127">完成精靈中的其餘必要欄位，並確認部署。</span><span class="sxs-lookup"><span data-stu-id="67009-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="67009-128">環境佈建時間會根據環境類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="67009-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="67009-129">佈建最多可能需要六小時的時間。</span><span class="sxs-lookup"><span data-stu-id="67009-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="67009-130">部署順利完成後，環境將會顯示為 **已部署**。</span><span class="sxs-lookup"><span data-stu-id="67009-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="67009-131">若要確認已成功部署環境，請選取 **登入**，並登入要確認的環境。</span><span class="sxs-lookup"><span data-stu-id="67009-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ 環境詳細資料](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="67009-133">套用 Project Operations 財務示範資料 (選用步驟)</span><span class="sxs-lookup"><span data-stu-id="67009-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="67009-134">將 Project Operations 財務示範資料套用至 10.0.13 服務版本雲端託管的環境，如[本文章](resource-apply-finance-demo-data.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="67009-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="67009-135">將更新套用至 Finance 環境</span><span class="sxs-lookup"><span data-stu-id="67009-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="67009-136">Project Operations 需要應用程式版本為 **10.0.13 (10.0.569.20009)** 或更新版本的 Finance 環境。</span><span class="sxs-lookup"><span data-stu-id="67009-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="67009-137">您可能需要將品質更新套用至 Finance 環境，才能收到此版本。</span><span class="sxs-lookup"><span data-stu-id="67009-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="67009-138">在 LCS 的 **環境詳細資料** 頁面上，選取 **可用更新** 區段中的 **檢視更新**。</span><span class="sxs-lookup"><span data-stu-id="67009-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![檢視更新](./media/5ViewUpdates.png)

2. <span data-ttu-id="67009-140">在 **二進位更新** 頁面上，選取 **儲存套件**。</span><span class="sxs-lookup"><span data-stu-id="67009-140">On the **Binary updates** page, select **Save package.**</span></span>

![儲存套件](./media/6SavePackage.png)

3. <span data-ttu-id="67009-142">按一下 **全選**，然後選取 **儲存套件**。</span><span class="sxs-lookup"><span data-stu-id="67009-142">Click **Select all** and then select **Save package**.</span></span>

![檢閱並儲存更新](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="67009-144">輸入套件的名稱和描述，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="67009-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="67009-145">視網際網路連線而定，此程序可能需要花費一些時間。</span><span class="sxs-lookup"><span data-stu-id="67009-145">Depending on the internet connection, this process might take some time.</span></span>

![將套件上載至資產庫](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="67009-147">儲存套件後，選取 **完成**，並將此套件儲存至 LCS 專案中的資產庫。</span><span class="sxs-lookup"><span data-stu-id="67009-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="67009-148">儲存和驗證套件可能需要約 15 分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="67009-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="67009-149">若要套用更新，請瀏覽至 LCS 中的 **環境詳細資料** 頁面，然後選取 **維護** >  **套用更新**。</span><span class="sxs-lookup"><span data-stu-id="67009-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![維護環境](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="67009-151">在更新清單中，選取您所建立的套件，並選取 **套用**。</span><span class="sxs-lookup"><span data-stu-id="67009-151">In the updates list select the package you created, and select **Apply**.</span></span>

![套用更新](./media/10ApplyUpdates.png)

<span data-ttu-id="67009-153">環境維護需要一些時間。</span><span class="sxs-lookup"><span data-stu-id="67009-153">Environment servicing will take some time.</span></span> <span data-ttu-id="67009-154">完成後，環境會回復到已部署的狀態。</span><span class="sxs-lookup"><span data-stu-id="67009-154">After it is complete, the environment will return to a deployed state.</span></span>

![環境已部署](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="67009-156">建立雙重寫入連接</span><span class="sxs-lookup"><span data-stu-id="67009-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="67009-157">在 LCS 專案中，移至 **環境詳細資料** 頁面。</span><span class="sxs-lookup"><span data-stu-id="67009-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="67009-158">在 **Common Data Service 環境資訊** 底下，選取 **連結至 CDS for Apps**。</span><span class="sxs-lookup"><span data-stu-id="67009-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="67009-159">連結完成後，請再次選取 **連結至 CDS for Apps**。</span><span class="sxs-lookup"><span data-stu-id="67009-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="67009-160">將您重新導向至 Finance 中的雙重寫入。</span><span class="sxs-lookup"><span data-stu-id="67009-160">You will be redirected to Dual Write in Finance.</span></span>

![連結至 CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="67009-162">選取 **套用解決方案**，以存取將在整合中對應的實體。</span><span class="sxs-lookup"><span data-stu-id="67009-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![套用解決方案](./media/13ApplySolutions.png)

5. <span data-ttu-id="67009-164">選取 **Dynamics 365 Finance and Operations 雙重寫入實體對應** 和 **Dynamics 365 Project Operations 雙重寫入實體對應** 這兩個解決方案，然後選取 **套用**。</span><span class="sxs-lookup"><span data-stu-id="67009-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![確認解決方案](./media/14ConfirmSolutions.png)

<span data-ttu-id="67009-166">套用解決方案後，將雙重寫入實體套用至環境。</span><span class="sxs-lookup"><span data-stu-id="67009-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![套用解決方案](./media/15ApplyingSolutions.png)

<span data-ttu-id="67009-168">套用實體後，環境中會列出所有可用的對應。</span><span class="sxs-lookup"><span data-stu-id="67009-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![雙重寫入對應](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="67009-170">更新後重新整理資料實體</span><span class="sxs-lookup"><span data-stu-id="67009-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="67009-171">在 Finance 中，移至 **資料管理** 工作區。</span><span class="sxs-lookup"><span data-stu-id="67009-171">In Finance, go to the **Data management** workspace.</span></span>

![資料管理工作區](./media/16DataManagement.png)

2. <span data-ttu-id="67009-173">選取 **架構參數** 圖標。</span><span class="sxs-lookup"><span data-stu-id="67009-173">Select the **Framework parameters** tile.</span></span>

![架構參數](./media/17FrameworkParameters.png)

3. <span data-ttu-id="67009-175">在 **實體設定** 頁面上，選取 **重新整理實體清單**。</span><span class="sxs-lookup"><span data-stu-id="67009-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![重新整理實體清單](./media/18RefreshEntityList.png)

<span data-ttu-id="67009-177">重新整理將需要約 20 分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="67009-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="67009-178">完成時，您會收到警示。</span><span class="sxs-lookup"><span data-stu-id="67009-178">You will receive an alert when it is complete.</span></span>

![重新整理確認](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="67009-180">執行 Project Operations 雙重寫入對應</span><span class="sxs-lookup"><span data-stu-id="67009-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="67009-181">在 LCS 專案中，移至 **環境詳細資料** 頁面。</span><span class="sxs-lookup"><span data-stu-id="67009-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="67009-182">在 **Common Data Service 環境資訊** 底下，選取 **連結至 CDS for Apps**。</span><span class="sxs-lookup"><span data-stu-id="67009-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="67009-183">選取連結之後，您會重新導向至對應中實體的清單。</span><span class="sxs-lookup"><span data-stu-id="67009-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="67009-184">依照下表所述，開始對應。</span><span class="sxs-lookup"><span data-stu-id="67009-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="67009-185">請務必遵循列示的順序進行。</span><span class="sxs-lookup"><span data-stu-id="67009-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="67009-186">**實體對應**</span><span class="sxs-lookup"><span data-stu-id="67009-186">**Entity Map**</span></span> | <span data-ttu-id="67009-187">**重新整理實體**</span><span class="sxs-lookup"><span data-stu-id="67009-187">**Refresh entity**</span></span> | <span data-ttu-id="67009-188">**初始同步**</span><span class="sxs-lookup"><span data-stu-id="67009-188">**Initial sync**</span></span> | <span data-ttu-id="67009-189">**初始同步處理的主要記錄**</span><span class="sxs-lookup"><span data-stu-id="67009-189">**Master for initial sync**</span></span> | <span data-ttu-id="67009-190">**執行先決條件**</span><span class="sxs-lookup"><span data-stu-id="67009-190">**Run prerequisites**</span></span> | <span data-ttu-id="67009-191">**先決條件初始同步**</span><span class="sxs-lookup"><span data-stu-id="67009-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="67009-192">**所有公司的專案資源角色 (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="67009-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="67009-193">無</span><span class="sxs-lookup"><span data-stu-id="67009-193">No</span></span> | <span data-ttu-id="67009-194">.是</span><span class="sxs-lookup"><span data-stu-id="67009-194">Yes</span></span> | <span data-ttu-id="67009-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="67009-195">Common Data Service</span></span> | <span data-ttu-id="67009-196">無</span><span class="sxs-lookup"><span data-stu-id="67009-196">No</span></span> | <span data-ttu-id="67009-197">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-197">N\A</span></span> |
| <span data-ttu-id="67009-198">**法律實體 (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="67009-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="67009-199">無</span><span class="sxs-lookup"><span data-stu-id="67009-199">No</span></span> | <span data-ttu-id="67009-200">.是</span><span class="sxs-lookup"><span data-stu-id="67009-200">Yes</span></span> | <span data-ttu-id="67009-201">Finance and Operations 應用程式</span><span class="sxs-lookup"><span data-stu-id="67009-201">Finance and Operations apps</span></span> | <span data-ttu-id="67009-202">無</span><span class="sxs-lookup"><span data-stu-id="67009-202">No</span></span> | <span data-ttu-id="67009-203">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-203">N\A</span></span> |
| <span data-ttu-id="67009-204">**Project Operations 整合實際值 (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="67009-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="67009-205">無</span><span class="sxs-lookup"><span data-stu-id="67009-205">No</span></span> | <span data-ttu-id="67009-206">無</span><span class="sxs-lookup"><span data-stu-id="67009-206">No</span></span> | <span data-ttu-id="67009-207">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-207">N\A</span></span> | <span data-ttu-id="67009-208">.是</span><span class="sxs-lookup"><span data-stu-id="67009-208">Yes</span></span> | <span data-ttu-id="67009-209">無</span><span class="sxs-lookup"><span data-stu-id="67009-209">No</span></span> |
| <span data-ttu-id="67009-210">**專案合約服務內容 (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="67009-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="67009-211">無</span><span class="sxs-lookup"><span data-stu-id="67009-211">No</span></span> | <span data-ttu-id="67009-212">無</span><span class="sxs-lookup"><span data-stu-id="67009-212">No</span></span> | <span data-ttu-id="67009-213">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-213">N\A</span></span> | <span data-ttu-id="67009-214">無</span><span class="sxs-lookup"><span data-stu-id="67009-214">No</span></span> | <span data-ttu-id="67009-215">無</span><span class="sxs-lookup"><span data-stu-id="67009-215">No</span></span> |
| <span data-ttu-id="67009-216">**專案交易關聯的整合實體 (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="67009-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="67009-217">無</span><span class="sxs-lookup"><span data-stu-id="67009-217">No</span></span> | <span data-ttu-id="67009-218">無</span><span class="sxs-lookup"><span data-stu-id="67009-218">No</span></span> | <span data-ttu-id="67009-219">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-219">N\A</span></span> | <span data-ttu-id="67009-220">無</span><span class="sxs-lookup"><span data-stu-id="67009-220">No</span></span> | <span data-ttu-id="67009-221">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-221">N\A</span></span> |
| <span data-ttu-id="67009-222">**Project Operations 整合合約服務內容里程碑 (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="67009-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="67009-223">無</span><span class="sxs-lookup"><span data-stu-id="67009-223">No</span></span> | <span data-ttu-id="67009-224">無</span><span class="sxs-lookup"><span data-stu-id="67009-224">No</span></span> | <span data-ttu-id="67009-225">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-225">N\A</span></span> | <span data-ttu-id="67009-226">無</span><span class="sxs-lookup"><span data-stu-id="67009-226">No</span></span> | <span data-ttu-id="67009-227">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-227">N\A</span></span> |
| <span data-ttu-id="67009-228">**費用估計值的 Project Operations 整合實體 (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="67009-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="67009-229">無</span><span class="sxs-lookup"><span data-stu-id="67009-229">No</span></span> | <span data-ttu-id="67009-230">無</span><span class="sxs-lookup"><span data-stu-id="67009-230">No</span></span> | <span data-ttu-id="67009-231">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-231">N\A</span></span> | <span data-ttu-id="67009-232">無</span><span class="sxs-lookup"><span data-stu-id="67009-232">No</span></span> | <span data-ttu-id="67009-233">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-233">N\A</span></span> |
| <span data-ttu-id="67009-234">**Project Operations 整合專案費用類別匯出實體 (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="67009-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="67009-235">無</span><span class="sxs-lookup"><span data-stu-id="67009-235">No</span></span> | <span data-ttu-id="67009-236">無</span><span class="sxs-lookup"><span data-stu-id="67009-236">No</span></span> | <span data-ttu-id="67009-237">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-237">N\A</span></span> | <span data-ttu-id="67009-238">無</span><span class="sxs-lookup"><span data-stu-id="67009-238">No</span></span> | <span data-ttu-id="67009-239">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-239">N\A</span></span> |
| <span data-ttu-id="67009-240">**Project Operations 整合專案費用匯出實體 (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="67009-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="67009-241">.是</span><span class="sxs-lookup"><span data-stu-id="67009-241">Yes</span></span> | <span data-ttu-id="67009-242">無</span><span class="sxs-lookup"><span data-stu-id="67009-242">No</span></span> | <span data-ttu-id="67009-243">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-243">N\A</span></span> | <span data-ttu-id="67009-244">無</span><span class="sxs-lookup"><span data-stu-id="67009-244">No</span></span> | <span data-ttu-id="67009-245">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-245">N\A</span></span> |
| <span data-ttu-id="67009-246">**時數估計值的 Project Operations 整合實體 (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="67009-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="67009-247">.是</span><span class="sxs-lookup"><span data-stu-id="67009-247">Yes</span></span> | <span data-ttu-id="67009-248">無</span><span class="sxs-lookup"><span data-stu-id="67009-248">No</span></span> | <span data-ttu-id="67009-249">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-249">N\A</span></span> | <span data-ttu-id="67009-250">無</span><span class="sxs-lookup"><span data-stu-id="67009-250">No</span></span> | <span data-ttu-id="67009-251">不適用</span><span class="sxs-lookup"><span data-stu-id="67009-251">N\A</span></span> |


4. <span data-ttu-id="67009-252">若要重新整理實體，請選取對應名稱，然後選取 **重新整理實體**。</span><span class="sxs-lookup"><span data-stu-id="67009-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![重新整理對應](./media/20RefreshMapping.png)

5. <span data-ttu-id="67009-254">重新整理完成後，執行對應。</span><span class="sxs-lookup"><span data-stu-id="67009-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="67009-255">啟用下一個對應之前，請確認表格中的對應處於 **執行中** 狀態。</span><span class="sxs-lookup"><span data-stu-id="67009-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="67009-256">執行有較大量先決條件的對應可能需要一些時間。</span><span class="sxs-lookup"><span data-stu-id="67009-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="67009-257">若要執行有先決條件的對應，請啟用 **顯示相關實體對應** 切換。</span><span class="sxs-lookup"><span data-stu-id="67009-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="67009-258">如果表中指示 **先決條件初始同步** 為 **否**，請先確認所有先決條件中的 **初始同步** 旗標是否為 **關閉**，再執行此對應。</span><span class="sxs-lookup"><span data-stu-id="67009-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![執行對應](./media/21RunMap.png)

6. <span data-ttu-id="67009-260">驗證所有專案相關的對應是否為執行中狀態。</span><span class="sxs-lookup"><span data-stu-id="67009-260">Validate all project related maps are in the running state.</span></span>

![所有正在執行的對應](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="67009-262">在適用於 Project Operations 的 CDS 中套用設定資料 (選用)</span><span class="sxs-lookup"><span data-stu-id="67009-262">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="67009-263">如果已將示範資料套用至 Finance 環境，請參閱[在適用於 Project Operations 的 Common Data Service 中設定和套用資料](resource-apply-pro-setup-config-data.md)，以將示範資料套用於 CDS 環境。</span><span class="sxs-lookup"><span data-stu-id="67009-263">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="67009-264">您的 Project Operations 環境現在已佈建並設定。</span><span class="sxs-lookup"><span data-stu-id="67009-264">Your Project Operations environment is now provisioned and configured.</span></span> 
