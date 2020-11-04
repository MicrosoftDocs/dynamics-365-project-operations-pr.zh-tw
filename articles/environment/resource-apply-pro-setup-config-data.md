---
title: 設定和套用 Project Operations 適用 Common Data Service 中的設定資料
description: 本主題提供有關在 Project Operations 中設定和套用示範設定的資訊。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072869"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="b9665-103">設定和套用 Project Operations 適用 Common Data Service 中的設定資料</span><span class="sxs-lookup"><span data-stu-id="b9665-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="b9665-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="b9665-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="b9665-105">安裝設定和設定資料</span><span class="sxs-lookup"><span data-stu-id="b9665-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="b9665-106">下載、解除封鎖和解壓縮[設定和設定資料套件](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)。</span><span class="sxs-lookup"><span data-stu-id="b9665-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="b9665-107">瀏覽至解壓縮後的資料夾，並執行可執行檔 *DataMigrationUtility* 。</span><span class="sxs-lookup"><span data-stu-id="b9665-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="b9665-108">在 Common Data Service 設定移轉 (CMT) 精靈的第 1 頁中，選取 **匯入資料** ，然後選取 **繼續** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![設定移轉](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="b9665-110">在 CMT 精靈的第 2 頁中，選取 **Microsoft 365** 做為 **部署類型** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="b9665-111">選取 **顯示可用組織的清單** 和 **顯示進階** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="b9665-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="b9665-112">選取您的租用戶所在地區、輸入您的認證，然後選取 **登入** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![設定登入](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="b9665-114">在第 3 頁中，從租用戶的組織清單中，選取要將示範資料匯入到的組織，然後選取 **登入** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="b9665-115">在第 4 頁中，從解壓縮後的資料夾中選取 ZIP 檔案 *SampleSetupAndConfigData* 。</span><span class="sxs-lookup"><span data-stu-id="b9665-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![ZIP 檔案選取](./media/3ZipFile.png)

![選擇檔案](./media/4SelectAFile.png)

9. <span data-ttu-id="b9665-118">選取 ZIP 檔案之後，選取 **匯入資料** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-118">After the zip file is selected, select **Import Data**.</span></span>

![匯入資料​​](./media/5ImportData.png)

10. <span data-ttu-id="b9665-120">視您的網路速度而定，匯入將會執行約二至十分鐘。</span><span class="sxs-lookup"><span data-stu-id="b9665-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="b9665-121">匯入完成後，結束 CMT 精靈。</span><span class="sxs-lookup"><span data-stu-id="b9665-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="b9665-122">檢查您的組織中是否有下列 19 個實體的資料：</span><span class="sxs-lookup"><span data-stu-id="b9665-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="b9665-123">貨幣</span><span class="sxs-lookup"><span data-stu-id="b9665-123">Currency</span></span>
  - <span data-ttu-id="b9665-124">組織單位</span><span class="sxs-lookup"><span data-stu-id="b9665-124">Organizational Unit</span></span>
  - <span data-ttu-id="b9665-125">連絡人</span><span class="sxs-lookup"><span data-stu-id="b9665-125">Contact</span></span>
  - <span data-ttu-id="b9665-126">課稅群組</span><span class="sxs-lookup"><span data-stu-id="b9665-126">Tax Group</span></span>
  - <span data-ttu-id="b9665-127">客戶群組</span><span class="sxs-lookup"><span data-stu-id="b9665-127">Customer Group</span></span>
  - <span data-ttu-id="b9665-128">單位</span><span class="sxs-lookup"><span data-stu-id="b9665-128">Unit</span></span>
  - <span data-ttu-id="b9665-129">單位群組</span><span class="sxs-lookup"><span data-stu-id="b9665-129">Unit Group</span></span>
  - <span data-ttu-id="b9665-130">價目表</span><span class="sxs-lookup"><span data-stu-id="b9665-130">Price List</span></span>
  - <span data-ttu-id="b9665-131">專案參數價目表</span><span class="sxs-lookup"><span data-stu-id="b9665-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="b9665-132">發票頻率</span><span class="sxs-lookup"><span data-stu-id="b9665-132">Invoice Frequency</span></span>
  - <span data-ttu-id="b9665-133">可預約資源類別</span><span class="sxs-lookup"><span data-stu-id="b9665-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="b9665-134">交易類別</span><span class="sxs-lookup"><span data-stu-id="b9665-134">Transaction Category</span></span>
  - <span data-ttu-id="b9665-135">費用類別</span><span class="sxs-lookup"><span data-stu-id="b9665-135">Expense Category</span></span>
  - <span data-ttu-id="b9665-136">角色價格</span><span class="sxs-lookup"><span data-stu-id="b9665-136">Role Price</span></span>
  - <span data-ttu-id="b9665-137">交易類別價格</span><span class="sxs-lookup"><span data-stu-id="b9665-137">Transaction Category Price</span></span>
  - <span data-ttu-id="b9665-138">特性</span><span class="sxs-lookup"><span data-stu-id="b9665-138">Characteristic</span></span>
  - <span data-ttu-id="b9665-139">可預約資源</span><span class="sxs-lookup"><span data-stu-id="b9665-139">Bookable Resource</span></span>
  - <span data-ttu-id="b9665-140">可預約資源類別關聯</span><span class="sxs-lookup"><span data-stu-id="b9665-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="b9665-141">可預約資源特性</span><span class="sxs-lookup"><span data-stu-id="b9665-141">Bookable Resource Characteristic</span></span>

![完成匯入](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="b9665-143">更新 Project Operations 設定</span><span class="sxs-lookup"><span data-stu-id="b9665-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="b9665-144">瀏覽至 CE 環境。</span><span class="sxs-lookup"><span data-stu-id="b9665-144">Navigate to the CE environment.</span></span> <span data-ttu-id="b9665-145">您可以開啟 [Power Platform 系統管理中心](https://admin.powerplatform.microsoft.com/environments)、選取環境，然後選取 **開啟環境** 來尋找它。</span><span class="sxs-lookup"><span data-stu-id="b9665-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![開啟環境](./media/7OpenEnvironment.png)

2. <span data-ttu-id="b9665-147">移至 **專案** > **資源** ，然後選取 **新增** ，為您的使用者建立可預約資源。</span><span class="sxs-lookup"><span data-stu-id="b9665-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![可預約資源](./media/8BookableResources.png)

3. <span data-ttu-id="b9665-149">在 **一般** 索引標籤上，選取您的管理使用者。</span><span class="sxs-lookup"><span data-stu-id="b9665-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="b9665-150">確認時區是否與您所在的時區相符。</span><span class="sxs-lookup"><span data-stu-id="b9665-150">Verify that the time zone matches the one you are in.</span></span> 

![新的可預約資源](./media/9NewBookableResource.png)

4. <span data-ttu-id="b9665-152">在 **排程** 索引標籤的 **公司** 欄位中，選取 **USPM** 公司，然後選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![[排程] 索引標籤](./media/10SchedulingTab.png)

5. <span data-ttu-id="b9665-154">選取 **工作時數** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="b9665-154">Select the **Work hours** tab.</span></span>  

![工作時數](./media/11WorkHours.png)

6. <span data-ttu-id="b9665-156">按兩下行事曆中的任何值，然後選取 **編輯** > **系列中的所有事件** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![工作行事曆](./media/12WorkCalendar.png)

7. <span data-ttu-id="b9665-158">將工作時數變更為八 (8) 小時工作日、將週末標示為非工作日，並確定時區與您的時區相符。</span><span class="sxs-lookup"><span data-stu-id="b9665-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="b9665-159">選取 **儲存後關閉** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-159">Select **Save and close**.</span></span>

![更新行事曆](./media/13UpdateCalendar.png)

9. <span data-ttu-id="b9665-161">移至 **設定** > **行事曆範本** ，並選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![行事曆範本](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="b9665-163">輸入名稱、選取您所建立的範本資源，然後選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![儲存行事曆範本](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="b9665-165">移至 **參數** ，並按兩下該記錄。</span><span class="sxs-lookup"><span data-stu-id="b9665-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![專案參數](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="b9665-167">更新下列欄位：</span><span class="sxs-lookup"><span data-stu-id="b9665-167">Update the following fields:</span></span>

 - <span data-ttu-id="b9665-168">**預設公司** ：USPM</span><span class="sxs-lookup"><span data-stu-id="b9665-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="b9665-169">**預設組織單位** ：Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="b9665-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="b9665-170">**發票週期** ：每月第七天和最後一天</span><span class="sxs-lookup"><span data-stu-id="b9665-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="b9665-171">**工作時數範本** ：變更為您所建立的範本。</span><span class="sxs-lookup"><span data-stu-id="b9665-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="b9665-172">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="b9665-172">Select **Save**.</span></span> 

![更新專案參數](./media/17UpdatedProjectParameters.png)
