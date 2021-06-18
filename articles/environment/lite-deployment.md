---
title: 部署 Project Operations - 精簡
description: 本主題提供有關如何安裝「Project Operations Lite 部署 – 交易至開立預估發票」的資訊。
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995521"
---
# <a name="deploy-project-operations---lite"></a>部署 Project Operations - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations 支援多個部署模型。 若要判斷最佳部署模型，請參閱[部署類型](determine-deployment-type.md)。


> [!IMPORTANT]
> 此部署 (精簡部署 – 交易至開立預估發票) 會產生 **Project Operations 的只有 Common Data Service 部署專**。

- [將 Project Operations 安裝到新的 CDS 環境中](#new)
- [安裝到現有的 CDS 環境中](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>將 Project Operations 安裝到新的 CDS 環境

1. 以持有 Project Operations 授權的 [全域和 Power Platform 管理員](/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)建立新的 CDS 環境。 請確定 **CDS 資料庫** 和 **Dynamics 365 應用程式** 已啟用。 如需詳細資訊，請參閱[在 Power Platform 系統管理中心建立和管理環境](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)。
2. 從 Dynamics 365 應用程式的部署清單中，選取 **Microsoft Dynamics 365 Project Operations**。


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>將 Project Operations 安裝到現有的 CDS 環境

1. 以持有 Project Operations 授權的[全域或 Power Platform 管理員](/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在您要安裝 Project Operations 所在的 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)尋找環境。
2. 從 Dynamics 365 應用程式的部署清單中，安裝 **Microsoft Dynamics 365 Project Operations**。 如需詳細資訊，請參閱[管理 Dynamics 365 應用程式](/power-platform/admin/manage-apps)。




[!INCLUDE[footer-include](../includes/footer-banner.md)]