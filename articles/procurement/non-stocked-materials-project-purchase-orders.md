---
title: 使用專案採購單為專案訂購非庫存材料
description: 本文說明如何使用專案採購單為專案訂購非庫存材料。
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929802"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>使用專案採購單為專案訂購採購類別或非庫存材料

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

您組織中的採購部門可能會使用[採購單](/dynamics365/supply-chain/procurement/purchase-order-overview)來追蹤商品及服務訂單。 採購類別或非庫存材料的採購單可劃歸於專案。 開立這些採購單的發票會將成本記錄作專案的帳項。

## <a name="prerequisites"></a>先決條件
完成下列步驟，以啟用專案採購單功能。

1. 在 Dynamics 365 Finance 中，移至 **功能管理** 工作區。
2. 在功能清單中，尋找並選取 **在資源型/非庫存案例適用的 Project Operations 中啟用專案採購單** 功能。
3. 選取 **啟用**。
4. 設定非庫存材料和待處理廠商發票，如[設定非庫存材料和待處理廠商發票](configure-materials-nonstocked.md)中所述。
5. 設定採購類別，如[將採購類別與專案採購單及待處理廠商發票搭配使用](configure-procurement-categories.md)中所述。

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>從專案採購單清單建立專案採購單

1. 在 Finance 中，移至 **專案管理與會計** > **專案** > **所有專案**，並選取專案。
2. 在動作窗格 **管理** 索引標籤的 **新增** 群組中，選取 **項目工作** > **採購單**。
3. 在 **建立採購單** 頁面上，選取您要向其下單採購的廠商、輸入適當的資訊，然後選取 **確定**。
4. 在 **採購單** 頁面的 **採購單明細** 網格中，選取 **新增明細**。
5. 視情況而定，輸入項目編號或採購類別、數量、單位、單價以及其他資訊。

    > [!NOTE]
    > 只有採購類別、非庫存項目和服務才能與專案採購單搭配使用。 不支援庫存項目。

6. 視需要繼續新增項目或採購類別，並確認採購單。

    您可以建立產品收據並將其過帳，以記錄商品及服務收款。

    > [!NOTE]
    > 產品收據不會記錄到 Microsoft Dataverse 中的專案實際值，也不會影響專案的明細分類帳。

    廠商傳送採購單中項目與服務的發票之後，採購部門可以移至動作窗格上的 **發票** > **產生** > **發票** 來產生採購單的發票。 如需待處理廠商發票的詳細資訊，請參閱[使用待處理廠商發票購買非庫存材料](pending-vendor-invoices.md)。
