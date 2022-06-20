---
title: 開立廠商發票- 概念和建立
description: 本文說明廠商發票的概念、使用案例，以及在 Microsoft Dynamics 365 Project Operations 中建立廠商發票的方式。
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911448"
---
# <a name="vendor-invoicing---concept-and-creation"></a>開立廠商發票- 概念和建立

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

Microsoft Dynamics 365 Project Operations 中的廠商發票功能，可用來記錄廠商在專案上交付服務和/或材料的成本。

當服務和/或材料轉包給廠商時，轉包合約代表與該廠商的契約協議。 當廠商提供服務，或材料經接收並用於專案工作的時，會在專案上記錄成本。 廠商會定期傳送經過驗證且符合專案上所記錄成本的發票。 完成驗證程序後，確認並發放廠商發票以進行付款。

## <a name="scenarios-for-use"></a>使用案例

Project Operations 中的廠商發票可以用來支援兩種不同的案例。

### <a name="customers-use-the-full-subcontracting-experiences"></a>客戶使用完整的轉承包體驗

廠商發票體驗提供一種方法來驗證參考轉包元件的時間項目、材料使用情況和費用項目，並將這些項目與廠商發票明細比對。 此程序可用於驗證廠商發票明細的正確性。 完成驗證程序並確認廠商發票之後，應用程式將會沖回由核准的時間、費用和材料使用記錄所記錄的實際值，並使用廠商發票明細建立新的成本實際值。

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>客戶不使用完整的轉承包體驗，但想要在 Project Operations 中對專案中的成本有整合的檢視

如果您要在協力廠商系統中追蹤轉包合約程序，則可以建立未參考轉包合約的廠商發票，以將成本從該協力廠商系統記錄到 Project Operations。 如此一來，專案經理對指定專案中的所有成本就可以有單一整合的檢視。

## <a name="creation-of-vendor-invoices-in-project-operations"></a>在 Project Operations 中建立廠商發票

有兩種方式可以建立廠商發票：

- 從廠商發票清單頁面或單一廠商發票的詳細資料頁面
- 從轉包合約清單頁面或單一轉包合約的詳細資料頁面

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>從廠商發票清單頁面或詳細資料頁面建立

1. 移至 **採購** \> **廠商發票**。
2. 在廠商發票清單頁面或單一廠商發票的詳細資料頁面上，選取 **新增** 以建立新的廠商發票。

以這種方式建立的廠商發票也可以參考轉包合約。

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>從轉包合約清單頁面或詳細資料頁面建立

1. 移至 **採購** \> **轉包合約**。
2. 選取一個或多個轉包合約。
3. 在轉包合約清單頁面或單一轉包合約的詳細資料頁面上，選取 **建立廠商發票** 以建立新的廠商發票。

您選取的每個轉包合約都會建立一個狀態為 **草稿** 的新廠商發票。

以這種方式建立的廠商發票一律會參考廠商發票標題上的轉包合約。 轉包合約中每項具有時間和材料帳務方式的明細，都會導致在廠商發票上建立一項明細。 轉包合約中每項具有固定價格帳務方式的明細，都會導致在廠商發票上針對狀態為 **已準備好開立發票** 的每個轉包合約服務內容里程碑建立一項明細。

下列欄位和相關記錄會從轉包合約複製到廠商發票的標題：

- 廠商。
- 相關價目表會複製到廠商發票做為價目表。
- 貨幣。
- 合約單位。
- 付款條件。

對於時間和材料轉包合約服務內容，下列欄位和相關記錄會從轉包合約服務內容複製到廠商發票明細：

- 轉包合約和轉包合約服務內容參考
- 交易分類
- 角色
- 交易類別
- 產品欄位
- 專案
- 工作
- 可預約資源

對於固定價格轉包合約服務內容，下列欄位會從轉包合約服務內容和轉包合約服務內容里程碑複製到廠商發票明細：

- 轉包合約和轉包合約服務內容參考。
- 交易分類。 根據預設，此值會是 **里程碑**。
- 里程碑名稱和金額會從相關轉包合約服務內容里程碑複製過來。
- 使用者可以選取廠商發票明細上的專案和工作。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
