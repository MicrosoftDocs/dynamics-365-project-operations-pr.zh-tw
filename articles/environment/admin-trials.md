---
title: 註冊 Project Operations 試用版
description: 本文提供有關如何部署 Dynamics 365 Project Operations 試用版的資訊。
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 60790d83d5fcc8c75fef8eac2877d1ca14a761f2
ms.sourcegitcommit: 385081ecc839d7d4a557eda2bb1578ca073f7e41
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/19/2022
ms.locfileid: "9527969"
---
# <a name="sign-up-for-project-operations-trials"></a>註冊 Project Operations 試用版 

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票、庫存/生產型案例適用的 Project Operations_ 



本文說明如何訂閱預覽版合作夥伴供應項目，以及部署 Dynamics 365 Project Operations 環境。

您可以透過新的 Project Operations 試用版，藉由完成一份建議最佳部署方式的問卷，讓系統自動部署三種支援的部署案例中的任何一種。 本文提供相關資訊，讓您了解如何：

- 兌換您的試用供應項目。
- 開始進行佈建。
- 設定雙重寫入。
- 深入了解 Project Operations。 

下表概述新試用供應項目的詳細資料。

| **供應項目**               | **詳細資料**                                  |
|------------------------------|----------------------------------------------|
| 供應項目類型                   | 此供應項目類型為管理負責人，因此需要租用戶管理員才能進行兌換。 |
| 供應項目使用                    | 每個租用戶一次                          |
| 供應項目期間               | 30 個日曆天                             |
| 每個租用戶的兌換次數       | 7                                            |
| 擴充                    | 1 次延長 30 個日曆天               |
| 試用環境的數目 | 3                                            |


## <a name="admin-trial-details"></a>管理員試用詳細資料
下表列出試用詳細資料，以及如何套用至每種部署類型。

| **項目**                      | **精簡**                                     | **非庫存材料** | **庫存材料** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| 提供的設定資料           | 是                                          | 是                       | 是 (USSI)            |
| 交易資料            | 否                                           | 否                        | 否                    |
| 佈建時間 (分鐘)  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>先決條件
必須具備下列先決條件，才能部署 Dynamics 365 Project Operations 試用版。

- 註冊 [Dynamics 365 Project Operations - 預覽版試用](https://www.aka.ms/try-po)。
- 部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。

> [!IMPORTANT]
> 只有組織中的一個人員 (租用戶系統管理員) 才需要執行此工作。 如果您不是此版本的訂閱者，請等到您的組織已註冊，而您收到您的使用者認證之後再說。

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - 預覽版試用 

開始之前，請透過您要預覽 Project Operations 所在租用戶中的使用者公司帳戶登入瀏覽器。

1. 將第一個供應項目代碼貼入瀏覽器 URL 以兌換 **Dynamics 365 Project Operations - 預覽版試用**。

    ![兌換供應項目](./media/16RedeemFirstOfferNew.png)

2. 確認您的訂閱。

    ![確認訂單](./media/17ConfirmOrderNew.png)

  您會看到已成功兌換供應項目的確認。

   ![確認](./media/18OrderConfirmationNew.png)

  系統會將您重新導向至 [Power Platform 系統管理中心](https://admin.powerplatform.microsoft.com/projectoperationstrial)。

## <a name="questionnaire-and-provisioning"></a>問卷和佈建

1.  前往 [Power Platform 系統管理中心](https://admin.powerplatform.com/projectoperationstrial)，然後完成問卷。  
2.  檢閱建議的部署類型，並選取 **開始設定** 以開始進行佈建。
3.  檢閱條款及條件，然後選取 **開始**。

   佈建開始後，系統會將您重新導向至 Power Platform 系統管理中心的環境清單。 佈建正在進行時，環境的狀態為 **PreparingInstance**。
 
  佈建完成時，環境的狀態會是 **就緒**。 環境的佈建包括部署示範資料。
 
4.  選取各自的 Microsoft Dataverse URL 以及財務和營運應用程式 URL 來驗證部署。

## <a name="configuring-dual-write"></a>設定雙重寫入
- 若要設定雙重寫入的資訊安全角色，請參閱[在 Dataverse 中更新 Project Operations 上的安全性設定](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse)。
- 若要存取雙重寫入設定，請瀏覽至財務和營運應用程式執行個體，然後瀏覽至 **資料管理** > **雙重寫入**。
- 若要設定雙重寫入對應，請參閱[執行 Project Operations 雙重寫入對應](resource-provision-new-environment.md#run-project-operations-dual-write-maps)。

## <a name="assign-licenses"></a>指派授權

您需要組織的 Microsoft 365 入口網站系統管理存取權，才能完成下列步驟。

1. 前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給使用者。

   ![系統管理中心首頁](./media/14AdminPortal.png)

2. 在 **使用中使用者** 頁面上，選取要將授權指派給的使用者。

   ![指派授權](./media/15AssignLicenses.png)

3. 確認是否已選取 **Dynamics 365 Project Operations 預覽版** 授權，然後選取 **儲存變更**。

## <a name="additional-resources"></a>其他資源

下列資源可在您開始使用 Project Operations 的過程中提供實用指引：

- [影片系列 - Project Operations 概觀、功能深入探索和藍圖](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/training/modules/examine-dynamics-365-project-operations/)
- [判斷您的部署類型](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>常見問題

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>如果我需要財務和營運應用程式環境的 ALM 或 ELM，該怎麼做？

- 需要完整環境生命週期管理功能的合作夥伴，請參閱[合作夥伴沙箱授權申請](https://experience.dynamics.com/requestlicense)以檢閱新的合作夥伴供應項目。 
- 尋求內部使用權相關詳細資訊的合作夥伴，請參閱[內部使用權雲端及軟體權益](https://partner.microsoft.com/membership/internal-use-software)。

### <a name="can-i-extend-my-trial-beyond-30-days"></a>可以試用期延長超過 30 天嗎？
若要延長試用期，請完成下列步驟。

1. 在 **Microsoft 365 系統管理中心**，移至 **帳務** > **您的產品**。
2. 選取 **Dynamics 365 Project Operations (CE) - 預覽版試用**。
3. 在 **到期日** 底下，選取 **延長日期**。

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>是否可以從精簡部署升級至資源/非庫存型案例部署？
目前不提供將環境從精簡升級至非庫存型部署的支援。

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>可以存取 Finance 環境的 Lifecycle Services (LCS) 嗎？  
號碼 對於這些試用版，部署是透過 Power Platform 系統管理中心來處理。 存取 Finance 環境受到限制。

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>可以在現有環境上安裝試用版嗎？
如果您目前已有此環境，則允許您透過 Power Platform 系統管理中心，將精簡部署安裝到現有的銷售 Dataverse 環境。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
