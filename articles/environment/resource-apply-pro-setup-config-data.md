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
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289809"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>在 Common Data Service 中設定和套用設定資料 

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>先決條件

在您開始在 Common Data Service (CDS) 中設定資料之前，必須符合下列先決條件：

1.  為 Project Operations 設定 CDS 環境以及 Dynamics 365 Finance 環境。
2.  來自 Dynamics 365 Finance 環境的法律實體已與 CDS 環境共用。 這表示 CDS 中的 **公司** 實體有下列公司記錄：
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>安裝設定和設定資料

1. 下載、解除封鎖和解壓縮[設定和設定資料套件](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)。
2. 瀏覽至解壓縮後的資料夾，並執行可執行檔 *DataMigrationUtility*。
3. 在 Common Data Service 設定移轉 (CMT) 精靈的第 1 頁中，選取 **匯入資料**，然後選取 **繼續**。

![設定移轉](./media/1ConfigurationMigration.png)

4. 在 CMT 精靈的第 2 頁中，選取 **Microsoft 365** 做為 **部署類型**。
5. 選取 **顯示可用組織的清單** 和 **顯示進階** 核取方塊。
6. 選取您的租用戶所在地區、輸入您的認證，然後選取 **登入**。

![設定登入](./media/2ConfigurationSignin.png)

7. 在第 3 頁中，從租用戶的組織清單中，選取要將示範資料匯入到的組織，然後選取 **登入**。
8. 在第 4 頁中，從解壓縮後的資料夾中選取 ZIP 檔案 *SampleSetupAndConfigData*。

![ZIP 檔案選取](./media/3ZipFile.png)

![選擇檔案](./media/4SelectAFile.png)

9. 選取 ZIP 檔案之後，選取 **匯入資料**。

![匯入資料​​](./media/5ImportData.png)

10. 視您的網路速度而定，匯入將會執行約二至十分鐘。 匯入完成後，結束 CMT 精靈。 
11. 檢查您的組織中是否有下列 19 個實體的資料：

  - 貨幣
  - 組織單位
  - 連絡人
  - 課稅群組
  - 客戶群組
  - 單位
  - 單位群組
  - 價目表
  - 專案參數價目表
  - 發票頻率
  - 可預約資源類別
  - 交易類別
  - 費用類別
  - 角色價格
  - 交易類別價格
  - 特性
  - 可預約資源
  - 可預約資源類別關聯
  - 可預約資源特性

![完成匯入](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>更新 Project Operations 設定

1. 瀏覽至 CE 環境。 您可以開啟 [Power Platform 系統管理中心](https://admin.powerplatform.microsoft.com/environments)、選取環境，然後選取 **開啟環境** 來尋找它。 

![開啟環境](./media/7OpenEnvironment.png)

2. 移至 **專案** > **資源**，然後選取 **新增**，為您的使用者建立可預約資源。

![可預約資源](./media/8BookableResources.png)

3. 在 **一般** 索引標籤上，選取您的管理使用者。 確認時區是否與您所在的時區相符。 

![新的可預約資源](./media/9NewBookableResource.png)

4. 在 **排程** 索引標籤的 **公司** 欄位中，選取 **USPM** 公司，然後選取 **儲存**。 

![[排程] 索引標籤](./media/10SchedulingTab.png)

5. 選取 **工作時數** 索引標籤。  

![工作時數](./media/11WorkHours.png)

6. 按兩下行事曆中的任何值，然後選取 **編輯** > **系列中的所有事件**。 

![工作行事曆](./media/12WorkCalendar.png)

7. 將工作時數變更為八 (8) 小時工作日、將週末標示為非工作日，並確定時區與您的時區相符。 
8. 選取 **儲存後關閉**。

![更新行事曆](./media/13UpdateCalendar.png)

9. 移至 **設定** > **行事曆範本**，並選取 **新增**。
 
 ![行事曆範本](./media/14CalendarTemplates.png)
 
 10. 輸入名稱、選取您所建立的範本資源，然後選取 **儲存**。 
 
 ![儲存行事曆範本](./media/15SaveCalendarTemplate.png)
 
 11. 移至 **參數**，並按兩下該記錄。 
 
 ![專案參數](./media/16ProjectParameters.png)
 
12. 更新下列欄位：

 - **預設公司**：USPM
 - **預設組織單位**：Contoso Robotics Global
 - **發票週期**：每月第七天和最後一天
 - **工作時數範本**：變更為您所建立的範本。

13. 選取 **儲存**。 

![更新專案參數](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]