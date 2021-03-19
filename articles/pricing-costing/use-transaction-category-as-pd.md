---
title: 使用交易類別做為定價維度
description: 本主題提供有關如何使用 [交易類別] 欄位做為定價維度的資訊。
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c84d3aaf7cd7577dcd15311f225c82b538586445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274583"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>使用交易類別做為定價維度


_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_


本主題說明如何使用 **交易類別** 欄位做為定價維度。 

## <a name="prerequisites"></a>先決條件
在您完成本主題中的步驟之前，您必須有一個新的定價維度解決方案供您的組織使用。 如果尚未建立一個，請參閱[將自訂欄位及實體建立為定價維度](create-custom-fields-entities-pricing-dimensions.md)。

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>將交易類別欄位新增至表單和檢視表
若要讓 **交易類別** 欄位顯示在定價維度解決方案中，您必須將欄位做為實體新增至所有表單和檢視表。

下表依實體列出所有現成可用的表單和檢視表。 您也必須將新欄位新增至自訂實體中的任何其他表單或檢視表。

|  Entity        | 表單     |檢視表        |
| ------------------------------|---------------------------------|----------------------------------|
|  角色價格| 資訊 |- 使用中資源類別價格<br> - 資源類別價格相關 |
|  角色價格加成| 資訊|- 使用中角色價格加成<br>- 角色價格加成相關 |
|  報價明細詳細資料|- 專案資訊<br>- 專案快速建立| - 使用中報價明細詳細資訊<br>- 合併的報價明細詳細資料<br>- 報價明細詳細資料相關 |
|  專案合約服務內容詳細資料|- 專案資訊<br>- 專案快速建立|- 合併的合約服務內容詳細資料<br>- 使用中合約服務內容詳細資料<br>- 合約服務內容詳細資料相關 |
|  專案工作|- 資訊<br>- 新表單| &nbsp; |
|  專案團隊成員|- 資訊<br>- 新表單|- 使用中專案團隊成員<br>- 專案團隊成員<br>- 專案團隊成員相關 |
|  時間項目|- 資訊<br>- 建立時間項目|- 我依日期的時間項目<br>- 我本週的時間項目<br>- 供核准的時間項目|
|  帳目明細|- 資訊<br>- 快速建立|- 使用中帳目明細<br>- 帳目明細相關|
|  發票明細詳細資料|- 資訊<br>- 快速建立|- 使用中發票明細詳細資料<br>- 應收費發票交易<br>- 附贈發票交易<br>- 發票明細詳細資料相關 <br>- 不應收費發票交易|
|  實際|- 資訊<br>- 使用中實際值| 實際值相關 |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>設定交易類別欄位做為定價維度

1. 移至 **設定** > **參數**。 
2. 在 **參數** 頁面的 **以金額為準的定價維度** 索引標籤上，確認網格會顯示 **定價維度** 實體中的記錄。
3. 將 **交易類別** 新增至此清單，並將 **適用於成本** 和 **適用於銷售** 欄位設定為 **是**。
4. 在 **維度類型** 欄位中，選取 **以金額為準**，然後選取與成本及銷售相關之 **交易類別** 的優先順序。


[!INCLUDE[footer-include](../includes/footer-banner.md)]