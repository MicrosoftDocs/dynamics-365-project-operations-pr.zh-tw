---
title: 註冊資源/非庫存案例適用的 Project Operations 預覽版訂閱
description: 本主題提供有關如何訂閱和部署資源/非庫存型案例適用 Project Operations 的資訊。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948782"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>註冊資源/非庫存案例適用的 Project Operations 預覽版訂閱

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本主題說明如何訂閱預覽/合作夥伴供應項目，以及部署資源/非庫存型案例適用的 Project Operations 環境。

## <a name="prerequisites"></a>先決條件

- 您將會收到電子郵件，邀請您參與預覽。 您可以在 [Project Operations 網站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上要求預覽。
- 部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。
- 部署 Finance 環境需要按環境計費的有效 Azure 訂閱。 您可以使用組織現有的訂閱，或使用 [Azure 試用版](https://azure.microsoft.com/en-us/free/)來開始進行。 CDS 環境會在有限的 30 天期間免費提供。

## <a name="subscribe"></a>訂閱

您的[預覽要求](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)獲得核准時，將會收到 Microsoft 透過電子郵件提供的兩個供應項目。 這些供應項目可讓您部署 Project Operations 預覽：

- Dynamics 365 Project Operations – 預覽版試用
- Dynamics 365 for Finance and Operations 預覽版試用。

> [!IMPORTANT]
> 組織中只有一個人 (租用戶管理員) 需要執行這項工作。 如果您不是此版本的訂閱者，請等到您的組織已註冊，而您收到您的使用者認證之後再說。

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – 預覽版試用

1. 使用歡迎電子郵件中提供的 URL 來兌換第一個供應項目 **Dynamics 365 Project Operations 試用版**。

![第一個供應項目](./media/1FirstOffer.png)

2. 確認您是以屬於負責訂閱服務之組織的使用者身分登入。
3. 繼續兌換供應項目。 
4. 選取**是，將它新增至我的帳戶**。

![兌換供應項目](./media/2RedeemFirstOffer.png)

![確認供應項目](./media/3ConfirmFirstOffer.png)

![供應項目已兌換](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance 預覽版試用

重複同樣的步驟，取得歡迎電子郵件中提供的第二個供應項目。

## <a name="assign-licenses"></a>指派授權

> [!IMPORTANT]
> 您需要組織的 Office 365 入口網站系統管理存取權，才能完成下列步驟。

1. 前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給您的使用者。

![Office 管理入口網站](./media/5OfficeAdminPortal.png)

2. 在**使用中使用者**頁面上，選取要將授權指派給的使用者。

![指派授權](./media/6AssignLicenses.png)

3. 確認是否已選取 Project Operations 授權，然後選取**儲存變更**。 

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

