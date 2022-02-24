---
title: 設定專案類別
description: 本主題提供有關設定專案類別的資訊。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131918"
---
# <a name="configure-project-categories"></a>設定專案類別

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

Project Operations 提供可在專案中分類營收及費用的強大功能。 類別提供用於報告和分析專案交易以及加速過帳至總帳的功能。

下圖說明交易類別、共用類別與專案類別之間的關聯性。 

交易類別是專案交易的基本群組。 在該群組中，有一組可以在應用程式與模組之間共用的共用類別。 專案類別更進一步深入細節，是最細微的類別等級。 專案類別是特定法律實體、模組和應用程式的專屬類別。

![交易類別、共用類別與專案類別之間的關聯性](media/project-categories.png)

## <a name="transaction-categories"></a>交易類別

交易類別代表專案交易的基本群組，並非特定公司或交易類型的專屬類別。 例如，Contoso Robotics 會使用設計、差旅、安裝及服務交易類別，將專案交易分為群組。

交易類別是在 Project Operations 模組中定義。 
1. 移至 **設定**\>**交易類別** 以開啟表單。 
2. 選取 **新增** 或選取 **從 Excel 匯入** 以建立新的交易類別。

## <a name="shared-categories"></a>共用類別

Dynamics 365 使用共用類別概念，將不同應用程式 (例如 Dynamics 365 Finance、Dynamics 365 Supply Chain 和 Dynamics 365 Project Operations) 中的費用分類。 對於建立的每個交易類別，Project Operations 都會自動建立四個相關的共用類別：時數、費用、服務費和項目。 您可以移至 **專案管理與會計**\>**設定**\>**類別**\>**共用類別**，檢閱並協調共用類別。

## <a name="project-categories"></a>專案類別

專案類別代表最細微的類別設定等級，而且必須由專案會計師分別為每個公司進行設定。

1. 移至 **專案管理與會計**\>**設定**\>**類別**\>**專案類別**。
2. 選取 **新增**。
3. 選取您在上一節所建立之共用類別的 **類別識別碼**。 Project Operations 只允許使用那些與交易類別有關聯的共用類別。
4. 選取類別群組。

## <a name="category-groups"></a>類別群組

類別群組會在相關專案類別之間用來共用屬性 (主要是過帳設定檔)。 每個交易類型都必須至少有一個類別群組，而且每個專案類別都已指派給群組。

Project Operations 中的過帳規範是由專案成本與營收設定檔規則、專案類別和類別群組所定義。 您可以移至 **專案管理與會計**\>**設定**\>**類別**\>**類別群組** 來設定類別群組。
