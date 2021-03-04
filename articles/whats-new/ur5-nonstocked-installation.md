---
title: 更新 Finance 環境中的 Project Operations
description: 本主題提供有關如何在 Dynamics 365 Finance 環境中更新 Project Operations 的資訊。
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816615"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="84e74-103">更新 Finance 環境中的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="84e74-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="84e74-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="84e74-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="84e74-105">本主題提供有關如何在 Dynamics 365 Finance 環境中更新 Dynamics 365 Project Operations 的資訊。</span><span class="sxs-lookup"><span data-stu-id="84e74-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="84e74-106">將 Project Operations 更新至更新 5 (UR5) 所需的程序有三個。</span><span class="sxs-lookup"><span data-stu-id="84e74-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="84e74-107">將套件匯入預覽版專案中</span><span class="sxs-lookup"><span data-stu-id="84e74-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="84e74-108">套用更新</span><span class="sxs-lookup"><span data-stu-id="84e74-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="84e74-109">更新 Dataverse 環境</span><span class="sxs-lookup"><span data-stu-id="84e74-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="84e74-110">將套件匯入 LCS 專案中</span><span class="sxs-lookup"><span data-stu-id="84e74-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="84e74-111">以專案負責人或環境管理員身分登入 [Lifecycle Services (LCS)](https://lcs.dynamics.com/)。</span><span class="sxs-lookup"><span data-stu-id="84e74-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="84e74-112">從專案清單中選取 LCS 專案。</span><span class="sxs-lookup"><span data-stu-id="84e74-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="84e74-113">在 **專案** 頁面的 **環境** 群組中，開啟您要更新的環境。</span><span class="sxs-lookup"><span data-stu-id="84e74-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="84e74-114">確認環境是否正在執行中。</span><span class="sxs-lookup"><span data-stu-id="84e74-114">Verify that the environment is running.</span></span> <span data-ttu-id="84e74-115">如果未啟動，請啟動環境。</span><span class="sxs-lookup"><span data-stu-id="84e74-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="84e74-116">在 **可用更新** 底下的 **新版本** 區段中，選取 **檢視更新** 以尋找 10.0.15。</span><span class="sxs-lookup"><span data-stu-id="84e74-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![[檢視更新] 按鈕](media/view-update.png)

6. <span data-ttu-id="84e74-118">在 **二進位更新** 頁面上，選取 **儲存套件**。</span><span class="sxs-lookup"><span data-stu-id="84e74-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="84e74-119">在 **檢閱並儲存更新** 頁面上，選取 **儲存套件**。</span><span class="sxs-lookup"><span data-stu-id="84e74-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="84e74-120">在開啟的 **將套件儲存至資產庫** 窗格中，輸入套件名稱，然後選取 **儲存套件**。</span><span class="sxs-lookup"><span data-stu-id="84e74-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="84e74-121">當 LCS 儲存套件完畢後，就會啟用 **完成** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="84e74-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="84e74-122">選取 **完成**。</span><span class="sxs-lookup"><span data-stu-id="84e74-122">Select **Done**.</span></span> <span data-ttu-id="84e74-123">LCS 將會驗證套件。</span><span class="sxs-lookup"><span data-stu-id="84e74-123">LCS will verify the package.</span></span> <span data-ttu-id="84e74-124">驗證可能需要幾分鐘或長達一小時。</span><span class="sxs-lookup"><span data-stu-id="84e74-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="84e74-125">套用套件更新</span><span class="sxs-lookup"><span data-stu-id="84e74-125">Apply the package update</span></span>

1. <span data-ttu-id="84e74-126">在 LCS 的 **環境詳細資料** 頁面上，選取 **維護** > **套用更新**。</span><span class="sxs-lookup"><span data-stu-id="84e74-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="84e74-127">從清單中選取先前儲存的套件，然後選取 **套用**。</span><span class="sxs-lookup"><span data-stu-id="84e74-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="84e74-128">選取 **是** 確認您要部署套件。</span><span class="sxs-lookup"><span data-stu-id="84e74-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![確認套件部署對話方塊](media/confirm-package-deployment.png)

4. <span data-ttu-id="84e74-130">選取 **是** 確認您要更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="84e74-130">Select **Yes** to confirm that you want to update the application.</span></span>

![確認應用程式更新對話方塊](media/confirm-application-update.png)

<span data-ttu-id="84e74-132">部署和應用程式更新將會開始。</span><span class="sxs-lookup"><span data-stu-id="84e74-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="84e74-133">在 **環境詳細資料** 頁面的右上角，環境狀態將會更新為 **服務中**。</span><span class="sxs-lookup"><span data-stu-id="84e74-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="84e74-134">更新大約會在 2 小時後完成。</span><span class="sxs-lookup"><span data-stu-id="84e74-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="84e74-135">應用程式版本資訊將會更新為 **Microsoft Dynamics 365 for Finance and Operations 10.0.15**，而環境狀態則更新為 **已部署**。</span><span class="sxs-lookup"><span data-stu-id="84e74-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="84e74-136">更新 Dataverse 環境</span><span class="sxs-lookup"><span data-stu-id="84e74-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="84e74-137">登入 [Power Platform 系統管理中心](https://admin.powerplatform.com/)。</span><span class="sxs-lookup"><span data-stu-id="84e74-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="84e74-138">在 清單中，尋找並開啟您用來安裝 Project Operations 的環境。</span><span class="sxs-lookup"><span data-stu-id="84e74-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="84e74-139">在 **環境** 頁面上，選取 **資源** > **Dynamics 365 應用程式**。</span><span class="sxs-lookup"><span data-stu-id="84e74-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="84e74-140">在清單中，找出 **Microsoft Dynamics 365 Project Operations**，然後選取 **狀態** 欄中的 **可用的更新**。</span><span class="sxs-lookup"><span data-stu-id="84e74-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="84e74-141">選取 **我同意服務條款** 核取方塊，然後選取 **更新**。</span><span class="sxs-lookup"><span data-stu-id="84e74-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="84e74-142">將會安裝最新版本的解決方案。</span><span class="sxs-lookup"><span data-stu-id="84e74-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="84e74-143">安裝完成後，您已安裝版本 4.5.0.134。</span><span class="sxs-lookup"><span data-stu-id="84e74-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="84e74-144">設定新功能</span><span class="sxs-lookup"><span data-stu-id="84e74-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="84e74-145">啟用雙重寫入對應</span><span class="sxs-lookup"><span data-stu-id="84e74-145">Enable dual-write mapping</span></span>

<span data-ttu-id="84e74-146">在 Finance 和 Dataverse 環境上完成更新後，您可以啟用必要的雙重寫入對應。</span><span class="sxs-lookup"><span data-stu-id="84e74-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="84e74-147">完成下列程序以啟用雙重寫入對應。</span><span class="sxs-lookup"><span data-stu-id="84e74-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="84e74-148">更新 Customer Engagement 環境的安全性設定</span><span class="sxs-lookup"><span data-stu-id="84e74-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="84e74-149">重新整理資料實體</span><span class="sxs-lookup"><span data-stu-id="84e74-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="84e74-150">更新並執行雙重寫入對應</span><span class="sxs-lookup"><span data-stu-id="84e74-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="84e74-151">更新 Dataverse 環境的安全性設定</span><span class="sxs-lookup"><span data-stu-id="84e74-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="84e74-152">在 UR5 的更新中需要對實體的安全性權限進行下列更新。</span><span class="sxs-lookup"><span data-stu-id="84e74-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="84e74-153">在 Dataverse 環境中，移至 **設定**，然後在 **系統** 群組中選取 **安全性**。</span><span class="sxs-lookup"><span data-stu-id="84e74-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse 環境設定](media/Picture21.png)

2. <span data-ttu-id="84e74-155">選取 **資訊安全角色**。</span><span class="sxs-lookup"><span data-stu-id="84e74-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="84e74-156">從角色清單中選取 **雙重寫入應用程式使用者**，然後選取 **自訂實體** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="84e74-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="84e74-157">確認角色是否對下列各項具有 **讀取** 和 **附加至** 權限：</span><span class="sxs-lookup"><span data-stu-id="84e74-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="84e74-158">**貨幣匯率類型**</span><span class="sxs-lookup"><span data-stu-id="84e74-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="84e74-159">**會計科目表**</span><span class="sxs-lookup"><span data-stu-id="84e74-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="84e74-160">**會計行事曆**</span><span class="sxs-lookup"><span data-stu-id="84e74-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="84e74-161">**總帳**</span><span class="sxs-lookup"><span data-stu-id="84e74-161">**Ledger**</span></span>

5. <span data-ttu-id="84e74-162">更新資訊安全角色之後，移至 **設定** > **安全** > **團隊**。</span><span class="sxs-lookup"><span data-stu-id="84e74-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="84e74-163">確認 **雙重寫入應用程式使用者** 角色是否已套用至團隊。</span><span class="sxs-lookup"><span data-stu-id="84e74-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="84e74-164">從更新中重新整理資料實體</span><span class="sxs-lookup"><span data-stu-id="84e74-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="84e74-165">在 Finance 環境中，開啟 **資料管理** 工作區，然後開啟 **架構參數** 頁面。</span><span class="sxs-lookup"><span data-stu-id="84e74-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="84e74-166">在 **實體設定** 索引標籤上，選取 **重新整理實體清單**。</span><span class="sxs-lookup"><span data-stu-id="84e74-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="84e74-167">選取 **關閉** 以確認實體重新整理。</span><span class="sxs-lookup"><span data-stu-id="84e74-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="84e74-168">此程序需要約 20 分鐘才能完成。</span><span class="sxs-lookup"><span data-stu-id="84e74-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="84e74-169">重新整理完成時，系統會通知您。</span><span class="sxs-lookup"><span data-stu-id="84e74-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="84e74-170">更新雙重寫入對應</span><span class="sxs-lookup"><span data-stu-id="84e74-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="84e74-171">在 **資料管理** 工作區中，選取 **雙重寫入**。</span><span class="sxs-lookup"><span data-stu-id="84e74-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="84e74-172">選取 **套用解決方案**、在清單中選取這兩個解決方案，然後選取 **套用**。</span><span class="sxs-lookup"><span data-stu-id="84e74-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="84e74-173">在 **雙重寫入** 頁面上，選取下列資料表對應，然後選取 **停止**。</span><span class="sxs-lookup"><span data-stu-id="84e74-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="84e74-174">**Project Operations 整合實際值 (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="84e74-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="84e74-175">**Project Operations 整合專案費用類別 (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="84e74-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="84e74-176">**Project Operations 整合實際值專案費用匯出實體 (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="84e74-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="84e74-177">在 **資料表對應版本** 頁面上，將新的對應版本套用至三個實體中的每一個。</span><span class="sxs-lookup"><span data-stu-id="84e74-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="84e74-178">在 **雙重寫入** 頁面上，選取 [執行] 以重新啟動對應。</span><span class="sxs-lookup"><span data-stu-id="84e74-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="84e74-179">從對應清單中選取與所有先決條件的 **總帳 (msdyn_ledgers)** 對應，然後選取 **初始同步** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="84e74-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="84e74-180">在 **初始同步主機** 欄位中，選取 **Finance and Operations 應用程式**，然後選取 **執行**。</span><span class="sxs-lookup"><span data-stu-id="84e74-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![總帳對應同步處理](media/DW6.png)
 
