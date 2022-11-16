---
title: 從 Project Service Automation 升級至 Project Operations
description: 本文概述從 Microsoft Dynamics 365 Project Service Automation 升級至 Dynamics 365 Project Operations 的程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736656"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>從 Project Service Automation 升級至 Project Operations

我們很高興宣布從 Microsoft Dynamics 365 Project Service Automation 升級至 Microsoft Dynamics 365 Project Operations 的三個階段中的第二階段。 本文為參與這段精彩過程的客戶提供概觀。 

升級傳遞計劃分成三個階段。

| 升級傳遞 | 階段 1 (2022 年 1 月) | 階段 2 (2022 年 11 月) | 階段 3 (2023 年 4 月浪潮)  |
|------------------|------------------------|---------------------------|---------------------------|
| 對專案的分工結構圖 (WBS) 沒有相依性 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| 在 Project Operations 目前支援的限制中的 WBS | | :heavy_check_mark: | :heavy_check_mark: |
| 在 Project Operations 目前所支援之限制 (包括對 Project Desktop Client 的支援) 以外的 WBS | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>升級程序功能 

在升級程序中，已將升級記錄新增至網站地圖，讓系統管理員可以更輕鬆地診斷失敗。 除了新的介面之外，還會加入新的驗證規則，以確保升級後的資料完整性。 下列驗證將會新增至升級程序。

| 驗證 | 階段 1 (2022 年 1 月) | 階段 2 (2022 年 11 月) | 階段 3  |
|-------------|------------------------|---------------------------|---------------------------|
| 將會對 WBS 進行一般資料完整性違規方面 (例如，資源指派與相同的上層工作相關聯，卻有不同的上層專案) 的驗證。 | | :heavy_check_mark: | :heavy_check_mark: |
| 將會對 WBS 進行 [Project for the Web 已知限制](/project-for-the-web/project-for-the-web-limits-and-boundaries)方面的驗證。 | | :heavy_check_mark: | :heavy_check_mark: |
| 將會對 WBS 進行 Project Desktop Client 已知限制方面的驗證。 | |  | :heavy_check_mark: |
| 將會對可預約資源和專案行事曆進行一般不相容行事曆規則例外方面的評估。 | | :heavy_check_mark: | :heavy_check_mark: |

在階段 2 中，升級至 Project Operations 的客戶會將其現有專案升級為專案規劃的唯讀體驗。 在此唯讀體驗中，追蹤網格將可顯示完整的 WBS。 若要編輯 WBS，專案經理可以在專案的主要頁面中選取 [**轉換**](/PSA-Upgrade-Project-Conversion.md)。 背景程序接著更新專案，以便支援 Project for the Web 的全新專案排程體驗。 此階段適用於專案在 [Project for the Web 已知限制](/project-for-the-web/project-for-the-web-limits-and-boundaries)範圍內的客戶。

在階段 3 中，顧及客戶想要繼續透過該應用程式編輯其專案的權益，將會新增對 Project Desktop Client 的支援。 不過，如果現有的專案已轉換為新的 Project for the Web 體驗，則會停用每個已轉換專案存取增益集的權限。

## <a name="prerequisites"></a>先決條件

若要取得階段 1 升級的資格，您必須符合下列準則：

- 目標環境不得包含 **msdyn_projecttask** 實體中的任何記錄。
- 必須將有效的 Project Operations 授權指派給所有的使用中使用者。 
- 您必須在至少一個包含與生產環境協調一致之代表性資料集的非生產環境中驗證升級程序。
- 目標環境必須已更新至 Project Service Automation 更新版本 37 (V3.10.58.120) 或更新的版本。

若要取得階段 2 升級的資格，您必須符合下列準則：

- 必須將有效的 Project Operations 授權指派給所有的使用中使用者。 
- 您必須在至少一個包含與生產環境協調一致之代表性資料集的非生產環境中驗證升級程序。
- 目標環境必須已更新至 Project Service Automation 更新版本 37 (V3.10.58.120) 或更新的版本。
- 只有在每個專案的工作總數為 500 或更少時，才會支援包含工作 (msdyn_projecttask) 的環境。

階段 3 的先決條件將會在正式發行日期臨近時進行更新。

## <a name="licensing"></a>授權

如果您有 Project Service Automation 的有效授權，則可以安裝和使用 Project Operations，其中包含 Project Operations 所有的功能以及其他項目。 如此一來，您就可以測試 Project Operations 的功能，同時繼續在生產環境中使用 Project Service Automation。 當您的 Project Service Automation 授權到期後，您必須轉換到 Project Operations。 規劃這次轉換時，您必須考慮到 Project Operations 授權沒有包含 Project Service Automation 授權的事實。 如果客戶已部署 Project Service Automation，並在計劃遷移至 Project Operations 時需要繼續使用或增加其 PSA 授權，則可能會在這些情況下根據已購買的 Project Operations 授權要求暫時 PSA 授權。 一個 Project Operations 授權會發行一個 Project Service Automation 授權。 您可以使用下列連結來要求暫時 PSA 授權：aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>測試和重構自訂

一開始，先將所有自訂匯入至全新的 Project Operations (精簡) 環境，以確認匯入是否成功，以及業務運作方式是否如預期那般。

以下是一些要注意的事項：

- 匯入可能會因為遺失相依性而失敗。 換句話說，自訂參考了 Project Operations 中已移除的欄位或其他元件。 在這種情況下，請從開發環境中移除這些相依性。
- 如果未受管理和受管理的解決方案包含未自訂的元件，請從解決方案移除這些元件。 例如，當您自訂 **專案** 實體時，只將實體標頭新增至解決方案。 請勿新增所有的欄位。 如果您先前已新增所有子元件，則可能必須手動建立新的解決方案，然後在其中新增相關元件。
- 表單和檢視表可能無法如預期般顯示。 在某些情況下，如果您已自訂任何現成可用的表單或檢視表，這些自訂可能會讓 Project Operations 中新的更新無法生效。 若要找出這些問題，建議您對 Project Operations 的全新安裝以及包含自訂的 Project Operations 安裝進行並排檢閱。 比較業務中最常用的表單，以確認您這一版的表單是否仍可發揮作用，以及全新版本的表單中是否遺失了什麼。 對任何您已自訂的檢視表，進行同樣類型的並排檢閱。
- 商務規則可能會在執行階段失敗。 由於匯入時不會對外掛程式中的欄位參考進行驗證，商務規則可能會因為欄位參考已不存在而發生失敗，而您可能會收到類似下列範例的錯誤訊息：「[專案] 實體未包含 Name = 'msdyn_plannedhours' 和 NameMapping = 'Logical' 的屬性」。在這種情況下，請修改您的自訂，讓這些自訂使用新的欄位。 如果您在外掛程式邏輯中使用自動產生的 Proxy 類別和強型別參考，請考慮從全新安裝中重新產生這些 Proxy。 如此一來，您就可以輕鬆找出外掛程式相依於已被取代欄位的所有位置。

將自訂更新為完全匯入 Project Operations 之後，請到下一個步驟繼續執行。

## <a name="end-to-end-testing-in-development-environments"></a>在開發環境中進行端對端測試

### <a name="initiate-upgrade"></a>開始進行升級 

1. 在 Power Platform 系統管理中心，尋找並選取您的環境。 然後在應用程式中尋找並選取 **Dynamics 365 Project Operations**。
2. 選取 **安裝** 以開始升級。 Power Platform 系統管理中心會將此安裝顯示為全新安裝。 不過，將會偵測到舊版 Project Service Automation 的存在，而且會升級現有的安裝。

    升級完成後，環境應該會指出已安裝 Project Operations，但未安裝 Project Service Automation。

    視環境中的資料量而定，升級可能需要數小時的時間。 管理升級的核心團隊應進行相應的規劃，並在非營業時間執行升級。 在某些情況下，如果資料量龐大，最好在週末執行升級。 對於排程的決策應根據較低階環境中的測試結果來制定。

3. 視情況而定升級自訂解決方案。 此時，請部署您在本文的[測試和重構自訂](#testing-and-refactoring-customizations)區段對自訂所做的任何變更。
4. 移至 **make.powerapps.com**，從入口網站右上角的下拉式清單中選取您的環境，從左功能表選取 **解決方案**，再選取 **Project Operations 已取代的元件** 解決方案並 **解除安裝**。

    此解決方案是保存升級過程中存在之資料模型和元件的暫時解決方案。 移除此解決方案，就會移除所有不再使用的欄位和元件。 如此一來，就有助於簡化介面，使整合和擴充變得更輕鬆。
    
### <a name="upgrade-to-project-operations-lite"></a>升級至 Project Operations 精簡版

下列步驟說明升級程序以及相關聯錯誤記錄：

1. **PSA 版本檢查：** 若要安裝 Project Operations，您必須有 V3.10.58.120 或更新版本。
1. **預先驗證：** 當系統管理員開始進行升級時，系統會對每個屬於 Project Operations 解決方案核心的實體執行預先驗證作業。 此步驟會驗證是否所有實體參考都有效，並確保與 WBS 相關的資料是在 Project for the Web 的已發佈限制內。
1. **中繼資料升級：** 成功進行預先驗證之後，系統會開始對結構描述進行變更，並建立已取代元件解決方案。 完成自訂項目的所有必要重構之後，您可以移除這個已取代解決方案。 此步驟是升級程序中最長的一部分，最多可能需要四個小時才能完成。
1. **資料升級：** 在中繼資料升級步驟中完成所有必要的結構描述變更之後，您的資料會移轉至新的結構描述，而且所有必要的預設設定和重新計算都會完成。
1. **專案排程引擎更新：** 成功進行資料升級之後，主要頁面上的 **排程** 索引標籤的標籤會重新指派為 **工作**。 當使用者在升級後選取此索引標籤時，系統會引導他們瀏覽至追蹤網格，以檢視 WBS 的唯讀版本。 若要編輯 WBS，他們必須開始執行排程[轉換程序](/PSA-Upgrade-Project-Conversion.md)。 所有沒有既存 WBS 的專案都可以不經轉換，直接使用新的排程體驗。
 
### <a name="validate-common-scenarios"></a>驗證常見案例

驗證您的特定自訂時，建議您還要審查各應用程式支援的商務程序。 這些商務程序包括 (但不限於) 建立銷售實體 (例如報價和合約)，以及建立包含 WBS 和實際值核准的專案。

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Project Service Automation 與 Project Operations 之間的主要變更

本節提供 Project Service Automation 與 Project Operations 間可預期之主要變更的摘要。

### <a name="project-planning"></a>專案規劃

Project Operations 中的專案規劃功能不再依賴於用戶端邏輯與伺服器端邏輯的組合。 Project Operations 反而會使用 Project for the Web 做為其排程引擎。 排程功能中的這項變更會啟用數種新功能，例如面板和甘特圖檢視、資源導向規劃、[工作檢查清單項目](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)以及專案排程模式。 也有一組豐富的全新[應用程式開發介面 (API)](../project-management/schedule-api-preview.md) 支援這些新的排程功能。 這些 API 旨在協助確保 WBS 中建立、更新或刪除實體的程式設計作業不會損毀排程中的導出欄位。

### <a name="billing-and-pricing"></a>帳單和定價

繼續投資 Project Operations 時，有多項新功能可在帳單和定價中使用。 以下列出一些範例：

- [記錄專案和專案工作的材料使用方式](../material/material-usage-log.md)
- [轉包合約管理](../pro/subcontracting/managing-subcontracts-overview.md)
- [預付金或定額保留後隨用即扣型合約](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [合約不得超過狀態和驗證](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- 工作型帳單

### <a name="resource-management"></a>資源管理

Project Operations 為 Universal Resource Scheduling (URS) 面板和排程小幫手提供選擇性支援。 這項新的體驗將會在 2023 年 4 月浪潮中成為強制性體驗。

## <a name="frequently-asked-questions"></a>常見問題

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>目前支援哪些部署類型進行升級？

| Source                                                 | Target                                                    | 執行狀態                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations 精簡部署                        | 支援               |
| Dynamics 365 Finance 專案管理與會計 | Project Operations 精簡部署                        | 目前不支援 |
| Finance 專案管理與會計              | 資源/非庫存案例適用的 Project Operations     | 目前不支援 |
| Project Service Automation 3.x                         | 資源/非庫存案例適用的 Project Operations     | 目前不支援 |
| Project for the Web (專用環境)            | Project Operations 精簡部署                        | 目前不支援 |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>如何在升級工具推出之前，先安裝 Project Operations？

有兩個選項可讓您在升級工具推出前安裝 Project Operations：

- 佈建新的環境。
- 在任何不存在 Project Service Automation 的銷售組織中，個別部署 Project Operations。

如果 Project Service Automation 已安裝在組織上，但未使用，則可以將其解除安裝。 完全移除 Project Service Automation 後，就可以將 Project Operations 安裝在那個組織中。
