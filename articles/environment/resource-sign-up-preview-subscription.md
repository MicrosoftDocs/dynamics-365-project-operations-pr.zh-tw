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
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="8339a-103">註冊資源/非庫存案例適用的 Project Operations 預覽版訂閱</span><span class="sxs-lookup"><span data-stu-id="8339a-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="8339a-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="8339a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8339a-105">本主題說明如何訂閱預覽/合作夥伴供應項目，以及部署資源/非庫存型案例適用的 Project Operations 環境。</span><span class="sxs-lookup"><span data-stu-id="8339a-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8339a-106">先決條件</span><span class="sxs-lookup"><span data-stu-id="8339a-106">Prerequisites</span></span>

- <span data-ttu-id="8339a-107">您將會收到電子郵件，邀請您參與預覽。</span><span class="sxs-lookup"><span data-stu-id="8339a-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="8339a-108">您可以在 [Project Operations 網站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上要求預覽。</span><span class="sxs-lookup"><span data-stu-id="8339a-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="8339a-109">部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。</span><span class="sxs-lookup"><span data-stu-id="8339a-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="8339a-110">部署 Finance 環境需要按環境計費的有效 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="8339a-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="8339a-111">您可以使用組織現有的訂閱，或使用 [Azure 試用版](https://azure.microsoft.com/en-us/free/)來開始進行。</span><span class="sxs-lookup"><span data-stu-id="8339a-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="8339a-112">CDS 環境會在有限的 30 天期間免費提供。</span><span class="sxs-lookup"><span data-stu-id="8339a-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="8339a-113">訂閱</span><span class="sxs-lookup"><span data-stu-id="8339a-113">Subscribe</span></span>

<span data-ttu-id="8339a-114">您的[預覽要求](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)獲得核准時，將會收到 Microsoft 透過電子郵件提供的三個供應項目。</span><span class="sxs-lookup"><span data-stu-id="8339a-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="8339a-115">這些供應項目可讓您部署 Project Operations 預覽：</span><span class="sxs-lookup"><span data-stu-id="8339a-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="8339a-116">Dynamics 365 Project Operations (CRM) - 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="8339a-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="8339a-117">Office 365 Project Operations - 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="8339a-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="8339a-118">Dynamics 365 Finance - 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="8339a-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8339a-119">組織中只有一個人 (租用戶管理員) 需要執行這項工作。</span><span class="sxs-lookup"><span data-stu-id="8339a-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="8339a-120">如果您不是此版本的訂閱者，請等到您的組織已註冊，而您收到您的使用者認證之後再說。</span><span class="sxs-lookup"><span data-stu-id="8339a-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="8339a-121">Dynamics 365 Project Operations (CRM) - 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="8339a-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="8339a-122">開始之前，請確定您已使用您要預覽 Project Operations 所在租用戶中的使用者公司帳戶來登入瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="8339a-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="8339a-123">在瀏覽器 URL 中貼上第一個供應項目代碼 **Dynamics 365 Project Operations (CRM) - 預覽版試用** 以進行兌換。</span><span class="sxs-lookup"><span data-stu-id="8339a-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![兌換供應項目](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="8339a-125">確認您的訂閱。</span><span class="sxs-lookup"><span data-stu-id="8339a-125">Confirm your order.</span></span>

![確認訂單](./media/17ConfirmOrderNew.png)

<span data-ttu-id="8339a-127">您會看到已成功兌換供應項目的確認。</span><span class="sxs-lookup"><span data-stu-id="8339a-127">You will see confirmation offer was successfully redeemed.</span></span>

![確認](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="8339a-129">Office 365 Project Operations - 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="8339a-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="8339a-130">重複與第一個供應項目代碼所用相同的步驟。</span><span class="sxs-lookup"><span data-stu-id="8339a-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="8339a-131">請務必使用與第一個供應項目代碼所用相同的使用者帳戶來新增第二個供應項目代碼。</span><span class="sxs-lookup"><span data-stu-id="8339a-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="8339a-132">Dynamics 365 Finance 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="8339a-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="8339a-133">重複同樣的步驟，取得歡迎電子郵件中提供的最後一個供應項目。</span><span class="sxs-lookup"><span data-stu-id="8339a-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="8339a-134">指派授權</span><span class="sxs-lookup"><span data-stu-id="8339a-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8339a-135">您需要組織的 Microsoft 365 入口網站系統管理存取權，才能完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="8339a-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="8339a-136">前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給您的使用者。</span><span class="sxs-lookup"><span data-stu-id="8339a-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![系統管理中心首頁](./media/14AdminPortal.png)

2. <span data-ttu-id="8339a-138">在 **使用中使用者** 頁面上，選取要將授權指派給的使用者。</span><span class="sxs-lookup"><span data-stu-id="8339a-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![指派授權](./media/15AssignLicenses.png)

3. <span data-ttu-id="8339a-140">確認是否已選取 **Dynamics 365 Project Operations (CRM) 預覽** 及 **Office 365 Project Operations - 預覽** 授權，然後選取 **儲存變更** 。</span><span class="sxs-lookup"><span data-stu-id="8339a-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="8339a-141">Finance 試用版供應項目不需要指派給使用者。</span><span class="sxs-lookup"><span data-stu-id="8339a-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="8339a-142">在 LCS 中開始新專案</span><span class="sxs-lookup"><span data-stu-id="8339a-142">Start a new project in LCS</span></span>

<span data-ttu-id="8339a-143">建立新的 LCS 專案，如[在 LCS 中開始新專案](create-lcs-project.md)主題中所述</span><span class="sxs-lookup"><span data-stu-id="8339a-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="8339a-144">將 Azure 訂閱新增至 LCS 專案</span><span class="sxs-lookup"><span data-stu-id="8339a-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="8339a-145">若要完成此工作，請依照主題[將 Azure 訂閱新增至 LCS 專案](resource-add-azure-subscription-lcs-project.md)中的步驟進行。</span><span class="sxs-lookup"><span data-stu-id="8339a-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="8339a-146">使用資源/非庫存案例適用的 Project Operations 部署 Finance 示範環境</span><span class="sxs-lookup"><span data-stu-id="8339a-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="8339a-147">依照主題[佈建新環境](resource-provision-new-environment.md)中的指引完成部署。</span><span class="sxs-lookup"><span data-stu-id="8339a-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="8339a-148">使用[示範環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)部署類型以進行預覽。</span><span class="sxs-lookup"><span data-stu-id="8339a-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="8339a-149">安裝 CDS 設定和設定資料</span><span class="sxs-lookup"><span data-stu-id="8339a-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="8339a-150">安裝 CDS 設定和設定資料，如主題[設定和套用 Common Data Service 中的設定資料](resource-apply-pro-setup-config-data.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="8339a-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="8339a-151">只有在部署了 Finance 示範環境，且 FO 中的示範資料準備就緒之後，才能完成此步驟。</span><span class="sxs-lookup"><span data-stu-id="8339a-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>
