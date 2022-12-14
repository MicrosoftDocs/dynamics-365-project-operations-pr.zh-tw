---
title: 部署 Project Operations 精簡版
description: 本文提供相關資訊，讓您了解如何安裝 Project Operations 精簡部署 - 交易至開立預估發票。
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810968"
---
# <a name="deploy-project-operations-lite"></a>部署 Project Operations 精簡版

_**適用於：** 精簡部署 - 交易至開立預估發票_



Project Operations 支援多個部署模型。 若要判斷最佳部署模型，請參閱[部署類型](determine-deployment-type.md)。


> [!IMPORTANT]
> 此部署 (精簡部署 – 交易至開立預估發票) 會產生 **Project Operations 的只有 Dataverse 部署專**。

- [將 Project Operations 安裝到新的 Dataverse 環境中](#new)
- [安裝到現有的 Dataverse 環境中](#existing)
- [安裝到具有雙重寫入元件的現有 Dataverse 環境](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>將 Project Operations 精簡版安裝到新的 Dataverse 環境

1. 以持有 Project Operations 授權的[全域和 Power Platform 管理員](/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)建立新的 Dataverse 環境。 確定 **為此環境建立資料庫** 和 **Dynamics 365 應用程式** 已啟用。 如需詳細資訊，請參閱[在 Power Platform 系統管理中心建立和管理環境](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)。
1. 從 Dynamics 365 應用程式的部署清單中，選取 **Microsoft Dynamics 365 Project Operations**。


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>將 Project Operations 精簡版安裝到現有的 Dataverse 環境 
1. 以持有 Project Operations 授權的[全域或 Power Platform 管理員](/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在您要安裝 Project Operations 所在的 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)尋找環境。
1. 從 Dynamics 365 應用程式的部署清單中，安裝 **Microsoft Dynamics 365 Project Operations**。 如需詳細資訊，請參閱[管理 Dynamics 365 應用程式](/power-platform/admin/manage-apps)。

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>將 Project Operations 精簡版安裝到已有雙重寫入解決方案的現有  Dataverse 環境

如果您想要繼續在精簡部署模式下執行 Project Operations，請執行下列步驟：

1. 以持有 Project Operations 授權的[全域或 Power Platform 管理員](/power-platform/admin/global-service-administrators-can-administer-without-license)身分，在您要安裝 Project Operations 所在的 [PowerPlatform 系統管理中心](https://admin.powerplatform.com)尋找環境。
1. 從 Dynamics 365 應用程式的部署清單中，安裝 **Microsoft Dynamics 365 Project Operations**。 如需詳細資訊，請參閱[管理 Dynamics 365 應用程式](/power-platform/admin/manage-apps)。
1. 由於您的環境已有對整合至所安裝財務和營運應用程式有幫助的雙重寫入元件，因此 Project Operations 安裝也會安裝將專案相關資料整合至財務和營運應用程式所需的功能與擴充功能。 既然您想要在精簡部署中執行 Project Operations，就必須移除這些整合元件，否則這些元件會為精簡部署案例帶來限制和額外負荷。 手動解除安裝解決方案 **Dynamics 365 Project Operations 雙重寫入** 和 **Dynamics 365 Project Operations 雙重寫入實體對應** ，以移除這些元件。
1. 移至 **Project Operations -> 設定 -> 參數**。 開啟 **專案參數** 詳細資料頁面，並將 **解決方案升級行為** 欄位設定為 **僅精簡版**。 這可確保 Project Operations 的任何後續升級都不會將整合元件重新移入 Project Operations 中。  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
