---
title: 使用新的定價維度來更新外掛程式屬性
description: 此主題提供有關如何更新定價維度的外掛程式屬性的資訊。
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643208"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>使用新的定價維度來更新外掛程式屬性

此主題提供有關如何更新定價維度的外掛程式屬性的資訊。

> [!NOTE]
> 此主題只適用於 Dynamics 365 Project Operations 中的報價及合約功能。

## <a name="prerequisites"></a>先決條件
在您完成此主題中的步驟之前，您必須已完成下列主題中的程序：

  - [建立自訂欄位和實體](create-custom-fields-entities-pricing-dimensions.md) 
  - [將自訂欄位新增至價格設定與交易實體](add-custom-fields-price-setup-transactional-entities.md)
  - [將自訂欄位設定為定價維度](set-up-custom-fields-pricing-dimensions.md)。 
  
如果您尚未完成這些程序，請先完成然後再回到本主題。

## <a name="register-a-plug-in"></a>註冊外掛程式
當報價明細詳細資料建立於專案報價明細的 **報價明細** 頁面時，系統會建立兩個估計明細。 其中一個明細用於成本面估計，另一個用於銷售面估計。 這同樣適用於專案合約服務內容。

對成本面欄位數量或欄位進行變更時，銷售面也會進行該變更。 這是可能的，因為 Quotelinedetail 和 contractline 詳細資料實體的 PreOperation 外掛程式會將成本面的特定屬性連接至交易的銷售面。 如果您需要對銷售面的定價維度值所做的變更也要在成本面進行，在變更定價維度後，必須重新註冊下列外掛程式。

以下是要更新並重新註冊的外掛程式：

- PreOperationContractLineDetailUpdate - **更新 msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **更新 msdyn_quotelinetransaction**

請完成下列步驟，更新並重新註冊外掛程式。

1. 開啟 **PluginRegistrationTool**，並連接至您的 Project Operations Dataverse 環境。
2. 選取 **搜尋**，然後輸入要更新之外掛程式的前幾個字母。
3. 找到外掛程式後，選取該外掛程式，然後選取 **在主要表單上選取**。
4. 選取 **更新 msdyn_orderlinetransaction** 步驟、按一下滑鼠右鍵，然後選取 **更新**。
5. 在 **更新** 對話方塊頁面中，選取篩選屬性中的省略符號 (**...**)。
6. 篩選屬性視窗隨即開啟，並提供實體和定價維度中的所有屬性清單。 選取定價維度屬性的核取方塊。
7. 選取 **確定** 關閉頁面，然後選取 **更新步驟**。
8. 對第二個外掛程式 **PreOperationQuoteLineDetail** 重複步驟 2 到 7。 對第二個外掛程式，您需更新 **msdyn_quotelinetransaction 的更新** 步驟。
9. 關閉 **PluginRegistrationTool**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]