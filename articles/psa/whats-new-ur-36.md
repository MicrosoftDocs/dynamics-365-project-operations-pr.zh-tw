---
title: Project Service Automation V3 更新版本 36 的新功能或變更內容
description: 本主題列出 Microsoft Dynamics 365 Project Service Automation 更新版本 36 V3 中可用的功能與修正。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 108c75598dc7dd3dd0cdb9ce68e30423d051a4cf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586656"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Project Service Automation V3 更新版本 36 的新功能或變更內容

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興發佈 Microsoft Dynamics 365 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 與 Dynamics 365 9.x 相容。 若要更新至此版本，請瀏覽系統管理中心以進入 Dynamics 365 online 解決方案頁面，並安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation 更新版本 36 V3 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.57.152，已於 2021 年 10 月透過自我更新正式推出。

## <a name="update-release-36"></a>更新版本 36

### <a name="bug-fixes"></a>錯誤修正

下列問題已獲修正。

**一般**
- **專案參數** 頁面上的 **預設工作時數範本** 欄位名稱翻譯不正確。
- 非同步外掛程式無法正確處理與 **SharedVariableService** 相關的例外狀況。

**時間和費用**
- 如果帳目明細遺失，或是使用者沒有帳目明細的適當讀取權限，則會在取消專案核准時出現不正確的錯誤。
- 當費用或時間項目有多個相關聯的專案核准時，使用者無法取消核准。
- **缺席** 與 **休假** 在 **時間項目** 快速建立頁面查詢中的中文語言翻譯不正確。

**資源管理**
- 當檢視模式設定為 **天**、**週** 或 **月** 時，使用者無法在 **排程小幫手** 中搜尋資源。
- 不正確地允許一般資源具有空白職位名稱。 
- 以未成交關閉合約並不會取消未來的預約。

**銷售**
- 當環境有大量產品時，**材料估計** 網格的效能會降低。
- 從範本建立專案時，專案貨幣不會預設為各自專案經理的合約單位。
- 實際金額不一定符合專案到期所反映的金額，或是金額在特定回收案例中變成負數。
- 將根據專案範本建立的專案關聯至合約服務內容時發生錯誤。
- 使用者可以刪除包含 **已準備好開立發票** 和 **發票已建立** 里程碑的合約服務內容。 不允許這樣做。
- 如果已從專案匯入估計值，則會在報價明細啟用工作型帳單時，不正確地設定報價明細詳細資料可收費率。
- 新增固定價格帳單里程碑時，除非重新整理頁面，否則里程碑不會反映在里程碑子網格中。
- 當您建立報價名稱為 Null 的專案合約時，會產生 Null 參考例外狀況。
- 專案貨幣與資源貨幣不同的手動模式工作會產生不正確的價格估計值。
- 使用者無法回收已由更正發票成功更正的交易。
- 已停用的交易類別會出現在 **費用估計值** 網格中。



