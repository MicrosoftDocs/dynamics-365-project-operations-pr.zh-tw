---
title: 註冊預覽版訂閱 - 精簡
description: 本主題提供有關如何訂閱和部署「Project Operations Lite 部署 – 交易至開立預估發票」的資訊。
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3b06ac29e8021967490534d3aefc8b5ce733413b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587990"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>註冊預覽版訂閱 - 精簡 

本主題說明如何訂閱試用版方案，以及部署 Dynamics 365 Project Operations 精簡部署 - 交易至開立預估發票。

> [!NOTE]
> 此程序將會在即將發行的 Project Operations 中變更。

## <a name="prerequisites"></a>先決條件
- 部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。 您可以在第一個供應項目兌換期間建立租用戶。

> [!IMPORTANT]
> 組織中只有一個人 (租用戶管理員) 需要執行這項工作。 如果您不是此版本的訂閱者，請等到您的組織已註冊，而您收到您的使用者認證之後再說。
> 
> 試用是在租用戶中單次使用。 您只能執行試用版一次。 建議您基於試用目的建立新的租用戶。

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations 試用版 

開始之前，請確定您已使用您要預覽 Project Operations 所在租用戶中的使用者公司帳戶來登入瀏覽器。

1. 移至 [Project Operations 試用](https://aka.ms/try-po)以兌換第一個供應項目代碼 **Dynamics 365 Project Operations**。
2. 確認您的訂閱。

  您會看到已成功兌換供應項目的確認。

## <a name="assign-licenses"></a>指派授權

> [!IMPORTANT]
> 您需要組織的 Microsoft 365 入口網站系統管理存取權，才能完成下列步驟。


1. 前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給您的使用者。
2. 在 **使用中使用者** 頁面上，選取要將授權指派給的使用者。
3. 確認是否已選取 **Dynamics 365 Project Operations** 授權。 
4. 選取 **儲存變更**。

## <a name="create-a-new-dataverse-environment"></a>建立新 Dataverse 環境

1. 依照主題 [Dataverse 部署模型](lite-deployment.md)中的指示，佈建新的 Project Operations Dataverse 部署環境。 選取環境類型時，請務必使用 **試用 (以訂閱為準)**。

  ![新環境。](./media/19CreateEnvironment.png)

2. 選取 **啟用 Dynamics 365 應用程式** 設定，並讓 **自動部署這些應用程式** 保持空白。  
3. 選取 **儲存** 以建立環境。

  ![新增資料庫。](./media/20CreateEnvironment1.png)

4. 建立環境之後，安裝 **Microsoft Dynamics 365 Project Operations** 解決方案。 

![安裝解決方案。](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>安裝 CDS 設定並設定示範資料

依照主題[套用示範設定和設定資料](lite-apply-demo-setup-config-data.md)中的指示，安裝 CDS 設定並設定示範資料。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
