---
title: 設定每個法律實體的 Project Operations 整合
description: 本主題提供有關在 Project Operations 中依法律實體設定整合的資訊。
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096742"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>設定每個法律實體的 Project Operations 整合 

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

本主題為您逐步解說依法律實體設定 Dynamics 365 Project Operations 所需的步驟。

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>在 Dynamics 365 Finance 中啟用功能金鑰

完成下列步驟以啟用必要的功能。

1. 在 Dynamics 365 Finance 中，移至 **功能管理** 工作區。
2. 在 **功能** 清單中，尋找並啟用下列功能：
  
    - **為專案啟用多個合約服務內容**
    - **在 Dynamics 365 Customer Engagement 上啟用 Project Operations**

> [!NOTE]
> 如果沒有看到 **功能金鑰** 列出，請確認您的 Finance 版本是否符合最低版本需求 (已套用品質更新的應用程式 10.0.13 版或更新版本)。 選取 **檢查更新** 以重新整理功能清單。

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>定義法律實體適用的 Project Operations 部署案例

您可以在法律實體層級啟用 Dynamics 365 Customer Engagement 上的 Project Operations。 您在 Dynamics 365 Customer Engagement 上可以有一個使用資源/非庫存型案例適用 Project Operations 的法律實體。 在相同的環境中，您可以有另一個使用庫存/生產訂單案例適用 Project Operations 的法律實體。

1. 在 Dynamics 365 Finance 中，移至 **專案管理與會計** > **設定** > **全域專案管理與會計參數** 。
2. 在可用法律實體清單中，選取要在 Dynamics 365 Customer Engagement 功能上啟用多個合約服務內容和 Project Operations 的實體。 讓將要使用庫存/生產訂單案例適用 Project Operations 的法律實體保持未選取狀態。

> [!NOTE]
> 只有在法律實體未包含任何現有的專案時，才能選取該法律實體。

## <a name="configure-project-management-and-accounting-parameters"></a>設定專案管理與會計參數

每個在 Dynamics 365 Customer Engagement 上使用 Project Operations 的法律實體都需要一組預設參數。 這些參數是在 **專案管理與會計參數** 頁面的 **Project Operations** 索引標籤上進行設定。 這些參數包括：

  - **帳單類型預設值** ：Project Operations 使用固定一組必須對應至 Finance 明細屬性的帳單類型預設值。 建立下列每個帳單類型的記錄： **未指定** 、 **應收費** 、 **不應收費** 、 **附贈** 和 **無法使用** 。
  - **專案類別預設值** ：選取每個交易類型要使用的預設專案類別。 這些預設值將用於 **Project Operations 整合帳目** 以及未指定專案實際值交易類別的估計值。
  - **預測** ：選取時間和費用估計值要使用的預測模型。
