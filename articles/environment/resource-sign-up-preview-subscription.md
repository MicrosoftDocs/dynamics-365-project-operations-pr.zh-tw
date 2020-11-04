---
title: 註冊資源/非庫存案例適用的 Project Operations 預覽版訂閱
description: 本主題提供有關如何訂閱和部署資源/非庫存型案例適用 Project Operations 的資訊。
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a03f021b1ae0a87dfc947976b8a16c8246e1684
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072882"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>註冊資源/非庫存案例適用的 Project Operations 預覽版訂閱

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本主題說明如何訂閱預覽/合作夥伴供應項目，以及部署資源/非庫存型案例適用的 Project Operations 環境。

## <a name="prerequisites"></a>先決條件

- 您將會收到電子郵件，邀請您參與預覽。 您可以在 [Project Operations 網站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上要求預覽。
- 部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。
- 部署 Finance 環境需要按環境計費的有效 Azure 訂閱。 您可以使用組織現有的訂閱，或使用 [Azure 試用版](https://azure.microsoft.com/en-us/free/)來開始進行。 CDS 環境會在有限的 30 天期間免費提供。

## <a name="subscribe"></a>訂閱

您的[預覽要求](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)獲得核准時，將會收到 Microsoft 透過電子郵件提供的三個供應項目。 這些供應項目可讓您部署 Project Operations 預覽：

- Dynamics 365 Project Operations (CRM) - 預覽版試用
- Office 365 Project Operations - 預覽版試用
- Dynamics 365 Finance - 預覽版試用

> [!IMPORTANT]
> 組織中只有一個人 (租用戶管理員) 需要執行這項工作。 如果您不是此版本的訂閱者，請等到您的組織已註冊，而您收到您的使用者認證之後再說。

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - 預覽版試用 

開始之前，請確定您已使用您要預覽 Project Operations 所在租用戶中的使用者公司帳戶來登入瀏覽器。

1. 在瀏覽器 URL 中貼上第一個供應項目代碼 **Dynamics 365 Project Operations (CRM) - 預覽版試用** 以進行兌換。

![兌換供應項目](./media/16RedeemFirstOfferNew.png)

2. 確認您的訂閱。

![確認訂單](./media/17ConfirmOrderNew.png)

您會看到已成功兌換供應項目的確認。

![確認](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - 預覽版試用

重複與第一個供應項目代碼所用相同的步驟。 請務必使用與第一個供應項目代碼所用相同的使用者帳戶來新增第二個供應項目代碼。

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance 預覽版試用

重複同樣的步驟，取得歡迎電子郵件中提供的最後一個供應項目。

## <a name="assign-licenses"></a>指派授權

> [!IMPORTANT]
> 您需要組織的 Microsoft 365 入口網站系統管理存取權，才能完成下列步驟。

1. 前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給您的使用者。

![系統管理中心首頁](./media/14AdminPortal.png)

2. 在 **使用中使用者** 頁面上，選取要將授權指派給的使用者。

![指派授權](./media/15AssignLicenses.png)

3. 確認是否已選取 **Dynamics 365 Project Operations (CRM) 預覽** 及 **Office 365 Project Operations - 預覽** 授權，然後選取 **儲存變更** 。

> [!NOTE]
> Finance 試用版供應項目不需要指派給使用者。

## <a name="start-a-new-project-in-lcs"></a>在 LCS 中開始新專案

建立新的 LCS 專案，如[在 LCS 中開始新專案](create-lcs-project.md)主題中所述

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>將 Azure 訂閱新增至 LCS 專案

若要完成此工作，請依照主題[將 Azure 訂閱新增至 LCS 專案](resource-add-azure-subscription-lcs-project.md)中的步驟進行。

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>使用資源/非庫存案例適用的 Project Operations 部署 Finance 示範環境

依照主題[佈建新環境](resource-provision-new-environment.md)中的指引完成部署。 使用[示範環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)部署類型以進行預覽。 

## <a name="install-cds-setup-and-configuration-data"></a>安裝 CDS 設定和設定資料

安裝 CDS 設定和設定資料，如主題[設定和套用 Common Data Service 中的設定資料](resource-apply-pro-setup-config-data.md)中所述。
只有在部署了 Finance 示範環境，且 FO 中的示範資料準備就緒之後，才能完成此步驟。
