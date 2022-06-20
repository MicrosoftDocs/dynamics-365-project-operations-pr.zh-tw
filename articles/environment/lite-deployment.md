---
title: 部署 Project Operations - 精簡
description: 本文提供相關資訊，讓您了解如何安裝 Project Operations 精簡部署 - 交易至開立預估發票。
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930308"
---
# <a name="deploy-project-operations---lite"></a>部署 Project Operations - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_



Project Operations 支援多個部署模型。 若要判斷最佳部署模型，請參閱[部署類型](determine-deployment-type.md)。


> [!IMPORTANT]
> 此部署 (精簡部署 – 交易至開立預估發票) 會產生 **Project Operations 的只有 Dataverse 部署專**。

- [將 Project Operations 安裝到新的 Dataverse 環境中](#new)
- [安裝到現有的 Dataverse 環境中](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>將 Project Operations 安裝到新的 Dataverse 環境

1. 以持有 Project Operations 授權的[全域和 Power Platform 管理員](/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)建立新的 Dataverse 環境。 確定 **為此環境建立資料庫** 和 **Dynamics 365 應用程式** 已啟用。 如需詳細資訊，請參閱[在 Power Platform 系統管理中心建立和管理環境](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)。
2. 從 Dynamics 365 應用程式的部署清單中，選取 **Microsoft Dynamics 365 Project Operations**。


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>將 Project Operations 安裝到現有的 Dataverse 環境
1. 確定尚未使用[雙重寫入](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview)對環境進行設定，因為安裝程式接著會安裝[資源/非庫存型案例適用的 Project Operations](project-operations-integrated-deployment-overview.md) 功能。
2. 以持有 Project Operations 授權的[全域或 Power Platform 管理員](/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在您要安裝 Project Operations 所在的 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)尋找環境。
3. 從 Dynamics 365 應用程式的部署清單中，安裝 **Microsoft Dynamics 365 Project Operations**。 如需詳細資訊，請參閱[管理 Dynamics 365 應用程式](/power-platform/admin/manage-apps)。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
