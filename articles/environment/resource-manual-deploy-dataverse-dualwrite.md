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
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>手動部署支援雙重寫入的 Project Operations Dataverse 應用程式

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本主題說明如何在 Microsoft Dataverse 中手動部署 Microsoft Dynamics 365 Project Operations，使其支援雙重寫入。 如果符合先決條件，Project Operations 就會偵測環境的設定，並新增對雙重寫入的額外支援。

透過 Microsoft Dynamics Lifecycle Services (LCS) 進行部署時，如果您已依照本主題中的指示操作，就可以跳過 Microsoft Power Platform 整合 (先前稱為 Common Data Service 環境) 的部署。

在 Dataverse 中部署 Project Operations 使其支援雙重寫入的步驟，有四個主要步驟：

1. [在 Dataverse 中建立支援雙重寫入的新環境](#create)。
2. [將雙重寫入先決條件新增至環境](#prerequisites)。
3. [新增 Project Operations Dataverse 應用程式](#dataverse)。
4. [連結您的環境](#link)。

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>在 Dataverse 中建立支援雙重寫入的新環境

若要完成此程序，必須以系統管理員身分登入。

1. 開啟 [Power Platform 系統管理中心](https://admin.powerplatform.com)，並以系統管理員身分登入。
2. 建立新環境，並將其命名。
3. 選取環境類型。 如果您已註冊試用版方案，請選取 **試用 (以訂閱為準)**。
4. 確認部署區域。
5. 啟用 **建立此環境的資料庫** 選項。 
6. 確認語言，然後確認貨幣符合 Finance and Operations 應用程式的貨幣。
7. 啟用 **Dynamics 365 應用程式** 選項，並確認 **自動部署這些應用程式** 欄位已設定為 **無**。
8. 如果需要安全性群組，請新增安全性群組。
9. 選取 **儲存** 以建立環境。
10. 等待直到部署已完成，且環境達到 **就緒** 狀態。

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>將雙重寫入先決條件新增至環境

雙重寫入支援包含另外新增至主要實體 (例如 **公司** 實體) 的其他欄位。 如果您要將雙重寫入支援新增至現有環境，則可能需要更新資料才可啟用此支援。 如需有關如何啟動載入資料的詳細資訊，請參閱[啟動載入公司資料](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data)。 如需雙重寫入的詳細資訊，請參閱[雙重寫入系統需求](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req)。

完成此程序，以將雙重寫入先決條件新增至您的環境。

1. 開啟剛才建立的環境，然後移至 **資源** \> **Dynamics 365 應用程式**。
2. 選取應用程式清單中的 **雙重寫入核心解決方案**，並加以安裝。
3. 等待直到完成安裝。 接著選取應用程式清單中的 **雙重寫入應用程式協調流程解決方案**，然後進行安裝。

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>新增 Project Operations Dataverse 應用程式

僅當您已在安裝 Project Operations 前完成先前程序時，才可完成此程序。 在安裝期間，系統會分析環境設定，並在需要時新增對雙重寫入的支援。

1. 開啟先前建立的環境，然後移至 **資源** \> **Dynamics 365 應用程式**。
2. 選取應用程式清單中的 **Microsoft Dynamics 365 Project Operations**，並加以安裝。

## <a name="link-your-environments"></a><a name="link"></a>連結您的環境

部署 Dataverse 環境後，您可以在 Finance and Operations 應用程式中設定連結。 請依照[使用雙重寫入精靈來連結您的環境](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment)中的步驟操作。
