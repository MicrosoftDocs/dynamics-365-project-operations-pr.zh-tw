---
title: 設定非庫存材料和待處理廠商發票
description: 本文說明如何啟用非庫存材料和待處理廠商發票。
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6473ef3510f0d3641a2d61b6a1b1f28980993277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913748"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>設定非庫存材料和待處理廠商發票

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

## <a name="minimum-version-requirement"></a>最小版本需求

針對 Dynamics 365 Project Operations 非庫存/資源型案例使用非庫存材料和待處理廠商發票時，需要下列版本：

Dynamics 365 Dataverse 解決方案：

- Project Operations – 4.9.0.221 或更新版本
- 雙重寫入應用程式協調流程解決方案 - 2.2.2.23 或更新版本

Dynamics 365 Finance：
- 10.0.18 (10.0.793.52) 或更新版本。 確定您的 Finance 環境是最新的，且已套用所有品質更新以符合最小版本需求。

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>對非庫存材料與待處理廠商發票整合執行雙重寫入對應

本節提供有關非庫存材料和待處理廠商發票所需之特定對應的資訊。 確認[佈建新環境](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps)一文中列出的先決條件對應正在您的環境中執行。

1. 前往 Lifecycle Services (LCS)、瀏覽至您的 LCS 專案，然後移至 **環境詳細資料** 頁面。
2. 在 **Common Data Service 環境資訊** 區段中，選取 **連結至 CDS for Apps**。 選取連結之後，您會重新導向至對應中實體的清單。
3. 確定下列對應正在執行。 如果未在執行，請啟動這些對應，並務必將所有相關的資料表對應都加入。

    - CDS 已發行相異的產品 (產品)
    - 廠商 v2 (msdyn_vendors)
    - Project Operations 材料估計值資料表 (msdyn_estimatelines)
    - Project Operations 整合專案廠商發票匯出實體 (msdyn_projectvendorinvoices)
    - Project Operations 整合專案廠商發票明細匯出實體 (msdyn_projectvendorinvoicelines)
    - Project Operations 整合實際值 (msdyn_actuals)。 確定您正在執行對應版本 1.0.0.14 或更新版本。 您可以在 **雙重寫入** 頁面的 **版本** 欄中查看對應的使用中版本。 您可以選取 **資料表對應版本**，然後儲存選取的版本來啟用新的對應版本。

如果您使用的是標準範本資料，則可能還需要透過初始同步停止並重新啟動下列實體對應：
  - 付款日 CDS V2 (msdyn_paymentdays)
  - 付款排程 (msdyn_paymentschedules)
  - 付款條件 (msdyn_paymentterms)
  - 廠商群組 (msdyn_vendorgroups)
  - 單位 (uom)

> [!NOTE]
> 廠商群組與單位的初始同步可能會因為現有示範資料集中的一些記錄而失敗。 您可以忽略失敗，因為這些失敗不會阻止您搭配 Project Operations 使用示範資料。

## <a name="configure-prerequisites-in-dataverse"></a>設定 Dataverse 中的先決條件

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>啟用工作流程以根據廠商實體建立科目

雙重寫入協調流程解決方案提供[廠商主機整合](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping)。 做為此功能的先決條件，廠商資料必須是在 **客戶** 實體中建立。 啟用範本工作流程程序，以便在 **客戶** 資料表中建立廠商，如[在廠商設計之間切換](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch)中所述。

### <a name="set-products-to-be-created-as-active"></a>將所要建立的產品設定為使用中

非庫存材料必須在 Finance 中設定為 **已發行的產品**。 雙重寫入協調流程解決方案提供現成可用的 [Dataverse 產品類別目錄的已發行產品整合](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping)。 預設會以草稿狀態將產品從 Finance 同步處理至 Dataverse。 若要將產品同步處理為使用中狀態，以便直接使用於材料使用單據或待處理廠商發票，請移至 **系統** > **管理** > **系統管理** > **系統設定**，並在 **銷售** 索引標籤上，將 **以使用中狀態建立產品** 設定為 **是**。

## <a name="configure-prerequisites-in-finance"></a>設定 Finance 中的先決條件

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>啟用待處理廠商發票的功能金鑰

完成下列步驟，啟用可在待處理廠商發票明細上新增專案詳細資料的功能。

1. 在 Finance 中，移至 **功能管理** 工作區。
2. 在功能清單中，下列 **在資源型/非庫存案例適用的 Project Operations 上啟用待處理廠商發票**，然後選取 **啟用**。

### <a name="define-category-groups-and-project-categories-for-items"></a>定義項目的類別群組和專案類別

為 **項目** 交易類型設定至少一個類別群組，以及至少一個使用此群組的專案類別。 如需詳細資訊，請參閱[設定專案類別](../project-accounting/configure-project-categories.md#category-groups)。

檢閱專案成本和 營收設定檔，並設定項目交易的總帳過帳設定。 如需詳細資訊，請參閱[設定計費專案會計](../project-accounting/configure-accounting-billable-projects.md)。

### <a name="set-up-a-write-in-product"></a>設定目錄外產品

在 Project Operations 中，您可以針對已發行產品類別目錄中所設定的產品類別目錄以及針對目錄外產品，記錄其材料估計值和使用方式。 使用目錄外產品需要已在 Finance 中針對此目的所設定的單一已發行產品。 完成下列步驟以設定目錄外產品。 在每個使用資源/非庫存案例適用的 Project Operations 的法律實體中重複這些步驟。

1. 在 Finance 中，移至 **產品資訊管理** > **產品** > **已發行產品**，然後選取 **新增**。
2. 在 **產品類型** 欄位中，選取 **項目**，並在 **產品子類型** 欄位中選取 **產品**。
3. 輸入產品編號 (WRITEIN) 和產品名稱 (目錄外產品)。
4. 選取項目模型群組。 產品您所選項目模型群組的 **庫存原則庫存產品** 欄位已設定為 **False**。
5. 選取 **項目群組**、**儲存體維度群組** 和 **追蹤維度群組** 欄位中的值。 僅使用 **網站** 的 **儲存體維度**，並在 **追蹤維度** 欄位中選取 **無**。
6. 選取 **庫存單位**、**採購單位** 和 **銷售單位** 欄位中的值，然後儲存您的變更。
7. 在 **計劃** 索引標籤中，設定預設訂單設定，並在 **庫存** 索引標籤上設定預設地點和倉庫。
8. 移至 **專案管理與會計** > **設定** > **專案管理與會計參數**，並開啟 **Dynamics 365 Dataverse 上的 Project Operations**。 
9. 在 **材料** 索引標籤的 **目錄外產品** 欄位中，選取您所建立的產品。
10. 在 Dataverse 環境的網站地圖中，開啟 **產品** 實體並尋找目錄外產品記錄。 
11. 開啟記錄詳細資料，並將產品狀態設定為 **已淘汰**。 此產品狀態可防止任何人不慎在材料估計值及使用單據中直接使用此記錄。

### <a name="set-up-a-procurement-integration-account"></a>設定採購整合科目

採購整合科目會在以歸屬於專案的明細進行待處理廠商發票過帳時，做為結算科目。

系統將待處理廠商發票過帳時，專案成本金額會使用此科目。 系統會在 Dataverse 中處理廠商發票詳細資料，並且建立對應的專案實際值。 專案實際值的資訊會新增至 Project Operations 整合帳目。 將整合帳目過帳時，金額會從採購整合科目結清並記錄至專案成本。

1. 若要設定採購整合科目，請移至 **專案管理與會計** > **設定** > **專案管理與會計參數**，並開啟 **Dynamics 365 Dataverse 上的 Project Operations**。 
2. 選取 **材料** 索引標籤，並選取 **採購整合科目** 欄位中的值。

#### <a name="set-up-project-category-defaults-for-an-item"></a>設定項目的專案類別預設值

1. 在 Finance 中，移至 **專案管理與會計** > **設定** > **專案管理與會計參數**，並開啟 **Dynamics 365 Dataverse 上的 Project Operations**。 
2. 在 **專案類別預設值** 索引標籤的 **項目** 欄位中，選取值。 如果專案實際值記錄中未設定專案類別，則材料交易會使用此專案類別。
