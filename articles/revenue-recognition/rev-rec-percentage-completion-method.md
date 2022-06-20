---
title: 固定價格營收估計值專案
description: 本文提供有關專案中固定價格營收的資訊。
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928376"
---
# <a name="fixed-price-revenue-estimate-projects"></a>固定價格營收估計值專案 

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

當您使用 Dynamics 365 Project Operations 中的下列屬性在 Microsoft Dataverse 上建立專案合約服務內容時，系統會自動建立固定價格營收估計值專案。 此專案中的資訊會根據下列項目而定：

  - 固定價格帳務方式。
  - 相關專案。
  - 在 **專案合約服務內容** 索引標籤上的 **發票清單** 索引標籤中，至少定義了一個里程碑。

## <a name="review-fixed-price-revenue-estimates-projects"></a>檢閱固定價格營收估計值專案
若要檢閱固定價格營收估計值專案，請完成下列步驟：

1. 在 Dynamics 365 Finance 環境中，移至 **專案管理與會計** > **專案** > **固定價格營收估計專案**。
2. 選取您要查看的專案，並按兩下 **估計專案識別碼** 以開啟該記錄，並審查專案的詳細資料。
3. 展開 **專案** 索引標籤。您會在 **選取的專案** 網格中看到一個專案。 系統會將此專案用做為預設專案，因為它是與專案合約服務內容相關聯的專案。 
4. 若要變更關聯，請選取其他專案，並將它們新增至 **選取的專案** 網格。 如果在此網格中選取多個專案，則會為所有選取的專案計算專案完成百分比和營收估計值。

  專案成本、營收設定檔、成本範本以及期間代碼可以手動設定。 如果不是手動設定，則這些值將預設為使用為專案成本和營收設定檔所設定規則在專案的第一次估計值計算。



[!INCLUDE[footer-include](../includes/footer-banner.md)]