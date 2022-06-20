---
title: 更新 Finance 環境中的 Project Operations
description: 本文提供有關如何在 Dynamics 365 Finance 環境中更新 Project Operations 的資訊。
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 0cf9da8cc9d1f29dc41d4b119278e545047020bc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912460"
---
# <a name="update-project-operations-in-your-finance-environment"></a>更新 Finance 環境中的 Project Operations

_**適用於：** 資源/非庫存型案例適用的 Project Operations_


本文提供有關如何在 Dynamics 365 Finance 環境中更新 Dynamics 365 Project Operations 的資訊。 將 Project Operations 更新至更新 5 (UR5) 所需的程序有三個。

- [將套件匯入預覽版專案中](#import)
- [套用更新](#apply)
- [更新 Dataverse 環境](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>將套件匯入 LCS 專案中

1. 以專案負責人或環境管理員身分登入 [Lifecycle Services (LCS)](https://lcs.dynamics.com/)。
2. 從專案清單中選取 LCS 專案。
3. 在 **專案** 頁面的 **環境** 群組中，開啟您要更新的環境。
4. 確認環境是否正在執行中。 如果未啟動，請啟動環境。
5. 在 **可用更新** 底下的 **新版本** 區段中，選取 **檢視更新** 以尋找 10.0.15。

![[檢視更新] 按鈕。](media/view-update.png)

6. 在 **二進位更新** 頁面上，選取 **儲存套件**。
7. 在 **檢閱並儲存更新** 頁面上，選取 **儲存套件**。
8. 在開啟的 **將套件儲存至資產庫** 窗格中，輸入套件名稱，然後選取 **儲存套件**。
9. 當 LCS 儲存套件完畢後，就會啟用 **完成** 按鈕。 選取 **完成**。 LCS 將會驗證套件。 驗證可能需要幾分鐘或長達一小時。


## <a name="apply-the-package-update"></a><a name="apply"></a>套用套件更新

1. 在 LCS 的 **環境詳細資料** 頁面上，選取 **維護** > **套用更新**。
2. 從清單中選取先前儲存的套件，然後選取 **套用**。
3. 選取 **是** 確認您要部署套件。

![確認套件部署對話方塊。](media/confirm-package-deployment.png)

4. 選取 **是** 確認您要更新應用程式。

![確認應用程式更新對話方塊。](media/confirm-application-update.png)

部署和應用程式更新將會開始。 

在 **環境詳細資料** 頁面的右上角，環境狀態將會更新為 **服務中**。 更新大約會在 2 小時後完成。 應用程式版本資訊將會更新為 **Microsoft Dynamics 365 for Finance and Operations 10.0.15**，而環境狀態則更新為 **已部署**。


## <a name="update-your-dataverse-environment"></a><a name="update"></a>更新 Dataverse 環境

1. 登入 [Power Platform 系統管理中心](https://admin.powerplatform.com/)。
2. 在 清單中，尋找並開啟您用來安裝 Project Operations 的環境。
3. 在 **環境** 頁面上，選取 **資源** > **Dynamics 365 應用程式**。
4. 在清單中，找出 **Microsoft Dynamics 365 Project Operations**，然後選取 **狀態** 欄中的 **可用的更新**。
5. 選取 **我同意服務條款** 核取方塊，然後選取 **更新**。 將會安裝最新版本的解決方案。

安裝完成後，您已安裝版本 4.5.0.134。

## <a name="configure-new-features"></a>設定新功能

### <a name="enable-dual-write-mapping"></a>啟用雙重寫入對應

在 Finance 和 Dataverse 環境上完成更新後，您可以啟用必要的雙重寫入對應。 完成下列程序以啟用雙重寫入對應。

- [更新 Customer Engagement 環境的安全性設定](#security)
- [重新整理資料實體](#refresh)
- [更新並執行雙重寫入對應](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>更新 Dataverse 環境的安全性設定

在 UR5 的更新中需要對實體的安全性權限進行下列更新。

1. 在 Dataverse 環境中，移至 **設定**，然後在 **系統** 群組中選取 **安全性**。

![Dataverse 環境設定。](media/Picture21.png)

2. 選取 **資訊安全角色**。
3. 從角色清單中選取 **雙重寫入應用程式使用者**，然後選取 **自訂實體** 索引標籤。 
4. 確認角色是否對下列各項具有 **讀取** 和 **附加至** 權限：

      - **貨幣匯率類型**
      - **會計科目表** 
      - **會計行事曆** 
      - **總帳**

5. 更新資訊安全角色之後，移至 **設定** > **安全** > **團隊**。 確認 **雙重寫入應用程式使用者** 角色是否已套用至團隊。 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>從更新中重新整理資料實體

1. 在 Finance 環境中，開啟 **資料管理** 工作區，然後開啟 **架構參數** 頁面。
2. 在 **實體設定** 索引標籤上，選取 **重新整理實體清單**。
3. 選取 **關閉** 以確認實體重新整理。

 > [!NOTE]
 > 此程序需要約 20 分鐘才能完成。 重新整理完成時，系統會通知您。

### <a name="update-dual-write-mappings"></a><a name="run"></a>更新雙重寫入對應

1. 在 **資料管理** 工作區中，選取 **雙重寫入**。
2. 選取 **套用解決方案**、在清單中選取這兩個解決方案，然後選取 **套用**。
3. 在 **雙重寫入** 頁面上，選取下列資料表對應，然後選取 **停止**。

    - **Project Operations 整合實際值 (msdyn_actuals)**
    - **Project Operations 整合專案費用類別 (msdyn_expensecategories)**
    - **Project Operations 整合實際值專案費用匯出實體 (msdyn_expenses)**

4. 在 **資料表對應版本** 頁面上，將新的對應版本套用至三個實體中的每一個。
5. 在 **雙重寫入** 頁面上，選取 [執行] 以重新啟動對應。
6. 從對應清單中選取與所有先決條件的 **總帳 (msdyn_ledgers)** 對應，然後選取 **初始同步** 核取方塊。 
7. 在 **初始同步主控端** 欄位中，選取 **財務和營運應用程式**，然後選取 **執行**。
 
 ![總帳對應同步處理。](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]