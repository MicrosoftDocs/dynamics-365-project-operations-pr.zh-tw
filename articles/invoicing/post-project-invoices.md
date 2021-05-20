---
title: 發票開立程序概觀
description: 本主題提供在資源/非庫存型案例適用的 Project Operations 中開立發票的程序概觀。
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9dc424cf69abfccc10bf551272a14e5cefb3dff0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275797"
---
# <a name="invoicing-process-overview"></a>發票開立程序概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

資源/非庫存型案例適用的 Project Operations 提供同時配合專案經理與應收帳款人員/專案會計師需求所訂製的完整功能。 在發票開立程序中，專案經理負責管理專案帳務積存，而應收賬款人員/專案會計師則建立合規且準確的客戶面向發票憑證。

![發票開立流程圖](./media/invoicing-flow.png)

專案合約服務內容會定義相關聯專案交易的帳務方式。 當專案經理核准時間和費用交易時，系統會在 **專案實際值** 實體中記錄這些交易，並將資訊傳送至 Dynamics 365 Finance 中的 **專案管理與會計** 模組。 專案會計師接著使用 [Project Operations 整合帳目](../project-accounting/project-operations-integration-journal.md)對這些記錄進行審查和過帳。 此帳目包含專案實際值的重要會計詳細資料，例如帳單、銷售稅群組、帳單項目銷售稅群組和財務維度。

專案經理可以在[時間和材料帳務積存](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog)中使用時間和材料帳務方式，以及在[固定價格里程碑](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones)中使用固定價格帳務方式，來審查未開單銷售交易。 這些檢視表可讓您篩選並選取需要包含在下一個帳單週期中的交易，然後將訊息交易標示為 **已準備好開立發票**。

您可以[手動建立預估發票](../proforma-invoicing/create-manual-proforma-invoice.md)，或使用[週期程序](../proforma-invoicing/configure-automated-invoice-creation.md)。 專案經理可以視需要[調整草稿預估發票](../proforma-invoicing/manage-proforma-invoice.md)，然後確認該發票。

確認的預估發票會傳送至 Finance 中的 **專案管理與會計** 模組。 專案會計師會對專案發票提案進行格式化和更新，然後將此憑證過帳並加以列印。 已過帳的專案發票會記錄在總帳以及客戶和專案的子分類帳中。


[!INCLUDE[footer-include](../includes/footer-banner.md)]