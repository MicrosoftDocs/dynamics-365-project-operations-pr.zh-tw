---
title: 使用交易類別做為定價維度
description: 本主題提供有關使用交易類別做為定價維度的資訊。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ce878665384b75fc44bba2d413217857e0ee467c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281873"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>使用交易類別做為定價維度

[!include [banner](../includes/psa-now-project-operations.md)]

本主題說明如何使用交易類別做為定價維度。 開始之前，如果尚未建立定價維度解決方案，就必須建立新的定價維度。 如果已經有定價維度解決方案，則可以在該解決方案中進行變更。 如果您沒有為組織建立新的定價維度解決方案，請完成[建立自訂欄位和實體](create-custom-fields-entities.md)主題中的程序。

## <a name="add-transaction-category-to-forms-and-views"></a>將交易類別新增至表單和檢視表
若要讓交易記錄類別在定價維度解決方案的 UI 中可見，您必須逐步瀏覽主要實體的所有表單和檢視表，並將這些欄位新增至這些實體的表單和檢視表中。
下表是一份需要以新欄位更新的預設表單及檢視表完整清單 (依實體列出)。 如果這些實體的自訂中有任何其他檢視表或表單，也請將新欄位新增至其中。

|  實體        | 表單     |檢視表        |
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

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>設定交易類別做為定價維度

1. 在 Web 介面中，移至 **Project Service** > **設定** > **參數**。 
2. 在 **參數** 頁面的 **以金額為準的定價維度** 索引標籤上，注意索引標籤上的網格會顯示 **定價維度** 實體中的記錄。
3. 將 **交易類別** 新增至此清單，並將 **適用於成本** 和 **適用於銷售** 欄位設定為 **是**。
4. 在 **維度類型** 欄位中，選取 **以金額為準**，然後選取與成本及銷售相關之 **交易類別** 的優先順序。


[!INCLUDE[footer-include](../includes/footer-banner.md)]