---
title: 使用可預約資源做為定價維度
description: 本主題提供有關如何使用可預約資源做為定價維度的資訊。
author: Rumant
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0c5cb85f7c43f7b2fd9c367d7f7ac9c3250e0a1
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643073"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>使用可預約資源做為定價維度

 _**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_ 

本主題提供有關如何使用可預約資源做為定價維度的資訊。 如果您設定了定價策略，讓每個可預約資源都必須具有特定的價格或成本費率，請使用可預約資源作為定價維度。

## <a name="prerequisites"></a>先決條件
在您完成本主題中的步驟之前，您必須有一個新的定價維度解決方案供您的組織使用。 如果尚未建立一個，請參閱[建立自訂欄位和實體](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md)。

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>將可預約資源欄位新增至表單和檢視表
若要讓 **可預約資源** 欄位顯示在定價維度解決方案中，您必須將欄位做為實體新增至所有表單和檢視表。

下表依實體列出所有現成可用的表單和檢視表。 您也必須將新欄位新增至自訂實體中的任何其他表單或檢視表。

|   Entity        | 表單   |檢視表        |
| ------------------------------|---------------------------------|----------------------------------|
|  角色價格| 資訊 | - 使用中資源類別價格<br> - 資源類別價格相關 |
|  角色價格加成| 資訊| - 使用中角色價格加成<br>- 角色價格加成相關 |
|  報價明細詳細資訊| - 專案資訊<br>- 專案快速建立| - 使用中報價明細詳細資訊<br>- 合併的報價明細詳細資料<br>- 報價明細詳細資料相關 |
|  • 專案合約服務內容詳細資料| - 專案資訊<br>- 專案快速建立| - 合併的合約服務內容詳細資料<br>- 使用中合約服務內容詳細資料<br>- 合約服務內容詳細資料相關 |
|  專案工作| - 資訊<br>- 新表單| &nbsp; |
|  專案團隊成員| - 資訊<br>- 新表單| - 使用中專案團隊成員<br>- 專案團隊成員<br>- 專案團隊成員相關 |
|  時間項目| - 資訊<br>- 建立時間項目| - 我依日期的時間項目<br>- 我本週的時間項目<br>- 供核准的時間項目|
|  帳目明細| - 資訊<br>- 快速建立| - 使用中帳目明細<br>- 帳目明細相關 |
|  發票明細詳細資料| - 資訊<br>- 快速建立| - 使用中發票明細詳細資料<br>- 應收費發票交易<br>- 附贈發票交易<br>- 發票明細詳細資料相關 <br>- 不應收費發票交易|
|  實際| - 資訊<br>- 使用中實際值| 實際值相關 |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>將可預約資源設定為定價維度
若要將可預約資源設定為定價維度，請執行下列步驟：

1. 移至 **設定** > **參數**。 
2. 在 **參數** 頁面的 **以金額為準的定價維度** 索引標籤上，確認網格會顯示 **定價維度** 實體中的記錄。 
2. 將 **可預約資源** 新增至此定價維度清單做為 **msdyn_bookableresource**。 
3. 在 **適用於成本** 和 **適用於銷售** 中，選取一個值。
4. 在 **維度類型** 中，選取 **以金額為準**。 
5. 選取可預約資源的成本及銷售優先順序。 可預約資源納入做為定價維度時，通常會有最高的優先順序。 將優先順序設定為 **1** (或 **0**，視優先順序計數方式而定) 可確保該行為。

## <a name="set-up-pricing-dimension-field-names"></a>設定定價維度欄位名稱

當 **角色價格** 表格中的定價維度欄位名稱與使用預設價格的任何其他實體中的欄位名稱不同時，就必須通知定價維度記錄有不同的名稱。  

至於可預約資源，**專案團隊成員** 實體的欄位名稱與其在 **角色價格** 實體上稱呼的名稱略微不同： 

 - **專案團隊成員** 實體 = **msdyn_bookableresourceid**
 - **角色價格** 實體 = **msdyn_bookableresource**

您必須讓 **msydn_bookableresource** 的定價維度記錄得知此點差異。

1. 按兩下 **定價維度** 網格中的列，以開啟 **msdyn_bookableresource** 的維度頁面。
2. 在維度頁面的 **相關** 索引標籤上，選取 **定價維度欄位名稱**。

  ![[定價維度欄位名稱] 索引標籤](media/PD-fieldname.png)

3. 在開啟的相關檢視表上，選取 **新增定價維度欄位名稱**。

  ![新增定價維度欄位名稱](media/Add-NewPD-fieldname.png)

  這會開啟 **msdyn_bookableresource** 的 **新增定價維度欄位名稱** 頁面。 

4. 在 **新增定價維度欄位名稱** 頁面上，新增 **msdyn_projectteam** 至 **實體邏輯名稱**。
5. 將 **msdyn_bookableresourceid** 新增至 **欄位名稱**。

 ![新增定價維度欄位名稱表單](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]