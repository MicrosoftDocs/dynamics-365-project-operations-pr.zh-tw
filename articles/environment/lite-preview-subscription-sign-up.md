---
title: 註冊預覽版訂閱
description: 本主題提供有關如何訂閱和部署「Project Operations Lite 部署 – 交易至開立預估發票」的資訊。
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948779"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>註冊「精簡部署 - 交易至開立預估發票」的預覽版訂閱

本主題說明如何訂閱預覽版合作夥伴供應項目，以及部署「Dynamics 365 Project Operations Lite 部署 – 交易至開立預估發票」。

> [!NOTE]
> 此程序將會在即將發行的 Project Operations 中變更。

## <a name="prerequisites"></a>先決條件

- 您將會收到電子郵件，邀請您參與預覽。 您可以在 [Project Operations 網站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上要求預覽。
- 部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。
- 部署預覽版的使用者需要電話號碼和有效信用卡。 註冊期間有六個月不會對此信用卡收費。 六個月過後，您需要取消訂閱。 
- 檢閱所有條款及條件。

## <a name="subscribe"></a>訂閱

獲得[預覽要求](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)核准時，您將會收到 Microsoft 透過電子郵件提供的兩個供應項目。 這些供應項目可讓您部署 Project Operations 預覽：

- Dynamics 365 Customer Service 預覽版試用 – 一次性驗證碼
- Dynamics 365 Project Operations – 預覽版試用

### <a name="dynamics-365-customer-service-paid-offer"></a>Dynamics 365 Customer Service 付費供應項目

1. 使用 InPrivate/Incognito 瀏覽器視窗，以第一個供應項目代碼來兌換 Dynamics 365 Customer Service。 若要註冊 Customer Service，您需要：

- 電話號碼
- 信用卡。 註冊時，有六個月期間不會對此信用卡收費。 六個月過後，您需要取消訂閱。
- 檢閱所有條款及條件。

2. 提供您的連絡資訊。

![連絡人資訊](./media/1ContactInformation.png)

3. 提供新的租用戶詳細資料。

![建立使用者識別碼](./media/2CreateUserID.png)

4. 確認您的身分識別、儲存新的使用者識別碼，然後選取**設定**。

![儲存資訊](./media/3SaveInfo.png)

5. 完成信用卡註冊，並檢閱所有條款及條件。 

![完整信用卡](./media/4CompleteCreditCard.png)

![信用卡結帳](./media/5CreditCardCheckout.png)

![儲存訂單](./media/6SaveOrder.png)

![信用卡資訊](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>取消 Dynamics 365 Customer Service Enterprise 供應項目

Dynamics 365 Customer Service Enterprise 供應項目提供六個月的免費期間。 此供應項目將在六個月期間結束時續約。 若要在續約日期之前取消，請完成下列指示。 

> [!NOTE]
> 完成這些步驟之後，就無法再使用 Project Operations 公開預覽環境。

1. 前往[管理入口網站](https://admin.microsoft.com/)，並在**帳務**底下選取**您的產品**。

![管理入口網站、您的產品頁面](./media/8AdminPortal.png)

2. 選取 **Dynamics 365 Customer Service Enterprise 供應項目**。

![取消訂閱](./media/9CancelSubscription.png)

3. 選取**設定** > **動作** > **取消訂閱**。
4. 在**訂閱取消**表單的必要欄位中輸入資訊。
5. 選取**取消** > **訂閱**。

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – 預覽版試用

1. 使用歡迎電子郵件中提供的 URL 來兌換第二個供應項目 Dynamics 365 Project Operations 試用版。

![兌換供應項目 2](./media/10RedeemOffer2.png)

2. 確認您是否以屬於使用第一個代碼進行訂閱之相同組織的使用者身分登入，然後繼續兌換供應項目。 
3. 選取**是，將它新增至我的帳戶**。

![新增至帳戶](./media/11AddToAccount.png)

![[立即試用] 畫面](./media/12TryNow.png)

![訂單詳細資料](./media/13Confirmation.png)

## <a name="assign-licenses"></a>指派授權

> [!IMPORTANT]
> 您需要組織的 Office 365 入口網站系統管理存取權，才能完成下列步驟。

1. 前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給您的使用者。

![系統管理中心首頁](./media/14AdminPortal.png)

2. 在**使用中使用者**頁面上，選取要將授權指派給的使用者。

![指派授權](./media/15AssignLicenses.png)

3. 確認是否已選取 **Customer Service Enterprise** 和 **Project Operations** 授權，然後選取**儲存變更**。

## <a name="create-a-new-cds-environment"></a>建立新的 CDS 環境

依照主題 [CDS 部署模型](lite-deployment.md)中的指示，佈建新的 Project Operations CDS 部署環境。

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>安裝 CDS 設定並設定示範資料

依照主題[套用示範設定和設定資料](lite-apply-demo-setup-config-data.md)中的指示，安裝 CDS 設定並設定示範資料。
