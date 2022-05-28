---
title: 廠商發票的狀態轉換
description: 本主題說明 Microsoft Dynamics 365 Project Operations 中廠商發票的狀態轉換。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584678"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>廠商發票的狀態轉換

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

本主題說明 Microsoft Dynamics 365 Project Operations 中廠商發票的狀態轉換。 使用下列狀態：**草稿**、**審查中**、**已確認**、**保留** 和 **已取消**。

下列圖表顯示狀態轉換。

![轉包合約狀態轉換模型。](../media/VI_State_Model.jpg)

下表說明廠商發票生命週期的每個狀態在 Project Operations 中所代表的意義。

| 州/省 | 名稱 | 允許的轉換 |
| --- | --- | --- |
| 草稿 | 此狀態是廠商發票的初始狀態。 這些明細和定價可能會有所修改。 可以編輯和刪除處於此狀態的廠商發票。 | 處理中 |
| 檢閱中 | 此狀態表示廠商發票的處理狀態。 至少一項廠商發票明細的驗證狀態為 **進行中**。 | 已確認、保留 |
| 已確認 | 此狀態表示廠商發票的階段，應用程式已為其中每項廠商發票明細建立成本實際值。 任何與廠商發票明細相符的已連結成本實際值都已沖回，並取代為這些廠商發票明細中的成本實際值。 無法編輯或刪除處於此狀態的廠商發票。 您可以使用 **取消** 按鈕來取消已確認的廠商發票。 取消動作會反轉確認動作的影響。 | 已取消 |
| 保留 | <p>此狀態表示廠商發票的階段，在階段中，廠商發票因為發票或廠商狀態的問題而無法移動。 無法確認、取消、編輯或刪除處於此狀態的廠商發票。</p><p>您可以使用重新開啟動作，將廠商發票轉移至 **草稿** 或 **審查中** 狀態。 如果廠商發票至少有一項明細的驗證狀態為 **進行中** 或 **完成**，就會在 **審查中** 狀態下重新開啟該廠商發票。 如果廠商發票所有的明細都有 **未開始** 的驗證狀態，則會在 **草稿** 狀態下重新開啟廠商發票。</p> | 草稿，審查中 |
| 已取消 | 此階段表示不再需要轉包合約在已轉包資源實際交付材料和/或工作時的階段。 處於此狀態的轉包合約無法用來估計專案對資源和材料的需求並為其配置人員，也無法在專案的時間、費用和材料使用方式中加以參考。 無法編輯或刪除處於此狀態的轉包合約。 | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
