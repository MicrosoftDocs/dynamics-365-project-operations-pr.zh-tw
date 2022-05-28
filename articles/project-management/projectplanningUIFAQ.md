---
title: 在工作窗格中工作時的疑難排解
description: 本主題提供在工作窗格中工作時所需的疑難排解資訊。
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: ee80363cf6f9a65a91be43a84434d37f02511f26
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596408"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>在工作窗格中工作時的疑難排解 


_**適用於：** 資源/非庫存型案例適用的 Project Operations 精簡部署 - 交易至開立預估發票、Project for the Web_

Dynamics 365 Project Operations 所運用的工作網格是 Microsoft Dataverse 中託管的 iFrame。 由於這種運用，因此必須符合特定需求，才能確保驗證和授權正確發揮作用。 本主題概述常見的問題，這些問題可能會影響在分工結構圖 (WBS) 中呈現網格或管理工作的能力。

常見問題包括：

- 工作網格中的 **工作** 索引標籤空白。
- 開啟專案時，無法載入專案，且使用者介面 (UI) 停滯在進度環上。
- **Project for the Web** 的權限管理。
- 建立、更新或刪除工作時，無法儲存所做的變更。

## <a name="issue-the-task-tab-is-empty"></a>問題：[工作] 索引標籤空白

### <a name="mitigation-1-enable-cookies"></a>風險降低措施 1：啟用 Cookie

Project Operations 需要啟用第三方 Cookie，才能呈現分工結構圖。 如果未啟用第三方 Cookie，當您在 **專案** 頁面上選取 **工作** 索引標籤時，看到的不是工作，而是空白頁面。

對於 Microsoft Edge或 Google Chrome 瀏覽器，下列程式概述如何更新瀏覽器設定以啟用第三方 Cookie。

#### <a name="microsoft-edge"></a>Microsoft Edge

1. 開啟 Edge 瀏覽器。
2. 選取右上角的 **省略符號** (...)，然後選取 **設定**。
3. 在 **Cookie 和網站權限** 底下，選取 **Cookie 和網站資料**。
4. 關閉 **封鎖第三方 Cookie**。
5. 重新整理您的瀏覽器。 

#### <a name="google-chrome"></a>Google Chrome

1. 開啟 Chrome 瀏覽器。
2. 選取右上角的三個垂直點，然後選取 **設定**。
3. 在 **隱私權和安全性** 底下，選取 **Cookie 和其他網站資料**。
4. 選取 **允許所有 Cookie**。
5. 重新整理您的瀏覽器。 

> [!NOTE]
> 如果您封鎖第三方 Cookie，其他網站的所有 Cookie 和網站資料也都會遭到封鎖，即使您的例外清單中允許該網站也一樣。

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>風險降低措施 2：驗證已正確設定 PEX 端點

Project Operations 需要專案參數參照 PEX 端點。 必須有此端點，才能與用來呈現分工結構圖的服務進行通訊。 如果未啟用此參數，您就會收到「專案參數無效」錯誤。 若要更新 PEX 端點，請完成下列步驟。

1. 將 **PEX 端點** 欄位新增至 **專案參數** 頁面。
2. 找出您正在使用的產品類型。 設定 PEX 端點時，會使用此值。 擷取時，PEX 端點中已定義產品類型。 保留該值。
3. 以下列值來更新欄位：`https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`。 下表提供須根據產品類型使用的類型參數。

      | **產品類型**                     | **類型參數** |
      |--------------------------------------|--------------------|
      | 預設組織上的 Project for the Web   | 類型=0             |
      |  CDS 具名組織上的 Project for the Web | 類型=1             |
      | Project Operations                   | 類型=2             |

4. 從 **專案參數** 頁面移除欄位。

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>風險降低措施 3：登入 project.microsoft.com
在 Microsoft Edge 瀏覽器中，開啟新的索引標籤、移至 project.microsoft.com，然後使用您要用來存取 Project Operations 的使用者角色登入。

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>問題：無法載入專案，且 UI 停滯在進度環上

為了驗證的目的，必須啟用快顯來讓工作網格載入。 如果快顯未啟用，畫面就會停滯在載入進度環上。 下圖顯示網址列中含有已封鎖快顯標籤的 URL，正是由此導致嘗試載入頁面的進度環停滯。 

   ![進度環停滯和快顯封鎖。](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>風險降低措施 1：啟用快顯

專案停滯在進度環時，可能是沒有啟用快顯。

#### <a name="microsoft-edge"></a>Microsoft Edge

有兩種方式可以在 Edge 瀏覽器中啟用快顯。

1. 在 Edge 瀏覽器中，選取瀏覽器右上方的 [通知]。
2. 選取 **永遠允許特定 Dataverse 環境的快顯視窗和重新導向**。
 
     ![[快顯已封鎖] 視窗。](media/enablepopups.png)

或者，也可以完成下列步驟。

1. 開啟 Edge 瀏覽器。
2. 選取右上角的 **省略符號** (...)，然後選取 **設定** > **網站權限** > **快顯視窗並重新導向**。
3. 將 **快顯視窗並重新導向** 切換為關閉以封鎖快顯，或切換為開啟以允許快顯出現在裝置上。
4. 啟用快顯後，重新整理瀏覽器。 

#### <a name="google-chrome"></a>Google Chrome
1. 開啟 Chrome 瀏覽器。
2. 瀏覽至封鎖快顯的頁面。
3. 在網址列中，選取 **快顯已封鎖**。
4. 選取您要看到的快顯的連結。
5. 啟用快顯後，重新整理瀏覽器。 

> [!NOTE]
> 若要一律都看到網站的快顯，請選取 **永遠允許 [網站] 的快顯視窗和重新導向**，然後選取 **完成**。

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>問題 3：Project for the Web 的權限管理

Project Operations 需要依賴外部排程服務。 此服務要求使用者必須已受指派數個允許他們讀取和寫入與 WBS 相關之實體的角色。 這些實體包括專案工作、資源指派和工作相依性。 如果使用者瀏覽至 **工作** 索引標籤時無法呈現 WBS，則可能是因為 **Project Operations** 尚未啟用 **專案**。 使用者可能會收到資訊安全角色錯誤，或收到與拒絕存取相關的錯誤。

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>風險降低措施 1：驗證應用程式使用者及終端使用者資訊安全角色

1. 移至 **設定** > **安全性** > **使用者** > **應用程式使用者**。  

   ![應用程式讀取器。](media/applicationuser.jpg)
   
2. 按兩下要驗證的應用程式使用者記錄：

     - 使用者可以存取專案。 您可以驗證使用者是否有 **專案經理** 資訊安全角色來執行此動作。
     - Microsoft Project 應用程式使用者存在且已正確設定。
 
3. 如果此使用者不存在，請建立新的使用者記錄。 
4. 選取 **新增使用者**，將項目表單變更為 **應用程式使用者**，然後新增 **應用程式識別碼**。

   ![應用程式使用者詳細資料。](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a> 4：建立、更新或刪除工作時，無法儲存所做的變更

對 WBS 進行一項或多項更新時，變更失敗且未儲存。 排程窗格中出現錯誤，並顯示訊息：「無法儲存您最近進行的變更」。

### <a name="mitigation-1-validate-the-license-assignment"></a>風險降低措施 1：驗證授權指派

1. 確認是否已將正確的授權指派給使用者，以及已在授權的服務方案詳細資料中啟用該服務。  
2. 確認使用者是否可以開啟 **project.microsoft.com**。
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>風險降低措施 2： Project 應用程式使用者的驗證設定
1. 確認是否已建立 Project 應用程式使用者。
2. 將下列資訊安全角色套用至使用者：
  
  - Dataverse 使用者或基本使用者
  - Project Operations 系統
  - Project 系統
  - Project Operations 雙重寫入系統。 Project Operations 的資源/非庫存型部署案例需要此角色。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
