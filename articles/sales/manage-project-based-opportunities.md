---
title: 管理專案型商機
description: 本主題提供有關如何使用與專案相關之商機的資訊。
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948365"
---
# <a name="manage-project-based-opportunities"></a>管理專案型商機

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

以專案為主的公司通常都會分佈在多個國家/地區和地理位置，展開其交付作業。 專案執行及交付成本會根據管理交付的地理位置或部門不同而不同。 反過來，這可能會影響交易的利潤。 交付專案型服務通常需要大量人力資源時間、可觀差旅費用、材料成本及其他費用。

Dynamics 365 Project Operations 中的專案型商機是使用 Dynamics 365 Sales 的擴充功能所設計。 主題提供有關包含在專案型公司管理專案型商機所需之其他功能中的不同欄位與商務規則的詳細資料。

## <a name="view-all-project-based-opportunities"></a>檢視所有專案型商機

您可以從 **商機** 清單頁面查看所有專案型商機的清單。 

1. 移至 **銷售** > **商機**。
2. 使用 **檢視表切換器** 來選取商機的其他篩選過的檢視。 若要設定這些檢視表和導覽選項，您可以使用自訂篩選準則來建立您自己的檢視表。

您可以從此清單頁面或詳細資料頁面建立或刪除專案商機。

## <a name="business-process-flow-for-project-based-deals"></a>專案型交易的商務程序流程

Project Operations 中的專案型交易支援下列商務程序流程：

- 潛在客戶變商機商務程序
- 商機銷售處理

### <a name="lead-to-opportunity-business-process"></a>潛在客戶變商機商務程序 
潛在客戶變商機商務程序支援下列階段：

| 階段 | 對應的實體 | 功能 |
| --- | --- | --- |
| 授與資格​​ | 潛在客戶​​ | 授與潛在客戶資格以建立客戶、連絡人和商機。 |
| 開發 | 商機​​ | 開發商機以新增有關所涉及工作、主要利害關係人和競爭者的詳細資訊。 |
| 提案 | 商機​​ | 開發提案，並取得內部審查團隊的核准。 |
| 關閉​​ | 商機​​ | 贏得商機以完成交易。 |

### <a name="opportunity-sales-process"></a>商機銷售處理
Project Operations 中的商機銷售處理是 Sales 應用程式中商機銷售處理商業流程的擴充功能。 此商務程序已設計為現成可用，以便在專案型商機中支援下列階段。

| 階段 | 對應的實體 | 功能 |
| --- | --- | --- |
| 授與資格​​ | 商機​​ | 授與潛在客戶資格以建立客戶、連絡人和商機。 |
| 提案 | 報價 | 使用專案報價開發提案，並取得內部審查團隊的核准。 |
| 合約 | 專案合約 | 贏得報價成交以建立合約，並開始專案的執行與交付。 |
| 關閉​​ | 專案合約 | 成功完成工作並結束專案合約。 |

> [!NOTE]
> 如果專案型交易是從潛在客戶起始，則優先考慮潛在客戶變商機商務程序。
>
> 如果專案型交易是從商機起始，則優先考慮商機銷售處理。

您可以編輯產品商務程序流程，也可以建立您自己的商務程序流程，視需要來追蹤銷售處理。 如需商務程序流程的詳細資訊，請參閱[商務程序流程概觀](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]