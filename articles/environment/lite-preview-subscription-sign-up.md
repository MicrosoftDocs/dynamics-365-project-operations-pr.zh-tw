---
title: 註冊預覽版訂閱 - 精簡
description: 本主題提供有關如何訂閱和部署「Project Operations Lite 部署 – 交易至開立預估發票」的資訊。
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175881"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>註冊預覽版訂閱 - 精簡 

本主題說明如何訂閱預覽版合作夥伴供應項目，以及部署「Dynamics 365 Project Operations Lite 部署 – 交易至開立預估發票」。

> [!NOTE]
> 此程序將會在即將發行的 Project Operations 中變更。

## <a name="prerequisites"></a>先決條件

- 您將收到電子郵件，邀請您參與預覽。 您可以在 [Project Operations 網站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上要求預覽。
- 部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。
- 檢閱所有條款及條件。

## <a name="subscribe"></a>訂閱

獲得[預覽要求](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)核准時，您會收到 Microsoft 透過電子郵件提供的兩個供應項目。 這些供應項目可讓您部署 Project Operations 預覽：

- Dynamics 365 Project Operations (CRM) - 預覽版試用
- Office 365 Project Operations - 預覽版試用

> [!IMPORTANT]
> 組織中只有一個人 (租用戶管理員) 需要執行這項工作。 如果您不是此版本的訂閱者，請等到您的組織已註冊，而您收到您的使用者認證之後再說。

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - 預覽版試用 

開始之前，請確定您已使用您要預覽 Project Operations 所在租用戶中的使用者公司帳戶來登入瀏覽器。

1. 在瀏覽器 URL 中貼上第一個供應項目代碼 **Dynamics 365 Project Operations (CRM) - 預覽版試用** 以進行兌換。

![兌換供應項目](./media/16RedeemFirstOfferNew.png)

2. 確認您的訂閱。
![確認訂單](./media/17ConfirmOrderNew.png)

您將會看到已成功兌換供應項目的確認。

![確認](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - 預覽版試用

重複與第一個供應項目代碼所用相同的步驟。 請務必使用與第一個供應項目代碼所用相同的使用者帳戶來新增第二個供應項目代碼。

## <a name="assign-licenses"></a>指派授權

> [!IMPORTANT]
> 您需要組織的 Microsoft 365 入口網站系統管理存取權，才能完成下列步驟。


1. 前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給您的使用者。

![系統管理中心首頁](./media/14AdminPortal.png)

2. 在 **使用中使用者** 頁面上，選取要將授權指派給的使用者。

![指派授權](./media/15AssignLicenses.png)

3. 確認是否已選取 **Dynamics 365 Project Operations (CRM) 預覽** 及 **Office 365 Project Operations - 預覽** 授權。 
4. 選取 **儲存變更**。

## <a name="create-a-new-cds-environment"></a>建立新的 CDS 環境

1. 依照主題 [CDS 部署模型](lite-deployment.md)中的指示，佈建新的 Project Operations CDS 部署環境。 選取環境類型時，請務必使用 **試用 (以訂閱為準)**。
![新環境](./media/19CreateEnvironment.png)

2. 選取 **啟用 Dynamics 365 應用程式** 設定，並讓 **自動部署這些應用程式** 保持空白。  
3. 選取 **儲存** 以建立環境。

![新增資料庫](./media/20CreateEnvironment1.png)

4. 建立環境之後，安裝 **Microsoft Dynamics 365 Project Operations** 解決方案。 

![安裝解決方案](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>安裝 CDS 設定並設定示範資料

依照主題[套用示範設定和設定資料](lite-apply-demo-setup-config-data.md)中的指示，安裝 CDS 設定並設定示範資料。
