---
title: 佈建新的環境
description: 本主題提供有關如何佈建新的 Project Operations 環境的資訊。
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949352"
---
# <a name="provision-a-new-environment"></a>佈建新的環境

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本主題提供有關如何為資源/非庫存型案例佈建新的 Dynamics 365 Project Operations 環境的資訊。

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>在 LCS 專案中啟用 Project Operations 自動化佈建

使用下列步驟，為您的 LCS 專案啟用 Project Operations 自動化佈建流程。

1. 前往 [LCS](https://lcs.dynamics.com/v2)，並選取**預覽功能管理**圖標。
2. 在**預覽功能**清單中，選取 **Project Operations**，然後選取**預覽功能已啟用**以啟用 Project Operations。

> [!NOTE]
> 每個 LCS 專案都只會執行此步驟一次。

## <a name="provision-a-project-operations-environment"></a>佈建 Project Operations 環境

1. 開啟新的 Dynamics 365 Finance [示範環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)或[沙箱/生產環境](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)部署。 
2. 逐步解說**環境佈建**精靈。 

> [!IMPORTANT]
> 請確定選取的應用程式版本是 10.0.13 或更高版本。

3. 若要佈建 Project Operations，請選取**進階設定**下方的 **Common Data Service**。 
4. 選取**是**，然後在必要欄位中輸入資訊，以啟用 **Common Data Service 設定**：

  - 名字
  - 地區
  - 語言
  - 貨幣
 
5. 在 **Common Data Service 範本**欄位中，選取 **Project Operations** 

6. 選取部署的環境類型。 以訂閱為主的試用可讓您 部署為期 30 天的 CDS 環境。 

![部署設定](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> 選取**同意**確認服務條款，然後選取**完成**以返回部署設定。

![部署同意](./media/2DeploymentConsent.png)

7. 完成精靈中的其餘必要欄位，並確認部署。 環境佈建時間會根據環境類型而有所不同。 佈建最多可能需要六小時的時間。

  部署順利完成後，環境將會顯示為**已部署**。

8. 若要確認已成功部署環境，請選取**登入**，並登入要確認的環境。

![ 環境詳細資料](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>套用 Project Operations 財務示範資料 (選用步驟)

將 Project Operations 財務示範資料套用至 10.0.13 服務版本雲端託管的環境，如[本文章](resource-apply-finance-demo-data.md)中所述。

## <a name="apply-updates-to-the-finance-environment"></a>將更新套用至 Finance 環境

Project Operations 需要應用程式版本為 **10.0.13 (10.0.569.20009)** 或更新版本的 Finance 環境。

您可能需要將品質更新套用至 Finance 環境，才能收到此版本。

1. 在 LCS 的**環境詳細資料**頁面上，選取**可用更新**區段中的**檢視更新**。

![檢視更新](./media/5ViewUpdates.png)

2. 在**二進位更新**頁面上，選取**儲存套件**。

![儲存套件](./media/6SavePackage.png)

3. 按一下**全選**，然後選取**儲存套件**。

![檢閱並儲存更新](./media/7ReviewAndSaveUpdates.png)

4. 輸入套件的名稱和描述，然後選取**儲存**。 視網際網路連線而定，此程序可能需要花費一些時間。

![將套件上載至資產庫](./media/8UploadPackageToAssetsLibrary.png)

5. 儲存套件後，選取**完成**，並將此套件儲存至 LCS 專案中的資產庫。

儲存和驗證套件可能需要約 15 分鐘的時間。

6. 若要套用更新，請瀏覽至 LCS 中的**環境詳細資料**頁面，然後選取**維護** >  **套用更新**。

![維護環境](./media/9MaintainEnvironment.png)

7. 在更新清單中，選取您所建立的套件，並選取**套用**。

![套用更新](./media/10ApplyUpdates.png)

環境維護需要一些時間。 完成後，環境會回復到已部署的狀態。

![環境已部署](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>建立雙重寫入連接 

1. 在 LCS 專案中，移至**環境詳細資料**頁面。
2. 在 **Common Data Service 環境資訊**底下，選取**連結至 CDS for Apps**。
3. 連結完成後，請再次選取**連結至 CDS for Apps**。 將您重新導向至 Finance 中的雙重寫入。

![連結至 CDS](./media/12LinktoCDS.png)

4. 選取**套用解決方案**，以存取將在整合中對應的實體。

![套用解決方案](./media/13ApplySolutions.png)

5. 選取 **Dynamics 365 Finance and Operations 雙重寫入實體對應**和 **Dynamics 365 Project Operations 雙重寫入實體對應**這兩個解決方案，然後選取**套用**。

![確認解決方案](./media/14ConfirmSolutions.png)

套用解決方案後，將雙重寫入實體套用至環境。

![套用解決方案](./media/15ApplyingSolutions.png)

套用實體後，環境中會列出所有可用的對應。

![雙重寫入對應](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>更新後重新整理資料實體

1. 在 Finance 中，移至**資料管理**工作區。

![資料管理工作區](./media/16DataManagement.png)

2. 選取**架構參數**圖標。

![架構參數](./media/17FrameworkParameters.png)

3. 在**實體設定**頁面上，選取**重新整理實體清單**。

![重新整理實體清單](./media/18RefreshEntityList.png)

重新整理將需要約 20 分鐘的時間。 完成時，您會收到警示。

![重新整理確認](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>執行 Project Operations 雙重寫入對應

1. 在 LCS 專案中，移至**環境詳細資料**頁面。
2. 在 **Common Data Service 環境資訊**底下，選取**連結至 CDS for Apps**。 選取連結之後，您會重新導向至對應中實體的清單。
3. 依照下表所述，開始對應。 請務必遵循列示的順序進行。

| **實體對應** | **重新整理實體** | **初始同步** | **初始同步處理的主要記錄** | **執行先決條件** | **先決條件初始同步** |
| --- | --- | --- | --- | --- | --- |
| **所有公司的專案資源角色 (bookableresourcecategories)** | 無 | .是 | Common Data Service | 無 | 不適用 |
| **法律實體 (cdm\_companies)** | 無 | .是 | Finance and Operations 應用程式 | 無 | 不適用 |
| **Project Operations 整合實際值 (msdyn\_actuals)** | 無 | 無 | 不適用 | .是 | 無 |
| **專案合約服務內容 (salesorderdetails)** | 無 | 無 | 不適用 | 無 | 無 |
| **專案交易關聯的整合實體 (msdyn\_transactionconnections)** | 無 | 無 | 不適用 | 無 | 不適用 |
| **Project Operations 整合合約服務內容里程碑 (msdyn\_contractlinesscheduleofvalues)** | 無 | 無 | 不適用 | 無 | 不適用 |
| **費用估計值的 Project Operations 整合實體 (msdyn\_estimateslines)** | 無 | 無 | 不適用 | 無 | 不適用 |
| **時數估計值的 Project Operations 整合實體 (msdyn\_resourceassignments)** | 無 | 無 | 不適用 | 無 | 不適用 |
| **Project Operations 整合專案費用匯出實體 (msdyn\_expenses)** | .是 | 無 | 不適用 | 無 | 不適用 |
| **時數估計值的 Project Operations 整合實體 (msdyn\_resourceassignments)** | .是 | 無 | 不適用 | 無 | 不適用 |

4. 若要重新整理實體，請選取對應名稱，然後選取**重新整理實體**。 
5. 重新整理完成後，繼續執行對應。

![重新整理對應](./media/20RefreshMapping.png)

啟用下一個對應之前，請確認表格中的對應處於**執行中**狀態。 執行有較大量先決條件的對應可能需要一些時間。

若要執行有先決條件的對應，請啟用**顯示相關實體對應**切換。 如果表中指示**先決條件初始同步**為**否**，請先確認所有先決條件中的**初始同步**旗標是否為**關閉**，再執行此對應。

![執行對應](./media/21RunMap.png)

6. 驗證所有專案相關的對應是否為執行中狀態。

![所有正在執行的對應](./media/22AllMapsRunning.png)

您的 Project Operations 環境現在已佈建並設定。
