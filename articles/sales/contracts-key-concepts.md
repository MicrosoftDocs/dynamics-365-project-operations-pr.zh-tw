---
title: 專案合約 - 重要概念
description: 本主題提供有關 Project Operations 中專案合約重要概念的資訊。
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f87a29893ca3d9bec6fbd07dded66a282ff597c3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582930"
---
# <a name="concepts-unique-to-project-based-contracts"></a>專案型合約獨有的概念

_**適用於：** 資源/非庫存型案例適用的 Project Operations_



此主題提供在 Dynamics 365 Project Operations 中開始使用專案合約之前，需注意的重要概念：

## <a name="owning-company"></a>負責公司

負責公司是 Project management and accounting module forfrom Dynamics 365 Finance 中 Project Operations **專案管理與會計** 模組的法律實體。 負責公司代表對交易所產生之成本與營收負有責任的法律實體。

## <a name="contracting-unit"></a>合約單位

合約單位代表負責交付專案的部門或業務單位。 您可以設定每個合約單位的資源成本。 指定資源的資源成本時，您也可以為資源設定不同的成本費率。 此合約單位會向企業中的其他部門或業務單位借用這些資源。 資源的成本費率即稱為轉撥價格、資源借用或借調價格。 設定從其他部門借用資源的成本費率時，請使用出借部門的貨幣。

## <a name="cost-currency"></a>成本貨幣

成本貨幣是在畫面上用來報告成本的貨幣。 此貨幣是取自合約及專案上附加至 **合約單位** 欄位的貨幣。 您可以在專案上使用任何貨幣來記錄成本。 不過，顯示在畫面上時，會發生從記錄成本所用貨幣到專案成本貨幣之間的貨幣轉換。

因為 Common Data Service (CDS) 平台中的匯率無法即日生效，如果您更新貨幣匯率，畫面上的總計成本可能會隨時間改變。 不過，記錄於資料庫中的成本仍會保持不變，因為金額是以其開支所用的貨幣來儲存。

## <a name="sales-currency"></a>銷售貨幣

Project Operations 中的銷售貨幣是記錄和顯示估計及實際銷售金額所用的貨幣。 銷售貨幣也是開立交易發票給客戶所用的貨幣。 在專案合約上，預設會使用客戶或客戶記錄的銷售貨幣，而且可以在建立合約時變更。 當合約是以成交關閉報價的方式建立時，合約的貨幣會預設為報價的貨幣。

從頭開始建立專案合約時，無法編輯 **銷售貨幣** 欄位。 產品及專案價目表會根據合約上的這個貨幣來設定預設值。

與成本不同，銷售值只能以銷售貨幣來記錄。

## <a name="billing-method"></a>計費方式

專案通常有兩種類型的合約模型，固定費用型和耗用量型。 這些模型代表 Project Operations 中的帳務方式，其中有兩個可能的值：

- 時間和材料：基於耗用量的合約模型，其中每項產生的成本都是以對應的營收為背景來源。 隨著您估計或產生更多成本時，對應的估計和實際銷售也會增加。 在使用此帳務方式的合約服務內容上指定不得超過的限制，這會設定實際營收的上限。 估計營收不受不得超過的限制所影響。
- 固定價格：固定費用合約模型，表示銷售值將與產生的成本無關。 銷售值已固定，不會因為您估計或產生更多成本而改變。

## <a name="project-price-lists"></a>專案價目表

專案價目表是用來設定時間、費用及其他專案相關元件預設價格 (不是預設成本費率) 的價目表。 可以有多個價目表。 每個價目表都有其本身對於各自專案合約的日期時效性。 Project Operations 不支援專案價目表的有效日期範圍重疊。

因專案報價成交而建立專案合約時，會將專案價目表連同合約名稱及日期一起複製。 複製此資訊會建立此專案合約中專案元件的自訂定價。

## <a name="transaction-classes"></a>交易分類

Project Operations 支援四種類型的交易分類：

- 時間
- 費用
- 資料
- 費用

成本值和銷售值可以在 [時間]、[費用] 和 [材料] 交易分類上進行估計和列計。 服務費是營收專屬交易分類。

## <a name="work-entities-and-billing-entities"></a>工作實體和帳單實體

代表工作的實體是 [專案] 和 [工作]。 代表帳單相關事項的實體是 [合約服務內容]。 您可以將不同工作實體繫結至合約服務內容，藉此將這些實體繫結至帳單選項。

## <a name="multi-customer-deals"></a>多客戶交易

多客戶交易會有多個需要開立交易發票的客戶。 常見的範例包括：

- OEM 企業及其合作夥伴：合作夥伴和轉銷商會搭配一些加值服務 (通常涉及與客戶的特定交易) 來銷售產品。 OEM 願意為一部分專案提供融資。 

- 公共事業專案：多個當地政府部門同意資助專案，並依據先前議定的分攤額度來開立發票。 例如，學區或當地政府部門同意資助興建游泳池。

## <a name="invoice-schedules"></a>發票排程

發票排程是每個特定合約服務內容專屬的排程，而且自動發票開立功能必須有此排程才能正常運作。 發票排程是根據特定開始和完成日期以及發票週期所建立。 此排程用於設定自動發票建立程序時的合約階段中。 從報價建立專案合約時，發票排程會從報價複製到專案合約。

## <a name="changes-from-dynamics-365-sales-orders"></a>Dynamics 365 Sales 訂單發生的變更

Project Operations 中的合約是以 Dynamics 365 Sales 中的訂單為基礎所建置。 不過，在功能上有重要的偏差與變化。 合約有其本身的表單以及 UI 元素、商務規則、外掛程式中的商務規則，以及使其與訂單有所不同的用戶端指令碼。 因此，不要交替使用 Sales 訂單與 Project Operations 合約。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
