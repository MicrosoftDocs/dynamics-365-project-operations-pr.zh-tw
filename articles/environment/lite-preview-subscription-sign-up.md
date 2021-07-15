---
title: 註冊預覽版訂閱 - 精簡
description: 本主題提供有關如何訂閱和部署「Project Operations Lite 部署 – 交易至開立預估發票」的資訊。
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334772"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="cc41b-103">註冊預覽版訂閱 - 精簡</span><span class="sxs-lookup"><span data-stu-id="cc41b-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="cc41b-104">本主題說明如何訂閱試用版方案，以及部署 Dynamics 365 Project Operations 精簡部署 - 交易至開立預估發票。</span><span class="sxs-lookup"><span data-stu-id="cc41b-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="cc41b-105">此程序將會在即將發行的 Project Operations 中變更。</span><span class="sxs-lookup"><span data-stu-id="cc41b-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cc41b-106">先決條件</span><span class="sxs-lookup"><span data-stu-id="cc41b-106">Prerequisites</span></span>
- <span data-ttu-id="cc41b-107">部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。</span><span class="sxs-lookup"><span data-stu-id="cc41b-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="cc41b-108">您可以在第一個供應項目兌換期間建立租用戶。</span><span class="sxs-lookup"><span data-stu-id="cc41b-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc41b-109">組織中只有一個人 (租用戶管理員) 需要執行這項工作。</span><span class="sxs-lookup"><span data-stu-id="cc41b-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="cc41b-110">如果您不是此版本的訂閱者，請等到您的組織已註冊，而您收到您的使用者認證之後再說。</span><span class="sxs-lookup"><span data-stu-id="cc41b-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="cc41b-111">試用是在租用戶中單次使用。</span><span class="sxs-lookup"><span data-stu-id="cc41b-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="cc41b-112">您只能執行試用版一次。</span><span class="sxs-lookup"><span data-stu-id="cc41b-112">You can only run a trial one time.</span></span> <span data-ttu-id="cc41b-113">建議您基於試用目的建立新的租用戶。</span><span class="sxs-lookup"><span data-stu-id="cc41b-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="cc41b-114">Dynamics 365 Project Operations 試用版</span><span class="sxs-lookup"><span data-stu-id="cc41b-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="cc41b-115">開始之前，請確定您已使用您要預覽 Project Operations 所在租用戶中的使用者公司帳戶來登入瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="cc41b-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="cc41b-116">移至 [Project Operations 試用](https://aka.ms/try-po)以兌換第一個供應項目代碼 **Dynamics 365 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="cc41b-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="cc41b-117">確認您的訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc41b-117">Confirm your order.</span></span>

  <span data-ttu-id="cc41b-118">您會看到已成功兌換供應項目的確認。</span><span class="sxs-lookup"><span data-stu-id="cc41b-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="cc41b-119">指派授權</span><span class="sxs-lookup"><span data-stu-id="cc41b-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc41b-120">您需要組織的 Microsoft 365 入口網站系統管理存取權，才能完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="cc41b-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="cc41b-121">前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給您的使用者。</span><span class="sxs-lookup"><span data-stu-id="cc41b-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="cc41b-122">在 **使用中使用者** 頁面上，選取要將授權指派給的使用者。</span><span class="sxs-lookup"><span data-stu-id="cc41b-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="cc41b-123">確認是否已選取 **Dynamics 365 Project Operations** 授權。</span><span class="sxs-lookup"><span data-stu-id="cc41b-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="cc41b-124">選取 **儲存變更**。</span><span class="sxs-lookup"><span data-stu-id="cc41b-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="cc41b-125">建立新 Dataverse 環境</span><span class="sxs-lookup"><span data-stu-id="cc41b-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="cc41b-126">依照主題 [Dataverse 部署模型](lite-deployment.md)中的指示，佈建新的 Project Operations Dataverse 部署環境。</span><span class="sxs-lookup"><span data-stu-id="cc41b-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="cc41b-127">選取環境類型時，請務必使用 **試用 (以訂閱為準)**。</span><span class="sxs-lookup"><span data-stu-id="cc41b-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![新環境](./media/19CreateEnvironment.png)

2. <span data-ttu-id="cc41b-129">選取 **啟用 Dynamics 365 應用程式** 設定，並讓 **自動部署這些應用程式** 保持空白。</span><span class="sxs-lookup"><span data-stu-id="cc41b-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="cc41b-130">選取 **儲存** 以建立環境。</span><span class="sxs-lookup"><span data-stu-id="cc41b-130">Select **Save** to create the environment.</span></span>

  ![新增資料庫](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="cc41b-132">建立環境之後，安裝 **Microsoft Dynamics 365 Project Operations** 解決方案。</span><span class="sxs-lookup"><span data-stu-id="cc41b-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![安裝解決方案](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="cc41b-134">安裝 CDS 設定並設定示範資料</span><span class="sxs-lookup"><span data-stu-id="cc41b-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="cc41b-135">依照主題[套用示範設定和設定資料](lite-apply-demo-setup-config-data.md)中的指示，安裝 CDS 設定並設定示範資料。</span><span class="sxs-lookup"><span data-stu-id="cc41b-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
