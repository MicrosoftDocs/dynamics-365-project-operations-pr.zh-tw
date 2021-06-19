---
title: 更新外掛程式屬性以包含新的定價維度
description: 此主題提供有關更新定價維度外掛程式屬性的資訊。
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
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
ms.openlocfilehash: b0d50733340f277453f4ef5b52bdd3ee089449cd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012801"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>更新外掛程式屬性以包含新的定價維度

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> 如果您沒有使用 Project Service Automation (PSA) 報價和合約功能，可略過本主題。

本主題假設您已完成[建立自訂欄位和實體](create-custom-fields-entities.md)、[將自訂欄位新增至價格設定與交易實體](field-references.md)以及[將自訂欄位設定為定價維度](set-up-pricing-dimensions.md)主題中的程序。 如果您尚未完成這些程序，請返回並加以完，然後再回到本主題。

在專案報價明細的 **報價明細** 頁面上建立報價明細詳細資料後，系統會在背景中建立兩個估計明細，其中一個明細用於成本面估計，另一個用於銷售面估計。 這同樣適用於專案合約服務內容。

對成本面欄位數量或欄位進行變更時，該變更會傳播至銷售面。 這可能是因為下列外掛程式必須在變更定價維度後重新註冊的緣故。

- PreOperationContractLineDetailUpdate - 更新 **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - 更新 **msdyn_quotelinetransaction**.

下列步驟將引導您逐步完成註冊外掛程式的程序。

1. 開啟 **PluginRegistrationTool** 並連接至您的線上執行個體。
2. 按一下 **搜尋**，然後搜尋要更新的外掛程式。

 ![搜尋樹狀結構的螢幕擷取畫面](media/PRT-1.png)

3. 找到外掛程式後，選取該外掛程式，然後按一下 **在主要表單上選取**。

4. 選取要更新外掛程式的步驟，按一下滑鼠右鍵，然後選取 **更新**。

 ![要更新的外掛程式螢幕擷取畫面](media/PRT-2.png)
 
5. 在更新視窗中，按一下篩選屬性中的省略符號 (**...**)。

 ![更新現有步驟設定資訊的螢幕擷取畫面](media/PRT-3.png)
 
6. 選取定價屬性核取方塊。

 ![螢幕擷取畫面顯示定價屬性的核取方塊選擇](media/PRT-4.png)

7. 按一下 **確定** 關閉頁面，然後選取 **更新步驟**。

 ![螢幕擷取畫面顯示 [更新步驟] 按鈕](media/PRT-5.png)
 
8. 對第二個外掛程式 **PreOperationQuoteLineDetail - msdyn_quotelinetransaction 的更新** 重複此程序。

9. 關閉外掛程式註冊工具



[!INCLUDE[footer-include](../includes/footer-banner.md)]