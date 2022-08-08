---
title: 在完全移轉時遷移完整開立發票的帳單里程碑
description: 本文說明如何遷移固定價格的帳單里程碑，此里程碑已在投入實際運作日期之前向客戶開立未交付專案合約的發票。
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028692"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>在完全移轉時遷移完整開立發票的帳單里程碑

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

## <a name="scenario"></a>案例

Contoso 正在將資源/非庫存案例適用的 Microsoft Dynamics 365 Project Operations 投入實際運作。 在完全移轉活動中，實作團隊必須從舊系統中遷移未交付的專案合約。 部分專案合約包含使用固定價格計費方式的合約服務內容，並且已部分開立發票給最終客戶。 實作團隊必須將這些帳單里程碑遷移為 **已過帳的客戶發票**，因為必須將這些里程碑包含在總合約價值中才能達到認列營收的目的。 然而，不可讓應收帳款和總帳的客戶餘額受到影響。

## <a name="solution"></a>方案

### <a name="prerequisites"></a>先決條件

- 必須安裝 Dynamics 365 Finance 10.0.24 或更新版本。
- 將完成遷移步驟的環境必須處於維護模式。 進行里程碑遷移時，不可執行任何其他活動。
- 遷移步驟必須完全依照本文所述方式進行，並且只能用於完全移轉活動。 Microsoft 不支援此功能的任何其他用途。

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>建立 Project Operations 整合合約服務內容里程碑雙重寫入對應的的完全移轉版本 

1. 確定 **Project Operations 整合合約服務內容里程碑** 實體的目標對應已是最新狀態。 

    1. 在 Finance 中，移至 **資料管理** \> **資料實體**，然後選取 **Project Operations 整合合約服務內容里程碑** 實體。 
    2. 選取 **修改目標對應**。 
    3. 在 **將暫存對應至目標** 頁面上，選取 **產生對應**，然後確認您要產生對應。

2. 停止並重新整理 **Project Operations 整合合約服務內容里程碑** (**msdyn\_contractlinescheduleofvalues**) 雙重寫入對應。 

    1. 移至 **資料管理** \> **雙重寫入**、選取對應，然後開啟其詳細資料。 
    2. 選取 **停止**，並等待直到系統停止對應為止。 
    3. 選取 **重新整理資料表**。

3. 新增交易狀態的對應。

    1. 選取 **新增對應**。
    2. 在新明細的 **財務和營運應用程式** 欄中，選取 **TRANSSTATUS \[TRANSSTATUS\]** 欄位。
    3. 在 **Microsoft Dataverse** 欄中，選取 **msdyn\_invoicestatus \[Invoice status\]**。
    4. 在 **對應類型** 欄中，選取向右箭頭 (**\>**)。
    5. 在出現的對話方塊中，選取 **同步方向** 欄位中的 **Dataverse 財務和營運應用程式**。
    6. 選取 **新增轉換**。
    7. 在 **轉換類型** 欄位中，選取 **ValueMap**。
    8. 選取 **新增值對應**。
    9. 在左側欄位中，輸入 **4**。 在右側欄位中，輸入 **192350001**。 
    10. 選取 **儲存**，然後關閉對話方塊。

4. 選取 **另存新檔** 以儲存雙重寫入對應的版本。 
5. 在 **新增資料表** 窗格的 **發行者** 欄位中，選取 **預設發行者**。
6. 在 **版本** 欄位中輸入版本。
7. 在 **描述** 欄位中，輸入此完全移轉版本對應的附註。 
8. 選取 **儲存**。
9. 開始執行對應。

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>將已開立發票的里程碑遷移至 Dataverse 環境

1. 在 Project Operations Dataverse 環境中，建立發票狀態為 **已準備好開立發票** 的里程碑。 此時，不要遷移任何尚未開立發票的里程碑。

    > [!NOTE]
    > 遷移帳單里程碑之前，請確定與專案合約服務內容相關的財務維度是依預期方式進行設定。 遷移完成後，無法編輯財務維度。

2. 遷移所有的里程碑之後，停止下列雙重寫入對應：

    - Project Operations 整合合約服務內容里程碑 (msdyn\_contractlinescheduleofvalues)
    - Project Operations 整合實際值 (msdyn\_actuals)
    - 專案發票提案 V2 (發票)

    若要停止對應，請依照下列步驟進行：

    1. 在 Finance 中，移至 **資料管理** \> **雙重寫入**、選取對應，然後開啟其詳細資料。
    2. 選取 **停止**，並等待直到系統停止對應為止。

3. 在 Project Operations Dataverse 環境中，建立並確認帳單里程碑的預估發票。 

    1. 在網站地圖中，移至專案合約、選取合約，然後選取 **建立發票**。
    2. 建立發票之後，從網站地圖的 **發票** 功能表中開啟這些發票，然後選取 **確認**。

    此步驟會在 Dataverse 環境中建立必要的記錄。 但是，並不會影響財務值和應收帳款，因為先前列出的雙重寫入對應已停止。

4. 確認過所有的預估發票之後，所有雙重寫入對應都會回復至其初始狀態。

    1. 將 **Project Operations 整合合約服務內容里程碑** (**msdyn\_contractlinescheduleofvalues**) 雙重寫入對應的版本更新回到原始版本。 
    2. 在對應清單中選取雙重寫入對應、選取 **資料表對應版本**，然後選取資料表對應的原始版本。
    3. 選取 **儲存**。
    4. 重新啟動下列雙重寫入對應：

        - Project Operations 整合合約服務內容里程碑 (msdyn\_contractlinescheduleofvalues)
        - Project Operations 整合實際值 (msdyn\_actuals)
        - 專案發票提案 V2 (發票)

里程碑現已遷移，且系統已準備好進行完全移轉活動中的後續步驟。
