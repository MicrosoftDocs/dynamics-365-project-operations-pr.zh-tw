---
title: 2021 年 3 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 本主題提供有關資源/非庫存型案例適用的 Project Operations 2021 年 3 月版本所提供的品質更新資訊。
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b11a57ae152be154fd6a7d330c8520f3b295ce3ef5cc7051ac9b343e3bcdbe12
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006326"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 3 月 - 資源/非庫存型案例適用的 Project Operations 新增功能

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

- Dataverse 環境的 Project Operations 版本 4.8.0.91 
- Dynamics 365 Finance 環境 10.0.16 版中的專案管理與會計 

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations


| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 帳單和定價 | 2133873 | 修正 **銷售單價** 貨幣符號在 **費用估計值** 網格中的顯示。 |
| 帳單和定價 | 2174616 | 報價成交時，從報價複製而來的合約服務內容詳細資料會參考合約自訂價目表。 |
| 商機管理 | 2167475 | 修正源自未開單實際值項目之更正發票中的稅額。 |
| 商機管理 | 2176285 | 不可將銷售合約/報價明細詳細資料中的稅額複製到成本合約/報價明細詳細資料。 |
| 商機管理 | 2188079 | 不可建立非工作型合約的分割帳單規則。 |
| 規劃和追蹤 | 2125274 | 將 **專案開始日期對應** 的 **專案 雙重寫入對應** 屬性從 **msdyn\_taskearlieststart** 為 **msdyn\_actualstart**。 |
| 規劃和追蹤 | 2138853 | 更新專案複製功能，確保已將參考工作的費用估計明細複製到目的地專案。 |
| 規劃和追蹤 | 2154306 | 修正與刪除資源型案例適用 Project Operations 中費用估計值有關的問題。 |
| 規劃和追蹤 | 2173259 | 更新專案複製功能，以確保此功能不會在特定案例中顯示 **複製 WBS** 錯誤訊息。 |
| 時間和費用 | 2148910 | 修正 **編輯項目** 頁面在 **時間項目** 網格中的顯示問題。 |
| 時間和費用 | 2159798 | 加強控制，以確保無法編輯已核准的費用項目。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

如需詳細資訊，請參閱 [2021 年 1 月 - 資源/非庫存型案例適用的 Project Operations 新增功能](whats-new-jan-2021-resource-based.md)。

## <a name="regulatory-updates"></a>法規更新

如需 Finance and Operations 應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。 另一個了解法規更新的方式就是，登入 LCS，並使用問題搜尋工具來檢視已規劃的法規更新。 問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。


[!INCLUDE[footer-include](../includes/footer-banner.md)]