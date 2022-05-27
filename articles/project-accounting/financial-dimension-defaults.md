---
title: 財務維度預設值
description: 本主題提供有關如何設定財務維度預設值的資訊。
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9f43fed57a1411a55dcd7929f34e87aed136a6b5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579480"
---
# <a name="financial-dimension-defaults"></a>財務維度預設值

_**適用於：** 資源/非庫存型案例適用的 Project Operations_



Dynamics 365 Project Operations 使用 Dynamics 365 Finance 中的[財務維度](/dynamics365/finance/general-ledger/financial-dimensions)架構，提供關於專案明細分類帳和總帳交易的其他見解。

您可以在客戶、專案資金來源、里程碑、專案合約服務內容或專案上設定預設財務維度。

## <a name="define-default-financial-dimensions-for-a-customer"></a>定義客戶的預設財務維度

客戶維度預設值是在 Finance 中進行指定。 請完成下列步驟，以設定維度預設值。

1. 移至 **應收帳款** > **客戶** > **所有客戶**。
2. 在 **客戶** 頁面的 **財務維度** 索引標籤中，設定特定客戶的財務維度值。

## <a name="define-default-financial-dimensions-for-project-contracts"></a>定義專案合約的預設財務維度

專案合約是在 Common Data Service (CDS) 中建立並進行維護。 專案合約的會計屬性是在 Finance 的 **專案管理與會計** 模組進行設定。

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>設定專案資金來源的財務維度

1. 移至 **專案管理與會計** > **專案** > **專案合約**。
2. 選取要更新的記錄，然後選取 **專案合約** 索引標籤中的 **顯示預設會計**。
3. 展開 **相關資訊**，然後選取 **資金來源** 索引標籤。
4. 設定財務維度預設值。 請注意，預設會使用客戶帳戶中的財務維度。

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>設定專案合約服務內容的財務維度

1. 移至 **專案管理與會計** > **專案** > **專案合約**。
2. 選取要更新的記錄，並選取 **專案合約** 索引標籤中的 **顯示預設會計**。
3. 展開 **相關資訊**，然後選取 **合約服務內容** 索引標籤。
4. 設定財務維度預設值。 財務維度預設值可適用，並且只能與固定價格 (里程碑) 合約服務內容搭配使用。

這些預設值是在相關專案記帳交易和發票明細上使用。

## <a name="define-default-financial-dimensions-for-projects"></a>定義專案的預設財務維度

專案是在 CDS 中建立並進行維護。 專案的會計屬性是在 Finance 的 **專案管理與會計** 模組進行設定。

1. 移至 **專案管理與會計** > **專案** > **所有專案**。
2. 選取要更新的記錄，並選取 **專案** 索引標籤中的 **顯示預設會計**。
3. 展開 **相關資訊**，然後選取 **設定** 索引標籤。
4. 設定財務維度預設值。 請注意，預設會使用客戶帳戶中的財務維度。 如果專案與包含多個專案合約客戶的合約服務內容相關聯，則會使用主要客戶來設定預設財務維度。

專案預設財務維度會在 **Project Operations 整合帳目** 和相關專案發票明細上用來設定時間、費用及服務費交易的帳目明細預設值。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
