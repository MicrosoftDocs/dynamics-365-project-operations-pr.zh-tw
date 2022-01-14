---
title: 2021 年 12 月新增功能 - Project Operations 精簡部署
description: 本主題提供有關 Project Operations 精簡部署 2021 年 12 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942967"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>2021 年 12 月新增功能 - Project Operations 精簡部署

_適用於：精簡部署 - 交易至開立預估發票_

本主題適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.27.0.195、4.27.0.242 版中的 Project Operations


## <a name="features-included-in-this-release"></a>此版本包含的功能

### <a name="subcontract-management"></a>轉包合約管理 

- [轉包專案團隊成員](../subcontracting/subcontracting-project-team-members.md)：專案經理可以使用轉包合約和轉包合約服務內容建立具名或一般團隊成員，以便影響人員配置和估計。
- [專案團隊成員的轉包選項](../subcontracting/subcon-options.md)：為具名或一般專案團隊成員選擇人員配置時，專案經理可以檢閱現有的轉包合約，或是為一個或多個專案團隊成員建立新的轉包合約。 
- [已轉包資源指派的成本估計](../subcontracting/costing-subcon-ra.md)：專案成本估計會將轉包的資源指派列入考慮，並使用與轉包合約相關聯的利購價目表來計算這些指派的成本。 
- [設定排程面板以顯示合約工作者和已轉包產能](../subcontracting/configure-sb-subcon.md)：Project Operations 中的排程面板現在可進行設定，以搜尋並建議可預約資源的合約工作者類型和已轉包產能以及員工。 當您在為特定專案需求配置人員的情境中搜尋資源時，或是在專案需求的情境以外進行搜尋時，可以套用此設定。
- [使用合約工作者和已轉包產能為專案配置人員](../subcontracting/staffing-cw.md)：合約工作者現在可以在專案上利用排程面板體驗進行預約。
- [在已轉包元件的專案上記錄時間、費用及材料使用方式](../subcontracting/recording-subcon-actuals.md)：合約工作者可以記錄時間和費用，而專案團隊成員也可以記錄使用專案的轉包合約所購買之材料的使用方式。 這終歸會在使用所購產能或材料的專案中記錄正確的成本。
- [轉包合約的狀態轉換](../subcontracting/subcon-states.md)：您可以確認轉包合約來完成與廠商的交涉、將其關閉來指示交貨完成，或是在完成交貨前加以取消來表示終止與廠商的合約。

### <a name="task-planning"></a>工作規劃
- 改善系統管理員的疑難排解功能。 當使用者無法開啟專案時，系統管理員可以檢閱[專案排程記錄](../../project-management/schedule-api-logs.md)中由 Project for the Web 所產生的非授權相關錯誤。
- [使用 Project for the Web 中的工作檢查清單](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)。 在 Project for the Web 中，您可以將檢查清單新增至工作來追蹤特定項目。

## <a name="quality-updates"></a>品質更新

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 規劃和追蹤 | 2392596 | 排程 API 現在允許更新 **剩餘未完成投入**、**已完成的投入** 和 **完成百分比** 欄位。 |
| 規劃和追蹤 | 2478497 | 排程 API 的 **活動編號** 和 **工作識別碼** 欄位在輸入時可以是空白，因為系統會使用自動編號來填入這些值。|
| 時間和費用 | 2468135 | 核准重試次數從五次減少為三次。 |
| 時間和費用 | 2468188 | 修正記錄文字超過 **註釋** 實體之 **notetext** 屬性中長度上限的問題。 |
