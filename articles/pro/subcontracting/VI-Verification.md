---
title: 使用核准的實際值驗證廠商發票
description: 本文說明 Microsoft Dynamics 365 Project Operations 如何讓專案經理透過已在轉包商執行工作並記錄時間時核准的實際值，以及專案團隊成員所使用的費用和材料來驗證廠商發票。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7bf48dd17063daece5df3ce44c0375eec3dc3cae
ms.sourcegitcommit: 49c2a668b8d7bf0acb9e9b0bb44687e6d3dcaa8c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/28/2022
ms.locfileid: "9204164"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>使用核准的實際值驗證廠商發票

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

Microsoft Dynamics 365 Project Operations 可讓專案經理以下列方式驗證廠商發票明細：

- 使用廠商發票明細上的 **驗證狀態** 欄位。
- 如果廠商發票明細參考轉包合約服務內容，請將轉包商活動中的成本實際值連結至這些廠商發票明細。 此連結是將成本實際值與廠商發票明細進行比對所建立。

    > [!NOTE]
    > 雖然可以針對未參考轉包合約的廠商發票明細追蹤驗證狀態，但是無法將成本實際值連結至這些廠商發票明細。

## <a name="verification-status"></a>驗證狀態

廠商發票明細上的 **驗證狀態** 欄位會指示該驗證狀態。 支援下列狀態：

1. 未開始
2. 進行中
3. 完成

可以編輯驗證狀態為 **未開始** 的廠商發票明細。

無法再編輯驗證狀態為 **進行中** 的廠商發票明細。 對於參考轉包合約的廠商發票明細，當第一個成本實際值符合廠商發票明細時，驗證狀態立即自動設定為 **進行中**。

無法再編輯驗證狀態為 **完成** 的廠商發票明細。 當廠商發票上所有的明細都有此驗證狀態時，即可確認此廠商發票。

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>將成本實際值與廠商發票明細進行比對

比對成本實際值有助於對廠商發票明細進行驗證程序。 若要將成本實際值與廠商發票明細進行比對，請執行下列步驟。

1. 開啟廠商發票明細，並選取 **不相符的成本實際值** 索引標籤。網格會顯示與廠商發票明細一樣參考相同轉包合約服務內容的成本實際值清單。
2. 選取一個或多個成本實際值，然後在網格上方的工具列中選取 **比對**。 系統會驗證選取的成本實際值是否可以比對相符。 通過驗證後，成本實際值會連結至廠商發票明細。

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>用於將成本實際值連結至廠商發票明細的驗證準則

進行比對程序時，只有在下列條件都符合時，才能建立成本實際值與廠商發票明細之間的連結：

- 每個所選成本實際值的 **調整狀態** 欄位都必須為空白。 換言之，進行回收、核准取消或更正帳目程序時，成本實際值不能已經取代為其他成本實際值。
- 下列欄位的值在廠商發票明細與所選成本實際值之間比對相符。 如果未在廠商發票明細上設定任何欄位，則不考慮將其進行比對。

    - 專案合約
    - 專案合約服務內容
    - 交易分類
    - 專案
    - 工作
    - 資源類別
    - 交易類別
    - 產品
    - 轉包合約服務內容
    - 可預約資源

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>取消成本實際值與廠商發票明細的相符對應

取消成本實際值的相符對應也可以藉由允許移除先前已建立的連結，協助您對廠商發票進行驗證程序。 成本實際值只能與驗證狀態為 **進行中** 的廠商發票明細取消相符對應。 若要取消成本實際值與廠商發票明細的相符對應，請執行下列步驟。

1. 開啟廠商發票明細，並選取 **相符的成本實際值** 索引標籤。網格會顯示參考廠商發票明細的成本實際值清單。
2. 選取一個或多個成本實際值，然後在網格上方的工具列中選取 **取消相符對應**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
