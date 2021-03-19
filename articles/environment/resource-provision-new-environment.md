---
title: 佈建新的環境
description: 本主題提供有關如何佈建新的 Project Operations 環境的資訊。
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 50e623d3716c9dd03ce34ec293ba57b5d966d39e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276878"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="f6b27-103">佈建新的環境</span><span class="sxs-lookup"><span data-stu-id="f6b27-103">Provision a new environment</span></span>

<span data-ttu-id="f6b27-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="f6b27-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f6b27-105">此主題提供關於如何佈建新的資源/非庫存型案例適用的 Dynamics 365 Project Operations 環境的資訊。</span><span class="sxs-lookup"><span data-stu-id="f6b27-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="f6b27-106">在 LCS 專案中啟用 Project Operations 自動化佈建</span><span class="sxs-lookup"><span data-stu-id="f6b27-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="f6b27-107">使用下列步驟，為您的 LCS 專案啟用 Project Operations 自動化佈建流程。</span><span class="sxs-lookup"><span data-stu-id="f6b27-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="f6b27-108">前往 [LCS](https://lcs.dynamics.com/v2)，並選取 **預覽功能管理** 圖標。</span><span class="sxs-lookup"><span data-stu-id="f6b27-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="f6b27-109">在 **預覽功能** 清單中，選取 **Project Operations 功能**，然後選取 **預覽功能已啟用** 以啟用 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="f6b27-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f6b27-110">每個 LCS 專案都只會執行此步驟一次。</span><span class="sxs-lookup"><span data-stu-id="f6b27-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="f6b27-111">佈建 Project Operations 環境</span><span class="sxs-lookup"><span data-stu-id="f6b27-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="f6b27-112">開啟新的 Dynamics 365 Finance [示範環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)或[沙箱/生產環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)部署。</span><span class="sxs-lookup"><span data-stu-id="f6b27-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="f6b27-113">逐步解說 **環境佈建** 精靈。</span><span class="sxs-lookup"><span data-stu-id="f6b27-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="f6b27-114">請確定選取的應用程式版本是 10.0.13 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="f6b27-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="f6b27-115">若要佈建 Project Operations，請選取 **進階設定** 下方的 **Common Data Service**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="f6b27-116">選取 **是**，然後在必要欄位中輸入資訊，以啟用 **Common Data Service 設定**：</span><span class="sxs-lookup"><span data-stu-id="f6b27-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="f6b27-117">名字</span><span class="sxs-lookup"><span data-stu-id="f6b27-117">Name</span></span>
  - <span data-ttu-id="f6b27-118">地區</span><span class="sxs-lookup"><span data-stu-id="f6b27-118">Region</span></span>
  - <span data-ttu-id="f6b27-119">語言</span><span class="sxs-lookup"><span data-stu-id="f6b27-119">Language</span></span>
  - <span data-ttu-id="f6b27-120">貨幣</span><span class="sxs-lookup"><span data-stu-id="f6b27-120">Currency</span></span>
 
5. <span data-ttu-id="f6b27-121">在 **Common Data Service 範本** 欄位中，選取 **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="f6b27-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="f6b27-122">選取部署的環境類型。</span><span class="sxs-lookup"><span data-stu-id="f6b27-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="f6b27-123">以訂閱為主的試用可讓您 部署為期 30 天的 CDS 環境。</span><span class="sxs-lookup"><span data-stu-id="f6b27-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![部署設定](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="f6b27-125">選取 **同意** 確認服務條款，然後選取 **完成** 以返回部署設定。</span><span class="sxs-lookup"><span data-stu-id="f6b27-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![部署同意](./media/2DeploymentConsent.png)

7. <span data-ttu-id="f6b27-127">選用 - 將示範資料套用至環境。</span><span class="sxs-lookup"><span data-stu-id="f6b27-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="f6b27-128">移至 **進階設定**、選取 **自訂 SQL Database 設定**，然後將 **指定應用程式資料庫的資料集** 設定為 **示範**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="f6b27-129">完成精靈中的其餘必要欄位，並確認部署。</span><span class="sxs-lookup"><span data-stu-id="f6b27-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="f6b27-130">佈建環境的時間會根據環境類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="f6b27-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="f6b27-131">佈建最多可能需要六小時的時間。</span><span class="sxs-lookup"><span data-stu-id="f6b27-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="f6b27-132">部署順利完成後，環境將會顯示為 **已部署**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="f6b27-133">若要確認環境已部署成功，請選取 **登入**，並登入要確認的環境。</span><span class="sxs-lookup"><span data-stu-id="f6b27-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ 環境詳細資料](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="f6b27-135">將更新套用至 Finance 環境</span><span class="sxs-lookup"><span data-stu-id="f6b27-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="f6b27-136">Project Operations 需要應用程式版本為 **10.0.13 (10.0.569.20009)** 或更新版本的 Finance 環境。</span><span class="sxs-lookup"><span data-stu-id="f6b27-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="f6b27-137">您可能需要將品質更新套用至 Finance 環境，才能收到此版本。</span><span class="sxs-lookup"><span data-stu-id="f6b27-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="f6b27-138">在 LCS 的 **環境詳細資料** 頁面上，選取 **可用更新** 區段中的 **檢視更新**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![檢視更新](./media/5ViewUpdates.png)

2. <span data-ttu-id="f6b27-140">在 **二進位更新** 頁面上，選取 **儲存套件**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-140">On the **Binary updates** page, select **Save package.**</span></span>

![儲存套件](./media/6SavePackage.png)

3. <span data-ttu-id="f6b27-142">按一下 **全選**，然後選取 **儲存套件**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-142">Click **Select all** and then select **Save package**.</span></span>

![檢閱並儲存更新](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="f6b27-144">輸入套件的名稱和描述，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="f6b27-145">視網際網路連線而定，此程序可能需要花費一些時間。</span><span class="sxs-lookup"><span data-stu-id="f6b27-145">Depending on the internet connection, this process might take some time.</span></span>

![將套件上載至資產庫](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="f6b27-147">儲存套件後，選取 **完成**，並將此套件儲存至 LCS 專案中的資產庫。</span><span class="sxs-lookup"><span data-stu-id="f6b27-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="f6b27-148">儲存和驗證套件可能需要約 15 分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="f6b27-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="f6b27-149">若要套用更新，請瀏覽至 LCS 中的 **環境詳細資料** 頁面，然後選取 **維護** >  **套用更新**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![維護環境](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="f6b27-151">在更新清單中，選取您所建立的套件，並選取 **套用**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-151">In the updates list select the package you created, and select **Apply**.</span></span>

![套用更新](./media/10ApplyUpdates.png)

<span data-ttu-id="f6b27-153">環境維護需要一些時間。</span><span class="sxs-lookup"><span data-stu-id="f6b27-153">Environment servicing will take some time.</span></span> <span data-ttu-id="f6b27-154">完成後，環境會回復到已部署的狀態。</span><span class="sxs-lookup"><span data-stu-id="f6b27-154">After it is complete, the environment will return to a deployed state.</span></span>

![環境已部署](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="f6b27-156">建立雙重寫入連接</span><span class="sxs-lookup"><span data-stu-id="f6b27-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="f6b27-157">在 LCS 專案中，移至 **環境詳細資料** 頁面。</span><span class="sxs-lookup"><span data-stu-id="f6b27-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="f6b27-158">在 **Common Data Service 環境資訊** 底下，選取 **連結至 CDS for Apps**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="f6b27-159">連結完成後，請再次選取 **連結至 CDS for Apps**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="f6b27-160">將您重新導向至 Finance 中的雙重寫入。</span><span class="sxs-lookup"><span data-stu-id="f6b27-160">You will be redirected to Dual Write in Finance.</span></span>

![連結至 CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="f6b27-162">選取 **套用解決方案**，以存取將在整合中對應的實體。</span><span class="sxs-lookup"><span data-stu-id="f6b27-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![套用解決方案](./media/13ApplySolutions.png)

5. <span data-ttu-id="f6b27-164">選取兩個解決方案 **Dynamics 365 Finance and Operations 雙重寫入實體對應** 和 **Dynamics 365 Project Operations 雙重寫入實體對應**，然後選取 **套用**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![確認解決方案](./media/14ConfirmSolutions.png)

<span data-ttu-id="f6b27-166">套用解決方案後，將雙重寫入實體套用至環境。</span><span class="sxs-lookup"><span data-stu-id="f6b27-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![套用解決方案](./media/15ApplyingSolutions.png)

<span data-ttu-id="f6b27-168">套用實體後，環境中會列出所有可用的對應。</span><span class="sxs-lookup"><span data-stu-id="f6b27-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![雙重寫入對應](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="f6b27-170">更新後重新整理資料實體</span><span class="sxs-lookup"><span data-stu-id="f6b27-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="f6b27-171">在 Finance 中，移至 **資料管理** 工作區。</span><span class="sxs-lookup"><span data-stu-id="f6b27-171">In Finance, go to the **Data management** workspace.</span></span>

![資料管理工作區](./media/16DataManagement.png)

2. <span data-ttu-id="f6b27-173">選取 **架構參數** 圖標。</span><span class="sxs-lookup"><span data-stu-id="f6b27-173">Select the **Framework parameters** tile.</span></span>

![架構參數](./media/17FrameworkParameters.png)

3. <span data-ttu-id="f6b27-175">在 **實體設定** 頁面上，選取 **重新整理實體清單**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![重新整理實體清單](./media/18RefreshEntityList.png)

<span data-ttu-id="f6b27-177">重新整理將需要約 20 分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="f6b27-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="f6b27-178">完成時，您會收到警示。</span><span class="sxs-lookup"><span data-stu-id="f6b27-178">You will receive an alert when it is complete.</span></span>

![重新整理確認](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="f6b27-180">在 Dataverse 上更新 Project Operations 的安全性設定</span><span class="sxs-lookup"><span data-stu-id="f6b27-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="f6b27-181">移至 Dataverse 環境上的 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="f6b27-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="f6b27-182">移至 **設定** > **安全性** > **資訊安全角色**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="f6b27-183">在 **資料安全角色** 頁面的角色清單中，選取 **雙重寫入應用程式使用者**，然後選取 **自訂實體** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="f6b27-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="f6b27-184">確認角色是否對下列各項具有 **讀取** 和 **附加至** 權限：</span><span class="sxs-lookup"><span data-stu-id="f6b27-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="f6b27-185">**貨幣匯率類型**</span><span class="sxs-lookup"><span data-stu-id="f6b27-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="f6b27-186">**會計科目表**</span><span class="sxs-lookup"><span data-stu-id="f6b27-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="f6b27-187">**會計行事曆**</span><span class="sxs-lookup"><span data-stu-id="f6b27-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="f6b27-188">**總帳**</span><span class="sxs-lookup"><span data-stu-id="f6b27-188">**Ledger**</span></span>

5. <span data-ttu-id="f6b27-189">更新資訊安全角色之後，移至 **設定** > **安全** > **團隊**，並在 **當地業務負責人** 團隊檢視表中選取預設團隊。</span><span class="sxs-lookup"><span data-stu-id="f6b27-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="f6b27-190">選取 **管理角色**，並確認 **雙重寫入應用程式使用者** 安全性權限是否已套用至此團隊。</span><span class="sxs-lookup"><span data-stu-id="f6b27-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="f6b27-191">執行 Project Operations 雙重寫入對應</span><span class="sxs-lookup"><span data-stu-id="f6b27-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="f6b27-192">在 LCS 專案中，移至 **環境詳細資料** 頁面。</span><span class="sxs-lookup"><span data-stu-id="f6b27-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="f6b27-193">在 **Common Data Service 環境資訊** 底下，選取 **連結至 CDS for Apps**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="f6b27-194">選取連結之後，您會重新導向至對應中實體的清單。</span><span class="sxs-lookup"><span data-stu-id="f6b27-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="f6b27-195">依照下表所述，開始對應。</span><span class="sxs-lookup"><span data-stu-id="f6b27-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="f6b27-196">請務必遵循列示的順序進行。</span><span class="sxs-lookup"><span data-stu-id="f6b27-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="f6b27-197">**實體對應**</span><span class="sxs-lookup"><span data-stu-id="f6b27-197">**Entity Map**</span></span> | <span data-ttu-id="f6b27-198">**重新整理實體**</span><span class="sxs-lookup"><span data-stu-id="f6b27-198">**Refresh entity**</span></span> | <span data-ttu-id="f6b27-199">**初始同步**</span><span class="sxs-lookup"><span data-stu-id="f6b27-199">**Initial sync**</span></span> | <span data-ttu-id="f6b27-200">**初始同步處理的主要記錄**</span><span class="sxs-lookup"><span data-stu-id="f6b27-200">**Master for initial sync**</span></span> | <span data-ttu-id="f6b27-201">**執行先決條件**</span><span class="sxs-lookup"><span data-stu-id="f6b27-201">**Run prerequisites**</span></span> | <span data-ttu-id="f6b27-202">**先決條件初始同步**</span><span class="sxs-lookup"><span data-stu-id="f6b27-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="f6b27-203">**所有公司的專案資源角色 (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="f6b27-204">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-204">No</span></span> | <span data-ttu-id="f6b27-205">.是</span><span class="sxs-lookup"><span data-stu-id="f6b27-205">Yes</span></span> | <span data-ttu-id="f6b27-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f6b27-206">Common Data Service</span></span> | <span data-ttu-id="f6b27-207">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-207">No</span></span> | <span data-ttu-id="f6b27-208">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-208">N\A</span></span> |
| <span data-ttu-id="f6b27-209">**法律實體 (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="f6b27-210">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-210">No</span></span> | <span data-ttu-id="f6b27-211">.是</span><span class="sxs-lookup"><span data-stu-id="f6b27-211">Yes</span></span> | <span data-ttu-id="f6b27-212">Finance and Operations 應用程式</span><span class="sxs-lookup"><span data-stu-id="f6b27-212">Finance and Operations apps</span></span> | <span data-ttu-id="f6b27-213">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-213">No</span></span> | <span data-ttu-id="f6b27-214">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-214">N\A</span></span> |
| <span data-ttu-id="f6b27-215">**分類帳 (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="f6b27-216">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-216">No</span></span> | <span data-ttu-id="f6b27-217">.是</span><span class="sxs-lookup"><span data-stu-id="f6b27-217">Yes</span></span> | <span data-ttu-id="f6b27-218">Finance and Operations 應用程式</span><span class="sxs-lookup"><span data-stu-id="f6b27-218">Finance and Operations apps</span></span> | <span data-ttu-id="f6b27-219">.是</span><span class="sxs-lookup"><span data-stu-id="f6b27-219">Yes</span></span> | <span data-ttu-id="f6b27-220">是，Finance and Operations 應用程式</span><span class="sxs-lookup"><span data-stu-id="f6b27-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="f6b27-221">**Project Operations 整合實際值 (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="f6b27-222">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-222">No</span></span> | <span data-ttu-id="f6b27-223">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-223">No</span></span> | <span data-ttu-id="f6b27-224">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-224">N\A</span></span> | <span data-ttu-id="f6b27-225">.是</span><span class="sxs-lookup"><span data-stu-id="f6b27-225">Yes</span></span> | <span data-ttu-id="f6b27-226">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-226">No</span></span> |
| <span data-ttu-id="f6b27-227">**專案合約服務內容 (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="f6b27-228">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-228">No</span></span> | <span data-ttu-id="f6b27-229">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-229">No</span></span> | <span data-ttu-id="f6b27-230">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-230">N\A</span></span> | <span data-ttu-id="f6b27-231">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-231">No</span></span> | <span data-ttu-id="f6b27-232">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-232">No</span></span> |
| <span data-ttu-id="f6b27-233">**專案交易關聯的整合實體 (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="f6b27-234">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-234">No</span></span> | <span data-ttu-id="f6b27-235">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-235">No</span></span> | <span data-ttu-id="f6b27-236">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-236">N\A</span></span> | <span data-ttu-id="f6b27-237">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-237">No</span></span> | <span data-ttu-id="f6b27-238">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-238">N\A</span></span> |
| <span data-ttu-id="f6b27-239">**Project Operations 整合合約服務內容里程碑 (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="f6b27-240">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-240">No</span></span> | <span data-ttu-id="f6b27-241">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-241">No</span></span> | <span data-ttu-id="f6b27-242">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-242">N\A</span></span> | <span data-ttu-id="f6b27-243">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-243">No</span></span> | <span data-ttu-id="f6b27-244">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-244">N\A</span></span> |
| <span data-ttu-id="f6b27-245">**費用估計值的 Project Operations 整合實體 (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="f6b27-246">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-246">No</span></span> | <span data-ttu-id="f6b27-247">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-247">No</span></span> | <span data-ttu-id="f6b27-248">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-248">N\A</span></span> | <span data-ttu-id="f6b27-249">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-249">No</span></span> | <span data-ttu-id="f6b27-250">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-250">N\A</span></span> |
| <span data-ttu-id="f6b27-251">**Project Operations 整合專案費用類別匯出實體 (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="f6b27-252">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-252">No</span></span> | <span data-ttu-id="f6b27-253">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-253">No</span></span> | <span data-ttu-id="f6b27-254">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-254">N\A</span></span> | <span data-ttu-id="f6b27-255">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-255">No</span></span> | <span data-ttu-id="f6b27-256">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-256">N\A</span></span> |
| <span data-ttu-id="f6b27-257">**Project Operations 整合專案費用匯出實體 (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="f6b27-258">.是</span><span class="sxs-lookup"><span data-stu-id="f6b27-258">Yes</span></span> | <span data-ttu-id="f6b27-259">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-259">No</span></span> | <span data-ttu-id="f6b27-260">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-260">N\A</span></span> | <span data-ttu-id="f6b27-261">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-261">No</span></span> | <span data-ttu-id="f6b27-262">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-262">N\A</span></span> |
| <span data-ttu-id="f6b27-263">**時數估計值的 Project Operations 整合實體 (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="f6b27-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="f6b27-264">.是</span><span class="sxs-lookup"><span data-stu-id="f6b27-264">Yes</span></span> | <span data-ttu-id="f6b27-265">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-265">No</span></span> | <span data-ttu-id="f6b27-266">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-266">N\A</span></span> | <span data-ttu-id="f6b27-267">無</span><span class="sxs-lookup"><span data-stu-id="f6b27-267">No</span></span> | <span data-ttu-id="f6b27-268">不適用</span><span class="sxs-lookup"><span data-stu-id="f6b27-268">N\A</span></span> |


4. <span data-ttu-id="f6b27-269">若要重新整理實體，請選取對應名稱，然後選取 **重新整理實體**。</span><span class="sxs-lookup"><span data-stu-id="f6b27-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![重新整理對應](./media/20RefreshMapping.png)

5. <span data-ttu-id="f6b27-271">重新整理完成後，執行對應。</span><span class="sxs-lookup"><span data-stu-id="f6b27-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="f6b27-272">啟用下一個對應之前，請確認表格中的對應處於 **執行中** 狀態。</span><span class="sxs-lookup"><span data-stu-id="f6b27-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="f6b27-273">執行有較大量先決條件的對應可能需要一些時間。</span><span class="sxs-lookup"><span data-stu-id="f6b27-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="f6b27-274">若要執行有先決條件的對應，請啟用 **顯示相關實體對應** 切換。</span><span class="sxs-lookup"><span data-stu-id="f6b27-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="f6b27-275">如果表中指示 **先決條件初始同步** 為 **否**，請先確認所有先決條件中的 **初始同步** 旗標是否為 **關閉**，再執行此對應。</span><span class="sxs-lookup"><span data-stu-id="f6b27-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![執行對應](./media/21RunMap.png)

6. <span data-ttu-id="f6b27-277">驗證所有專案相關的對應是否為執行中狀態。</span><span class="sxs-lookup"><span data-stu-id="f6b27-277">Validate all project related maps are in the running state.</span></span>

![所有正在執行的對應](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="f6b27-279">在適用於 Project Operations 的 CDS 中套用設定資料 (選用)</span><span class="sxs-lookup"><span data-stu-id="f6b27-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="f6b27-280">如果已將示範資料套用至 Finance 環境，請參閱[在適用於 Project Operations 的 Common Data Service 中設定和套用資料](resource-apply-pro-setup-config-data.md)，以將示範資料套用於 CDS 環境。</span><span class="sxs-lookup"><span data-stu-id="f6b27-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="f6b27-281">您的 Project Operations 環境現在已佈建並設定。</span><span class="sxs-lookup"><span data-stu-id="f6b27-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]