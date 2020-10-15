---
title: 套用示範設定和設定資料
description: 本主題提供有關如何套用 Project Operations 示範設定和設定資料的資訊。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948777"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="9e365-103">套用「Project Operations Lite 部署 – 交易至開立預估發票」的示範設定和設定資料</span><span class="sxs-lookup"><span data-stu-id="9e365-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="9e365-104">_\*\*精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="9e365-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="9e365-105">下載[主要資料套件](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip)。</span><span class="sxs-lookup"><span data-stu-id="9e365-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="9e365-106">瀏覽至資料夾 *ProjOpsDemoDataSetupAndMaster - Integrated CMT*，並執行可執行檔 *DataMigrationUtility*。</span><span class="sxs-lookup"><span data-stu-id="9e365-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="9e365-107">在 Common Data Service 設定移轉 (CMT) 精靈的第 1 頁中，選取**匯入資料**，然後選取**繼續**。</span><span class="sxs-lookup"><span data-stu-id="9e365-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![設定移轉](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="9e365-109">在 CMT 精靈的第 2 頁中，選取 **Office 365** 做為**部署類型**。</span><span class="sxs-lookup"><span data-stu-id="9e365-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="9e365-110">選取**顯示可用組織的清單**和**顯示進階**核取方塊。</span><span class="sxs-lookup"><span data-stu-id="9e365-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="9e365-111">選取您的租用戶所在地區、輸入您的認證，然後選取**登入**。</span><span class="sxs-lookup"><span data-stu-id="9e365-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![設定登入](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="9e365-113">在第 3 頁中，從租用戶的組織清單中，選取要將示範資料匯入到的組織，然後選取**登入**。</span><span class="sxs-lookup"><span data-stu-id="9e365-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="9e365-114">在第 4 頁中，從解壓縮後的資料夾 *ProjOpsDemoDataSetupAndMaster - Integrated CMT* 中選取 ZIP 檔案 *MasterAndSetupData*。</span><span class="sxs-lookup"><span data-stu-id="9e365-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ZIP 檔案](./media/3ZipFile.png)

![選擇檔案](./media/4SelectAFile.png)

9. <span data-ttu-id="9e365-117">選取 ZIP 檔案之後，選取**匯入資料**。</span><span class="sxs-lookup"><span data-stu-id="9e365-117">After the zip file is selected, select **Import Data**.</span></span>

![匯入資料](./media/5ImportData.png)

10. <span data-ttu-id="9e365-119">視您的網路速度而定，匯入將會執行約二至十分鐘。</span><span class="sxs-lookup"><span data-stu-id="9e365-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="9e365-120">完成後，結束 CMT 精靈。</span><span class="sxs-lookup"><span data-stu-id="9e365-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="9e365-121">檢查您的組織中是否有下列 20 個實體的資料：</span><span class="sxs-lookup"><span data-stu-id="9e365-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="9e365-122">貨幣</span><span class="sxs-lookup"><span data-stu-id="9e365-122">Currency</span></span>
- <span data-ttu-id="9e365-123">組織單位</span><span class="sxs-lookup"><span data-stu-id="9e365-123">Organizational Unit</span></span>
- <span data-ttu-id="9e365-124">連絡人</span><span class="sxs-lookup"><span data-stu-id="9e365-124">Contact</span></span>
- <span data-ttu-id="9e365-125">課稅群組</span><span class="sxs-lookup"><span data-stu-id="9e365-125">Tax Group</span></span>
- <span data-ttu-id="9e365-126">客戶群組</span><span class="sxs-lookup"><span data-stu-id="9e365-126">Customer Group</span></span>
- <span data-ttu-id="9e365-127">單位</span><span class="sxs-lookup"><span data-stu-id="9e365-127">Unit</span></span>
- <span data-ttu-id="9e365-128">單位群組</span><span class="sxs-lookup"><span data-stu-id="9e365-128">Unit Group</span></span>
- <span data-ttu-id="9e365-129">價目表</span><span class="sxs-lookup"><span data-stu-id="9e365-129">Price List</span></span>
- <span data-ttu-id="9e365-130">專案參數價目表</span><span class="sxs-lookup"><span data-stu-id="9e365-130">Project Parameter Price List</span></span>
- <span data-ttu-id="9e365-131">發票頻率</span><span class="sxs-lookup"><span data-stu-id="9e365-131">Invoice Frequency</span></span>
- <span data-ttu-id="9e365-132">發票週期詳細資料</span><span class="sxs-lookup"><span data-stu-id="9e365-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="9e365-133">可預約資源類別</span><span class="sxs-lookup"><span data-stu-id="9e365-133">Bookable Resource Category</span></span>
- <span data-ttu-id="9e365-134">交易類別</span><span class="sxs-lookup"><span data-stu-id="9e365-134">Transaction Category</span></span>
- <span data-ttu-id="9e365-135">費用類別</span><span class="sxs-lookup"><span data-stu-id="9e365-135">Expense Category</span></span>
- <span data-ttu-id="9e365-136">角色價格</span><span class="sxs-lookup"><span data-stu-id="9e365-136">Role Price</span></span>
- <span data-ttu-id="9e365-137">交易類別價格</span><span class="sxs-lookup"><span data-stu-id="9e365-137">Transaction Category Price</span></span>
- <span data-ttu-id="9e365-138">特性</span><span class="sxs-lookup"><span data-stu-id="9e365-138">Characteristic</span></span>
- <span data-ttu-id="9e365-139">可預約資源</span><span class="sxs-lookup"><span data-stu-id="9e365-139">Bookable Resource</span></span>
- <span data-ttu-id="9e365-140">可預約資源類別關聯</span><span class="sxs-lookup"><span data-stu-id="9e365-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="9e365-141">可預約資源特性</span><span class="sxs-lookup"><span data-stu-id="9e365-141">Bookable Resource Characteristic</span></span>

![匯入完成](./media/6CompleteImport.png)
