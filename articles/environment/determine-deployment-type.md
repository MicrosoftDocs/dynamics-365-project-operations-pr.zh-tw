---
title: 部署類型
description: 本主題提供資訊以協助您判斷適合您公司的正確 Project Operations 部署類型。
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948778"
---
# <a name="deployment-types"></a>部署類型

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

> [!IMPORTANT]
> 購買授權之後，請從這裡開始使用[引導式安裝流程](https://aka.ms/provisionprojectoperations)來判斷 Dynamics 365 Project Operations 的最佳部署模型。
> 完成引導式安裝流程之後，系統會將您導向至正確的管理入口網站，以完成您的安裝。 請參閱下方部署詳細資料，以完成安裝。


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>使用 Dynamics 365 Project Service Automation 的 Dynamics 現有客戶
Project Operations 包含隨附於 Project Service Automation 的功能。 日後將會為這些客戶發行升級路徑。

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>使用專案管理與會計的 Dynamics 365 Finance 現有客戶 

使用專案管理與會計功能的現有 Finance 客戶可以依照原本方式繼續使用。 請參閱[庫存/生產訂單案例適用的 Project Operations](#pma)。

Project Operations 支援多個部署選項，以符合您的需求。 不論您是新的或現有 Dynamics 365 客戶，Project Operations 都能支援您的需求。

我們的[部署問卷 ](https://aka.ms/provisionprojectoperations)會協助您判斷適當的部署。 結果將引導您前往下列其中一個部署類型：

- [精簡部署 - 交易至開立預估發票](#lite)
- [資源/非庫存案例適用的 Project Operations](#integrated)
- [庫存/生產訂單案例適用的 Project Operations](#pma)

Project Operations 透過法律實體層級設定在同一個環境中支援庫存/生產訂單案例以及非庫存/資源型案例。 例如，Contoso 可以利用其美國製造設施 (法律實體 = Contoso Manufacturing United States) 中的庫存/生產訂單功能，以及其在英國的 Contoso 機器人手臂維修設施 (法律實體 = Contoso Robotics United Kingdom) 中的非庫存/資源型功能。

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>精簡部署 - 交易至開立預估發票
精簡部署包含下列功能：

- 使用 Microsoft Project 網頁版進行專案規劃
- 多維度定價
- 統一資源管理
- 時間追蹤
- 基本費用
- 發票提案

### <a name="deployment-steps"></a>部署步驟：
使用[部署問卷](https://aka.ms/provisionprojectoperations)來判斷 Project Operations 的最佳部署模型。

若要進行此部署，請參閱[註冊預覽版訂閱](lite-preview-subscription-sign-up.md)和[佈建新環境](lite-deployment.md)。 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>資源/非庫存案例適用的 Project Operations
資源/非庫存案例適用的 Project Operations 包含下列功能：
  
- 使用 Microsoft Project 網頁版進行專案規劃
- 多維度定價
- 統一資源管理
- 時間追蹤
- 基本費用
- 全額費用
- 收據 OCR
- 完整發票
- 收入認列

### <a name="deployment-steps"></a>部署步驟：
使用[部署問卷](https://aka.ms/provisionprojectoperations)來判斷 Project Operations 的最佳部署模型。

若要進行此部署，請參閱[註冊預覽版訂閱](resource-sign-up-preview-subscription.md)和[佈建新環境](resource-provision-new-environment.md)。 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>庫存/生產訂單案例適用的 Project Operations

- 使用 WBS 進行專案規劃
- 資源管理
- 時間追蹤
- 全額費用
- 收據 OCR
- 完整發票
- 收入認列
- 生產訂單
- 材料支援

### <a name="deployment-steps"></a>部署步驟：
使用[部署問卷](https://aka.ms/provisionprojectoperations)來判斷 Project Operations 的最佳部署模型。

若要進行此部署，請參閱[註冊預覽版訂閱](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json)和[佈建新環境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)。 



