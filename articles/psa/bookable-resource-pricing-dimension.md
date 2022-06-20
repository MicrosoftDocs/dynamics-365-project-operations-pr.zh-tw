---
title: 使用可預約資源做為定價維度
description: 本文提供有關使用可預約資源做為定價維度的資訊。
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: becb64bb137079422a765dd7cd61369297e1ffb1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916094"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>使用可預約資源做為定價維度

[!include [banner](../includes/psa-now-project-operations.md)]

本文提供有關使用可預約資源做為定價維度的資訊。 開始之前，如果尚未建立定價維度解決方案，就必須建立新的定價維度。 如果已經有定價維度解決方案，則可以在該解決方案中進行變更。 如果您沒有為組織建立新的定價維度解決方案，請完成[建立自訂欄位和實體](create-custom-fields-entities.md)文章中的程序。

## <a name="add-bookable-resource-to-forms-and-views"></a>將可預約資源新增至表單和檢視表
若要讓欄位在定價維度解決方案的 UI 中可見，您必須逐步瀏覽主要 Project Service 實體的所有表單和檢視表，並將這些欄位新增至這些實體的表單和檢視表中。
下表是一份需要更新的預設表單及檢視表完整清單 (依實體列出)。 如果這些實體的自訂中有任何其他檢視表或表單，也請將新欄位新增至其中。
開啟定價維度解決方案的方案總管，然後按一下 **發行所有自訂**。


|   實體        | 表單   |檢視表        |
| ------------------------------|---------------------------------|----------------------------------|
|  角色價格|• 資訊 |• 使用中資源類別價格<br> • 資源類別價格相關檢視表|
|  角色價格加成|• 資訊|• 使用中角色價格加成<br>• 角色價格加成相關檢視|
|  報價明細詳細資訊|• 專案資訊<br>• 專案快速建立|• 使用中報價明細詳細資訊<br>• 合併的報價明細詳細資料<br>• 報價明細詳細資料相關檢視表|
|  • 專案合約服務內容詳細資料|• 專案資訊<br>• 專案快速建立|• 合併的合約服務內容詳細資料<br>• 使用中合約服務內容詳細資料<br>• 合約服務內容詳細資料相關檢視表|
|  專案工作|• 資訊<br>• 新表單||
|  專案團隊成員|• 資訊<br>• 新表單|• 使用中專案團隊成員<br>• 專案團隊成員<br>• 專案團隊成員相關檢視表|
|  時間項目|• 資訊<br>• 建立時間項目|• 我依日期的時間項目<br>• 我本週的時間項目<br>• 供核准的時間項目|
|  帳目明細|• 資訊<br>• 快速建立|• 使用中帳目明細<br>• 帳目明細相關檢視表|
|  發票明細詳細資料|• 資訊<br>• 快速建立|• 使用中發票明細詳細資料<br>• 應收費發票交易<br>• 附贈發票交易<br>• 發票明細詳細資料相關檢視表<br>• 不應收費發票交易|
|  實際|• 資訊<br>• 使用中實際值|• 實際值相關檢視表|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>將可預約資源設定為定價維度

1. 在 Web 介面中，移至 **Project Service** > **設定** > **參數**。 在 **參數** 頁面的 **以金額為準的定價維度** 索引標籤上，注意索引標籤上的網格會顯示定價維度實體中的記錄。 
2. 將 **可預約資源** 新增至此定價維度清單做為 **msdyn_bookableresource**。 
3. 指示可預約資源用作定價維度所在的內容，並設定 **適用於成本** 和 **適用於銷售** 值。
4. 在 **維度類型** 欄位中，選取 **以金額為準**。 
5. 選取可預約資源的成本及銷售優先順序。 納入做為定價維度時，可預約資源通常會有最高的優先順序，因此將此設定為 **1**  (或 **0**，視優先順序計數方式而定) 可確保該行為。

## <a name="set-up-pricing-dimension-field-names"></a>設定定價維度欄位名稱

當 **角色價格** 表格中的定價維度欄位名稱與其在價格預設必須作用所在任何其他實體中的欄位名稱不同時，就必須讓定價維度記錄知道不同的名稱。    
至於可預約資源，**專案團隊成員** 實體的欄位名稱 (**msdyn_bookableresourceid**) 與其在 **角色價格** 實體上稱呼的名稱 (**msdyn_bookableresource**) 略微不同。 您必須讓 **msydn_bookableresource** 的定價維度記錄得知這一點。 
1. 若要這樣做，請按兩下 **定價維度** 網格中的列，以開啟 **msdyn_bookableresource** 的維度頁面。
2. 在維度頁面的 **相關** 索引標籤上，按一下 **定價維度欄位名稱**。

 ![[定價維度欄位名稱] 索引標籤。](media/PD-fieldname.png)

4. 在開啟的相關檢視表上，按一下 **新增定價維度欄位名稱**。

 ![新增定價維度欄位名稱。](media/Add-NewPD-fieldname.png)


這會開啟 **msdyn_bookableresource** 的 **新增定價維度欄位名稱** 頁面。 

5. 將 **msdyn_projectteam** 新增至 **實體邏輯名稱** 欄位，並將 **msdyn_bookableresourceid** 新增至 **欄位名稱** 欄位。 儲存記錄。

 ![新增定價維度欄位名稱表單。](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
