---
title: 將示範資料套用至 Finance 雲端託管的環境
description: 本主題說明如何將 Project Operations 的示範資料套用至 Dynamics 365 Finance 雲端託管的環境。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365228"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="7fa19-103">將示範資料套用至 Finance 雲端託管的環境</span><span class="sxs-lookup"><span data-stu-id="7fa19-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="7fa19-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7fa19-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7fa19-105">本主題僅適用於 Microsoft Dynamics 365 Finance 10.0.13 版，而且只能在雲端託管的環境中執行。</span><span class="sxs-lookup"><span data-stu-id="7fa19-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="7fa19-106">將品質更新套用至環境 **之前**，請先完成本主題中的步驟。</span><span class="sxs-lookup"><span data-stu-id="7fa19-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="7fa19-107">在 LCS 專案中，開啟 **環境詳細資料** 頁面。</span><span class="sxs-lookup"><span data-stu-id="7fa19-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="7fa19-108">請注意，其中包含使用遠端桌面通訊協定 (RDP) 連接至環境所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7fa19-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![ 環境詳細資料](./media/1EnvironmentDetails.png)

<span data-ttu-id="7fa19-110">第一組反白顯示的認證是本機帳戶認證，並且包含遠端桌面連線的超連結。</span><span class="sxs-lookup"><span data-stu-id="7fa19-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="7fa19-111">此認證包含環境管理使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="7fa19-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="7fa19-112">第二組認證是用來登入此環境中的 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="7fa19-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="7fa19-113">透過 **本機帳戶** 中的超連結進行環境的遠端作業，並使用 **本機帳戶認證** 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="7fa19-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="7fa19-114">移至 **Internet Information Services** > **應用程式集區** > **AOSService**，並停止服務。</span><span class="sxs-lookup"><span data-stu-id="7fa19-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="7fa19-115">您要在此時停止服務，以便繼續取代 SQL Database。</span><span class="sxs-lookup"><span data-stu-id="7fa19-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![停止 AOS](./media/2StopAOS.png)

4. <span data-ttu-id="7fa19-117">移至 **服務**，並停止下列兩個項目：</span><span class="sxs-lookup"><span data-stu-id="7fa19-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="7fa19-118">Microsoft Dynamics 365 Unified Operations：批次管理服務</span><span class="sxs-lookup"><span data-stu-id="7fa19-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="7fa19-119">Microsoft Dynamics 365 Unified Operations：資料匯入匯出架構</span><span class="sxs-lookup"><span data-stu-id="7fa19-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![停止服務](./media/3StopServices.png)

5. <span data-ttu-id="7fa19-121">開啟 Microsoft SQL Server Management Studio。</span><span class="sxs-lookup"><span data-stu-id="7fa19-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="7fa19-122">使用 SQL Server 認證登入，並使用 LCS **環境詳細資料** 頁面中的 axdbadmin 使用者和密碼。</span><span class="sxs-lookup"><span data-stu-id="7fa19-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="7fa19-124">在物件總管中，選取 **資料庫** 並尋找 **AXDB**。</span><span class="sxs-lookup"><span data-stu-id="7fa19-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="7fa19-125">您會將資料庫取代為位於[下載中心](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip)的新資料庫。</span><span class="sxs-lookup"><span data-stu-id="7fa19-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="7fa19-126">將 ZIP 檔案複製到您遠端操作的 VM，然後解壓縮 ZIP 內容。</span><span class="sxs-lookup"><span data-stu-id="7fa19-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="7fa19-127">在 SQL Server Management Studio 中，以滑鼠右鍵按一下 **AxDB**，然後選取 **工作** > **還原** > **資料庫**。</span><span class="sxs-lookup"><span data-stu-id="7fa19-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![還原資料庫](./media/5RestoreDatabase.png)

9. <span data-ttu-id="7fa19-129">選取 **來源裝置**，並瀏覽至從您複製的 ZIP 中解壓縮的檔案。</span><span class="sxs-lookup"><span data-stu-id="7fa19-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![來源裝置](./media/6SourceDevice.png)

10. <span data-ttu-id="7fa19-131">選取 **選項**，然後選取 **覆寫現有的資料庫** 和 **關閉與目的地資料庫的現有連接**。</span><span class="sxs-lookup"><span data-stu-id="7fa19-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="7fa19-132">選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="7fa19-132">Select **OK**.</span></span>

![還原設定](./media/7RestoreSetting.png)

<span data-ttu-id="7fa19-134">您將會收到 AXDB 還原成功的確認。</span><span class="sxs-lookup"><span data-stu-id="7fa19-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="7fa19-135">收到此確認後，您可以關閉 SQL Services Management Studio。</span><span class="sxs-lookup"><span data-stu-id="7fa19-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="7fa19-136">返回 **Internet Information Services** > **應用程式集區** > **AOSService**，並啟動 AOSService。</span><span class="sxs-lookup"><span data-stu-id="7fa19-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="7fa19-137">移至 **服務**，並啟動兩個先前停止的服務。</span><span class="sxs-lookup"><span data-stu-id="7fa19-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="7fa19-138">在此 VM 上找出 AdminUserProvisioning 工具。</span><span class="sxs-lookup"><span data-stu-id="7fa19-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="7fa19-139">查看 K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe 下方。</span><span class="sxs-lookup"><span data-stu-id="7fa19-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="7fa19-140">使用 **電子郵件地址** 欄位中的使用者位址來執行 .ext 檔案 。</span><span class="sxs-lookup"><span data-stu-id="7fa19-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="7fa19-141">選取 **送出**。</span><span class="sxs-lookup"><span data-stu-id="7fa19-141">Select **Submit**.</span></span>

![管理使用者佈建](./media/8AdminUserProvisioning.png)

<span data-ttu-id="7fa19-143">這需要花費幾分鐘的時間完成。</span><span class="sxs-lookup"><span data-stu-id="7fa19-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="7fa19-144">您應該會收到成功更新管理使用者的確認訊息。</span><span class="sxs-lookup"><span data-stu-id="7fa19-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="7fa19-145">最後，以系統管理員身分執行命令提示字元，並執行 iisreset</span><span class="sxs-lookup"><span data-stu-id="7fa19-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS 重設](./media/9IISReset.png)

18. <span data-ttu-id="7fa19-147">關閉遠端桌面工作階段，並使用 LCS **環境詳細資料** 頁面登入環境，以確認其可依預期正常運作。</span><span class="sxs-lookup"><span data-stu-id="7fa19-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
