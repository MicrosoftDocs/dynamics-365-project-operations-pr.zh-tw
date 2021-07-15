---
title: 手動部署支援雙重寫入的 Project Operations Dataverse 應用程式
description: 本主題說明如何手動部署 Project Operations Dataverse 應用程式，使其支援雙重寫入。
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273998"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="96590-103">手動部署支援雙重寫入的 Project Operations Dataverse 應用程式</span><span class="sxs-lookup"><span data-stu-id="96590-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="96590-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="96590-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="96590-105">本主題說明如何在 Microsoft Dataverse 中手動部署 Microsoft Dynamics 365 Project Operations，使其支援雙重寫入。</span><span class="sxs-lookup"><span data-stu-id="96590-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="96590-106">如果符合先決條件，Project Operations 就會偵測環境的設定，並新增對雙重寫入的額外支援。</span><span class="sxs-lookup"><span data-stu-id="96590-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="96590-107">透過 Microsoft Dynamics Lifecycle Services (LCS) 進行部署時，如果您已依照本主題中的指示操作，就可以跳過 Microsoft Power Platform 整合 (先前稱為 Common Data Service 環境) 的部署。</span><span class="sxs-lookup"><span data-stu-id="96590-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="96590-108">在 Dataverse 中部署 Project Operations 使其支援雙重寫入的步驟，有四個主要步驟：</span><span class="sxs-lookup"><span data-stu-id="96590-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="96590-109">[在 Dataverse 中建立支援雙重寫入的新環境](#create)。</span><span class="sxs-lookup"><span data-stu-id="96590-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="96590-110">[將雙重寫入先決條件新增至環境](#prerequisites)。</span><span class="sxs-lookup"><span data-stu-id="96590-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="96590-111">[新增 Project Operations Dataverse 應用程式](#dataverse)。</span><span class="sxs-lookup"><span data-stu-id="96590-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="96590-112">[連結您的環境](#link)。</span><span class="sxs-lookup"><span data-stu-id="96590-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="96590-113">在 Dataverse 中建立支援雙重寫入的新環境</span><span class="sxs-lookup"><span data-stu-id="96590-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="96590-114">若要完成此程序，必須以系統管理員身分登入。</span><span class="sxs-lookup"><span data-stu-id="96590-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="96590-115">開啟 [Power Platform 系統管理中心](https://admin.powerplatform.com)，並以系統管理員身分登入。</span><span class="sxs-lookup"><span data-stu-id="96590-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="96590-116">建立新環境，並將其命名。</span><span class="sxs-lookup"><span data-stu-id="96590-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="96590-117">選取環境類型。</span><span class="sxs-lookup"><span data-stu-id="96590-117">Select the environment type.</span></span> <span data-ttu-id="96590-118">如果您已註冊試用版方案，請選取 **試用 (以訂閱為準)**。</span><span class="sxs-lookup"><span data-stu-id="96590-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="96590-119">確認部署區域。</span><span class="sxs-lookup"><span data-stu-id="96590-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="96590-120">啟用 **建立此環境的資料庫** 選項。</span><span class="sxs-lookup"><span data-stu-id="96590-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="96590-121">確認語言，然後確認貨幣符合 Finance and Operations 應用程式的貨幣。</span><span class="sxs-lookup"><span data-stu-id="96590-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="96590-122">啟用 **Dynamics 365 應用程式** 選項，並確認 **自動部署這些應用程式** 欄位已設定為 **無**。</span><span class="sxs-lookup"><span data-stu-id="96590-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="96590-123">如果需要安全性群組，請新增安全性群組。</span><span class="sxs-lookup"><span data-stu-id="96590-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="96590-124">選取 **儲存** 以建立環境。</span><span class="sxs-lookup"><span data-stu-id="96590-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="96590-125">等待直到部署已完成，且環境達到 **就緒** 狀態。</span><span class="sxs-lookup"><span data-stu-id="96590-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="96590-126">將雙重寫入先決條件新增至環境</span><span class="sxs-lookup"><span data-stu-id="96590-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="96590-127">雙重寫入支援包含另外新增至主要實體 (例如 **公司** 實體) 的其他欄位。</span><span class="sxs-lookup"><span data-stu-id="96590-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="96590-128">如果您要將雙重寫入支援新增至現有環境，則可能需要更新資料才可啟用此支援。</span><span class="sxs-lookup"><span data-stu-id="96590-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="96590-129">如需有關如何啟動載入資料的詳細資訊，請參閱[啟動載入公司資料](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data)。</span><span class="sxs-lookup"><span data-stu-id="96590-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="96590-130">如需雙重寫入的詳細資訊，請參閱[雙重寫入系統需求](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req)。</span><span class="sxs-lookup"><span data-stu-id="96590-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="96590-131">完成此程序，以將雙重寫入先決條件新增至您的環境。</span><span class="sxs-lookup"><span data-stu-id="96590-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="96590-132">開啟剛才建立的環境，然後移至 **資源** \> **Dynamics 365 應用程式**。</span><span class="sxs-lookup"><span data-stu-id="96590-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="96590-133">選取應用程式清單中的 **雙重寫入核心解決方案**，並加以安裝。</span><span class="sxs-lookup"><span data-stu-id="96590-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="96590-134">等待直到完成安裝。</span><span class="sxs-lookup"><span data-stu-id="96590-134">Wait until the installation is completed.</span></span> <span data-ttu-id="96590-135">接著選取應用程式清單中的 **雙重寫入應用程式協調流程解決方案**，然後進行安裝。</span><span class="sxs-lookup"><span data-stu-id="96590-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="96590-136">新增 Project Operations Dataverse 應用程式</span><span class="sxs-lookup"><span data-stu-id="96590-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="96590-137">僅當您已在安裝 Project Operations 前完成先前程序時，才可完成此程序。</span><span class="sxs-lookup"><span data-stu-id="96590-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="96590-138">在安裝期間，系統會分析環境設定，並在需要時新增對雙重寫入的支援。</span><span class="sxs-lookup"><span data-stu-id="96590-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="96590-139">開啟先前建立的環境，然後移至 **資源** \> **Dynamics 365 應用程式**。</span><span class="sxs-lookup"><span data-stu-id="96590-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="96590-140">選取應用程式清單中的 **Microsoft Dynamics 365 Project Operations**，並加以安裝。</span><span class="sxs-lookup"><span data-stu-id="96590-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="96590-141">連結您的環境</span><span class="sxs-lookup"><span data-stu-id="96590-141">Link your environments</span></span>

<span data-ttu-id="96590-142">部署 Dataverse 環境後，您可以在 Finance and Operations 應用程式中設定連結。</span><span class="sxs-lookup"><span data-stu-id="96590-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="96590-143">請依照[使用雙重寫入精靈來連結您的環境](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment)中的步驟操作。</span><span class="sxs-lookup"><span data-stu-id="96590-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
