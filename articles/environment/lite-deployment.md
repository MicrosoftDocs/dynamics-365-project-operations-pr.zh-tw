---
title: 部署 Project Operations - 精簡
description: 本主題提供有關如何安裝「Project Operations Lite 部署 – 交易至開立預估發票」的資訊。
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950254"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="0acc1-103">部署 Project Operations - 精簡</span><span class="sxs-lookup"><span data-stu-id="0acc1-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="0acc1-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="0acc1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0acc1-105">Project Operations 支援多個部署模型。</span><span class="sxs-lookup"><span data-stu-id="0acc1-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="0acc1-106">若要判斷最佳部署模型，請參閱[部署類型](determine-deployment-type.md)。</span><span class="sxs-lookup"><span data-stu-id="0acc1-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="0acc1-107">此部署 (精簡部署 – 交易至開立預估發票) 會產生 **Project Operations 的只有 Common Data Service 部署專**。</span><span class="sxs-lookup"><span data-stu-id="0acc1-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="0acc1-108">將 Project Operations 安裝到新的 CDS 環境中</span><span class="sxs-lookup"><span data-stu-id="0acc1-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="0acc1-109">安裝到現有的 CDS 環境中</span><span class="sxs-lookup"><span data-stu-id="0acc1-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="0acc1-110">將 Project Operations 安裝到新的 CDS 環境</span><span class="sxs-lookup"><span data-stu-id="0acc1-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="0acc1-111">以持有 Project Operations 授權的 [全域和 Power Platform 管理員](/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)建立新的 CDS 環境。</span><span class="sxs-lookup"><span data-stu-id="0acc1-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="0acc1-112">請確定 **CDS 資料庫** 和 **Dynamics 365 應用程式** 已啟用。</span><span class="sxs-lookup"><span data-stu-id="0acc1-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="0acc1-113">如需詳細資訊，請參閱[在 Power Platform 系統管理中心建立和管理環境](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)。</span><span class="sxs-lookup"><span data-stu-id="0acc1-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="0acc1-114">從 Dynamics 365 應用程式的部署清單中，選取 **Microsoft Dynamics 365 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="0acc1-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="0acc1-115">將 Project Operations 安裝到現有的 CDS 環境</span><span class="sxs-lookup"><span data-stu-id="0acc1-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="0acc1-116">以持有 Project Operations 授權的[全域或 Power Platform 管理員](/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在您要安裝 Project Operations 所在的 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)尋找環境。</span><span class="sxs-lookup"><span data-stu-id="0acc1-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="0acc1-117">從 Dynamics 365 應用程式的部署清單中，安裝 **Microsoft Dynamics 365 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="0acc1-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="0acc1-118">如需詳細資訊，請參閱[管理 Dynamics 365 應用程式](/power-platform/admin/manage-apps)。</span><span class="sxs-lookup"><span data-stu-id="0acc1-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]