---
title: 檢閱專案與專案合約上的開立發票待辦項目
description: 此主題提供有關如何檢閱時間、費用及產品待辦項目的資訊，以及說明如何將這些待辦項目標示為已準備好開立發票。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150478"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>檢閱專案與專案合約上的開立發票待辦項目

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

當交易已準備好可以建立並處理發票時，該交易應標示 **已準備好開立發票**。 本主題說明可以建立的交易類型。

## <a name="review-the-time-and-material-billing-backlog"></a>檢閱時間和資料帳務待辦項目

專案的時間或費用項目已送出並獲核准時，PSA 會建立專案實際值。 如果專案和交易分類的組合已對應至時間和材料專案的合約服務內容，則該項目獲核准時，就會建立兩個實際值：

- 成本實際值 
- 未開單銷售實際值

未開單銷售實際值代表帳務待辦項目，且其帳單狀態必須設定為 **已準備好開立發票**。 建立專案發票時，標示為 **已準備好開立發票** 的未開單銷售實際值會複製到發票明細詳細資料。

若要檢閱時間和材料的帳務待辦項目，請移至 **銷售** \> **帳務** \> **時間和資料帳務待辦項目**。 選取所有已準備好開立發票的未開單銷售實際值，然後選取 **已準備好開立發票**。 這些實際值的帳單狀態會變更為 **已準備好開立發票**。

![時間和資料帳務待辦項目](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>檢閱產品帳務待辦項目

在 PSA 中，如果專案合約有產品型合約服務內容，每當為專案合約建立發票時，都會考慮這些服務內容來開立發票。 任何有合約服務內容標示為 **已準備好開立發票** 的產品都會複製到專案發票上做為專案發票明細。

若要檢閱產品的帳務待辦項目，請移至 **銷售**\>**帳務**\>**產品帳務待辦項目**。 選取所有已準備好開立發票的產品型合約服務內容，然後選取 **已準備好開立發票**。 這些服務內容的帳單狀態會變更為 **已準備好開立發票**。

![產品帳務待辦項目](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>檢閱固定價格合約上的帳單里程碑

每個具有固定價格帳務方式的專案合約服務內容都必須定義合約里程碑。 只有合約里程碑已標示為 **已準備好開立發票** 時，才能為這些合約里程碑開立發票。 

若要檢閱帳單里程碑，請移至 **銷售** \> **帳務**\>**固定價格里程碑**。 選取已準備好開立發票的里程碑，然後選取 **已準備好開立發票**。 這些里程碑的帳單狀態會變更為 **已準備好開立發票**。

![固定價格里程碑](media/FPBacklog.png)
