---
title: 2021 年 2 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 本主題提供有關資源/非庫存型案例適用的 Project Operations 2021 年 2 月版本所提供的品質更新資訊。
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 41d7d7133652069ca3899db7f12e67e9ba531bcd3e36d67c3686a6b637b077d3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986796"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 2 月 - 資源/非庫存型案例適用的 Project Operations 新增功能

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

- Dataverse 環境 4.7.0.95 上的 Project Operations
- Dynamics 365 Finance 環境 10.0.16 版本的專案管理與會計 

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| **帳單和定價** | 2053736 | 現在可移至 **發票** > **相關資訊** 存取發票明細詳細資料。 |
| **帳單和定價** | 2122613 | **啟用** 和 **停用** 動作已從 **價目表** 關聯實體中移除。 |
| **帳單和定價** | 2128606 | 解決 **GetEstimatesForProject** 外掛程式中有關 **ullReferenceException** 的問題。 |
| **部署和設定** | 2139346 | 解決匯入未受管理的 **Dynamics365ProjectOperationsDualWrite** 解決方案的問題。 |
| **部署和設定** | 2140569 | 不可將 Project 解決方案安裝在 Dataverse Teams 環境中。 |
| **部署和設定** | 2086991 | 限制自訂 Web 資源的當地語系化。 |
| **商機管理** | 2136794 | 在 **確認發票** 或 **將發票標示為已付** 程序失敗時顯示正確的錯誤訊息。 |
| **商機管理** | 2139330 | 變更專案的專案經理時，不可將擁有公司重設回預設值。 |
| **商機管理** | 2146376 | 不應收費實際值中已更正的稅金金額是從發票確認所建立。 |
| **專案規劃和追蹤** | 2099879 | Dataverse 環境部署必須使用靜態識別碼建立預設交易類別，不可每個環境隨機產生一個類別。 |
| **專案規劃和追蹤** | 2128577 | 修正 Project Service 使用者權限，以更新資源指派上的交易類別。 |
| **專案規劃和追蹤** | 2164035 | 修正 **複製專案** 功能的問題。 |
| **時間項目** | 2129161 | 套用更嚴格的限制，以確保使用者無法變更和更新已提交或核准的時間項目。 |
| **時間項目** | 2103572 | 非專案時間項目的時間核准不得尋找專案核准者角色。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計 

如需 Dynamics 365 Finance 中 [專案管理與會計] 的詳細資訊，請參閱 [2021 年 1 月 - 資源/非庫存型案例適用的 Project Operations 新增功能](whats-new-jan-2021-resource-based.md)。


## <a name="regulatory-updates"></a>法規更新

如需 Finance and Operations 應用程式的法規更新資訊，請參閱[法規更新](/dynamics365/finance/localizations/regulatory-updates)。 另一個了解法規更新的方式就是，登入 Lifecycle Services (LCS)，並使用問題搜尋工具來檢視已規劃的法規更新。 問題搜尋可讓您依國家/地區、功能類型和版本進行搜尋。


[!INCLUDE[footer-include](../includes/footer-banner.md)]