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
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="860dd-103">註冊資源/非庫存案例適用的 Project Operations 預覽版訂閱</span><span class="sxs-lookup"><span data-stu-id="860dd-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="860dd-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="860dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="860dd-105">本主題說明如何訂閱預覽/合作夥伴供應項目，以及部署資源/非庫存型案例適用的 Project Operations 環境。</span><span class="sxs-lookup"><span data-stu-id="860dd-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="860dd-106">先決條件</span><span class="sxs-lookup"><span data-stu-id="860dd-106">Prerequisites</span></span>

- <span data-ttu-id="860dd-107">您將會收到電子郵件，邀請您參與預覽。</span><span class="sxs-lookup"><span data-stu-id="860dd-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="860dd-108">您可以在 [Project Operations 網站](https://dynamics.microsoft.com/en-us/project-operations/overview/)上要求預覽。</span><span class="sxs-lookup"><span data-stu-id="860dd-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="860dd-109">部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。</span><span class="sxs-lookup"><span data-stu-id="860dd-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="860dd-110">部署 Finance 環境需要按環境計費的有效 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="860dd-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="860dd-111">您可以使用組織現有的訂閱，或使用 [Azure 試用版](https://azure.microsoft.com/en-us/free/)來開始進行。</span><span class="sxs-lookup"><span data-stu-id="860dd-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="860dd-112">CDS 環境會在有限的 30 天期間免費提供。</span><span class="sxs-lookup"><span data-stu-id="860dd-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="860dd-113">訂閱</span><span class="sxs-lookup"><span data-stu-id="860dd-113">Subscribe</span></span>

<span data-ttu-id="860dd-114">您的[預覽要求](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u)獲得核准時，將會收到 Microsoft 透過電子郵件提供的兩個供應項目。</span><span class="sxs-lookup"><span data-stu-id="860dd-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="860dd-115">這些供應項目可讓您部署 Project Operations 預覽：</span><span class="sxs-lookup"><span data-stu-id="860dd-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="860dd-116">Dynamics 365 Project Operations – 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="860dd-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="860dd-117">Dynamics 365 for Finance and Operations 預覽版試用。</span><span class="sxs-lookup"><span data-stu-id="860dd-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="860dd-118">組織中只有一個人 (租用戶管理員) 需要執行這項工作。</span><span class="sxs-lookup"><span data-stu-id="860dd-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="860dd-119">如果您不是此版本的訂閱者，請等到您的組織已註冊，而您收到您的使用者認證之後再說。</span><span class="sxs-lookup"><span data-stu-id="860dd-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="860dd-120">Dynamics 365 Project Operations – 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="860dd-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="860dd-121">使用歡迎電子郵件中提供的 URL 來兌換第一個供應項目 **Dynamics 365 Project Operations 試用版**。</span><span class="sxs-lookup"><span data-stu-id="860dd-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![第一個供應項目](./media/1FirstOffer.png)

2. <span data-ttu-id="860dd-123">確認您是以屬於負責訂閱服務之組織的使用者身分登入。</span><span class="sxs-lookup"><span data-stu-id="860dd-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="860dd-124">繼續兌換供應項目。</span><span class="sxs-lookup"><span data-stu-id="860dd-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="860dd-125">選取**是，將它新增至我的帳戶**。</span><span class="sxs-lookup"><span data-stu-id="860dd-125">Select **Yes, add it to my account**.</span></span>

![兌換供應項目](./media/2RedeemFirstOffer.png)

![確認供應項目](./media/3ConfirmFirstOffer.png)

![供應項目已兌換](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="860dd-129">Dynamics 365 Finance 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="860dd-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="860dd-130">重複同樣的步驟，取得歡迎電子郵件中提供的第二個供應項目。</span><span class="sxs-lookup"><span data-stu-id="860dd-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="860dd-131">指派授權</span><span class="sxs-lookup"><span data-stu-id="860dd-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="860dd-132">您需要組織的 Office 365 入口網站系統管理存取權，才能完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="860dd-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="860dd-133">前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給您的使用者。</span><span class="sxs-lookup"><span data-stu-id="860dd-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Office 管理入口網站](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="860dd-135">在**使用中使用者**頁面上，選取要將授權指派給的使用者。</span><span class="sxs-lookup"><span data-stu-id="860dd-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![指派授權](./media/6AssignLicenses.png)

3. <span data-ttu-id="860dd-137">確認是否已選取 Project Operations 授權，然後選取**儲存變更**。</span><span class="sxs-lookup"><span data-stu-id="860dd-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="860dd-138">Finance 試用版供應項目不需要指派給使用者。</span><span class="sxs-lookup"><span data-stu-id="860dd-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="860dd-139">在 LCS 中開始新專案</span><span class="sxs-lookup"><span data-stu-id="860dd-139">Start a new project in LCS</span></span>

<span data-ttu-id="860dd-140">建立新的 LCS 專案，如[在 LCS 中開始新專案](create-lcs-project.md)主題中所述</span><span class="sxs-lookup"><span data-stu-id="860dd-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="860dd-141">將 Azure 訂閱新增至 LCS 專案</span><span class="sxs-lookup"><span data-stu-id="860dd-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="860dd-142">若要完成此工作，請依照主題[將 Azure 訂閱新增至 LCS 專案](resource-add-azure-subscription-lcs-project.md)中的步驟進行。</span><span class="sxs-lookup"><span data-stu-id="860dd-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="860dd-143">使用資源/非庫存案例適用的 Project Operations 部署 Finance 示範環境</span><span class="sxs-lookup"><span data-stu-id="860dd-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="860dd-144">依照主題[佈建新環境](resource-provision-new-environment.md)中的指引完成部署。</span><span class="sxs-lookup"><span data-stu-id="860dd-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="860dd-145">使用[示範環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)部署類型以進行預覽。</span><span class="sxs-lookup"><span data-stu-id="860dd-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="860dd-146">安裝 CDS 設定和設定資料</span><span class="sxs-lookup"><span data-stu-id="860dd-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="860dd-147">安裝 CDS 設定和設定資料，如主題[設定和套用 Common Data Service 中的設定資料](resource-apply-pro-setup-config-data.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="860dd-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

