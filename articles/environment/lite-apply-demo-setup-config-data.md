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
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072861"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>套用「Project Operations Lite 部署 – 交易至開立預估發票」的示範設定和設定資料

_**精簡部署 - 交易至開立預估發票_

1. 下載[主要資料套件](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip)。 
2. 瀏覽至資料夾 *ProjOpsDemoDataSetupAndMaster - Integrated CMT*，並執行可執行檔 *DataMigrationUtility*。
3. 在 Common Data Service 設定移轉 (CMT) 精靈的第 1 頁中，選取 **匯入資料**，然後選取 **繼續**。

![設定移轉](./media/1ConfigurationMigration.png)

4. 在 CMT 精靈的第 2 頁中，選取 **Microsoft 365** 做為 **部署類型**。
5. 選取 **顯示可用組織的清單** 和 **顯示進階** 核取方塊。
6. 選取您的租用戶所在地區、輸入您的認證，然後選取 **登入**。

![設定登入](./media/2ConfigurationSignin.png)

7. 在第 3 頁中，從租用戶的組織清單中，選取要將示範資料匯入到的組織，然後選取 **登入**。
8. 在第 4 頁中，從解壓縮後的資料夾 *ProjOpsDemoDataSetupAndMaster - Integrated CMT* 中選取 ZIP 檔案 *MasterAndSetupData*。

![ZIP 檔案](./media/3ZipFile.png)

![選擇檔案](./media/4SelectAFile.png)

9. 選取 ZIP 檔案之後，選取 **匯入資料**。

![匯入資料](./media/5ImportData.png)

10. 視您的網路速度而定，匯入將會執行約二至十分鐘。 完成後，結束 CMT 精靈。 
11. 檢查您的組織中是否有下列 20 個實體的資料：

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
- 發票週期詳細資料
- 可預約資源類別
- 交易類別
- 費用類別
- 角色價格
- 交易類別價格
- 特性
- 可預約資源
- 可預約資源類別關聯
- 可預約資源特性

![匯入完成](./media/6CompleteImport.png)
