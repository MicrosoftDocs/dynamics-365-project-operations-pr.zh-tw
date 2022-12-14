---
title: 專案型報價獨有的概念
description: 本文提供有關 Microsoft Dynamics 365 Project Operations 中專案報價的資訊。
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824317"
---
# <a name="concepts-unique-to-project-based-quotes"></a>專案型報價獨有的概念

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

開始使用 Microsoft Dynamics 365 Project Operations 中的專案報價之前，您應該先了解下列重要概念。

## <a name="owning-company"></a>負責公司

擁有公司代表負責交付專案的法律實體。 報價中的客戶應是該法律實體在財務和營運應用程式中的有效客戶。 擁有公司的貨幣必須與專案型報價上所選合約單位的貨幣相符。

## <a name="contracting-unit"></a>合約單位

合約單位代表負責交付專案的部門或業務單位。 您可以設定每個合約單位的資源成本。 指定合約單位中資源的資源成本時，您可以針對合約單位所借用的資源或企業中的其他部門或業務單位，設定不同的成本費率。 這些成本費率即稱為轉撥價格、資源借用或借調價格。 設定從其他部門借用資源的成本時，您可以選擇以出借部門的貨幣來設定成本費率。

## <a name="cost-currency"></a>成本貨幣

Project Operations 中的成本貨幣是用來報告成本的貨幣。 此貨幣是取自報價、合約及專案中附加至 **合約單位** 欄位的貨幣。 專案的成本可以用任何貨幣來記錄。 不過，從記錄成本所用貨幣到專案的成本貨幣之間會進行貨幣轉換。

因為 Dataverse 平台中的匯率無法即日生效，如果您更新貨幣匯率，畫面上的總計成本可能會隨時間改變。 不過，資料庫中所記錄的成本仍會保持不變，因為金額是以其開支所用的貨幣來儲存。

## <a name="sales-currency"></a>銷售貨幣

Project Operations 中的銷售貨幣是用來記錄和顯示估計及實際銷售金額的貨幣。 這也是開立交易發票給客戶所用的貨幣。 在專案報價中，預設銷售貨幣是在顧客或客戶記錄中所設定，並且可以在建立報價時變更。 不過，儲存報價後，就無法變更銷售貨幣。 預設產品及專案價目表是根據報價的銷售貨幣來設定。

與成本不同，銷售值 **只能** 以銷售貨幣來記錄。

## <a name="billing-method"></a>帳務方式

專案通常會有基於固定費用和耗用量的合約模型。 在 Project Operations 中，專案的合約模型是以帳務方式表示。 帳務方式有兩個值：時間和材料以及固定價格。

- **時間和材料**：這是基於耗用量的合約模型，其中每項產生的成本都有對應的營收做為背景來源。 隨著您估計或產生更多成本時，對應的估計和實際銷售也會增加。 您可以在使用此帳務方式的報價明細上指定不得超過的限制。 如此一來，您就可以設定實際營收的上限。 估計營收不受不得超過的限制所影響。
- **固定價格**：固定費用合約模型，其中銷售值與產生的成本無關。 銷售值已固定，不會因為您估計或產生更多成本而改變。

## <a name="project-price-lists"></a>專案價目表

專案價目表是用來輸入時間、費用及其他專案相關元件預設價格 (而非預設成本費率) 的價目表。 可以有多份價目表，而每一份價目表都可以為個別專案報價提供其本身的有效日期範圍。 Project Operations 對於專案價目表不支援重疊的有效日期範圍。

## <a name="product-price-lists"></a>產品價目表

產品價目表是在報價上用來輸入產品型明細預設價格 (而非預設成本費率) 的價目表。 每個報價只有一份產品價目表。

## <a name="transaction-classes"></a>交易分類

Project Operations 支援四種類型的交易分類：

- 時間
- 費用
- 資料
- 費用

成本值和銷售值可以根據 **時間**、**費用** 和 **材料** 交易分類進行估計和列計。 **服務費** 是營收專屬交易分類。

## <a name="work-entities-and-billing-entities"></a>工作實體和帳單實體

[專案] 和 [工作] 是表示工作的實體。 [報價明細] 和 [合約服務內容] 是表示帳單的實體。 您可以建立不同工作實體與 [報價明細] 及 [合約服務內容] 的關聯，藉此將這些實體連結至帳單選項。

## <a name="multi-customer-deals"></a>多客戶交易

每張發票有多個客戶時，就會發生多客戶交易。 以下是一些一般範例：

- **原始設備製造商 (OEM) 企業及其合作夥伴**：合作夥伴和轉銷商會銷售包含加值服務的產品。 與客戶進行交易時，OEM 通常願意為部分專案提供融資。
- **公共事業專案**：多個當地政府部門同意資助專案，並依據先前議定的分攤額度來開立發票。 例如，學區和城市或當地政府部門同意資助興建游泳池。

## <a name="invoice-schedules"></a>發票排程

發票排程是每個報價明細特定的排程，並且為選用項目。 發票排程是根據特定開始和結束日期以及發票週期所建立。 這些排程用於設定自動發票建立程序時的合約階段中。 在報價階段中，發票排程是選用項目。 如果在報價階段建立這些排程，則會將其複製到專案報價成交時所建立的專案合約。

## <a name="differences-from-dynamics-365-sales-quotes"></a>與 Dynamics 365 Sales 報價的差異

Project Operations 報價是建立在 Dynamics 365 Sales 報價的基礎上。 不過，您會在功能上注意到一些重要差異：

- Project Operations 報價有兩種不同類型的明細：一個用於專案，一個用於產品。
- Project Operations 報價有其本身的頁面和使用者介面 (UI) 元素、商務規則、外掛程式中的商務規則，以及使其與 Sales 報價有所不同的用戶端指令碼。
- 在 Sales 中，您可以將多個訂單附加至單一銷售報價。 在 Project Operations 中，只能將一個專案合約附加至專案報價。
- 贏得銷售報價時，相關商機可以保持開啟。 贏得專案報價後，便會關閉相關商機。
- 銷售報價不包含專案報價所包含的一些欄位與概念。 這些欄位包括 **承包單位**、**客戶經理** 和 **帳單連絡人**。
- 銷售報價與專案報價是由選項組型 **類型** 欄位來識別。 就銷售報價而言，此欄位的值是 **項目型**。 至於專案報價，其值為 **工作型**。

因為這些差異，不建議您以可互換的方式使用 Sales 報價與 Project Operations 報價。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
