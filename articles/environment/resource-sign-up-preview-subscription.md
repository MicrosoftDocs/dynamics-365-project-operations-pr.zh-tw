---
title: 註冊資源/非庫存案例適用的 Project Operations 預覽版訂閱
description: 本主題提供有關如何訂閱和部署資源/非庫存型案例適用 Project Operations 的資訊。
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334817"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="bf109-103">註冊資源/非庫存案例適用的 Project Operations 預覽版訂閱</span><span class="sxs-lookup"><span data-stu-id="bf109-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="bf109-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="bf109-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bf109-105">本主題說明如何訂閱試用版方案，以及部署資源/非庫存型案例適用的 Project Operations 環境。</span><span class="sxs-lookup"><span data-stu-id="bf109-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bf109-106">先決條件</span><span class="sxs-lookup"><span data-stu-id="bf109-106">Prerequisites</span></span>
- <span data-ttu-id="bf109-107">部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。</span><span class="sxs-lookup"><span data-stu-id="bf109-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="bf109-108">您可以在第一個供應項目兌換期間建立租用戶。</span><span class="sxs-lookup"><span data-stu-id="bf109-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="bf109-109">部署 Finance 環境需要按環境計費的有效 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf109-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="bf109-110">您可以使用組織現有的訂閱，或使用 [Azure 試用版](https://azure.microsoft.com/en-us/free/)來開始進行。</span><span class="sxs-lookup"><span data-stu-id="bf109-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="bf109-111">CDS 環境會在有限的 30 天期間免費提供。</span><span class="sxs-lookup"><span data-stu-id="bf109-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf109-112">組織中只有一個人 (租用戶管理員) 需要執行這項工作。</span><span class="sxs-lookup"><span data-stu-id="bf109-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="bf109-113">如果您不是此版本的訂閱者，請等到您的組織已註冊，而您收到您的使用者認證之後再說。</span><span class="sxs-lookup"><span data-stu-id="bf109-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="bf109-114">試用是在租用戶中單次使用。</span><span class="sxs-lookup"><span data-stu-id="bf109-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="bf109-115">您只能執行試用版一次。</span><span class="sxs-lookup"><span data-stu-id="bf109-115">You can only run a trial one time.</span></span> <span data-ttu-id="bf109-116">建議您基於試用目的建立新的租用戶。</span><span class="sxs-lookup"><span data-stu-id="bf109-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="bf109-117">Dynamics 365 Project Operations (CE) - 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="bf109-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="bf109-118">開始之前，請確定您已使用您要預覽 Project Operations 所在租用戶中的使用者公司帳戶來登入瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="bf109-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="bf109-119">在 [Project Operations 試用](https://aka.ms/try-po)這裡兌換第一個供應項目代碼 **Dynamics 365 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="bf109-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="bf109-120">確認您的訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf109-120">Confirm your order.</span></span>

  <span data-ttu-id="bf109-121">您會看到已成功兌換供應項目的確認。</span><span class="sxs-lookup"><span data-stu-id="bf109-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="bf109-122">Dynamics 365 Finance 預覽版試用</span><span class="sxs-lookup"><span data-stu-id="bf109-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="bf109-123">移至 [Dynamics 365 for Finance 預覽版試用](https://aka.ms/trypoche)，並對供應項目 [註冊雲端託管的環境] 重複上一節的步驟。</span><span class="sxs-lookup"><span data-stu-id="bf109-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="bf109-124">指派授權</span><span class="sxs-lookup"><span data-stu-id="bf109-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf109-125">您需要組織的 Microsoft 365 入口網站系統管理存取權，才能完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="bf109-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="bf109-126">前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給您的使用者。</span><span class="sxs-lookup"><span data-stu-id="bf109-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="bf109-127">在 **使用中使用者** 頁面上，選取要將授權指派給的使用者。</span><span class="sxs-lookup"><span data-stu-id="bf109-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="bf109-128">確認是否已選取 **Dynamics 365 Project Operations** 授權，並選取 **儲存變更**。</span><span class="sxs-lookup"><span data-stu-id="bf109-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="bf109-129">Finance 試用版供應項目不需要指派給使用者。</span><span class="sxs-lookup"><span data-stu-id="bf109-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="bf109-130">在 LCS 中開始新專案</span><span class="sxs-lookup"><span data-stu-id="bf109-130">Start a new project in LCS</span></span>

<span data-ttu-id="bf109-131">建立新的 LCS 專案，如[在 LCS 中開始新專案](create-lcs-project.md)主題中所述</span><span class="sxs-lookup"><span data-stu-id="bf109-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="bf109-132">將 Azure 訂閱新增至 LCS 專案</span><span class="sxs-lookup"><span data-stu-id="bf109-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="bf109-133">若要完成此工作，請依照主題[將 Azure 訂閱新增至 LCS 專案](resource-add-azure-subscription-lcs-project.md)中的步驟進行。</span><span class="sxs-lookup"><span data-stu-id="bf109-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="bf109-134">使用資源/非庫存案例適用的 Project Operations 部署 Finance 示範環境</span><span class="sxs-lookup"><span data-stu-id="bf109-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="bf109-135">依照主題[佈建新環境](resource-provision-new-environment.md)中的指引完成部署。</span><span class="sxs-lookup"><span data-stu-id="bf109-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="bf109-136">使用[示範環境](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)部署類型以進行預覽。</span><span class="sxs-lookup"><span data-stu-id="bf109-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="bf109-137">安裝 CDS 設定和設定資料</span><span class="sxs-lookup"><span data-stu-id="bf109-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="bf109-138">安裝 CDS 設定和設定資料，如主題[設定和套用 Common Data Service 中的設定資料](resource-apply-pro-setup-config-data.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="bf109-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="bf109-139">只有在部署 Finance 示範環境並準備好示範資料後，才可完成此步驟。</span><span class="sxs-lookup"><span data-stu-id="bf109-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
