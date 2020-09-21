---
title: 升級首頁
description: 本主題顯示到哪裡尋找有關 Dynamics 365 Project Service Automation 的新功能和其已變更功能的重要資訊，以及升級為最新版本的程序。
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749950"
---
# <a name="upgrade-home-page"></a>升級首頁

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>從 PSA 2.x 或 1.x 版升級至 3.x 版

### <a name="new-instances"></a>新的執行個體

自 2019 年 5 月 17 日起，在佈建新執行個體期間選取 Project Service Automation 時，預設會安裝版本 3.x。

### <a name="existing-instances"></a>現有的執行個體

先前有 PSA 2.x 版執行個體且需要升級至 3.x 版 (這是 PSA 的整合用戶端介面架構 (UCI) 版本) 的客戶，必須連絡 Microsoft 支援服務，並提供其執行個體的詳細資料，讓支援服務可以啟用執行個體以升級至 3. x 版。 從 2020 年 3 月 1 日起，擁有 PSA 2.x 版執行個體且需要升級至 3.x 版的客戶，將可以從管理入口網站直接升級其其執行個體，而不需連絡 Microsoft 支援服務。  

> [!NOTE]
> PSA 3.x 版包含重大變更。 這已內建於整合介面架構，可協助您改善使用者體驗。 重新設計的應用程式提供一致的整合使用者介面 (UI)，並遵循回應式設計原則，讓您在任何螢幕大小或裝置上都能看到最佳畫面。 整個應用程式已徹底進行了其他變更。 一些已有所變更的部分包括定價、預約以及指派資源、時間、費用和核准。

開始升級程序前，建議您完成下列工作：

- 確認是否 Dynamics 365 Field Service 和 Project Service Automation 都已安裝在已識別的執行個體。 如果這兩個解決方案都已安裝，您必須先規劃升級這兩項，再繼續正常使用該執行個體。
- 仔細檢閱下列主題。 知道並了解版本之間的變更將有助於進行您的升級程序。 這些主題提供有關 PSA 中主要變更的資訊，以及規劃升級至版本 3.x 的考量和建議。

    - [Project Service Automation 版本 3 的新功能或變更](whats-new-changed-v3.md)
    - [升級考量 - 從 Project Service Automation 2.x 或 1.x 版升級至版本 3](upgrade-v3.md)

- 先升級沙箱執行個體以評估您的實作中的變更，然後再升級生產執行個體。

檢閱過前述主題並準備好升級至 PSA 3.x 版或 UCI 架構版本時，請送出要求至 Microsoft 支援服務，讓升級可在系統管理中心進行。 在要求中，提供您的執行個體的詳細資料。

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>新建立執行個體中的舊版 PSA (PSA 2.x 版)

自 2019 年 5 月 17 日起，所有新的執行個體都會有 UCI 做為預設用戶端。 為了配合這項變更，預設情況下會佈建 PSA 3.x 版和 Field Service 8.x 版，因為這些版本是專門設計來搭配 UCI 用戶端使用的。

從 2020 年 3 月 1 日開始，Dynamics PSA 的客戶無法再使用舊版 PSA (例如 PSA 2.x 版或更舊版本) 建立新環境。 任何新的環境都只能取得 PSA 3.x 版。

> [!NOTE]
> 為了在您使用舊版 Field Service 和 PSA 應用程式時獲得最佳體驗，請前往**系統設定**頁面，並針對**僅使用新的整合介面 (建議使用)** 欄位選取**否**，因為這些版本不是設計要在 UCI 中正確載入。 關閉 UCI 之後，您可以使用舊版 Web 用戶端，開啟並執行這些版本的 Field Service 和 PSA。 如需有關如何關閉 UCI 用戶端的指示，請參閱[僅啟用整合介面](../admin/enable-unified-interface-only.md)。
