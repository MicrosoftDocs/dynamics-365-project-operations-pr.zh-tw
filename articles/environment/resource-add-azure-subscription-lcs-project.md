---
title: 將 Azure 訂閱新增至 LCS 專案
description: 本主題提供有關如何將您的 Azure 訂閱連接至 LCS 專案的資訊。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948781"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>將 Azure 訂閱新增至 LCS 專案

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

雲端託管的環境必須使用現有的 Azure 訂閱來進行部署。 本主題說明如何將現有的 Azure 訂閱連接至 LCS 專案。 

## <a name="grant-admin-consent"></a>授與管理員同意

1. 在 LCS 專案的**環境**區段中，選取 **Microsoft Azure 設定**。

![Microsoft Azure 設定](./media/1MicrosoftAzureSettings.png)

2. 在**專案設定**頁面的 **Azure 連接器**索引標籤上，選取**授權**。 這可讓環境部署至此專案。

![Azure 連接器](./media/2AzureConnectors.png)

3. 再次選取**授權**以提供管理員同意。

![授與管理員同意](./media/3GrantAdminConsent.png)

4. 接受權限要求。

![接受權限要求](./media/4AcceptPermissionRequest.png)

授權現已完成。 

![授權成功](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>提供 Dynamics 部署服務存取權給您的 Azure 訂閱

1. 前往 [Microsoft Azure 帳單](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade)，並選取您的訂閱。 Dynamics 部署服務必須存取此訂閱，才能部署環境。

![Azure 訂閱詳細資料](./media/6AzureSubscription.png)

2. 選取導覽窗格中的**存取控制 (IAM)**，然後選取**新增角色指派**。
3. 在右側滑桿中，選取**參與者角色**，然後在提供的清單中尋找並選取 **Dynamics 部署服務**。 
4. 選取**儲存**。

![訂閱存取](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>將訂閱連接器新增至 LCS 專案

1. 在 LCS 專案的 **Microsoft Azure 設定**頁面上，選取**新增**以新增連接器。
2. 輸入您的 Azure 訂閱識別碼。 您可以前往 [Azure 入口網站](https://ms.portal.azure.com/)，在畫面左下角的**設定**下方找到您的 Azure 訂閱識別碼。
3. 在**設定使用 Azure Resource Manager** 欄位中，選取**是**。
4. 請確定 Azure 訂閱 AAD 租用戶網域與您使用中網域擁有的 Azure 訂閱相符，然後選取**下一步**。
5. 在 **Microsoft Azure 設定**畫面上，選取**下一步**以確認。 如果在此畫面中收到錯誤，請返回本主題的[提供 Dynamics 部署服務存取權給您的 Azure 訂閱](#provide)一節，並確定您已完成所有的步驟。
6. 將 Azure 管理憑證下載到電腦中的本機資料夾，然後移至**設定** > **管理憑證**，將其上傳至 Azure 管理入口網站。 此憑證允許 LCS 代表您與 Azure 進行通訊。 如果使用者有權存取訂閱，您可以略過此步驟。
7. 選取**下一步**。
8. 選取要在其中進行部署的 Azure 區域，並選取接近您打算使用此系統所在位置的資料中心。
9.  選取**連接**。

您已成功連接 Azure 訂閱。 您現在可以部署 Dynamics 365 Finance 雲端託管的環境。


