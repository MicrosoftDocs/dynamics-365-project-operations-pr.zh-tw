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
ms.openlocfilehash: 0af8067fc0673890a317ac6f4e62d74b7f4eebca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290079"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="975d5-103">部署 Project Operations - 精簡</span><span class="sxs-lookup"><span data-stu-id="975d5-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="975d5-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="975d5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="975d5-105">Project Operations 支援多個部署模型。</span><span class="sxs-lookup"><span data-stu-id="975d5-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="975d5-106">若要判斷最佳部署模型，請參閱[部署類型](determine-deployment-type.md)。</span><span class="sxs-lookup"><span data-stu-id="975d5-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="975d5-107">此部署 (精簡部署 – 交易至開立預估發票) 會產生 **Project Operations 的只有 Common Data Service 部署專**。</span><span class="sxs-lookup"><span data-stu-id="975d5-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="975d5-108">將 Project Operations 安裝到新的 CDS 環境中</span><span class="sxs-lookup"><span data-stu-id="975d5-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="975d5-109">安裝到現有的 CDS 環境中</span><span class="sxs-lookup"><span data-stu-id="975d5-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="975d5-110">將 Project Operations 安裝到新的 CDS 環境</span><span class="sxs-lookup"><span data-stu-id="975d5-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="975d5-111">以持有 Project Operations 授權的 [全域和 Power Platform 管理員](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)建立新的 CDS 環境。</span><span class="sxs-lookup"><span data-stu-id="975d5-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="975d5-112">請確定 **CDS 資料庫** 和 **Dynamics 365 應用程式** 已啟用。</span><span class="sxs-lookup"><span data-stu-id="975d5-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="975d5-113">如需詳細資訊，請參閱[在 Power Platform 系統管理中心建立和管理環境](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)。</span><span class="sxs-lookup"><span data-stu-id="975d5-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="975d5-114">從 Dynamics 365 應用程式的部署清單中，選取 **Microsoft Dynamics 365 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="975d5-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="975d5-115">將 Project Operations 安裝到現有的 CDS 環境</span><span class="sxs-lookup"><span data-stu-id="975d5-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="975d5-116">以持有 Project Operations 授權的[全域或 Power Platform 管理員](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在您要安裝 Project Operations 所在的 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)尋找環境。</span><span class="sxs-lookup"><span data-stu-id="975d5-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="975d5-117">從 Dynamics 365 應用程式的部署清單中，安裝 **Microsoft Dynamics 365 Project Operations**。</span><span class="sxs-lookup"><span data-stu-id="975d5-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="975d5-118">如需詳細資訊，請參閱[管理 Dynamics 365 應用程式](https://docs.microsoft.com/power-platform/admin/manage-apps)。</span><span class="sxs-lookup"><span data-stu-id="975d5-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]