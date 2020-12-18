---
title: 在 Common Data Service 中設定和套用設定資料
description: 本主題提供有關在 Project Operations 中設定和套用示範設定的資訊。
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642218"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="e3667-103">在 Common Data Service 中設定和套用設定資料</span><span class="sxs-lookup"><span data-stu-id="e3667-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="e3667-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="e3667-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="e3667-105">先決條件</span><span class="sxs-lookup"><span data-stu-id="e3667-105">Prerequisites</span></span>

<span data-ttu-id="e3667-106">在您開始在 Common Data Service (CDS) 中設定資料之前，必須符合下列先決條件：</span><span class="sxs-lookup"><span data-stu-id="e3667-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="e3667-107">為 Project Operations 設定 CDS 環境以及 Dynamics 365 Finance 環境。</span><span class="sxs-lookup"><span data-stu-id="e3667-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="e3667-108">來自 Dynamics 365 Finance 環境的法律實體已與 CDS 環境共用。</span><span class="sxs-lookup"><span data-stu-id="e3667-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="e3667-109">這表示 CDS 中的 **公司** 實體有下列公司記錄：</span><span class="sxs-lookup"><span data-stu-id="e3667-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="e3667-110">THPM</span><span class="sxs-lookup"><span data-stu-id="e3667-110">THPM</span></span>
  - <span data-ttu-id="e3667-111">USPM</span><span class="sxs-lookup"><span data-stu-id="e3667-111">USPM</span></span>
  - <span data-ttu-id="e3667-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="e3667-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="e3667-113">安裝設定和設定資料</span><span class="sxs-lookup"><span data-stu-id="e3667-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="e3667-114">下載、解除封鎖和解壓縮[設定和設定資料套件](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)。</span><span class="sxs-lookup"><span data-stu-id="e3667-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="e3667-115">瀏覽至解壓縮後的資料夾，並執行可執行檔 *DataMigrationUtility*。</span><span class="sxs-lookup"><span data-stu-id="e3667-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e3667-116">在 Common Data Service 設定移轉 (CMT) 精靈的第 1 頁中，選取 **匯入資料**，然後選取 **繼續**。</span><span class="sxs-lookup"><span data-stu-id="e3667-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![設定移轉](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e3667-118">在 CMT 精靈的第 2 頁中，選取 **Microsoft 365** 做為 **部署類型**。</span><span class="sxs-lookup"><span data-stu-id="e3667-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e3667-119">選取 **顯示可用組織的清單** 和 **顯示進階** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="e3667-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e3667-120">選取您的租用戶所在地區、輸入您的認證，然後選取 **登入**。</span><span class="sxs-lookup"><span data-stu-id="e3667-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![設定登入](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e3667-122">在第 3 頁中，從租用戶的組織清單中，選取要將示範資料匯入到的組織，然後選取 **登入**。</span><span class="sxs-lookup"><span data-stu-id="e3667-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="e3667-123">在第 4 頁中，從解壓縮後的資料夾中選取 ZIP 檔案 *SampleSetupAndConfigData*。</span><span class="sxs-lookup"><span data-stu-id="e3667-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![ZIP 檔案選取](./media/3ZipFile.png)

![選擇檔案](./media/4SelectAFile.png)

9. <span data-ttu-id="e3667-126">選取 ZIP 檔案之後，選取 **匯入資料**。</span><span class="sxs-lookup"><span data-stu-id="e3667-126">After the zip file is selected, select **Import Data**.</span></span>

![匯入資料​​](./media/5ImportData.png)

10. <span data-ttu-id="e3667-128">視您的網路速度而定，匯入將會執行約二至十分鐘。</span><span class="sxs-lookup"><span data-stu-id="e3667-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e3667-129">匯入完成後，結束 CMT 精靈。</span><span class="sxs-lookup"><span data-stu-id="e3667-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e3667-130">檢查您的組織中是否有下列 19 個實體的資料：</span><span class="sxs-lookup"><span data-stu-id="e3667-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="e3667-131">貨幣</span><span class="sxs-lookup"><span data-stu-id="e3667-131">Currency</span></span>
  - <span data-ttu-id="e3667-132">組織單位</span><span class="sxs-lookup"><span data-stu-id="e3667-132">Organizational Unit</span></span>
  - <span data-ttu-id="e3667-133">連絡人</span><span class="sxs-lookup"><span data-stu-id="e3667-133">Contact</span></span>
  - <span data-ttu-id="e3667-134">課稅群組</span><span class="sxs-lookup"><span data-stu-id="e3667-134">Tax Group</span></span>
  - <span data-ttu-id="e3667-135">客戶群組</span><span class="sxs-lookup"><span data-stu-id="e3667-135">Customer Group</span></span>
  - <span data-ttu-id="e3667-136">單位</span><span class="sxs-lookup"><span data-stu-id="e3667-136">Unit</span></span>
  - <span data-ttu-id="e3667-137">單位群組</span><span class="sxs-lookup"><span data-stu-id="e3667-137">Unit Group</span></span>
  - <span data-ttu-id="e3667-138">價目表</span><span class="sxs-lookup"><span data-stu-id="e3667-138">Price List</span></span>
  - <span data-ttu-id="e3667-139">專案參數價目表</span><span class="sxs-lookup"><span data-stu-id="e3667-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="e3667-140">發票頻率</span><span class="sxs-lookup"><span data-stu-id="e3667-140">Invoice Frequency</span></span>
  - <span data-ttu-id="e3667-141">可預約資源類別</span><span class="sxs-lookup"><span data-stu-id="e3667-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="e3667-142">交易類別</span><span class="sxs-lookup"><span data-stu-id="e3667-142">Transaction Category</span></span>
  - <span data-ttu-id="e3667-143">費用類別</span><span class="sxs-lookup"><span data-stu-id="e3667-143">Expense Category</span></span>
  - <span data-ttu-id="e3667-144">角色價格</span><span class="sxs-lookup"><span data-stu-id="e3667-144">Role Price</span></span>
  - <span data-ttu-id="e3667-145">交易類別價格</span><span class="sxs-lookup"><span data-stu-id="e3667-145">Transaction Category Price</span></span>
  - <span data-ttu-id="e3667-146">特性</span><span class="sxs-lookup"><span data-stu-id="e3667-146">Characteristic</span></span>
  - <span data-ttu-id="e3667-147">可預約資源</span><span class="sxs-lookup"><span data-stu-id="e3667-147">Bookable Resource</span></span>
  - <span data-ttu-id="e3667-148">可預約資源類別關聯</span><span class="sxs-lookup"><span data-stu-id="e3667-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="e3667-149">可預約資源特性</span><span class="sxs-lookup"><span data-stu-id="e3667-149">Bookable Resource Characteristic</span></span>

![完成匯入](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="e3667-151">更新 Project Operations 設定</span><span class="sxs-lookup"><span data-stu-id="e3667-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="e3667-152">瀏覽至 CE 環境。</span><span class="sxs-lookup"><span data-stu-id="e3667-152">Navigate to the CE environment.</span></span> <span data-ttu-id="e3667-153">您可以開啟 [Power Platform 系統管理中心](https://admin.powerplatform.microsoft.com/environments)、選取環境，然後選取 **開啟環境** 來尋找它。</span><span class="sxs-lookup"><span data-stu-id="e3667-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![開啟環境](./media/7OpenEnvironment.png)

2. <span data-ttu-id="e3667-155">移至 **專案** > **資源**，然後選取 **新增**，為您的使用者建立可預約資源。</span><span class="sxs-lookup"><span data-stu-id="e3667-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![可預約資源](./media/8BookableResources.png)

3. <span data-ttu-id="e3667-157">在 **一般** 索引標籤上，選取您的管理使用者。</span><span class="sxs-lookup"><span data-stu-id="e3667-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="e3667-158">確認時區是否與您所在的時區相符。</span><span class="sxs-lookup"><span data-stu-id="e3667-158">Verify that the time zone matches the one you are in.</span></span> 

![新的可預約資源](./media/9NewBookableResource.png)

4. <span data-ttu-id="e3667-160">在 **排程** 索引標籤的 **公司** 欄位中，選取 **USPM** 公司，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="e3667-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![[排程] 索引標籤](./media/10SchedulingTab.png)

5. <span data-ttu-id="e3667-162">選取 **工作時數** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="e3667-162">Select the **Work hours** tab.</span></span>  

![工作時數](./media/11WorkHours.png)

6. <span data-ttu-id="e3667-164">按兩下行事曆中的任何值，然後選取 **編輯** > **系列中的所有事件**。</span><span class="sxs-lookup"><span data-stu-id="e3667-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![工作行事曆](./media/12WorkCalendar.png)

7. <span data-ttu-id="e3667-166">將工作時數變更為八 (8) 小時工作日、將週末標示為非工作日，並確定時區與您的時區相符。</span><span class="sxs-lookup"><span data-stu-id="e3667-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="e3667-167">選取 **儲存後關閉**。</span><span class="sxs-lookup"><span data-stu-id="e3667-167">Select **Save and close**.</span></span>

![更新行事曆](./media/13UpdateCalendar.png)

9. <span data-ttu-id="e3667-169">移至 **設定** > **行事曆範本**，並選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="e3667-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![行事曆範本](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="e3667-171">輸入名稱、選取您所建立的範本資源，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="e3667-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![儲存行事曆範本](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="e3667-173">移至 **參數**，並按兩下該記錄。</span><span class="sxs-lookup"><span data-stu-id="e3667-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![專案參數](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="e3667-175">更新下列欄位：</span><span class="sxs-lookup"><span data-stu-id="e3667-175">Update the following fields:</span></span>

 - <span data-ttu-id="e3667-176">**預設公司**：USPM</span><span class="sxs-lookup"><span data-stu-id="e3667-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="e3667-177">**預設組織單位**：Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="e3667-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="e3667-178">**發票週期**：每月第七天和最後一天</span><span class="sxs-lookup"><span data-stu-id="e3667-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="e3667-179">**工作時數範本**：變更為您所建立的範本。</span><span class="sxs-lookup"><span data-stu-id="e3667-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="e3667-180">選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="e3667-180">Select **Save**.</span></span> 

![更新專案參數](./media/17UpdatedProjectParameters.png)
