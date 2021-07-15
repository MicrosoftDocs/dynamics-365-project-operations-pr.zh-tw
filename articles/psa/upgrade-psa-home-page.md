---
title: 升級首頁
description: 本主題顯示到哪裡尋找有關 Dynamics 365 Project Service Automation 的新功能和其已變更功能的重要資訊，以及升級為最新版本的程序。
ms.prod: ''
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8fc820d8fa0e421cdc963f391133e7311de96982
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368511"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="0d710-103">升級首頁</span><span class="sxs-lookup"><span data-stu-id="0d710-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="0d710-104">從 PSA 2.x 或 1.x 版升級至 3.x 版</span><span class="sxs-lookup"><span data-stu-id="0d710-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="0d710-105">新的執行個體</span><span class="sxs-lookup"><span data-stu-id="0d710-105">New instances</span></span>

<span data-ttu-id="0d710-106">自 2019 年 5 月 17 日起，在佈建新執行個體期間選取 Project Service Automation 時，預設會安裝版本 3.x。</span><span class="sxs-lookup"><span data-stu-id="0d710-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="0d710-107">現有的執行個體</span><span class="sxs-lookup"><span data-stu-id="0d710-107">Existing instances</span></span>

<span data-ttu-id="0d710-108">先前擁有 PSA 2.x 版執行個體且需要升級至 3.x 版 (這是 PSA 的整合用戶端介面架構 (UCI) 版本) 的客戶，必須連絡 Microsoft 支援服務，並提供其執行個體的詳細資料，讓支援服務可以啟用執行個體以升級至版本 3. x。</span><span class="sxs-lookup"><span data-stu-id="0d710-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="0d710-109">自 2020 年 3 月 1 日起，擁有 PSA 2. x 版執行個體且需要升級至 3. x 版的客戶，可以直接從管理入口網站升級其執行個體，不需要連絡 Microsoft 支援服務。</span><span class="sxs-lookup"><span data-stu-id="0d710-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="0d710-110">PSA 3.x 版包含重大變更。</span><span class="sxs-lookup"><span data-stu-id="0d710-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="0d710-111">這已內建於整合介面架構，可協助您改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="0d710-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="0d710-112">重新設計的應用程式提供一致的整合使用者介面 (UI)，並遵循回應式設計原則，讓您在任何螢幕大小或裝置上都能看到最佳畫面。</span><span class="sxs-lookup"><span data-stu-id="0d710-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="0d710-113">整個應用程式已徹底進行了其他變更。</span><span class="sxs-lookup"><span data-stu-id="0d710-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="0d710-114">一些已有所變更的部分包括定價、預約以及指派資源、時間、費用和核准。</span><span class="sxs-lookup"><span data-stu-id="0d710-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="0d710-115">開始升級程序前，建議您完成下列工作：</span><span class="sxs-lookup"><span data-stu-id="0d710-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="0d710-116">確認是否 Dynamics 365 Field Service 和 Project Service Automation 都已安裝在已識別的執行個體。</span><span class="sxs-lookup"><span data-stu-id="0d710-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="0d710-117">如果這兩個解決方案都已安裝，您必須先規劃升級這兩項，再繼續正常使用該執行個體。</span><span class="sxs-lookup"><span data-stu-id="0d710-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="0d710-118">仔細檢閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="0d710-118">Carefully review the following topics.</span></span> <span data-ttu-id="0d710-119">知道並了解版本之間的變更將有助於進行您的升級程序。</span><span class="sxs-lookup"><span data-stu-id="0d710-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="0d710-120">這些主題提供有關 PSA 中主要變更的資訊，以及規劃升級至版本 3.x 的考量和建議。</span><span class="sxs-lookup"><span data-stu-id="0d710-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="0d710-121">Project Service Automation 版本 3 的新功能或變更</span><span class="sxs-lookup"><span data-stu-id="0d710-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="0d710-122">升級考量 - 從 Project Service Automation 2.x 或 1.x 版升級至版本 3</span><span class="sxs-lookup"><span data-stu-id="0d710-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="0d710-123">先升級沙箱執行個體以評估您的實作中的變更，然後再升級生產執行個體。</span><span class="sxs-lookup"><span data-stu-id="0d710-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="0d710-124">檢閱過前述主題並準備好升級至 PSA 3.x 版或 UCI 架構版本時，請送出要求至 Microsoft 支援服務，讓升級可在系統管理中心進行。</span><span class="sxs-lookup"><span data-stu-id="0d710-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="0d710-125">在要求中，提供您的執行個體的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0d710-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="0d710-126">新建立執行個體中的舊版 PSA (PSA 2.x 版)</span><span class="sxs-lookup"><span data-stu-id="0d710-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="0d710-127">自 2019 年 5 月 17 日起，所有新的執行個體都會有 UCI 做為預設用戶端。</span><span class="sxs-lookup"><span data-stu-id="0d710-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="0d710-128">為了配合這項變更，預設情況下會佈建 PSA 3.x 版和 Field Service 8.x 版，因為這些版本是專門設計來搭配 UCI 用戶端使用的。</span><span class="sxs-lookup"><span data-stu-id="0d710-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="0d710-129">自 2020 年 3 月 1 日起，Dynamics PSA 的客戶已無法建立含舊版 PSA (例如 PSA 2. x 版或更舊版本) 的新環境。</span><span class="sxs-lookup"><span data-stu-id="0d710-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="0d710-130">任何新的環境都只能取得 PSA 3.x 版。</span><span class="sxs-lookup"><span data-stu-id="0d710-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="0d710-131">為了在您使用舊版 Field Service 和 PSA 應用程式時獲得最佳體驗，請前往 **系統設定** 頁面，並針對 **僅使用新的整合介面 (建議使用)** 欄位選取 **否**，因為這些版本不是設計要在 UCI 中正確載入。</span><span class="sxs-lookup"><span data-stu-id="0d710-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="0d710-132">關閉 UCI 之後，您可以使用舊版 Web 用戶端，開啟並執行這些版本的 Field Service 和 PSA。</span><span class="sxs-lookup"><span data-stu-id="0d710-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]