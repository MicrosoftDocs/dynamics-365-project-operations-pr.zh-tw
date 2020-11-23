---
title: 套用示範設定和設定資料 - 精簡
description: 本主題提供有關如何套用 Project Operations 示範設定和設定資料的資訊。
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401253"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="7d371-103">套用 Project Operations 的示範設定和設定資料 - 精簡</span><span class="sxs-lookup"><span data-stu-id="7d371-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="7d371-104">_\*\*精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="7d371-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7d371-105">先決條件</span><span class="sxs-lookup"><span data-stu-id="7d371-105">Prerequisites</span></span>

<span data-ttu-id="7d371-106">開始設定之前，您必須已為 Dynamics 365 Project Operations 佈建 Common Data Service (CDS) 環境。</span><span class="sxs-lookup"><span data-stu-id="7d371-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="7d371-107">指示</span><span class="sxs-lookup"><span data-stu-id="7d371-107">Instructions</span></span>

1. <span data-ttu-id="7d371-108">下載[主要資料套件](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip)。</span><span class="sxs-lookup"><span data-stu-id="7d371-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="7d371-109">瀏覽至資料夾 *ProjOpsDemoDataSetupAndMaster - Integrated CMT*，並執行可執行檔 *DataMigrationUtility*。</span><span class="sxs-lookup"><span data-stu-id="7d371-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="7d371-110">在 Common Data Service 設定移轉 (CMT) 精靈的第 1 頁中，選取 **匯入資料**，然後選取 **繼續**。</span><span class="sxs-lookup"><span data-stu-id="7d371-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![設定移轉](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="7d371-112">在 CMT 精靈的第 2 頁中，選取 **Microsoft 365** 做為 **部署類型**。</span><span class="sxs-lookup"><span data-stu-id="7d371-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="7d371-113">選取 **顯示可用組織的清單** 和 **顯示進階** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="7d371-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="7d371-114">選取您的租用戶所在地區、輸入您的認證，然後選取 **登入**。</span><span class="sxs-lookup"><span data-stu-id="7d371-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![設定登入](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="7d371-116">在第 3 頁中，從租用戶的組織清單中，選取要將示範資料匯入到的組織，然後選取 **登入**。</span><span class="sxs-lookup"><span data-stu-id="7d371-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="7d371-117">在第 4 頁中，從解壓縮後的資料夾 *ProjOpsDemoDataSetupAndMaster - Integrated CMT* 中選取 ZIP 檔案 *MasterAndSetupData*。</span><span class="sxs-lookup"><span data-stu-id="7d371-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ZIP 檔案](./media/3ZipFile.png)

![選擇檔案](./media/4SelectAFile.png)

9. <span data-ttu-id="7d371-120">選取 ZIP 檔案之後，選取 **匯入資料**。</span><span class="sxs-lookup"><span data-stu-id="7d371-120">After the zip file is selected, select **Import Data**.</span></span>

![匯入資料](./media/5ImportData.png)

10. <span data-ttu-id="7d371-122">視您的網路速度而定，匯入將會執行約二至十分鐘。</span><span class="sxs-lookup"><span data-stu-id="7d371-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="7d371-123">完成後，結束 CMT 精靈。</span><span class="sxs-lookup"><span data-stu-id="7d371-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="7d371-124">檢查您的組織中是否有下列 20 個實體的資料：</span><span class="sxs-lookup"><span data-stu-id="7d371-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="7d371-125">貨幣</span><span class="sxs-lookup"><span data-stu-id="7d371-125">Currency</span></span>
-   <span data-ttu-id="7d371-126">帳戶</span><span class="sxs-lookup"><span data-stu-id="7d371-126">Account</span></span>
-   <span data-ttu-id="7d371-127">組織單位</span><span class="sxs-lookup"><span data-stu-id="7d371-127">Organizational Unit</span></span>
-   <span data-ttu-id="7d371-128">連絡人</span><span class="sxs-lookup"><span data-stu-id="7d371-128">Contact</span></span>
-   <span data-ttu-id="7d371-129">課稅群組</span><span class="sxs-lookup"><span data-stu-id="7d371-129">Tax Group</span></span>
-   <span data-ttu-id="7d371-130">客戶群組</span><span class="sxs-lookup"><span data-stu-id="7d371-130">Customer Group</span></span>
-   <span data-ttu-id="7d371-131">單位</span><span class="sxs-lookup"><span data-stu-id="7d371-131">Unit</span></span>
-   <span data-ttu-id="7d371-132">單位群組</span><span class="sxs-lookup"><span data-stu-id="7d371-132">Unit Group</span></span>
-   <span data-ttu-id="7d371-133">價目表</span><span class="sxs-lookup"><span data-stu-id="7d371-133">Price List</span></span>
-   <span data-ttu-id="7d371-134">專案參數價目表</span><span class="sxs-lookup"><span data-stu-id="7d371-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="7d371-135">發票頻率</span><span class="sxs-lookup"><span data-stu-id="7d371-135">Invoice Frequency</span></span>
-   <span data-ttu-id="7d371-136">可預約資源類別</span><span class="sxs-lookup"><span data-stu-id="7d371-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="7d371-137">交易類別</span><span class="sxs-lookup"><span data-stu-id="7d371-137">Transaction Category</span></span>
-   <span data-ttu-id="7d371-138">費用類別</span><span class="sxs-lookup"><span data-stu-id="7d371-138">Expense Category</span></span>
-   <span data-ttu-id="7d371-139">角色價格</span><span class="sxs-lookup"><span data-stu-id="7d371-139">Role Price</span></span>
-   <span data-ttu-id="7d371-140">交易類別價格</span><span class="sxs-lookup"><span data-stu-id="7d371-140">Transaction Category Price</span></span>
-   <span data-ttu-id="7d371-141">特性</span><span class="sxs-lookup"><span data-stu-id="7d371-141">Characteristic</span></span>
-   <span data-ttu-id="7d371-142">可預約資源</span><span class="sxs-lookup"><span data-stu-id="7d371-142">Bookable Resource</span></span>
-   <span data-ttu-id="7d371-143">可預約資源類別關聯</span><span class="sxs-lookup"><span data-stu-id="7d371-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="7d371-144">可預約資源特性</span><span class="sxs-lookup"><span data-stu-id="7d371-144">Bookable Resource Characteristic</span></span>

![匯入完成](./media/6CompleteImport.png)
