---
title: Dynamics 365 Project Operations 中已移除或已取代的功能
description: 本文說明 Dynamics 365 Project Operations 中已移除或已規劃要移除的功能。
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028319"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Dynamics 365 Project Operations 中已移除或已取代的功能

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票，以及庫存/生產型案例適用的 Project Operations_

本文說明 Dynamics 365 Project Operations 中已移除或已規劃要移除的功能。

- *已移除的* 功能在產品中不復存在。
- *已取代的* 功能已不在現行開發之列，而且可能會在未來的更新中移除。

本清單旨在協助您在自己的規劃中考慮這些移除及取代情形。

> [!NOTE]
> 有關財務和營運應用程式中物件的詳細資訊，可在 [**技術參考報告**](/dynamics/s-e/global/axtechrefrep_61)中找到。 您可以比較這些報告的各種不同版本，了解每個財務和營運應用程式版本中已變更或已移除的物件。

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Project Operations 2022 年 3 月發行版本中已移除或已取代的功能

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>專案管理與會計 [一律建立調整交易] 參數

| &nbsp; | &nbsp; |
|--------|--------|
| **取代/移除的原因** | 需要調整交易以作稽核之用。 取代之後，將會隱藏此參數。 系統永遠都會建立調整交易，就像在目前參數設定為 **是** 時那樣。 |
| **已由其他功能取代？** | 無 |
| **受影響的產品區域** | 應用程式 |
| **部署選項** | 生產/庫存案例適用的 Project Operations |
| **狀態** | 已取代：到了 2023 年 3 月 1 日，我們將會隱藏參數，並變更系統行為，讓系統一律建立調整交易。 |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>專案管理與會計 [使用調整日期做為新的專案日期] 參數

| &nbsp; | &nbsp; |
|--------|--------|
| **取代/移除的原因** | 此參數最初用於允許在會計週期關閉時進行調整。 然而，不再需要此參數，因為交易記錄的會計日期可以變更為未結期間的第一個日期 (如果參數已設定)。 不能變更專案日期，因為此日期代表的是交易發生日期。 |
| **已由其他功能取代？** | 無 |
| **受影響的產品區域** | 應用程式 |
| **部署選項** | 生產/庫存案例適用的 Project Operations |
| **狀態** | 已取代：到了 2023 年 3 月 1 日，我們將會隱藏參數，並變更系統行為，讓專案日期永遠不會在調整上變更。 |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>庫存/生產型案例適用的 Project Operations中的資源要求工作流程

| &nbsp; | &nbsp; |
|--------|--------|
| **取代/移除的原因** | 因使用率低和交易量限制而被取代。 |
| **已由其他功能取代？** | 無 |
| **受影響的產品區域** | 應用程式 |
| **部署選項** | 生產/庫存案例適用的 Project Operations |
| **狀態** | 已取代：到了 2023 年 3 月 1 日，我們將停用使用工作流程要求專案資源的選項。 |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>[專案發票提案] 頁面，不含 [標題] 和 [明細] 檢視表

| &nbsp; | &nbsp; |
|--------|--------|
| **取代/移除的原因** | 因改進與 **將專案發票提案及發票帳目表單與標題和明細檢視表搭配使用** 功能金鑰一起引進的頁面而被取代。 |
| **已由其他功能取代？** | .是 |
| **受影響的產品區域** | 應用程式 |
| **部署選項** | 生產/庫存案例適用的 Project Operations；資源/非庫存案例適用的 Project Operations |
| **狀態** | 被取代：到了 2023 年 3 月 1 日，我們將關閉先前的 (舊版) 頁面，並根據預設開啟 **將專案發票提案及發票帳目表單與標題和明細檢視表搭配使用** 功能金鑰。 |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Project Operations 2021 年 12 月發行版本中已移除或已取代的功能

### <a name="collaboration-workspaces"></a>共同作業工作區

[建立或連結至共同作業工作區 (專案)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **取代/移除的原因** | 因使用率低而被取代。 使用資源/非庫存案例適用的 Project Operations 的使用者，可以利用[與 Office 群組的共同作業](../project-management/collaboration-groups.md)。 |
| **已由其他功能取代？** | 無 |
| **受影響的產品區域** | 應用程式  |
| **部署選項** | 生產/庫存案例適用的 Project Operations |
| **狀態** | 取代：到 2022 年 12 月 1 日，我們計劃不再支援共同作業工作區。 |
