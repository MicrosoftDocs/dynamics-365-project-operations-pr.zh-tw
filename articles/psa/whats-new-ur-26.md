---
title: Project Service Automation V3 更新版本 26 的新功能或變更內容
description: 本主題列出 Project Service Automation 更新版本 26 V3 中提供的功能和修正。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948814"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation 更新版本 26 V3

[!include [banner](../includes/psa-now-project-operations.md)]

我們很高興地宣佈 Dynamics 365 的 Project Service Automation 應用程式的最新更新。 此版本包含一些對品質、效能和可用性的重要改進。 此版本與 Dynamics 365 9. x 相容。 若要更新至此版本，請前往 Dynamics 365 online 系統管理中心，請移至解決方案頁面以安裝更新。 如需詳細資訊，請參閱[安裝、更新或移除偏好的解決方案](/power-platform/admin/install-remove-preferred-solution)。

本主題列出 Project Service Automation 更新版本 26 V3 新推出或已變更的功能及修正。 此版本的組建編號為 V3.10.44.59，一般可透過 2020 年 12 月的自我更新獲得。

## <a name="update-release-26"></a>更新版本 26

### <a name="bug-fixes"></a>Bug 修正

**時間和費用**

下列問題已獲修正：

- 使用者可以變更已核准/已送出之時間項目上的工作。
- 儲存時間項目時發生「物件參照未設定」錯誤。
- 從資源指派匯入的時間項目會建立具有不正確日期時間值的時間項目。
- 當 Project Service Automation 與 Field Service 應用程式皆已安裝時，**新增** 按鈕在命令列上為 Field Service 應用程式中的時間項目顯示兩次。
- **允許單位** 與 **單位群組** 儲存格更新現在可在 **費用估計值** 窗格中運作。
- **更新時間項目編輯** 表單包括 **時間表**。
- 非專案時間項目的時間核准會在搜尋專案核准者角色時封鎖系統。

**資源管理**

下列問題已獲修正：

- 新增在 **PostProjectCreate** 外掛程式中的驗證，以在建立之前檢查主要需求。
- 如果已從表單移除欄位，則 **專案團隊成員** 快速建立表單將會擲回 null 參照例外狀況。
- 產生超過 1 年的 12 小時需求將會失敗。
- 在建立資源需求期間，改善了錯誤訊息 null 參照例外狀況。

**專案管理**

下列問題已獲修正：

- 改善驗證以解決 **PreProjectUpdate** 外掛程式中所產生的 null 參照例外狀況。
- Microsoft Project 桌面增益集所發行的專案會刪除未指派的指派。
- 新增驗證以因應 **PreValidateProjectTaskUpdate** 外掛程式中的 null 參照例外狀況而導致工作專案參照無效。
- 團隊成員網格不會在團隊成員記錄中顯示不同的指派。
- 由於 **PreProjectTaskDelete** 外掛程式中的 null 參照例外狀況而新增了新的驗證和錯誤訊息。

**Sales**

下列問題已獲修正：

- 當選取報價或合約中的專案型條項時，只有在選取與現有產品相關的專案型條項時，才會顯示 **建議** 按鈕。
- 從 **Create_ProjectContract** 權限分割 **Create_Product** 權限。
- 刪除發票明細會造成 **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** 上的 null 參照失敗。


[!INCLUDE[footer-include](../includes/footer-banner.md)]