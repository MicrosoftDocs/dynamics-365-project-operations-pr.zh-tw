---
title: 公司間開立開票概觀
description: 此主題提供專案的公司間開立發票的資訊與範例。
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287318"
---
# <a name="intercompany-invoicing-overview"></a>公司間開立開票概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

您的組織可能有多個會在專案中互相轉移產品與服務的部門、子公司及其他法律實體。 提供服務或產品的法律實體稱為 *貸方法律實體*。 接收服務或產品的法律實體稱為 *借方法律實體*。

下圖顯示典型案例，其中的兩個法律實體 Contoso Robotics USA (借方法律實體) 和 Contoso Robotics UK (貸方法律實體) 共享資源，為客戶 Adventure Works 交付專案。 在此案例中，Contoso Robotics USA 已簽約要交付工作給 Adventure Works。

![公司間開立開票](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations 使用以下流程來處理公司間交易：

1. 貸方法律實體的資源透過針對借方法律實體中的專案預約時間和費用，來記錄公司間時間或費用交易。
2. 時間和費用成本透過使用借方公司的單位成本價目表記錄在貸方公司中。
3. 公司間未開單銷售交易透過使用借方公司的單位成本價目表記錄在貸方公司中。
4. 未開單營收是使用專案合約銷售價目表在借方公司中進行記錄。 當記錄未開單營收時，可以向客戶收費。 客戶無需等到公司間發票處理完成。
5. 會在貸方公司中定期建立公司間客戶發票。 發票是手動建立的，或是使用週期自動程序建立。 可以為每個貸方法律實體建立單一發票，或依專案建立不同的發票。
6. 將公司間客戶發票過帳到貸方法律實體中時，將在借方法律實體中建立對應的擱置中廠商發票。 在過帳發票時，擱置中廠商發票中的成本將記錄至專案分類帳。

下圖顯示公司間開立發票，因其與會計事件相關且預期過帳到總帳。

![公司間流程](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>其他資源

- [設定公司間開立發票](configure-intercompany-invoicing.md)
- [記錄公司間交易](create-intercompany-transactions.md)
- [建立公司間客戶與廠商發票](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]