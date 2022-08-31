---
title: 同步專案狀態以防止進入已結案的專案
description: 本文解釋如何同步專案狀態，以防止進入非使用中或已結案的專案。
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348006"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>同步專案狀態以防止進入已結案的專案

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

## <a name="scenario"></a>案例

Contoso 正在將資源/非庫存案例適用的 Microsoft Dynamics 365 Project Operations 投入實際運作。 在正常的商務活動中，專案可能會完成或暫停。 您可以停用專案，以確保不會產生任何費用或發票。

## <a name="solution"></a>方案

### <a name="prerequisites"></a>先決條件

-   必須安裝 Microsoft Dynamics 365 Finance 10.0.29 或更新的版本。
-   必須按照底下所述，安裝或手動設定專案 V2 的雙重寫入對應 1.0.0.3 (msdyn \_projects) 。

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>建立 Project Operations 整合專案 V2 雙重寫入對應的的更新版本

若要更新 Project Operations 專案 V2 的雙重寫入對應：

1. 請移至 **資料管理** 工作區，並選取 **雙重寫入**。
2. 選取 **雙重寫入** 圖標。
3. 從 T **Table map** 欄中，尋找並選取 **專案 V2 (msdyn \_projects)**，然後選取停止。
4. 選取對應名稱以打開對應，然後選取 **[無]**。
5. 從選取欄對話方塊中，選取 **statecode \[Project Status \]**，然後選取確定。 您可以在篩選條件值中輸入 **狀態**，以縮小清單的範圍。
6.  在 **對應類型** 欄中，選取 **新增或編輯轉換**，以編輯轉換。
7.  從 **轉換類型** 選取 **ValueMap**。
8.  選取 **新增值對應**，然後新增下列 **鍵** 和 **值**：

   機碼       | 數值 
   ----------|-------
   InProcess | 12     
   已完成 | 7     

![顯示雙重寫入對應的螢幕截圖](media/projectstage-dw-mapping.png)

9. 選取 **儲存**。
10. 從 **雙重寫入 > 專案 V2 (msdyn_projects)** 頁面的頂端 ，選取 **另存新檔**。
11. 從 **發行者** 欄位中的 **新增資料表**，選取 **CDS 預設發行者**。
12. 設定 **版本** 欄位為 1.0.0.3。
13. 輸入 **描述**，然後選取 **儲存**。
14. 從 **雙重寫入 > 專案 V2 (msdyn_projects)** 頁面的頂端 ，選取 **執行** 以開始對應，然後選取 **是** (如果系統要求在執行之前確認)。 

### <a name="close-a-newly-completed-project"></a>關閉剛完成的專案

Dynamics 365 Finance 使用 **專案階段** 欄位來區分 **進行中** 或 **已完成** 的專案 。 **已完成** 的專案無法支付費用或為客戶開出發票。

1. 打開要停用的專案。
2. 從功能區選取 **停用**。

> [!NOTE]
> 您可以停用或關閉專案，因為它們在 Finance 背景中的行為相同。

3. 在 Finance 中，打開 **所有專案清單** 頁面。
4. 確認已停用的專案未出現在清單中。
5. 在 **顯示專案** 篩選清單上方，將值從 **進行中** 變更為 **全部**。
6. 您現在會看到已停用的專案。

如果您想在 Finance 中針對此專案記錄時間或費用，您就不應該看到要選取的專案。 如果您手動輸入費用的專案編號，您會看到類似「專案階段已完成，無法在專案中記錄」的訊息。 必須停用發票及其他帳務功能，因為它們將會在已關閉專案的背景中。

