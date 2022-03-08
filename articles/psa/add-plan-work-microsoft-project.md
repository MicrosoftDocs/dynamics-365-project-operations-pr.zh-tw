---
title: 使用 Project Service 增益集在 Microsoft Project 中規劃您的工作 | MicrosoftDocs
description: 此主題提供有關如何新增、設定和使用 Microsoft Project Service 的 Microsoft Project 增益集的資訊。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ccebf1439f49092b23da5b4fc2ebb4fc484de4dd17c870eea9fe37b00fbb3689
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005291"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>使用 Project Service Automation 增益集在 Microsoft Project 中規劃您的工作

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 讓您更容易進行專案規劃，包括估計值。 您可以定義工作，在提交最終提案時清楚呈現成本、努力及銷售值。  

 現在您可以安裝 [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)]，並且在您熟悉的 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 環境中規劃工作。 使用 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 健全的規劃及管理功能，然後在 Project Service Automation 中更新您的專案計劃。  

> [!IMPORTANT]
> - 若要使用 SharePoint 文件管理儲存您的 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 檔案以用於 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 專案，[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 系統管理員必須開啟文件管理。 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] 僅與 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition 相容。  

## <a name="download-and-install-the-add-in"></a>下載並安裝增益集  
 準備好 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 登入資訊。 您需要這項資訊從 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 連線至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。  

1.  您可以從「下載中心」下載支援的 Project Service 版本 [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) 或 [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) 的增益集。  

2.  按一下下載連結。  

3.  下載完成時，按一下 **是** 以安裝增益集。  

## <a name="configure-the-add-in"></a>設定增益集  

1. 開啟 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]，然後按一下 **Project Service** 索引標籤。  

2. 按一下 **連線**。  

3. 輸入您的登入資訊，然後按一下 **登入**。  

   現在您可以開始使用增益集。  

## <a name="read-from-a-template"></a>從範本讀取  
 從您在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中建立並複製到 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 的範本讀取，開始您的專案規劃。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)][建立專案範本 (Project Service Automation)](../psa/create-project-template.md)  

1.  從 **Project Service** 索引標籤按一下 **讀取** > **Project Service Automation 專案範本**。  

2.  從清單中選擇專案範本，然後按一下 **開啟**。  

    > [!NOTE]
    >  根據預設，從範本複製到 Project 的工作會設定為手動排程。  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>將 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 角色指派給專案資源  

1.  開啟專案，然後按一下 **工作** 功能區。  

2.  按一下 **甘特圖** 功能表，然後選擇 **資源工作表**。  

3.  在 [資源工作表] 上按一下 **Project Service 資源角色** 下拉式功能表，然後選擇 Project Service Automation 角色。  

## <a name="staff-your-project-with-resources"></a>為您的專案配置資源  

1.  從 [Project Service] 索引標籤中選取一列，然後按一下 **尋找資源**。  

2.  在 **預約資源** 畫面中，選取要用於專案的資源。  

3.  按一下 **預約**，然後按一下 **確定**。  

## <a name="publish-your-project"></a>發行您的專案  
專案規劃完成後，下一步是匯入專案並發行至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中。  

專案將匯入到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。 定價和團隊產生程序會套用。 在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中開啟專案，會看見團隊、專案估計值及分工結構圖已產生。 下表顯示何處可找到結果：


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **甘特圖**   | 匯入至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **分工結構圖** 畫面。 |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **資源工作表** |   匯入至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **團隊成員** 畫面。   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **使用方式**    |    匯入至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **專案估計值** 畫面。     |

**若要匯入和發行您的專案**  
1. 從 **Project Service** 索引標籤按一下 **發行** > **新的 Project Service Automation 專案**。  

2. 在 **發行至 Project Service 中的新專案** 對話方塊中，輸入 **專案名稱**，然後選取 **客戶**。  

3. 選擇性地核取 **將專案計劃連結至 Project Service Automation**，將計劃專案檔案連結至 Project Service Automation。  

4. 按一下 **發行**。  

   將專案檔案連結至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]，讓專案檔案成為主要，並且在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中將分工結構圖設為唯讀。  若要對專案計劃進行變更，您需要在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中進行變更，並將它們做為更新發行至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。  

## <a name="edit-a-project-thats-been-imported"></a>編輯已匯入的專案  
 若要對已匯入 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 的專案計劃進行變更，您有兩個選項︰  

- 開啟主檔案，並在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中編輯。  

- 取消連結檔案，並直接在 Project Service 中編輯。 根據預設，已從 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 上傳的專案會鎖定，且只能在 Project 中編輯。 若要在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中編輯檔案，必須將檔案取消連結。  

### <a name="edit-in-pn_microsoft_project"></a>在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中編輯  

1. 從主要功能表按一下 **Project Service** > **專案**。  

2. 從專案清單中，開啟您在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中建立的專案。  

3. 從功能區按一下 **在 MS Project 中開啟**。 這樣會在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟連結的主檔案。  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>取消連結檔案，並在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service 中編輯  

1. 從主要功能表按一下 **Project Service** > **專案**。  

2. 從專案清單中，開啟您在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中建立的專案。  

3. 從功能區按一下 **與 MS Project 取消連結**。  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>將專案檔案上傳至 SharePoint 或 Office 群組  
 您可以將專案檔案上傳到 SharePoint，它會位在您的 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 專案的相關聯文件底下。  您需要請系統管理員設定 SharePoint 文件管理功能，並開啟專案實體的這項功能。 

 如果您已設定 Office 群組，也可以將專案檔案上傳至[!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]。

### <a name="upload-a-file-for-sharepoint"></a>上傳檔案以用於 SharePoint  

1. 從主要功能表按一下 **Project Service** > **上傳**。  

2. 選取 **至 Project Service Automation 專案文件**。  

3. 在 **啟用在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 對話方塊中，選取 **是** 或 **否**。  

   - 如果您按一下 **是**，就可以選取 Project Service Automation 中的 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 按鈕、啟動 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]，然後從 SharePoint 文件庫載入專案檔案。  

   - 如果按一下 **否**，則 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 按鈕的連結會沒有作用。  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 檔案位於 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中特定 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 專案的 **文件** 底下。  

### <a name="upload-a-file-for-office-groups"></a>上傳用於 Office 群組的檔案  

1. 從主要功能表按一下 **Project Service** > **上傳**。  

2. 選取 **至 Project Service Automation 專案文件**。  

3. 在 **啟用在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 對話方塊中，選取 **是** 或 **否**。  

   - 如果您按一下 **是**，就可以選取 Project Service Automation 中的 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 按鈕、啟動 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]，然後從 SharePoint 文件庫載入專案檔案。  

   - 如果按一下 **否**，則 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中開啟** 按鈕的連結會沒有作用。  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 檔案位於 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中特定 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 專案的 **文件** 底下。  

## <a name="publish--your-project-as-a-template"></a>將專案發行為範本  
 您可以儲存專案並重複使用，只要將它儲存為 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中的專案範本。  專案範本是 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中可重複使用的專案計劃。 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)][建立專案範本 (Project Service Automation)](../psa/create-project-template.md)  

1. 從 **Project Service** 索引標籤按一下 **發行** > **新的 Project Service Automation 專案範本**。  

2. 在 **發行至 Project Service 中的新專案範本** 對話方塊中，輸入 **專案範本名稱**。  

3. 選擇性地核取 **將專案計劃連結至 Project Service Automation**，將專案檔案連結至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。  

4. 按一下 **發行**。  

將專案檔案連結至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]，讓專案檔案成為主要，並且在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 範本中將分工結構圖設為唯讀。  若要對專案計劃進行變更，您需要在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中進行變更，並將它們做為更新發行至 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。

## <a name="read-a-resource-loaded-schedule"></a>讀取資源載入的排程

從 Project Service Automation 讀取專案時，資源的行事曆並不會同步處理至桌面用戶端。 如果工作期間、工作或結束有差異，則可能是因為資源與桌面用戶端的專案中並未套用相同的工作時數範本行事曆。


## <a name="data-synchronization"></a>資料同步

下表概述如何在 Project Service Automation 與 Microsoft Project 桌面增益集之間同步處理資料。

| **實體** | **欄位** | **Microsoft Project 至 Project Service Automation** | **Project Service Automation 至 Microsoft Project** |
| --- | --- | --- | --- |
| 專案工作 | Due Date | ● | - |
| 專案工作 | 預估投入的資源 | ● | - |
| 專案工作 | MS Project 用戶端識別碼 | ● | - |
| 專案工作 | 上層工作 | ● | - |
| 專案工作 | Project | ● | - |
| 專案工作 | 專案工作 | ● | - |
| 專案工作 | 專案工作名稱 | ● | - |
| 專案工作 | 資源分配單位 (已於 v3.0 取代) | ● | - |
| 專案工作 | 已排程的期間 | ● | - |
| 專案工作 | 開始日期 | ● | - |
| 專案工作 | WBS 識別碼 | ● | - |

| **實體** | **欄位** | **Microsoft Project 至 Project Service Automation** | **Project Service Automation 至 Microsoft Project** |
| --- | --- | --- | --- |
| 小組成員 | MS Project 用戶端識別碼 | ● | - |
| 小組成員 | 職位名稱 | ● | - |
| 小組成員 | 專案 | ● | ● |
| 小組成員 | 專案團隊 | ● | ● |
| 小組成員 | 資源分配單位 | - | ● |
| 小組成員 | 角色 | - | ● |
| 小組成員 | 工作時數 | 未同步處理 | 未同步處理 |

| **實體** | **欄位** | **Microsoft Project 至 Project Service Automation** | **Project Service Automation 至 Microsoft Project** |
| --- | --- | --- | --- |
| 資源指派 | 開始日期 | ● | - |
| 資源指派 | 小時 | ● | - |
| 資源指派 | MS Project 用戶端識別碼 | ● | - |
| 資源指派 | 計劃的工作 | ● | - |
| 資源指派 | Project | ● | - |
| 資源指派 | 專案團隊 | ● | - |
| 資源指派 | 資源指派 | ● | - |
| 資源指派 | 工作​​ | ● | - |
| 資源指派 | 至今 | ● | - |

| **實體** | **欄位** | **Microsoft Project 至 Project Service Automation** | **Project Service Automation 至 Microsoft Project** |
| --- | --- | --- | --- |
| 專案工作相依性 | 專案工作相依性 | ● | - |
| 專案工作相依性 | 連結類型 | ● | - |
| 專案工作相依性 | 前置任務工作 | ● | - |
| 專案工作相依性 | Project | ● | - |
| 專案工作相依性 | 後續任務工作 | ● | - |

### <a name="see-also"></a>請參閱  
 [專案經理指南](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]