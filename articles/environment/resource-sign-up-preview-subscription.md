---
title: 註冊資源/非庫存案例適用的 Project Operations 預覽版訂閱
description: 本主題提供有關如何訂閱和部署資源/非庫存型案例適用 Project Operations 的資訊。
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334817"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>註冊資源/非庫存案例適用的 Project Operations 預覽版訂閱

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主題說明如何訂閱試用版方案，以及部署資源/非庫存型案例適用的 Project Operations 環境。

## <a name="prerequisites"></a>先決條件
- 部署預覽版的使用者必須具備 Azure 租用戶全域管理員權限。 您可以在第一個供應項目兌換期間建立租用戶。 
- 部署 Finance 環境需要按環境計費的有效 Azure 訂閱。 您可以使用組織現有的訂閱，或使用 [Azure 試用版](https://azure.microsoft.com/en-us/free/)來開始進行。 CDS 環境會在有限的 30 天期間免費提供。

> [!IMPORTANT]
> 組織中只有一個人 (租用戶管理員) 需要執行這項工作。 如果您不是此版本的訂閱者，請等到您的組織已註冊，而您收到您的使用者認證之後再說。
> 
> 試用是在租用戶中單次使用。 您只能執行試用版一次。 建議您基於試用目的建立新的租用戶。


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - 預覽版試用 

開始之前，請確定您已使用您要預覽 Project Operations 所在租用戶中的使用者公司帳戶來登入瀏覽器。

1. 在 [Project Operations 試用](https://aka.ms/try-po)這裡兌換第一個供應項目代碼 **Dynamics 365 Project Operations**。
2. 確認您的訂閱。

  您會看到已成功兌換供應項目的確認。

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance 預覽版試用

移至 [Dynamics 365 for Finance 預覽版試用](https://aka.ms/trypoche)，並對供應項目 [註冊雲端託管的環境] 重複上一節的步驟。  

## <a name="assign-licenses"></a>指派授權

> [!IMPORTANT]
> 您需要組織的 Microsoft 365 入口網站系統管理存取權，才能完成下列步驟。

1. 前往 [Microsoft 365 系統管理中心](https://portal.office.com/)，將授權指派給您的使用者。

2. 在 **使用中使用者** 頁面上，選取要將授權指派給的使用者。

3. 確認是否已選取 **Dynamics 365 Project Operations** 授權，並選取 **儲存變更**。

> [!NOTE]
> Finance 試用版供應項目不需要指派給使用者。

## <a name="start-a-new-project-in-lcs"></a>在 LCS 中開始新專案

建立新的 LCS 專案，如[在 LCS 中開始新專案](create-lcs-project.md)主題中所述

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>將 Azure 訂閱新增至 LCS 專案

若要完成此工作，請依照主題[將 Azure 訂閱新增至 LCS 專案](resource-add-azure-subscription-lcs-project.md)中的步驟進行。

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>使用資源/非庫存案例適用的 Project Operations 部署 Finance 示範環境

依照主題[佈建新環境](resource-provision-new-environment.md)中的指引完成部署。 使用[示範環境](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)部署類型以進行預覽。 

## <a name="install-cds-setup-and-configuration-data"></a>安裝 CDS 設定和設定資料

安裝 CDS 設定和設定資料，如主題[設定和套用 Common Data Service 中的設定資料](resource-apply-pro-setup-config-data.md)中所述。
只有在部署 Finance 示範環境並準備好示範資料後，才可完成此步驟。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
