---
title: 在工作窗格中工作時的疑難排解
description: 本主題提供在工作窗格中工作時所需的疑難排解資訊。
author: ruhercul
ms.date: 08/02/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 07e7bd42db48842edee17fdfdd22fdcd8207644c1751f453ec29c3194aac625e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989091"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>在工作窗格中工作時的疑難排解 

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

本主題說明如何修正您使用成本管理時可能遇到的問題。

## <a name="enable-cookies"></a>啟用 Cookie

Project Operations 需要啟用第三方 Cookie，以便呈現分工結構圖。 如果未啟用第三方 Cookie，當您在 **專案** 頁面上選取 **工作** 索引標籤時，看到的不是工作，而是空白頁面。

![未啟用第三方 Cookie 時的空白索引標籤。](media/blankschedule.png)


### <a name="workaround"></a>因應措施
對於 Microsoft Edge或 Google Chrome 瀏覽器，下列程式概述如何更新瀏覽器設定以啟用第三方 Cookie。

#### <a name="microsoft-edge"></a>Microsoft Edge

1. 開啟 Edge 瀏覽器。
2. 選取右上角的 **省略符號** (...)，然後選取 **設定**。
3. 在 **Cookie 和網站權限** 底下，選取 **Cookie 和網站資料**。
4. 關閉 **封鎖第三方 Cookie**。

#### <a name="google-chrome"></a>Google Chrome

1. 開啟 Chrome 瀏覽器。
2. 選取右上角的三個垂直點，然後選取 **設定**。
3. 在 **隱私權和安全性** 底下，選取 **Cookie 和其他網站資料**。
4. 選取 **允許所有 Cookie**。

> [!IMPORTANT]
> 如果您封鎖第三方 Cookie，其他網站的所有 Cookie 和網站資料也都會遭到封鎖，即使您的例外清單中允許該網站也一樣。

## <a name="pex-endpoint"></a>PEX 端點

Project Operations 需要專案參數參照 PEX 端點。 必須有此端點，才能與用於呈現分工結構圖的服務進行通訊。 如果未啟用此參數，您就會收到「專案參數無效」錯誤。 

### <a name="workaround"></a>因應措施

1. 將 **PEX 端點** 欄位新增至 **專案參數** 頁面。
2. 找出您正在使用的產品類型。 設定 PEX 端點時，會使用此值。 擷取時，PEX 端點中已定義產品類型。 保留該值。 
   
    ![專案參數上的 PEX 端點欄位。](media/pex-endpoint.png)

3. 以下列值來更新欄位：`https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`。

   
   | 產品類型                         | 類型參數 |
   |--------------------------------------|----------------|
   | 預設組織上的 Project for the Web   | 類型=0         |
   |  CDS 具名組織上的 Project for the Web | 類型=1         |
   | Project Operations                   | 類型=2         |
   
4. 從 **專案參數** 頁面移除欄位。

## <a name="privileges-for-project-for-the-web"></a>Project 網頁版的權限

Project Operations 需要依賴外部排程服務。 此服務要求使用者必須已獲指派數個可讀取和寫入與分工結構圖相關之實體的角色。 這些實體包括專案工作、資源指派和工作相依性。 如果使用者移至 **工作** 索引標籤時無法呈現分工結構圖，可能是因為尚未啟用 Project Operations 適用的 Project。 使用者可能會收到資訊安全角色錯誤，或收到與拒絕存取相關的錯誤。


## <a name="workaround"></a>因應措施

1. 移至 **設定 > 安全性 > 使用者 > 應用程式使用者**。  

   ![應用程式讀取器。](media/applicationuser.jpg)
   
2. 按兩下應用程式使用者記錄，以驗證：

 - 使用者可以存取專案。 這項驗證通常是透過確定使用者具備 **專案經理** 資訊安全角色來完成。
 - Microsoft Project 應用程式使用者存在且已正確設定。
 
3. 如果此使用者不存在，您可以建立新的使用者記錄。 選取 **新增使用者**。 將輸入表單變更至 **應用程式使用者**，然後新增 **應用程式識別碼**。

   ![應用程式使用者詳細資料。](media/applicationuserdetails.jpg)

4. 確認是否已將正確的授權指派給使用者，以及已在授權的服務方案詳細資料中啟用該服務。
5. 確認使用者是否可以開啟 project.microsoft.com。
6. 透過專案參數確認系統是否指向正確的專案端點。
7. 確認是否已建立 Project 應用程式使用者。
8. 將下列資訊安全角色套用至使用者：

  - Dataverse 使用者
  - Project Operations 系統
  - Project 系統

## <a name="error-when-updating-the-work-breakdown-structure"></a>更新分工結構圖時發生錯誤

對分工結構圖進行一項或多項更新時，變更最終會失敗且不會儲存。 排程窗格中發生錯誤，指出「無法儲存您最近所做的變更」。

### <a name="workaround"></a>因應措施

1. 確認是否已將正確的授權指派給使用者，以及已在授權的服務方案詳細資料中啟用該服務。
2. 確認使用者是否可以開啟 project.microsoft.com。
3. 確認系統是否指向正確的專案端點。
4. 確認是否已建立 Project 應用程式使用者。
5. 將下列資訊安全角色套用至使用者：
  
  - Dataverse 使用者或基本使用者
  - Project Operations 系統
  - Project 系統
  - Project Operations 雙重寫入系統 (如果您要部署資源/非庫存型案例適用的 Project Operations，就必須有此角色)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
