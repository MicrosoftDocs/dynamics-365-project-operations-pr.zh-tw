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
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>將示範資料套用至 Finance 雲端託管的環境

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

> [!IMPORTANT]
> 本主題僅適用於 Microsoft Dynamics 365 Finance 10.0.13 版，而且只能在雲端託管的環境中執行。 將品質更新套用至環境 **之前**，請先完成本主題中的步驟。

1. 在 LCS 專案中，開啟 **環境詳細資料** 頁面。 請注意，其中包含使用遠端桌面通訊協定 (RDP) 連接至環境所需的詳細資料。

![ 環境詳細資料](./media/1EnvironmentDetails.png)

第一組反白顯示的認證是本機帳戶認證，並且包含遠端桌面連線的超連結。 此認證包含環境管理使用者名稱和密碼。 第二組認證是用來登入此環境中的 SQL Server。

2. 透過 **本機帳戶** 中的超連結進行環境的遠端作業，並使用 **本機帳戶認證** 進行驗證。
3. 移至 **Internet Information Services** > **應用程式集區** > **AOSService**，並停止服務。 您要在此時停止服務，以便繼續取代 SQL Database。

![停止 AOS](./media/2StopAOS.png)

4. 移至 **服務**，並停止下列兩個項目：

- Microsoft Dynamics 365 Unified Operations：批次管理服務
- Microsoft Dynamics 365 Unified Operations：資料匯入匯出架構

![停止服務](./media/3StopServices.png)

5. 開啟 Microsoft SQL Server Management Studio。 使用 SQL Server 認證登入，並使用 LCS **環境詳細資料** 頁面中的 axdbadmin 使用者和密碼。

![SQL Server Management Studio](./media/4SSMS.png)

6. 在物件總管中，選取 **資料庫** 並尋找 **AXDB**。 您會將資料庫取代為位於[下載中心](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip)的新資料庫。 
7. 將 ZIP 檔案複製到您遠端操作的 VM，然後解壓縮 ZIP 內容。
8. 在 SQL Server Management Studio 中，以滑鼠右鍵按一下 **AxDB**，然後選取 **工作** > **還原** > **資料庫**。

![還原資料庫](./media/5RestoreDatabase.png)

9. 選取 **來源裝置**，並瀏覽至從您複製的 ZIP 中解壓縮的檔案。

![來源裝置](./media/6SourceDevice.png)

10. 選取 **選項**，然後選取 **覆寫現有的資料庫** 和 **關閉與目的地資料庫的現有連接**。 
11. 選取 **確定**。

![還原設定](./media/7RestoreSetting.png)

您將會收到 AXDB 還原成功的確認。 收到此確認後，您可以關閉 SQL Services Management Studio。

12. 返回 **Internet Information Services** > **應用程式集區** > **AOSService**，並啟動 AOSService。
13. 移至 **服務**，並啟動兩個先前停止的服務。

14. 在此 VM 上找出 AdminUserProvisioning 工具。 查看 K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe 下方。
15. 使用 **電子郵件地址** 欄位中的使用者位址來執行 .ext 檔案 。 
16. 選取 **送出**。

![管理使用者佈建](./media/8AdminUserProvisioning.png)

這需要花費幾分鐘的時間完成。 您應該會收到成功更新管理使用者的確認訊息。

17. 最後，以系統管理員身分執行命令提示字元，並執行 iisreset

![IIS 重設](./media/9IISReset.png)

18. 關閉遠端桌面工作階段，並使用 LCS **環境詳細資料** 頁面登入環境，以確認其可依預期正常運作。

![Finance and Operations](./media/10FinanceAndOperations.png)
